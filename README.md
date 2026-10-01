# Capítulo VI: Product Verification & Validation

## 6.1. Testing Suites & Validation

NursePulse cuenta con una suite de pruebas automatizadas de 61 pruebas en el backend (JUnit 5 + Mockito) y 25 pruebas en el frontend (Vitest), ejecutadas automáticamente en cada Pull Request mediante los workflows `Backend CI` y `Frontend CI` (ver Capítulo VII, sección 7.1).

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
- Generación de una alerta crítica → notificación SMS a médicos registrados (Twilio).
- Exportación del registro de auditoría a PDF, descargado y verificado directamente desde la interfaz.
- Flujo de permisos por rol (NURSE/DOCTOR/ADMIN) replicado en la interfaz real, no solo a nivel de API.

> Automatizar estos flujos con un framework de pruebas de sistema (end-to-end) queda identificado como una mejora pendiente, priorizada en las recomendaciones del proyecto.

## 6.2. Static testing & Verification
### 6.2.1. Static Code Analysis
#### 6.2.1.1. Coding standard & Code conventions
#### 6.2.1.2. Code Quality & Code Security
### 6.2.2. Reviews

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