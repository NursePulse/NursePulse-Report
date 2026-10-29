# Capítulo VIII: Experiment-Driven Development

## 8.1. Experiment Planning

### 8.1.1. As-Is Summary.

### 8.1.2. Raw Material: Assumptions, Knowledge Gaps, Ideas, Claims.

### 8.1.3. Experiment-Ready Questions.

### 8.1.4. Question Backlog.

### 8.1.5. Experiments Cards.


## 8.2. Experiment Design

El diseño del experimento define qué se va a probar, con qué medidas y bajo qué condiciones, antes de recolectar cualquier dato. Su propósito es que cada experimento de NursePulse parta de una hipótesis clara, específica y medible, de modo que el resultado permita decidir si una funcionalidad se mantiene, se ajusta o se descarta.

Las hipótesis de esta sección no se inventan desde cero: provienen de los *Lean UX Hypothesis Statements* H-01 a H-08 de la sección 1.2.2.3, que a su vez se apoyan en los supuestos de la sección 1.2.2.2. Los umbrales numéricos se vinculan, cuando corresponde, con los Business Goals SMART de la sección 3.4 (BG-02: validación del traspaso SBAR en al menos 3 instituciones; BG-03: reducción de 30 % en el tiempo de búsqueda de información clínica; BG-05: 85 % de trazabilidad completa).

Como se indicó en el Capítulo I, **los valores cuantitativos son objetivos provisionales**: se ajustarán cuando se obtenga una línea base mediante las primeras sesiones con usuarios. Esta sección describe el **diseño**; la ejecución y los resultados se documentarán en la sección 8.3 y no se anticipan aquí.

### 8.2.1. Hypotheses.

Cada hipótesis se expresa con cuatro elementos: la **pregunta** que se quiere responder, la **creencia** del equipo que la origina, la **hipótesis** con su umbral medible y la **hipótesis nula** que se asume cierta hasta que la evidencia indique lo contrario. Para cada una se indica el identificador de la hipótesis Lean UX de la que proviene.

**H-01 — Traspaso de turno mediante SBAR**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿El personal de enfermería cardiovascular comunicará información más completa durante un cambio de turno si usa un formulario digital estructurado con SBAR que si usa un mensaje no estructurado? |
| Creencia | La comunicación no estructurada durante un cambio de turno puede provocar omisiones, y un formulario basado en SBAR ayuda a estructurar la entrega de información. |
| Hipótesis | Creemos que, al usar el formulario SBAR de NursePulse, el personal de enfermería omitirá menos elementos relevantes del traspaso porque el formulario exige completar situación, antecedentes, evaluación y recomendación, evidenciado por una tasa de omisión al menos 15 puntos porcentuales menor que con un mensaje libre. |
| Hipótesis nula | La tasa de omisión con el formulario SBAR será menos de 15 puntos porcentuales menor que con un mensaje libre, por lo que estructurar el traspaso no mejora de forma relevante su completitud. |

**H-02 — Registro de signos vitales**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿El personal de enfermería completará correctamente el registro de signos vitales en NursePulse, sin omitir campos esenciales, en escenarios simulados de atención? |
| Creencia | El registro digital de signos vitales puede facilitar la toma de mediciones y reducir la dependencia de registros complementarios. |
| Hipótesis | Creemos que al menos el 90 % de los registros de signos vitales se completarán correctamente a la primera, con una omisión de campos esenciales de 5 % o menos, porque el formulario muestra el rango válido de cada medición, evidenciado por una tasa de finalización correcta igual o superior al 90 %. |
| Hipótesis nula | La tasa de finalización correcta será inferior al 90 %, por lo que el formulario no resulta lo bastante claro para registrar las mediciones sin errores ni omisiones. |

**H-03 — Consulta de evolución clínica**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿Los médicos especialistas cardiovasculares localizarán más rápido la información reciente de un paciente con una vista resumida de evolución que con datos distribuidos en secciones separadas? |
| Creencia | La fragmentación de la información aumenta el tiempo necesario para completar tareas de consulta, y una vista resumida facilita encontrar lo relevante. |
| Hipótesis | Creemos que el tiempo medio para localizar la información solicitada será al menos 30 % menor con la vista de seguimiento del paciente de NursePulse que con una vista donde los datos están separados, sin aumentar las respuestas incorrectas, evidenciado por una reducción del tiempo medio de localización de 30 % o más. |
| Hipótesis nula | La reducción del tiempo medio de localización será inferior al 30 %, o las respuestas incorrectas aumentarán, por lo que la vista resumida no mejora de forma relevante la consulta. |

**H-04 — Trazabilidad clínica**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿Los profesionales clínicos podrán identificar quién realizó una acción, cuándo y sobre qué registro al revisar el historial y la auditoría de NursePulse? |
| Creencia | Los usuarios necesitan saber quién realizó determinados registros y cuándo ocurrieron, y mostrar responsable, fecha y hora genera confianza en los datos. |
| Hipótesis | Creemos que al menos el 85 % de las respuestas sobre responsable, fecha, hora y registro involucrado serán correctas porque cada registro muestra esos datos, evidenciado por una tasa de respuestas correctas igual o superior al 85 %. |
| Hipótesis nula | La tasa de respuestas correctas será inferior al 85 %, por lo que mostrar responsable, fecha y hora no basta para reconstruir las acciones con facilidad. |

**H-05 — Alertas y eventos relevantes**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿Los usuarios clínicos reconocerán más rápido la alerta que requiere atención prioritaria si la lista de alertas tiene jerarquía visual (severidad, estado y filtros) que si se presenta sin priorización? |
| Creencia | La presentación visual de las alertas ayuda a reconocer la información que requiere atención. |
| Hipótesis | Creemos que el tiempo para identificar la alerta de mayor prioridad será al menos 30 % menor con la jerarquía visual de NursePulse, con una identificación correcta de al menos 90 %, evidenciado por la reducción del tiempo de reconocimiento y la tasa de acierto. |
| Hipótesis nula | La reducción del tiempo será inferior al 30 %, o la identificación correcta será inferior al 90 %, por lo que la jerarquía visual no mejora de forma relevante el reconocimiento de alertas. |

**H-06 — Aplicación móvil**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿El personal de enfermería realizará tareas de registro y consulta cerca del paciente con la aplicación móvil al menos igual de bien, y más rápido, que con la aplicación web en una estación de trabajo? |
| Creencia | Una aplicación móvil puede resultar útil para actividades realizadas cerca del paciente. |
| Hipótesis | Creemos que la aplicación móvil logrará una tasa de finalización de tareas no inferior a la de la web (margen de 10 puntos porcentuales) y un tiempo al menos 20 % menor, sin más errores, evidenciado por ambas medidas en el mismo conjunto de tareas. |
| Hipótesis nula | La tasa de finalización móvil será más de 10 puntos porcentuales inferior a la de la web, o el ahorro de tiempo será menor al 20 %, por lo que la aplicación móvil no aporta valor adicional en ese escenario. |

**H-07 — Landing Page**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿Los visitantes comprenderán qué problema resuelve NursePulse y encontrarán por su cuenta cómo solicitar información después de explorar la Landing Page? |
| Creencia | Una Landing Page con propuesta de valor clara, funcionalidades principales y llamados a la acción permite que el visitante comprenda el producto. |
| Hipótesis | Creemos que al menos el 70 % de los visitantes explicará correctamente la finalidad de NursePulse y al menos el 80 % localizará sin ayuda la acción para solicitar información, evidenciado por ambas tasas de comprensión y localización. |
| Hipótesis nula | La tasa de comprensión será inferior al 70 % o la de localización inferior al 80 %, por lo que la Landing Page no comunica con claridad la propuesta de valor. |

**H-08 — Adopción institucional**

| Elemento | Descripción |
| :--- | :--- |
| Pregunta | ¿Los representantes de instituciones de salud entenderán que NursePulse es una herramienta complementaria, y no un reemplazo de su sistema hospitalario, y mostrarán interés en evaluarla? |
| Creencia | Presentar NursePulse como una herramienta digital complementaria enfocada en comunicación, trazabilidad y seguimiento cardiovascular facilita su comprensión y su evaluación. |
| Hipótesis | Creemos que al menos el 70 % de los representantes institucionales entrevistados diferenciará correctamente el alcance de NursePulse frente a un HIS o EHR, y que al menos 3 instituciones mostrarán interés en evaluarlo en un escenario definido, evidenciado por ambas condiciones (BG-02). |
| Hipótesis nula | Menos del 70 % diferenciará correctamente el alcance, o menos de 3 instituciones mostrarán interés, por lo que el planteamiento actual no logra una adopción inicial. |

### 8.2.2. Domain Business Metrics.

Cada hipótesis se evalúa con una métrica de dominio. La tabla indica qué mide, cómo se calcula, cómo se recolecta y cuál es la meta que respalda la hipótesis.

| Métrica | Descripción | Fórmula / Método de cálculo | Técnica de recolección | Meta deseada |
| :--- | :--- | :--- | :--- | :--- |
| **M-01** Tasa de omisión SBAR | Porcentaje de elementos relevantes del traspaso que no se comunican. | (Elementos omitidos / Elementos relevantes del escenario) × 100 | Lista de verificación aplicada por el equipo sobre cada traspaso simulado | ≥ 15 puntos porcentuales menos que el mensaje libre |
| **M-02** Tasa de finalización correcta de signos vitales | Porcentaje de registros completados sin errores ni campos esenciales omitidos. | (Registros correctos a la primera / Registros intentados) × 100 | Observación de escenarios simulados y registro de los datos guardados | ≥ 90 % |
| **M-03** Tiempo de localización de información | Tiempo para encontrar un dato clínico solicitado y reducción frente a la vista de control. | ((Tiempo control − Tiempo NursePulse) / Tiempo control) × 100 | Cronometraje por tarea y verificación de la respuesta | ≥ 30 % de reducción |
| **M-04** Tasa de respuestas correctas de trazabilidad | Porcentaje de preguntas sobre responsable, fecha, hora y registro respondidas correctamente. | (Respuestas correctas / Respuestas totales) × 100 | Cuestionario de escenario sobre el historial y la auditoría | ≥ 85 % |
| **M-05** Tiempo y acierto en reconocimiento de alertas | Tiempo para identificar la alerta de mayor prioridad y si fue la correcta. | Tiempo hasta la primera selección; (Aciertos / Intentos) × 100 | Cronometraje y registro de la alerta elegida | ≥ 30 % menos tiempo y ≥ 90 % de acierto |
| **M-06** Eficiencia de tareas móvil vs. web | Tasa de finalización y tiempo por tarea en móvil frente a web. | (Tareas completadas / Tareas intentadas) × 100 y reducción porcentual del tiempo | Observación cronometrada con las mismas tareas en ambos dispositivos | Finalización no inferior (margen 10 pp) y ≥ 20 % menos tiempo |
| **M-07** Comprensión de la propuesta de valor | Porcentaje de visitantes que explica la finalidad del producto y encuentra el llamado a la acción. | (Visitantes que explican y localizan / Visitantes observados) × 100 | Prueba de comprensión con una pregunta abierta y una tarea | ≥ 70 % explican y ≥ 80 % localizan |
| **M-08** Diferenciación de alcance e interés institucional | Porcentaje que diferencia a NursePulse de un HIS y número de instituciones interesadas. | (Representantes que diferencian / Entrevistados) × 100; recuento de instituciones | Entrevista guiada y escenario de evaluación | ≥ 70 % y ≥ 3 instituciones |

### 8.2.3. Measures.

Esta sección define las medidas que reúnen la evidencia para aceptar o refutar cada hipótesis. Se priorizan medidas cuantificables, comparables entre la condición experimental y la de control, y recolectables con herramientas que el proyecto ya tiene o puede incorporar sin costo (ver 8.2.6). Cada medida responde a una métrica de dominio de la sección 8.2.2.

**Medidas seleccionadas:**

* **SBAR Omission Rate (SOR)**
  * Propósito: medir cuántos elementos relevantes del traspaso de turno se omiten con SBAR y con un mensaje libre.
  * Indicador esperado: al menos 15 puntos porcentuales menos de omisión con SBAR.
  * Método: lista de verificación de los elementos definidos para cada escenario, aplicada a cada traspaso simulado.

* **Vital Signs Completion Rate (VCR)**
  * Propósito: medir cuántos registros de signos vitales se completan correctamente a la primera.
  * Indicador esperado: al menos 90 % de registros correctos y 5 % o menos de campos esenciales omitidos.
  * Método: observación de escenarios simulados y revisión de los datos guardados.

* **Clinical Information Retrieval Time (CIRT)**
  * Propósito: medir el tiempo que toma localizar información reciente de un paciente.
  * Indicador esperado: reducción del tiempo medio de al menos 30 % frente a la vista de control, sin aumentar las respuestas incorrectas.
  * Método: cronometraje por tarea con verificación de la respuesta.

* **Traceability Accuracy Rate (TAR)**
  * Propósito: medir si el usuario reconstruye correctamente quién hizo qué y cuándo.
  * Indicador esperado: al menos 85 % de respuestas correctas.
  * Método: cuestionario de escenario sobre el historial del paciente y la auditoría.

* **Priority Alert Recognition Time (PART)**
  * Propósito: medir cuánto tarda el usuario en identificar la alerta que requiere atención prioritaria y si acierta.
  * Indicador esperado: al menos 30 % menos de tiempo y 90 % de acierto.
  * Método: cronometraje y registro de la alerta seleccionada en una lista con y sin jerarquía visual.

* **Mobile Task Efficiency (MTE)**
  * Propósito: comparar tasa de finalización y tiempo de las mismas tareas en la aplicación móvil y en la web.
  * Indicador esperado: finalización no inferior en más de 10 puntos porcentuales y al menos 20 % menos de tiempo.
  * Método: observación cronometrada con un mismo guion de tareas.

* **Value Proposition Comprehension Rate (VPCR)**
  * Propósito: verificar que el visitante comprende qué resuelve NursePulse y encuentra cómo solicitar información.
  * Indicador esperado: al menos 70 % explica correctamente la finalidad y 80 % localiza la acción sin ayuda.
  * Método: prueba de comprensión con una pregunta abierta y una tarea de localización.

* **Scope Differentiation Rate (SDR)**
  * Propósito: verificar que los representantes institucionales entienden el alcance complementario de NursePulse y su interés en evaluarlo.
  * Indicador esperado: al menos 70 % diferencia el alcance y al menos 3 instituciones muestran interés.
  * Método: entrevista guiada y escenario de evaluación institucional.

* **System Usability Scale (SUS)** *(medida transversal)*
  * Propósito: obtener una valoración global de usabilidad de la web y de la aplicación móvil que acompañe a las medidas anteriores.
  * Indicador esperado: puntaje SUS igual o superior a 68, valor de referencia habitual para una usabilidad aceptable.
  * Método: cuestionario de 10 preguntas al terminar cada sesión.

### 8.2.4. Conditions.

Para cada pregunta se redacta una **condición experimental**, que introduce la funcionalidad de NursePulse para buscar evidencia a favor de la hipótesis, y una **condición de control**, que representa la práctica actual sin esa funcionalidad y supone que la hipótesis nula es cierta. Todas las sesiones usan **escenarios y datos simulados**, sin pacientes reales.

| Hipótesis | Condición experimental | Condición de control |
| :--- | :--- | :--- |
| **H-01** SBAR | Cada participante realiza traspasos simulados con el formulario SBAR de NursePulse (situación, antecedentes, evaluación y recomendación). Se espera una omisión al menos 15 puntos porcentuales menor que en el control. | Los mismos escenarios se comunican con un mensaje libre, como se hace hoy por mensajería o de forma verbal. La diferencia de omisión es menor a 15 puntos porcentuales. |
| **H-02** Signos vitales | Los participantes registran las mediciones de un escenario en el formulario de signos vitales, que muestra el rango válido de cada campo. Al menos 90 % de los registros se completan correctamente. | Los participantes anotan las mismas mediciones en el formato que usan actualmente (papel o planilla). La tasa de registros correctos es inferior al 90 %. |
| **H-03** Evolución clínica | Los médicos responden preguntas sobre un paciente usando la vista de seguimiento de NursePulse (historial de signos vitales, alertas y diagnóstico). El tiempo medio es al menos 30 % menor. | Los médicos responden las mismas preguntas consultando los datos en secciones separadas. La reducción del tiempo es inferior al 30 %. |
| **H-04** Trazabilidad | Los participantes revisan el historial y la auditoría de NursePulse, que muestran responsable, fecha y hora, y responden sobre quién hizo qué y cuándo. Al menos 85 % de respuestas correctas. | Los participantes responden las mismas preguntas con registros que no muestran esos datos. Menos de 85 % de respuestas correctas. |
| **H-05** Alertas | Los participantes identifican la alerta prioritaria en una lista con severidad, estado y filtros. El tiempo es al menos 30 % menor y el acierto de 90 % o más. | Los participantes identifican la alerta prioritaria en una lista plana, sin jerarquía visual. La reducción es inferior al 30 % o el acierto inferior al 90 %. |
| **H-06** Móvil | Los participantes realizan tareas de registro y consulta con la aplicación móvil. La finalización no es inferior en más de 10 puntos porcentuales y el tiempo es al menos 20 % menor. | Los participantes realizan las mismas tareas con la aplicación web en una estación de trabajo. |
| **H-07** Landing | Los visitantes exploran la Landing Page y se les pide explicar la finalidad del producto y encontrar cómo solicitar información. Al menos 70 % y 80 % respectivamente. | Los visitantes observan una versión sin propuesta de valor ni llamados a la acción destacados. Las tasas son inferiores a esos umbrales. |
| **H-08** Adopción institucional | Se presenta NursePulse como herramienta complementaria y se pide a cada representante describir su alcance y su interés. Al menos 70 % lo diferencia de un HIS y al menos 3 instituciones se interesan. | Se presenta una descripción genérica de plataforma de gestión clínica. Menos de 70 % diferencia el alcance o menos de 3 instituciones se interesan. |

### 8.2.5. Scale Calculations and Decisions.

Cada hipótesis se asocia con un indicador de éxito y con tres zonas de decisión. El resultado se considera **favorable** cuando la métrica alcanza el valor objetivo, **inconcluso** cuando queda entre el mínimo aceptable y el objetivo, y **desfavorable** cuando queda por debajo del mínimo, caso en el que se revisa la estrategia. Un nivel **excelente** corresponde a superar el objetivo por 25 % o más.

Todas las pruebas usan un **nivel de significación de 5 %** y un **poder estadístico de 80 %**. Los tamaños de muestra se calcularon así: para una proporción frente a un umbral, la aproximación normal de una cola; para dos proporciones, la aproximación normal de dos colas; y para comparaciones de tiempos con los mismos participantes (diseño pareado), una prueba *t* con tamaño de efecto grande (d = 0,8), añadiendo 2 participantes por usar la distribución *t*.

**H-01 — Traspaso de turno mediante SBAR**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | La omisión con SBAR será al menos 15 puntos porcentuales menor que con mensaje libre. |
| Hipótesis nula | La diferencia será menor a 15 puntos porcentuales. |
| Nivel de significación | 5 %. |
| Poder estadístico | 80 %. |
| MDE | 15 puntos porcentuales (supuesto de partida: 30 % de omisión en el control y 15 % con SBAR). |
| Cantidad de evidencia necesaria | 121 elementos evaluados por condición. Con 8 elementos relevantes por traspaso (2 por cada componente de SBAR) equivalen a unos 15 traspasos por condición; como los elementos de un mismo traspaso no son independientes, se analizarán por traspaso. |
| Criterio para validar H1 | Diferencia de omisión ≥ 15 puntos porcentuales. |
| Criterio para validar H0 | Diferencia < 8 puntos porcentuales. |
| Resultado inconcluso | Entre 8 y 15 puntos porcentuales. |

**H-02 — Registro de signos vitales**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | Al menos 90 % de los registros se completan correctamente a la primera. |
| Hipótesis nula | La tasa de finalización correcta es inferior al 90 %. |
| Nivel de significación | 5 %. |
| Poder estadístico | 80 %. |
| MDE | 10 puntos porcentuales (mínimo aceptable 80 %). |
| Cantidad de evidencia necesaria | 83 intentos de registro. Con 5 escenarios por participante equivalen a unos 17 participantes. |
| Criterio para validar H1 | Tasa de finalización correcta ≥ 90 %. |
| Criterio para validar H0 | Tasa de finalización correcta < 80 %. |
| Resultado inconcluso | Entre 80 % y 90 %. |

**H-03 — Consulta de evolución clínica**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | El tiempo medio de localización se reduce al menos 30 % con la vista de seguimiento. |
| Hipótesis nula | La reducción es inferior al 30 % o aumentan las respuestas incorrectas. |
| Nivel de significación | 5 %. |
| Poder estadístico | 80 %. |
| MDE | Reducción de 30 % del tiempo (tamaño de efecto grande, d = 0,8). |
| Cantidad de evidencia necesaria | 15 participantes, cada uno con ambas vistas (diseño pareado), alternando el orden. |
| Criterio para validar H1 | Reducción ≥ 30 % con diferencia significativa y sin aumento de respuestas incorrectas. |
| Criterio para validar H0 | Reducción < 15 % o aumento de respuestas incorrectas. |
| Resultado inconcluso | Reducción entre 15 % y 30 %. |

**H-04 — Trazabilidad clínica**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | Al menos 85 % de las respuestas sobre responsable, fecha y hora son correctas. |
| Hipótesis nula | La tasa de respuestas correctas es inferior al 85 %. |
| Nivel de significación | 5 %. |
| Poder estadístico | 80 %. |
| MDE | 15 puntos porcentuales (mínimo aceptable 70 %). |
| Cantidad de evidencia necesaria | 50 respuestas. Con 5 preguntas por participante equivalen a 10 participantes. |
| Criterio para validar H1 | Respuestas correctas ≥ 85 %. |
| Criterio para validar H0 | Respuestas correctas < 70 %. |
| Resultado inconcluso | Entre 70 % y 85 %. |

**H-05 — Alertas y eventos relevantes**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | El tiempo para identificar la alerta prioritaria se reduce al menos 30 % con la jerarquía visual y el acierto es de al menos 90 %. |
| Hipótesis nula | La reducción es inferior al 30 % o el acierto es inferior al 90 %. |
| Nivel de significación | 5 %. |
| Poder estadístico | 80 %. |
| MDE | Reducción de 30 % del tiempo (d = 0,8); para el acierto, 15 puntos porcentuales sobre un mínimo de 75 %. |
| Cantidad de evidencia necesaria | 15 participantes con ambas listas (pareado) para el tiempo, y 42 intentos para el acierto, que se cubren con 3 intentos por participante. |
| Criterio para validar H1 | Reducción de tiempo ≥ 30 % y acierto ≥ 90 %. |
| Criterio para validar H0 | Reducción < 15 % o acierto < 75 %. |
| Resultado inconcluso | Cualquier otro caso entre esos valores. |

**H-06 — Aplicación móvil**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | La finalización móvil no es inferior a la de la web en más de 10 puntos porcentuales y el tiempo es al menos 20 % menor. |
| Hipótesis nula | La finalización móvil es más de 10 puntos porcentuales inferior o el ahorro de tiempo es menor al 20 %. |
| Nivel de significación | 5 %. |
| Poder estadístico | 80 %. |
| MDE | Reducción de 20 % del tiempo y margen de no inferioridad de 10 puntos porcentuales. |
| Cantidad de evidencia necesaria | 15 participantes que realicen el mismo guion en móvil y en web (pareado). |
| Criterio para validar H1 | Ambas condiciones se cumplen y no hay más errores en móvil. |
| Criterio para validar H0 | Finalización móvil más de 10 puntos porcentuales inferior o ahorro de tiempo < 10 %. |
| Resultado inconcluso | Ahorro de tiempo entre 10 % y 20 %, o evidencia insuficiente sobre la finalización. |

**H-07 — Landing Page**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | Al menos 70 % explica correctamente la finalidad y 80 % localiza la acción sin ayuda. |
| Hipótesis nula | La comprensión es inferior al 70 % o la localización inferior al 80 %. |
| Nivel de significación | 5 %. |
| Poder estadístico | 80 %. |
| MDE | 20 puntos porcentuales (mínimo aceptable 50 % de comprensión). |
| Cantidad de evidencia necesaria | 37 visitantes. |
| Criterio para validar H1 | Comprensión ≥ 70 % y localización ≥ 80 %. |
| Criterio para validar H0 | Comprensión < 50 %. |
| Resultado inconcluso | Comprensión entre 50 % y 70 %. |

**H-08 — Adopción institucional**

| Elemento | Descripción |
| :--- | :--- |
| Hipótesis | Al menos 70 % diferencia el alcance frente a un HIS y al menos 3 instituciones muestran interés (BG-02). |
| Hipótesis nula | Menos de 70 % diferencia el alcance o menos de 3 instituciones muestran interés. |
| Nivel de significación | No aplica una prueba estadística: es un estudio cualitativo y descriptivo. |
| Poder estadístico | No aplica. |
| MDE | No aplica. |
| Cantidad de evidencia necesaria | Entre 5 y 8 entrevistas institucionales, hasta que las respuestas dejen de aportar objeciones nuevas. |
| Criterio para validar H1 | Al menos 70 % de diferenciación correcta y 3 o más instituciones interesadas. |
| Criterio para validar H0 | Menos de 50 % de diferenciación correcta o menos de 2 instituciones interesadas. |
| Resultado inconcluso | Cualquier caso intermedio. |

**Consideraciones sobre las muestras.** Las cifras anteriores son el mínimo para decidir con la confianza indicada. El proyecto trabaja con recursos de un equipo universitario, por lo que el primer ciclo puede contar con menos participantes. En ese caso los resultados se presentarán como **exploratorios**, con su intervalo de confianza, y se ampliarán en un segundo ciclo antes de tomar decisiones definitivas. Antes de la primera sesión se medirá una **línea base** para confirmar o corregir los supuestos de partida (por ejemplo, el 30 % de omisión del control en H-01).

### 8.2.6. Methods Selection.

Para recolectar las medidas se compararon herramientas gratuitas o ya presentes en el proyecto. Se eligió una combinación que cubre la observación del comportamiento en la web, la analítica de la aplicación móvil, la salud del sistema, la calidad web y la percepción de los usuarios.

| Herramienta | Microsoft Clarity | Firebase Analytics | Grafana Cloud | Lighthouse | Cuestionario SUS (Google Forms) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Precio** | Gratuito | Gratuito | Plan gratuito con límites mensuales | Gratuito (código abierto) | Gratuito |
| **Capacidad de análisis** | Grabaciones de sesión y mapas de calor de la aplicación web y de la Landing Page | Eventos, pantallas y embudos de la aplicación móvil Flutter | Métricas del backend (JVM y HTTP) y paneles de disponibilidad | Rendimiento, accesibilidad, buenas prácticas y SEO de una página | Puntaje de usabilidad percibida y comentarios abiertos |
| **Sencillez** | Se agrega con un script y no requiere configuración avanzada | Se integra con un paquete de Flutter y un proyecto de Firebase | Ya configurado: el backend exporta métricas por OTLP | Ya integrado en el pipeline del frontend | Formulario sin instalación |
| **Ventajas** | Muestra cómo interactúa el usuario con alertas, SBAR y la vista del paciente sin cambiar el código de negocio | El proyecto ya usa Firebase App Distribution, por lo que el proyecto de Firebase existe | Permite relacionar el uso con la salud del sistema durante las sesiones | Mide objetivamente la calidad de la Landing Page y de la pantalla de inicio de sesión | Permite comparar la percepción de enfermería, médicos y administradores |
| **Limitaciones** | Debe enmascarar los datos del paciente y usarse solo con datos simulados | Requiere agregar el SDK y definir los eventos (8.2.8) | No mide comportamiento de usuario, solo infraestructura | Solo evalúa páginas individuales, no flujos | Depende de que el participante responda |
| **Hipótesis que respalda** | H-03, H-05, H-07 | H-02, H-06 | Contexto de todas | H-07 | Todas (transversal) |

Además de estas herramientas externas, el sistema ya cuenta con una fuente propia de datos: la **tabla de auditoría** del backend, que registra la acción, el usuario, la entidad y la fecha y hora de cada operación. Sirve para respaldar H-04 (trazabilidad) y para verificar qué acciones realizó cada participante durante una sesión.

**Evidencia de ejecución de los métodos**

Solo se indica como ejecutado lo que existe hoy en el proyecto. El resto queda como planificado para la sección 8.3, donde se documentarán las fechas y los resultados reales.

| Herramienta | Métrica asociada | Estado | Evidencia |
| :--- | :--- | :--- | :--- |
| Lighthouse | H-07: calidad de la interfaz web | Ejecutado en el pipeline `Frontend CI` contra la pantalla de inicio de sesión desplegada | Reporte y análisis en el Capítulo VI (sección 6.1.4) |
| Grafana Cloud | Contexto de salud del sistema | Ejecutado: el backend exporta métricas desde producción (TS-09) | Descripción y paneles en el Capítulo VII (sección 7.4) |
| Tabla de auditoría del backend | H-04: trazabilidad | Disponible: se registra cada operación de las aplicaciones | Historia US-35 y su prueba (Capítulo VI, sección 6.1.5) |
| Microsoft Clarity | H-03, H-05, H-07 | Planificado: aún no está instalado | Se documentará en 8.3 |
| Firebase Analytics | H-02, H-06 | Planificado: aún no está instalado | Se documentará en 8.3 |
| Cuestionario SUS | Todas | Planificado: aún no se ha aplicado | Se documentará en 8.3 |

### 8.2.7. Data Analysis: Goals, KPIs and Metrics Selection.

Esta sección vincula los objetivos de negocio con los indicadores que se analizarán. Parte de los Business Goals de la sección 3.4, define el KPI de cada uno, las métricas que lo alimentan y la fuente de datos. Se separan los indicadores de la **aplicación web** y de la **aplicación móvil**, y siempre que es posible se segmentan por rol (enfermería, médico y administrador).

#### Web

| Objetivo | KPI | Métricas que lo alimentan | Fuente de datos | Segmento |
| :--- | :--- | :--- | :--- | :--- |
| Reducir el tiempo de búsqueda de información clínica (BG-03) | Reducción del tiempo de localización | M-03 (CIRT) | Cronometraje y grabaciones de sesión | Médico |
| Lograr traspasos más completos (BG-02) | Tasa de omisión SBAR | M-01 (SOR) | Lista de verificación y tabla de auditoría | Enfermería |
| Garantizar trazabilidad de los registros (BG-05) | Tasa de respuestas correctas de trazabilidad | M-04 (TAR) | Cuestionario de escenario y auditoría | Médico y administrador |
| Reconocer rápido la alerta prioritaria | Tiempo y acierto en la primera alerta | M-05 (PART) | Cronometraje y eventos de la lista de alertas | Enfermería y médico |
| Captar interesados desde la Landing Page (BG-01) | Comprensión de la propuesta y clics en el llamado a la acción | M-07 (VPCR) | Grabaciones de sesión, mapas de calor y reporte de Lighthouse | Visitantes |
| Validar la adopción institucional (BG-02) | Instituciones interesadas | M-08 (SDR) | Entrevistas | Representantes institucionales |
| Evaluar la usabilidad general | Puntaje SUS | SUS | Cuestionario | Todos los roles |

#### Mobile

| Objetivo | KPI | Métricas que lo alimentan | Fuente de datos | Segmento |
| :--- | :--- | :--- | :--- | :--- |
| Registrar signos vitales sin errores cerca del paciente (BG-04) | Tasa de finalización correcta | M-02 (VCR) | Eventos de Firebase Analytics y observación | Enfermería |
| Comprobar el valor del dispositivo móvil | Eficiencia móvil frente a web | M-06 (MTE) | Observación cronometrada y eventos | Enfermería |
| Reducir omisiones en traspasos desde el móvil (BG-02) | Tasa de omisión SBAR en móvil | M-01 (SOR) | Lista de verificación y auditoría | Enfermería |
| Atender alertas a tiempo | Tiempo hasta atender la alerta | M-05 (PART) | Eventos de la lista de alertas | Enfermería y médico |
| Medir la salud de la aplicación | Sesiones sin error | Sesiones, errores y tiempo de respuesta del backend | Firebase Analytics y Grafana Cloud | Todos los roles |

Los tableros se construirán en la sección 8.3, cuando existan datos de las sesiones. Hasta entonces no se incluyen capturas, porque no hay datos reales que mostrar.

### 8.2.8. Web and Mobile Tracking Plan.

El objetivo del plan de seguimiento es registrar, en la aplicación web y en la móvil, los eventos mínimos necesarios para calcular las métricas de la sección 8.2.2 durante los experimentos y, después, para seguir el uso real de NursePulse. El seguimiento se hará en dos etapas.

**1. Línea base y experimentos controlados**

- **Qué se recopila:** los eventos de la tabla siguiente en sesiones con escenarios simulados, junto con el cronometraje y el cuestionario SUS.
- **Para qué:** establecer la línea base de cada métrica y confirmar o corregir los umbrales provisionales de la sección 8.2.5.
- **Análisis:** comparación entre la condición experimental y la de control de cada hipótesis.

**2. Seguimiento continuo**

- **Métricas de uso:** usuarios activos, sesiones, tareas completadas y errores, segmentados por rol y por dispositivo.
- **Retención:** proporción de usuarios que regresan a la aplicación en semanas sucesivas.
- **Informes periódicos:** un resumen con los hallazgos y los ajustes recomendados, para iterar el producto con evidencia.

**Estado actual.** NursePulse **todavía no tiene una herramienta de analítica de producto instalada** (ni en la web ni en la móvil). Lo que sí existe hoy es la tabla de auditoría del backend, que ya recibe las operaciones de las aplicaciones: creación, actualización, consulta, registro de signos vitales, traspaso SBAR, alerta generada y alerta atendida. Los eventos marcados como "Nuevo" deberán implementarse en la fase de experimentación.

**Convención de nombres.** Los eventos usan `snake_case`, empiezan por el módulo (por ejemplo `sbar_`, `vital_signs_`, `alert_`) y llevan siempre la propiedad `channel` con valor `web` o `mobile`, y `role` con el rol del usuario.

**Eventos de la aplicación web**

| Evento | Cuándo se dispara | Propiedades principales | Métrica / hipótesis | Estado |
| :--- | :--- | :--- | :--- | :--- |
| `sign_in_succeeded` | El usuario inicia sesión | `role` | Contexto | Nuevo |
| `sbar_form_opened` | Se abre el formulario SBAR | `role` | M-01 / H-01 | Nuevo |
| `sbar_submitted` | Se guarda un traspaso | `fields_completed`, `duration_ms` | M-01 / H-01 | Parcial: la auditoría registra el traspaso |
| `vital_signs_form_opened` | Se abre el formulario de signos vitales | `role` | M-02 / H-02 | Nuevo |
| `vital_signs_submitted` | Se guardan signos vitales | `validation_errors`, `duration_ms` | M-02 / H-02 | Parcial: la auditoría registra el registro |
| `patient_monitoring_opened` | Se abre la ficha de seguimiento | `patient_ref` | M-03 / H-03 | Nuevo |
| `info_found` | El participante marca que localizó el dato pedido | `task_id`, `duration_ms` | M-03 / H-03 | Nuevo |
| `audit_log_viewed` | Se consulta la auditoría | `patient_filter_used` | M-04 / H-04 | Parcial: la auditoría registra la consulta |
| `alert_list_viewed` | Se abre la lista de alertas | `filter` | M-05 / H-05 | Nuevo |
| `alert_first_opened` | Se abre la primera alerta | `severity`, `duration_ms` | M-05 / H-05 | Nuevo |
| `alert_attended` | Se atiende una alerta | `severity` | M-05 / H-05 | Parcial: la auditoría registra la atención |
| `landing_cta_clicked` | Se pulsa el llamado a la acción de la Landing Page | `cta_id` | M-07 / H-07 | Nuevo |

**Eventos de la aplicación móvil**

| Evento | Cuándo se dispara | Propiedades principales | Métrica / hipótesis | Estado |
| :--- | :--- | :--- | :--- | :--- |
| `app_opened` | Se abre la aplicación | `role` | Contexto | Nuevo |
| `sbar_submitted` | Se guarda un traspaso | `fields_completed`, `duration_ms` | M-01 / H-01, H-06 | Parcial: la auditoría registra el traspaso |
| `vital_signs_form_opened` | Se abre el formulario de signos vitales | `role` | M-02 / H-02, H-06 | Nuevo |
| `vital_signs_submitted` | Se guardan signos vitales | `validation_errors`, `duration_ms` | M-02 / H-02, H-06 | Parcial: la auditoría registra el registro |
| `task_completed` | Se completa una tarea del guion | `task_id`, `duration_ms` | M-06 / H-06 | Nuevo |
| `alert_attended` | Se atiende una alerta | `severity`, `duration_ms` | M-05 / H-05 | Parcial: la auditoría registra la atención |
| `app_error` | Ocurre un error no controlado | `screen`, `error_type` | Salud de la aplicación | Nuevo |

**Privacidad.** Ningún evento incluye nombres, documentos ni otros datos que identifiquen a un paciente: cuando hace falta referirse a uno se usa una referencia seudónima (`patient_ref`). Las sesiones experimentales se realizan con **datos simulados**, y cualquier grabación de pantalla debe enmascarar los campos de datos clínicos. Esto es coherente con la Ley N.° 29733, de Protección de Datos Personales, que rige en el Perú.


## 8.3. Experimentation

### 8.3.1. To-Be User Stories.

### 8.3.2. To-Be Product Backlog.
