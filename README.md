# Capítulo VI: Product Verification & Validation

## 6.1. Testing Suites & Validation

NursePulse cuenta con una suite de pruebas automatizadas de 61 pruebas en el backend (JUnit 5 + Mockito) y 29 pruebas en el frontend (Vitest), ejecutadas automáticamente en cada `push` y `pull request` hacia la rama principal mediante los workflows `Backend CI` y `Frontend CI`.

**Backend**

![Resultado de la suite del backend: 61 pruebas, 0 fallos, BUILD SUCCESS](assets/chapter-6/61pruebas.png)

**Front-end**

![Resultado de la suite del frontend: 29 pruebas aprobadas](assets/chapter-6/frontend-tests-29.png)

### 6.1.1. Core Entities Unit Tests.

Pruebas unitarias puras sobre entidades y value objects del dominio, sin dependencias externas ni framework de Spring:

| Clase de prueba | Módulo | Qué valida |
| :--- | :--- | :--- |
| `RoleTest` | IAM | Reglas del value object `Role` (rol por defecto, comparación por nombre). |
| `SignUpResourceValidationTest` | IAM | Las 10 reglas de validación del registro (usuario, contraseña, nombre, email, teléfono, edad) mediante Jakarta Bean Validation. |
| `SignUpCommandFromResourceAssemblerTest` | IAM | Transformación correcta de `SignUpResource` a `SignUpCommand`. |

### 6.1.2. Core Integration Tests.

Pruebas que levantan el contexto completo de Spring Boot (`@SpringBootTest`) para validar el comportamiento end-to-end de la capa de seguridad y los casos de uso de aplicación con sus colaboradores simulados:

| Clase de prueba | Tipo | Qué valida |
| :--- | :--- | :--- |
| `ClinicalAuthorizationIntegrationTest` | Integración (`@SpringBootTest` + `MockMvc`) | 19 escenarios de autorización por rol (NURSE/DOCTOR/ADMIN) contra los endpoints reales de pacientes, signos vitales, SBAR, alertas y auditoría. |
| `UserCommandServiceImplTest` | Unitaria con Mockito | Registro, inicio de sesión (incluyendo el bloqueo por email no verificado), conflictos de usuario/email/teléfono duplicado y verificación de cuenta. |
| `AlertCommandServiceImplTest` | Unitaria con Mockito | Creación, atención y cierre de alertas; envío de SMS a médicos cuando la alerta es crítica. |
| `AuditLogsControllerTest` | Unitaria con Mockito | Respuesta del controlador de auditoría ante resultados exitosos y fallidos. |
| `AuditLogPdfExportServiceTest` | Unitaria | Generación de un PDF válido (magic bytes `%PDF`) a partir de una lista de entradas de auditoría. |
| `BrevoEmailNotificationServiceTest` / `TwilioSmsNotificationServiceTest` | Unitaria | Manejo seguro de credenciales inválidas, destinatarios vacíos y fallos del proveedor externo, sin interrumpir el flujo principal. |
| `TokenServiceImplTest` | Unitaria | Generación y validación de tokens JWT. |
| `OpenApiConfigurationTest` | Unitaria | Configuración de la documentación Swagger/OpenAPI. |

### 6.1.3. Core Behavior-Driven Development

El proyecto **no implementa BDD ejecutable** (no se utiliza Cucumber ni un runner de Gherkin sobre el código). Lo que sí existe es la especificación de criterios de aceptación en formato Gherkin (`Given/When/Then`) a nivel de documentación, como parte de las User Stories del Capítulo III y de la guía de estilo de código (Capítulo V, sección 5.1.3) — pero estos escenarios no están automatizados ni se ejecutan como parte del pipeline de CI.

> Implementar BDD ejecutable (por ejemplo, con Cucumber + Spring) sobre los escenarios Gherkin ya documentados queda identificado como una mejora pendiente del proyecto.

### 6.1.4. Core System Tests

No existe automatización de pruebas de sistema end-to-end (tipo Selenium/Playwright/Cypress) contra la aplicación desplegada. La verificación a nivel de sistema se realizó de forma **manual y exploratoria directamente en producción** a lo largo del desarrollo, cubriendo flujos completos como:

- Registro de usuario → verificación de cuenta por correo (Brevo) → inicio de sesión.
- Creación de pacientes, registro de signos vitales, eventos clínicos y traspasos SBAR con las validaciones de formato (nombres, documento, fecha de nacimiento, límites de caracteres).
- Generación de una alerta crítica → solicitud de SMS a los médicos registrados (Twilio). La solicitud llega correctamente a la API de Twilio, pero la entrega del mensaje **no pudo completarse**: la cuenta de prueba (*trial*) de Twilio solo permite enviar a números verificados y exige una plantilla de contenido que requiere una cuenta de pago. Por eso esta integración queda validada a nivel de código y de pruebas unitarias (6.1.2), no de entrega real.
- Exportación del registro de auditoría a PDF, descargado y verificado directamente desde la interfaz.
- Flujo de permisos por rol (NURSE/DOCTOR/ADMIN) replicado en la interfaz real, no solo a nivel de API.

Evidencia del primer flujo: el correo de verificación recibido y la pantalla de confirmación de cuenta.

![Correo de verificación de cuenta recibido con el botón de confirmación](assets/chapter-6/flow-verify-email-inbox.png)

![Pantalla de cuenta verificada tras abrir el enlace del correo](assets/chapter-6/flow-verify-email-page.png)

Evidencia del flujo de exportación de auditoría:

![PDF del registro de auditoría exportado desde la interfaz](assets/chapter-6/flow-audit-pdf.png)

**Auditoría automatizada de calidad web (Lighthouse).** La única verificación automatizada que se ejecuta contra la aplicación desplegada es una auditoría de Lighthouse sobre la pantalla de inicio de sesión del frontend, integrada en `Frontend CI` (ver Capítulo VII, secciones 7.1.2 y 7.4.1). La medición del 3 de octubre de 2026 arrojó Rendimiento 96, Accesibilidad 100, Buenas prácticas 100 y SEO 82. Esta auditoría mide calidad no funcional (carga, accesibilidad, buenas prácticas); no recorre flujos de negocio ni reemplaza las pruebas de sistema.

![Reporte de Lighthouse sobre la pantalla de inicio de sesión desplegada](assets/chapter-6/lighthouse-report.png)

## 6.2. Static testing & Verification

A diferencia de la sección 6.1 (pruebas dinámicas, que ejecutan el código), esta sección cubre la verificación **estática** del proyecto: revisión de convenciones de código y de la calidad/seguridad del código fuente sin necesidad de ejecutarlo.

### 6.2.1. Static Code Analysis

#### 6.2.1.1. Coding standard & Code conventions

NursePulse define una guía de estilo de código explícita por tecnología (HTML/CSS, Angular/TypeScript, Java/Spring Boot), documentada en el Capítulo V, sección 5.1.3. El cumplimiento de esta guía se verifica de las siguientes formas:

- **ESLint** (`angular-eslint` + `typescript-eslint`) en el frontend: analiza el código TypeScript y las plantillas de Angular con las reglas recomendadas (por ejemplo, uso de `inject()`, accesibilidad de elementos interactivos en las plantillas y restricciones sobre el tipo `any`). Se ejecuta con `npm run lint` y como paso del pipeline `Frontend CI` (ver 6.2.1.2).
- **TypeScript Strict Mode**: el compilador de Angular (`tsc --strict`) rechaza el build (`ng build`, ejecutado en `Frontend CI`) ante tipos implícitos `any`, variables no inicializadas o accesos nulos no controlados, forzando el cumplimiento de la convención de "Seguridad de tipos" definida en 5.1.3.
- **Jakarta Bean Validation** en el backend actúa como verificación declarativa de las reglas de negocio en el límite de la API (`@NotBlank`, `@Pattern`, `@Size`, `@Email`), en línea con la convención de "Validación de datos" de 5.1.3.
- **Revisión por pares**: en los cambios que se integran mediante Pull Request, un integrante distinto al autor puede verificar que el código sigue la nomenclatura (`camelCase`/`PascalCase`/`kebab-case` según corresponda) y la arquitectura por capas (DDD) descrita en 5.1.3. Esta revisión solo está forzada por el repositorio en la rama de producción del Backend; en el resto es una práctica del equipo (ver el alcance real en 6.2.2).

#### 6.2.1.2. Code Quality & Code Security

El frontend cuenta con **ESLint** como herramienta de análisis estático, integrada al repositorio (`eslint.config.js`, script `npm run lint`) y al pipeline `Frontend CI` como paso informativo: tiene `continue-on-error`, por lo que reporta hallazgos sin detener el pipeline. En la ejecución del 3 de octubre de 2026 detectó **44 problemas (todos de nivel error) en 19 archivos**, que corresponden a código previo a la incorporación de la herramienta y todavía no se han corregido:

| Regla | Hallazgos | Qué detecta |
| :--- | :---: | :--- |
| `@typescript-eslint/no-explicit-any` | 12 | Uso del tipo `any`, que desactiva la verificación de tipos. |
| `@angular-eslint/template/click-events-have-key-events` | 11 | Elementos con evento `click` sin equivalente de teclado (accesibilidad). |
| `@angular-eslint/prefer-inject` | 9 | Inyección por constructor en lugar de la función `inject()`. |
| `@angular-eslint/template/interactive-supports-focus` | 9 | Elementos interactivos que no reciben foco con el teclado (accesibilidad). |
| `@typescript-eslint/no-duplicate-enum-values` | 4 | Valores duplicados dentro de un `enum`. |
| `@angular-eslint/directive-selector` | 2 | Selectores de directiva que no siguen la convención configurada. |
| `@typescript-eslint/array-type` | 1 | Estilo de declaración de tipos de arreglo. |

![Salida de ESLint con los 44 hallazgos del frontend](assets/chapter-6/eslint-report.png)

La aplicación móvil tiene configurado el paquete `flutter_lints` (`analysis_options.yaml`), que aplica reglas recomendadas de Dart/Flutter en el IDE y con `flutter analyze`, pero el pipeline `Mobile CI/CD` no ejecuta ese comando. El backend **no cuenta con una herramienta dedicada de análisis estático** (como SonarQube o SonarLint) integrada al pipeline. La calidad y seguridad del código se sostienen adicionalmente mediante:

- **Inspecciones del IDE**: IntelliJ IDEA (backend) y WebStorm (frontend) señalan en tiempo real código muerto, imports no utilizados, complejidad excesiva y antipatrones comunes mientras se escribe el código, aunque sin un reporte centralizado ni umbrales de calidad exigidos por el pipeline.
- **Spring Security** gestiona la autorización por rol de forma centralizada (`WebSecurityConfiguration`), evitando que la lógica de permisos quede dispersa o implementada de forma inconsistente entre controladores.
- **Manejo centralizado de secretos**: credenciales de base de datos, JWT y de los proveedores externos (Brevo, Twilio) se inyectan exclusivamente mediante variables de entorno (`${VARIABLE:}`), nunca como valores hardcodeados en el repositorio.

> Quedan identificadas dos mejoras pendientes: (1) corregir los 44 hallazgos de ESLint y, una vez resueltos, volver el paso de lint bloqueante en el pipeline; y (2) incorporar análisis estático al backend (por ejemplo, SonarQube/SonarCloud). Hasta entonces, en el backend la detección de problemas de calidad depende del criterio del desarrollador y del revisor, no de una herramienta objetiva.

### 6.2.2. Reviews

La revisión de código en NursePulse se apoya en los **Pull Requests de GitHub**, como se describe en el Capítulo V (sección 5.1.2) y el Capítulo VII (sección 7.2.1). Según el historial de los repositorios al 3 de octubre de 2026, se registraron 10 Pull Requests en Backend, 4 en Frontend, 4 en la aplicación móvil y 1 en la Landing Page. Varios del Backend siguen la convención de ramas descrita en el Capítulo V (`feature/sbar-structured-fields`, `feature/password-policy-ts01`, `fix/audit-log-null-metadata-and-500-handling`, entre otras).

Alcance real de esta práctica:

- **La rama de producción del Backend tiene protección activa desde el 3 de octubre de 2026**: `deploy/render-docker`, cuyo `push` despliega automáticamente a Render, cuenta con una regla de protección de rama que exige (a) Pull Request antes de fusionar, (b) la aprobación de otro integrante y (c) que el check `build-and-test` del workflow `Backend CI` finalice en éxito. La regla rige también para los administradores y bloquea el *force push* y el borrado de la rama. Es el único caso en que la revisión y el CI son condiciones técnicamente forzadas.
- **El resto de las ramas principales no tiene protección**: `main` del Backend, `main` del Frontend, `main` de Mobile y `main` de Landing no tienen reglas de protección. En ellas la revisión y el CI en verde siguen siendo prácticas del equipo, no condiciones que GitHub verifique.
- **Parte de los cambios se integró por `push` directo**: antes de activar la protección, y todavía hoy en las ramas sin ella, muchos commits se publicaron directamente a la rama principal, y cada `push` dispara el despliegue automático (ver Capítulo VII, sección 7.3). En esos casos la verificación recae en el pipeline de CI posterior al `push` y en la comprobación manual en producción (6.1.4).
- **Cuando hay Pull Request**, otro integrante revisa el cambio verificando correctitud funcional, cumplimiento de la guía de estilo (sección 6.2.1.1) y que no se introduzcan credenciales ni datos sensibles.

![Ejemplo de Pull Request revisado en el repositorio Backend, con sus verificaciones de CI](assets/chapter-6/pull-request-review.png)

No se utiliza una herramienta externa de gestión de revisiones (como Gerrit o Crucible); el proceso ocurre dentro de la interfaz nativa de Pull Requests de GitHub.

> Extender las mismas reglas de protección de rama (CI exitoso y una aprobación obligatoria antes de fusionar) a `main` del Backend, del Frontend, de Mobile y de Landing queda identificado como una mejora pendiente, para que la práctica de revisión sea verificable en todos los repositorios y no dependa de la disciplina del equipo.

## 6.3. Validation Interviews

> **⚠️ Sección pendiente de completar con información real.** Las subsecciones 6.3.1, 6.3.2 y 6.3.3 requieren los datos originales de las Validation Interviews y de la evaluación heurística ya referenciadas en el documento de "Conclusiones y Recomendaciones" (rama `docs/Conclusions`), que cita explícitamente "sección 6.3" y "sección 6.3.2". Para completarlas se necesita:
>
> 1. Las notas, grabaciones o transcripciones de las Validation Interviews realizadas (participantes, rol/ocupación, fecha, hallazgos).
> 2. El resultado de la evaluación heurística (heurísticas evaluadas, hallazgos y severidades encontradas).
>
> No se completó esta sección con datos inventados para no comprometer la integridad de la investigación de usuario del informe.

### 6.3.1. Diseño de Entrevistas

*(pendiente — ver nota arriba)*

### 6.3.2. Registro de Entrevistas

*(pendiente — ver nota arriba)*

### 6.3.3. Evaluaciones según heurísticas

*(pendiente — ver nota arriba)*