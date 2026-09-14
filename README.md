## Capítulo V: Product Implementation, Validation & Deployment

### 5.1. Software Configuration Management.

En esta sección se describe la gestión de la configuración del software utilizado en el proyecto de NursePulse, la cual tiene como objetivo garantizar la trazabilidad y digitalización de procesos vitales durante la estadía de un paciente en un hospital cardiovascular.
Desde registro de pacientes hasta generación de alertas y traspasos SBAR. Esta gestión permite mantener la integridad, trazabilidad y consistencia del código fuente, así como coordinar de manera eficiente el trabajo colaborativo del equipo.

El Software Configuration Management en NursePulse se basa en el uso de herramientas de control de versiones y buenas prácticas profesionales de desarrollo que permiten administrar
las distintas versiones del sistema a lo largo del tiempo. Esto incluye la organización de los repositorios del proyecto, la definición de estrategias de ramificación, la gestión
de cambios mediante commits bien documentados y la integración del trabajo realizado por los diferentes miembros del equipo.

#### 5.1.1. Software Development Environment Configuration.

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
- **Web Services RESTful API (Backend)**: desplegado en un Cloud Provider (Render / Heroku).

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


### 5.2. Landing Page, Services & Applications Implementation.

#### 5.2.1 Sprint 1

El Sprint 1 se enfocó en el desarrollo e implementación de la Landing Page de NursePulse, la cual representa el primer punto de contacto entre la solución y los usuarios potenciales.
Este sprint tuvo como objetivo establecer una presencia digital sólida que comunique de manera clara la propuesta de valor del producto.

Durante este sprint, se desarrollaron e integraron las secciones principales de la Landing Page, incluyendo presentación del producto, funcionalidades clave, llamadas a la acción, equipo desarrollador, sectores beneficiados, 
preguntas frecuentes, sección de contacto y testimonios, siguiendo los lineamientos de diseño y los wireframes definidos previamente en el Capítulo IV. Asimismo, se priorizó la usabilidad, accesibilidad y coherencia visual, con el fin de ofrecer una experiencia atractiva y profesional.

#### 5.2.1.1. Sprint Planning 1

<table><tr> <th colspan="5">Sprint #</th> <th colspan="9">Sprint 1</th> </tr> <tr> <td colspan="13">Sprint Planning Background</td> </tr> <tr> <td colspan="5">Date</td> <td colspan="8">15-04-2026</td> </tr> <tr> <td colspan="5">Time</td> <td colspan="8">9:30 AM</td> </tr> <tr> <td colspan="5">Location</td> <td colspan="8">Reunion presencial en el campus de la universidad</td> </tr> <tr> <td colspan="5">Prepared By</td> <td colspan="8">Rios Cespedes, Adrian Matias</td> </tr> <tr> <td colspan="5">Attendees (to planning meeting)</td> <td colspan="8">Aliaga Ocampo, Alexander Auden / Huamán Cuba, Johan Giovani / Rios Cespedes, Adrian Matias / Rocca Leon, Anhelo Rodrigo </td> </tr> <tr> <td colspan="5">Sprint n-1 Review Summary</td> <td colspan="8">No aplica - Este es el primer Sprint del proyecto</td> </tr> <tr> <td colspan="5">Sprint n-1 Retrospective Summary</td> <td colspan="8">No aplica - Este es el primer Sprint del proyecto</td> </tr> <tr> <td colspan="13">Sprint Goal & User Stories</td> </tr> <tr> <td colspan="5">Sprint 1 Goal</td> <td colspan="8"> <strong>"Our focus is on delivering a fully functional and user-friendly Landing Page for NursePulse, 
accompanied by complete and well-structured documentation. We believe this will provide an engaging first impression and clearly 
communicate the value proposition of our solution for enhancing clinical processes in cardiovascular nursing. This will 
be validated when the Landing Page is successfully deployed and accessible online, with all core sections (hero, how it works, 
features, benefits, FAQs, and contact) working correctly, and all corresponding documentation completed."</strong> </td> </tr> <tr> <td colspan="5">Sprint 1 Velocity</td> <td colspan="8">22 Story Points</td> </tr> <tr> <td colspan="5">Sum of Story Points</td> <td colspan="8">22 Story Points</td> </tr> </table>


#### 5.2.1.2. Aspect Leaders and Collaborators
<div align="center">
  <table style="width:100%; border-collapse: collapse; font-family: Arial, sans-serif; font-size: 13px; text-align: center;">
    <thead>
      <tr style="background-color: #f2f2f2;">
        <th style="border: 1px solid #dddddd; padding: 10px;">Team Member (Last Name, First Name)</th>
        <th style="border: 1px solid #dddddd; padding: 10px;">GitHub Username</th>
        <th style="border: 1px solid #dddddd; padding: 10px;">Diseño del Layout Principal (L/C)</th>
        <th style="border: 1px solid #dddddd; padding: 10px;">Navegacion (L/C)</th>
        <th style="border: 1px solid #dddddd; padding: 10px;">Llamada a la Accion ( CTA ) (L/C)</th>
        <th style="border: 1px solid #dddddd; padding: 10px;">Despliegue de la Landing (L/C)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="border: 1px solid #dddddd; padding: 8px;">Aliaga Ocampo, Alexander Auden</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">AlexanderAliaga19</td>
        <td style="border: 1px solid #dddddd; padding: 8px; font-weight: bold;">L</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">L</td>
        <td style="border: 1px solid #dddddd; padding: 8px; font-weight: bold;">L</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">L</td>
      </tr>
      <tr>
        <td style="border: 1px solid #dddddd; padding: 8px;">Rios Cespedes, Adrian Matias</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">AdrianR16-C</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px; font-weight: bold;">C</td>
      </tr>
      <tr>
        <td style="border: 1px solid #dddddd; padding: 8px;">Huamán Cuba, Johan Giovani</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">Johancuba</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px; font-weight: bold;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
      </tr>
        <tr>
        <td style="border: 1px solid #dddddd; padding: 8px;">Rodrigo Rocca, Anhelo</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">RoccaA4</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px; font-weight: bold;">C</td>
        <td style="border: 1px solid #dddddd; padding: 8px;">C</td>
      </tr>
    </tbody>
  </table>
</div>


#### 5.2.1.3. Sprint Backlog 1

El objetivo principal del Sprint 1 fue implementar la primera versión de la Landing Page de NursePulse, enfocada en comunicar la propuesta de valor, explicar la problemática de información clínica dispersa, presentar beneficios principales, incluir llamados a la acción, habilitar contacto inicial y asegurar una experiencia responsive. Este sprint permitió establecer el primer punto de entrada público del producto y validar la claridad inicial de la solución frente a visitantes interesados.

*Nota: Todas las tareas de ingeniería (Tasks) han sido estimadas rigurosamente en un rango de 4 a 8 horas como máximo, asegurando una descomposición granulada y manejable según los requerimientos del marco Scrum.*

**Board del Sprint (Jira):**

![Jira Board](assets/chapter-5/jira-board.png)



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

#### 5.2.1.4. Development Evidence for Sprint Review.

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

#### 5.2.1.5. Execution Evidence for Sprint Review


## 1. Resumen de Logros del Sprint
En este Sprint, el equipo se ha enfocado en el diseño, maquetación y despliegue de la interfaz principal de **NursePulse**. 
Se ha logrado consolidar la identidad visual de la marca y la arquitectura de información necesaria para comunicar una solución técnica compleja de manera sencilla y efectiva.

**Hitos alcanzados:**
* **Desarrollo de Interfaz:** Implementación completa de la Landing Page utilizando estándares modernos de diseño UI/UX.
* **Optimización de Activos:** Organización y renombrado semántico de recursos visuales para mejorar la mantenibilidad del proyecto.
* **Propuesta de Valor:** Estructuración de las secciones de monetización (Planes) y validación social (Testimonios).
* **Navegación:** Configuración de una experiencia de usuario fluida y orientada a la conversión (CTAs).

## 2. Screenshots de las Principales Vistas

A continuación, se presentan las capturas de pantalla que sirven como evidencia de la implementación funcional del sitio. Las vistas se organizan según las secciones de navegación del Landing Page (Plataforma, El problema, ¿Cómo funciona?, Características, Beneficios, Planes, Nosotros y Preguntas frecuentes), indicando el propósito de cada una y el perfil de visitante al que atiende (racional, emocional o recurrente).

### A. Plataforma (Portada y Propuesta de Valor)

![Hero Section](assets/chapter-5/image_hero.png)
*Sección de portada que presenta la propuesta de valor central de la plataforma: una solución digital diseñada específicamente para mejorar los procesos de enfermería cardiovascular mediante la centralización de información clínica, la facilitación de la comunicación entre turnos y la garantía de trazabilidad en eventos críticos. Incluye los Call-To-Action principales que dirigen al visitante recurrente hacia la aplicación desplegada, así como el selector de idioma (ES/EN) y el acceso a "Iniciar sesión".*

### B. El Problema

![The Problem](assets/chapter-5/problem.png)
<!-- TODO: agregar la captura real de la sección "El problema" (assets/chapter-5/problem.png) -->
*Explica la problemática que da origen a NursePulse: la información clínica dispersa y el registro manual dificultan la continuidad asistencial y la trazabilidad de eventos críticos en enfermería cardiovascular. Esta sección atiende al perfil de visitante racional, ayudándole a reconocer la necesidad que resuelve la plataforma.*

![Proposal & Sectors Benefiting](assets/chapter-5/proposal-sectors-benefited.png)
*Complementa la sección del problema mostrando cómo NursePulse impacta directamente en instituciones de salud como hospitales, clínicas privadas y centros especializados en cardiología, proporcionando soluciones concretas para optimizar la gestión de procesos críticos.*

### C. ¿Cómo Funciona?

![How it works](assets/chapter-5/how-it-works.png)
*Describe el flujo integral de la plataforma, mostrando cómo el personal de enfermería cardiovascular puede registrar signos vitales, documentar traspasos SBAR (Situación, Antecedentes, Evaluación y Recomendaciones), consultar historiales clínicos y mantener trazabilidad de eventos para mejorar la comunicación entre turnos.*

### D. Características

![Features](assets/chapter-5/main-features.png)
*Detalla las funcionalidades clave como registro de pacientes y citas, monitoreo de signos vitales, gestión de traspasos SBAR, seguimiento de tratamientos, registro de eventos críticos, alertas automáticas ante fluctuaciones cardiovasculares anormales y sistema de auditoría inalterable.*

### E. Beneficios

![Benefits](assets/chapter-5/main-benefits.png)
*Ilustra cómo NursePulse reduce errores en documentación clínica, optimiza el tiempo del personal de salud en tareas de registro, mejora la continuidad del cuidado del paciente y fortalece la eficiencia operativa mediante la digitalización y trazabilidad de procesos críticos.*

### F. Planes

![Plans](assets/chapter-5/plans.png)
<!-- TODO: agregar la captura real de la sección "Planes" (assets/chapter-5/plans.png) -->
*Presenta los planes y precios disponibles de NursePulse para las instituciones de salud, detallando las características incluidas en cada nivel de servicio. Esta sección atiende al perfil de visitante racional, ya que le entrega la información necesaria para comparar opciones y facilitar la decisión de contratación de la plataforma.*

### G. Nosotros (Equipo)

![Team](assets/chapter-5/dev-team.png)
*Presenta a los integrantes del equipo responsable del diseño, desarrollo e implementación de NursePulse, incluyendo sus perfiles y motivaciones. Esta sección atiende al perfil de visitante emocional, generando confianza al mostrar quiénes están detrás de la solución.*

### H. Preguntas Frecuentes

![FAQ](assets/chapter-5/faq.png)
*Aborda las consultas comunes del personal de enfermería cardiovascular y administradores de instituciones de salud sobre seguridad de datos, facilidad de acceso, integración con sistemas existentes, escalabilidad de la plataforma y soporte técnico disponible.*

### I. Testimonios

![Testimonials](assets/chapter-5/testimonials.png)
*Presenta experiencias y perspectivas del personal de salud e instituciones que han validado NursePulse, destacando mejoras en eficiencia operativa, reducción de errores, mejor comunicación entre turnos y fortalecimiento de la continuidad clínica. Esta sección atiende al perfil de visitante emocional, generando confianza a través de la experiencia de terceros y permitiendo conocer los beneficios del producto sin haberlo usado.*

### J. Contacto con Care-Labs

![Contact](assets/chapter-5/contact.png)
*Proporciona los canales de comunicación disponibles para hospitales, clínicas, centros especializados y profesionales de salud interesados en conocer más sobre NursePulse, solicitar demostraciones, consultar precios o gestionar suscripciones a la plataforma.*
#### 5.2.1.6. Services Documentation Evidence for Sprint Review.

En esta sección se presenta la documentación relacionada con los servicios que serán ofrecidos a través de la plataforma web de NursePulse. 
Estos servicios incluirán funcionalidades como el registro de pacientes y citas, traspasos SBAR, generación de alertas ante fluctuaciones cardiovasculares inusuales del paciente y registro de los signos vitales del paciente.

Durante el presente Sprint 1, el enfoque del equipo estuvo centrado exclusivamente en el diseño y desarrollo de la Landing Page del producto, 
con el objetivo de definir la propuesta de valor, los segmentos de usuarios y la experiencia inicial del sistema. Debido a este alcance, 
no se implementaron ni desplegaron servicios web funcionales, por lo que no se cuenta aún con endpoints operativos ni documentación técnica asociada 
a su consumo.


#### 5.2.1.7. Software Deployment Evidence for Sprint Review.

En esta sección se describe el proceso de implementación de la plataforma en un entorno de producción. Además, se 
presentarán los hitos más importantes que marcarán el despliegue del proyecto y garantizarán su disponibilidad para los usuarios finales.

URL de despliegue del Landing Page: [Landing Page Desplegado](https://github.com/NursePulse/Landing-NursePulse)

1. Para la Landing Page, nuestro equipo creó una rama denominada “develop” dentro del repositorio, en la cual se organizaron y almacenaron todos los archivos correspondientes al desarrollo de la Landing Page.
<p align="center">
  <img src="assets/chapter-5/deployment-landing-page-1.png" alt="deployment1" width="1000">
</p>

2. Posteriormente, nos dirigimos a configuración y empleamos GitHub Pages, el servicio de alojamiento para sitios estáticos de GitHub, para publicar y poner en línea nuestra Landing Page.
<p align="center">
  <img src="assets/chapter-5/deployment-landing-page2.png" alt="deployment2" width="1000">
</p>

3. Se seleccionó la rama previamente configurada y se procedió con el despliegue de la página.
<p align="center">
  <img src="assets/chapter-5/deployment-landing-page-3.png" alt="deployment3" width="1000">
</p>


4. Finalmente, obtuvimos el enlace de publicación, que nos permite acceder y visualizar la Landing Page en línea.
<p align="center">
  <img src="assets/chapter-5/deployment-landing-page-4.png" alt="deployment4" width="1000">
</p>

#### 5.2.1.8. Team Collaboration Insights during Sprint.

La herramienta de Insights de GitHub demuestra que todos los miembros del equipo han colaborado activamente mediante la subida de commits. Hubo un esfuerzo distribuido:

Alexander Aliaga gestionó la maquetación principal.
Anhelo Rocca estructuró las secciones interactivas de equipo y testimonios.
Johan Huamán trabajó en la internacionalización.
Adrian Rios resolvió bugs de media queries y gestionó el flujo GitFlow.

<p align="center">
  <img src="assets/chapter-5/members-commit.png" alt="deployment4" width="1000">
</p>

### 5.3. Validation Interviews

En esta sección se describen las entrevistas de validación realizadas con usuarios pertenecientes a los segmentos objetivo de NursePulse. Estas entrevistas tuvieron como propósito evaluar la interacción de los usuarios con el Landing Page y con las funcionalidades del sistema, obteniendo retroalimentación sobre usabilidad, comprensión y valor percibido.

Las entrevistas fueron registradas en video como evidencia y se analizaron en base a tareas asignadas durante la sesión.

---

### 5.3.1. Diseño de Entrevistas

Se definieron los siguientes segmentos objetivo:

- Segmento 1: Personal de salud (médicos/enfermeros)
- Segmento 2: Usuarios con interés en soluciones digitales clínicas

---

#### Elementos evaluados

Durante la sesión de validación, los usuarios interactuaron con:

- Landing Page de NursePulse
- Documentación de endpoints mediante Swagger UI
- Flujo de registro y consulta de signos vitales

---

#### User Flows evaluados

1. Navegación del Landing Page
2. Comprensión de la propuesta de valor
3. Interpretación de funcionalidades del sistema
4. Simulación de uso del sistema (explicación de endpoints)
5. Percepción de utilidad en contexto real

---

#### Estructura de la entrevista

1. Introducción al proyecto
2. Exploración del Landing Page
3. Explicación del sistema (backend)
4. Tareas guiadas
5. Preguntas de validación

---
#### Guion de preguntas por segmento objetivo

Para asegurar una validación adecuada, se diseñaron guiones de preguntas específicos para cada segmento objetivo, considerando su contexto de uso y relación con el sistema.

---

### Segmento 1: Personal de salud (Enfermeros)

**Objetivo:**  
Evaluar la utilidad del sistema en el registro y consulta de información clínica, así como la claridad de las funcionalidades relacionadas a signos vitales.

**Preguntas – Landing Page:**
- ¿Qué entiendes que hace esta plataforma?
- ¿Te queda claro el problema que busca resolver?
- ¿Consideras que la información presentada es relevante para tu trabajo?
- ¿Qué sección te parece más útil o importante?

**Preguntas – Sistema (flujo funcional):**
- ¿Crees que este sistema facilitaría el registro de signos vitales?
- ¿Te parece claro cómo se registra la información del paciente?
- ¿Consideras útil poder consultar el último registro de signos vitales?
- ¿Qué tan fácil crees que sería usar este sistema en tu rutina diaria?

**Preguntas – Experiencia de usuario:**
- ¿Te resulta intuitiva la forma en que se presenta la información?
- ¿Qué mejorarías en el sistema?
- ¿Usarías esta herramienta en tu entorno laboral?

---

### Segmento 2: Personal de salud (Médicos)

**Objetivo:**  
Evaluar la utilidad del sistema en la toma de decisiones clínicas y consulta rápida de información del paciente.

**Preguntas – Landing Page:**
- ¿El landing page transmite claramente el propósito del sistema?
- ¿Te parece relevante la solución presentada para el entorno clínico?
- ¿Qué mejorarías en la forma en que se presenta la información?

**Preguntas – Sistema (flujo funcional):**
- ¿Te resulta útil poder consultar rápidamente los signos vitales de un paciente?
- ¿Consideras importante acceder al último registro clínico?
- ¿La información presentada te parece suficiente para apoyar decisiones médicas?
- ¿Qué otras funcionalidades agregarías?

**Preguntas – Experiencia de usuario:**
- ¿La interfaz te parece clara y comprensible?
- ¿Qué tan útil consideras el sistema en tu práctica médica?
- ¿Qué mejorarías para hacerlo más eficiente?

---

### Segmento 3: Usuarios generales / interesados en tecnología

**Objetivo:**  
Evaluar la comprensión general del sistema y la claridad de la propuesta de valor.

**Preguntas – Landing Page:**
- ¿Qué entiendes que hace este sistema?
- ¿Te parece clara la propuesta de valor?
- ¿El diseño te parece atractivo?

**Preguntas – Sistema:**
- ¿Te resulta fácil entender cómo funciona el sistema?
- ¿Consideras que la solución tiene valor en el sector salud?

**Preguntas – Experiencia de usuario:**
- ¿Te parece fácil de usar?
- ¿Qué mejorarías del sistema?
- ¿Recomendarías esta solución?


### 5.3.2. Registro de Entrevistas

#### Segmento: Usuarios generales / Personal de salud

---

### Entrevista 1
- Nombre: Milagros Mendoza
- Edad: 22
- Distrito: Lima
- Video: https://youtu.be/RMx0DzfhOL0
- Inicio: 00:00
- Duración: 11:55 min
- Screenshot: 

**Resumen:**
El usuario logró identificar correctamente el propósito del sistema. Consideró que el landing page es claro y bien estructurado. Sin embargo, mencionó que algunas funcionalidades técnicas podrían explicarse mejor para usuarios no especializados.

---

### Entrevista 2
- Nombre: Miguel Zevallos
- Edad: 24
- Distrito: Lima
- Video: https://youtu.be/ERz3jkvERR8
- Inicio: 00:00
- Duración: 9:00 min
- Screenshot: 

**Resumen:**
El usuario destacó la organización visual del landing page y la claridad de la información. Indicó que el sistema tiene potencial en entornos clínicos reales. Sugirió mejorar la interfaz para hacerla más intuitiva.

---

### Entrevista 3
- Nombre: Karen Mio
- Edad: 23
- Distrito: Lima
- Video: https://youtu.be/ypqKHHFEOTU
- Inicio: 00:00
- Duración: 8:32 min
- Screenshot: 

**Resumen:**
El usuario comprendió las funcionalidades principales del sistema. Consideró que la solución es innovadora. Recomendó incluir ejemplos prácticos para mejorar la comprensión del sistema.

---

### Entrevista 4
- Nombre: Olenka Rios
- Edad: 25
- Distrito: Lima
- Video: https://youtu.be/Pu3OU6O2b9I
- Inicio: 00:00
- Duración: 9:36 min
- Screenshot:


**Resumen:**
El usuario tuvo una experiencia positiva con el sistema. Destacó la propuesta de valor, pero sugirió optimizar la navegación y simplificar algunos textos.

---

### 5.3.3. Evaluaciones según heurísticas

Se realizó la evaluación basada en heurísticas de usabilidad, arquitectura de información e inclusive design.

---

#### Evaluación heurística (basado en Anexo D)

| # | Heurística | Descripción | Evaluación | Problema identificado | Severidad |
|---|-----------|------------|------------|----------------------|----------|
| 1 | Visibilidad del sistema | El sistema debe comunicar su estado claramente | Alta | No se identificaron problemas graves | Baja |
| 2 | Relación con el mundo real | Uso de lenguaje comprensible | Media | Algunos términos técnicos no claros | Media |
| 3 | Control del usuario | Facilidad de navegación | Media | Navegación puede mejorar | Media |
| 4 | Consistencia | Uniformidad en diseño | Alta | Diseño consistente | Baja |
| 5 | Prevención de errores | Evitar errores del usuario | Media | Falta feedback visual en acciones | Media |
| 6 | Reconocimiento vs memoria | Fácil comprensión visual | Alta | Información clara | Baja |
| 7 | Flexibilidad | Adaptabilidad del sistema | Media | Limitada personalización | Media |
| 8 | Diseño estético | Interfaz atractiva | Alta | Diseño moderno | Baja |

---

### Conclusión de validación

Las entrevistas permitieron validar que NursePulse cumple con comunicar su propuesta de valor y presentar una solución útil para el entorno clínico. No obstante, se identificaron mejoras necesarias en la claridad de algunas funcionalidades, navegación y experiencia de usuario.

El sistema demuestra potencial de aplicación real, especialmente en la gestión de información clínica estructurada.

### 5.4. Video About-the-Product

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
## Conclusiones

### Conclusiones y recomendaciones

Esta sección contrasta los resultados obtenidos en las Validation Interviews (sección 5.3) frente a los Problem Statements, Assumptions e Hypothesis Statements planteados durante el proceso de Lean UX (sección 1.2.2).

**Sobre los Problem Statements**

- **Problem Statement 1 (personal de enfermería cardiovascular):** las entrevistas de validación confirmaron que la propuesta de valor de NursePulse se comprende con claridad y que la comunicación estructurada durante el traspaso de turno es percibida como un problema real. Sin embargo, las sesiones registradas evaluaron principalmente el Landing Page y la documentación de endpoints (Swagger), sin interacción directa con el formulario SBAR ni con el registro de signos vitales, por lo que este Problem Statement queda validado de forma parcial.
- **Problem Statement 2 (médicos especialistas cardiovasculares):** la muestra de entrevistas registrada en la sección 5.3.2 no identifica explícitamente a médicos especialistas entre los participantes, por lo que este Problem Statement todavía no cuenta con validación directa del segmento objetivo.
- **Problem Statement 3 (cliente institucional):** tampoco se registraron entrevistas con responsables institucionales (hospitales o clínicas), por lo que este Problem Statement permanece como validación pendiente.

**Sobre los Assumptions e Hypothesis Statements**

- El supuesto de que los usuarios valoran interfaces simples y directas (sección 1.2.2.2) se confirma parcialmente: los entrevistados destacaron la claridad del Landing Page, pero también señalaron que algunos términos técnicos y la navegación podían mejorar, lo que coincide con los hallazgos de severidad media de la evaluación heurística (relación con el mundo real, control del usuario y prevención de errores).
- La **Hipótesis 6 (Landing Page)** es la que cuenta con mayor evidencia de validación: los usuarios lograron identificar el propósito del sistema y su propuesta de valor sin apoyo adicional.
- Las **Hipótesis 1, 2, 3, 4 y 5** (traspaso SBAR, registro de signos vitales, vista resumida de evolución clínica, trazabilidad y alertas) no fueron validadas mediante interacción directa con la interfaz real de esos módulos, ya que las sesiones registradas se centraron en el Landing Page y en una simulación sobre la documentación Swagger del backend. Quedan como hipótesis abiertas para una siguiente ronda de validación con los prototipos interactivos de esas pantallas.

**Recomendaciones**

1. Ampliar las Validation Interviews a personal de enfermería y médicos especialistas cardiovasculares identificados explícitamente por su rol clínico, ya que la muestra actual (sección 5.3.2) no registra la ocupación de los participantes.
2. Diseñar sesiones de validación sobre el prototipo interactivo del formulario SBAR y del registro de signos vitales, para contrastar directamente las Hipótesis 1, 2, 3, 4 y 5.
3. Simplificar el lenguaje técnico expuesto a usuarios no especializados y mejorar la navegación, atendiendo los hallazgos de severidad media de la evaluación heurística.
4. Incorporar retroalimentación visual ante las acciones del usuario, señalada como punto débil en la evaluación heurística (prevención de errores).
5. Validar con instituciones de salud reales el modelo de precios SaaS (Basic, Standard, Premium) planteado en el Capítulo II, dado que el Problem Statement 3 aún no cuenta con validación directa.

**Conclusiones generales del equipo**

1. Concluimos que el desarrollo de NursePulse ha demostrado el potencial transformador de las tecnologías web en la mejora de los procesos de enfermería cardiovascular, facilitando la digitalización de registros de signos vitales, traspasos SBAR y eventos clínicos, lo que contribuye a reducir errores médicos y mejorar la continuidad del cuidado del paciente.
2. También concluimos que la aplicación de Scrum en el proyecto ha permitido una entrega iterativa y colaborativa, adaptándose a los requerimientos cambiantes del dominio clínico y asegurando que el producto final se alinee con las necesidades reales de los usuarios finales, como enfermeras y médicos especialistas.
3. Por último, a través del proyecto, el equipo ha fortalecido sus habilidades en desarrollo frontend con Angular, gestión de proyectos open-source y colaboración en entornos distribuidos, sentando las bases para futuras contribuciones en el ámbito de la salud digital y el software libre.

### Video About-the-Team

En esta sección se presenta el video About-the-Team de BrainSpark, donde los integrantes explican el proceso de trabajo realizado durante el desarrollo de NursePulse, la distribución de responsabilidades, las actividades desarrolladas en los sprints y la retrospectiva final del equipo.

**URL del video About-the-Team:**  


El video incluye la presentación del equipo, explicación de la colaboración en los repositorios, evidencias de trabajo en Landing Page, Web Application, RESTful API, documentación del informe, validación y despliegue. Asimismo, cada integrante participa explicando su aporte principal y los aprendizajes obtenidos durante el proyecto.

| Integrante | Participación destacada |
|-----------|--------------------------|
| Navarro Flores, Renzo Jesus| Landing Page, comunicación de propuesta de valor, evidencias y soporte en integración final. |
| Luque Minaya, Renzo Andrés | Requirements, entrevistas, validación, Product Backlog y apoyo en despliegue. |
| Paredes Davila, Jose Adrian | UX/UI, prototipos, flujos de usuario, coordinación del equipo y ajustes finales. |
| Taipe Sangama, Jorge Francisco| Arquitectura, base de datos, documentación técnica y soporte en despliegue. |
| Carlos Mansilla | Backend, Vital Signs, documentación OpenAPI, Sprint 4 y revisión final del informe. |

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
