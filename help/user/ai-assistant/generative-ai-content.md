---
title: IA generativa para contenido
description: Aprenda a crear correos electrónicos y páginas de aterrizaje personalizados con IA generativa en  [!DNL Journey Optimizer B2B Edition], incluidas las prácticas recomendadas de solicitud.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
exl-id: 36baf7f9-2fff-4c33-bca0-7d43ec48e74a
source-git-commit: ce4df9a2726cf842c088738521b3e5dd88dd768f
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 2%

---

# IA generativa para contenido {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="Generación de contenido de IA"
>abstract="Después de haber creado el diseño, puede usar herramientas de IA generativa en [!DNL Journey Optimizer B2B Edition] para mejorar el contenido. Esta función simplifica el proceso de personalización y mejora de contenido al ajustar el contenido según el mensaje descriptivo."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="Contenido de referencia"
>abstract="Use _Contenido de referencia_ para cargar un archivo de recursos que contenga contenido que proporcione contexto adicional para IA generativa en [!DNL Journey Optimizer B2B Edition] o para seleccionar un archivo cargado anteriormente. Esta opción garantiza que todos los materiales necesarios estén disponibles para mejorar la calidad y la relevancia del contenido generado."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Términos generativos de IA de Adobe"
>abstract="El acceso a esta función está sujeto a su acuerdo con las directrices de usuario de IA generativa de Adobe Experience Cloud. Revise la precisión de cualquier resultado de esta función y asegúrese de que sea apropiado para su caso de uso."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Directrices del usuario de IA generativa de Adobe"

La IA generativa para el contenido en [!DNL Adobe Journey Optimizer B2B Edition], con tecnología de Microsoft Azure OpenAI y Adobe Firefly, proporciona sugerencias de variación del contenido proactivas para texto e imágenes. Optimice el impacto de su contenido experimentando con diferentes títulos e imágenes principales.

Utilice las características de IA generativa para la creación de contenido en [!DNL Journey Optimizer B2B Edition] para aprovechar las capacidades de IA generativa de Adobe. Cree texto e imágenes personalizados para correos electrónicos, mensajes SMS, páginas de aterrizaje y mucho más. Cuando crea una campaña completa o simplemente perfecciona recursos específicos, estas funciones le ayudan a alinear el contenido sin problemas con las directrices de marca, a la vez que ahorran un tiempo valioso.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>Para tener acceso a estas características en [!DNL Journey Optimizer B2B Edition], debe tener el permiso _[!UICONTROL Asistente de IA]_ > _[!UICONTROL Generar contenido]_. Para obtener más información sobre cómo un administrador de productos puede conceder permisos de características, consulte [Editar roles para permisos de productos](../admin/user-management.md#edit-roles-for-product-permissions).

Las herramientas del Asistente de IA para la generación de contenido son compatibles con los siguientes tipos de recursos:

* [Correos electrónicos](../content/ai-assistant-emails.md)
* [!BADGE Beta] [Páginas de aterrizaje](../content/ai-assistant-landing-pages.md)

## Directrices y limitaciones generales {#general-guidelines-and-limitations}

Su uso de las funciones de IA generativa está sujeto a las [Directrices del usuario de IA generativa de Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Con el compromiso de Adobe con la transparencia en el uso de herramientas de IA generativa para la creación de medios, Adobe aplica [credenciales de contenido](https://helpx.adobe.com/es/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} para cualquier contenido o proyecto que incluya un recurso generado por [!DNL Firefly] cuando se descarga o exporta.

Revise estas directrices generales para usar IA generativa para el contenido en [!DNL Journey Optimizer B2B Edition]:

* Utilice peticiones de datos bien definidas para que el modelo de IA generativa interprete con precisión. El objetivo de marketing o la solicitud que proporcione afectan fuertemente a la calidad del contenido generado.

* Cargue archivos de referencia de contenido para tener un contenido preciso y sin marca. De lo contrario, el contenido se basa en información disponible públicamente. El contenido cargado puede tener los siguientes formatos de archivo: PDF, JPEG, PNG o ZIP (con los formatos de archivo compatibles). El tamaño máximo de un archivo cargado es 50 MB. Pueden funcionar archivos más grandes o un gran número de imágenes, pero esto aumenta el tiempo de procesamiento.

* Utilice una plantilla personalizada o específica de la marca para crear el contenido del correo electrónico. Se recomiendan plantillas de correo electrónico con hasta 8-10 imágenes.

* Asegúrese de informar de cualquier salida problemática utilizando los iconos de la miniatura hacia arriba, la miniatura hacia abajo o el indicador al seleccionar variantes.

## Prácticas recomendadas rápidas para IA generativa {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="Guía rápida"
>abstract="Explore la documentación de [!DNL Journey Optimizer B2B Edition] para aprender a crear indicadores eficaces que produzcan contenido de marketing de alta conversión y sin marca."

Esta guía le ayuda a estructurar sus solicitudes, comunicar la intención con claridad y asegurarse de que la IA produzca mensajes que se ajusten a las directrices de marca, las necesidades de audiencia y los objetivos de la campaña.

Aprenda a escribir indicadores eficaces que permitan al asistente de IA generar contenido de marketing de alta calidad y de marca adaptado a sus objetivos.

### Uso del marco CO-STAR {#costar-framework}

Para obtener los mejores resultados con el contenido generado, organice las indicaciones mediante el marco de trabajo CO-STAR. Este enfoque estructurado proporciona claridad para exactamente lo que necesita.

| Componente | Lo que significa | Por qué importa |
| --- | ---- | ------ |
| **C - Contexto** | Antecedentes de su campaña, producto o situación | Proporciona una comprensión más amplia. |
| **O - Objetivo** | Su objetivo de marketing específico | Controla lo que el contenido debe lograr |
| **S - Estilo** | Cómo desea comunicarse. | Establece el enfoque |
| **T - Tono** | Estilo emocional y voz | Da forma a cómo se siente el mensaje |
| **A - Audiencia** | La audiencia a la que está dirigiendo | Garantiza que el mensaje resuene con las personas adecuadas |
| **R - Requisitos** | Restricciones específicas o elementos imprescindibles | Define límites y elementos críticos |

{style="table-layout:fixed"}

### Solicitar elementos esenciales {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Hacer</th>
<th>No lo hagas</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>Utilice el marco CO-STAR para la estructura
<li>Sea explícito sobre el contenido nuevo frente al existente
<li>Centrar el uso de documentos con directrices de extracción específicas
<li>Realice selecciones de tono, estrategia y configuración regional
<li>Hacer coincidir los objetivos de marketing con las capacidades de tipo de contenido
<li>Generar varias variantes para las pruebas A/B</ul>
</td>
<td>
<ul><li>Solicite cambios estructurales, estilo o edición de imágenes en las solicitudes
<li>Mencione el tono o la estrategia en las solicitudes si están disponibles en las opciones
<li>Utilice objetivos vagos como _promocionar el producto_
<li>Solicitar selecciones de elementos condicionales
<li>Esperar modificaciones de diseño mediante mensajes</ul>
</td>
</tr>
</tbody>
</table>

### Contenido no admitido en las peticiones de datos

>[!TIP]
>
>Use las herramientas de diseño o [!DNL Adobe Express] para modificaciones visuales o de imagen.

Las siguientes solicitudes **_no son compatibles_** y se deben administrar con otras herramientas:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Cruz roja fuera">  Modificaciones de estructura de correo electrónico</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Cruz roja fuera">  Cambios de estilo visuales</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Cruz roja fuera">  Operaciones de edición de imágenes</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Selección de secciones específicas para cambiar</li>
<li>Eliminación o clonación de elementos</li>
<li>Selecciones condicionales</li>
<li>Adición o eliminación de secciones de diseño</li>
</ul>
</td>
<td>
<ul>
<li>Formato de texto (negrita, cursiva, tamaño de fuente)</li>
<li>Modificaciones de color</li>
<li>Estilo del diseño (bordes, relleno, márgenes)</li>
<li>Efectos visuales (sombras)</li>
</ul>
</td>
<td>
<ul>
<li>Cambios de fondo</li>
<li>Adición de superposiciones de texto o logotipos</li>
<li>Recorte o cambio de tamaño de imagen</li>
<li>Ajustes de color</li>
<li>Reemplazo de imagen</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Lista de comprobación de calidad {#quality-checklist}

Antes de generar contenido, asegúrese de lo siguiente:

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Borrar objetivo**: Indica claramente la acción, el producto/servicio, el valor y el contexto.

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Audiencia de destino definida**: Especifica el grupo demográfico, la función o el segmento.

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Alineación de tipo de contenido**: El objetivo coincide con el canal o formato seleccionado.

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Revisar selecciones**: se elige el tono, la estrategia y la configuración regional; no los incluya en el mensaje.

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Se especificó el enfoque del documento**: resalta qué contenido o secciones hacer referencia.

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Aplicada a la marca**: se han seleccionado las directrices de marca adecuadas.

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} **Ámbito realista**: evite solicitudes de cambios de diseño, estilo o ediciones estructurales.

### Objetivos de marketing efectivos {#marketing-objectives}

Al diseñar los objetivos de marketing, asegúrese de que sean claros, procesables y mensurables. Evite declaraciones vagas o genéricas.

**Ejemplos de buenos objetivos:**

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Registros de unidad para la versión de prueba gratuita de 30 días del nuevo tablero de análisis con tecnología de IA&quot;

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Generar posibles clientes para el seminario web B2B sobre &#39;Reducción de los costos de nube en un 40 %&#39; que se celebrará el 15 de marzo&quot;

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Promociona el descuento del 25% por tiempo limitado en las suscripciones premium, que finalizará el 25 de diciembre&quot;

**Ejemplos que se deben evitar:**

![Cruz roja](../../assets/do-not-localize/check-box-red.svg){width="20"} al &quot;Promocionar el producto&quot; (demasiado vago)

![Cruz roja](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Hacer que la gente firme acuerdos&quot; (valor poco claro)

![Correo electrónico sobre nuevas características tachado de rojo](../../assets/do-not-localize/check-box-red.svg){width="20"}&quot; (carece de propósito)

#### Estructurar el objetivo

Proporcione siempre el contexto y la propuesta de valor para producir contenido relevante. Utilice la siguiente fórmula para escribir objetivos eficaces: **Acción + Producto/Servicio + Valor/Beneficio + Urgencia/Contexto**

**Ejemplos de buenos objetivos:**

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"}: &quot;Fomente las descargas de la nueva aplicación móvil que ayuda a los usuarios a seguir hábitos de vida sostenibles con recomendaciones personalizadas y ecológicas&quot;

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Promover el registro para el taller exclusivo sobre técnicas avanzadas de visualización de datos para profesionales de marketing&quot;

![Marca de verificación verde](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Impulse la asistencia al evento de lanzamiento del producto que muestra el revolucionario asistente de escritura de IA que ahorra más de 5 horas por semana&quot;

**Ejemplos que se deben evitar:**

![Tachar de rojo](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Anunciar nueva aplicación&quot; (falta propuesta de valor y contexto)

![Cruz roja](../../assets/do-not-localize/check-box-red.svg){width="20"}: &quot;Haga que la gente se inscriba en el taller&quot; (carece de especificidad acerca de la audiencia y el beneficio)

![Tachar de rojo](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Promocionar evento&quot; (sin acción, valor o urgencia claros)

#### Ejemplos de solicitudes por tipo de canal {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canal</th>
<th>Ejemplo</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Correo electrónico</strong></td>
<td>"Fomente las perspectivas empresariales mostrando tres casos de éxito de clientes con métricas detalladas de ROI (Oracle: reducción de costes del 45 %, Accenture: aumento de posibles clientes del 200 %, Microsoft: ahorro de tiempo del 60 %). Directores de TI objetivo en empresas con más de 1000 empleados"</td>
</tr>
<tr>
<td><strong>Páginas de aterrizaje</strong></td>
<td>"Convierta a los visitantes B2B en posibles clientes cualificados demostrando cómo la solución de seguridad empresarial evita el 99,9 % de los ataques cibernéticos, con testimonios de Fortune 500 y auditorías de seguridad gratuitas".</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### Contenido nuevo frente a modificación de contenido existente {#new-vs-modify}

Indique claramente si su solicitud implica la generación de contenido nuevo o la actualización de material existente. Esta distinción es importante porque guía a la IA en la selección del enfoque adecuado y garantiza un resultado más preciso y útil.

#### Creación de nuevo contenido

Aplique esta estrategia al iniciar campañas de marketing, descubrir nuevas soluciones o iniciar comunicaciones actualizadas o actualizadas. Garantiza que el mensaje comience con fuerza y se ajuste a sus objetivos.

**Cómo preguntar** ➤ Al crear contenido nuevo, céntrese en su objetivo de marketing sin hacer referencia al contenido existente.

>[!BEGINSHADEBOX &quot;Ejemplos&quot;]

* **Prueba de SaaS**: &quot;Lance el nuevo software CRM a los propietarios de pequeñas empresas, destacando un ahorro de tiempo del 50%, una calificación de clientes potenciales 90% más rápida y una prueba gratuita de 30 días con incorporación personalizada&quot;
* **Anuncio de características**: &quot;Anuncie nuevas funciones de integración de API que reduzcan el tiempo de desarrollo en un 60 % para los clientes empresariales, dirigiéndose a los responsables técnicos de la toma de decisiones&quot;
* **Promoción de eventos**: &quot;Impulse los registros para el seminario web sobre &#39;Tendencias de marketing digital 2024&#39; con expertos de Google, Meta y Adobe, haciendo hincapié en perspectivas procesables y puestos limitados (500 como máximo)&quot;

>[!ENDSHADEBOX]

#### Modificación del contenido existente

>[!TIP]
>
>Para realizar modificaciones estándar como elaborar, resumir o simplificar, seleccione **_Refinar_** en lugar de escribir instrucciones personalizadas.

Utilice un mensaje de modificación cuando necesite actualizar, actualizar o adaptar sus campañas de marketing actuales. Este método admite mejoras incrementales, lo que garantiza que la mensajería siga siendo relevante sin comenzar desde cero.

**Cómo preguntar** ➤ Al modificar contenido existente, especifique claramente qué desea cambiar y cómo hacerlo.

>[!BEGINSHADEBOX &quot;Ejemplos&quot;]

* **Actualización de la campaña**: &quot;Modifique el correo electrónico de inicio del programa para que se centre en las características de seguridad empresarial en lugar de en las ventajas generales de productividad, dirigiéndose a los responsables de la toma de decisiones de TI con certificaciones de cumplimiento&quot;.
* **Giro de audiencia**: &quot;Adapte la invitación de demostración de software para dirigirse específicamente a la atención médica, reemplazando los ejemplos genéricos por casos de uso de atención médica y beneficios de cumplimiento de HIPAA&quot;
* **Actualización estacional**: &quot;Actualice la campaña promocional del tercer trimestre para las compras de las vacaciones del cuarto trimestre, cambiando el enfoque de los regalos de vuelta al colegio a las vacaciones, con énfasis en los envíos rápidos&quot;

>[!ENDSHADEBOX]

## Configuración de texto avanzada {#text-settings}

Además de utilizar un mensaje claro y bien formado, la configuración de texto de las herramientas de contenido del Ayudante de IA incluye una configuración de texto que puede utilizar para optimizar los resultados generados.

>[!TIP]
>
>Use las opciones _[!UICONTROL Estrategia de comunicación]_ y _[!UICONTROL Tono]_ en la _[!UICONTROL configuración de texto]_ en lugar de mencionar estas características en el mensaje.

### Tipos de estrategias de comunicación

Su estrategia de comunicación determina cómo presentar el mensaje para maximizar el impacto. Las diferentes estrategias funcionan mejor para diferentes objetivos, ya sea que esté generando urgencia, estableciendo confianza o impulsando una acción inmediata. Elija la estrategia que mejor se ajuste a los objetivos de su campaña y a la mentalidad de su audiencia.

| **Estrategia** | **Mejor para** | **Estilo de mensajería** | **Ejemplos** |
| ------------ | ------------ | ------------------- | ------------ |
| **Urgente** | Ofertas con distinción de tiempo, plazos, acción inmediata | Crea presión inmediata con lenguaje basado en el tiempo | <li>&quot;Actuar ahora: la oferta caduca a medianoche&quot; <li>&quot;Regístrese hoy antes de que los lugares se llenen&quot; <li>&quot;La venta flash de 48 horas comienza ahora&quot; |
| **FOMO (Miedo a perderse)** | Ofertas limitadas, eventos, acceso exclusivo | Utiliza señales de urgencia, escasez y presión de tiempo | <li>&quot;¡Solo quedan 24 horas! Acciones limitadas con un descuento del 40 %&quot; <li>&quot;Última oportunidad: El precio por anticipado termina mañana&quot; <li>&quot;Solo quedan 100 puntos beta&quot; |
| **Revisión social** | Confianza, testimonios, productos populares | Aprovecha las experiencias y la validación de otros | <li>&quot;Únase a más de 50 000 clientes satisfechos&quot; <li>&quot;Clasificado 4.9/5 estrellas por profesionales del sector&quot; <li>&quot;Confiado por las empresas de Fortune 500&quot; |
| **Escasez** | Inventario limitado, versiones exclusivas, artículos de alta demanda | Destaca la disponibilidad y exclusividad limitadas | <li>&quot;Solo quedan 5 en stock&quot; <li>Edición limitada: 100 unidades disponibles <li>&quot;Lanzamiento exclusivo: primero en llegar, primero en llegar&quot; |
| **Incentivo** | Promociones, programas de recompensa, ofertas especiales | Destaca beneficios tangibles y recompensas | <li>&quot;Consigue un 20% de descuento en tu primer pedido&quot; <li>&quot;Consigue puntos dobles este fin de semana&quot; <li>&quot;Envío gratuito en pedidos superiores a $50&quot; |
| **Exclusividad** | Productos Premium, experiencias de VIP, ofertas solo para miembros | Utiliza un idioma de posicionamiento premium y acceso especial | <li>&quot;Invitación exclusiva a una vista previa privada&quot; <li>&quot;La membresía Elite desbloquea los análisis avanzados&quot; <li>&quot;Únase a determinadas empresas de la lista Fortune 500 que ya nos utilizan&quot; |
| **Gamification** | Campañas de participación, programas de fidelización y contenido interactivo | Utiliza la mecánica de juegos y el lenguaje de logros | <li>&quot;Desbloquea tu siguiente nivel de recompensa&quot; <li>&quot;Completar retos para conseguir insignias&quot; <li>&quot;Sube a la tabla de clasificación para obtener premios exclusivos&quot; |
| **Informativo** | Educación, investigación, productos complejos, liderazgo mental | Utiliza hechos, datos, perspectivas y explicaciones | <li>&quot;5 datos del análisis de más de 10 000 interacciones&quot; <li>&quot;Una nueva investigación revela 3 enfoques innovadores&quot; <li>&quot;Guía completa para la implementación de la IA en marketing&quot; |
| **Educación e información** | Contenido de aprendizaje, tendencias del sector, prácticas recomendadas | Proporciona conocimientos valiosos y procedimientos útiles | <li>&quot;Aprenda técnicas avanzadas con una guía de expertos&quot; <li>&quot;Descubra 7 estrategias que utilizan los mejores especialistas en marketing&quot; <li>&quot;Aprenda a optimizar el flujo de trabajo en 5 pasos&quot; |

### Establecer el tono correcto {#tone}

El tono define cómo la audiencia percibe y responde al mensaje. Seleccione siempre un tono que se ajuste a la voz de su marca y al escenario del recorrido del perfil.

Revise las opciones de tono disponibles, incluyendo cuándo funciona mejor cada una y ejemplos de contenido que se ajustan a cada estilo.

| Tonalidad | Mejor para | Ejemplo de contenido |
| ---- | ----- | ----- |
| Profesional | Comunicaciones B2B, anuncios formales | &quot;Nos complace anunciar nuestra asociación estratégica...&quot; |
| Empático | Asistencia al cliente, temas confidenciales | &quot;Entendemos lo frustrante que este asunto debe ser para usted...&quot; |
| Divertido | Campañas atractivas, contenido desenfadado | &quot;Advertencia: ¡Puede causar importantes mejoras en la productividad!&quot; |
| Emocionante | Lanzamientos de productos, promociones de eventos | &quot;¡Este es el momento que has estado esperando!&quot; |
| Inspirador | Campañas de motivación, objetivo de marca | &quot;Juntos, podemos hacer una diferencia en el mundo...&quot; |
| Persuasivo | Campañas de ventas, conversiones | &quot;No pierdas esta oportunidad de tiempo limitado para...&quot; |
| Amistoso | Participación del cliente, mensajes de bienvenida | &quot;¡Me alegra que estés aquí con nosotros!&quot; |
| Formal | Comunicaciones legales, avisos oficiales | &quot;Esta es una notificación de los siguientes cambios...&quot; |
| Apologético | Recuperación del servicio, resolución de problemas | &quot;Bodea se disculpa sinceramente por cualquier inconveniente causado...&quot; |
| Asertivo | Contenido de liderazgo, mensajería autorizada | &quot;Esto es lo que tienes que hacer ahora mismo...&quot; |
| Narración | Narrativas de marca, conexiones emocionales | &quot;Todo comenzó con una simple pregunta...&quot; |
| Conversatorio | Nutrir campañas, construir relaciones | &quot;Hablemos de cómo este programa puede ayudarte...&quot; |

## Contenido de referencia optimizado {#reference-content}

>[!TIP]
>
>Si ya ha subido un recurso a través del menú **[!UICONTROL Contenido de referencia]**, no es necesario que haga referencia a él en su solicitud. El sistema utiliza automáticamente los documentos seleccionados.

Los archivos de contenido de referencia proporcionan información objetiva que enriquece el contenido generado con detalles específicos y precisos. Al cargar documentos, como folletos de productos o white papers, modifique el mensaje para incluir las partes que tienen el enfoque:

* **En lugar de** _&quot;Use el folleto del producto&quot;_ **debería usar** _&quot;Céntrese en las características de seguridad avanzadas y las certificaciones de cumplimiento, específicamente en el cumplimiento de SOC 2 y el cifrado de datos&quot;_

* **En lugar de** _&quot;Consulte los estudios de caso&quot;_ **debería usar** _&quot;Resaltar los resultados de retorno de la inversión de los clientes del sector sanitario, específicamente la reducción de costos del 40% en el Centro Médico Regional&quot;_

* **En lugar de** _&quot;Incluir detalles técnicos&quot;_ **debe usar** _&quot;Enfatizar las capacidades de integración de API y los beneficios para desarrolladores, centrándose en los extremos de API de REST y en el tiempo de actividad del 99,9 % de SLA&quot;_

### Refinamiento de contenido

Una vez generado el contenido, use la característica **_[!UICONTROL Refine]_** para iterarla y mejorarla con las siguientes opciones:

* **[!UICONTROL Elaborar]**: el asistente de IA puede ayudarle a ampliar temas específicos y proporcionar detalles adicionales para una mejor comprensión y participación.

* **[!UICONTROL Resumir]**: la información larga puede sobrecargar los visores de la página. Utilice el asistente de IA para condensar los puntos clave en resúmenes claros y concisos que llamen la atención y los animen a leer más.

* **[!UICONTROL Reformular]**: vuelva a escribir el mensaje conservando su significado. Esta opción le ayuda a generar frases alternativas, mejorar el flujo o ajustar el estilo sin cambiar el mensaje principal.

* **[!UICONTROL Use un lenguaje más sencillo]**: simplifique el lenguaje y garantice la claridad y accesibilidad para una audiencia más amplia.

* **[!UICONTROL Traducir]** - Traduzca el texto a otro idioma. (Actualmente, el inglés es el único idioma admitido).

* **[!UICONTROL Cambiar tono]**: ajuste el tono del mensaje para que se ajuste a su estilo de comunicación, por ejemplo, para que sea más cordial, profesional, urgente o inspirador.

* **[!UICONTROL Cambiar estrategia de comunicación]**: modifique el enfoque de mensajería en función de sus objetivos, como crear urgencia o enfatizar atractivo interesante.
