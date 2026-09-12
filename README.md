## Capítulo III: Requirements Specification
### 3.1 To-Be Scenario Mapping

Para entender hacia dónde se dirige el producto, es necesario visualizar la experiencia deseada. Si el mapa del estado actual (*As-Is Scenario Mapping*) nos ayudó a diagnosticar los problemas de dispersión y demoras en el flujo clínico habitual, el **To-Be Scenario Mapping** (Mapa de Escenarios Futuros) es la herramienta de diseño de experiencia con la que proyectamos el **estado ideal** de interacción. 

Su propósito es modelar cómo el personal de salud (enfermeros y médicos especialistas) interactuará con **Nurse Pulse** para resolver sus tareas diarias, eliminando los cuellos de botella identificados. Este mapa organiza el recorrido en cuatro dimensiones clave:

- **Phases (Fases):** Las etapas cronológicas que atraviesa el usuario para completar un objetivo clínico (por ejemplo: recepción de guardia, registro a pie de cama, traspaso SBAR).
- **Doing (Acciones):** Las tareas operativas concretas que realiza el profesional dentro y fuera del sistema digital.
- **Thinking (Pensamientos):** Las preguntas, expectativas y razonamientos que pasan por la mente del profesional mientras ejecuta la tarea.
- **Feeling (Emociones):** La carga emocional y nivel de satisfacción del usuario a lo largo del proceso, evidenciando la reducción de estrés y el aumento de confianza y seguridad clínica.

---

#### Proceso metodológico desarrollado por el equipo

Para construir un escenario futuro viable, riguroso y centrado en las necesidades reales de los profesionales de la salud, el equipo de Nurse Pulse siguió un flujo de diseño iterativo de cinco pasos:

1. **Preparación:** El equipo consolidó los hallazgos del diagnóstico clínico, los *Lean UX Problem Statements* y los dolores documentados previamente en los mapas de estado actual (*As-Is*), definiendo los objetivos de eficiencia y trazabilidad esperados para cada segmento.
2. **Lluvia de ideas individual:** Cada integrante del equipo formuló propuestas de interacción digital enfocadas en resolver las fricciones existentes (por ejemplo: estandarización de formularios SBAR, alertas visuales automáticas y acceso consolidado a signos vitales desde dispositivos móviles y web).
3. **Revisión e identificación de fases:** Se agruparon las propuestas por afinidad funcional para establecer las columnas cronológicas que marcan el ciclo de trabajo del profesional de salud durante una jornada o turno.
4. **Nombrado y consolidación de fases:** Se nombraron las etapas de forma estandarizada y se completaron los carriles de *Phases*, *Doing*, *Thinking* y *Feeling* para cada User Persona representativo.
5. **Comparación y validación frente al As-Is:** Se contrastó cada paso del escenario futuro contra el escenario actual para garantizar que **Nurse Pulse** no introdujera pasos redundantes ni sobrecarga administrativa, verificando que los momentos de frustración y ansiedad del *As-Is* se transformen en certezas y tranquilidad en el *To-Be*.

---

#### Artefactos del To-Be Scenario Mapping

A continuación, se presentan los escenarios futuros proyectados para los dos segmentos objetivos del sistema.

##### A. To-Be Scenario Mapping: Personal de Enfermería Cardiovascular
*Enfocado en el flujo de recepción de turno, monitoreo continuo a pie de cama con la Native Mobile Application y entrega de guardia estandarizada mediante SBAR.*

<div align="center">

![To-Be Scenario Mapping - Personal de Enfermería](assets/Chapter-3/ScenarioEnfermeria.png)

</div>
<p align="center"><em>Figura 1.1 Mapa de escenario futuro para el personal de enfermería cardiovascular.</em></p>

---

##### B. To-Be Scenario Mapping: Médico Especialista Cardiovascular
*Enfocado en la ronda médica matutina, consulta rápida del estado del paciente en el Dashboard Web consolidado, toma de decisiones informada e indicación trazable de nuevas conductas médicas.*

<div align="center">

![To-Be Scenario Mapping - Médico Especialista](assets/Chapter-3/ScenariMedico.png)

</div>
<p align="center"><em>Figura 2.1 Mapa de escenario futuro para el médico especialista cardiovascular.</em></p>

---

#### Espacio de Trabajo Colaborativo

Para auditar en detalle la matriz completa de post-its virtuales, interacciones de usuario y trazabilidad de cada fase de los mapas *To-Be*, puede acceder al tablero colaborativo del proyecto en el siguiente enlace:

> 🔗 **Acceso al Tablero de Diseño (Miro / Canvas):**  
> [Ver To-Be Scenario Mapping interactivo en Miro](https://miro.com/app/board/uXjVHnjGnd0=/?share_link_id=39885473758)


### 3.2. User Stories

La presente sección desarrolla el conjunto de Epics, User Stories y Technical Stories definidos para el proyecto NursePulse. Estos requisitos fueron elaborados a partir de los hallazgos obtenidos en entrevistas, User Personas, User Task Matrix, User Journey Maps, Empathy Maps, Big Picture Event Storming, Ubiquitous Language y el avance desarrollado de la Landing Page.

Las User Stories representan necesidades funcionales desde la perspectiva de los usuarios finales y visitantes del sitio web. Las Technical Stories representan necesidades técnicas necesarias para implementar los recursos del RESTful API, utilizando el rol Developer. Asimismo, se incluyen historias correspondientes al sitio web estático o Landing Page, tomando como rol base al visitante, debido a que la página comunica la propuesta de valor, funcionamiento, características, beneficios, testimonios, equipo, preguntas frecuentes y canales de contacto de **Nurse Pulse**.

Los criterios de aceptación se redactan en formato Gherkin, siguiendo la estructura Given – When – Then. Además, se mantienen en tiempo presente, tercera persona, sin referencia innecesaria a detalles específicos de interfaz gráfica y con condiciones comprobables.

Cuadro de Epics, User Stories y Technical Stories

**Cuadro de Epics, User Stories y Technical Stories**

<!-- EP-01 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>—</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Landing Page informativa</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero conocer la propuesta de valor, funcionamiento, beneficios, planes y canales de contacto de Nurse Pulse para evaluar si la solución responde a necesidades clínicas de comunicación, trazabilidad y continuidad asistencial.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante accede al sitio web, <b>When</b> revisa la información disponible, <b>Then</b> comprende el propósito general de Nurse Pulse.<br><br>
      <b>Given</b> que el visitante desea conocer la solución, <b>When</b> navega por las secciones del sitio, <b>Then</b> encuentra información sobre propuesta de valor, funcionamiento, características, beneficios, planes, preguntas frecuentes, testimonios, equipo, llamados a la acción y contacto.
    </td>
  </tr>
</table>

<br>

<!-- EP-02 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>—</b></td>
    <td>Personal clínico</td>
    <td>Media</td>
    <td>EP-02</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Gestión de traspaso clínico SBAR</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como personal clínico, quiero estructurar la información del cambio de turno para reducir omisiones y mejorar la continuidad de atención.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el personal clínico realiza un cambio de turno, <b>When</b> registra información bajo estructura SBAR, <b>Then</b> la información queda organizada en situación, antecedentes, evaluación y recomendación.<br><br>
      <b>Given</b> que el nuevo turno recibe información, <b>When</b> consulta el traspaso clínico, <b>Then</b> comprende el estado del paciente y los pendientes relevantes.
    </td>
  </tr>
</table>

<br>

<!-- EP-03 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>—</b></td>
    <td>Personal clínico</td>
    <td>Media</td>
    <td>EP-03</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Registro y seguimiento clínico del paciente</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como personal clínico, quiero registrar y consultar información clínica relevante para mantener actualizado el estado del paciente cardiovascular.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el personal clínico registra información del paciente, <b>When</b> la información es guardada correctamente, <b>Then</b> queda disponible para seguimiento clínico.<br><br>
      <b>Given</b> que un profesional consulta al paciente, <b>When</b> accede a su información clínica, <b>Then</b> revisa datos relevantes para su atención.
    </td>
  </tr>
</table>

<br>

<!-- EP-04 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>—</b></td>
    <td>Equipo clínico</td>
    <td>Media</td>
    <td>EP-04</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Trazabilidad clínica</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como equipo clínico, quiero conocer la secuencia de eventos, responsables y horarios para mejorar seguimiento, auditoría y continuidad de atención.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que se registra una acción clínica, <b>When</b> la información queda guardada, <b>Then</b> se almacena responsable, fecha y hora.<br><br>
      <b>Given</b> que se consulta la trazabilidad de un paciente, <b>When</b> existen registros asociados, <b>Then</b> se muestra la secuencia de eventos clínicos registrados.
    </td>
  </tr>
</table>

<br>

<!-- EP-05 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>—</b></td>
    <td>Médico especialista cardiovascular</td>
    <td>Baja</td>
    <td>EP-05</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Soporte a la toma de decisiones clínicas</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como médico especialista cardiovascular, quiero acceder rápidamente a información consolidada para tomar decisiones clínicas oportunas y seguras.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el médico evalúa a un paciente cardiovascular, <b>When</b> consulta su información clínica, <b>Then</b> accede a datos relevantes para la toma de decisiones.<br><br>
      <b>Given</b> que existen cambios relevantes del paciente, <b>When</b> el médico revisa la evolución, <b>Then</b> identifica información clínica reciente.
    </td>
  </tr>
</table>

<br>

<!-- EP-06 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>—</b></td>
    <td>Developer</td>
    <td>Baja</td>
    <td>EP-06</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">RESTful API de Nurse Pulse</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como Developer, quiero contar con una API RESTful para exponer de forma segura los recursos clínicos necesarios para la aplicación Nurse Pulse.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que un cliente autorizado realiza una solicitud válida, <b>When</b> el API procesa la solicitud, <b>Then</b> responde con el recurso solicitado y código HTTP correspondiente.<br><br>
      <b>Given</b> que ocurre un error de validación o autorización, <b>When</b> el API procesa la solicitud, <b>Then</b> responde con código HTTP y mensaje consistente.
    </td>
  </tr>
</table>

<!-- US-01 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-01</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Visualizar landing page</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero visualizar la landing page de Nurse Pulse para conocer rápidamente la solución propuesta.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante accede al sitio web, <b>When</b> la página carga correctamente, <b>Then</b> visualiza información general de Nurse Pulse.<br><br>
      <b>Given</b> que el visitante usa un navegador compatible, <b>When</b> ingresa al sitio, <b>Then</b> visualiza el contenido principal sin errores de carga.
    </td>
  </tr>
</table>

<br>

<!-- US-02 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-02</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Ver propuesta de valor</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero conocer la propuesta de valor de Nurse Pulse para entender qué problema clínico busca resolver.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante revisa la información principal, <b>When</b> lee la propuesta presentada, <b>Then</b> identifica que Nurse Pulse se enfoca en comunicación clínica y trazabilidad en tiempo real.<br><br>
      <b>Given</b> que el visitante pertenece al sector salud, <b>When</b> revisa la propuesta de valor, <b>Then</b> reconoce beneficios relacionados con continuidad asistencial, trazabilidad de eventos críticos y comunicación entre turnos.
    </td>
  </tr>
</table>

<br>

<!-- US-03 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-03</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Consultar el problema que resuelve Nurse Pulse</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero entender por qué existe la necesidad de Nurse Pulse para reconocer el problema actual de información clínica dispersa.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante consulta la sección informativa del problema, <b>When</b> lee la explicación presentada, <b>Then</b> identifica que la información clínica dispersa dificulta la continuidad asistencial y la trazabilidad.<br><br>
      <b>Given</b> que el visitante analiza la necesidad del producto, <b>When</b> revisa el problema descrito, <b>Then</b> comprende que Nurse Pulse busca centralizar procesos esenciales de enfermería cardiovascular.
    </td>
  </tr>
</table>

<br>

<!-- US-04 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-04</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Revisar cómo funciona Nurse Pulse</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero conocer cómo funciona Nurse Pulse en pasos simples para comprender el flujo general de uso de la solución.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante revisa la explicación de funcionamiento, <b>When</b> consulta los pasos presentados, <b>Then</b> identifica las etapas generales de registro, monitoreo y trazabilidad.<br><br>
      <b>Given</b> que el visitante desea entender el funcionamiento general, <b>When</b> revisa los pasos descritos, <b>Then</b> comprende que la solución permite digitalizar traspasos SBAR, consultar información clínica y mantener historial de eventos.
    </td>
  </tr>
</table>

<br>

<!-- US-05 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-05</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Visualizar características clave</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero conocer las características principales de Nurse Pulse para evaluar si la solución responde a necesidades del entorno clínico cardiovascular.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante consulta la información de características, <b>When</b> revisa el contenido disponible, <b>Then</b> identifica capacidades relacionadas con SBAR digital, gestión de pacientes, seguimiento de tratamientos, monitoreo de signos vitales, historial clínico digital y trazabilidad.<br><br>
      <b>Given</b> que el visitante compara beneficios funcionales, <b>When</b> revisa cada característica presentada, <b>Then</b> comprende el valor de cada capacidad descrita.
    </td>
  </tr>
</table>

<br>

<!-- US-06 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-06</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Visualizar beneficios</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero revisar los beneficios de Nurse Pulse para comprender el valor que aporta al entorno clínico.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante consulta la información de beneficios, <b>When</b> revisa los beneficios disponibles, <b>Then</b> identifica mejoras relacionadas con comunicación entre turnos, reducción de omisiones, trazabilidad, organización de información y atención oportuna.<br><br>
      <b>Given</b> que el visitante evalúa la utilidad del producto, <b>When</b> revisa los beneficios, <b>Then</b> comprende cómo Nurse Pulse puede aportar valor a hospitales, clínicas o centros especializados.
    </td>
  </tr>
</table>

<br>

<!-- US-07 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-07</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Consultar preguntas frecuentes</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero revisar preguntas frecuentes para resolver dudas básicas sobre alcance, uso y modelo de servicio de Nurse Pulse.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante consulta las preguntas frecuentes, <b>When</b> revisa las respuestas disponibles, <b>Then</b> obtiene información sobre orientación del producto, consulta de información, público objetivo y modelo de servicio.<br><br>
      <b>Given</b> que el visitante tiene dudas sobre la solución, <b>When</b> revisa las preguntas frecuentes, <b>Then</b> encuentra respuestas claras sobre el alcance de Nurse Pulse.
    </td>
  </tr>
</table>

<br>

<!-- US-08 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-08</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Visualizar testimonios</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero revisar testimonios sobre Nurse Pulse para aumentar mi confianza en la solución.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante consulta los testimonios disponibles, <b>When</b> revisa las opiniones presentadas, <b>Then</b> identifica percepciones positivas relacionadas con organización, seguimiento y mejora del trabajo clínico.<br><br>
      <b>Given</b> que el visitante evalúa la credibilidad del producto, <b>When</b> lee los testimonios, <b>Then</b> obtiene información que respalda la propuesta de valor.
    </td>
  </tr>
</table>

<br>

<!-- US-09 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-09</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Conocer al equipo</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero conocer al equipo detrás de Nurse Pulse para identificar quiénes desarrollan la solución.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante consulta la información del equipo, <b>When</b> revisa los datos presentados, <b>Then</b> visualiza integrantes y roles asociados al proyecto.<br><br>
      <b>Given</b> que el visitante evalúa confianza institucional, <b>When</b> revisa el equipo del proyecto, <b>Then</b> reconoce que existe un equipo responsable detrás de la solución.
    </td>
  </tr>
</table>

<br>

<!-- US-10 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-10</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Contactar al equipo de Nurse Pulse</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero contactar al equipo de Nurse Pulse para solicitar información adicional o una demostración.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante desea contactar al equipo, <b>When</b> proporciona los datos requeridos, <b>Then</b> la solicitud queda lista para ser enviada.<br><br>
      <b>Given</b> que existen datos obligatorios, <b>When</b> el visitante intenta enviar información incompleta, <b>Then</b> el sistema solicita completar los datos requeridos.
    </td>
  </tr>
</table>

<br>

<!-- US-11 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-11</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Cambiar idioma del sitio</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero cambiar el idioma del sitio entre español e inglés para revisar la información en el idioma de mi preferencia.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante se encuentra en la landing page, <b>When</b> selecciona un idioma disponible, <b>Then</b> el contenido del sitio se muestra en el idioma seleccionado.<br><br>
      <b>Given</b> que el visitante vuelve a ingresar al sitio, <b>When</b> existe una preferencia de idioma guardada, <b>Then</b> el sitio mantiene el idioma previamente seleccionado.
    </td>
  </tr>
</table>

<br>

<!-- US-12 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-12</b></td>
    <td>Visitante</td>
    <td>Alta</td>
    <td>EP-01</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Acceder desde dispositivos móviles</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como visitante, quiero acceder al sitio web desde dispositivos móviles para revisar información de Nurse Pulse desde cualquier lugar.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el visitante accede desde un dispositivo móvil, <b>When</b> carga el sitio web, <b>Then</b> el contenido se adapta al tamaño del dispositivo.<br><br>
      <b>Given</b> que el visitante navega desde un dispositivo móvil, <b>When</b> revisa las secciones del sitio, <b>Then</b> consulta la información sin pérdida de contenido relevante.
    </td>
  </tr>
</table>

<br>

<!-- US-13 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-13</b></td>
    <td>Enfermera cardiovascular</td>
    <td>Media</td>
    <td>EP-02</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Registrar traspaso SBAR</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como enfermera cardiovascular, quiero registrar un traspaso clínico usando SBAR para comunicar información relevante al siguiente turno[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que la enfermera necesita entregar información clínica, <b>When</b> registra situación, antecedentes, evaluación y recomendación, <b>Then</b> el traspaso queda registrado con estructura SBAR[cite: 1, 2].<br><br>
      <b>Given</b> que falta información obligatoria, <b>When</b> la enfermera intenta guardar el traspaso, <b>Then</b> el sistema solicita completar la información requerida.
    </td>
  </tr>
</table>

<br>

<!-- US-14 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-14</b></td>
    <td>Enfermera entrante</td>
    <td>Media</td>
    <td>EP-02</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Consultar traspaso de turno</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como enfermera entrante, quiero consultar el traspaso clínico del turno anterior para continuar la atención del paciente sin perder información relevante[cite: 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que existe un traspaso registrado, <b>When</b> la enfermera entrante consulta la información del paciente, <b>Then</b> visualiza la información clínica entregada por el turno anterior[cite: 2].<br><br>
      <b>Given</b> que el traspaso contiene pendientes, <b>When</b> la enfermera lo revisa, <b>Then</b> identifica acciones pendientes para el nuevo turno.
    </td>
  </tr>
</table>

<br>

<!-- US-15 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-15</b></td>
    <td>Enfermera entrante</td>
    <td>Media</td>
    <td>EP-02</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Confirmar recepción de traspaso</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como enfermera entrante, quiero confirmar que recibí el traspaso clínico para dejar constancia de continuidad de atención[cite: 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que la enfermera entrante revisa el traspaso, <b>When</b> confirma la recepción, <b>Then</b> el sistema registra que el traspaso fue recibido.<br><br>
      <b>Given</b> que el traspaso aún no fue confirmado, <b>When</b> se consulta su estado, <b>Then</b> aparece como pendiente de recepción.
    </td>
  </tr>
</table>

<br>

<!-- US-16 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-16</b></td>
    <td>Enfermera cardiovascular</td>
    <td>Media</td>
    <td>EP-03</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Registrar signos vitales</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como enfermera cardiovascular, quiero registrar signos vitales del paciente para mantener actualizado el monitoreo clínico[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que la enfermera registra signos vitales, <b>When</b> ingresa los valores requeridos, <b>Then</b> el sistema guarda el registro asociado al paciente[cite: 1].<br><br>
      <b>Given</b> que falta un valor obligatorio, <b>When</b> la enfermera intenta guardar el registro, <b>Then</b> el sistema informa que falta información requerida.
    </td>
  </tr>
</table>

<br>

<!-- US-17 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-17</b></td>
    <td>Médico especialista cardiovascular</td>
    <td>Media</td>
    <td>EP-03</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Consultar evolución clínica</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como médico especialista cardiovascular, quiero consultar la evolución clínica reciente del paciente para tomar decisiones con información actualizada[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que existen registros clínicos del paciente, <b>When</b> el médico consulta su evolución, <b>Then</b> el sistema muestra eventos y registros recientes asociados al paciente[cite: 1, 2].<br><br>
      <b>Given</b> que no existen registros recientes, <b>When</b> el médico consulta la evolución, <b>Then</b> el sistema informa que no hay información registrada en el periodo consultado.
    </td>
  </tr>
</table>

<br>

<!-- US-18 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-18</b></td>
    <td>Enfermera cardiovascular</td>
    <td>Media</td>
    <td>EP-03</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Registrar evento clínico relevante</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como enfermera cardiovascular, quiero registrar eventos clínicos relevantes para que el equipo pueda dar seguimiento oportuno al paciente[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que ocurre un evento clínico relevante, <b>When</b> la enfermera registra el evento, <b>Then</b> el sistema guarda descripción, fecha, hora y responsable[cite: 1, 2].<br><br>
      <b>Given</b> que un médico consulta la evolución del paciente, <b>When</b> existen eventos relevantes registrados, <b>Then</b> aparecen asociados al historial clínico del paciente[cite: 1, 2].
    </td>
  </tr>
</table>

<br>

<!-- US-19 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-19</b></td>
    <td>Médico especialista cardiovascular</td>
    <td>Media</td>
    <td>EP-04</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Consultar historial de eventos</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como médico especialista cardiovascular, quiero consultar el historial de eventos clínicos para reconstruir la evolución del paciente[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el paciente tiene eventos registrados, <b>When</b> el médico consulta el historial, <b>Then</b> el sistema muestra los eventos ordenados cronológicamente[cite: 1, 2].<br><br>
      <b>Given</b> que el médico necesita validar un evento específico, <b>When</b> revisa el historial, <b>Then</b> identifica fecha, hora y responsable del registro[cite: 1, 2].
    </td>
  </tr>
</table>

<br>

<!-- US-20 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-20</b></td>
    <td>Usuario clínico</td>
    <td>Baja</td>
    <td>EP-04</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Identificar responsable de registro</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como usuario clínico, quiero identificar quién registró una información clínica para asegurar trazabilidad y responsabilidad profesional[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que existe un registro clínico guardado, <b>When</b> el usuario consulta el detalle del registro, <b>Then</b> el sistema muestra el responsable asociado[cite: 1, 2].<br><br>
      <b>Given</b> que el registro fue actualizado, <b>When</b> se consulta su información, <b>Then</b> el sistema conserva evidencia del responsable de la actualización[cite: 1, 2].
    </td>
  </tr>
</table>

<br>

<!-- US-21 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-21</b></td>
    <td>Médico especialista cardiovascular</td>
    <td>Baja</td>
    <td>EP-05</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Consultar resumen clínico del paciente</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como médico especialista cardiovascular, quiero consultar un resumen clínico del paciente para comprender rápidamente su estado actual[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que el paciente tiene información clínica registrada, <b>When</b> el médico consulta el resumen, <b>Then</b> el sistema muestra datos relevantes del estado actual del paciente[cite: 2].<br><br>
      <b>Given</b> que existe información reciente, <b>When</b> el médico revisa el resumen, <b>Then</b> identifica evolución, eventos e indicaciones relevantes[cite: 1, 2].
    </td>
  </tr>
</table>

<br>

<!-- US-22 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>US-22</b></td>
    <td>Médico especialista cardiovascular</td>
    <td>Baja</td>
    <td>EP-05</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Identificar cambios críticos</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como médico especialista cardiovascular, quiero identificar cambios críticos del paciente para responder oportunamente ante deterioros clínicos[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que existen registros clínicos recientes, <b>When</b> se identifica un cambio crítico definido por reglas clínicas, <b>Then</b> el sistema marca el evento como relevante[cite: 1, 2].<br><br>
      <b>Given</b> que el médico consulta la evolución, <b>When</b> existen cambios críticos registrados, <b>Then</b> puede identificarlos dentro del historial del paciente[cite: 1, 2].
    </td>
  </tr>
</table>

<br>

<!-- TS-01 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>TS-01</b></td>
    <td>Developer</td>
    <td>Baja</td>
    <td>EP-06</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Autenticación de usuarios</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como Developer, quiero implementar autenticación para proteger el acceso a recursos clínicos del sistema, incluyendo una política de contraseñas seguras en el registro de nuevas cuentas[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que un usuario envía credenciales válidas, <b>When</b> el API procesa la autenticación, <b>Then</b> responde con un token válido.<br><br>
      <b>Given</b> que un usuario envía credenciales inválidas, <b>When</b> el API procesa la autenticación, <b>Then</b> responde con estado 401.<br><br>
      <b>Given</b> que un usuario se registra con una contraseña de entre 12 y 20 caracteres, que incluye al menos una mayúscula y un carácter especial, <b>When</b> el API procesa el registro, <b>Then</b> crea la cuenta correctamente.<br><br>
      <b>Given</b> que un usuario se registra con una contraseña que no cumple la longitud requerida, <b>When</b> el API procesa el registro, <b>Then</b> responde con estado 400 indicando el requisito de longitud.<br><br>
      <b>Given</b> que un usuario se registra con una contraseña sin mayúscula o sin carácter especial, <b>When</b> el API procesa el registro, <b>Then</b> responde con estado 400 indicando qué requisito de complejidad falta.
    </td>
  </tr>
</table>

<br>

<!-- TS-02 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>TS-02</b></td>
    <td>Developer</td>
    <td>Baja</td>
    <td>EP-06</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Gestión de pacientes mediante API</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como Developer, quiero exponer endpoints de pacientes para crear, consultar y actualizar información básica del paciente cardiovascular[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que un cliente autorizado solicita un paciente existente, <b>When</b> el API recibe la solicitud, <b>Then</b> responde con la información del paciente y estado 200.<br><br>
      <b>Given</b> que el paciente no existe, <b>When</b> el API recibe la solicitud, <b>Then</b> responde con estado 404.
    </td>
  </tr>
</table>

<br>

<!-- TS-03 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>TS-03</b></td>
    <td>Developer</td>
    <td>Baja</td>
    <td>EP-06</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Gestión de registros clínicos mediante API</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como Developer, quiero exponer endpoints de registros clínicos para permitir el registro y consulta de signos vitales, eventos e indicaciones[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que un cliente autorizado envía un registro clínico válido, <b>When</b> el API procesa la solicitud, <b>Then</b> guarda el registro y responde con estado 201.<br><br>
      <b>Given</b> que el registro clínico contiene datos inválidos, <b>When</b> el API procesa la solicitud, <b>Then</b> responde con estado 400 y detalle de validación.
    </td>
  </tr>
</table>

<br>

<!-- TS-04 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>TS-04</b></td>
    <td>Developer</td>
    <td>Baja</td>
    <td>EP-06</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Gestión de traspasos SBAR mediante API</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como Developer, quiero implementar endpoints de traspasos SBAR para registrar y consultar entregas de turno[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que un cliente autorizado envía un traspaso SBAR válido, <b>When</b> el API procesa la solicitud, <b>Then</b> guarda el traspaso asociado al paciente y responde con estado 201[cite: 1, 2].<br><br>
      <b>Given</b> que falta un campo requerido del SBAR, <b>When</b> el API procesa la solicitud, <b>Then</b> responde con estado 400[cite: 1, 2].
    </td>
  </tr>
</table>

<br>

<!-- TS-05 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>TS-05</b></td>
    <td>Developer</td>
    <td>Baja</td>
    <td>EP-06</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Trazabilidad de acciones clínicas</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como Developer, quiero registrar auditoría de acciones clínicas para conservar responsable, fecha y tipo de operación realizada[cite: 1, 2].</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que un usuario autorizado crea o actualiza un registro clínico, <b>When</b> el API completa la operación, <b>Then</b> almacena usuario, fecha, hora y tipo de acción[cite: 1, 2].<br><br>
      <b>Given</b> que se consulta la auditoría de un registro, <b>When</b> existe información de trazabilidad, <b>Then</b> el API responde con la secuencia de acciones registradas[cite: 1, 2].
    </td>
  </tr>
</table>

<br>

<!-- TS-06 -->
<table width="100%">
  <tr>
    <th width="20%">Story ID</th>
    <th width="30%">User</th>
    <th width="25%">Priority</th>
    <th width="25%">Epic</th>
  </tr>
  <tr>
    <td align="center"><b>TS-06</b></td>
    <td>Developer</td>
    <td>Baja</td>
    <td>EP-06</td>
  </tr>
  <tr>
    <th>Title</th>
    <td colspan="3">Manejo consistente de errores del API</td>
  </tr>
  <tr>
    <th colspan="4">Description</th>
  </tr>
  <tr>
    <td colspan="4">Como Developer, quiero estandarizar las respuestas de error para facilitar el consumo del API por parte del frontend.</td>
  </tr>
  <tr>
    <th colspan="4">Acceptance Criteria</th>
  </tr>
  <tr>
    <td colspan="4">
      <b>Given</b> que ocurre un error de validación, <b>When</b> el API responde, <b>Then</b> incluye código HTTP 400 y detalle del error.<br><br>
      <b>Given</b> que un usuario no autorizado solicita un recurso protegido, <b>When</b> el API procesa la solicitud, <b>Then</b> responde con estado 401 o 403 según corresponda.
    </td>
  </tr>
</table>


#### Resumen de Epics, User Stories y Technical Stories

| Epic ID   | Bloque                                      | Historias relacionadas | Propósito                                                                                                                                                      |
|-----------|---------------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EP-01** | Landing Page informativa                    | US-01 a US-12          | Comunicar la propuesta de valor de Nurse Pulse, explicar el problema, presentar beneficios, generar confianza y facilitar contacto con visitantes interesados. |
| **EP-02** | Gestión de traspaso clínico SBAR            | US-13 a US-15          | Estructurar la comunicación clínica durante cambios de turno mediante el modelo SBAR.                                                                          |
| **EP-03** | Registro y seguimiento clínico del paciente | US-16 a US-18          | Registrar información clínica relevante como signos vitales, eventos clínicos.                                                |
| **EP-04** | Trazabilidad clínica                        | US-19 a US-21          | Consultar historial, responsables y cumplimiento de indicaciones para fortalecer seguimiento, auditoría y continuidad clínica.                                 |
| **EP-05** | Soporte a la toma de decisiones clínicas    | US-22 a US-23          | Facilitar consulta de información consolidada, identificación de cambios críticos y validación de información con enfermería.                                  |
| **EP-06** | RESTful API de Nurse Pulse                  | TS-01 a TS-06          | Implementar recursos técnicos del backend necesarios para exponer pacientes, registros clínicos, traspasos, trazabilidad, autenticación y manejo de errores.   |

La distribución de Epics, User Stories y Technical Stories permite mantener trazabilidad entre la investigación de usuarios, los Business Goals, el Impact Mapping, el Product Backlog y las funcionalidades implementadas en los sprints del proyecto.

### 3.3. Product Backlog

La presente sección desarrolla el Product Backlog del proyecto Nurse Pulse, incluyendo la priorización y estimación de las User Stories y Technical Stories definidas previamente. El orden del backlog se establece considerando el valor para el negocio, la validación temprana del producto, la relación con los Business Goals y la necesidad de contar con una primera versión funcional del sistema.

De acuerdo con el criterio solicitado, las historias relacionadas con el sitio web estático o Landing Page se consideran desde el primer sprint, ya que permiten comunicar la propuesta de valor, captar visitantes interesados y validar el interés inicial del mercado. Posteriormente se priorizan las funcionalidades clínicas centrales relacionadas con traspaso SBAR, registro clínico, trazabilidad, consulta de información y soporte a la toma de decisiones.

La estimación se realiza utilizando Story Points con valores **1, 2, 3, 5 y 8**, considerando complejidad funcional, esfuerzo técnico, validaciones requeridas, dependencias y riesgo de implementación.

#### Criterios de priorización

| Criterio | Descripción |
| -------- | ----------- |
| **Valor para el negocio** | Se priorizan primero las historias que permiten comunicar la propuesta de valor, validar interés inicial y demostrar funcionalidad clínica central. |
| **Relación con Business Goals** | Las historias se ordenan considerando su aporte a los objetivos definidos en el Impact Mapping. |
| **Validación temprana** | Se colocan primero historias que permiten obtener retroalimentación de visitantes, usuarios clínicos y potenciales clientes institucionales. |
| **Dependencias funcionales** | Algunas historias requieren que primero existan pacientes, registros, traspasos o recursos base del sistema. |
| **Riesgo técnico** | Las Technical Stories se priorizan según su necesidad para soportar funcionalidades clínicas y no únicamente por seguridad o autenticación. |
| **Alcance por sprints** | El backlog considera la evolución del producto desde Landing Page hasta Web Application, RESTful API, validación y cierre final. |

#### Product Backlog — Nurse Pulse

| # Orden | User Story Id | Título | Descripción | Story Points |
| ------: | ------------- | ------ | ----------- | -----------: |
| 1 | US-01 | Visualizar landing page | Como visitante, deseo visualizar la landing page de Nurse Pulse para conocer rápidamente la solución propuesta. | 3 |
| 2 | US-02 | Ver propuesta de valor | Como visitante, deseo conocer la propuesta de valor de Nurse Pulse para entender qué problema clínico busca resolver. | 3 |
| 3 | US-03 | Consultar el problema que resuelve Nurse Pulse | Como visitante, deseo entender por qué existe la necesidad de Nurse Pulse para reconocer el problema actual de información clínica dispersa. | 3 |
| 4 | US-04 | Revisar cómo funciona Nurse Pulse | Como visitante, deseo conocer cómo funciona Nurse Pulse en pasos simples para comprender el flujo general de uso de la solución. | 3 |
| 5 | US-05 | Visualizar características clave | Como visitante, deseo conocer las características principales de Nurse Pulse para evaluar si la solución responde a necesidades del entorno clínico cardiovascular. | 3 |
| 6 | US-06 | Visualizar beneficios | Como visitante, deseo revisar los beneficios de Nurse Pulse para comprender el valor que aporta al entorno clínico. | 3 |
| 7 | US-10 | Contactar al equipo de Nurse Pulse | Como visitante, deseo contactar al equipo de Nurse Pulse para solicitar información adicional o una demostración. | 5 |
| 8 | US-12 | Acceder desde dispositivos móviles | Como visitante, deseo acceder al sitio web desde dispositivos móviles para revisar información de Nurse Pulse desde cualquier lugar. | 5 |
| 9 | US-11 | Cambiar idioma del sitio | Como visitante, deseo cambiar el idioma del sitio entre español e inglés para revisar la información en el idioma de mi preferencia. | 5 |
| 10 | US-07 | Consultar preguntas frecuentes | Como visitante, deseo revisar preguntas frecuentes para resolver dudas básicas sobre alcance, uso y modelo de servicio de Nurse Pulse. | 2 |
| 11 | US-08 | Visualizar testimonios | Como visitante, deseo revisar testimonios sobre Nurse Pulse para aumentar mi confianza en la solución. | 2 |
| 12 | US-09 | Conocer al equipo | Como visitante, deseo conocer al equipo detrás de Nurse Pulse para identificar quiénes desarrollan la solución. | 2 |
| 13 | US-13 | Registrar traspaso SBAR | Como enfermera cardiovascular, deseo registrar un traspaso clínico usando SBAR para comunicar información relevante al siguiente turno. | 8 |
| 14 | US-14 | Consultar traspaso de turno | Como enfermera entrante, deseo consultar el traspaso clínico del turno anterior para continuar la atención del paciente sin perder información relevante. | 5 |
| 15 | US-15 | Confirmar recepción de traspaso | Como enfermera entrante, deseo confirmar que recibí el traspaso clínico para dejar constancia de continuidad de atención. | 3 |
| 16 | US-16 | Registrar signos vitales | Como enfermera cardiovascular, deseo registrar signos vitales del paciente para mantener actualizado el monitoreo clínico. | 5 |
| 17 | US-19 | Registrar evento clínico relevante | Como enfermera cardiovascular, deseo registrar eventos clínicos relevantes para que el equipo pueda dar seguimiento oportuno al paciente. | 5 |
| 18 | US-17 | Consultar evolución clínica | Como médico especialista cardiovascular, deseo consultar la evolución clínica reciente del paciente para tomar decisiones con información actualizada. | 5 |
| 20 | US-23 | Consultar resumen clínico del paciente | Como médico especialista cardiovascular, deseo consultar un resumen clínico del paciente para comprender rápidamente su estado actual. | 8 |
| 21 | US-20 | Consultar historial de eventos | Como médico especialista cardiovascular, deseo consultar el historial de eventos clínicos para reconstruir la evolución del paciente. | 5 |
| 22 | US-21 | Identificar responsable de registro | Como usuario clínico, deseo identificar quién registró una información clínica para asegurar trazabilidad y responsabilidad profesional. | 5 |
| 23 | US-24 | Identificar cambios críticos | Como médico especialista cardiovascular, deseo identificar cambios críticos del paciente para responder oportunamente ante deterioros clínicos. | 8 |
| 24 | TS-02 | Gestión de pacientes mediante API | Como Developer, deseo exponer endpoints de pacientes para crear, consultar y actualizar información básica del paciente cardiovascular. | 5 |
| 25 | TS-03 | Gestión de registros clínicos mediante API | Como Developer, deseo exponer endpoints de registros clínicos para permitir el registro y consulta de signos vitales, eventos e indicaciones. | 8 |
| 26 | TS-04 | Gestión de traspasos SBAR mediante API | Como Developer, deseo implementar endpoints de traspasos SBAR para registrar y consultar entregas de turno. | 5 |
| 27 | TS-05 | Trazabilidad de acciones clínicas | Como Developer, deseo registrar auditoría de acciones clínicas para conservar responsable, fecha y tipo de operación realizada. | 5 |
| 28 | TS-01 | Autenticación de usuarios | Como Developer, deseo implementar autenticación para proteger el acceso a recursos clínicos del sistema. | 5 |
| 29 | TS-06 | Manejo consistente de errores del API | Como Developer, deseo estandarizar las respuestas de error para facilitar el consumo del API por parte del frontend. | 3 |

#### Distribución por bloques funcionales

| Bloque | Historias incluidas | Propósito |
| ------ | ------------------- | --------- |
| **Landing Page** | US-01 a US-12 | Comunicar la propuesta de valor, captar interesados y validar interés inicial. |
| **Traspaso SBAR** | US-13 a US-15 | Mejorar comunicación clínica durante cambios de turno. |
| **Registro clínico** | US-16, US-18, US-19 | Reducir duplicidad, registrar información relevante y disminuir dependencia de papel. |
| **Consulta clínica** | US-17, US-20, US-23 | Facilitar acceso rápido a evolución, historial y estado actual del paciente. |
| **Trazabilidad clínica** | US-21, US-22 | Reconstruir responsables, horarios y cumplimiento de indicaciones. |
| **Soporte a decisiones clínicas** | US-24, US-25 | Identificar cambios críticos y validar información relevante con enfermería. |
| **RESTful API** | TS-01 a TS-06 | Habilitar recursos técnicos para pacientes, registros, traspasos, trazabilidad, autenticación y errores. |

#### Relación del Product Backlog con los Business Goals

| Business Goal | Historias principales relacionadas | Justificación |
| ------------- | ---------------------------------- | ------------- |
| **BG-01** | US-01 a US-12 | Estas historias permiten comunicar el valor de Nurse Pulse, generar confianza y facilitar contacto desde la Landing Page. |
| **BG-02** | US-13, US-14, US-15, TS-04 | Estas historias permiten validar el flujo de traspaso SBAR digital con usuarios clínicos e instituciones. |
| **BG-03** | US-16, US-17, US-20, US-23 | Estas historias reducen fricción al registrar y consultar información clínica relevante. |
| **BG-04** | US-13, US-16, US-18, US-19, TS-02, TS-03, TS-04 | Estas historias permiten reemplazar registros físicos complementarios por flujos digitales funcionales. |
| **BG-05** | US-20, US-21, US-22, US-24, US-25, TS-01, TS-05, TS-06 | Estas historias fortalecen trazabilidad clínica, seguridad, auditoría y soporte a decisiones clínicas. |

#### Relación del Product Backlog con los sprints

| Sprint | Historias principales consideradas | Enfoque |
| ------ | --------------------------------- | ------- |
| **Sprint 1** | US-01, US-02, US-03, US-04, US-05, US-06, US-07, US-08, US-09, US-10, US-11, US-12, US-13, US-14, US-15, US-16, US-17, US-18, US-19, US-20, US-21, US-22 | Desarrollo inicial de Landing Page, comunicación de propuesta de valor, secciones principales, contacto y responsive design. Mejora de Landing Page, primeras vistas de Web Application, traspaso SBAR, signos vitales y consulta clínica inicial  Implementación de Web Services, registros clínicos, eventos, trazabilidad, endpoints REST y documentación de API. Cierre de funcionalidades, validación final, autenticación, manejo de errores, evidencias finales y mejoras del producto.
|

#### Captura y URL del Product Backlog

La siguiente captura corresponde al Product Backlog elaborado en la herramienta de gestión utilizada por el equipo. En ella se evidencia la priorización de historias, estimación mediante Story Points y organización del backlog según valor para el negocio.

<p align="center">
  <img src="assets/chapter-3/product-backlog.png" alt="Product Backlog Nurse Pulse" width="850">
</p>

**URL del Product Backlog:**  
https://docs.google.com/spreadsheets/d/1JWzVr2lEd1AoSZBmGx0D0B3Pd09Je_w_lRHvN-_5y40/edit?usp=sharing

#### Conclusión del Product Backlog

El Product Backlog de Nurse Pulse prioriza primero las historias relacionadas con la Landing Page porque permiten comunicar la propuesta de valor, presentar beneficios, mostrar planes, validar interés inicial y obtener contacto con visitantes interesados mediante llamados a la acción. Luego se priorizan funcionalidades clínicas centrales relacionadas con traspaso SBAR, registro de signos vitales, eventos clínicos, consulta de evolución, trazabilidad y soporte a decisiones clínicas.

Las Technical Stories se ubican después de las historias funcionales principales porque su propósito es habilitar técnicamente los recursos necesarios para la Web Application y el RESTful API. Esta organización evita priorizar autenticación o seguridad al inicio sin una relación directa con valor de negocio visible, y mantiene coherencia con el enfoque solicitado para el Product Backlog.


### 3.4. Impact Mapping

La presente sección desarrolla el Impact Mapping del proyecto Nurse Pulse, elaborado para el modelo de negocio digital a partir de los User Personas, User Stories, User Journey Maps, Empathy Maps, Big Picture Event Storming y Ubiquitous Language.

El Impact Mapping permite conectar los objetivos de negocio con los actores que pueden contribuir a lograrlos, los cambios de comportamiento esperados, los entregables digitales necesarios y las User Stories que permiten construir dichos entregables. De esta manera, se evita que las funcionalidades sean definidas de forma aislada y se mantiene trazabilidad entre investigación, requerimientos, diseño e implementación.

La estructura utilizada responde a las siguientes preguntas:

| Elemento | Pregunta que responde |
| -------- | --------------------- |
| **Business Goal** | ¿Qué objetivo de negocio se quiere alcanzar? |
| **Actor / Persona** | ¿Quién puede ayudar a lograr la meta? |
| **Impact** | ¿Qué tendría que hacer el actor para contribuir al objetivo? |
| **Deliverable** | ¿Qué puede construir el negocio digital para provocar ese impacto? |
| **User Stories** | ¿Qué historias permiten desarrollar los features necesarios para producir los entregables? |

Para este proyecto se consideran Business Goals definidos bajo criterios SMART, los User Personas previamente identificados y las User Stories del backlog del proyecto Nurse Pulse.

#### Business Goals SMART

| Business Goal ID | Business Goal SMART |
| ---------------- | ------------------- |
| **BG-01** | Lograr que al menos **60 visitantes interesados** soliciten información o una demostración de Nurse Pulse mediante la Landing Page durante los primeros **4 meses** posteriores a su publicación. |
| **BG-02** | Conseguir que al menos **3 instituciones de salud o áreas clínicas cardiovasculares** validen el flujo de traspaso SBAR digital durante los primeros **6 meses** del proyecto. |
| **BG-03** | Reducir en un **30% el tiempo estimado de búsqueda y revisión de información clínica relevante** durante escenarios simulados de UCI cardiovascular en un periodo de **6 meses**. |
| **BG-04** | Lograr que al menos el **80% de usuarios clínicos participantes en pruebas piloto** registre eventos clínicos, signos vitales o traspasos usando Nurse Pulse sin recurrir a registros físicos complementarios en un periodo de **8 meses**. |
| **BG-05** | Alcanzar un nivel mínimo de **85% de trazabilidad completa** en eventos clínicos registrados durante pruebas piloto, considerando responsable, fecha, hora y tipo de acción, en un periodo de **8 meses**. |

#### Actors / Personas considerados

| Actor / Persona | Relación con Nurse Pulse |
| --------------- | ------------------------ |
| **Visitante de la Landing Page** | Persona interesada en conocer la solución, revisar beneficios, evaluar confianza y solicitar información o una demostración. |
| **Daniela Ríos — Personal de enfermería cardiovascular** | User Persona encargado de registrar signos vitales, eventos clínicos, administración y traspasos SBAR durante el turno. |
| **Dr. Alejandro Torres — Médico especialista cardiovascular** | User Persona encargado de consultar información clínica, validar evolución del paciente y tomar decisiones médicas oportunas. |
| **Cliente institucional** | Hospital, clínica privada o centro especializado en cardiología que puede adoptar Nurse Pulse para mejorar procesos internos. |
| **Developer** | Actor técnico encargado de implementar y consumir recursos del RESTful API que soportan la Web Application. |

#### Capturas del Impact Mapping

El Impact Mapping visual fue elaborado en una herramienta colaborativa y organizado en tres capturas para facilitar su lectura. Cada captura relaciona Business Goals, actores, impactos, entregables y User Stories asociadas.

<p align="center">
  <img src="assets/chapter-3/impact-mapping-bg01-bg02.png" alt="Impact Mapping BG-01 y BG-02" width="850">
</p>

<p align="center">
  <img src="assets/chapter-3/impact-mapping-bg03-bg04.png" alt="Impact Mapping BG-03 y BG-04" width="850">
</p>

<p align="center">
  <img src="assets/chapter-3/impact-mapping-bg05.png" alt="Impact Mapping BG-05" width="850">
</p>

#### Impact Mapping detallado

Debido a que las capturas visuales presentan los identificadores principales para mantener legibilidad, la siguiente tabla detalla la relación completa entre Business Goals, actores, impactos esperados, entregables digitales y User Stories asociadas.

| Business Goal | Actor / Persona | Impact esperado | Deliverable | User Stories relacionadas |
| ------------- | --------------- | --------------- | ----------- | ------------------------- |
| **BG-01** | Visitante de la Landing Page | Comprender rápidamente qué es Nurse Pulse, qué problema resuelve y por qué puede aportar valor al entorno clínico cardiovascular. | Landing Page informativa con propuesta de valor, explicación del problema, funcionamiento y beneficios. | **US-01:** Como visitante, deseo visualizar la landing page de Nurse Pulse para conocer rápidamente la solución propuesta. <br><br> **US-02:** Como visitante, deseo conocer la propuesta de valor de Nurse Pulse para entender qué problema clínico busca resolver. <br><br> **US-03:** Como visitante, deseo entender por qué existe la necesidad de Nurse Pulse para reconocer el problema actual de información clínica dispersa. |
| **BG-01** | Visitante de la Landing Page | Evaluar confianza, resolver dudas y decidir si desea solicitar información adicional. | Secciones de características, beneficios, planes, preguntas frecuentes, testimonios, equipo, llamados a la acción y contacto. | **US-04:** Como visitante, deseo conocer cómo funciona Nurse Pulse en pasos simples para comprender el flujo general de uso de la solución. <br><br> **US-05:** Como visitante, deseo conocer las características principales de Nurse Pulse para evaluar si la solución responde a necesidades del entorno clínico cardiovascular. <br><br> **US-06:** Como visitante, deseo revisar los beneficios de Nurse Pulse para comprender el valor que aporta al entorno clínico. <br><br> **US-07:** Como visitante, deseo revisar preguntas frecuentes para resolver dudas básicas sobre alcance, uso y modelo de servicio de Nurse Pulse. <br><br> **US-08:** Como visitante, deseo revisar testimonios sobre Nurse Pulse para aumentar mi confianza en la solución. <br><br> **US-09:** Como visitante, deseo conocer al equipo detrás de Nurse Pulse para identificar quiénes desarrollan la solución. <br><br> **US-10:** Como visitante, deseo contactar al equipo de Nurse Pulse para solicitar información adicional o una demostración. |
| **BG-01** | Visitante de la Landing Page | Acceder a la información desde distintos dispositivos y revisar el contenido en su idioma de preferencia. | Landing Page responsive e internacionalizada. | **US-11:** Como visitante, deseo cambiar el idioma del sitio entre español e inglés para revisar la información en el idioma de mi preferencia. <br><br> **US-12:** Como visitante, deseo acceder al sitio web desde dispositivos móviles para revisar información de Nurse Pulse desde cualquier lugar. |
| **BG-02** | Daniela Ríos — Personal de enfermería cardiovascular | Registrar información del cambio de turno de manera estructurada para reducir omisiones y mejorar continuidad clínica. | Módulo de traspaso clínico SBAR. | **US-13:** Como enfermera cardiovascular, deseo registrar un traspaso clínico usando SBAR para comunicar información relevante al siguiente turno. <br><br> **US-14:** Como enfermera entrante, deseo consultar el traspaso clínico del turno anterior para continuar la atención del paciente sin perder información relevante. <br><br> **US-15:** Como enfermera entrante, deseo confirmar que recibí el traspaso clínico para dejar constancia de continuidad de atención. |
| **BG-02** | Cliente institucional | Validar si el flujo SBAR digital puede aplicarse como apoyo operativo dentro de áreas cardiovasculares. | Flujo demostrable de traspaso SBAR, evidencias de uso, documentación del proceso y validación con usuarios. | **US-13:** Como enfermera cardiovascular, deseo registrar un traspaso clínico usando SBAR para comunicar información relevante al siguiente turno. <br><br> **US-14:** Como enfermera entrante, deseo consultar el traspaso clínico del turno anterior para continuar la atención del paciente sin perder información relevante. <br><br> **TS-04:** Como Developer, deseo implementar endpoints de traspasos SBAR para registrar y consultar entregas de turno. |
| **BG-03** | Dr. Alejandro Torres — Médico especialista cardiovascular | Consultar información clínica consolidada y reducir el tiempo de búsqueda entre múltiples fuentes. | Vista de evolución clínica, resumen clínico del paciente e historial de eventos. | **US-17:** Como médico especialista cardiovascular, deseo consultar la evolución clínica reciente del paciente para tomar decisiones con información actualizada. <br><br> **US-20:** Como médico especialista cardiovascular, deseo consultar el historial de eventos clínicos para reconstruir la evolución del paciente. <br><br> **US-22:** Como médico especialista cardiovascular, deseo consultar un resumen clínico del paciente para comprender rápidamente su estado actual. |
| **BG-03** | Daniela Ríos — Personal de enfermería cardiovascular | Registrar información clínica de manera ordenada para que luego pueda ser consultada con menor fricción por otros profesionales. | Formularios de registro clínico para signos vitales y eventos relevantes. | **US-16:** Como enfermera cardiovascular, deseo registrar signos vitales del paciente para mantener actualizado el monitoreo clínico. <br><br> **US-18:** Como enfermera cardiovascular, deseo registrar eventos clínicos relevantes para que el equipo pueda dar seguimiento oportuno al paciente. |
| **BG-04** | Daniela Ríos — Personal de enfermería cardiovascular | Registrar signos vitales, eventos y traspasos en un flujo digital para reducir dependencia de apuntes físicos complementarios. | Módulos digitales de registro clínico, eventos relevantes y traspaso SBAR. | **US-13:** Como enfermera cardiovascular, deseo registrar un traspaso clínico usando SBAR para comunicar información relevante al siguiente turno. <br><br> **US-16:** Como enfermera cardiovascular, deseo registrar signos vitales del paciente para mantener actualizado el monitoreo clínico. <br><br> **US-18:** Como enfermera cardiovascular, deseo registrar eventos clínicos relevantes para que el equipo pueda dar seguimiento oportuno al paciente. |
| **BG-04** | Developer | Exponer recursos técnicos que permitan al frontend registrar y consultar información clínica desde el RESTful API. | Endpoints de pacientes, registros clínicos, traspasos y manejo consistente de errores. | **TS-02:** Como Developer, deseo exponer endpoints de pacientes para crear, consultar y actualizar información básica del paciente cardiovascular. <br><br> **TS-03:** Como Developer, deseo exponer endpoints de registros clínicos para permitir el registro y consulta de signos vitales, eventos e indicaciones. <br><br> **TS-04:** Como Developer, deseo implementar endpoints de traspasos SBAR para registrar y consultar entregas de turno. <br><br> **TS-06:** Como Developer, deseo estandarizar las respuestas de error para facilitar el consumo del API por parte del frontend. |
| **BG-05** | Dr. Alejandro Torres — Médico especialista cardiovascular | Identificar responsables, horarios, secuencia de eventos y cumplimiento de indicaciones para tomar decisiones con información trazable. | Historial de eventos, detalle de responsable de registro, cumplimiento de indicaciones y resumen clínico. | **US-19:** Como médico especialista cardiovascular, deseo consultar el historial de eventos clínicos para reconstruir la evolución del paciente. <br><br> **US-20:** Como usuario clínico, deseo identificar quién registró una información clínica para asegurar trazabilidad y responsabilidad profesional. <br><br> **US-22:** Como médico especialista cardiovascular, deseo consultar un resumen clínico del paciente para comprender rápidamente su estado actual. |
| **BG-05** | Daniela Ríos — Personal de enfermería cardiovascular | Registrar información con responsable, fecha, hora y estado para fortalecer continuidad de atención. | Registro trazable de signos vitales, eventos y traspasos. | **US-16:** Como enfermera cardiovascular, deseo registrar signos vitales del paciente para mantener actualizado el monitoreo clínico. <br><br> **US-19:** Como enfermera cardiovascular, deseo registrar eventos clínicos relevantes para que el equipo pueda dar seguimiento oportuno al paciente. |
| **BG-05** | Developer | Garantizar que las acciones clínicas registradas mantengan evidencia técnica de auditoría, seguridad y trazabilidad. | Auditoría de acciones clínicas, autenticación, autorización y protección de recursos del API. | **TS-01:** Como Developer, deseo implementar autenticación para proteger el acceso a recursos clínicos del sistema. <br><br> **TS-05:** Como Developer, deseo registrar auditoría de acciones clínicas para conservar responsable, fecha y tipo de operación realizada. <br><br> **TS-06:** Como Developer, deseo estandarizar las respuestas de error para facilitar el consumo del API por parte del frontend. |
| **BG-05** | Dr. Alejandro Torres — Médico especialista cardiovascular | Identificar cambios críticos y validar información con enfermería para responder oportunamente ante deterioros clínicos. | Alertas o marcadores de cambios críticos y registro de validación clínica entre médico y enfermería. | **US-24:** Como médico especialista cardiovascular, deseo identificar cambios críticos del paciente para responder oportunamente ante deterioros clínicos. <br><br> **US-25:** Como médico especialista cardiovascular, deseo validar información relevante con enfermería para reducir incertidumbre antes de tomar una decisión clínica. |

#### Conclusión del Impact Mapping

El Impact Mapping permite evidenciar que las funcionalidades priorizadas de Nurse Pulse responden a objetivos de negocio concretos. La Landing Page se relaciona con la adquisición de visitantes interesados y la comunicación de la propuesta de valor. Los módulos clínicos de traspaso SBAR, signos vitales, eventos, resumen clínico e historial se relacionan con la mejora de comunicación, reducción del tiempo de búsqueda de información, disminución de dependencia de registros físicos y fortalecimiento de trazabilidad. Finalmente, las Technical Stories del RESTful API permiten sostener técnicamente los entregables necesarios para registro, consulta, seguridad, auditoría y continuidad clínica.
