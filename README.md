## Capítulo IV: Product Design
### 4.1. Style Guidelines
#### 4.1.1. General Style Guidelines

El diseño de estilo general de **NursePulse** responde a la necesidad de transmitir profesionalismo, seguridad, claridad y confianza, valores fundamentales en una solución digital orientada al sector salud. La propuesta visual busca reflejar una identidad moderna y ordenada, alineada con el propósito del producto: mejorar la comunicación clínica, la trazabilidad de la información y el seguimiento de pacientes cardiovasculares dentro de entornos asistenciales.

- **Colores**: la paleta seleccionada combina azul oscuro (#0F172A), teal oscuro (#0F766E), turquesa (#14B8A6), blanco (#FFFFFF) y tonos grises suaves (#E5E7EB y #1F2937). El azul transmite confianza, estabilidad y profesionalismo, cualidades importantes en plataformas relacionadas con procesos clínicos. El turquesa refuerza la idea de innovación, accesibilidad y tecnología en salud. Los tonos neutros equilibran la interfaz, mejoran el contraste y favorecen la lectura del contenido.

![colores.png](assets/chapter-4/colores.png)


- **Tipografía**: se utiliza una tipografía sans serif como base visual por su claridad, legibilidad y apariencia profesional en entornos web. La elección de fuentes como Arial y Helvetica responde a la necesidad de mantener una lectura fluida en títulos, botones, menús y descripciones, además de proyectar una imagen moderna, limpia y confiable para el usuario.

- ![TIPOGRAFIA.png](assets/chapter-4/TIPOGRAFIA.png)


- **Distribución y espaciado**: se adopta una estructura visual ordenada, con bloques bien definidos, espaciado consistente y una jerarquía clara entre secciones. La landing page organiza su contenido de manera progresiva, permitiendo que el usuario identifique fácilmente el propósito del producto, sus características, beneficios y medios de contacto. Esta distribución mejora la navegación y facilita una experiencia visual limpia y comprensible.

![distribucion.png](assets/chapter-4/distribucion.png)


- **Lenguaje y tono**: la comunicación es directa, clara y profesional, evitando tecnicismos innecesarios. Los textos de la interfaz emplean un tono formal y accesible para transmitir confianza y facilitar la comprensión de la propuesta de valor tanto a instituciones de salud como a usuarios interesados en la solución. Expresiones como “Solicitar demo”, “Ver cómo funciona” y “¡Hablemos!” refuerzan un lenguaje orientado a la acción y a la claridad informativa.

![lenguaje.png](assets/chapter-4/lenguaje.png)

- **Iconografía**: se emplean símbolos visuales vinculados al entorno médico y a la comunicación asistencial, como íconos relacionados con salud, registro clínico, monitoreo y comunicación entre usuarios. Esto permite reforzar visualmente el enfoque del producto, reducir la complejidad de interpretación y mejorar la usabilidad general de la landing page.

![iconografia.png](assets/chapter-4/iconografia.png)

#### 4.1.2. Web Style Guidelines

El diseño web de **NursePulse** se implementa como una solución digital orientada al sector salud, buscando que tanto la Landing Page como la Web Application mantengan una experiencia uniforme, clara, responsiva y accesible. El objetivo es asegurar una interfaz confiable y profesional que facilite la interacción de visitantes, personal de enfermería cardiovascular, médicos especialistas y clientes institucionales.

- **Diseño adaptable**: la interfaz se ajusta a distintos dispositivos (desktop, tablet y móvil), manteniendo consistencia visual entre la Landing Page y la Web Application. Esto permite que los usuarios puedan acceder al sistema desde diferentes contextos, facilitando la consulta de información y el uso de la plataforma en distintos entornos de trabajo.

![diseño.png](assets/chapter-4/dise%C3%B1o.png)

- **Componentes de interfaz**: los botones principales se presentan con colores más intensos para resaltar acciones relevantes como solicitar una demo, registrar información o confirmar procesos, mientras que los elementos secundarios mantienen un estilo más neutral. Esto establece jerarquía visual y permite que el usuario identifique con rapidez las acciones prioritarias dentro de la interfaz.

![componentes.png](assets/chapter-4/componentes.png)

- **Notificaciones y estados**: los mensajes del sistema utilizan convenciones visuales claras para comunicar el estado de una acción o proceso. Los estados positivos se muestran en verde para indicar confirmación o guardado exitoso, las advertencias en amarillo para señalar elementos pendientes o en revisión, y los errores en rojo para representar fallos o problemas de sincronización. Esta diferenciación mejora la comprensión y reduce la posibilidad de confusión por parte del usuario.

![notificaciones.png](assets/chapter-4/notificaciones.png)

- **Tablas y dashboards**: se prioriza una presentación clara y ordenada de la información dentro de tablas y paneles de control, facilitando la consulta y el análisis de datos relevantes. La organización visual de registros, métricas y estados permite que el usuario interprete rápidamente la información y pueda dar seguimiento a los procesos del sistema de manera más eficiente.

![tablas.png](assets/chapter-4/tablas.png)

- **Accesibilidad**: se consideran contrastes adecuados, una disposición clara del contenido y elementos visuales comprensibles para favorecer la interacción de distintos tipos de usuarios. Además, se busca mantener una navegación sencilla y una lectura legible en toda la interfaz, fortaleciendo la usabilidad general de la plataforma.

![accesibilidad.png](assets/chapter-4/accesibilidad.png)

### 4.1.3. Mobile Style Guidelines

#### 4.1.3.1 IOS Mobile Style Guidelines

#### 4.1.3.2 Android Mobile Style Guidelines


### 4.2. Information Architecture
#### 4.2.1. Organization Systems

1. Organization Scheme (Esquema de organización)
- Temático/Funcional: la información se organiza según las funciones principales del sistema:
    - Gestión de usuarios (registro, login, perfil, documentos).
    - Gestión clínica (pacientes, tratamientos, signos vitales, historial clínico).
    - Traspasos y comunicación asistencial (SBAR, seguimiento entre turnos y áreas).
    - Landing Page (información y promoción del producto).
    - Reportes y analítica.

2. Organization Structure (Estructura de organización)

- Jerárquica (Árbol): desde la Landing Page como entrada, se navega a los módulos principales del sistema.
- Lineal: en procesos como registro de cuenta, ingreso de pacientes o traspaso SBAR, los pasos siguen una secuencia.
- Matriz: en búsquedas y filtrados, por ejemplo en pacientes o reportes, donde la información puede organizarse por fecha, estado clínico, área asistencial o tipo de registro.

3. Organization System (Sistema de organización aplicado)
- Global navigation (menú principal en el header): acceso a
    - Home (Landing Page)
    - Pacientes
    - Traspasos SBAR
    - Tratamientos
    - Reportes
    - Contacto

- Local navigation (submenús dentro de cada sección):
    - Pacientes → Registrar, Historial, Signos vitales.
    - Traspasos SBAR → Pendientes, En revisión, Aprobados.
    - Tratamientos → Activos, Seguimiento, Finalizados.
    - Reportes → Pacientes, Tratamientos, Eventos críticos.

- Contextual navigation (botones de acción dentro de un flujo):
    - “Registrar paciente”
    - “Guardar SBAR”
    - “Actualizar signos vitales”
    - “Generar reporte”



![organization-diagram.png](assets/chapter-4/organization-diagram.png)


### 4.2.2. Labeling Systems

**Objetivos**

- Facilitar la identificación rápida de módulos, secciones y funciones dentro de la Landing Page y la Web Application.
- Mantener consistencia en los nombres utilizados en navegación, formularios, tablas y reportes.
- Mejorar la comprensión del sistema por parte de los usuarios, empleando etiquetas claras, breves y fáciles de reconocer.
- Favorecer una navegación intuitiva y una mejor organización del contenido, tanto en la parte informativa como en la operativa.

**Estructura recomendada**

- Estructura: **Módulo principal → Submódulo → Acción o estado**.
  - Ejemplo: **Inventario > Registrar ítem > Guardar**
  - Ejemplo: **Inspecciones > Pendientes > Revisar**
  - Ejemplo: **Perfil > Documentos > Cargar archivo**

- Tipos de etiquetas:
  - **Módulos**: nombres principales de navegación, como `Inicio`, `Inventario`, `Inspecciones`, `Perfil`, `Reportes`, `Contacto`.
  - **Submódulos**: categorías internas dentro de cada sección, como `Stock actual`, `Historial`, `Pendientes`, `Aprobados`, `Documentos`.
  - **Acciones**: etiquetas orientadas a tareas, como `Registrar`, `Editar`, `Guardar`, `Enviar`, `Generar reporte`.
  - **Estados**: etiquetas para representar la situación de un elemento, como `Pendiente`, `En revisión`, `Aprobado`, `Rechazado`, `Activo`.

**Convenciones (formato)**

- Uso de palabras claras y comprensibles para el usuario final.
- Etiquetas breves, directas y consistentes en toda la interfaz.
- En navegación y botones se priorizan etiquetas de **1 a 3 palabras**.
- Para URLs y slugs se utiliza formato en minúsculas y con guiones.
  - Ejemplo: `inventario/stock-actual`
  - Ejemplo: `inspecciones/en-revision`
- En la interfaz visible se emplean nombres legibles y amigables.
  - Ejemplo: `Stock actual`
  - Ejemplo: `Generar reporte`

**Modelo de datos (ejemplo JSON)**

```json
{
  "id": "lbl_001",
  "type": "module",
  "slug": "inventario",
  "name": "Inventario",
  "parent_id": null,
  "created_at": "2026-04-21T10:00:00Z"
}

```

#### Interfaz de gestión
- Gestión centralizada de etiquetas para mantener uniformidad entre la Landing Page y la Web Application.
- Posibilidad de reutilizar etiquetas en menús, tablas, formularios y botones.
- Edición sencilla de nombres visibles sin afectar la lógica interna del sistema.
- Vista previa del uso de cada etiqueta dentro de menús, breadcrumbs o secciones.

#### Reglas y validaciones
- No se permiten etiquetas duplicadas dentro de un mismo contexto.
- Cada etiqueta debe tener un nombre visible y un identificador interno único.
- Se valida que las etiquetas sean consistentes con la jerarquía del sistema.
- Se recomienda reutilizar etiquetas existentes antes de crear nuevas.
- Los nombres deben evitar tecnicismos innecesarios o abreviaturas confusas.

#### Ejemplos de uso en URLs
- `/inventario/stock-actual`
- `/inventario/historial`
- `/inspecciones/aprobados`

#### 4.2.3. SEO Tags and Meta Tags

**Objetivos**

- Mejorar la visibilidad de la **Landing Page** de **PulseReport** en motores de búsqueda.
- Aumentar el CTR en resultados de búsqueda mediante títulos y descripciones claras y atractivas.
- Optimizar la vista previa al compartir enlaces en redes sociales usando **Open Graph** y **Twitter Cards**.
- Controlar qué páginas deben indexarse y cuáles no, diferenciando entre la **Landing Page pública** y la **Web Application privada**.
- Incorporar datos estructurados para describir el producto digital y la organización.

**Meta tags clave (plantilla)**

```html
<title>{{page_title}} | Care-Labs</title>
<meta name="description" content="{{page_description}}" />
<link rel="canonical" href="{{canonical_url}}" />
<meta name="robots" content="{{robots_value}}" />

<!-- Open Graph -->
<meta property="og:title" content="{{page_title}} | Care-Labs" />
<meta property="og:description" content="{{page_description}}" />
<meta property="og:image" content="{{og_image}}" />
<meta property="og:url" content="{{canonical_url}}" />
<meta property="og:type" content="website" />
<meta property="og:site_name" content="Care-Labs" />

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="{{page_title}} | Care-Labs" />
<meta name="twitter:description" content="{{page_description}}" />
<meta name="twitter:image" content="{{twitter_image}}" />
```
**Reglas prácticas**

- **Título**: entre 50 y 60 caracteres, incluyendo el nombre del producto o de la empresa.
- **Meta description**: entre 120 y 160 caracteres, explicando de forma clara la propuesta de valor.
- **Canonical**: obligatorio en páginas públicas para evitar contenido duplicado.
- **Meta robots**:
  - `index, follow` para la **Landing Page** y secciones públicas.
  - `noindex, nofollow` para páginas privadas del sistema como dashboard, perfil o reportes internos.
- Las palabras clave deben enfocarse en términos como:
  - comunicación clínica,
  - trazabilidad en tiempo real,
  - continuidad asistencial,
  - software de gestión clínica,
  - plataforma de salud digital.

**JSON-LD (ejemplo para el producto digital)**

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "PulseReport",
  "applicationCategory": "HealthApplication",
  "operatingSystem": "Web",
  "description": "Plataforma web de Pulse-Report orientada a mejorar la comunicación clínica, la trazabilidad y el seguimiento en tiempo real.",
  "publisher": {
    "@type": "Organization",
    "name": "Care-Labs"
  },
  "url": "https://care-labs.com/pulsereport"
}
</script>
```
**Renderizado (server vs client)**

- Para la **Landing Page**, es recomendable utilizar **prerendering** o **SSR**, de modo que los meta tags estén disponibles desde la carga inicial y sean interpretados correctamente por los motores de búsqueda.
- En el caso de Angular, esto puede implementarse mediante opciones de **Angular SSR** o **prerender** para mejorar el posicionamiento SEO.
- Para la **Web Application interna**, el SEO no es prioritario, ya que su contenido es funcional y de acceso restringido.

**Sitemaps y robots.txt**

- `sitemap.xml`: incluir únicamente las rutas públicas relevantes, como:
  - Inicio
  - Características
  - Beneficios
  - Preguntas frecuentes
  - Contacto
- `robots.txt`: permitir el rastreo de la Landing Page y bloquear secciones privadas o internas del sistema.
- Ejemplo:
  - permitir indexación de `/`
  - bloquear rutas como `/dashboard`, `/perfil`, `/reportes-internos` o cualquier módulo autenticado.

#### 4.2.4. Searching Systems.

**Requerimientos funcionales**

- Búsqueda por texto en módulos clave como pacientes, tratamientos, traspasos SBAR y reportes.
- Autocomplete / sugerencias para acelerar la localización de pacientes, registros o áreas asistenciales.
- Filtros por estado, fecha, área, tipo de registro o nivel de prioridad.
- Búsqueda por historial clínico o eventos asociados al paciente.
- Ordenamiento de resultados por fecha, estado, prioridad o coincidencia.
- Visualización clara de resultados para facilitar la identificación rápida de la información.
- Posibilidad de combinar búsqueda + filtros en tablas y paneles del sistema.

**Opciones de tecnología (comparativa rápida)**

- **PostgreSQL Full-Text Search**
  - Pros: integrado, práctico y suficiente para búsquedas básicas dentro del sistema.
  - Contras: menor flexibilidad para búsquedas avanzadas o ranking complejo.

- **Elasticsearch / OpenSearch**
  - Pros: alto rendimiento, búsquedas avanzadas, filtros potentes y mejor relevancia.
  - Contras: requiere infraestructura adicional y mayor mantenimiento.

- **Algolia (SaaS)**
  - Pros: búsqueda muy rápida, autocomplete eficiente y buena experiencia de usuario.
  - Contras: dependencia de un servicio externo y costo adicional.

**Esquema de índice (ejemplo para Elastic)**

```json
{
  "mappings": {
    "properties": {
      "id": { "type": "keyword" },
      "patient_name": { "type": "text", "analyzer": "standard" },
      "clinical_area": { "type": "keyword" },
      "sbar_status": { "type": "keyword" },
      "treatment_status": { "type": "keyword" },
      "record_type": { "type": "keyword" },
      "created_at": { "type": "date" },
      "priority": { "type": "keyword" }
    }
  }
}
```

#### 4.2.5. Navigation Systems.

A continuación, se presenta el sistema de navegación de **PulseReport**, el cual permite al usuario desplazarse tanto en la **Landing Page** como en la **Web Application** de manera clara, ordenada y consistente.

La navegación fue definida considerando los principales perfiles del producto: visitantes interesados en conocer la solución, personal de enfermería cardiovascular, médicos especialistas cardiovasculares y usuarios administradores de la plataforma. Esto permite diferenciar la navegación informativa de la Landing Page y la navegación operativa de la Web Application.

Se implementará un sistema de navegación que facilite el acceso rápido a las principales secciones del producto, manteniendo consistencia visual y funcional en toda la experiencia web. Esto permitirá que los usuarios identifiquen fácilmente dónde se encuentran y hacia dónde pueden dirigirse dentro de la plataforma.

**Estructura del Sistema de Navegación**

- **Navegación global**: ubicada en el header principal, permite acceder a las secciones principales de la Landing Page, como inicio, beneficios, características, planes, preguntas frecuentes, equipo y contacto. En la Web Application, permite acceder a módulos como dashboard, pacientes, signos vitales, traspasos SBAR, eventos clínicos, reportes, auditoría y suscripciones.

- **Navegación local**: presente dentro de cada módulo de la Web Application, facilita el acceso a subsecciones específicas. Por ejemplo:
  - Pacientes → listado, detalle del paciente, registros clínicos y signos vitales.
  - Traspasos SBAR → creación de traspaso, consulta de traspasos y confirmación de recepción.
  - Signos vitales → registro, historial y último registro del paciente.
  - Suscripciones → visualización de planes, selección de plan y estado de suscripción.

- **Navegación contextual**: integrada mediante botones y acciones dentro de cada flujo, permitiendo ejecutar tareas específicas como:
  - “Registrar paciente”
  - “Registrar signos vitales”
  - “Guardar SBAR”
  - “Ver historial”
  - “Seleccionar plan”
  - “Generar reporte”

- **Consistencia de navegación**: los menús, accesos y botones mantienen una ubicación y estilo uniforme, ayudando a que el usuario navegue de manera intuitiva y sin confusión entre las distintas secciones.


![navigation-system-structure.png](assets/chapter-4/navigation-system-structure.png)


### 4.3. Landing Page UI Design.
La Landing Page de NursePulse fue diseñada como el principal punto de entrada público al producto. Su objetivo es comunicar rápidamente la propuesta de valor, explicar el problema de información clínica dispersa, presentar beneficios, características, planes, preguntas frecuentes, equipo y canales de contacto.

El diseño considera distintos perfiles de visitantes. Para usuarios recurrentes, se priorizan llamados a la acción visibles en la parte superior. Para visitantes emocionales, se utiliza una sección hero clara con mensaje directo sobre continuidad clínica y reducción de pérdida de información. Para visitantes racionales, se incluyen secciones de características, beneficios, planes, preguntas frecuentes y testimonios que permiten evaluar el valor de la solución.

#### 4.3.1. Landing Page Wireframe.

El wireframe de la landing page de **NursePulse** presenta una estructura clara y ordenada, diseñada para comunicar la propuesta de valor del producto de forma directa. La página incluye secciones estratégicas como hero section, funcionamiento, características, beneficios, preguntas frecuentes, contacto y llamados a la acción que orientan al usuario durante la navegación.

- **Inicio**: en la parte superior se ubica el logo principal de **NursePulse** junto con la barra de navegación, que permite acceder a las principales secciones de la landing page. Además, se incluye un botón de **“Solicitar demo”** como llamado a la acción destacado, con el objetivo de captar rápidamente el interés del usuario.


![hero-wf.png](assets/chapter-4/hero-wf.png)

- **¿Cómo funciona?**: en esta sección se explica de forma breve y visual cómo funciona la solución, mostrando el flujo general del producto en pasos simples. Esto permite que el usuario comprenda rápidamente la lógica de uso de **NursePulse** dentro del entorno clínico.

![hdiw-wf.png](assets/chapter-4/hdiw-wf.png)

- **Características**: se presentan las funcionalidades principales de la plataforma, como traspasos SBAR, gestión de pacientes, seguimiento de tratamientos, monitoreo de signos vitales, historial clínico digital y log de auditoría. Estas características se muestran en bloques simples con descripciones breves para facilitar la comprensión del producto.

![features-wf.png](assets/chapter-4/features-wf.png)

- **Beneficios y FAQs**: esta sección destaca el valor agregado de la solución, resaltando beneficios como una mejor comunicación entre turnos, mayor trazabilidad clínica, organización de la información y atención más confiable. Además, se incluye una sección de preguntas frecuentes para resolver dudas comunes y reforzar la claridad de la propuesta.


![benefits-wf.png](assets/chapter-4/benefits-wf.png)

![faqs-wf.png](assets/chapter-4/faqs-wf.png)



- **Contacto y Footer**: en la parte final se encuentra el formulario de contacto, que permite a los usuarios interesados enviar consultas o solicitar información adicional sobre la plataforma. Finalmente, el footer incluye información general de la marca y accesos complementarios a secciones relevantes de la landing page.

![contact-wf.png](assets/chapter-4/contact-wf.png)

![footer-wf.png](assets/chapter-4/footer-wf.png)

#### 4.3.2. Landing Page Mock-up

![hero-mu.png](assets/chapter-4/hero-mu.png)

![hdiw-mu.png](assets/chapter-4/hdiw-mu.png)

![features-mu.png](assets/chapter-4/features-mu.png)

![benefits-mu.png](assets/chapter-4/benefits-mu.png)

![faqs-mu.png](assets/chapter-4/faqs-mu.png)

![contact-mu.png](assets/chapter-4/contact-mu.png)

![footer-mu.png](assets/chapter-4/footer-mu.png)


### 4.4. Mobile Application UX/UI Design


#### 4.4.1. Mobile Applications Wireframes

#### 4.4.2. Mobile Applications Wireflow Diagrams

#### 4.4.3. Mobile Applications Mock-ups

#### 4.4.4. Mobile Applications User Flow Diagrams  

### 4.5. Mobile Applications Prototyping

#### 4.5.1. Android Mobile Applications Prototyping

#### 4.5.2. iOS Mobile Applications Prototyping



### 4.6. Web Applications UX/UI Design


#### 4.6.1. Web Applications Wireframes

![dashboardCarelabs-wf.png](assets/chapter-4/dashboardCarelabs-wf.png)

![monitereoCarelabs-wf.png](assets/chapter-4/monitereoCarelabs-wf.png)

![traspasoSBAR-wf.png](assets/chapter-4/traspasoSBAR-wf.png)

![registro-wf.png](assets/chapter-4/registro-wf.png)

![W-Subscription Management.png](assets/chapter-4/W-Subscription%20Management.png)

![W-Subscription Management-1.png](assets/chapter-4/W-Subscription%20Management-1.png)

![W-Subscription Management-2.png](assets/chapter-4/W-Subscription%20Management-2.png)


#### 4.6.2. Web Applications Wireflow Diagrams

#### User Goal 1

Segmento: Personal de enfermería cardiovascular
User Goal: Registrar signos vitales y evaluar la evolución clínica del paciente.
Explicación: El usuario ingresa al perfil del paciente y selecciona registrar signos vitales. En la ruta esperada (happy path), ingresa los valores, el sistema los valida, guarda el registro y actualiza la gráfica en tiempo real. Como flujos alternativos (unhappy paths), si el usuario ingresa valores incompletos o fuera de los rangos biológicos lógicos, el sistema detiene el flujo y muestra advertencias de validación para evitar errores médicos.

![flow01-wf.png](assets/chapter-4/flow01-wf.png)

#### User Goal 2
Segmento: Personal de enfermería cardiovascular
User Goal: Realizar el traspaso de información clínica entre turnos utilizando el modelo SBAR.
Explicación: El enfermero inicia un nuevo reporte SBAR. El flujo principal lo guía obligatoriamente por las 4 secciones (Situación, Antecedentes, Evaluación, Recomendación) hasta su publicación exitosa. En rutas alternativas, si el usuario intenta cancelar el proceso o cerrar la ventana, el sistema interrumpe la acción con un modal de confirmación para evitar la pérdida de documentación crítica.

![flow02-wf.png](assets/chapter-4/flow02-wf.png)

![flow03-wf.png](assets/chapter-4/flow03-wf.png)

#### User Goal 3
Segmento: Hospitales, clínicas privadas y centros especializados en cardiología
User Goal: Monitorear procesos críticos y revisar la trazabilidad del área cardiovascular.
Explicación: El supervisor ingresa al Dashboard para revisar el estado general. El flujo ideal permite hacer clic en una métrica o alerta activa para ser redirigido al log de auditoría detallado del paciente involucrado. En un flujo alternativo, si el supervisor aplica filtros de búsqueda para fechas sin actividad registrada, el sistema le indica claramente que no existen eventos, permitiéndole reajustar su búsqueda rápidamente.

![flow04-wf.png](assets/chapter-4/flow04-wf.png)

![flow05-wf.png](assets/chapter-4/flow05-wf.png)


#### 4.6.3. Web Applications Mock-ups 

#### Perfil

Esta interfaz está dedicada a la gestión de la información personal y profesional del usuario, ya sea personal de enfermería o administrador. Permite la configuración de la cuenta, visualización de roles y administración de credenciales de acceso.

![perfil.png](assets/chapter-4/perfil.png)

#### Detalle Clínico

Vista especializada que expone la información médica detallada de un paciente específico. Centraliza diagnósticos cardiovasculares, tratamientos activos, medicación y notas clínicas relevantes para asegurar la continuidad del cuidado.

![detalle-clinico.png](assets/chapter-4/detalle-clinico.png)

#### Alertas

Panel de notificaciones y advertencias críticas del sistema. Está diseñado para informar al personal de salud de manera inmediata sobre anomalías en los parámetros de los pacientes, garantizando un tiempo de respuesta rápido ante emergencias.

![alertas.png](assets/chapter-4/alertas.png)

#### Eventos Clínicos

Interfaz orientada al registro y visualización de sucesos médicos importantes ocurridos durante el turno. Facilita la trazabilidad de las intervenciones y apoya directamente la comunicación estructurada mediante el modelo SBAR.

![eventos-clinicos.png](assets/chapter-4/eventos-clinicos.png)


#### Signos Vitales

Módulo enfocado en el monitoreo y registro de los parámetros fisiológicos del paciente. Permite un seguimiento preciso de métricas clave en cardiología, como la presión arterial y la frecuencia cardíaca, mostrando su evolución temporal.

![signos-vitales.png](assets/chapter-4/signos-vitales.png)

#### Paciente
Sección general para la administración de los datos demográficos, información de contacto y estado de admisión de los pacientes dentro del centro de salud, sirviendo como punto de partida para acceder a su historial completo.

![paciente.png](assets/chapter-4/paciente.png)


#### Dashboard
Panel de control principal que ofrece una visión panorámica y resumida del entorno clínico. Muestra indicadores clave de rendimiento, el estado general del área cardiovascular y un resumen de las tareas y pacientes de mayor prioridad.

![dashboard.png](assets/chapter-4/dashboard.png)


#### 4.6.4. Web Applications User Flow Diagrams

En esta sección se presentan los diagramas de flujo de usuario que detallan la lógica de navegación y los puntos de decisión dentro de Care-Labs. Estos flujos han sido diseñados para garantizar que el personal de enfermería y los administradores cumplan sus objetivos de manera eficiente, integrando rutas principales y alternativas para el manejo de datos críticos.  Los diagramas reflejan la interacción completa del sistema, asegurando la consistencia con los wireflows previos y validando cada paso del proceso clínico, desde el registro de signos vitales hasta la supervisión de alertas en el dashboard.  

![user-flow.png](assets/chapter-4/user-flow.png)


### 4.7. Web Applications Prototyping.

En esta sección se presentan los prototipos de interfaz web de Care-Labs, desarrollados para simular los principales flujos de interacción de la plataforma en navegador web. Los prototipos fueron diseñados considerando una arquitectura de información organizada por perfiles de usuario: personal de enfermería cardiovascular y administración o supervisión clínica.

Las decisiones de interacción se enfocan en facilitar una navegación rápida, segura y orientada a procesos críticos, dada la alta exigencia del entorno médico. Para el personal de enfermería, se prioriza la búsqueda ágil de pacientes, el acceso directo al historial clínico, el registro eficiente de signos vitales y la documentación estructurada de eventos y traspasos mediante el modelo SBAR. Para la administración y supervisores, se presenta un dashboard centralizado que permite monitorear el estado general del área cardiovascular, visualizar alertas críticas y acceder al log de auditoría para asegurar la trazabilidad.

Los prototipos incluyen interacciones como botones de acción rápida, formularios clínicos especializados, tarjetas de pacientes seleccionables, filtros de búsqueda, indicadores de estado visuales, notificaciones de alertas en tiempo real y transiciones fluidas entre pantallas. Estas decisiones están estrictamente alineadas con los User Flow Diagrams y con las User Stories definidas para Care-Labs.


### 4.8. Domain-Driven Software Architecture

El Design-Level Event Storming constituye una técnica colaborativa proveniente del marco Lean UX y Domain-Driven Design (DDD) que permite modelar el comportamiento interno de un sistema a nivel de diseño de software. A diferencia del Big Picture Event Storming —orientado a explorar el dominio de negocio de forma amplia—, el nivel de diseño desciende a la granularidad de los comandos, políticas, modelos de lectura y bounded contexts que estructuran la solución técnica.

En el contexto del sistema pulsereport para la UCI Cardiovascular, este ejercicio permitió identificar los flujos de eventos más críticos del proceso de atención, mapear los actores involucrados en cada contexto delimitado y detectar los puntos de fricción que generan riesgos clínicos o ineficiencias operativas.


#### Objetivo del Design-Level Event Storming

El propósito de esta sesión fue descomponer el flujo clínico de la UCI Cardiovascular en eventos de dominio concretos, identificar los bounded contexts que agrupan responsabilidades cohesivas, y derivar los comandos e invariantes que debe respetar el diseño del sistema pulsereport.


#### Paso 1: Recolección de Domain Events

El primer paso consistió en identificar todos los eventos de dominio relevantes del proceso clínico, es decir, hechos concretos que ocurren en el sistema y que son significativos para el negocio. Siguiendo la convención de Event Storming, cada evento se expresa en pasado y se representa con una tarjeta de color naranja.

Los domain events identificados para el sistema pulsereport en la UCI Cardiovascular fueron:

- Información clínica entregada al nuevo turno
- Turno anterior finalizado
- Pacientes asignados revisados
- Estado inicial del paciente verificado
- Signos vitales registrados
- Signos vitales monitoreados
- Medicamento administrado
- Indicación médica revisada
- Evolución reciente del paciente revisada
- Evolución posterior monitoreada
- Evento clínico relevante detectado
- Cambio crítico identificado
- Médico informado sobre cambio clínico
- Cumplimiento de indicación registrado
- Medicación e indicaciones validadas
- Información clínica consultada por el médico
- Nueva indicación médica registrada
- Indicación ejecutada por enfermería

Estos eventos representan el ciclo completo de atención en la UCI, desde el cambio de turno hasta la ejecución de nuevas indicaciones médicas, pasando por el monitoreo continuo del paciente y la detección de eventos críticos.



#### Paso 2: Identificación de Bounded Contexts

Una vez identificados los eventos, el segundo paso consistió en agruparlos en bounded contexts: subdominios con una lógica cohesiva y una responsabilidad bien delimitada. La definición de estos contextos se basa en el análisis de los requerimientos del proyecto Care-Labs, las recomendaciones del enunciado para plataformas SaaS y los principios de Domain-Driven Design.

##### BC-01: Identity and Access Management (IAM) Context — Subdominio Genérico

Subdominio genérico responsable de garantizar que solo el personal autorizado pueda acceder a la información sensible de los pacientes en la UCI Cardiovascular.

- **Domain Events clave:** Usuario autenticado, Rol asignado (RBAC), Sesión iniciada, Permiso denegado
- **Responsabilidades:** Autenticación de usuarios, gestión de roles basada en atributos (RBAC) y control de sesiones activas
- **Alineación arquitectónica:** Actúa como proveedor de identidad para todos los demás bounded contexts del sistema



##### BC-02: Patient Administration Context — Profiles and Preferences Management

Centraliza la información base de los pacientes, alineado con el subdominio de Profiles and Preferences Management. Actúa como el directorio maestro de identidad clínica dentro del sistema.

- **Domain Events clave:** Paciente admitido, Datos demográficos registrados, Estado de admisión actualizado, Paciente dado de alta
- **Responsabilidades:** Registro de datos demográficos, gestión del estado de admisión y mantenimiento del directorio general de pacientes
- **Alineación arquitectónica:** Proporciona el contexto de identidad del paciente al Clinical Monitoring y Clinical Documentation contexts



##### BC-03: Clinical Monitoring Context — CORE DOMAIN

Este es el corazón de pulsereport y donde reside la mayor ventaja competitiva del sistema. Se alinea con el subdominio Service Execution and Monitoring. Concentra la lógica clínica crítica de monitoreo en tiempo real.

- **Domain Events clave:** Signos vitales registrados, Alerta crítica generada, Tratamiento actualizado, Medicamento administrado, Cumplimiento de indicación registrado
- **Responsabilidades:** Registro y monitoreo de signos vitales (presión arterial, frecuencia cardíaca), seguimiento de tratamientos y gestión de alertas críticas en tiempo real
- **Pain Point identificado:** Registro tardío de eventos críticos y duplicidad entre papel y sistema EHR
- **Solución pulsereport:** Dashboard de monitoreo en tiempo real con alertas automáticas y flujo de registro simplificado



##### BC-04: Clinical Documentation Context — Trazabilidad Clínica

Específico para la trazabilidad y comunicación clínica entre turnos. Garantiza que todo evento clínico relevante quede registrado de forma inmutable y auditable.

- **Domain Events clave:** Entrega SBAR registrada, Turno finalizado, Log de auditoría creado, Cambio crítico documentado
- **Responsabilidades:** Implementación del modelo SBAR para el traspaso de turnos y mantenimiento del log de auditoría inalterable
- **Pain Point identificado:** Comunicación verbal no trazable durante cambios de turno y pérdida de información clínica
- **Solución pulsereport:** Protocolo SBAR estandarizado con resumen estructurado y registro inmutable de cada entrega de turno


##### BC-05: Appointments & Scheduling Context — Service Design and Planning

Alineado con el subdominio de Service Design and Planning. Gestiona la programación y coordinación de citas médicas para los pacientes del área cardiovascular.

- **Domain Events clave:** Cita programada, Cita cancelada, Agenda actualizada, Recordatorio enviado
- **Responsabilidades:** Gestión y programación de citas médicas para los pacientes del área cardiovascular
- **Alineación con el flujo clínico:** Conecta con Patient Administration para verificar disponibilidad y con Clinical Monitoring para priorizar citas según estado clínico


#### BC-06: Health Analytics & Dashboard Context — Dashboard and Analytics

Alineado con el subdominio de Dashboard and Analytics. Proporciona inteligencia clínica operacional a supervisores y jefaturas, consolidando datos de todos los contextos para la toma de decisiones estratégicas.

- **Domain Events clave:** Métrica generada, Tendencia de salud calculada, Panel de control actualizado, Reporte exportado
- **Responsabilidades:** Generación de métricas de rendimiento, visualización de tendencias de salud y paneles de control para supervisores y jefaturas clínicas
- **Fuentes de datos:** Consume eventos del Clinical Monitoring, Clinical Documentation, Patient Administration y Appointments contexts


### Tabla Resumen de Bounded Contexts

| Bounded Context | Tipo | Actor Principal | Domain Events Clave | Dominio |
|---|---|---|---|---|
| IAM Context | Genérico | Enfermeros / Administradores | Usuario autenticado, Rol asignado, Sesión iniciada | Seguridad y acceso |
| Patient Administration | Soporte | Personal administrativo / Enfermeros | Paciente admitido, Datos demográficos registrados, Estado actualizado | Gestión de pacientes |
| Clinical Monitoring | **Core Domain** | Enfermero cardiovascular / Médico | Signos vitales registrados, Alerta crítica generada, Tratamiento actualizado | Monitoreo en tiempo real |
| Clinical Documentation | Soporte | Enfermera saliente / entrante | Entrega SBAR registrada, Log de auditoría creado, Turno finalizado | Trazabilidad clínica |
| Appointments & Scheduling | Soporte | Médico / Coordinador | Cita programada, Cita cancelada, Agenda actualizada | Gestión de citas |
| Health Analytics & Dashboard | Soporte | Supervisor / Jefatura clínica | Métrica generada, Tendencia calculada, Panel actualizado | Analítica y reportes |


#### Paso 3: Identificación de Comandos y Políticas

El tercer paso consistió en derivar los comandos que desencadenan los eventos y las políticas que conectan eventos con acciones subsecuentes. Los comandos representan la intención del usuario o del sistema de ejecutar una acción, mientras que las políticas definen las reglas automáticas del negocio que se activan ante determinados eventos.

**Comandos identificados:**

- Registrar signos vitales del paciente
- Iniciar entrega de turno
- Reportar evento clínico crítico
- Emitir nueva indicación médica
- Marcar indicación como ejecutada
- Consultar evolución del paciente

**Políticas de dominio identificadas:**

- Cuando se registra un cambio crítico → notificar al médico de guardia de forma inmediata
- Cuando se emite una nueva indicación médica → habilitar el flujo de ejecución para enfermería
- Cuando se inicia el cambio de turno → generar un resumen estructurado SBAR de los pacientes asignados
- Cuando un signo vital supera el umbral configurado → generar alerta en el dashboard


#### Paso 4: Modelos de Lectura y Vistas del Sistema

En este paso se identificaron los read models: las vistas que necesitan los actores para tomar decisiones y ejecutar comandos. Cada modelo de lectura representa información consolidada que el sistema debe presentar de forma eficiente al usuario correcto en el momento correcto.

- **Vista de entrega de turno:** Resumen SBAR de cada paciente con eventos pendientes del turno anterior
- **Dashboard de monitoreo:** Signos vitales en tiempo real, alertas activas y tendencias de evolución
- **Panel de indicaciones:** Lista priorizada de indicaciones médicas activas con estado de cumplimiento
- **Historial de eventos críticos:** Registro trazable de eventos clínicos con timestamp, actor y acción tomada
- **Vista de decisión médica:** Información consolidada del paciente para el médico: signos, indicaciones, evolución


#### Síntesis y Derivaciones de Diseño

El Design-Level Event Storming del sistema pulsereport reveló que el flujo clínico de la UCI Cardiovascular puede modelarse en seis bounded contexts con responsabilidades claramente delimitadas: IAM, Patient Administration, Clinical Monitoring (Core Domain), Clinical Documentation, Appointments & Scheduling y Health Analytics. Esta descomposición permite:

- Diseñar módulos de software independientes y desacoplados para cada contexto
- Priorizar el desarrollo iterativo según el impacto clínico de cada contexto
- Establecer contratos claros entre contextos para garantizar la integridad del flujo de información
- Validar el diseño directamente con los usuarios clave (enfermeras y médicos) usando el lenguaje del dominio

Esta metodología, alineada con los principios de Lean UX de reducir el desperdicio y validar rápidamente con usuarios reales, garantiza que el diseño de pulsereport responde a necesidades clínicas concretas y no a supuestos técnicos desconectados de la realidad del servicio.

#### 4.8.1. Software Architecture Context Diagram

Este diagrama presenta una vista general de la plataforma Care-Labs. En la imagen se identifican sus actores principales y los sistemas externos con los que se comunica directamente:

![Context-diagram.png](assets/chapter-4/Context-diagram.png)

#### 4.8.2. Software Architecture Container Diagrams

Este diagrama de nivel C2 aplica un zoom al sistema para identificar sus contenedores internos. En esta estructura, la aplicación API funciona bajo una arquitectura de monolito.

![Container-diagram.png](assets/chapter-4/Container-diagram.png)

#### 4.8.3. Software Architecture Components Diagrams

El nivel C3 permite explorar a detalle cada uno de los contenedores del sistema. En esta sección, el análisis incluye la estructura de los bounded contexts para representar la arquitectura de forma clara y precisa.

Frontend:
La siguiente vista detalla los componentes internos de la aplicación web, donde se organiza la lógica de los servicios, los modelos de dominio y las interfaces de usuario.

![Components-diagrams.png](assets/chapter-4/Components-diagrams.png)


### 4.9. Software Object-Oriented Design
#### 4.9.1. Class Diagrams.


En esta sección, el equipo presenta el Diagrama de Clases UML enfocado en el diseño orientado a objetos de la plataforma Care-Labs. Este diseño se estructura en base a los *Bounded Contexts* (Contextos Delimitados) identificados en la arquitectura, asegurando una alta cohesión y un bajo acoplamiento entre los módulos del sistema.

El diagrama expone un alto nivel de detalle técnico para cada contexto, incluyendo:
* **Clases, Interfaces y Enumeraciones:** Clasificadas mediante estereotipos (`<<Service>>`, `<<Assembler>>`, `<<Entity>>`, `<<Resource>>`) para identificar claramente su rol en la arquitectura.
* **Miembros de Clase:** Se detallan los atributos y métodos con sus respectivos tipos de datos y parámetros.
* **Alcance (Scope):** Se definen los niveles de visibilidad utilizando la notación estándar UML (`+` público, `-` privado, `#` protegido).
* **Relaciones:** Se especifican las dependencias, asociaciones y composiciones, indicando la dirección de la lectura, el nombre de la relación y su multiplicidad exacta (ej. `1` a `0..*`).

**Contextos Delimitados Principales:**
1.  **Clinical Bounded Context:** Constituye el núcleo del sistema. Gestiona las entidades críticas de enfermería cardiovascular, como el registro de signos vitales (`VitalSign`) y los traspasos de pacientes (`SbarTransfer`).
2.  **Patient Bounded Context:** Administra la información demográfica de los pacientes, sus historiales médicos y la programación de citas.
3.  **Security & Audit Bounded Context:** Controla el acceso del personal médico y mantiene un registro inalterable (`AuditLog`) de las acciones críticas para asegurar la trazabilidad.
4.  **Notification Bounded Context:** Procesa y emite alertas en tiempo real frente a anomalías en los signos vitales de los pacientes.

A continuación, se presenta el diagrama general modelado con la herramienta PlantUML:

![Diagram-class.png](assets/chapter-4/Diagram-class.png)

#### 4.9.2. Class Dictionary



