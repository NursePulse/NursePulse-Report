<p align="center">
  <img src="assets/chapter-1/UPC_logo_transparente.png" alt="UPC" width="110">
</p>

<div align="center">

<p><strong>Universidad Peruana de Ciencias Aplicadas</strong></p>
<p><strong>Carrera de Ingeniería de Software</strong></p>
<p><strong><big>1ASI0732</big></strong></p>
<p><strong><big>Diseño de Experimentos de Ingeniería de Software</big></strong></p>

<p><strong>NRC</strong></p>
<p><strong><big>9095</big></strong></p>

<p><strong><big>Informe del Trabajo Final</big></strong></p>

<p><strong>Docente</strong></p>
<p><strong><big>Julio Manuel Noriega Melendez</big></strong></p>

<p><strong>Startup</strong></p>
<p><strong><big>Nurse Pulse</big></strong></p>

<p><strong>Producto</strong></p>
<p><strong><big>Nurse Pulse</big></strong></p>

<p><strong>Integrantes</strong></p>

| Código UPC   | Apellidos y nombres             |
|--------------|---------------------------------|
| u202414510   | Mansilla Rivero, Carlos Marcelo |
| u202313458 | Taipe Sangama, Jorge Francisco    |
| u202216163 | Paredes Davila, Jose Adrian       |
| [Código UPC] | [Apellidos y nombres]           |
| [Código UPC] | [Apellidos y nombres]           |

<p><strong>Periodo 202620</strong></p>
<p><strong>Septiembre de 2026</strong></p>

</div>

<div style="page-break-after: always;"></div>

# Part I: As-Is Software Project

## Capítulo I: Introducción

### 1.1. Startup Profile

#### 1.1.1. Descripción de la Startup

**Nurse Pulse** es una startup tecnológica conformada por estudiantes de la carrera de Ingeniería de Software de la Universidad Peruana de Ciencias Aplicadas. El equipo se enfoca en el desarrollo de soluciones digitales orientadas a mejorar procesos críticos dentro del sector salud, aplicando investigación con usuarios, diseño de experiencias digitales, desarrollo de aplicaciones y construcción de servicios de software.

La propuesta principal de la startup es **Nurse Pulse**, una solución digital orientada a mejorar la gestión de información clínica en entornos cardiovasculares. El producto busca apoyar a profesionales de la salud en actividades como el registro y consulta de signos vitales, documentación de eventos clínicos, comunicación durante cambios de turno y seguimiento de la evolución reciente del paciente.

Nurse Pulse surge a partir de una problemática relacionada con la dispersión de información clínica, la duplicidad de registros, la comunicación no estructurada entre profesionales y la dificultad para mantener trazabilidad sobre eventos, responsables, fechas y horarios. En escenarios cardiovasculares, donde el estado del paciente puede requerir seguimiento constante, disponer de información organizada y actualizada resulta especialmente relevante.

Frente a esta situación, Nurse Pulse propone centralizar información clínica relevante y estructurar determinados procesos utilizados por el personal de enfermería y los médicos especialistas. Entre las funcionalidades consideradas se encuentran el registro de signos vitales, los traspasos de turno mediante SBAR, el registro de eventos clínicos, la visualización de alertas, la consulta de la evolución del paciente y la trazabilidad de las acciones realizadas.

La solución no pretende reemplazar una Historia Clínica Electrónica (EHR), un Hospital Information System (HIS) completo ni el criterio profesional del personal de salud. Nurse Pulse se plantea como una herramienta digital complementaria enfocada en mejorar la comunicación, consulta y trazabilidad de información clínica dentro del contexto cardiovascular.

Como startup, Nurse Pulse busca desarrollar un producto digital accesible, seguro, escalable y centrado en las necesidades reales de sus usuarios. Para ello, el proyecto combina investigación del problema, experimentación, diseño centrado en el usuario, desarrollo de software, documentación técnica y validación de las funcionalidades propuestas.

**Misión:** Desarrollar soluciones digitales que ayuden a mejorar la comunicación, trazabilidad y organización de procesos clínicos cardiovasculares, aportando valor a los profesionales de salud y a las instituciones que buscan fortalecer la continuidad de atención de sus pacientes.

**Visión:** Ser una startup reconocida por crear soluciones tecnológicas confiables, accesibles y escalables para el sector salud, contribuyendo a una mejor gestión de información clínica y a la transformación digital de los procesos de atención.

---

#### 1.1.2. Perfiles de integrantes del equipo

<table>
  <tr>
    <th colspan="2">Mansilla Rivero, Carlos Marcelo</th>
  </tr>
  <tr>
    <td>
      <img src="assets/chapter-1/carlos.png" alt="Fotografía de Carlos Mansilla" width="300px">
    </td>
    <td>
      <b>Código:</b> u202414510<br>
      <b>Carrera:</b> Ingeniería de Software<br><br>
      Soy estudiante de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas. Cuento con conocimientos en programación, desarrollo web, servicios RESTful, bases de datos y arquitectura de software, utilizando tecnologías como C++, Python, JavaScript, Angular y .NET. Dentro de Nurse Pulse, aporto en el análisis de la solución, desarrollo técnico, documentación del proyecto y revisión de la coherencia entre los requerimientos, los experimentos y las funcionalidades propuestas. También contribuyo con responsabilidad, organización, pensamiento crítico y trabajo colaborativo.
    </td>
  </tr>

  <tr>
    <th colspan="2">Taipe Sangama, Jorge Francisco</th>
  </tr>
  <tr>
    <td>
      <img src="assets/chapter-1/Foto%20Jorge.png" alt="Fotografía de Jorge Taipe" width="300px">
    </td>
    <td>
      <b>Código:</b> u202313458<br>
      <b>Carrera:</b> Ingeniería de Software<br><br>
      Soy estudiante de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas. Cuento con conocimientos en desarrollo Front-end y Backend. Dentro de Nurse Pulse, aportaré como líder del equipo las habilidades adquiridas durante ciclos anteriores, incluyendo trabajo colaborativo, organización y puntualidad.
    </td>
  </tr>

  <tr>
    <th colspan="2">Paredes Davila, Jose Adrian</th>
  </tr>
  <tr>
    <td>
      <img src="assets/chapter-1/foto_jose.jpeg" alt="Fotografía de Jose Paredes" width="300px">
    </td>
    <td>
      <b>Código:</b> u202216163<br>
      <b>Carrera:</b> Ingeniería de Software<br><br>
      Soy estudiante de Ingeniería de Software en la Universidad Peruana de Ciencias Aplicadas. Cuento con conocimientos en desarrollo de software, gestión de bases de datos y metodologías ágiles. En el proyecto Nurse Pulse, aportaré en la implementación técnica, pruebas de calidad y elaboración de la documentación integral, contribuyendo con atención al detalle, proactividad y trabajo en equipo.
    </td>
  </tr>

  <tr>
    <th colspan="2">[Apellidos y nombres del integrante 4]</th>
  </tr>
  <tr>
    <td>
      <img src="assets/chapter-1/member-4.png" alt="Fotografía del integrante 4" width="300px">
    </td>
    <td>
      <b>Código:</b> [Código UPC]<br>
      <b>Carrera:</b> Ingeniería de Software<br><br>
      [Redactar una presentación que incluya los principales conocimientos técnicos, habilidades interpersonales y responsabilidades que el integrante aportará al desarrollo de Nurse Pulse.]
    </td>
  </tr>

  <tr>
    <th colspan="2">[Apellidos y nombres del integrante 5]</th>
  </tr>
  <tr>
    <td>
      <img src="assets/chapter-1/member-5.png" alt="Fotografía del integrante 5" width="300px">
    </td>
    <td>
      <b>Código:</b> [Código UPC]<br>
      <b>Carrera:</b> Ingeniería de Software<br><br>
      [Redactar una presentación que incluya los principales conocimientos técnicos, habilidades interpersonales y responsabilidades que el integrante aportará al desarrollo de Nurse Pulse.]
    </td>
  </tr>
</table>

---

### 1.2. Solution Profile

#### 1.2.1. Antecedentes y problemática

Nurse Pulse toma como antecedente conceptual **PulseReport**, una solución académica desarrollada previamente por el equipo BrainSpark para apoyar la gestión de información clínica en entornos cardiovasculares. El proyecto anterior abordó procesos como el registro de signos vitales, los traspasos de turno mediante SBAR, el registro de eventos clínicos y la trazabilidad de las acciones realizadas por profesionales de la salud.

A partir de dicho antecedente, Nurse Pulse mantiene el enfoque en el contexto cardiovascular y utiliza los conocimientos obtenidos durante el desarrollo previo como punto de partida para una nueva etapa de investigación y experimentación. Las hipótesis, decisiones de diseño y resultados del proyecto actual deberán ser nuevamente evaluados dentro del contexto de este curso.

La problemática identificada se relaciona con la forma en que información clínica relevante puede encontrarse distribuida entre registros físicos, sistemas hospitalarios, hojas de cálculo, reportes escritos y comunicación verbal entre profesionales de la salud.

En áreas cardiovasculares, el personal de enfermería y los médicos especialistas requieren consultar, registrar y comunicar información con rapidez. Datos como signos vitales, eventos clínicos, tratamientos, evolución reciente del paciente y traspasos de turno deben encontrarse disponibles de manera clara y trazable. Cuando la información está fragmentada o no se comunica de manera estructurada, pueden producirse omisiones, duplicidad de registros, retrasos en la consulta y dificultades para reconstruir lo ocurrido durante la atención.

Nurse Pulse plantea una solución digital complementaria que permita centralizar información relevante del paciente cardiovascular y facilitar determinados procesos de comunicación y seguimiento clínico.

##### A. Quiénes están involucrados (Who)

Los principales involucrados son los profesionales de salud y las instituciones relacionadas con la atención de pacientes cardiovasculares.

El **personal de enfermería cardiovascular** participa directamente en el monitoreo del paciente, registro de signos vitales, administración y seguimiento de tratamientos indicados, documentación de eventos clínicos y comunicación de información durante los cambios de turno. Estas actividades requieren rapidez, precisión y continuidad.

Los **médicos especialistas cardiovasculares**, como cardiólogos, intensivistas, cirujanos cardiovasculares y otros profesionales relacionados, necesitan consultar información clínica para evaluar la evolución del paciente, analizar eventos relevantes y tomar decisiones clínicas. Para ellos, la información debe estar disponible de manera organizada, resumida, confiable y actualizada.

También participan las **instituciones de salud**, incluyendo hospitales, clínicas privadas y centros especializados en cardiología, debido a que requieren organizar sus procesos, mantener trazabilidad de la información y garantizar continuidad entre los distintos profesionales que participan en la atención.

Finalmente, los **pacientes cardiovasculares** representan beneficiarios indirectos de la solución, dado que una gestión más organizada de la información puede contribuir a mejorar la continuidad y coordinación de su atención.

##### B. Qué problema resuelve la solución (What)

El problema principal que Nurse Pulse busca abordar es la **gestión dispersa, poco estructurada y con trazabilidad limitada de información clínica en entornos cardiovasculares**.

La información relevante para la atención puede encontrarse distribuida entre diferentes medios o depender de comunicación verbal entre profesionales. Esta situación puede generar dificultades como:

- Pérdida parcial de información durante cambios de turno.
- Duplicidad entre registros físicos y digitales.
- Retrasos al consultar información clínica relevante.
- Posibles omisiones de información durante eventos importantes.
- Dificultad para identificar quién registró una acción y cuándo ocurrió.
- Mayor carga operativa para el personal de salud.
- Dificultad para reconstruir la evolución reciente del paciente.
- Falta de una vista consolidada para la consulta de información relevante.

Nurse Pulse propone centralizar determinados registros clínicos y relacionarlos con el paciente, el profesional responsable, la fecha y la hora correspondiente. Además, plantea estructurar procesos como el traspaso de turno mediante SBAR y facilitar la visualización de signos vitales, eventos y evolución clínica.

##### C. Cuándo ocurre el problema (When)

La problemática puede presentarse durante diferentes momentos de la jornada clínica, especialmente cuando la información debe ser registrada, consultada o comunicada con rapidez.

Entre estos momentos se encuentran:

- Cambios de turno entre equipos de enfermería.
- Registro periódico de signos vitales.
- Aparición y documentación de eventos clínicos.
- Consulta de la evolución reciente del paciente.
- Seguimiento de tratamientos o indicaciones registradas.
- Situaciones en las que se requiere identificar información relevante rápidamente.
- Revisión posterior de eventos para seguimiento o auditoría.

En estos escenarios, la disponibilidad de información estructurada y trazable puede facilitar la continuidad entre los profesionales involucrados en la atención.

##### D. Dónde ocurre el problema (Where)

La problemática se presenta principalmente en instituciones de salud que atienden pacientes cardiovasculares, tales como:

- Hospitales.
- Clínicas privadas.
- Centros especializados en cardiología.
- Unidades de cuidados intensivos.
- Áreas de hospitalización cardiovascular.
- Servicios de emergencia.
- Otras unidades donde se realiza seguimiento de pacientes con condiciones cardiovasculares.

En estos espacios pueden participar diferentes profesionales en la atención de un mismo paciente, por lo que resulta necesario mantener información clínica organizada, accesible y correctamente registrada.

##### E. Por qué es relevante este problema (Why)

El problema resulta relevante porque la información clínica constituye un elemento importante para mantener la continuidad de atención y apoyar la toma de decisiones de los profesionales de salud.

Cuando los datos se encuentran incompletos, duplicados, dispersos o son difíciles de localizar, los usuarios pueden requerir más tiempo para buscar, validar o reconstruir la información disponible.

Esta situación puede relacionarse con:

- Menor eficiencia operativa durante el turno.
- Riesgo de omisiones de información.
- Dificultad para realizar seguimiento de eventos relevantes.
- Comunicación poco estructurada entre profesionales.
- Mayor carga administrativa para el personal de enfermería.
- Mayor tiempo de consulta para los médicos.
- Menor capacidad de auditoría y trazabilidad sobre las acciones realizadas.

Por ello, Nurse Pulse busca evaluar si una herramienta especializada puede reducir parte de esta fricción mediante una experiencia digital enfocada en los principales flujos de información cardiovascular.

##### F. Cómo se gestiona actualmente el problema (How)

La gestión de información clínica puede realizarse mediante una combinación de sistemas hospitalarios, historias clínicas electrónicas, registros físicos, hojas de cálculo, reportes y comunicación verbal.

La forma específica de trabajar depende de cada institución y deberá ser estudiada mediante la investigación con los usuarios objetivo. Nurse Pulse no parte de la premisa de que todos los establecimientos utilizan procesos deficientes ni los mismos sistemas.

Sin embargo, cuando la información necesaria para una actividad se encuentra distribuida entre diferentes fuentes, el profesional puede necesitar consultar varios medios antes de completar una tarea. Del mismo modo, los cambios de turno pueden depender de diferentes métodos de comunicación cuya estructura varía según la organización.

Nurse Pulse plantea evaluar un flujo digital centralizado para determinados procesos cardiovasculares, permitiendo que los profesionales autorizados registren y consulten información desde una misma plataforma.

##### G. Cuánto impacta el problema (How much)

En esta etapa del proyecto no se cuenta todavía con evidencia propia suficiente para determinar exactamente cuánto tiempo pierden los profesionales debido a la fragmentación de información, con qué frecuencia se producen omisiones o qué porcentaje de instituciones presenta esta problemática.

Por esta razón, el proyecto utilizará la investigación y los experimentos para establecer una línea base y medir indicadores como:

- Tiempo necesario para encontrar información clínica determinada.
- Cantidad de fuentes consultadas para completar una tarea.
- Tiempo requerido para registrar signos vitales.
- Porcentaje de elementos relevantes incluidos en un traspaso de turno.
- Tasa de tareas completadas correctamente.
- Tiempo necesario para identificar un evento, responsable, fecha u hora.
- Percepción de claridad, utilidad y facilidad de uso.

Estos resultados permitirán determinar si las funcionalidades propuestas producen mejoras medibles frente a las alternativas evaluadas durante los experimentos.

##### Puntos principales que debe resolver la solución

Nurse Pulse busca abordar los siguientes puntos:

- Centralizar información clínica relevante del paciente cardiovascular.
- Facilitar el registro y consulta de signos vitales.
- Estructurar la comunicación durante cambios de turno mediante SBAR.
- Registrar eventos clínicos relevantes.
- Presentar alertas e información que requiera atención.
- Permitir la consulta de la evolución reciente del paciente.
- Mantener trazabilidad sobre responsables, fechas, horas y acciones realizadas.
- Facilitar el acceso a información para personal de enfermería y médicos autorizados.
- Reducir la dependencia de registros complementarios cuando el flujo digital resulte adecuado.
- Mantener una experiencia clara y comprensible en los productos digitales desarrollados.

##### Objetivos de la solución

**Objetivo general**

Desarrollar una solución digital que apoye la gestión de información clínica cardiovascular, facilitando la comunicación entre profesionales de salud, la trazabilidad de eventos y la continuidad de atención del paciente.

**Objetivos específicos**

- Diseñar una Landing Page que comunique claramente la propuesta de valor de Nurse Pulse.
- Implementar una Web Application que permita registrar y consultar información clínica relevante.
- Desarrollar una Native Mobile Application que permita acceder a los principales flujos definidos para el contexto móvil.
- Desarrollar un RESTful API que brinde soporte a los recursos principales del sistema.
- Integrar las aplicaciones cliente con los servicios desarrollados.
- Incorporar flujos para el registro de signos vitales, eventos clínicos, traspasos SBAR y consulta de evolución.
- Mantener trazabilidad sobre las acciones realizadas por los usuarios autorizados.
- Validar las principales funcionalidades mediante experimentos con usuarios representativos de los segmentos objetivo.
- Utilizar los resultados obtenidos para mantener, modificar o descartar las hipótesis planteadas.

##### Restricciones y alcance del proyecto

- Nurse Pulse será una herramienta de soporte y no realizará diagnósticos médicos.
- La solución no reemplazará una Historia Clínica Electrónica ni un Hospital Information System completo.
- Las decisiones médicas continuarán siendo responsabilidad exclusiva de profesionales autorizados.
- Los experimentos académicos utilizarán escenarios controlados y datos sintéticos, evitando el uso de historias clínicas reales.
- El alcance funcional inicial se concentrará en procesos relacionados con información clínica cardiovascular.
- La solución deberá aplicar roles y permisos para controlar el acceso a información y funcionalidades.
- El proyecto incluirá Landing Page, Frontend Web Application, Native Mobile Application y RESTful API conforme a los requerimientos del curso.
- Las funcionalidades propuestas deberán ser validadas mediante experimentos antes de asumir que generan los resultados esperados.

---

#### 1.2.2. Lean UX Process

El Lean UX Process de Nurse Pulse se plantea como un ciclo de aprendizaje continuo orientado a resultados y no únicamente a la construcción de funcionalidades.

Este proceso permite transformar la problemática identificada en supuestos e hipótesis que puedan ser evaluados mediante entrevistas, pruebas de usabilidad, tareas controladas y otros experimentos.

Siguiendo el enfoque de Lean UX, la lógica utilizada será:

**problema → outcomes → supuestos → hipótesis → experimentos → aprendizaje → iteración**

Para Nurse Pulse se consideran dos segmentos principales de usuarios directos:

1. **Personal de enfermería cardiovascular.**
2. **Médicos especialistas cardiovasculares.**

Además, se reconoce como cliente institucional a los **hospitales, clínicas y centros especializados en cardiología**, debido a que estas organizaciones son quienes podrían adoptar e implementar la solución dentro de sus procesos.

##### Business Outcomes y User Outcomes

**Business Outcomes**

- Reducir el tiempo necesario para registrar y consultar información clínica relevante.
- Disminuir la duplicidad de registros entre diferentes medios.
- Mejorar la trazabilidad de eventos, responsables, fechas y horas.
- Identificar cuáles funcionalidades generan mayor valor para los profesionales cardiovasculares.
- Incrementar el interés de instituciones de salud en conocer o evaluar Nurse Pulse.
- Obtener evidencia que permita priorizar el roadmap del producto.
- Reducir el riesgo de invertir recursos en funcionalidades que no produzcan resultados relevantes para los usuarios.

**User Outcomes**

- El personal de enfermería cardiovascular registra información clínica mediante flujos claros y comprensibles.
- Los enfermeros comunican los cambios de turno de forma estructurada mediante SBAR.
- Los médicos especialistas encuentran con mayor rapidez información sobre la evolución reciente del paciente.
- Los profesionales pueden consultar signos vitales y eventos clínicos desde una vista organizada.
- Los usuarios identifican con facilidad responsables, fechas y horas de los registros.
- Los profesionales reconocen rápidamente eventos o información que requiere atención.
- Los usuarios realizan sus tareas sin incrementar innecesariamente su carga operativa.

---

##### 1.2.2.1. Lean UX Problem Statements

###### Problem Statement 1 - Personal de enfermería cardiovascular

**Domain:** Gestión de información clínica cardiovascular durante los turnos de atención.

**Customer segment:** Personal de enfermería que trabaja con pacientes cardiovasculares y participa en el registro de signos vitales, eventos clínicos y traspasos de turno.

**Pain points:** Posible duplicidad de registros, utilización de múltiples fuentes de información, comunicación no estructurada durante cambios de turno y dificultad para mantener trazabilidad de determinadas acciones.

**Gap:** Los sistemas utilizados en una institución pueden cubrir numerosos procesos hospitalarios, pero determinados flujos de registro, consulta y comunicación pueden requerir varios pasos o encontrarse distribuidos entre diferentes medios.

**Vision / Strategy:** Nurse Pulse busca proporcionar una experiencia digital enfocada en determinados procesos cardiovasculares, incluyendo signos vitales, eventos clínicos, comunicación mediante SBAR y trazabilidad.

**Initial segment:** Enfermeros y enfermeras que atienden pacientes cardiovasculares en hospitalización, unidades críticas, emergencia o áreas especializadas.

**Problem Statement:**

El personal de enfermería que trabaja con pacientes cardiovasculares necesita una manera rápida, estructurada y trazable de registrar y comunicar información clínica relevante porque los datos utilizados durante el turno pueden encontrarse distribuidos entre diferentes medios o presentarse mediante flujos que dificultan su consulta y transferencia.

**Pregunta clave:**

¿Cómo podríamos ayudar al personal de enfermería cardiovascular a registrar y comunicar información clínica de manera rápida, clara y trazable durante su turno?

---

###### Problem Statement 2 - Médicos especialistas cardiovasculares

**Domain:** Consulta, seguimiento y toma de decisiones relacionadas con pacientes cardiovasculares.

**Customer segment:** Médicos cardiólogos, intensivistas, cirujanos cardiovasculares y otros especialistas que requieren consultar información clínica durante el seguimiento de pacientes.

**Pain points:** Necesidad de revisar información proveniente de diferentes registros, dificultad para visualizar rápidamente la evolución reciente y necesidad de validar cuándo y quién realizó determinados registros.

**Gap:** La información relevante para una consulta puede no encontrarse presentada en una única vista resumida que facilite identificar la evolución reciente, signos vitales y eventos registrados.

**Vision / Strategy:** Nurse Pulse busca proporcionar una vista clínica organizada que permita consultar información relevante del paciente y mantener trazabilidad sobre los registros realizados.

**Initial segment:** Médicos especialistas que atienden pacientes cardiovasculares en hospitalización, unidades críticas, emergencia o centros especializados.

**Problem Statement:**

Los médicos especialistas cardiovasculares necesitan acceder a información clínica consolidada, comprensible y trazable porque consultar datos distribuidos entre diferentes fuentes puede aumentar el tiempo requerido para comprender la evolución reciente de un paciente.

**Pregunta clave:**

¿Cómo podríamos ayudar a los médicos especialistas cardiovasculares a consultar información relevante del paciente de forma rápida, resumida y confiable?

---

###### Problem Statement 3 - Instituciones de salud

**Domain:** Gestión y supervisión de procesos relacionados con información clínica cardiovascular.

**Customer segment:** Hospitales, clínicas y centros especializados en cardiología que atienden pacientes cardiovasculares.

**Pain points:** Necesidad de mantener continuidad entre profesionales, supervisar determinados registros y garantizar trazabilidad sobre las actividades realizadas.

**Gap:** Los sistemas hospitalarios pueden abarcar numerosos procesos institucionales, mientras que ciertos flujos especializados de comunicación y seguimiento cardiovascular pueden encontrarse distribuidos entre diferentes herramientas o procedimientos.

**Vision / Strategy:** Nurse Pulse busca funcionar como una solución complementaria enfocada en comunicación, seguimiento y trazabilidad de información relacionada con pacientes cardiovasculares.

**Initial segment:** Instituciones de salud con servicios de atención cardiovascular interesadas en evaluar herramientas digitales complementarias para determinados procesos clínicos.

**Problem Statement:**

Las instituciones de salud que atienden pacientes cardiovasculares necesitan mantener información organizada y trazable entre los profesionales involucrados porque la fragmentación de determinados procesos puede dificultar la supervisión, seguimiento y continuidad de atención.

**Pregunta clave:**

¿Cómo podríamos ofrecer una solución digital complementaria que mejore la comunicación, trazabilidad y consulta de información clínica en entornos cardiovasculares?

---

##### 1.2.2.2. Lean UX Assumptions

###### Supuestos sobre los usuarios

- El personal de enfermería cardiovascular registra información clínica varias veces durante un turno.
- Los cambios de turno requieren transferir información relevante sobre el estado y evolución del paciente.
- Los médicos especialistas necesitan consultar información reciente antes de evaluar determinados casos.
- Los profesionales clínicos valoran interfaces claras y con pocos pasos.
- Los usuarios necesitan conocer quién realizó determinados registros y cuándo ocurrieron.
- Los profesionales estarán dispuestos a utilizar una nueva herramienta si esta aporta valor sin incrementar innecesariamente su carga operativa.
- Los dispositivos utilizados dependerán de las políticas y recursos disponibles en cada institución.

###### Supuestos sobre las necesidades

- La fragmentación de información puede aumentar el tiempo requerido para completar determinadas tareas.
- La comunicación no estructurada durante un cambio de turno puede provocar omisiones.
- El registro digital de signos vitales puede reducir la dependencia de registros complementarios.
- Una vista resumida de la evolución puede facilitar la consulta de información.
- Los eventos clínicos relevantes necesitan quedar registrados de manera clara y trazable.
- La identificación de responsables, fechas y horas genera mayor confianza en los registros.
- La presentación visual de alertas puede ayudar a reconocer información que requiere atención.

###### Supuestos sobre la solución

- Un formulario digital basado en SBAR puede ayudar a estructurar los traspasos de turno.
- Un módulo de signos vitales puede facilitar el registro y consulta de mediciones.
- Una vista de evolución clínica puede reducir el tiempo requerido para encontrar información relevante.
- Un dashboard puede ayudar a visualizar información reciente del paciente.
- Un registro de auditoría puede mejorar la trazabilidad de determinadas acciones.
- Una aplicación móvil puede resultar útil para ciertas actividades realizadas cerca del paciente.
- Una Landing Page clara puede permitir que potenciales usuarios y clientes comprendan la propuesta de valor de Nurse Pulse.

###### Supuestos sobre el negocio

- Hospitales, clínicas y centros especializados pueden reconocer valor en una solución complementaria enfocada en información clínica cardiovascular.
- Las instituciones pueden considerar una solución SaaS si ofrece una implementación comprensible y un costo razonable.
- La adopción dependerá de que Nurse Pulse sea percibido como útil, seguro y compatible con el flujo de trabajo.
- La facilidad de uso, trazabilidad, seguridad y soporte influirán en la decisión institucional.
- La validación con usuarios representativos permitirá identificar las funcionalidades de mayor valor antes de ampliar el producto.

###### Lean UX Assumption Prioritization

Las suposiciones se priorizan considerando principalmente su nivel de riesgo e incertidumbre. Se evaluarán primero aquellos supuestos que, en caso de resultar incorrectos, puedan afectar significativamente la propuesta de valor de Nurse Pulse.

| ID | Supuesto | Riesgo | Incertidumbre | Prioridad |
| -- | -------- | ------ | ------------- | --------- |
| A-01 | Un traspaso mediante SBAR reduce omisiones frente a una comunicación no estructurada. | Alto | Alto | Alta |
| A-02 | El registro digital de signos vitales reduce la dependencia de medios complementarios. | Alto | Alto | Alta |
| A-03 | Una vista resumida permite al médico encontrar información reciente con mayor rapidez. | Alto | Alto | Alta |
| A-04 | La trazabilidad mediante responsable, fecha y hora aporta valor a los usuarios clínicos. | Medio | Medio | Media |
| A-05 | Las instituciones de salud reconocen valor en una solución complementaria especializada. | Alto | Alto | Alta |
| A-06 | Una aplicación móvil facilita determinados registros realizados cerca del paciente. | Medio | Alto | Media |
| A-07 | Una Landing Page clara comunica adecuadamente la propuesta de valor del producto. | Medio | Medio | Media |

---

##### 1.2.2.3. Lean UX Hypothesis Statements

Las hipótesis de Nurse Pulse se redactan como afirmaciones comprobables que relacionan una funcionalidad o experiencia propuesta con un segmento de usuarios, un resultado esperado y una evidencia que permita evaluar el supuesto.

Los valores cuantitativos utilizados inicialmente representan objetivos provisionales y podrán ajustarse cuando se obtenga una línea base mediante investigación preliminar.

###### Hipótesis 1 - Traspaso de turno mediante SBAR

Creemos que proporcionar un **formulario digital estructurado mediante SBAR** al **personal de enfermería cardiovascular** permitirá comunicar información más completa durante los cambios de turno frente a un método no estructurado.

Sabremos que la hipótesis obtiene evidencia favorable si, durante un experimento controlado, los participantes que utilizan SBAR presentan una menor tasa de omisión de los elementos definidos como relevantes frente a la condición de comparación.

---

###### Hipótesis 2 - Registro de signos vitales

Creemos que proporcionar un **módulo digital de registro de signos vitales** al **personal de enfermería cardiovascular** facilitará el registro de las mediciones relevantes del paciente.

Sabremos que la hipótesis obtiene evidencia favorable si los participantes completan correctamente la tarea de registro con una alta tasa de finalización, sin omitir campos definidos como esenciales y sin aumentar los errores frente a la alternativa evaluada.

---

###### Hipótesis 3 - Consulta de evolución clínica

Creemos que proporcionar una **vista resumida de evolución clínica** a los **médicos especialistas cardiovasculares** permitirá localizar con mayor rapidez información relevante sobre el estado reciente de un paciente.

Sabremos que la hipótesis obtiene evidencia favorable si el tiempo medio necesario para encontrar la información solicitada es menor que en una vista donde los datos se encuentran distribuidos en diferentes secciones y no aumenta la tasa de respuestas incorrectas.

---

###### Hipótesis 4 - Trazabilidad clínica

Creemos que mostrar **responsable, fecha y hora** en los registros permitirá a los **profesionales clínicos** identificar con mayor facilidad el origen de una acción realizada durante la atención.

Sabremos que la hipótesis obtiene evidencia favorable si los participantes pueden responder correctamente preguntas relacionadas con quién realizó una acción, cuándo ocurrió y qué registro estuvo involucrado.

---

###### Hipótesis 5 - Alertas y eventos relevantes

Creemos que presentar **eventos y alertas clínicas mediante una jerarquía visual clara** permitirá a los **usuarios clínicos** reconocer con mayor rapidez información que requiere atención.

Sabremos que la hipótesis obtiene evidencia favorable si los participantes identifican correctamente el evento de mayor prioridad en menor tiempo que utilizando una visualización sin priorización.

---

###### Hipótesis 6 - Aplicación móvil

Creemos que proporcionar una **Native Mobile Application** al **personal de enfermería cardiovascular** facilitará determinadas tareas de registro y consulta realizadas cerca del paciente.

Sabremos que la hipótesis obtiene evidencia favorable si los participantes completan las tareas definidas con una tasa de finalización igual o superior a la alternativa de escritorio y reducen el tiempo requerido sin aumentar los errores.

---

###### Hipótesis 7 - Landing Page

Creemos que crear una **Landing Page con una propuesta de valor clara, funcionalidades principales y llamados a la acción** permitirá que los **visitantes y representantes de instituciones de salud** comprendan qué problema resuelve Nurse Pulse.

Sabremos que la hipótesis obtiene evidencia favorable si los participantes pueden explicar correctamente la finalidad del producto después de explorar la página e identificar sin asistencia la acción necesaria para solicitar información o conocer la solución.

---

###### Hipótesis 8 - Adopción institucional

Creemos que presentar Nurse Pulse como una **herramienta digital complementaria enfocada en comunicación, trazabilidad y seguimiento cardiovascular** permitirá que los **representantes de instituciones de salud** comprendan su función sin interpretarla como un reemplazo de su sistema hospitalario completo.

Sabremos que la hipótesis obtiene evidencia favorable si los participantes institucionales pueden diferenciar correctamente el alcance de Nurse Pulse frente a un HIS o EHR y muestran interés en evaluar su utilización dentro de un escenario definido.

---

###### Lean UX Experiments and Learning

Cada hipótesis será evaluada mediante experimentos orientados a obtener evidencia suficiente para tomar decisiones sobre el producto.

| Hipótesis | Experimento inicial | Evidencia principal | Aprendizaje esperado |
| --------- | ------------------- | ------------------- | -------------------- |
| H-01 - SBAR | Comparación entre formulario SBAR y registro no estructurado. | Omisiones, tiempo y errores. | Determinar si SBAR mejora la completitud de la información comunicada. |
| H-02 - Signos vitales | Prueba de registro con escenarios simulados. | Finalización, omisiones, tiempo y errores. | Determinar si el flujo de registro resulta comprensible y eficiente. |
| H-03 - Evolución clínica | Comparación de búsqueda de información entre dos interfaces. | Tiempo y respuestas correctas. | Determinar si una vista resumida facilita la consulta médica. |
| H-04 - Trazabilidad | Escenario simulado de revisión de registros. | Respuestas correctas sobre responsable, fecha y hora. | Evaluar si la trazabilidad permite reconstruir acciones con facilidad. |
| H-05 - Alertas | Prueba de reconocimiento y priorización visual. | Primera alerta identificada y tiempo. | Determinar si la jerarquía visual facilita reconocer eventos relevantes. |
| H-06 - Mobile | Comparación de tareas entre móvil y estación de trabajo. | Tiempo, errores y tasa de finalización. | Evaluar si el dispositivo móvil aporta valor en el escenario estudiado. |
| H-07 - Landing Page | Test de comprensión de propuesta de valor. | Comprensión y localización del CTA. | Determinar si los visitantes comprenden la finalidad del producto. |
| H-08 - Adopción institucional | Entrevista y escenario de evaluación institucional. | Comprensión, interés y objeciones. | Identificar condiciones y barreras para una posible adopción. |

Los experimentos se realizarán en ciclos de aprendizaje. Si una hipótesis obtiene evidencia favorable, podrá mantenerse y continuar su evaluación. Si los resultados contradicen el supuesto, la funcionalidad o planteamiento deberá modificarse, descartarse o someterse a un nuevo experimento.

---

##### 1.2.2.4. Lean UX Canvas

El Lean UX Canvas sintetiza los principales elementos del modelo de aprendizaje de Nurse Pulse y relaciona el problema de negocio con los usuarios, resultados, supuestos, soluciones e hipótesis que serán evaluadas.

| Sección | Descripción para Nurse Pulse |
| ------- | ---------------------------- |
| **1. Business Problem** | En entornos cardiovasculares, determinada información clínica puede encontrarse distribuida entre diferentes sistemas, registros físicos y procesos de comunicación. Esta fragmentación puede dificultar la consulta, comunicación y trazabilidad de información relevante. Nurse Pulse busca evaluar una solución digital complementaria enfocada en centralizar determinados flujos clínicos cardiovasculares. |
| **2. Business Outcomes** | Reducir fricción en procesos de registro y consulta, mejorar trazabilidad, identificar funcionalidades de mayor valor y generar interés institucional en la solución. |
| **3. Users and Customers** | **Usuarios directos:** personal de enfermería cardiovascular y médicos especialistas cardiovasculares. **Cliente institucional:** hospitales, clínicas y centros especializados en cardiología. |
| **4. User Outcomes** | Registrar signos vitales, comunicar traspasos SBAR, consultar evolución clínica, identificar eventos relevantes y conocer la trazabilidad de las acciones realizadas. |
| **5. User Benefits** | Menor esfuerzo para encontrar información, mayor claridad durante cambios de turno, mejor organización de registros y mayor visibilidad sobre responsables, fechas y eventos. |
| **6. Solutions** | Landing Page, Web Application, Native Mobile Application, registro de signos vitales, traspasos SBAR, eventos clínicos, alertas, vista de evolución, dashboard y registros de trazabilidad. |
| **7. Hypotheses** | SBAR puede reducir omisiones; el registro digital puede facilitar el flujo de signos vitales; una vista resumida puede reducir tiempos de consulta; la trazabilidad puede facilitar la revisión de registros; y la priorización visual puede facilitar el reconocimiento de eventos. |
| **8. Assumptions** | Los profesionales valoran rapidez, simplicidad y trazabilidad; determinadas tareas se ven afectadas por la fragmentación de información; y las instituciones pueden reconocer valor en una solución complementaria especializada. |
| **9. Experiments** | Entrevistas, pruebas comparativas, tareas de usabilidad, experimentos SBAR, evaluación de navegación, pruebas móviles y validación de Landing Page. |
| **10. Learning** | Los resultados determinarán qué funcionalidades deben mantenerse, modificarse, descartarse o someterse a nuevos experimentos antes de ampliar el producto. |

> **Artefacto:** Lean UX Canvas

<p align="center">
  <img src="assets/chapter-1/LEAN-UX-CANVAS.png" alt="Lean UX Canvas de Nurse Pulse" width="700px">
</p>

---

### 1.3. Segmentos objetivo

Nurse Pulse diferencia entre los **usuarios directos** que interactúan con la plataforma dentro de las actividades relacionadas con la atención cardiovascular y el **cliente institucional** responsable de evaluar o adoptar la solución.

Los dos segmentos principales de usuarios definidos para la investigación son el **personal de enfermería cardiovascular** y los **médicos especialistas cardiovasculares**. Como cliente institucional se consideran hospitales, clínicas y centros especializados en cardiología.

---

#### Segmento objetivo #1: Personal de enfermería cardiovascular

Este segmento está conformado por enfermeros y enfermeras que atienden pacientes cardiovasculares en áreas como hospitalización, unidades de cuidados intensivos, emergencia y centros especializados en cardiología.

Sus actividades pueden incluir monitoreo del paciente, registro de signos vitales, seguimiento de tratamientos indicados, documentación de eventos clínicos y transferencia de información durante los cambios de turno.

**Características demográficas y profesionales preliminares:**

- Profesionales de salud con formación técnica o universitaria en enfermería.
- Edad aproximada entre 24 y 55 años, rango que deberá validarse mediante la investigación.
- Experiencia variable, desde profesionales en etapas iniciales hasta personal con amplia experiencia clínica.
- Participación frecuente en turnos rotativos y guardias.
- Trabajo en áreas donde la información del paciente puede cambiar constantemente.
- Uso de herramientas digitales y sistemas institucionales según los recursos disponibles en el establecimiento.

**Características clave del segmento:**

- Registra información clínica con alta frecuencia.
- Necesita consultar información durante diferentes momentos del turno.
- Participa en la transferencia de información entre equipos.
- Trabaja en escenarios donde rapidez y precisión son relevantes.
- Requiere identificar signos vitales y eventos recientes.
- Necesita mantener trazabilidad sobre determinadas acciones realizadas.
- Valora interfaces claras que no añadan pasos innecesarios.

**Necesidades principales:**

- Registrar información clínica de manera rápida y comprensible.
- Consultar signos vitales y eventos recientes.
- Comunicar información estructurada durante el cambio de turno.
- Reducir omisiones durante la transferencia de información.
- Evitar duplicidad innecesaria entre diferentes medios.
- Identificar información que requiere seguimiento.
- Mantener evidencia de las acciones realizadas durante el turno.

---

#### Segmento objetivo #2: Médicos especialistas cardiovasculares

Este segmento está compuesto por médicos cardiólogos, intensivistas, cirujanos cardiovasculares y otros profesionales médicos relacionados con la evaluación y seguimiento de pacientes cardiovasculares.

Su interacción con Nurse Pulse se orienta principalmente a la consulta de información clínica, revisión de signos vitales, análisis de eventos recientes y seguimiento de la evolución del paciente.

**Características demográficas y profesionales preliminares:**

- Profesionales médicos con especialización o experiencia en cardiología, medicina intensiva, cirugía cardiovascular u otras áreas relacionadas.
- Edad aproximada entre 28 y 60 años, rango que deberá validarse mediante la investigación.
- Formación especializada y experiencia clínica variable.
- Trabajo en hospitales, clínicas, centros cardiovasculares, UCI, emergencia o áreas de hospitalización.
- Interacción frecuente con personal de enfermería y otros profesionales.
- Uso de historias clínicas, sistemas hospitalarios y diferentes fuentes de información para evaluar pacientes.

**Características clave del segmento:**

- Consulta información clínica para evaluar la evolución del paciente.
- Necesita revisar signos vitales y eventos relevantes.
- Busca información resumida y fácil de interpretar.
- Requiere conocer información actualizada antes de determinadas decisiones.
- Coordina actividades con personal de enfermería y otros profesionales.
- Valora la trazabilidad para verificar cuándo y quién realizó determinados registros.
- Rechaza herramientas que incrementen innecesariamente la complejidad de su trabajo.

**Necesidades principales:**

- Consultar rápidamente información relevante del paciente.
- Visualizar la evolución reciente.
- Revisar signos vitales registrados.
- Identificar eventos clínicos relevantes.
- Reconocer responsables, fechas y horas de determinados registros.
- Reducir el tiempo requerido para localizar información.
- Contar con una vista organizada y comprensible del estado reciente del paciente.

---

#### Cliente objetivo: Hospitales, clínicas y centros especializados en cardiología

Además de los usuarios directos, Nurse Pulse considera como cliente objetivo a las instituciones de salud que atienden pacientes cardiovasculares.

Estas organizaciones pueden disponer de distintos niveles de digitalización y contar con diferentes sistemas para administrar su información clínica. Nurse Pulse no pretende sustituir esa infraestructura, sino evaluar su valor como herramienta complementaria para determinados procesos de comunicación, consulta y trazabilidad.

**Características del cliente institucional:**

- Instituciones públicas o privadas del sector salud.
- Hospitales y clínicas con atención cardiovascular.
- Centros especializados en cardiología.
- Instituciones con áreas de hospitalización, emergencia o cuidados intensivos.
- Organizaciones que pueden disponer previamente de sistemas hospitalarios.
- Entidades interesadas en mejorar trazabilidad y continuidad de determinados procesos clínicos.

**Necesidades principales:**

- Facilitar la comunicación entre profesionales.
- Reducir la pérdida u omisión de información relevante.
- Mantener trazabilidad de registros y eventos.
- Facilitar la supervisión y revisión de determinadas acciones.
- Implementar soluciones digitales sin reemplazar inmediatamente toda su infraestructura existente.
- Evaluar herramientas que aporten valor sin incrementar excesivamente la complejidad operativa.

---

#### Sustento estadístico de los segmentos

Las enfermedades cardiovasculares representan un problema relevante de salud pública. La Organización Mundial de la Salud señala que constituyen la principal causa de muerte a nivel mundial, lo que evidencia la magnitud de este conjunto de enfermedades y la importancia de los procesos relacionados con su prevención, monitoreo y atención (Organización Mundial de la Salud [OMS], s. f.).

En el contexto de las Américas, la Organización Panamericana de la Salud también identifica a las enfermedades cardiovasculares como una de las principales causas de mortalidad de la región. Este panorama evidencia que los servicios relacionados con atención cardiovascular involucran una demanda permanente de profesionales capaces de monitorear, registrar y evaluar información clínica de estos pacientes (Organización Panamericana de la Salud [OPS], s. f.).

En el Perú, las enfermedades cardiovasculares forman parte de los principales problemas de salud pública. Asimismo, la Encuesta Demográfica y de Salud Familiar correspondiente a 2024 reportó que aproximadamente el **14.2 % de las personas de 15 años a más presentó presión arterial alta**, indicador relacionado con uno de los principales factores de riesgo cardiovascular de la población (Instituto Nacional de Estadística e Informática [INEI], 2025).

Este contexto permite sustentar la selección del **personal de enfermería cardiovascular** y los **médicos especialistas cardiovasculares** como segmentos principales de Nurse Pulse. Ambos participan directamente en procesos de registro, monitoreo, consulta y comunicación de información relacionada con pacientes que presentan enfermedades cardiovasculares o factores de riesgo asociados.

---

#### Justificación de selección de segmentos

Los segmentos seleccionados se relacionan directamente con el problema central de Nurse Pulse: la **gestión y trazabilidad de información clínica cardiovascular**.

El **personal de enfermería cardiovascular** representa principalmente los procesos de monitoreo, registro de signos vitales, documentación de eventos y comunicación entre turnos.

Los **médicos especialistas cardiovasculares** representan los procesos de consulta, interpretación de la evolución clínica y utilización de información relevante para la evaluación del paciente.

Finalmente, los **hospitales, clínicas y centros especializados en cardiología** representan al cliente institucional que podría adoptar la solución, definir sus condiciones de utilización y evaluar su integración dentro de los procesos existentes.

Esta separación permite mantener coherencia entre la problemática, los segmentos objetivo, las entrevistas, los User Personas, las hipótesis, los experimentos y las funcionalidades propuestas para Nurse Pulse.

La investigación deberá evitar asumir que todos los profesionales o instituciones trabajan de la misma manera. Las características, necesidades y dificultades planteadas en este capítulo representan hipótesis iniciales que deberán ser contrastadas posteriormente mediante entrevistas y experimentos con participantes representativos.
