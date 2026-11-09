# Capítulo VIII: Experiment-Driven Development

## 8.1. Experiment Planning

### 8.1.1. As-Is Summary.

Antes de introducir NursePulse, la comunicación y el registro de información clínica en los servicios de cardiología dependen principalmente de medios no estructurados y en parte físicos. El personal de enfermería transmite los cambios de turno de forma verbal o mediante mensajes libres, sin un formato que obligue a cubrir todos los puntos relevantes del estado del paciente. Los signos vitales y los eventos clínicos se anotan en registros complementarios (papel o planillas) que luego deben transcribirse o consultarse por separado, y la evolución de un paciente solo puede reconstruirse revisando varias fuentes de información dispersas. Tampoco existe un mecanismo uniforme para identificar quién registró una acción ni cuándo ocurrió, ni para priorizar visualmente los eventos que requieren atención inmediata.

**Problemas identificados:**

- **Comunicación no estructurada:** los traspasos de turno no siguen un formato fijo, lo que puede provocar la omisión de información relevante sobre el estado del paciente.
- **Fragmentación de la información:** los signos vitales, los eventos clínicos y las indicaciones se registran en fuentes separadas, lo que aumenta el tiempo necesario para consultar la evolución de un paciente.
- **Trazabilidad limitada:** no siempre es posible identificar con certeza quién realizó un registro ni en qué momento, lo que reduce la confianza en la información disponible.
- **Dependencia de registros físicos:** buena parte de la información queda en papel o en formatos no digitales, lo que dificulta su consulta posterior y su consolidación.
- **Falta de priorización visual de eventos:** los eventos y alertas relevantes no siempre destacan sobre el resto de la información, lo que puede retrasar su reconocimiento.
- **Acceso limitado cerca del paciente:** el registro y la consulta de información suelen depender de estaciones de trabajo fijas, lo que dificulta su uso inmediato junto a la cama del paciente.

**Objetivos de mejora:**

- **Estructurar la comunicación de traspasos:** introducir un formulario digital basado en SBAR que guíe al personal de enfermería a cubrir situación, antecedentes, evaluación y recomendación en cada cambio de turno.
- **Consolidar la información clínica:** ofrecer una vista resumida de evolución clínica que reúna signos vitales, eventos y antecedentes recientes del paciente en un mismo lugar.
- **Fortalecer la trazabilidad:** registrar automáticamente el responsable, la fecha y la hora de cada acción clínica relevante.
- **Reducir la dependencia del papel:** digitalizar el registro de signos vitales y eventos clínicos para que puedan consultarse sin recurrir a formatos físicos complementarios.
- **Priorizar visualmente los eventos relevantes:** presentar alertas y eventos clínicos con una jerarquía visual que facilite reconocer lo que requiere atención inmediata.
- **Permitir el registro cercano al paciente:** ofrecer una aplicación móvil nativa para tareas de registro y consulta que no dependan de una estación de trabajo fija.

### 8.1.2. Raw Material: Assumptions, Knowledge Gaps, Ideas, Claims.

**Ideas**

- Ofrecer un formulario digital estructurado con SBAR para los traspasos de turno.
- Incorporar un módulo de registro de signos vitales con validación del rango de cada campo.
- Consolidar una vista de evolución clínica que reúna signos vitales, eventos y alertas recientes del paciente.
- Registrar automáticamente el responsable, la fecha y la hora de cada acción clínica relevante mediante un módulo de auditoría.
- Presentar las alertas y los eventos clínicos con una jerarquía visual según severidad y estado.
- Desarrollar una aplicación móvil nativa para registrar y consultar información cerca del paciente.
- Construir una Landing Page que comunique la propuesta de valor de NursePulse a visitantes y representantes institucionales.

**Claims**

- El personal de enfermería cardiovascular necesita comunicar los cambios de turno sin omitir información relevante sobre el paciente.
- Los médicos especialistas cardiovasculares necesitan consultar la evolución reciente del paciente sin revisar múltiples fuentes dispersas.
- Los profesionales clínicos necesitan saber quién registró una acción, cuándo y sobre qué paciente, para confiar en la información disponible.
- Los usuarios clínicos necesitan reconocer con rapidez qué eventos o alertas requieren atención prioritaria.
- El personal de enfermería necesita registrar y consultar información clínica sin depender de una estación de trabajo fija.
- Los visitantes y representantes institucionales necesitan comprender qué problema resuelve NursePulse antes de solicitar más información.
- Las instituciones de salud necesitan diferenciar a NursePulse de su sistema hospitalario (HIS/EHR) para no interpretarlo como un reemplazo.
- Los profesionales clínicos estarán dispuestos a adoptar NursePulse si aporta valor sin aumentar su carga operativa.

**Assumptions**

Estos supuestos retoman, con el mismo identificador, los definidos en la sección 1.2.2.2.

- Un traspaso mediante SBAR reduce omisiones frente a una comunicación no estructurada (A-01).
- El registro digital de signos vitales reduce la dependencia de medios complementarios como el papel (A-02).
- Una vista resumida de evolución permite a los médicos encontrar información reciente con mayor rapidez (A-03).
- La trazabilidad mediante responsable, fecha y hora aporta valor a los usuarios clínicos (A-04).
- Las instituciones de salud reconocen valor en una solución complementaria especializada en comunicación y trazabilidad cardiovascular (A-05).
- Una aplicación móvil facilita determinados registros realizados cerca del paciente (A-06).
- Una Landing Page clara comunica adecuadamente la propuesta de valor del producto (A-07).

**Knowledge Gaps**

- Se desconoce cuántos elementos del traspaso SBAR el personal de enfermería considera realmente indispensables frente a los que completaría solo por obligación del formulario.
- No se ha determinado si los profesionales clínicos valorarían recibir notificaciones push ante eventos críticos, además de verlos en la lista de alertas.
- Falta información sobre con qué frecuencia los médicos especialistas consultan la evolución de un paciente durante un mismo turno, lo que afecta cuánto debe optimizarse ese flujo.
- No se ha definido con qué frecuencia las instituciones de salud auditarían la trazabilidad de los registros, ni qué nivel de detalle esperan encontrar en ese historial.
- Se desconoce qué proporción de las tareas de registro y consulta ocurre efectivamente cerca del paciente frente a en una estación de trabajo, lo que afecta el valor real de la aplicación móvil.
- No se ha determinado qué tan dispuestos están los médicos especialistas a adoptar un formulario adicional de registro, aun cuando reduzca el tiempo de búsqueda de información.
- Se desconoce qué objeciones concretas plantearían las instituciones de salud sobre seguridad, interoperabilidad o costo antes de evaluar la adopción de NursePulse.

### 8.1.3. Experiment-Ready Questions.

A continuación, se presentan las preguntas generadas a partir de las Ideas, Claims, Assumptions y Knowledge Gaps identificados en la sección de Raw Material. Las preguntas impulsadas por creencias retoman directamente la pregunta y la creencia de cada una de las hipótesis Lean UX H-01 a H-08 de la sección 1.2.2.3, de modo que el diseño experimental de la sección 8.2 responda exactamente a estas preguntas. Las preguntas exploratorias, en cambio, se generaron aplicando la técnica de las 5W2H sobre los Knowledge Gaps, ya que todavía no cuentan con una hipótesis formulada.

#### Preguntas impulsadas por creencias (Belief-led)

**Creencia 1**

<table>
    <tr>
        <th>Creencia</th>
        <td>La comunicación no estructurada durante un cambio de turno puede provocar omisiones, y un formulario basado en SBAR ayuda a estructurar la entrega de información.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿El personal de enfermería cardiovascular comunicará información más completa durante un cambio de turno si usa un formulario digital estructurado con SBAR que si usa un mensaje no estructurado?</td>
    </tr>
</table>

**Creencia 2**

<table>
    <tr>
        <th>Creencia</th>
        <td>El registro digital de signos vitales puede facilitar la toma de mediciones y reducir la dependencia de registros complementarios.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿El personal de enfermería completará correctamente el registro de signos vitales en NursePulse, sin omitir campos esenciales, en escenarios simulados de atención?</td>
    </tr>
</table>

**Creencia 3**

<table>
    <tr>
        <th>Creencia</th>
        <td>La fragmentación de la información aumenta el tiempo necesario para completar tareas de consulta, y una vista resumida facilita encontrar lo relevante.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Los médicos especialistas cardiovasculares localizarán más rápido la información reciente de un paciente con una vista resumida de evolución que con datos distribuidos en secciones separadas?</td>
    </tr>
</table>

**Creencia 4**

<table>
    <tr>
        <th>Creencia</th>
        <td>Los usuarios necesitan saber quién realizó determinados registros y cuándo ocurrieron, y mostrar responsable, fecha y hora genera confianza en los datos.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Los profesionales clínicos podrán identificar quién realizó una acción, cuándo y sobre qué registro al revisar el historial y la auditoría de NursePulse?</td>
    </tr>
</table>

**Creencia 5**

<table>
    <tr>
        <th>Creencia</th>
        <td>La presentación visual de las alertas ayuda a reconocer la información que requiere atención.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Los usuarios clínicos reconocerán más rápido la alerta que requiere atención prioritaria si la lista de alertas tiene jerarquía visual (severidad, estado y filtros) que si se presenta sin priorización?</td>
    </tr>
</table>

**Creencia 6**

<table>
    <tr>
        <th>Creencia</th>
        <td>Una aplicación móvil puede resultar útil para actividades realizadas cerca del paciente.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿El personal de enfermería realizará tareas de registro y consulta cerca del paciente con la aplicación móvil al menos igual de bien, y más rápido, que con la aplicación web en una estación de trabajo?</td>
    </tr>
</table>

**Creencia 7**

<table>
    <tr>
        <th>Creencia</th>
        <td>Una Landing Page con propuesta de valor clara, funcionalidades principales y llamados a la acción permite que el visitante comprenda el producto.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Los visitantes comprenderán qué problema resuelve NursePulse y encontrarán por su cuenta cómo solicitar información después de explorar la Landing Page?</td>
    </tr>
</table>

**Creencia 8**

<table>
    <tr>
        <th>Creencia</th>
        <td>Presentar NursePulse como una herramienta digital complementaria enfocada en comunicación, trazabilidad y seguimiento cardiovascular facilita su comprensión y su evaluación.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Los representantes de instituciones de salud entenderán que NursePulse es una herramienta complementaria, y no un reemplazo de su sistema hospitalario, y mostrarán interés en evaluarla?</td>
    </tr>
</table>

#### Preguntas exploratorias (Exploratory)

Para estas preguntas se utilizaron los Knowledge Gaps identificados en la sección de Raw Material, aplicando la técnica de las 5W2H para obtener información relevante para el diseño del experimento.

**Knowledge Gap 1**

<table>
    <tr>
        <th>Knowledge Gap</th>
        <td>Se desconoce cuántos elementos del traspaso SBAR el personal de enfermería considera realmente indispensables frente a los que completaría solo por obligación del formulario.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Qué elementos del traspaso SBAR considera el personal de enfermería realmente indispensables, quién los usa en el turno siguiente, en qué situaciones los omitiría si tuviera prisa y por qué los priorizaría sobre el resto del formulario?</td>
    </tr>
</table>

**Knowledge Gap 2**

<table>
    <tr>
        <th>Knowledge Gap</th>
        <td>No se ha determinado si los profesionales clínicos valorarían recibir notificaciones push ante eventos críticos, además de verlos en la lista de alertas.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Qué interés tienen los profesionales clínicos en recibir notificaciones push ante eventos críticos, en qué momentos de su turno las considerarían útiles, con qué frecuencia esperarían recibirlas y por qué canal preferirían que llegaran?</td>
    </tr>
</table>

**Knowledge Gap 3**

<table>
    <tr>
        <th>Knowledge Gap</th>
        <td>Falta información sobre con qué frecuencia los médicos especialistas consultan la evolución de un paciente durante un mismo turno.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Con qué frecuencia consultan los médicos especialistas la evolución de un paciente durante un mismo turno, en qué momentos lo hacen, qué información revisan primero y cuánto tiempo dedican actualmente a esa consulta?</td>
    </tr>
</table>

**Knowledge Gap 4**

<table>
    <tr>
        <th>Knowledge Gap</th>
        <td>No se ha definido con qué frecuencia las instituciones de salud auditarían la trazabilidad de los registros, ni qué nivel de detalle esperan encontrar en ese historial.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Con qué frecuencia auditarían las instituciones de salud la trazabilidad de los registros clínicos, quién realizaría esa revisión, qué nivel de detalle esperarían encontrar y en qué situaciones recurrirían a ese historial?</td>
    </tr>
</table>

**Knowledge Gap 5**

<table>
    <tr>
        <th>Knowledge Gap</th>
        <td>Se desconoce qué proporción de las tareas de registro y consulta ocurre efectivamente cerca del paciente frente a en una estación de trabajo.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Qué proporción de las tareas de registro y consulta realiza el personal de enfermería cerca del paciente en lugar de en una estación de trabajo, en qué momentos del turno ocurre esto y qué las motiva a hacerlo en un lugar u otro?</td>
    </tr>
</table>

**Knowledge Gap 6**

<table>
    <tr>
        <th>Knowledge Gap</th>
        <td>No se ha determinado qué tan dispuestos están los médicos especialistas a adoptar un formulario adicional de registro, aun cuando reduzca el tiempo de búsqueda de información.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Qué tan dispuestos están los médicos especialistas a incorporar un paso adicional de registro en su rutina, qué beneficio mínimo esperarían a cambio y qué objeciones plantearían frente a ese cambio de hábito?</td>
    </tr>
</table>

**Knowledge Gap 7**

<table>
    <tr>
        <th>Knowledge Gap</th>
        <td>Se desconoce qué objeciones concretas plantearían las instituciones de salud sobre seguridad, interoperabilidad o costo antes de evaluar la adopción de NursePulse.</td>
    </tr>
    <tr>
        <th>Pregunta</th>
        <td>¿Qué objeciones concretas sobre seguridad, interoperabilidad o costo plantearían las instituciones de salud antes de evaluar NursePulse, quién dentro de la institución las plantearía y qué información necesitarían para resolverlas?</td>
    </tr>
</table>

### 8.1.4. Question Backlog.

A continuación, se muestra el backlog priorizado de las preguntas generadas en la sección anterior. Las preguntas se priorizan según su confianza, riesgo, impacto e interés, de modo que las más críticas para la propuesta de valor de NursePulse se evalúen primero. El Deep Backlog agrupa las preguntas de prioridad 1 a 6, y el Broad Backlog las de prioridad 7 a 15.

<table>
<tr>
    <th>Prioridad</th>
    <th>Pregunta</th>
    <th>Motivación</th>
    <th>Confianza</th>
    <th>Riesgo</th>
    <th>Impacto</th>
    <th>Interés</th>
    <th>Puntaje total</th>
</tr>

<tr>
    <td>1</td>
    <td>¿El personal de enfermería cardiovascular comunicará información más completa durante un cambio de turno si usa un formulario digital estructurado con SBAR que si usa un mensaje no estructurado? (H-01)</td>
    <td>Valida el diferenciador principal del producto y está directamente ligada a BG-02.</td>
    <td>6</td>
    <td>10</td>
    <td>10</td>
    <td>8</td>
    <td>34</td>
</tr>

<tr>
    <td>2</td>
    <td>¿Qué elementos del traspaso SBAR considera el personal de enfermería realmente indispensables, quién los usa en el turno siguiente, en qué situaciones los omitiría si tuviera prisa y por qué los priorizaría sobre el resto del formulario?</td>
    <td>Permite calibrar el formulario SBAR antes de medir su efectividad frente al mensaje libre.</td>
    <td>5</td>
    <td>9</td>
    <td>9</td>
    <td>9</td>
    <td>32</td>
</tr>

<tr>
    <td>3</td>
    <td>¿Los profesionales clínicos podrán identificar quién realizó una acción, cuándo y sobre qué registro al revisar el historial y la auditoría de NursePulse? (H-04)</td>
    <td>Sostiene la propuesta de trazabilidad, ligada a BG-05.</td>
    <td>6</td>
    <td>9</td>
    <td>8</td>
    <td>8</td>
    <td>31</td>
</tr>

<tr>
    <td>4</td>
    <td>¿Los médicos especialistas cardiovasculares localizarán más rápido la información reciente de un paciente con una vista resumida de evolución que con datos distribuidos en secciones separadas? (H-03)</td>
    <td>Valida la reducción de 30 % en el tiempo de búsqueda clínica definida en BG-03.</td>
    <td>6</td>
    <td>8</td>
    <td>8</td>
    <td>8</td>
    <td>30</td>
</tr>

<tr>
    <td>5</td>
    <td>¿El personal de enfermería completará correctamente el registro de signos vitales en NursePulse, sin omitir campos esenciales, en escenarios simulados de atención? (H-02)</td>
    <td>Confirma la viabilidad del reemplazo del registro físico de signos vitales, ligado a BG-03 y BG-04.</td>
    <td>6</td>
    <td>8</td>
    <td>8</td>
    <td>7</td>
    <td>29</td>
</tr>

<tr>
    <td>6</td>
    <td>¿Con qué frecuencia consultan los médicos especialistas la evolución de un paciente durante un mismo turno, en qué momentos lo hacen, qué información revisan primero y cuánto tiempo dedican actualmente a esa consulta?</td>
    <td>Define la línea base necesaria para medir la reducción de tiempo prometida en H-03.</td>
    <td>5</td>
    <td>8</td>
    <td>8</td>
    <td>7</td>
    <td>28</td>
</tr>

<tr>
    <td>7</td>
    <td>¿Los usuarios clínicos reconocerán más rápido la alerta que requiere atención prioritaria si la lista de alertas tiene jerarquía visual que si se presenta sin priorización? (H-05)</td>
    <td>Valida que la jerarquía visual de alertas aporte valor real en una situación de deterioro clínico.</td>
    <td>6</td>
    <td>7</td>
    <td>7</td>
    <td>7</td>
    <td>27</td>
</tr>

<tr>
    <td>8</td>
    <td>¿Los representantes de instituciones de salud entenderán que NursePulse es una herramienta complementaria, y no un reemplazo de su sistema hospitalario, y mostrarán interés en evaluarla? (H-08)</td>
    <td>Determina si existe adopción institucional viable, condición necesaria para cumplir BG-02.</td>
    <td>5</td>
    <td>7</td>
    <td>7</td>
    <td>7</td>
    <td>26</td>
</tr>

<tr>
    <td>9</td>
    <td>¿Con qué frecuencia auditarían las instituciones de salud la trazabilidad de los registros clínicos, quién realizaría esa revisión, qué nivel de detalle esperarían encontrar y en qué situaciones recurrirían a ese historial?</td>
    <td>Aporta contexto institucional para dimensionar correctamente el módulo de auditoría.</td>
    <td>5</td>
    <td>7</td>
    <td>7</td>
    <td>6</td>
    <td>25</td>
</tr>

<tr>
    <td>10</td>
    <td>¿El personal de enfermería realizará tareas de registro y consulta cerca del paciente con la aplicación móvil al menos igual de bien, y más rápido, que con la aplicación web en una estación de trabajo? (H-06)</td>
    <td>Justifica la inversión en una aplicación móvil nativa frente a mantener solo la versión web.</td>
    <td>6</td>
    <td>6</td>
    <td>6</td>
    <td>6</td>
    <td>24</td>
</tr>

<tr>
    <td>11</td>
    <td>¿Qué proporción de las tareas de registro y consulta realiza el personal de enfermería cerca del paciente en lugar de en una estación de trabajo, en qué momentos del turno ocurre esto y qué las motiva a hacerlo en un lugar u otro?</td>
    <td>Permite entender si el escenario de uso que justifica la app móvil ocurre con la frecuencia esperada.</td>
    <td>5</td>
    <td>6</td>
    <td>6</td>
    <td>6</td>
    <td>23</td>
</tr>

<tr>
    <td>12</td>
    <td>¿Qué tan dispuestos están los médicos especialistas a incorporar un paso adicional de registro en su rutina, qué beneficio mínimo esperarían a cambio y qué objeciones plantearían frente a ese cambio de hábito?</td>
    <td>Identifica posibles barreras de adopción entre el personal médico, no solo de enfermería.</td>
    <td>5</td>
    <td>6</td>
    <td>6</td>
    <td>5</td>
    <td>22</td>
</tr>

<tr>
    <td>13</td>
    <td>¿Los visitantes comprenderán qué problema resuelve NursePulse y encontrarán por su cuenta cómo solicitar información después de explorar la Landing Page? (H-07)</td>
    <td>Valida el primer punto de contacto con visitantes e instituciones, ligado a BG-01.</td>
    <td>6</td>
    <td>5</td>
    <td>5</td>
    <td>5</td>
    <td>21</td>
</tr>

<tr>
    <td>14</td>
    <td>¿Qué interés tienen los profesionales clínicos en recibir notificaciones push ante eventos críticos, en qué momentos de su turno las considerarían útiles, con qué frecuencia esperarían recibirlas y por qué canal preferirían que llegaran?</td>
    <td>Explora una mejora futura sobre el sistema de alertas, no crítica para la primera validación.</td>
    <td>5</td>
    <td>5</td>
    <td>5</td>
    <td>4</td>
    <td>19</td>
</tr>

<tr>
    <td>15</td>
    <td>¿Qué objeciones concretas sobre seguridad, interoperabilidad o costo plantearían las instituciones de salud antes de evaluar NursePulse, quién dentro de la institución las plantearía y qué información necesitarían para resolverlas?</td>
    <td>Es relevante para una futura negociación comercial, pero depende de validar primero el interés institucional (H-08).</td>
    <td>4</td>
    <td>5</td>
    <td>4</td>
    <td>4</td>
    <td>17</td>
</tr>
</table>

### 8.1.5. Experiments Cards.

Las siguientes tarjetas desarrollan las ocho preguntas impulsadas por creencias (H-01 a H-08), ordenadas según su prioridad en el Question Backlog. Las hipótesis, medidas, condiciones y métricas de cada tarjeta son las mismas que se detallan en las secciones 8.2.1 a 8.2.4, de modo que la planificación y el diseño del experimento sean consistentes entre sí.

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿El personal de enfermería cardiovascular comunicará información más completa durante un cambio de turno si usa un formulario digital estructurado con SBAR que si usa un mensaje no estructurado?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Valida el diferenciador principal del producto frente a la comunicación no estructurada actual, condición de BG-02.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Creemos que, al usar el formulario SBAR de NursePulse, el personal de enfermería omitirá menos elementos relevantes del traspaso porque el formulario exige completar situación, antecedentes, evaluación y recomendación, evidenciado por una tasa de omisión al menos 15 puntos porcentuales menor que con un mensaje libre.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Prototipo funcional del formulario SBAR de NursePulse, evaluado con traspasos simulados.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>SBAR Omission Rate (SOR): elementos relevantes omitidos sobre elementos relevantes del escenario.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>A) Traspaso con el formulario SBAR de NursePulse. B) Traspaso con mensaje libre, como se hace hoy.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Razón</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>M-01 Tasa de omisión SBAR.</td>
</tr>
</table>

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿Qué elementos del traspaso SBAR considera el personal de enfermería realmente indispensables, quién los usa en el turno siguiente, en qué situaciones los omitiría si tuviera prisa y por qué los priorizaría sobre el resto del formulario?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Permite calibrar qué campos del formulario SBAR deben mantenerse obligatorios antes de medir su efectividad frente al mensaje libre.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Pregunta exploratoria: no cuenta con una hipótesis formulada en esta etapa, su resultado alimentará el diseño del formulario SBAR evaluado en H-01.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Entrevista semiestructurada con personal de enfermería sobre el contenido del formulario SBAR.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>Elementos señalados como indispensables; elementos señalados como prescindibles bajo presión de tiempo.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>Entrevista individual con un guion de preguntas abiertas sobre cada componente del formulario SBAR.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Nominal</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>No aplica (resultado cualitativo).</td>
</tr>
</table>

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿Los profesionales clínicos podrán identificar quién realizó una acción, cuándo y sobre qué registro al revisar el historial y la auditoría de NursePulse?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Sostiene la propuesta de trazabilidad completa definida en BG-05.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Creemos que al menos el 85 % de las respuestas sobre responsable, fecha, hora y registro involucrado serán correctas porque cada registro muestra esos datos, evidenciado por una tasa de respuestas correctas igual o superior al 85 %.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Cuestionario de escenario sobre el historial y la auditoría de NursePulse.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>Traceability Accuracy Rate (TAR): respuestas correctas sobre respuestas totales.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>A) Revisión del historial y la auditoría de NursePulse (responsable, fecha y hora visibles). B) Revisión de registros sin esos datos.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Razón</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>M-04 Tasa de respuestas correctas de trazabilidad.</td>
</tr>
</table>

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿Los médicos especialistas cardiovasculares localizarán más rápido la información reciente de un paciente con una vista resumida de evolución que con datos distribuidos en secciones separadas?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Valida la reducción de 30 % en el tiempo de búsqueda de información clínica definida en BG-03.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Creemos que el tiempo medio para localizar la información solicitada será al menos 30 % menor con la vista de seguimiento del paciente de NursePulse que con una vista donde los datos están separados, sin aumentar las respuestas incorrectas, evidenciado por una reducción del tiempo medio de localización de 30 % o más.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Prototipo de la vista de seguimiento del paciente, evaluado con tareas de búsqueda cronometradas.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>Clinical Information Retrieval Time (CIRT): reducción porcentual del tiempo de localización frente al control.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>A) Consulta mediante la vista de seguimiento de NursePulse. B) Consulta con los mismos datos distribuidos en secciones separadas.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Razón</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>M-03 Tiempo de localización de información.</td>
</tr>
</table>

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿El personal de enfermería completará correctamente el registro de signos vitales en NursePulse, sin omitir campos esenciales, en escenarios simulados de atención?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Confirma la viabilidad de reemplazar el registro físico de signos vitales, condición de BG-03 y BG-04.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Creemos que al menos el 90 % de los registros de signos vitales se completarán correctamente a la primera, con una omisión de campos esenciales de 5 % o menos, porque el formulario muestra el rango válido de cada medición, evidenciado por una tasa de finalización correcta igual o superior al 90 %.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Prototipo funcional del formulario de signos vitales, evaluado con mediciones de escenarios simulados.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>Vital Signs Completion Rate (VCR): registros correctos a la primera sobre registros intentados.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>A) Registro en el formulario digital de NursePulse. B) Registro en el formato físico o en planilla que se usa actualmente.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Razón</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>M-02 Tasa de finalización correcta de signos vitales.</td>
</tr>
</table>

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿Los usuarios clínicos reconocerán más rápido la alerta que requiere atención prioritaria si la lista de alertas tiene jerarquía visual (severidad, estado y filtros) que si se presenta sin priorización?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Valida que la jerarquía visual de alertas acelere el reconocimiento de eventos que requieren atención inmediata.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Creemos que el tiempo para identificar la alerta de mayor prioridad será al menos 30 % menor con la jerarquía visual de NursePulse, con una identificación correcta de al menos 90 %, evidenciado por la reducción del tiempo de reconocimiento y la tasa de acierto.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Prototipo de la lista de alertas con severidad, estado y filtros visuales.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>Priority Alert Recognition Time (PART): tiempo hasta la primera selección y tasa de acierto.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>A) Lista de alertas con jerarquía visual. B) Lista de alertas plana, sin priorización visual.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Razón</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>M-05 Tiempo y acierto en reconocimiento de alertas.</td>
</tr>
</table>

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿Los representantes de instituciones de salud entenderán que NursePulse es una herramienta complementaria, y no un reemplazo de su sistema hospitalario, y mostrarán interés en evaluarla?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Determina si existe una adopción institucional viable, condición necesaria para cumplir BG-02.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Creemos que al menos el 70 % de los representantes institucionales entrevistados diferenciará correctamente el alcance de NursePulse frente a un HIS o EHR, y que al menos 3 instituciones mostrarán interés en evaluarlo en un escenario definido, evidenciado por ambas condiciones.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Entrevista guiada y escenario de evaluación institucional con representantes de instituciones de salud.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>Scope Differentiation Rate (SDR): representantes que diferencian el alcance sobre entrevistados; número de instituciones interesadas.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>A) Presentación de NursePulse como herramienta complementaria. B) Presentación genérica de una plataforma de gestión clínica.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Razón</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>M-08 Diferenciación de alcance e interés institucional.</td>
</tr>
</table>

<table>
<tr>
    <th>Elemento</th>
    <th>Descripción</th>
</tr>
<tr>
    <td>Pregunta</td>
    <td>¿El personal de enfermería realizará tareas de registro y consulta cerca del paciente con la aplicación móvil al menos igual de bien, y más rápido, que con la aplicación web en una estación de trabajo?</td>
</tr>
<tr>
    <td>Por qué</td>
    <td>Justifica mantener una aplicación móvil nativa, propuesta de valor de BG-04.</td>
</tr>
<tr>
    <td>Hipótesis</td>
    <td>Creemos que la aplicación móvil logrará una tasa de finalización de tareas no inferior a la de la web (margen de 10 puntos porcentuales) y un tiempo al menos 20 % menor, sin más errores, evidenciado por ambas medidas en el mismo conjunto de tareas.</td>
</tr>
<tr>
    <td>Qué</td>
    <td>Prototipo de la aplicación móvil, evaluado con el mismo guion de tareas que la aplicación web.</td>
</tr>
<tr>
    <td>Medidas</td>
    <td>Mobile Task Efficiency (MTE): tasa de finalización y tiempo por tarea en móvil frente a web.</td>
</tr>
<tr>
    <td>Condiciones</td>
    <td>A) Tareas realizadas con la aplicación móvil. B) Mismas tareas realizadas con la aplicación web en una estación de trabajo.</td>
</tr>
<tr>
    <td>Escala</td>
    <td>Razón</td>
</tr>
<tr>
    <td>Métrica</td>
    <td>M-06 Eficiencia de tareas móvil vs. web.</td>
</tr>
</table>


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

La fase de *Experimentation* de NursePulse tiene como finalidad transformar los hallazgos obtenidos durante el análisis del estado actual (*As-Is*), las entrevistas de validación y el diseño experimental en propuestas concretas de mejora del producto digital. Esta etapa permite relacionar las necesidades identificadas en los usuarios con nuevas historias de usuario y un Product Backlog actualizado, orientado a generar evidencia sobre el valor de las funcionalidades propuestas.

El punto de partida de esta fase corresponde a los resultados documentados en los capítulos anteriores. En el Capítulo III se establecieron las historias de usuario y los requisitos funcionales del producto. En el Capítulo V se documentó la implementación de la Landing Page, la aplicación web desarrollada en Angular, la aplicación móvil en Flutter y los servicios RESTful implementados mediante Spring Boot. Posteriormente, el Capítulo VI permitió identificar oportunidades de mejora mediante pruebas y entrevistas de validación, mientras que el Capítulo VII describió las prácticas DevOps utilizadas durante el desarrollo.

A partir de estos antecedentes, la sección 8.1 permitió identificar y priorizar preguntas de investigación. Asimismo, en la sección 8.2 se definieron ocho hipótesis experimentales, sus métricas de dominio, condiciones de evaluación, criterios de escala y mecanismos de recolección de información.

Las principales oportunidades de mejora identificadas son:

- Mejorar la completitud de los traspasos clínicos mediante la estructura SBAR, reduciendo la necesidad de ingresar repetidamente información existente.
- Facilitar el registro de signos vitales y proporcionar retroalimentación clara sobre el resultado del guardado.
- Optimizar la consulta de información clínica mediante vistas resumidas y tendencias temporales.
- Fortalecer la trazabilidad y confiabilidad de los registros mediante una identificación verificable del usuario responsable.
- Mejorar la priorización, visualización y gestión segura de alertas clínicas.
- Incrementar la eficiencia de las actividades realizadas desde la aplicación móvil.
- Mejorar la comprensión de la propuesta de valor y los mecanismos de contacto de la Landing Page.
- Facilitar la comprensión del modelo SaaS y su carácter complementario frente a los sistemas hospitalarios existentes.

Para estructurar las mejoras propuestas se consideran las ocho hipótesis del diseño experimental y sus métricas de dominio:

| Hipótesis | Área de evaluación | Métrica |
|---|---|---|
| H-01 | Traspaso de turno mediante SBAR | M-01: SBAR Omission Rate (SOR) |
| H-02 | Registro de signos vitales | M-02: Vital Signs Completion Rate (VCR) |
| H-03 | Consulta de evolución clínica | M-03: Clinical Information Retrieval Time (CIRT) |
| H-04 | Trazabilidad clínica | M-04: Traceability Accuracy Rate (TAR) |
| H-05 | Priorización de alertas | M-05: Priority Alert Recognition Time (PART) |
| H-06 | Eficiencia de la aplicación móvil | M-06: Mobile Task Efficiency (MTE) |
| H-07 | Comprensión de la Landing Page | M-07: Value Proposition Comprehension Rate (VPCR) |
| H-08 | Adopción institucional | M-08: Scope Differentiation Rate (SDR) |

La propuesta To-Be conserva el alcance general de NursePulse como plataforma de apoyo a los procesos de enfermería en clínicas privadas. La validación inicial se concentra en escenarios de hospitalización general, manteniendo a los profesionales de enfermería y coordinadores como usuarios principales, así como a los médicos y administradores autorizados como actores complementarios.

Las pruebas se diseñan utilizando datos clínicos sintéticos y escenarios controlados, sin involucrar información identificable de pacientes reales. De esta manera, se busca obtener evidencia útil respetando las responsabilidades éticas y profesionales del equipo.

La presente sección desarrolla las historias de usuario To-Be y su correspondiente Product Backlog. Las funcionalidades aquí descritas constituyen propuestas de mejora sujetas a implementación y validación experimental. Su inclusión no implica que se encuentren desarrolladas ni que las hipótesis hayan sido confirmadas.

---

### 8.3.1. To-Be User Stories

Las *To-Be User Stories* representan las funcionalidades y mejoras propuestas para la siguiente evolución de NursePulse, tomando como referencia los resultados del proceso de *Needfinding*, los hallazgos de las entrevistas de validación, la evaluación heurística y las hipótesis definidas en el apartado 8.2.

A diferencia de las historias originales, cuyo objetivo fue construir la primera versión funcional de la plataforma, las historias To-Be buscan mejorar los procesos existentes y atender problemas específicos identificados durante su evaluación.

Para conservar la trazabilidad con el Product Backlog original, las nuevas historias se identifican mediante el prefijo `TB-US`, seguido de un número correlativo. Los criterios de aceptación se redactan utilizando la estructura Gherkin *Given–When–Then*, expresada mediante **Dado, Cuando y Entonces**.

#### TB-US-01: Autocompletar antecedentes clínicos en el traspaso SBAR

| Campo | Descripción |
|---|---|
| Story ID | TB-US-01 |
| Epic | EP-02: Gestión de traspaso clínico SBAR |
| Prioridad | Alta |
| Hipótesis relacionada | H-01 |
| Métrica | M-01: SBAR Omission Rate |
| Historias originales | US-13, US-14, US-15 |

**User Story**

Como profesional de enfermería, deseo que el formulario de traspaso SBAR complete automáticamente los antecedentes clínicos disponibles del paciente para evitar registrar información repetida y facilitar una comunicación más completa durante el cambio de turno.

**Justificación**

Durante las entrevistas de validación y la evaluación heurística se identificó que la necesidad de ingresar nuevamente antecedentes clínicos puede aumentar el tiempo de documentación y provocar omisiones. Esta mejora aprovecha información previamente registrada en NursePulse, manteniendo la posibilidad de actualizar los datos relevantes para el turno.

**Criterios de aceptación**

**Escenario 1: Recuperación de antecedentes clínicos**

```gherkin
Dado que el paciente cuenta con información clínica registrada
Cuando el profesional de enfermería inicia un nuevo traspaso SBAR
Entonces el sistema presenta los antecedentes disponibles en el apartado correspondiente
```

**Escenario 2: Información clínica no disponible**

```gherkin
Dado que el paciente no cuenta con antecedentes previamente registrados
Cuando el usuario accede al formulario SBAR
Entonces el sistema permite completar manualmente la información faltante sin generar datos inexistentes
```

**Escenario 3: Actualización de la información**

```gherkin
Dado que los antecedentes han sido recuperados
Cuando el usuario modifica información para el traspaso actual
Entonces el sistema registra los datos del nuevo traspaso sin modificar automáticamente el historial clínico original
```

**Resultado esperado:** disminuir los elementos relevantes omitidos durante el traspaso y reducir la duplicidad de ingreso de información.

#### TB-US-02: Verificación de completitud del formulario SBAR

| Campo | Descripción |
|---|---|
| Story ID | TB-US-02 |
| Epic | EP-02: Gestión de traspaso clínico SBAR |
| Prioridad | Alta |
| Hipótesis relacionada | H-01 |
| Métrica | M-01: SBAR Omission Rate |
| Historias originales | US-13, US-15 |

**User Story**

Como profesional de enfermería, deseo visualizar el estado de completitud de los componentes del formulario SBAR para identificar información faltante antes de finalizar el traspaso de turno.

**Justificación**

El modelo SBAR constituye uno de los principales diferenciadores de NursePulse. La identificación de campos incompletos permite apoyar su uso estructurado y reducir la posibilidad de omitir información relevante durante una transferencia de responsabilidad asistencial.

**Criterios de aceptación**

**Escenario 1: Identificación de información faltante**

```gherkin
Dado que el usuario está completando un formulario SBAR
Cuando uno o más campos obligatorios permanecen incompletos
Entonces el sistema identifica visualmente los campos pendientes
```

**Escenario 2: Finalización del traspaso**

```gherkin
Dado que todos los campos obligatorios contienen información válida
Cuando el usuario confirma el traspaso
Entonces el sistema permite guardar el registro y muestra una confirmación de éxito
```

**Resultado esperado:** reducir al menos 15 puntos porcentuales la tasa de omisión frente a la condición de comunicación no estructurada, conforme al umbral propuesto en la sección 8.2.

#### TB-US-03: Registro de signos vitales con observaciones clínicas

| Campo | Descripción |
|---|---|
| Story ID | TB-US-03 |
| Epic | EP-03: Registro y seguimiento clínico |
| Prioridad | Alta |
| Hipótesis relacionada | H-02 |
| Métrica | M-02: Vital Signs Completion Rate |
| Historias originales | US-16, US-17 |

**User Story**

Como profesional de enfermería, deseo agregar observaciones clínicas al registrar los signos vitales de un paciente para complementar las mediciones con información contextual relevante para el seguimiento asistencial.

**Justificación**

Las entrevistas de validación identificaron la necesidad de agregar comentarios a los registros de signos vitales. El registro numérico permite documentar parámetros fisiológicos, pero no siempre refleja circunstancias relevantes para su interpretación, como las condiciones en las que se realizó una medición.

**Criterios de aceptación**

**Escenario 1: Registro con observaciones**

```gherkin
Dado que el usuario se encuentra en el formulario de signos vitales
Cuando ingresa mediciones válidas y una observación complementaria
Entonces el sistema guarda los valores y la observación asociados al paciente correspondiente
```

**Escenario 2: Registro sin observaciones**

```gherkin
Dado que el campo de observaciones es opcional
Cuando el usuario ingresa correctamente los signos vitales sin comentarios
Entonces el sistema permite guardar el registro
```

**Escenario 3: Validación de mediciones**

```gherkin
Dado que existe un valor fuera de los límites permitidos por el formulario
Cuando el usuario intenta guardar el registro
Entonces el sistema muestra el campo que requiere revisión sin descartar los demás datos ingresados
```

**Resultado esperado:** alcanzar una tasa de registros correctos a la primera de al menos 90 %, manteniendo una omisión de campos esenciales no superior al 5 %.

#### TB-US-04: Visualización del estado de guardado en la aplicación móvil

| Campo | Descripción |
|---|---|
| Story ID | TB-US-04 |
| Epic | EP-11: Plataforma web y móvil |
| Prioridad | Alta |
| Hipótesis relacionada | H-02, H-06 |
| Métricas | M-02: VCR; M-06: MTE |
| Historias originales | US-16, US-38 |

**User Story**

Como profesional de enfermería, deseo recibir una confirmación visual del estado de guardado de los registros realizados desde la aplicación móvil para saber si la información se almacenó correctamente y evitar registros duplicados.

**Justificación**

La evaluación de usabilidad identificó la ausencia de retroalimentación clara durante el registro móvil. Esta situación puede producir incertidumbre cuando el usuario presiona el botón de guardar, especialmente bajo condiciones de conectividad limitada.

**Criterios de aceptación**

**Escenario 1: Guardado exitoso**

```gherkin
Dado que el usuario ha completado correctamente un formulario
Cuando el servidor confirma la operación
Entonces la aplicación muestra un mensaje de guardado exitoso
```

**Escenario 2: Operación en proceso**

```gherkin
Dado que una solicitud de guardado se encuentra en ejecución
Cuando el usuario observa la pantalla
Entonces la aplicación presenta un indicador de procesamiento y evita envíos duplicados
```

**Escenario 3: Error de conexión**

```gherkin
Dado que el servidor no confirma el guardado
Cuando ocurre un error de conexión
Entonces el sistema informa que la operación no fue confirmada y permite recuperarla de manera controlada
```

**Resultado esperado:** mejorar la tasa de finalización de tareas móviles y reducir errores asociados a la incertidumbre del guardado.

Esta historia no presupone la existencia de un modo offline completo, cuya implementación requeriría un alcance técnico adicional.

#### TB-US-05: Visualización integrada de evolución clínica

| Campo | Descripción |
|---|---|
| Story ID | TB-US-05 |
| Epic | EP-05: Soporte a la toma de decisiones clínicas |
| Prioridad | Alta |
| Hipótesis relacionada | H-03 |
| Métrica | M-03: Clinical Information Retrieval Time |
| Historias originales | US-17, US-21, US-29 |

**User Story**

Como profesional clínico autorizado, deseo visualizar en una misma pantalla los signos vitales recientes, los eventos clínicos y las alertas del paciente para consultar su evolución sin navegar entre diferentes módulos.

**Justificación**

El análisis de entrevistas identificó que la fragmentación de información incrementa el esfuerzo necesario para consultar el estado reciente de los pacientes. Asimismo, en la evaluación heurística se señaló la ausencia de curvas de tendencia temporal de parámetros hemodinámicos.

**Criterios de aceptación**

**Escenario 1: Consulta de información consolidada**

```gherkin
Dado que el paciente cuenta con registros clínicos
Cuando el usuario autorizado accede a su vista de seguimiento
Entonces el sistema presenta los signos vitales, eventos y alertas disponibles en una vista integrada
```

**Escenario 2: Visualización de tendencias**

```gherkin
Dado que el paciente cuenta con múltiples mediciones registradas
Cuando el usuario selecciona un parámetro fisiológico
Entonces el sistema presenta su evolución temporal mediante una representación gráfica
```

**Escenario 3: Ausencia de registros**

```gherkin
Dado que no existen datos para el periodo seleccionado
Cuando el usuario consulta la evolución
Entonces el sistema informa que no hay registros disponibles, sin generar valores estimados
```

**Resultado esperado:** reducir al menos un 30 % el tiempo de localización de información clínica respecto a la condición de control, sin incrementar las respuestas incorrectas.

#### TB-US-06: Filtrado y priorización de alertas clínicas

| Campo | Descripción |
|---|---|
| Story ID | TB-US-06 |
| Epic | EP-09: Alertas clínicas |
| Prioridad | Alta |
| Hipótesis relacionada | H-05 |
| Métrica | M-05: Priority Alert Recognition Time |
| Historias originales | US-31, US-32, US-33 |

**User Story**

Como profesional de enfermería, deseo visualizar las alertas clínicas ordenadas y filtradas por severidad y estado para identificar rápidamente aquellas que requieren atención prioritaria.

**Justificación**

La evaluación heurística identificó sobrecarga visual y ausencia de filtros inmediatos en la consola de alertas. Esta situación puede dificultar el reconocimiento de eventos relevantes dentro de una lista extensa.

**Criterios de aceptación**

**Escenario 1: Priorización de alertas**

```gherkin
Dado que existen alertas de diferentes niveles de severidad
Cuando el usuario abre el listado
Entonces el sistema permite identificar visualmente las alertas de mayor prioridad
```

**Escenario 2: Aplicación de filtros**

```gherkin
Dado que existen alertas con diferentes estados
Cuando el usuario selecciona un filtro
Entonces el sistema presenta únicamente las alertas que cumplen las condiciones seleccionadas
```

**Escenario 3: Consulta del detalle**

```gherkin
Dado que el usuario identifica una alerta
Cuando selecciona el registro
Entonces el sistema presenta la información correspondiente y su estado actual
```

**Resultado esperado:** reducir al menos 30 % el tiempo de identificación de la alerta prioritaria y alcanzar una tasa de acierto mínima de 90 %.

#### TB-US-07: Confirmación del cierre de alertas críticas

| Campo | Descripción |
|---|---|
| Story ID | TB-US-07 |
| Epic | EP-09: Alertas clínicas |
| Prioridad | Alta |
| Hipótesis relacionada | H-05 |
| Métrica relacionada | M-05; evaluación complementaria de errores |
| Historias originales | US-31, US-32 |

**User Story**

Como profesional clínico autorizado, deseo confirmar y justificar el cierre de una alerta crítica para evitar cierres accidentales y mantener evidencia de las decisiones tomadas durante su atención.

**Justificación**

La evaluación heurística identificó como problema la posibilidad de cerrar alertas clínicas críticas sin una confirmación ni justificación obligatoria. Esta mejora responde a la necesidad de prevenir errores en operaciones que pueden afectar el seguimiento de eventos relevantes.

**Criterios de aceptación**

**Escenario 1: Solicitud de cierre**

```gherkin
Dado que una alerta crítica se encuentra en un estado que permite su cierre
Cuando el usuario selecciona la opción correspondiente
Entonces el sistema solicita confirmación y una justificación
```

**Escenario 2: Cancelación**

```gherkin
Dado que el diálogo de confirmación se encuentra abierto
Cuando el usuario cancela la operación
Entonces la alerta conserva su estado anterior
```

**Escenario 3: Cierre confirmado**

```gherkin
Dado que el usuario autorizado confirma la operación e ingresa una justificación válida
Cuando el sistema procesa el cierre
Entonces actualiza el estado de la alerta y registra el responsable, fecha, hora y motivo de la acción
```

**Resultado esperado:** reducir cierres involuntarios y fortalecer la seguridad de las operaciones clínicas y su trazabilidad.

#### TB-US-08: Fortalecimiento de la trazabilidad de acciones clínicas

| Campo | Descripción |
|---|---|
| Story ID | TB-US-08 |
| Epic | EP-04: Trazabilidad clínica |
| Prioridad | Alta |
| Hipótesis relacionada | H-04 |
| Métrica | M-04: Traceability Accuracy Rate |
| Historias originales | US-20, US-35, US-36 |

**User Story**

Como jefe o coordinador de enfermería, deseo consultar un historial confiable de las acciones realizadas por el personal autorizado para identificar al responsable de cada registro y reconstruir lo ocurrido durante un turno.

**Justificación**

El Product Backlog original reconoce que algunas operaciones registran el identificador del responsable proporcionado por la aplicación cliente sin contrastarlo con el token de autenticación. Este comportamiento representa una oportunidad de mejora en la confiabilidad de la auditoría.

**Criterios de aceptación**

**Escenario 1: Registro del responsable**

```gherkin
Dado que un usuario autenticado realiza una acción clínica
Cuando el servidor procesa la operación
Entonces registra como responsable al usuario identificado mediante la sesión autenticada, sin confiar exclusivamente en un identificador enviado por el cliente
```

**Escenario 2: Consulta de auditoría**

```gherkin
Dado que un supervisor autorizado accede al historial
Cuando consulta una acción registrada
Entonces visualiza el responsable, la fecha, la hora, el tipo de operación y la entidad relacionada
```

**Escenario 3: Acceso no autorizado**

```gherkin
Dado que un usuario carece de permisos para consultar determinados registros
Cuando intenta acceder a ellos
Entonces el sistema rechaza la solicitud conforme a las reglas de autorización
```

**Resultado esperado:** alcanzar al menos un 85 % de respuestas correctas en los escenarios de reconstrucción de acciones clínicas.

#### TB-US-09: Dashboard de seguimiento de actividades y pendientes

| Campo | Descripción |
|---|---|
| Story ID | TB-US-09 |
| Epic | EP-08: Pacientes y monitoreo |
| Prioridad | Media |
| Hipótesis relacionada | H-03, H-05 |
| Métricas | M-03: CIRT; M-05: PART |
| Historias originales | US-29, US-30 |

**User Story**

Como jefe o coordinador de enfermería, deseo consultar un dashboard con información resumida de pacientes, alertas y actividades pendientes para supervisar el estado general del turno sin revisar cada módulo individualmente.

**Justificación**

El primer capítulo del informe identifica a los coordinadores de enfermería como un segmento objetivo que necesita visibilidad sobre responsables, pendientes y eventos relevantes. Esta historia complementa las funcionalidades existentes del dashboard y la propuesta de centralización de información.

**Criterios de aceptación**

**Escenario 1: Visualización del dashboard**

```gherkin
Dado que el usuario autorizado inicia sesión
Cuando accede al dashboard
Entonces visualiza los indicadores y registros disponibles correspondientes a su ámbito de autorización
```

**Escenario 2: Identificación de pendientes**

```gherkin
Dado que existen actividades o alertas pendientes registradas en el sistema
Cuando el usuario consulta el resumen
Entonces puede identificar los elementos que requieren seguimiento
```

**Escenario 3: Acceso al detalle**

```gherkin
Dado que el usuario selecciona un elemento del dashboard
Cuando solicita información adicional
Entonces el sistema muestra el registro asociado, respetando los permisos existentes
```

**Resultado esperado:** reducir el tiempo requerido para identificar información relevante y facilitar el seguimiento de las actividades documentadas.

#### TB-US-10: Registro de eventos de interacción para experimentación

| Campo | Descripción |
|---|---|
| Story ID | TB-US-10 |
| Epic | EP-11: Plataforma web y móvil |
| Prioridad | Alta |
| Hipótesis relacionada | H-01 a H-07 |
| Métricas | M-01 a M-07 |
| Historias originales | TS-08, TS-09, US-38 |

**User Story**

Como integrante del equipo de investigación de NursePulse, deseo disponer de registros de interacción de las tareas experimentales para calcular las métricas definidas y analizar el comportamiento de los participantes durante las pruebas.

**Justificación**

La sección 8.2.8 establece un plan de seguimiento de eventos para la aplicación web y móvil, pero reconoce que todavía no existe una herramienta de analítica de producto implementada. Por ello, esta historia permite preparar la infraestructura necesaria para ejecutar las pruebas y obtener datos cuantitativos.

**Criterios de aceptación**

**Escenario 1: Registro de eventos**

```gherkin
Dado que un participante realiza una tarea experimental
Cuando ocurre una interacción definida en el Tracking Plan
Entonces el sistema registra el evento y sus propiedades necesarias para calcular la métrica correspondiente
```

**Escenario 2: Diferenciación de plataforma**

```gherkin
Dado que el evento ocurre desde la aplicación web o móvil
Cuando se almacena el registro
Entonces se identifica el canal mediante la propiedad channel
```

**Escenario 3: Protección de datos**

```gherkin
Dado que se registra una interacción experimental
Cuando se recopila la información
Entonces se evita almacenar nombres, documentos u otros identificadores personales de pacientes
```

**Resultado esperado:** disponer de datos consistentes que permitan calcular las métricas experimentales y comparar las condiciones definidas en la sección 8.2.

#### TB-US-11: Mejorar la comprensión y conversión de la Landing Page

| Campo | Descripción |
|---|---|
| Story ID | TB-US-11 |
| Epic | EP-01: Landing Page informativa |
| Prioridad | Media |
| Hipótesis relacionada | H-07 |
| Métrica | M-07: Value Proposition Comprehension Rate |
| Historias originales | US-01, US-02, US-05, US-10 |

**User Story**

Como visitante de la Landing Page, deseo comprender rápidamente el propósito de NursePulse y localizar la opción para solicitar una demostración para evaluar si la plataforma responde a las necesidades de mi institución.

**Justificación**

Las entrevistas identificaron una percepción favorable sobre la claridad visual de la Landing Page, pero también oportunidades para simplificar algunos términos técnicos y mejorar la navegación.

**Criterios de aceptación**

**Escenario 1: Comprensión de la propuesta de valor**

```gherkin
Dado que el visitante accede a la página principal
Cuando revisa la información presentada
Entonces encuentra una explicación del propósito de NursePulse, sus funcionalidades principales y su alcance complementario
```

**Escenario 2: Solicitud de información**

```gherkin
Dado que el visitante desea conocer más sobre el producto
Cuando busca la opción de contacto o demostración
Entonces puede identificar y acceder al llamado a la acción correspondiente
```

**Escenario 3: Registro de interacción**

```gherkin
Dado que el visitante selecciona el llamado a la acción
Cuando ocurre la interacción
Entonces se registra el evento landing_cta_clicked, conforme al Tracking Plan
```

**Resultado esperado:** alcanzar al menos 70 % de comprensión correcta y 80 % de localización del llamado a la acción sin asistencia.

#### TB-US-12: Comprensión de los planes y el alcance institucional

| Campo | Descripción |
|---|---|
| Story ID | TB-US-12 |
| Epic | EP-11: Plataforma y suscripciones |
| Prioridad | Media |
| Hipótesis relacionada | H-08 |
| Métrica | M-08: Scope Differentiation Rate |
| Historias originales | US-39, US-10 |

**User Story**

Como representante de una clínica privada, deseo comparar los planes y funcionalidades de NursePulse y conocer sus limitaciones frente a un HIS o EHR para evaluar una posible adopción institucional de acuerdo con las necesidades de mi organización.

**Justificación**

El modelo comercial documentado contempla los planes Essential, Professional y Enterprise. Sin embargo, las conclusiones del proyecto identifican la necesidad de obtener validación directa de representantes institucionales respecto a los precios, características y condiciones de adopción.

**Criterios de aceptación**

**Escenario 1: Comparación de planes**

```gherkin
Dado que un representante institucional accede a la información comercial
Cuando consulta los planes disponibles
Entonces el sistema presenta los límites de usuarios y las funcionalidades correspondientes a cada plan
```

**Escenario 2: Comprensión del alcance**

```gherkin
Dado que el representante revisa la propuesta de valor
Cuando consulta el funcionamiento de NursePulse
Entonces encuentra una explicación de que la solución complementa los sistemas hospitalarios existentes y no pretende sustituir un HIS o EHR completo
```

**Escenario 3: Solicitud de información institucional**

```gherkin
Dado que el representante desea evaluar la plataforma
Cuando selecciona la opción de contacto
Entonces puede acceder al canal disponible para solicitar información o una demostración
```

**Resultado esperado:** lograr que al menos 70 % de los representantes entrevistados diferencie correctamente el alcance de NursePulse y que al menos tres instituciones manifiesten interés en evaluarlo.

Esta historia no contempla implementar una pasarela de pagos, ya que dicha funcionalidad no forma parte de las capacidades verificadas en el producto actual.

#### Relación entre las To-Be User Stories y los hallazgos de validación

| Hallazgo identificado | Historia To-Be |
|---|---|
| Redigitación de antecedentes en SBAR | TB-US-01 |
| Posibles omisiones en traspasos | TB-US-02 |
| Ausencia de observaciones en signos vitales | TB-US-03 |
| Falta de confirmación visual en móvil | TB-US-04 |
| Ausencia de tendencias temporales | TB-US-05 |
| Sobrecarga visual de alertas | TB-US-06 |
| Cierre de alertas sin confirmación | TB-US-07 |
| Limitaciones de trazabilidad | TB-US-08 |
| Necesidad de supervisar pendientes | TB-US-09 |
| Ausencia de instrumentación experimental | TB-US-10 |
| Oportunidades de mejora en Landing Page | TB-US-11 |
| Validación institucional pendiente | TB-US-12 |

Las historias propuestas deben considerarse candidatas para su incorporación al siguiente ciclo de desarrollo. Su aprobación definitiva dependerá de los resultados experimentales y de las prioridades establecidas por el equipo.

---

### 8.3.2. To-Be Product Backlog

El *To-Be Product Backlog* de NursePulse organiza y prioriza las historias de usuario derivadas de las oportunidades identificadas durante la validación del producto y del diseño experimental.

Su propósito es establecer una secuencia de implementación que permita abordar primero los riesgos relacionados con la continuidad de atención, integridad de los registros, trazabilidad y disponibilidad de datos experimentales. Posteriormente se consideran mejoras de experiencia de usuario, visualización de información y comunicación de valor institucional.

La priorización toma como referencia los criterios empleados en el Question Backlog de la sección 8.1.4:

- **Confianza:** nivel de evidencia disponible sobre el problema.
- **Riesgo:** consecuencias de mantener el problema sin resolver.
- **Impacto:** beneficio esperado para los usuarios y los objetivos del negocio.
- **Interés:** relevancia de la pregunta para los usuarios y stakeholders del proyecto.

Asimismo, se consideran las dependencias técnicas entre historias, el alcance del producto y la necesidad de recopilar evidencia antes de tomar decisiones de implementación adicionales.

#### Criterios de estimación y priorización

Para la estimación del esfuerzo se emplea la escala de Story Points utilizada en el Product Backlog original del Capítulo III: **1, 2, 3, 5 y 8**.

Los Story Points representan estimaciones relativas de complejidad, esfuerzo e incertidumbre técnica. No equivalen directamente a horas de desarrollo.

Las estimaciones siguientes constituyen una propuesta inicial y deberán ser confirmadas por el equipo durante la planificación del Sprint.

Se establecen dos niveles de prioridad:

- **Alta:** historias relacionadas con problemas de seguridad, calidad de los registros, trazabilidad, eficiencia del traspaso e instrumentación necesaria para ejecutar los experimentos.
- **Media:** mejoras que complementan la experiencia de usuario, permiten ampliar el seguimiento operativo o facilitan la comunicación institucional.

#### Product Backlog To-Be — NursePulse

| Orden | Story ID | Título | Prioridad | Story Points | Hipótesis |
|---:|---|---|---|---:|---|
| 1 | TB-US-10 | Registro de eventos para experimentación | Alta | 5 | H-01 a H-07 |
| 2 | TB-US-08 | Fortalecimiento de la trazabilidad | Alta | 8 | H-04 |
| 3 | TB-US-01 | Autocompletar antecedentes SBAR | Alta | 5 | H-01 |
| 4 | TB-US-02 | Verificación de completitud SBAR | Alta | 3 | H-01 |
| 5 | TB-US-07 | Confirmación del cierre de alertas críticas | Alta | 5 | H-05 |
| 6 | TB-US-03 | Registro de signos vitales con observaciones | Alta | 5 | H-02 |
| 7 | TB-US-04 | Estado de guardado en la aplicación móvil | Alta | 8 | H-02, H-06 |
| 8 | TB-US-06 | Filtrado y priorización de alertas | Alta | 5 | H-05 |
| 9 | TB-US-05 | Visualización integrada de evolución clínica | Alta | 8 | H-03 |
| 10 | TB-US-09 | Dashboard de actividades y pendientes | Media | 5 | H-03, H-05 |
| 11 | TB-US-11 | Comprensión y conversión de Landing Page | Media | 3 | H-07 |
| 12 | TB-US-12 | Comprensión de planes y alcance institucional | Media | 5 | H-08 |
| | | **Total estimado** | | **65 SP** | |

#### Distribución del Product Backlog por bloques funcionales

| Bloque funcional | Historias relacionadas | Propósito |
|---|---|---|
| Experimentación y analítica | TB-US-10 | Incorporar los mecanismos necesarios para medir los resultados de las pruebas |
| Traspasos SBAR | TB-US-01, TB-US-02 | Mejorar la completitud y reducir la duplicidad de información |
| Registro de signos vitales | TB-US-03, TB-US-04 | Facilitar el registro y mejorar la retroalimentación al usuario |
| Consulta y seguimiento | TB-US-05, TB-US-09 | Centralizar información y mejorar la identificación de elementos relevantes |
| Alertas clínicas | TB-US-06, TB-US-07 | Facilitar la priorización y prevenir errores de cierre |
| Auditoría y trazabilidad | TB-US-08 | Fortalecer la confiabilidad de los registros |
| Landing Page | TB-US-11 | Facilitar la comprensión y el contacto institucional |
| Suscripciones y adopción | TB-US-12 | Mejorar la comprensión de los planes y el alcance del producto |

#### Dependencias técnicas del To-Be Product Backlog

La ejecución de las historias funcionales debe acompañarse de determinadas actividades técnicas para asegurar que los cambios sean comprobables y que los experimentos generen datos utilizables.

| Actividad técnica | Relación | Descripción |
|---|---|---|
| Instrumentación del Tracking Plan | TB-US-10 | Implementar los eventos definidos en 8.2.8, incluyendo `sbar_submitted`, `vital_signs_submitted`, `info_found`, `alert_first_opened` y `task_completed` |
| Validación de identidad del responsable | TB-US-08 | Verificar la identidad mediante el contexto de autenticación del backend, sin depender de identificadores proporcionados por el cliente |
| Validación de entidades relacionadas | TB-US-01, TB-US-03, TB-US-08 | Comprobar la existencia y autorización de acceso al paciente antes de registrar operaciones asociadas |
| Prevención de duplicados | TB-US-04 | Gestionar correctamente los intentos de guardado y sus respuestas |
| Adaptación de interfaces | TB-US-05, TB-US-06, TB-US-09 | Implementar componentes de visualización utilizando información realmente disponible en los módulos existentes |
| Ejecución de pruebas automatizadas | Todas | Incorporar o actualizar pruebas unitarias, de integración y de comportamiento para verificar los criterios de aceptación |

Estas actividades se vinculan con las Technical Stories originales TS-01 a TS-10, especialmente aquellas relacionadas con autenticación, manejo de errores, trazabilidad, CI/CD y observabilidad.

#### Relación con las métricas y experimentos

| Historias To-Be | Métrica principal | Criterio experimental |
|---|---|---|
| TB-US-01, TB-US-02 | M-01 | Reducción de omisiones SBAR de al menos 15 puntos porcentuales |
| TB-US-03 | M-02 | Al menos 90 % de registros correctos |
| TB-US-04 | M-06 | Al menos 20 % menos tiempo sin disminuir la finalización más de 10 puntos porcentuales |
| TB-US-05, TB-US-09 | M-03 | Al menos 30 % menos tiempo de consulta clínica |
| TB-US-06 | M-05 | Al menos 30 % menos tiempo y 90 % de reconocimiento correcto |
| TB-US-07 | M-05 y observación de errores | Confirmación segura de acciones críticas y ausencia de cierres accidentales en escenarios evaluados |
| TB-US-08 | M-04 | Al menos 85 % de respuestas correctas sobre trazabilidad |
| TB-US-10 | M-01 a M-07 | Disponibilidad y consistencia de eventos necesarios para el análisis |
| TB-US-11 | M-07 | 70 % de comprensión y 80 % de localización del CTA |
| TB-US-12 | M-08 | 70 % de diferenciación del alcance y al menos tres instituciones interesadas |

#### Relación del To-Be Product Backlog con los Business Goals

El backlog propuesto conserva su relación con los Business Goals documentados en el Capítulo III, considerando las áreas de mejora definidas en las hipótesis de la sección 8.2.

| Business Goal | Historias To-Be relacionadas | Contribución esperada |
|---|---|---|
| BG-01: Captación de interesados | TB-US-11, TB-US-12 | Facilitar la comprensión de la propuesta de valor y el acceso a solicitudes de información |
| BG-02: Validación de traspasos SBAR | TB-US-01, TB-US-02 | Mejorar la completitud de la información y facilitar la evaluación institucional del proceso |
| BG-03: Reducción del tiempo de consulta | TB-US-05, TB-US-09 | Facilitar el acceso a información consolidada y reducir la navegación entre módulos |
| BG-04: Adopción de registros digitales | TB-US-03, TB-US-04 | Mejorar la eficiencia y confiabilidad percibida del registro clínico |
| BG-05: Trazabilidad de acciones | TB-US-07, TB-US-08 | Fortalecer el registro de responsables, fechas, horas y operaciones realizadas |

#### Propuesta de organización por Sprints

La siguiente distribución constituye una propuesta de planificación inicial. Su ejecución deberá ajustarse de acuerdo con la capacidad del equipo, las dependencias técnicas y la evidencia obtenida durante las sesiones experimentales.

**Sprint To-Be 1: Instrumentación y confiabilidad**

Historias:

- TB-US-10: Registro de eventos para experimentación.
- TB-US-08: Fortalecimiento de la trazabilidad.
- TB-US-07: Confirmación del cierre de alertas críticas.

**Objetivo:** preparar la recolección de datos experimentales y mejorar la confiabilidad de los registros y las operaciones críticas.

**Sprint To-Be 2: Optimización de los registros clínicos**

Historias:

- TB-US-01: Autocompletar antecedentes SBAR.
- TB-US-02: Verificación de completitud SBAR.
- TB-US-03: Registro de signos vitales con observaciones.
- TB-US-04: Estado de guardado en la aplicación móvil.

**Objetivo:** mejorar las funcionalidades de registro y comunicación utilizadas frecuentemente por el personal de enfermería.

**Sprint To-Be 3: Seguimiento, alertas y experiencia institucional**

Historias:

- TB-US-05: Visualización integrada de evolución clínica.
- TB-US-06: Filtrado y priorización de alertas.
- TB-US-09: Dashboard de actividades y pendientes.
- TB-US-11: Comprensión y conversión de Landing Page.
- TB-US-12: Comprensión de planes y alcance institucional.

**Objetivo:** facilitar la consulta de información relevante, la supervisión de procesos y la comunicación del valor de NursePulse.

#### Criterios para considerar completada una historia To-Be

Una historia solo podrá considerarse terminada cuando:

1. Cumpla los criterios de aceptación especificados en la sección 8.3.1.
2. Su implementación haya sido integrada en el repositorio correspondiente.
3. Las pruebas automatizadas aplicables se ejecuten satisfactoriamente.
4. Se verifique su comportamiento mediante escenarios funcionales.
5. Se compruebe que las restricciones de acceso y seguridad se mantienen.
6. Se documenten las evidencias de implementación y pruebas.
7. Los eventos necesarios para medir su impacto estén disponibles cuando correspondan.

Además, la finalización técnica de una historia no implica que la hipótesis experimental haya sido confirmada. La decisión sobre el valor de la funcionalidad deberá basarse en los datos recolectados y analizados durante la experimentación.

#### Conclusión del To-Be Product Backlog

El To-Be Product Backlog de NursePulse establece una propuesta de evolución del producto basada en los problemas identificados durante su validación y en los riesgos priorizados mediante el diseño experimental.

La planificación evita incorporar funcionalidades sin relación con los objetivos del producto y concentra los esfuerzos en mejorar la completitud del traspaso SBAR, la calidad de los registros clínicos, la trazabilidad, el reconocimiento de alertas y la eficiencia de consulta.

Asimismo, incorpora como requisito transversal la disponibilidad de datos experimentales, indispensables para comprobar las hipótesis formuladas y sustentar decisiones posteriores.

La implementación de estas historias permitirá preparar una nueva versión de NursePulse para su evaluación. Los resultados de las pruebas deberán utilizarse posteriormente para actualizar el Question Backlog y determinar qué mejoras mantener, modificar o descartar.
