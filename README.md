# Conclusiones y Recomendaciones

### Conclusiones y recomendaciones

Esta sección contrasta los resultados obtenidos en las Validation Interviews (Capítulo VI, sección 6.3) frente a los Problem Statements, Assumptions e Hypothesis Statements planteados durante el proceso de Lean UX (sección 1.2.2).

**Sobre los Problem Statements**

- **Problem Statement 1 (personal de enfermería cardiovascular):** las entrevistas de validación confirmaron que la propuesta de valor de NursePulse se comprende con claridad y que la comunicación estructurada durante el traspaso de turno es percibida como un problema real. Sin embargo, las sesiones registradas evaluaron principalmente el Landing Page y la documentación de endpoints (Swagger), sin interacción directa con el formulario SBAR ni con el registro de signos vitales, por lo que este Problem Statement queda validado de forma parcial.
- **Problem Statement 2 (médicos especialistas cardiovasculares):** la muestra de entrevistas registrada en la sección 6.3.2 no identifica explícitamente a médicos especialistas entre los participantes, por lo que este Problem Statement todavía no cuenta con validación directa del segmento objetivo.
- **Problem Statement 3 (cliente institucional):** tampoco se registraron entrevistas con responsables institucionales (hospitales o clínicas), por lo que este Problem Statement permanece como validación pendiente.

**Sobre los Assumptions e Hypothesis Statements**

- El supuesto de que los usuarios valoran interfaces simples y directas (sección 1.2.2.2) se confirma parcialmente: los entrevistados destacaron la claridad del Landing Page, pero también señalaron que algunos términos técnicos y la navegación podían mejorar, lo que coincide con los hallazgos de severidad media de la evaluación heurística (relación con el mundo real, control del usuario y prevención de errores).
- La **Hipótesis 6 (Landing Page)** es la que cuenta con mayor evidencia de validación: los usuarios lograron identificar el propósito del sistema y su propuesta de valor sin apoyo adicional.
- Las **Hipótesis 1, 2, 3, 4 y 5** (traspaso SBAR, registro de signos vitales, vista resumida de evolución clínica, trazabilidad y alertas) no fueron validadas mediante interacción directa con la interfaz real de esos módulos, ya que las sesiones registradas se centraron en el Landing Page y en una simulación sobre la documentación Swagger del backend. Quedan como hipótesis abiertas para una siguiente ronda de validación con los prototipos interactivos de esas pantallas.

**Recomendaciones**

1. Ampliar las Validation Interviews a personal de enfermería y médicos especialistas cardiovasculares identificados explícitamente por su rol clínico, ya que la muestra actual (sección 6.3.2) no registra la ocupación de los participantes.
2. Diseñar sesiones de validación sobre el prototipo interactivo del formulario SBAR y del registro de signos vitales, para contrastar directamente las Hipótesis 1, 2, 3, 4 y 5.
3. Simplificar el lenguaje técnico expuesto a usuarios no especializados y mejorar la navegación, atendiendo los hallazgos de severidad media de la evaluación heurística.
4. Incorporar retroalimentación visual ante las acciones del usuario, señalada como punto débil en la evaluación heurística (prevención de errores).
5. Validar con instituciones de salud reales el modelo de precios SaaS (Essential, Professional, Enterprise) planteado en el Capítulo II, dado que el Problem Statement 3 aún no cuenta con validación directa.

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
