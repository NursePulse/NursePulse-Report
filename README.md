# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.

En esta sección se describe la gestión de la configuración del software utilizado en el proyecto de NursePulse, la cual tiene como objetivo garantizar la trazabilidad y digitalización de procesos vitales durante la estadía de un paciente en un hospital cardiovascular.
Desde registro de pacientes hasta generación de alertas y traspasos SBAR. Esta gestión permite mantener la integridad, trazabilidad y consistencia del código fuente, así como coordinar de manera eficiente el trabajo colaborativo del equipo.

El Software Configuration Management en NursePulse se basa en el uso de herramientas de control de versiones y buenas prácticas profesionales de desarrollo que permiten administrar
las distintas versiones del sistema a lo largo del tiempo. Esto incluye la organización de los repositorios del proyecto, la definición de estrategias de ramificación, la gestión
de cambios mediante commits bien documentados y la integración del trabajo realizado por los diferentes miembros del equipo.

### 5.1.1. Software Development Environment Configuration.

En esta sección se describen las herramientas utilizadas por el equipo encargado de desarrollar NursePulse para colaborar de manera efectiva durante todo el ciclo de vida del producto digital. Estas herramientas han sido seleccionadas estratégicamente con el objetivo de optimizar la comunicación, organización, diseño, desarrollo, despliegue y documentación del sistema, permitiendo un trabajo colaborativo eficiente y escalable.

Las herramientas se organizan según las principales actividades del ciclo de vida del software: gestión del proyecto y requisitos, diseño UX/UI, desarrollo de software, despliegue y documentación técnica.

### Project Management y Requirements Management

- [**Jira Software**](https://www.atlassian.com/es/software/jira): Es la herramienta principal utilizada para la gestión del proyecto bajo un enfoque ágil. Permite organizar tareas en tableros, listas y tarjetas, facilitando el seguimiento del avance del Sprint, la asignación de actividades y el control del backlog del producto NursePulse. Gracias a su interfaz visual, el equipo puede mantener una visión clara del progreso del proyecto.

- [**Google Docs & Google Workspace**](https://docs.google.com/): Google Drive y Google Docs se utilizan como plataforma de almacenamiento y colaboración en la nube. Estas herramientas permiten al equipo crear, editar y compartir documentos en tiempo real, facilitando la elaboración de historias de usuario, informes, entregables y documentación general del proyecto.

### Product UX/UI Design

- [**Figma**](https://www.figma.com/files/team/1542201510350230976/recents-and-sharing?fuid=1227966816494785121): Es la herramienta principal utilizada para el diseño de la interfaz de usuario de NursePulse. Se emplea para crear wireframes, prototipos y diseños finales de la Landing Page. Su funcionalidad colaborativa permite que todo el equipo partícipe en el proceso de diseño de forma simultánea, asegurando coherencia visual y funcional.

- [**UXPressia**](https://uxpressia.com/): Se utiliza para la etapa de Needfinding y análisis centrado en el usuario. Permitió desarrollar los User Personas, así como elaborar el User Journey Mapping, Empathy Mapping e Impact Mapping, facilitando la identificación de necesidades, comportamientos, puntos de dolor y objetivos de los usuarios para estructurar de manera más precisa el diseño y enfoque del sistema.

- [**dbdiagram**](https://dbdiagram.io/): Se utiliza como herramienta de apoyo para la creación de diagramas de base de datos. Permite visualizar y diseñar la estructura de la base de datos de forma colaborativa.


### Software Development

- [**Webstorm**](https://code.visualstudio.com/) Es el editor de código utilizado para el desarrollo de la Landing Page de NursePulse. Permite trabajar de manera eficiente con tecnologías como HTML, CSS y JavaScript, ofreciendo soporte para extensiones, terminal integrada y herramientas de depuración.

- [**IntelliJ IDEA**](https://www.jetbrains.com/idea/): Entorno de desarrollo integrado utilizado para la construcción del Server Side Software (RESTful API) implementado con Spring Boot y Java.

- [**Git**](https://git-scm.com/): Es el sistema de control de versiones utilizado para gestionar el código fuente del proyecto. Permite llevar un registro de los cambios realizados, trabajar de forma colaborativa y mantener un historial organizado del desarrollo del sistema.

- [**GitHub**](https://github.com/): Es la plataforma utilizada para alojar el repositorio del proyecto NursePulse. Facilita la colaboración entre los miembros del equipo, la revisión de código y la integración continua del desarrollo.


### Software Deployment

- [**GitHub Pages**](https://pages.github.com/):  Es el servicio utilizado para desplegar la Landing Page de NursePulse. Permite publicar el sitio web directamente desde el repositorio de GitHub, haciendo que esté disponible de forma pública y accesible desde internet.

- [**Firebase Hosting**](https://firebase.google.com/):  Es una plataforma en la nube utilizada para el despliegue de aplicaciones web. En futuras etapas del proyecto, se utilizará para publicar tanto el frontend como el backend del sistema, permitiendo su acceso desde cualquier dispositivo conectado a internet.

- [**Swagger / OpenAPI**](https://swagger.io/): Herramienta utilizada para la documentación interactiva y estandarizada del RESTful API.

El uso de estos entornos nos permitió mantener una estructura de trabajo clara, con seguimiento de cambios y separación
entre documentación e implementación. Asimismo, se facilita la revisión de avances por parte de los integrantes y se asegura
coherencia entre la propuesta del informe y el producto a desarrollar.

### 5.1.2. Source Code Management

En esta sección se describe la gestión del código fuente del proyecto NursePulse, el cual se ha implementado utilizando GitHub como plataforma principal de control de versiones. 
Este sistema permite al equipo trabajar de forma colaborativa, mantener un historial completo de cambios y asegurar la correcta integración de las funcionalidades desarrolladas durante el proyecto.

El repositorio principal del proyecto es el siguiente:

- **Landing Page Repository**: [https://github.com/NursePulse/Landing-NursePulse](https://github.com/NursePulse/Landing-NursePulse)
- **Frontend Web App Repository**: [https://github.com/NursePulse/Application-Web-Nurse-Pulse](https://github.com/NursePulse/Application-Web-Nurse-Pulse)
- **Backend (Web Services) Repository**: [https://github.com/NursePulse/Backend-NursePulse](https://github.com/NursePulse/Backend-NursePulse)
- **Mobile Multiplatform Application:**: [https://github.com/NursePulse/MultiPlatform-App-NursePulse](https://github.com/NursePulse/MultiPlatform-App-NursePulse)

### GitFlow Workflow implementado

El equipo ha adoptado la metodología GitFlow como modelo de control de versiones, lo cual permite separar el desarrollo de nuevas funcionalidades, la integración de cambios y la preparación de versiones estables.

Las ramas principales utilizadas son:

- **main**: rama principal que contiene la versión estable del proyecto.
- **develop**: rama de integración donde se consolidan todas las funcionalidades completadas antes de ser llevadas a producción.
- **feature/**: ramas utilizadas para el desarrollo de funcionalidades específicas del sistema.
- **release/** : Ramas utilizadas para preparar versiones finales para despliegue y corregir errores críticos en producción, respectivamente.

### Feature Branches utilizados en el proyecto  PENDIENTEE

El desarrollo de la Landing Page de NursePulse se ha organizado mediante ramas feature específicas por componente funcional:

- feature/hero → sección principal de presentación
- feature/benefits → sección de beneficios del sistema
- feature/call-to-action → botones y acciones de conversión
- feature/characteristic → características del producto
- feature/footer → pie de página del sistema
- feature/how-it-works → explicación del funcionamiento de NursePulse
- feature/pricing → sección de planes o precios
- feature/team → sección de equipo desarrollador

Esta organización permite un desarrollo modular, donde cada funcionalidad se implementa de forma independiente antes de integrarse a la rama develop.


### Convención de ramas

El proyecto sigue la siguiente convención de nomenclatura:

- feature/nombre-descriptivo → nuevas funcionalidades
- develop → integración de funcionalidades
- main → versión estable del sistema

### Semantic Versioning

Aunque en esta primera etapa se ha trabajado principalmente en la Landing Page, el proyecto adopta el estándar de versionado semántico:

MAJOR.MINOR.PATCH

- MAJOR: cambios estructurales grandes
- MINOR: nuevas funcionalidades
- PATCH: corrección de errores

Versión actual del proyecto: v1.0.0 (Landing Page inicial)

### Conventional Commits

Para mantener un historial claro de cambios, el equipo utiliza Conventional Commits en todos los commits del repositorio.

##### Tipos de commits utilizados:

- `feat`: Nueva funcionalidad
- `fix`: Corrección de errores
- `docs`: Cambios en documentación
- `style`: Cambios en formato/estilo sin afectar la lógica
- `refactor`: Reestructuración del código sin cambio funcional
- `test`: Cambios en tests
- `build`: Cambios que afectan al sistema de compilación o dependencias
- `ci`: Configuraciones de integración continua
- `chore`: Tareas menores de mantenimiento
- `perf`: Mejoras de rendimiento
- `revert`: Reversión de un commit anterior

### 5.1.3. Source Code Style Guide & Conventions

Con el objetivo de mantener un código legible, limpio, coherente y fácilmente mantenible, el proyecto **NursePulse** adopta un conjunto de guías de estilo y convenciones estándar para todos los lenguajes utilizados en la solución. 
Estas buenas prácticas permiten asegurar consistencia entre los miembros del equipo, mejorar la calidad del código y facilitar su escalabilidad en futuras iteraciones.

Como regla principal, **todas las variables, funciones, clases, componentes y archivos se nombran estrictamente en idioma inglés**, evitando el uso del "spanglish", traducciones incorrectas (como *deployar*, *aplicativo*) o nomenclatura en español en la lógica interna del software.

Por lo que todas las variables, funciones, clases, componentes y archivos se nombran en inglés, siguiendo estándares internacionales de la industria del software.


### HTML / CSS (Landing Page y vistas estáticas)

**Guía adoptada:** Google HTML/CSS Style Guide y W3C Standards

### HTML
- Se utiliza una estructura semántica clara usando etiquetas como `header`, `main`, `section`, `article` y `footer`.
- El código HTML se escribe con indentación de 2 espacios.
- Todas las etiquetas deben cerrarse correctamente.
- Se utilizan comillas dobles para atributos HTML.
- Se evita el uso de estilos inline para mantener separación entre estructura y diseño.

### CSS
- Se utiliza la metodología BEM (Block Element Modifier) para la nomenclatura de clases:
    - Ejemplo: `btn--primary`
- Se prioriza el uso de clases reutilizables.
- Se evita la duplicación de estilos.
- Se aplican variables CSS para colores, espaciados y medidas globales.
- Se organiza el CSS de forma modular por componentes o secciones.


### AngularJS (Frontend Web Application)

**Guías adoptadas:** *Angular Coding Style Guide* y *Google TypeScript Style Guide*.

### Nomenclatura
- `camelCase` para variables, funciones, métodos y propiedades.
- `PascalCase` para clases, interfaces, componentes y enumeraciones (`enums`).
- `UPPER_SNAKE_CASE` para constantes globales.
- `kebab-case` para nombres de archivos y carpetas (ej. `patient-list.component.ts`).
- Prefijo `_` para propiedades privadas y *signals* privados.

### Buenas prácticas
- Clean Architecture junto con Domain-Driven Design (DDD): Separación lógica en capas (`application`, `domain`, `infrastructure` y `presentation`).
- Inyección de dependencias: Uso de `@Injectable()` y la función `inject()` de Angular para la gestión ágil de dependencias.
- Patrón Assembler/Mapper: Conversión de DTOs a entidades de dominio para no acoplar la respuesta del API directamente a la vista.
- Manejo de estado reactivo: Uso de *Signals* nativos para el control del estado en los componentes.
- Lógica derivada: Uso de `computed` *signals* para variables que dependen reactivamente de otros estados.
- Seguridad en la navegación: Implementación de *Route Guards* para la protección de acceso a rutas privadas o clínicas.

### Estilo de código
- Declaración de variables: Uso estricto de `const` (por defecto) y `let` (solo si mutará). Prohibido el uso de `var`.
- Reusabilidad: Código altamente modular, priorizando componentes "tontos" (Dumb/Presentational Components) y servicios "inteligentes" (Smart Services).
- Manejo de errores estructurado: Uso de bloques `try/catch` o el operador `catchError` de RxJS con mensajes descriptivos y amigables para el usuario.
- Sintaxis moderna: Uso de operadores ternarios y *optional chaining* (`?.`) para simplificar validaciones y evitar errores en consola.
- Seguridad de tipos: Habilitación estricta de *TypeScript Strict Mode* para garantizar la máxima seguridad y detección de errores durante la compilación.


### Java / Spring Boot (RESTful API Backend)

**Guía adoptada:** *Google Java Style Guide* y convenciones de *Spring Boot Features*.

### Nomenclatura
- `camelCase` para variables, métodos, atributos y parámetros.
- `PascalCase` para clases, interfaces, registros (*records*) y enumeraciones.
- `UPPER_SNAKE_CASE` para constantes (`static final`).
- `kebab-case` para las rutas (URLs) de los endpoints REST (ej. `/api/v1/vital-signs`).
- Minúsculas (sin guiones ni mayúsculas) para la estructura de paquetes (ej. `com.brainspark.nursepulse.platform.patients`).

### Buenas prácticas
- Domain-Driven Design (DDD): Organización del código fuente en paquetes alineados con *Bounded Contexts*.
- Arquitectura en capas: Separación lógica estricta en `Controller` (Presentación), `Service` (Aplicación/Lógica de Negocio), `Repository` (Infraestructura) y `Domain Model`.
- Inyección de dependencias: Uso de inyección por constructor mediante anotaciones estándar de Spring (`@RestController`, `@Service`, `@Repository`).
- Patrón DTO y Assembler/Mapper: Conversión entre DTOs y Entidades para evitar exponer el modelo de dominio y la persistencia directamente en la API.
- Persistencia Relacional: Uso de JPA/Hibernate para el mapeo objeto-relacional (ORM).
- Respuestas estandarizadas: Uso consistente de `ResponseEntity` para manejar y estructurar los códigos de estado HTTP y el cuerpo de las respuestas.

### Estilo de código
- Inmutabilidad: Preferencia por variables `final` y uso de Java *Records* para la creación concisa de DTOs inmutables.
- Código modular y aplicación de principios SOLID.
- Manejo de errores estructurado: Excepciones centralizadas globales mediante `@ControllerAdvice` y `@ExceptionHandler` para retornar mensajes de error consistentes (400, 404, 500).
- Seguridad contra nulos: Uso de `Optional<T>` en las consultas de base de datos y flujos lógicos para evitar `NullPointerException`.
- Validación de datos: Implementación de *Jakarta Bean Validation* (`@Valid`, `@NotNull`, `@NotBlank`, etc.) para sanitizar el *request body* directamente en los controladores.

### Convenciones generales del proyecto NursePulse

- Todo el código está escrito en inglés.
- Se aplica el principio SOLID.
- Se sigue el principio DRY.
- Se prioriza la legibilidad sobre la complejidad.

### Gherkin (Especificaciones)

Para la definición de criterios de aceptación en historias de usuario se utiliza Gherkin:

- Given / When / Then
- Lenguaje claro y entendible por el negocio

### Ejemplos:

```gherkin
Given a patient is registered in the system
When vital signs are recorded outside the normal range
Then the system generates an automatic alert

Given I am on the patient view
When I record vital signs data
Then it is saved correctly in the medical record

Given I complete the SBAR form
When I save the shift handover
Then it is stored with the date, time, and responsible user

Given a critical clinical event occurs
When the system records it
Then it is logged in the audit log with full details
````


### 5.1.4. Software Deployment Configuration


En esta sección el equipo especifica la configuración del despliegue de la solución **NursePulse**, incluyendo los procedimientos necesarios para que,
a partir de los repositorios de código fuente, se pueda realizar la publicación exitosa de los productos digitales que componen el sistema: Landing Page, Frontend Web Application y Web Services (Backend).

La solución se encuentra estructurada bajo una arquitectura desacoplada, donde cada componente es desplegado de manera 
independiente utilizando plataformas especializadas en la nube, lo que permite mejorar la escalabilidad, disponibilidad y mantenimiento del sistema.


### Componentes de Despliegue

- **Landing Page**: desplegada en GitHub Pages.
- **Frontend Web Application (Angular)**: desplegada en Firebase Hosting.
- **Web Services RESTful API (Backend)**: desplegado como contenedor Docker en Render (PaaS).
- **Base de Datos (MySQL)**: gestionada como servicio administrado en Aiven.
- **Monitoreo de Disponibilidad**: UptimeRobot, encargado de mantener activo el backend y notificar caídas.

### 1. Control de Versiones

El proyecto utiliza **Git** como sistema de control de versiones y **GitHub** como plataforma para la gestión de repositorios.

### Estrategia de ramas

- `main`: contiene la versión estable lista para producción.
- `develop`: integra las funcionalidades en desarrollo.
- `feature/*`: ramas destinadas al desarrollo de nuevas funcionalidades.


### 2. Despliegue de Landing Page (GitHub Pages)

La Landing Page es un sitio web responsivo construido con HTML5, CSS3 y JS.

### Pasos de despliegue

#### 1. Inicializar y preparar el repositorio
- `git init`
- `git add .`
- `git commit -m "deploy landing page"`

#### 2. Conectar el repositorio con GitHub
- `git branch -M main`
- `git remote add origin <repo-url>`
- `git push -u origin main`

#### 3. Configurar GitHub Pages
- Ir a **Settings** del repositorio.
- Acceder a la sección **Pages**.
- Seleccionar:
    - **Source**: Deploy from branch
    - **Branch**: main
    - **Folder**: / (root)

#### Resultado: 
Publicación automática bajo un subdominio HTTPS gestionado por GitHub (ejemplo: `https://nursepulse.github.io/Landing-NursePulse/`).


### 3. Despliegue del Frontend Web Application (Angular en Firebase Hosting)

La aplicación es una *Single Page Application* (SPA) desarrollada en Angular 17+ y se despliega utilizando Firebase Hosting.

### Pasos de despliegue

#### 1. Subir el proyecto al repositorio
- `git add .`
- `git commit -m "deploy frontend"`
- `git push origin main`

#### 2. Configurar en Firebase
- Acceder a: https://firebase.google.com/
- Iniciar Sesión y dirigirse a 'Ir a Consola'.
- Seleccionar **Crear un proyecto de Firebase nuevo → Escribir el nombre del proyecto (`application-web-nurse-pulse`) → Crear Proyecto**.
- Instalar Firebase CLI: `npm install -g firebase-tools`
- Iniciar sesión en Firebase CLI: `firebase login`
- Inicializar el proyecto: `firebase init`
    - Seleccionar **Hosting**.
    - Seleccionar el proyecto creado en Firebase.
    - Configurar el directorio público: `dist/browser` (o `dist/`).
    - Configurar como SPA: Sí.
    - Por el momento decimos que no se configure GitHub Action para despliegue automático.

#### 3. Configurar variables de entorno
- Configurar el archivo `environment.prod.ts` para apuntar a la URL pública del RESTful API:
  - `apiBaseUrl: 'https://<backend-url>'`

#### 4. Configurar el build
- **Build command**:
  - `ng build`
- **Publish directory**:
  - `dist/browser`

#### 5. Ejecutar Despliegue
- Ejecutamos el comando de compilación: `ng build`
- Ejecutamos el comando de publicación: `firebase deploy --only hosting`
- Firebase genera una URL pública accesible.


### 4. Despliegue de los Web Services RESTful API (Cloud Provider)

El backend desarrollado en Spring Boot y documentado con OpenAPI (Swagger) ha sido configurado para su despliegue continuo en un servicio Platform as a Service (PaaS) como Render o Heroku.

### Pasos de despliegue

#### 1. Configurar credenciales y entorno
- Ajustar la configuración del archivo `application-prod.properties`.
- Inyectar dinámicamente las credenciales de entorno para la conexión segura a la base de datos (MySQL gestionado en la nube).

#### 2. Construcción del artefacto
- Empaquetar y construir el archivo `.jar` usando Maven ejecutando el comando:
  - `mvn clean package -DskipTests`

#### 3. Publicación en el servicio Cloud
- Vincular el repositorio (rama `main`) al servicio PaaS (ej. Render/Heroku) para disparar el despliegue de la imagen/artefacto.
- El Cloud Provider asigna los recursos, levanta el servidor y genera una URL HTTPS pública.

#### 4. Documentación desplegada
- Una vez levantado el servidor, la documentación estandarizada Swagger UI queda expuesta públicamente.
- **Ruta de acceso:** `https://<backend-url>/swagger-ui.html`


### 5. Integración de Componentes

El sistema funciona de la siguiente manera:

- La **Landing Page** actúa como punto de entrada y promoción, redirigiendo al usuario mediante llamados a la acción (CTA) hacia el frontend.
- El **Frontend** (SPA en Angular) gestiona la experiencia de usuario y consume los servicios expuestos por el backend.
- El **Backend** (Spring Boot RESTful API) procesa la lógica de negocio, se conecta a la base de datos MySQL en la nube para persistir la información y devuelve las respuestas estructuradas al frontend.

### 6. Consideraciones de Despliegue

- Uso obligatorio de variables de entorno para configuraciones sensibles (credenciales de BD, tokens, URIs).
- Separación de entornos (desarrollo y producción).
- Evitar exponer credenciales dentro del código fuente bajo ninguna circunstancia.
- Verificación de URLs públicas y endpoints de Swagger después de cada despliegue.
- Mantener compatibilidad entre versiones de frontend y backend, respetando el control de versiones semántico.


## 5.2. Landing Page, Services & Applications Implementation.

### 5.2.1 Sprint Backlog 1

El Sprint 1 se enfocó en el desarrollo e implementación de la Landing Page de NursePulse, la cual representa el primer punto de contacto entre la solución y los usuarios potenciales.
Este sprint tuvo como objetivo establecer una presencia digital sólida que comunique de manera clara la propuesta de valor del producto.

Durante este sprint, se desarrollaron e integraron las secciones principales de la Landing Page, incluyendo presentación del producto, funcionalidades clave, llamadas a la acción, equipo desarrollador, sectores beneficiados, 
preguntas frecuentes, sección de contacto y testimonios, siguiendo los lineamientos de diseño y los wireframes definidos previamente en el Capítulo IV. Asimismo, se priorizó la usabilidad, accesibilidad y coherencia visual, con el fin de ofrecer una experiencia atractiva y profesional.


###  Sprint Backlog

<table>
  <thead>
    <tr>
      <th align="left">Sprint #</th>
      <th align="left" colspan="7">Sprint 1</th>
    </tr>
    <tr>
      <th align="left" colspan="2">User Story</th>
      <th align="left" colspan="6">Work-Item / Task</th>
    </tr>
    <tr>
      <th align="left">Id</th>
      <th align="left">Title</th>
      <th align="left">Id</th>
      <th align="left">Title</th>
      <th align="left">Description</th>
      <th align="left">Estimation<br>(Hours)</th>
      <th align="left">Assigned To</th>
      <th align="left">Status<br>(To-do / In-Process / To-Review / Done)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>US-01</td>
      <td>Visualizar landing page</td>
      <td>T-01.1</td>
      <td>Layout General Responsive</td>
      <td>Maquetar estructura base HTML5/CSS3 adaptativa para desktop, tablet y móvil.</td>
      <td>6</td>
      <td>Aliaga Ocampo, Alexander</td>
      <td>Done</td>
    </tr>
    <tr>
      <td>US-02</td>
      <td>Ver propuesta de valor</td>
      <td>T-02.1</td>
      <td>Sección Hero y Pitch</td>
      <td>Diseñar e implementar sección principal con pitch interactivo y llamados a la acción.</td>
      <td>4</td>
      <td>Aliaga Ocampo, Alexander</td>
      <td>Done</td>
    </tr>
    <tr>
      <td>US-05</td>
      <td>Visualizar características clave</td>
      <td>T-03.1</td>
      <td>Módulo de Features</td>
      <td>Programar cuadrícula responsive con assets gráficos detallando el funcionamiento del producto.</td>
      <td>5</td>
      <td>Rocca Leon, Anhelo</td>
      <td>Done</td>
    </tr>
    <tr>
      <td>US-11</td>
      <td>Cambiar idioma del sitio</td>
      <td>T-04.1</td>
      <td>Internacionalización</td>
      <td>Configurar lógica de internacionalización (i18n) para soportar idiomas ES y EN en toda la navegación.</td>
      <td>6</td>
      <td>Huamán Cuba, Johan</td>
      <td>Done</td>
    </tr>
    <tr>
      <td>US-10</td>
      <td>Contactar al equipo de NursePulse</td>
      <td>T-05.1</td>
      <td>Formulario de Contacto</td>
      <td>Desarrollar formulario de contacto con validaciones de campos y alertas visuales integradas.</td>
      <td>5</td>
      <td>Huamán Cuba, Johan</td>
      <td>Done</td>
    </tr>
    <tr>
      <td>US-08</td>
      <td>Visualizar testimonios</td>
      <td>T-06.1</td>
      <td>Sección Testimonios y Redes</td>
      <td>Crear carrusel interactivo de testimonios y pie de página con accesos a social media accounts.</td>
      <td>5</td>
      <td>Rocca Leon, Anhelo</td>
      <td>Done</td>
    </tr>
    <tr>
      <td>US-12</td>
      <td>Acceder desde dispositivos móviles</td>
      <td>T-07.1</td>
      <td>Ajustes Media Queries</td>
      <td>Refactorización final de media queries para asegurar que no exista desbordamiento en vistas móviles.</td>
      <td>4</td>
      <td>Rios Cespedes, Adrian</td>
      <td>Done</td>
    </tr>
    <tr>
      <td>US-04</td>
      <td>Revisar cómo funciona NursePulse</td>
      <td>T-08.1</td>
      <td>GitFlow y GitHub Pages</td>
      <td>Configurar repositorios, workflows de CI/CD básicos y desplegar la Landing Page de forma exitosa.</td>
      <td>4</td>
      <td>Rios Cespedes, Adrian</td>
      <td>Done</td>
    </tr>
  </tbody>
</table>

###  Estados de las tareas
- **To-do**: Pendiente
- **InProcess**: En desarrollo
- **ToReview**: En revisión
- **Done**: Finalizado


| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| NursePulse/Landing-NursePulse | Development | 9ff4a793ddf7ff1873134c071741c287ff50a4c8 | Resolve merge conflicts keeping local version | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | 55b09037de17a616ab3ed8665b8b6506849a3394 | Actualizar README y resolver conflictos restantes | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | c6e40f12a70340ac1c0e2566ec1df686a0536cd6 | Clean conflict markers from angular files | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | 541b310e8007861f3592d9f91685d80ef3d0aff1 | Trigger GitHub Pages deployment | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | 663bc7f2ca819a443b193750f644808035221969 | Fix GitHub Pages artifact path | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | 4ea13236773fc4bbf077099cab40c29f64344e04 | Fix logo path for GitHub Pages | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | 7d04f51cff7f222f8f4ca0f000b7782d84de3545 | Remove unused app.ts and keep bootstrap in main.ts | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | ecf95865b356bb30db6c25c4907b5b392fdcb5dc | Remove duplicated CSS rules | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | b7a5d1e876657e069a3c867cddccc53f6dae48bb | Remove duplicated HTML and CSS | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | 9baa03f8bf6fce32ba693a0a5112aeb4d5189b9d | Update favicon | - | 17/04/2026 |
| NursePulse/Landing-NursePulse | Development | 99921715b9b5216afff51a55171bf845550ca0a8 | feat(landing): add testimonials section with styles and mock data | Added testimonials section to landing page, Included sample testimonial data in component y Styled section with separators and highlighted ratings | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | 3159ea4356ed8fe07b91cd0c074548009b1fc8fc | feat(team): add team section with member profiles and styles | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | 283ac5e8519ed3e425bbfad5e8661bf58ef5e9cf | fix: update favicon file name to match new naming convention. All in kebab-case | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | d07dba9c161d526743692e87746f95333d637244 | refactor: update section IDs and links to use kebab-case for consistency | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | 6a5443642f334dc1c4aa91ff00d3ce47cbc08d25 | feat(ui): add header actions and improve navigation layout | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | 00b0d5a842a06e24b8314a513447c84b15fc0ed0 | feat(i18n): implement internationalization for navigation and header components | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | d3d73e8eedf656ec4fb9fdf6ccd4cf050aac1ebb | feat(i18n): integrate I18nService and LanguageSwitcher component | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | 2da46c1213b6a28aebc3564cf0de5d6746c7d41c | test(i18n): add unit tests for I18n service | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | 64b091e281796d2243c96e7a9c0a5c7a4d7cf30d | feat(i18n): create I18nService with Signal state and localStorage persistence | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | 6940588d45bb1a41d404277839b89bd0dc563343 | feat(i18n): create LanguageSwitcher component and toggle logic | - | 23/04/2026 |
| NursePulse/Landing-NursePulse | Development | bd0c467ec2e47510f2e09f1165dffcb5e340681c | Delete .github/workflows directory | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | 8e27b36bf65f70792da689add050baeca363ea6e | Delete .vscode directory | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | 2b2e6f919a12325ceecba774ece0c465da0241af | Delete public directory | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | ad2a49e391500a25ac18bdd7d61ebbd31e01cefe | Delete src directory | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | cb0cd1dd35a8ca27a758c4f2527897095b0c3cf9 | Delete .editorconfig | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | 714456b7713ffcdf30b51eb2f1d8bb616b68cee6 | Delete .gitignore | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | ee0ecb8ed16ca62fdfb9a289dfebcd05e7dbef82 | Delete .prettierrc | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | cc790fa7d47a027d667ed35876468c3c8d9e6eca | Delete README.md | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | 6c021310eae77681cb09e152b11cbc4d380efca5 | Delete angular.json | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | c1c2c99efa9a461733ea7497cddeb38ed89de71f | Delete package-lock.json | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | 7544d9392a8430c57f806755a5c9d0e561e42081 | Delete package.json | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | 2d6620d94abc89652f1f99f408a193de3267d5b6 | Delete tsconfig.app.json | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | cd761a5c564e4408764f6e985a86e7076405f231 | Delete tsconfig.json | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | 509148aa54b4ebaf08717e97b323b079c5fd386c | Delete tsconfig.spec.json | - | 11/05/2026 |
| NursePulse/Landing-NursePulse | Development | fac634067aca0bc95ad4471ecca765aa5a3338c0 | Add files via upload | - | 11/05/2026 |

### 5.2.2. Implemented Landing Page Evidence

A continuación se presenta evidencia visual de las secciones implementadas de la Landing Page de NursePulse, desplegada en GitHub Pages: [https://nursepulse.github.io/Landing-NursePulse/](https://nursepulse.github.io/Landing-NursePulse/).

**Sección Hero (presentación y propuesta de valor)**

📸 *[FOTO AQUÍ: captura de la parte superior de la Landing Page — abrir la URL de arriba y capturar el hero con el título, el pitch y los botones de llamada a la acción]*

![Landing - Hero](assets/chapter-5/landing-hero.png)

**Sección de características / cómo funciona**

📸 *[FOTO AQUÍ: scrollear hasta la sección "Cómo funciona" / "Características" y capturarla]*

![Landing - Características](assets/chapter-5/landing-features.png)

**Sección de planes (pricing)**

📸 *[FOTO AQUÍ: scrollear hasta la sección de planes Essential / Professional / Enterprise]*

![Landing - Pricing](assets/chapter-5/landing-pricing.png)

**Sección de equipo y testimonios**

📸 *[FOTO AQUÍ: capturar la sección "Equipo" y la sección "Testimonios"]*

![Landing - Equipo](assets/chapter-5/landing-team.png)

**Página de descarga de la app móvil**

📸 *[FOTO AQUÍ: abrir [https://nursepulse.github.io/Landing-NursePulse/download.html](https://nursepulse.github.io/Landing-NursePulse/download.html) y capturar la tarjeta de descarga con el botón "Download on the App Store or Google Play Store"]*

![Landing - Descarga app](assets/chapter-5/landing-download.png)

### 5.2.3. Implemented Frontend-Web Application Evidence

A continuación se presenta evidencia visual de los módulos implementados en la Web Application (Angular), desplegada en: [https://application-web-nurse-pulse.vercel.app](https://application-web-nurse-pulse.vercel.app).

**Inicio de sesión**

📸 *[FOTO AQUÍ: abrir `/sign-in` y capturar la pantalla de acceso clínico]*

![Frontend - Sign in](assets/chapter-5/frontend-sign-in.png)

**Registro con verificación de cuenta por correo**

Para evitar que alguien se registre con un correo que no le pertenece, el registro de nuevos usuarios (enfermería/médico) requiere confirmar la cuenta antes de poder iniciar sesión:

1. El usuario completa el formulario de `/sign-up` con sus datos (nombre, apellido, teléfono, edad, correo, rol clínico y contraseña).
2. El backend crea la cuenta marcada como **no verificada** y genera un token de verificación de un solo uso con vigencia de 24 horas.
3. Se envía automáticamente (vía Brevo) un correo de bienvenida con un botón **"Verificar mi cuenta"**.
4. Mientras la cuenta no esté verificada, cualquier intento de inicio de sesión es rechazado (`HTTP 422`) con un mensaje indicando que debe confirmar su correo.
5. Al hacer clic en el botón del correo, el backend valida el token y marca la cuenta como verificada, mostrando una página de confirmación; desde ahí el usuario ya puede iniciar sesión normalmente.

📸 *[FOTO AQUÍ: en `/sign-up`, completar el formulario y capturar la pantalla "Confirma tu correo" que aparece después de registrarse]*

![Frontend - Verificación de cuenta](assets/chapter-5/frontend-verify-account.png)

📸 *[FOTO AQUÍ: abrir el correo de bienvenida recibido y capturar el botón "Verificar mi cuenta"]*

![Frontend - Correo de verificación](assets/chapter-5/email-verification-button.png)

📸 *[FOTO AQUÍ: capturar la página de confirmación que muestra el backend al hacer clic en el botón del correo ("Cuenta verificada")]*

![Backend - Página de verificación exitosa](assets/chapter-5/backend-verify-success.png)

**Dashboard**

📸 *[FOTO AQUÍ: iniciar sesión con un usuario y capturar el Dashboard principal, con el resumen de pacientes en monitoreo y alertas]*

![Frontend - Dashboard](assets/chapter-5/frontend-dashboard.png)

**Gestión de pacientes**

📸 *[FOTO AQUÍ: capturar la vista `/patients`, la tabla de pacientes y el formulario de registro/edición abierto (con el campo "Médico tratante" como select)]*

![Frontend - Pacientes](assets/chapter-5/frontend-patients.png)

**Signos vitales**

📸 *[FOTO AQUÍ: entrar al detalle clínico de un paciente, pestaña de Signos Vitales, con el formulario de registro abierto]*

![Frontend - Signos vitales](assets/chapter-5/frontend-vital-signs.png)

**Eventos clínicos**

📸 *[FOTO AQUÍ: capturar la vista de Eventos Clínicos con el formulario de registro abierto]*

![Frontend - Eventos clínicos](assets/chapter-5/frontend-clinical-events.png)

**Traspasos SBAR**

📸 *[FOTO AQUÍ: capturar la vista de SBAR con el formulario de Situación/Antecedentes/Evaluación/Recomendación abierto]*

![Frontend - SBAR](assets/chapter-5/frontend-sbar.png)

**Alertas clínicas**

📸 *[FOTO AQUÍ: capturar el Centro de Alertas, mostrando alertas pendientes y el botón de atender/cerrar]*

![Frontend - Alertas](assets/chapter-5/frontend-alerts.png)

**Auditoría (trazabilidad) y exportación a PDF**

📸 *[FOTO AQUÍ: capturar la vista de Auditoría con la tabla de movimientos y el botón "Exportar PDF"]*

![Frontend - Auditoría](assets/chapter-5/frontend-audit.png)

**Gestión de usuarios (solo Administrador)**

📸 *[FOTO AQUÍ: iniciar sesión como admin, capturar `/users` con la lista de usuarios y el selector de roles]*

![Frontend - Usuarios](assets/chapter-5/frontend-users.png)

**Reportes**

📸 *[FOTO AQUÍ: capturar la vista de Reportes con un reporte generado]*

![Frontend - Reportes](assets/chapter-5/frontend-reports.png)

### 5.2.4. Acuerdo de Servicio - SaaS

NursePulse se ofrece bajo un modelo de suscripción SaaS (Software as a Service) con tres planes diferenciados por número de asientos (usuarios clínicos) y funcionalidades habilitadas. Esta sección resume las condiciones comerciales simuladas dentro del producto, implementadas en el módulo de Suscripciones de la Web Application.

| Plan | Precio mensual | Asientos incluidos | Funcionalidades incluidas |
| :--- | :--- | :--- | :--- |
| **Essential** | US$ 0 (gratuito) | Hasta 5 usuarios | Gestión de pacientes, registro de signos vitales, alertas clínicas |
| **Professional** | US$ 49 / mes | Hasta 25 usuarios | Todo lo del plan Essential + Traspasos SBAR + Reportes |
| **Enterprise** | US$ 129 / mes | Hasta 100 usuarios | Todo lo del plan Professional + Auditoría (trazabilidad completa) + Soporte prioritario |

**Condiciones generales del acuerdo de servicio:**

1. **Vigencia**: la suscripción se renueva automáticamente de forma mensual mientras el cliente (institución de salud) mantenga el pago activo.
2. **Cambio de plan**: el cliente puede subir o bajar de plan en cualquier momento; el cambio aplica de forma inmediata sobre los límites de asientos y funcionalidades disponibles.
3. **Datos clínicos**: la información de pacientes, signos vitales, eventos clínicos y traspasos SBAR pertenece a la institución cliente; NursePulse actúa únicamente como proveedor de la plataforma (Data Processor).
4. **Disponibilidad**: el proveedor procura una disponibilidad continua del servicio, monitoreada mediante UptimeRobot sobre el backend desplegado en Render.
5. **Soporte**: los planes Professional y Enterprise incluyen soporte prioritario vía canal de contacto directo; el plan Essential recibe soporte por el canal estándar (formulario de contacto de la Landing Page).
6. **Cancelación**: el cliente puede cancelar la suscripción en cualquier momento, sin penalidad, manteniendo acceso hasta el final del periodo ya pagado.

> **Nota:** en esta etapa del proyecto, el pago de suscripciones se encuentra **simulado** dentro de la propia aplicación (no se procesan pagos reales con una pasarela como Stripe); la integración con una pasarela de pago real queda planteada como trabajo futuro (ver sección de recomendaciones).

📸 *[FOTO AQUÍ: capturar la vista `/subscription-plans` de la Web Application mostrando las 3 tarjetas de planes]*

![Frontend - Planes de suscripción](assets/chapter-5/frontend-subscription-plans.png)

### 5.2.5. Implemented Native-Mobile Application Evidence

A continuación se presenta evidencia visual de la aplicación móvil multiplataforma (Flutter), la cual replica las funcionalidades clínicas principales de la Web Application para su uso desde el celular del personal de enfermería y médico durante el turno.

**Inicio de sesión y registro**

📸 *[FOTO AQUÍ: capturar en un emulador o dispositivo Android la pantalla de sign-in y sign-up de la app móvil]*

![Mobile - Sign in](assets/chapter-5/mobile-sign-in.png)

**Gestión de pacientes**

📸 *[FOTO AQUÍ: capturar la lista de pacientes y el formulario de registro en la app móvil]*

![Mobile - Pacientes](assets/chapter-5/mobile-patients.png)

**Signos vitales y alertas**

📸 *[FOTO AQUÍ: capturar el registro de signos vitales y la lista de alertas en la app móvil]*

![Mobile - Signos vitales y alertas](assets/chapter-5/mobile-vitals-alerts.png)

**Descarga del APK**

La aplicación se distribuye como archivo APK, generado automáticamente mediante el pipeline de CI/CD del repositorio `MultiPlatform-App-NursePulse` (ver Capítulo VII) y publicado como GitHub Release. El botón "Download" de la Landing Page enlaza directamente a la última versión disponible:

`https://github.com/NursePulse/MultiPlatform-App-NursePulse/releases/latest/download/app-release.apk`

### 5.2.6. Implemented RESTful API and/or Serverless Backend Evidence

El backend de NursePulse se implementó como una RESTful API utilizando Spring Boot, siguiendo una arquitectura de módulos por *Bounded Context* (Domain-Driven Design). El servicio se encuentra desplegado como contenedor Docker en Render y documentado con Swagger/OpenAPI.

**Swagger UI del backend desplegado**

📸 *[FOTO AQUÍ: abrir `https://backend-nursepulse-qfct.onrender.com/swagger-ui/index.html` y capturar la lista de controladores/endpoints documentados]*

![Backend - Swagger UI](assets/chapter-5/backend-swagger.png)

**Módulos (Bounded Contexts) implementados:**

| Módulo | Responsabilidad |
| :--- | :--- |
| `iam` | Autenticación (sign-in/sign-up), gestión de usuarios y roles (NURSE, DOCTOR, ADMIN) |
| `patients` | Registro, consulta, actualización, alta y eliminación de pacientes |
| `vitalsigns` | Registro y consulta de signos vitales por paciente |
| `clinicalevents` | Registro de eventos clínicos del turno (observación, medicación, complicación, emergencia, etc.) |
| `handover` | Traspasos de turno estructurados en formato SBAR |
| `criticalevents` | Alertas clínicas (creación, atención y cierre) |
| `auditlogs` | Trazabilidad/auditoría de todas las acciones clínicas del sistema, con exportación a PDF |

**Evidencia de ejecución del servicio en producción**

📸 *[FOTO AQUÍ: capturar `https://backend-nursepulse-qfct.onrender.com/actuator/health` mostrando `{"status":"UP"}`]*

![Backend - Health check](assets/chapter-5/backend-health.png)

### 5.2.7. RESTful API documentation

La siguiente tabla resume los endpoints principales expuestos por el backend, agrupados por módulo, junto con los roles autorizados para consumirlos según la configuración de seguridad (`WebSecurityConfiguration`):

**Autenticación (`/api/v1/authentication`)** — público

| Método | Endpoint | Descripción |
| :--- | :--- | :--- |
| POST | `/sign-in` | Inicio de sesión, retorna JWT (rechaza con `422` si el correo no ha sido verificado) |
| POST | `/sign-up` | Registro público de enfermería/médico (ROLE_NURSE o ROLE_DOCTOR); envía un correo de verificación |
| GET | `/verify-email?token=...` | Confirma la cuenta a partir del link enviado por correo; renderiza una página HTML de confirmación |

**Usuarios (`/api/v1/users`)** — NURSE, DOCTOR, ADMIN (lectura) / ADMIN (gestión)

| Método | Endpoint | Roles | Descripción |
| :--- | :--- | :--- | :--- |
| GET | `/users` | NURSE, DOCTOR, ADMIN | Lista de usuarios registrados (directorio de personal) |
| GET | `/users/{userId}` | ADMIN | Detalle de un usuario |
| PATCH | `/users/{userId}/roles` | ADMIN | Cambiar el rol asignado a un usuario |

**Pacientes (`/api/v1/patients`)**

| Método | Endpoint | Roles | Descripción |
| :--- | :--- | :--- | :--- |
| POST | `/patients` | NURSE, ADMIN | Registrar un nuevo paciente |
| GET | `/patients` | NURSE, DOCTOR, ADMIN | Listar pacientes |
| GET | `/patients/{patientId}` | NURSE, DOCTOR, ADMIN | Detalle de un paciente |
| PUT | `/patients/{patientId}` | NURSE, DOCTOR, ADMIN | Actualizar datos de un paciente |
| DELETE | `/patients/{patientId}` | ADMIN | Eliminar un paciente |

**Signos vitales (`/api/v1/vital-sign-records`)**

| Método | Endpoint | Roles | Descripción |
| :--- | :--- | :--- | :--- |
| POST | `/vital-sign-records` | NURSE, ADMIN | Registrar signos vitales |
| GET | `/vital-sign-records` | NURSE, DOCTOR, ADMIN | Listar registros |
| GET | `/vital-sign-records/patients/{patientId}` | NURSE, DOCTOR, ADMIN | Historial de un paciente |
| GET | `/vital-sign-records/patients/{patientId}/latest` | NURSE, DOCTOR, ADMIN | Último registro de un paciente |
| GET | `/vital-sign-records/{vitalSignRecordId}` | NURSE, DOCTOR, ADMIN | Detalle de un registro |

**Eventos clínicos (`/api/v1/clinical-events`)**

| Método | Endpoint | Roles | Descripción |
| :--- | :--- | :--- | :--- |
| POST | `/clinical-events` | NURSE, DOCTOR, ADMIN | Registrar un evento clínico |
| GET | `/clinical-events` | NURSE, DOCTOR, ADMIN | Listar eventos |
| GET | `/clinical-events/patients/{patientId}` | NURSE, DOCTOR, ADMIN | Eventos de un paciente |

**Traspasos SBAR (`/api/v1/handovers`)**

| Método | Endpoint | Roles | Descripción |
| :--- | :--- | :--- | :--- |
| POST | `/handovers` | NURSE, ADMIN | Crear un traspaso SBAR |
| GET | `/handovers/patients/{patientId}` | NURSE, DOCTOR, ADMIN | Traspasos de un paciente |
| GET | `/handovers/{handoverId}` | NURSE, DOCTOR, ADMIN | Detalle de un traspaso |
| PATCH | `/handovers/{handoverId}/acknowledge` | NURSE, ADMIN | Confirmar recepción del traspaso |

**Alertas clínicas (`/api/v1/alerts`)**

| Método | Endpoint | Roles | Descripción |
| :--- | :--- | :--- | :--- |
| POST | `/alerts` | NURSE, DOCTOR, ADMIN | Crear una alerta manual |
| GET | `/alerts` | NURSE, DOCTOR, ADMIN | Listar alertas |
| GET | `/alerts/patients/{patientId}` | NURSE, DOCTOR, ADMIN | Alertas de un paciente |
| PATCH | `/alerts/{alertId}/attend` | NURSE, DOCTOR, ADMIN | Marcar alerta como atendida |
| PATCH | `/alerts/{alertId}/close` | DOCTOR, ADMIN | Cerrar (resolver) una alerta — cierre clínico exclusivo del médico |

**Auditoría (`/api/v1/audit-logs`)**

| Método | Endpoint | Roles | Descripción |
| :--- | :--- | :--- | :--- |
| POST | `/audit-logs` | NURSE, DOCTOR, ADMIN | Registrar una entrada de auditoría |
| GET | `/audit-logs` | DOCTOR, ADMIN | Listar entradas de auditoría |
| GET | `/audit-logs/export/pdf` | DOCTOR, ADMIN | Exportar el registro de auditoría en PDF |
| GET | `/audit-logs/{auditLogId}` | DOCTOR, ADMIN | Detalle de una entrada |
| GET | `/audit-logs/patients/{patientId}/timeline` | DOCTOR, ADMIN | Línea de tiempo de auditoría de un paciente |
| GET | `/audit-logs/entities/{entityType}/{entityId}` | DOCTOR, ADMIN | Auditoría de una entidad específica |

La documentación interactiva y siempre actualizada de todos los endpoints (con esquemas de request/response) está disponible públicamente en Swagger UI: [https://backend-nursepulse-qfct.onrender.com/swagger-ui/index.html](https://backend-nursepulse-qfct.onrender.com/swagger-ui/index.html)

### 5.2.8. Team Collaboration Insights

Durante el desarrollo de NursePulse, el equipo mantuvo una dinámica de colaboración apoyada en las herramientas descritas en la sección 5.1.1:

- **Jira Software** se utilizó como tablero central del Sprint Backlog, permitiendo visualizar el estado de cada tarea (To-do, In-Process, To-Review, Done) y distribuir el trabajo entre los integrantes según su rol dentro del equipo (frontend, backend, diseño, documentación).
- **GitHub** funcionó como plataforma de integración de código: cada funcionalidad se desarrolló en una rama `feature/*` independiente y se integró mediante Pull Requests, lo que permitió revisión de código entre pares antes de fusionar cambios a `develop`/`main`.
- **Google Docs y Google Drive** se usaron para la redacción colaborativa en tiempo real del informe, las historias de usuario y las actas de reunión, permitiendo que todos los integrantes aportaran simultáneamente sin conflictos de versión.
- **Comunicación diaria**: el equipo sostuvo coordinaciones periódicas (estilo daily/stand-up) para reportar avances, bloqueos y reasignar tareas cuando algún integrante encontraba un impedimento técnico.
- **Revisión cruzada**: los cambios de un módulo (por ejemplo, un endpoint nuevo en el backend) se comunicaban al integrante responsable del frontend correspondiente para mantener sincronizados los contratos de datos entre ambas capas, evitando desalineaciones entre lo que el cliente esperaba y lo que el servidor exponía.

Esta forma de trabajo permitió que, pese a ser un equipo distribuido y con integrantes enfocados en distintas capas de la solución (Landing Page, Frontend Web, Backend, Mobile), el producto final mantuviera coherencia funcional y visual entre todos sus componentes.

## 5.3. Video About-the-Product

En esta sección se presenta el video "About the Product", en el cual el equipo muestra el funcionamiento general del sistema NursePulse, explicando su propósito, principales funcionalidades y valor dentro del contexto clínico.

El objetivo del video es evidenciar de manera práctica cómo la solución desarrollada permite mejorar la gestión de información clínica, específicamente en el registro y consulta de signos vitales, facilitando el acceso a datos relevantes para el personal de salud.

---

### Descripción del contenido del video

El video desarrollado incluye los siguientes elementos:

- **Introducción del problema:**  
  Se explica la problemática relacionada a la gestión manual o poco estructurada de la información clínica, especialmente en el registro de signos vitales.

- **Presentación de la solución:**  
  Se introduce NursePulse como una herramienta que busca digitalizar y estructurar la información clínica, mejorando la accesibilidad y organización de los datos.

- **Demostración del Landing Page:**  
  Se muestra la interfaz del landing page, destacando la propuesta de valor, funcionalidades principales y secciones informativas del producto.

- **Demostración del sistema (backend):**  
  Se realiza una demostración utilizando Swagger UI, donde se evidencian los principales endpoints implementados:
  - Registro de signos vitales
  - Consulta de registros por paciente
  - Obtención del último registro clínico

- **Explicación de funcionalidades clave:**  
  Se explica cómo cada endpoint contribuye a resolver el problema identificado, facilitando el trabajo del personal de salud.

- **Conclusión del equipo:**  
  Se resume el impacto de la solución y su potencial aplicación en entornos reales.

---

### Enlace del video

El video "About the Product" se encuentra disponible en el siguiente enlace:
Youtube: [https://youtu.be/3A5RHi0I9Y0]

Upc:[https://upcedupe-my.sharepoint.com/:v:/g/personal/u202217893_upc_edu_pe/IQAYdJDORBeKRLUWSeZyVdoNAbQq78Aig73g8Ok6sZhPcbA?e=5Ar5CS&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D]

---

### Conclusión

El video permite validar el funcionamiento del sistema desarrollado, mostrando evidencia real de las funcionalidades implementadas durante el proyecto. Asimismo, refuerza la propuesta de valor de NursePulse, evidenciando su utilidad en la gestión de información clínica y su potencial uso en escenarios reales.

## Bibliografía

- Pressman, R. S., & Maxim, B. R. (2020). Software Engineering: A Practitioner’s Approach (9th ed.). McGraw-Hill Education.
- Angular. (2026). Angular Documentation. Retrieved from https://angular.dev/
- Spring. (2026). Spring Boot Documentation. Retrieved from https://docs.spring.io/spring-boot/
- OpenAPI Initiative. (2026). OpenAPI Specification. Retrieved from https://spec.openapis.org/oas/latest.html
- Swagger. (2026). Swagger UI Documentation. Retrieved from https://swagger.io/tools/swagger-ui/
- GitHub Docs. (2026). GitHub Documentation. Retrieved from https://docs.github.com/
- Vercel. (2026). Vercel Documentation. Retrieved from https://vercel.com/docs
- Railway. (2026). Railway Documentation. Retrieved from https://docs.railway.com/
- World Health Organization. (2025). Cardiovascular diseases. Retrieved from https://www.who.int/

## Anexos
- Link de la organización de GitHub: https://github.com/NursePulse
- Link del repositorio del reporte: https://github.com/NursePulse/NursePulse-Report
- Link de la landing page desplegada: https://nursepulse.github.io/Landing-NursePulse/#funciona
- Link del repositorio del frontend: https://github.com/NursePulse/Application-Web-Nurse-Pulse
- Link del frontend desplegado: https://application-web-nurse-pulse.vercel.app/sign-in
- Link del backend desplegado / Swagger UI: https://backpulsereport-production-7576.up.railway.app/swagger-ui/index.html
- Link del repositorio del backend: https://github.com/NursePulse/Backend-NursePulse
