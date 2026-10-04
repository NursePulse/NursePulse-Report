# Capítulo VII: DevOps Practices

## 7.1. Continuous Integration

### 7.1.1. Tools and Practices.

El equipo utiliza un conjunto de herramientas de pruebas automatizadas para asegurar que cada cambio de código mantenga la calidad y el comportamiento esperado antes de integrarse a las ramas principales de cada repositorio (Backend, Frontend y Mobile).

| Herramienta | Tipo | Descripción | Propósito |
| :--- | :--- | :--- | :--- |
| **JUnit 5** | Framework de pruebas unitarias (TDD) | Incluido mediante `spring-boot-starter-test`, se usa para probar entidades de dominio, servicios de aplicación y recursos REST del backend (Spring Boot). | Verificar que las unidades de lógica de negocio (agregados, command services, validaciones) se comporten como se espera. |
| **Mockito** | Herramienta de simulaciones (TDD) | Se usa en pruebas como `UserCommandServiceImplTest` y `AuditLogsControllerTest` para simular repositorios y servicios colaboradores sin depender de la base de datos real. | Aislar la unidad bajo prueba de sus dependencias externas. |
| **Vitest** | Framework de pruebas unitarias (Frontend) | Ejecutado mediante el builder `@angular/build:unit-test` de Angular, corre las pruebas de componentes, stores y assemblers del Frontend Web Application. | Validar la lógica de los componentes standalone, signals y stores de Angular antes de integrarlos. |
| **flutter test / flutter analyze / dart format** | Pruebas y análisis estático (Mobile) | `flutter test` ejecuta 21 pruebas unitarias y de widgets de la aplicación móvil; `flutter analyze` aplica las reglas de `flutter_lints`; `dart format --set-exit-if-changed` verifica el formato del código. Los tres son pasos del job `Verify Flutter`. | Validar el registro y el inicio de sesión de la app móvil y mantener un código consistente. Son pasos obligatorios: si fallan, el pipeline se detiene. |
| **ESLint** (`angular-eslint`) | Análisis estático (Frontend) | Se ejecuta con `npm run lint` dentro del pipeline del Frontend; revisa el código TypeScript y las plantillas de Angular. | Detectar problemas de calidad y malas prácticas sin ejecutar el código. Corre en modo informativo (`continue-on-error`), por lo que sus hallazgos no bloquean el pipeline. |
| **Lighthouse** | Auditoría de calidad web (Frontend) | Se ejecuta con `npx lighthouse` en el pipeline del Frontend contra la página de inicio de sesión desplegada en Vercel y genera un reporte JSON y HTML. | Medir rendimiento, accesibilidad, buenas prácticas y SEO de la aplicación en producción. Es informativo y no bloquea el pipeline. |
| **GitHub Actions** | Orquestador de CI/CD | Ejecuta automáticamente los pipelines de build y pruebas en cada repositorio (Backend, Frontend, Mobile) ante cada `push`/`pull request`. | Automatizar la integración continua sin depender de ejecución manual. |

**Prácticas:**

- **Feature Branching**: la convención del proyecto es desarrollar cada funcionalidad en una rama `feature/*` independiente (ver Capítulo V, sección 5.1.2) e integrarla mediante Pull Request. En la práctica se aplicó en parte de los cambios; en las etapas finales muchos commits se publicaron directamente a la rama principal. Desde el 3 de octubre de 2026 la rama de producción del Backend (`deploy/render-docker`) ya no admite `push` directo y exige Pull Request (ver Capítulo VI, sección 6.2.2).
- **Conventional Commits**: el equipo adoptó el estándar `tipo(scope): descripción` (`feat`, `fix`, `docs`, `test`, `ci`, etc.) para identificar rápidamente el propósito de cada cambio. No se aplicó de forma uniforme: al 3 de octubre de 2026, y sin contar los commits de fusión, lo siguen 19 de 27 commits recientes de la rama `deploy/render-docker` del Backend, 15 de 28 del Frontend, 13 de 15 de Mobile y 1 de 17 de la Landing Page.
- **Build en cada integración**: el pipeline de CI se ejecuta en cada `push` y `pull request` hacia la rama principal. Es una condición técnicamente forzada únicamente en `deploy/render-docker` del Backend, donde el check `build-and-test` debe finalizar en éxito para poder fusionar. En `main` del Backend, del Frontend, de Mobile y de Landing no hay reglas de protección, por lo que un cambio puede integrarse aunque el pipeline falle (ver Capítulo VI, sección 6.2.2).

### 7.1.2. Build & Test Suite Pipeline Components.

Cada uno de los tres repositorios de código de NursePulse cuenta con su propio workflow de GitHub Actions, disparado en cada `push` y `pull request` hacia sus ramas principales (en Mobile, también hacia la rama `test`):

**Backend CI** (`Backend-NursePulse/.github/workflows/ci.yml`)

| Paso | Herramienta | Descripción |
| :--- | :--- | :--- |
| Checkout | `actions/checkout@v4` | Descarga el código fuente del repositorio. |
| Set up JDK | `actions/setup-java@v4` (Temurin 26) | Configura el entorno de ejecución de Java, con caché de dependencias Maven. |
| Build and run tests | `./mvnw -B clean verify` | Compila el proyecto y ejecuta la suite completa de pruebas unitarias e de integración (actualmente 63 pruebas, ver Capítulo VI sección 6.1). |

**Frontend CI** (`Application-Web-Nurse-Pulse/.github/workflows/ci.yml`)

| Paso | Herramienta | Descripción |
| :--- | :--- | :--- |
| Checkout | `actions/checkout@v4` | Descarga el código fuente del repositorio. |
| Set up Node | `actions/setup-node@v4` (Node 22.x) | Configura el entorno de ejecución de Node.js, con caché de dependencias npm. |
| Install dependencies | `npm ci` | Instala las dependencias de forma reproducible según `package-lock.json`. |
| Lint | `npm run lint` (ESLint) | Análisis estático del código. Tiene `continue-on-error: true`: informa hallazgos pero no detiene el pipeline. |
| Run unit tests | `npm test` (Vitest) | Ejecuta las pruebas unitarias de componentes, stores y servicios de Angular. |
| Build | `npm run build` (`ng build`) | Genera el build de producción, validando que no existan errores de compilación de TypeScript/Angular. |
| Lighthouse audit | `npx lighthouse` | Audita la página `/sign-in` desplegada en Vercel y genera un reporte JSON y HTML. Tiene `continue-on-error: true`. |
| Upload Lighthouse report | `actions/upload-artifact@v4` | Publica el reporte como artifact `lighthouse-report` del run, descargable desde la pestaña Actions de GitHub. |

**Mobile CI/CD** (`MultiPlatform-App-NursePulse/.github/workflows/ci.yml`)

El workflow tiene dos jobs. El primero, `Verify Flutter`, corre en todo `push` y `pull request`:

| Paso | Herramienta | Descripción |
| :--- | :--- | :--- |
| Checkout | `actions/checkout@v4` | Descarga el código fuente del repositorio. |
| Set up Java | `actions/setup-java@v4` (Temurin 17) | Configura el JDK requerido por la compilación de Android. |
| Set up Flutter | `subosito/flutter-action@v2` (3.47.2, canal stable) | Configura el SDK de Flutter/Dart, con caché. |
| Install dependencies | `flutter pub get` | Resuelve las dependencias del proyecto móvil. |
| Check formatting | `dart format --output=none --set-exit-if-changed lib test` | Falla si algún archivo no respeta el formato estándar de Dart. |
| Analyze | `flutter analyze` | Análisis estático con las reglas de `flutter_lints`. |
| Run tests | `flutter test` | Ejecuta las 21 pruebas unitarias y de widgets de la app móvil. |
| Build release APK | `flutter build apk --release` | Compila el APK de producción, apuntando a la URL pública del backend mediante `--dart-define`. |
| Upload APK | `actions/upload-artifact@v4` | Guarda el APK verificado como artifact (7 días) para el job siguiente. |

El segundo job, `Distribute Android`, depende de `Verify Flutter` (`needs: verify`) y solo se ejecuta en un `push` a `main`: descarga el APK verificado, lo distribuye por Firebase App Distribution y publica una GitHub Release (ver 7.3.2).

En los tres casos, un fallo en cualquiera de los pasos obligatorios (instalación, formato y análisis en Mobile, pruebas y build) detiene el pipeline e impide que el código avance hacia las siguientes etapas (Delivery/Deployment), evitando que código roto llegue a producción. Las únicas excepciones son los pasos informativos del Frontend (Lint y Lighthouse), que reportan resultados sin bloquear el flujo.

## 7.2. Continuous Delivery

En el estado actual del proyecto, NursePulse no cuenta con un entorno de *staging* independiente ni con un paso de aprobación manual explícito entre la integración continua y el despliegue a producción: solo en la aplicación móvil el despliegue forma parte del mismo workflow y depende de que la verificación termine en éxito (`needs: verify`). En Backend, Frontend y Landing Page, el despliegue lo dispara directamente el `push` a la rama (Render, Vercel y GitHub Pages escuchan el repositorio) y corre en paralelo al CI: según la configuración revisada en los repositorios, el resultado del workflow no condiciona técnicamente ese despliegue (sección 7.3). Por este motivo, la "entrega continua" del proyecto se sostiene en el pipeline de CI posterior a cada integración. La excepción es el Backend: desde el 3 de octubre de 2026 su rama de producción (`deploy/render-docker`) exige un Pull Request con una aprobación y el check `build-and-test` en verde antes de fusionar, lo que funciona como aprobación previa al despliegue en Render.

### 7.2.1. Tools and Practices.

**Tools:**

- **GitHub** (Pull Requests): los cambios a `main` (o a `deploy/render-docker` en el caso del backend) pueden integrarse mediante Pull Request, donde el pipeline de CI se ejecuta y un integrante del equipo puede revisar el cambio antes de fusionarlo. En `deploy/render-docker` esto es obligatorio mediante una regla de protección de rama (1 aprobación, check `build-and-test`, vigente también para administradores, sin *force push* ni borrado de la rama). El proyecto registra 21 PRs al 3 de octubre de 2026 (10 en Backend, 4 en Frontend, 6 en Mobile y 1 en Landing); el resto de los cambios se publicó por `push` directo.
- **GitHub Actions**: el mismo motor de CI (sección 7.1.2) sirve como validador de que el código está en un estado "desplegable" en todo momento.

**Practices (Prácticas):**

- **Feature Branching y Pull Requests**: las funcionalidades que se integran mediante Pull Request se desarrollan en ramas separadas, y el PR documenta el cambio y deja trazabilidad de quién lo propuso y lo fusionó. Ninguno de los PRs registrados tiene una revisión en GitHub.
- **Revisión por pares (Code Review)**: es una práctica prevista, pero hasta ahora no queda registrada: ninguno de los 21 PRs tiene una revisión en GitHub y los 19 abiertos por integrantes fueron fusionados por su propio autor. En `deploy/render-docker` (Backend), desde el 3 de octubre de 2026, la aprobación de otro integrante es obligatoria y actúa como aprobación previa al despliegue en producción; en el resto de las ramas principales no hay aprobación obligatoria configurada.
- **Build verde**: en `deploy/render-docker` (Backend) GitHub impide fusionar si el check `build-and-test` no está en éxito. En las demás ramas principales el equipo espera que el CI esté en verde antes de fusionar, pero GitHub no lo impide: no tienen protección y un PR con CI fallido sí puede fusionarse.

> **Nota:** a diferencia de un esquema clásico de Continuous Delivery con *staging* y aprobación manual del despliegue, en NursePulse el paso de "listo para desplegar" y el despliegue mismo ocurren en el mismo flujo, sin una etapa intermedia (ver sección 7.3). Introducir un entorno de staging independiente, y extender las reglas de protección de rama a `main` del Backend, del Frontend, de Mobile y de Landing, queda identificado como una mejora pendiente del proyecto.

### 7.2.2. Stages Deployment Pipeline Components.

- **Apertura del Pull Request** (cuando se usa): un desarrollador abre un PR desde su rama `feature/*` o `fix/*` hacia la rama principal del repositorio correspondiente.
- **Integración Continua (CI)**: se ejecuta automáticamente el pipeline de build y pruebas (sección 7.1.2) sobre el código del PR.
- **Revisión del equipo**: opcional salvo en `deploy/render-docker` (Backend). Un integrante distinto puede revisar los cambios y verificar que el CI haya finalizado correctamente, aunque hasta ahora los PRs registrados no tienen revisiones en GitHub.
- **Fusión o `push` a la rama principal**: el cambio llega a `main` (Frontend, Mobile, Landing) fusionando un PR o mediante `push` directo. En `deploy/render-docker` (Backend) solo puede llegar fusionando un PR aprobado y con el check `build-and-test` en verde.
- **Disparo automático del despliegue**: la llegada de un cambio a la rama principal dispara automáticamente el pipeline de Continuous Deployment (sección 7.3), sin pasos manuales adicionales.

## 7.3. Continuous Deployment

El objetivo de Continuous Deployment en NursePulse es que cada cambio que llega a la rama principal de cada repositorio se despliegue automáticamente a producción, sin intervención manual. El despliegue lo dispara el propio `push`; en el Backend, además, la protección de rama de `deploy/render-docker` garantiza que solo llegue código cuyo check `build-and-test` pasó en el Pull Request, y en la app móvil el job de distribución exige que la verificación haya terminado en éxito.

### 7.3.1. Tools and Practices.

**Tools (Herramientas):**

- **GitHub Actions**: automatiza los pipelines de CI/CD de los cuatro componentes del sistema (Backend, Frontend, Mobile, Landing Page).
- **Docker**: conteneriza el backend (Spring Boot) mediante un `Dockerfile` multi-stage (`build` con Maven + `runtime` con JRE), asegurando que el entorno de ejecución en producción sea idéntico al validado en CI.
- **Render**: plataforma PaaS que aloja el contenedor Docker del backend y lo redespliega automáticamente ante cada push a la rama `deploy/render-docker`.
- **Vercel**: plataforma utilizada para el despliegue automático del Frontend Web Application (Angular), redesplegando ante cada push a `main`.
- **GitHub Pages**: aloja la Landing Page, redesplegando automáticamente el contenido estático ante cada push a `main`.
- **Firebase App Distribution + GitHub Releases**: distribuyen la aplicación móvil (APK) — Firebase a un grupo cerrado de *testers*, y GitHub Releases como fuente pública y estable para el botón de descarga de la Landing Page.
- **Aiven (MySQL administrado)**: base de datos relacional en la nube; el esquema se actualiza automáticamente por Hibernate (`spring.jpa.hibernate.ddl-auto=update`) cuando el backend arranca con un modelo de datos nuevo, sin un paso de migración manual separado.

**Commit-based deployment:**

- Cada push a la rama principal de un repositorio dispara automáticamente su respectivo pipeline de despliegue — el flujo normal de despliegue no requiere ninguna acción manual (las plataformas permiten, además, redesplegar a mano desde su panel).
- **Rollback**: actualmente el rollback no es automático; ante un despliegue defectuoso, el equipo revierte el cambio mediante un nuevo commit (`git revert`) que dispara un nuevo despliegue automático con la versión anterior del código (en el Backend, ese revert también debe pasar por Pull Request, por la protección de rama). No existe todavía un mecanismo de rollback automático ante fallos detectados en producción — se identifica como mejora pendiente.

### 7.3.2. Production Deployment Pipeline Components.

**Componentes del Pipeline del Backend (Render):**

1. **Integración continua**: el cambio llega a `deploy/render-docker` ya aprobado en un Pull Request con el check `build-and-test` en verde (regla de protección de rama). Al llegar, el workflow `Backend CI` se ejecuta de nuevo sobre la rama (`mvn clean verify`), en paralelo al despliegue.
2. **Construcción de la imagen Docker**: Render toma el `Dockerfile` del repositorio y construye la imagen en dos etapas (build con Maven, runtime con JRE únicamente), minimizando el tamaño final de la imagen.
3. **Despliegue**: Render reemplaza el contenedor en ejecución por la nueva imagen, exponiendo el servicio en `https://backend-nursepulse-qfct.onrender.com`.
4. **Verificación de salud**: el endpoint `/actuator/health` (Spring Boot Actuator) permite confirmar que el servicio quedó arriba tras el despliegue (ver sección 7.4).

**Componentes del Pipeline de la Base de Datos (Aiven MySQL):**

1. **Actualización de esquema automática**: al desplegarse una nueva versión del backend con cambios en las entidades JPA, Hibernate aplica automáticamente los cambios de esquema (`ddl-auto=update`) contra la base de datos en Aiven al arrancar la aplicación.
2. **Conexión segura**: la conexión se establece mediante SSL (Aiven exige conexiones cifradas), con las credenciales inyectadas como variables de entorno en Render.

**Componentes del Pipeline del Frontend (Vercel):**

1. **Compilación**: al detectar un nuevo push a `main`, Vercel ejecuta `ng build` sobre el proyecto Angular en modo producción.
2. **Verificación en paralelo**: el workflow `Frontend CI` de GitHub Actions ejecuta lint, pruebas unitarias (Vitest), build y Lighthouse sobre el mismo cambio. El despliegue de Vercel no espera su resultado, porque `main` del Frontend no tiene regla de protección.
3. **Despliegue en Vercel**: si el build es exitoso, Vercel publica automáticamente la nueva versión en `https://application-web-nurse-pulse.vercel.app`, distribuida mediante su CDN global.

**Componentes del Pipeline de la Landing Page (GitHub Pages):**

1. **Push a `main`**: cualquier cambio en el repositorio `Landing-NursePulse` dispara el build nativo de GitHub Pages (sitio estático HTML/CSS/JS, sin paso de compilación adicional).
2. **Publicación**: GitHub Pages republica automáticamente el contenido en `https://nursepulse.github.io/Landing-NursePulse/`.

**Componentes del Pipeline Móvil (GitHub Actions + Firebase + GitHub Releases):**

1. **Verificación y build del APK**: el job `Verify Flutter` revisa el formato, ejecuta `flutter analyze` y las 21 pruebas, y compila el APK de release.
2. **Distribución a testers**: el job `Distribute Android`, que solo corre tras una verificación exitosa y únicamente en un `push` a `main`, sube el APK a Firebase App Distribution y notifica al grupo `testers`.
3. **Publicación de versión pública**: el mismo workflow crea una GitHub Release (`softprops/action-gh-release`) con el APK como asset, marcada como `latest`.
4. **Descarga desde la Landing Page**: el botón de descarga de la Landing Page apunta a la URL estable `.../releases/latest/download/app-release.apk`, que siempre resuelve a la versión más reciente sin necesidad de actualizar el enlace manualmente.

## 7.4. Continuous monitoring

### 7.4.1. Tools and Practices

El monitoreo continuo de NursePulse combina tres capas complementarias: un *ping* interno programado (keep-alive), un monitor externo de disponibilidad independiente de la plataforma de hosting, y la telemetría de métricas del backend enviada a Grafana Cloud. Además, una auditoría de Lighthouse sobre el frontend desplegado mide su calidad web en cada ejecución del CI.

- **Spring Boot Actuator**: expone el endpoint `/actuator/health`, utilizado tanto manualmente (verificación post-despliegue) como automáticamente (ver siguiente punto) para confirmar que el backend y su conexión a base de datos están operativos.
- **GitHub Actions (workflow programado)**: el workflow `keep-alive.yml` del repositorio Backend se ejecuta automáticamente cada 6 horas (`cron: '0 */6 * * *'`) y hace una petición HTTP al endpoint de salud del backend en producción.
- **UptimeRobot**: monitor externo (SaaS) configurado directamente desde su propio dashboard sobre `https://backend-nursepulse-qfct.onrender.com/swagger-ui.html`, con chequeos cada 5 minutos desde fuera de la infraestructura de Render. **No requiere ningún cambio de código ni credenciales en el proyecto** — a diferencia del Actuator o del workflow `keep-alive.yml`, que sí forman parte del repositorio, UptimeRobot es configuración externa: solo se le indica la URL a vigilar y la frecuencia, y notifica al equipo por correo ante cualquier caída detectada.


![Monitoreo UptimeRobot del backend](assets/chapter-7/uptimerobot-dashboard.png)

- **Grafana Cloud (métricas del backend)**: el backend envía sus métricas de ejecución a una cuenta gratuita de Grafana Cloud mediante el protocolo OpenTelemetry (OTLP). A diferencia de UptimeRobot, que solo informa si el servicio responde o no, Grafana permite observar su comportamiento interno: uso de memoria de la JVM por área (*heap* y *non-heap*), solicitudes HTTP atendidas, tiempo de actividad del proceso, entre otras. La integración sí forma parte del repositorio Backend:
  - **Código**: la dependencia `micrometer-registry-otlp` y el módulo `spring-boot-starter-opentelemetry` en el `pom.xml`, junto con tres propiedades de `application-prod.properties` (`management.otlp.metrics.export.url`, `...headers.Authorization` y `...step=1m`). No se escribió ninguna clase adicional.
  - **Credenciales**: el endpoint y el encabezado de autenticación se leen de las variables de entorno `GRAFANA_OTLP_ENDPOINT` y `GRAFANA_OTLP_AUTH_HEADER`, configuradas en el panel de Render y nunca versionadas en el repositorio.
  - **Modelo de envío (*push*)**: es el propio backend quien envía las métricas cada minuto. Se descartó el modelo *pull* (que Grafana consulte un endpoint `/actuator/prometheus`) porque exigiría mantener un agente recolector (Grafana Alloy) ejecutándose de forma permanente en algún servidor, que el proyecto no tiene.

![Métricas de memoria de la JVM del backend en Grafana Cloud (Explore)](assets/chapter-7/grafana-jvm-memory.png)

- **Lighthouse (calidad web del frontend)**: el pipeline `Frontend CI` ejecuta una auditoría de Lighthouse sobre la página de inicio de sesión desplegada en Vercel (`/sign-in`) y publica el reporte como artifact de GitHub Actions. La medición realizada el 3 de octubre de 2026 arrojó:

| Categoría | Puntaje |
| :--- | :---: |
| Rendimiento (*Performance*) | 96 |
| Accesibilidad (*Accessibility*) | 100 |
| Buenas prácticas (*Best Practices*) | 100 |
| SEO | 82 |

  Las métricas de carga que sustentan el puntaje de rendimiento fueron: *First Contentful Paint* 1,8 s, *Largest Contentful Paint* 2,3 s, *Total Blocking Time* 140 ms, *Cumulative Layout Shift* 0 y *Speed Index* 2,3 s. El puntaje de SEO es el más bajo de las cuatro categorías y queda identificado como oportunidad de mejora. La auditoría cubre únicamente la pantalla de inicio de sesión, que es la única accesible sin autenticar; las vistas internas no se auditan.

![Reporte de Lighthouse sobre la página de inicio de sesión desplegada](assets/chapter-7/lighthouse-report.png)

### 7.4.2. Monitoring Pipeline Components

El pipeline de monitoreo actual consiste en tres flujos independientes:

**Flujo 1: ping programado (keep-alive)**

1. **Disparo programado**: GitHub Actions ejecuta el workflow `Keep-alive (Render + Aiven MySQL)` cada 6 horas, o manualmente mediante `workflow_dispatch`.
2. **Ping de salud**: el workflow ejecuta `curl` contra `https://backend-nursepulse-qfct.onrender.com/actuator/health`.
3. **Efecto doble**: la petición cumple dos propósitos — (a) verificar que el servicio responde, y (b) evitar que el backend (en el plan gratuito de Render) entre en estado inactivo por falta de tráfico, y que la conexión a la base de datos en Aiven se mantenga activa.

**Flujo 2: telemetría de métricas (Grafana Cloud)**

1. **Recolección**: Micrometer, integrado en Spring Boot Actuator, registra de forma continua las métricas de la JVM y de las solicitudes HTTP del backend en ejecución en Render.
2. **Envío**: cada minuto, el registro OTLP de Micrometer envía las métricas por HTTPS al *gateway* OTLP de Grafana Cloud, autenticándose con el encabezado leído de la variable de entorno.
3. **Consulta**: las métricas quedan disponibles para consulta y graficación en Grafana (sección *Explore*), con una retención definida por el plan gratuito.

**Flujo 3: auditoría de calidad web (Lighthouse)**

1. **Disparo**: se ejecuta en cada `push` o `pull request` hacia `main` del repositorio Frontend, después del build.
2. **Auditoría**: Lighthouse analiza la versión desplegada en Vercel de la página `/sign-in`.
3. **Publicación**: el reporte JSON y HTML se sube como artifact `lighthouse-report` del run de GitHub Actions. Como el paso tiene `continue-on-error`, un puntaje bajo no detiene el pipeline.

### 7.4.3. Alerting Pipeline Components

NursePulse recibe métricas de ejecución del backend en Grafana Cloud (sección 7.4.1), pero todavía no tiene reglas de alerta configuradas sobre ellas. Las alertas actuales combinan las notificaciones nativas de cada plataforma del pipeline con un monitor externo de disponibilidad (UptimeRobot, sección 7.4.1):

**Alertas configuradas:**

- **UptimeRobot** notifica por correo al equipo ante cualquier caída detectada en los chequeos cada 5 minutos sobre el backend — es la única alerta de disponibilidad verificada *desde fuera* de la infraestructura de hosting (ver evidencia en 7.4.1).
- Fallo del workflow `Backend CI`, `Frontend CI` o `Mobile CI/CD` ante un error de compilación o una prueba rota (GitHub Actions → correo al autor del commit/PR).
- Fallo del workflow programado `keep-alive.yml` cuando el backend no responde en Render (GitHub Actions → correo a los mantenedores del repositorio).
- Fallo de build o de despliegue del Frontend Web Application en Vercel (notificación nativa de Vercel por correo al equipo del proyecto).
- Fallo de build de la imagen Docker o caída del servicio del backend en Render (notificación nativa de Render por correo al dueño del servicio).
- Fallo en la distribución del APK a través de Firebase App Distribution, si el build sube correctamente pero la subida al grupo de *testers* falla.

**Lo que todavía no existe:**

- Umbrales de rendimiento (latencia, uso de memoria) que generen una alerta automática — UptimeRobot detecta caídas totales del servicio, pero no degradaciones graduales de performance. Las métricas necesarias ya llegan a Grafana, por lo que falta únicamente definir las reglas de alerta.
- Un canal de alertas centralizado para el equipo (Slack, Microsoft Teams); cada integrante depende del correo asociado a su propia cuenta de GitHub/Render/Vercel/UptimeRobot.

> Definir reglas de alerta en Grafana (por ejemplo, sobre uso de memoria de la JVM o tiempo de respuesta HTTP) para detectar degradaciones de rendimiento antes de que se conviertan en una caída total queda identificado como la mejora pendiente más inmediata, ya que la recolección de métricas está operativa.

### 7.4.4. Notification Pipeline Components

De forma análoga a la sección anterior, las notificaciones del proyecto se apoyan en las capacidades nativas de GitHub:

- **Notificaciones de CI/CD**: GitHub notifica automáticamente al autor de un commit o Pull Request cuando un workflow (`Backend CI`, `Frontend CI`, `Mobile CI/CD`) falla, mostrando el detalle del paso que causó el error directamente en la interfaz de GitHub.
- **Notificaciones de monitoreo**: como se describió en 7.4.3, una falla del workflow `keep-alive.yml` genera una notificación automática por correo a los mantenedores del repositorio.

No se utiliza actualmente una herramienta de notificación centralizada (como Slack o Microsoft Teams) para el equipo; las notificaciones dependen del correo asociado a cada cuenta de GitHub de los integrantes.
