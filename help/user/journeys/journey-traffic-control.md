---
title: Control de tráfico de recorrido
description: Aprenda cómo el control de tráfico de recorrido inscribe a cada persona en el recorrido de mejor ajuste cuando cumplen los requisitos para varios, y cómo ajustar las ponderaciones y revisar las decisiones.
hide: true
autotag-review: '2026-10-16T18:41:12.165Z'
TQID: 'https://experienceleague.adobe.com/oD1nTkrgqGZ-nzfHNFS66XvjQkn5FmOZ-cI3EDKnb4U'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: 4515ee43-e3ce-55db-9ba1-60b2b42b9d75
    internal-label: Privacy
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
subfeature_v2:
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
    internal-label: Decisioning
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d9b663ab-b785-4c49-8fc3-d3dda520c908
    internal-label: Automated decisioning
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 050fcccbef4e84a540d415cfabc65f25310c062f
workflow-type: tm+mt
source-wordcount: '2692'
ht-degree: 0%
---
# control de tráfico de recorrido

En [!DNL Adobe Journey Optimizer B2B Edition], las audiencias se superponen con frecuencia. Un director de marketing de una empresa de servicios financieros podría cumplir los requisitos para el recorrido del sector, el recorrido de interés de productos y el recorrido de cuenta empresarial el mismo día. Sin coordinación, esa persona se inscribe en las tres y recibe mensajes concurrentes o redundantes. Use _control de tráfico de Recorrido_ para inscribir a cada persona en el recorrido de una persona que mejor se ajuste a sus necesidades cuando califique para más de un recorrido al mismo tiempo.

El control de tráfico del recorrido revisa a todas las personas que califican para más de un recorrido participante. Compara lo que sabe sobre la persona con cada propósito de recorrido e inscribe a la persona en la mejor coincidencia. Una persona que califica para un solo recorrido está inscrita en ese recorrido. Una persona que cumple los requisitos para ninguno no está inscrita.

## Ventajas del control de tráfico de recorrido {#benefits}

El control de tráfico de recorrido sustituye la gestión manual de la superposición por una decisión registrada y adaptada para cada persona.

| Sin control de tráfico de recorrido | Con control de tráfico de recorrido |
|---|---|
| Una persona que coincide con varias audiencias se inscribe en varios recorridos y recibe mensajes superpuestos. | Cada persona está inscrita en un recorrido participante como máximo para cada evaluación. |
| Los equipos administran la superposición a mano con segmentos de exclusión y reglas de audiencia. Estas reglas se vuelven más difíciles de mantener con cada nuevo recorrido. | El sistema elige en función del ajuste. No genera ni mantiene la lógica de exclusión. |
| Es difícil explicar por qué una persona recibió un determinado recorrido. | Todas las decisiones se registran y pueden verse, incluida la puntuación de cada recorrido de la competencia. |
| La fatiga de los mensajes y la mensajería mixta reducen la participación. | Cada persona tiene una experiencia relevante y consistente. |

## Ejemplos de uso {#examples}

Utilice el control de tráfico de recorrido cuando los recorridos se dirijan a audiencias superpuestas. Por ejemplo:

* **Programas de nutrición en la industria**: Usted ejecuta recorridos separados para Servicios Financieros, Salud y Manufactura. Un contacto no tiene valor en el sector, pero su perfil está vinculado a la cuenta de un banco. El control de tráfico del recorrido hace coincidir el contacto con el recorrido de Servicios Financieros en lugar de inscribirlos en los tres.
* **Campañas de interés en productos**: ejecuta un recorrido para cada línea de productos. Un cliente potencial con señales de interés recientes en dos productos se inscribe en el recorrido del producto con el interés más alto.
* **Mensajería basada en roles**: Ejecuta un recorrido para evaluadores técnicos y otro para patrocinadores ejecutivos. El cargo y la función de una persona deciden a qué recorrido se une.
* **Programas para empresas y pymes**: ejecuta diferentes recorridos según el tamaño de la compañía. El segmento de cliente y la información de cuenta de un contacto deciden a qué recorrido se unen.
* **Se inicia un nuevo recorrido**: Usted publica un nuevo recorrido en una audiencia que otros recorridos ya cubren. El control de tráfico de recorrido evalúa la superposición, por lo que no se rediseñan las reglas de audiencia existentes.

## Selección por ajuste {#dimensions}

Cuando una persona cumple los requisitos para más de un recorrido, el control de tráfico de recorrido compara el perfil de la persona con el nombre y la descripción de cada recorrido candidato. La comparación abarca cuatro dimensiones.

| Dimensión | Qué se compara |
|---|---|
| Industria | La industria de la persona. Si falta el sector, el sector de la cuenta vinculada. |
| Ajuste funcional | El rol y la función laboral de la persona. |
| Tamaño de empresa | Segmento de cliente, tipo de cuenta y contexto de gasto de la persona. |
| Intención | El producto por el que la persona ha mostrado el interés reciente más fuerte. |

Tenga en cuenta los siguientes puntos:

* **Importan los nombres y las descripciones de los Recorridos.** Le dicen al sistema para qué sirve cada recorrido. Las descripciones específicas y precisas producen mejores coincidencias.
* **Los datos que faltan se omiten, no se adivinan.** Si una persona no tiene valor para una dimensión, el control de tráfico de recorrido excluye esa dimensión para esa persona. Toma la decisión sobre las dimensiones que tienen datos.

El registro de decisión de cada persona en las vistas de creación de informes muestra la puntuación de cada recorrido de la competencia y las dimensiones utilizadas. Una dimensión sin datos se marca como excluida.

### Comparaciones {#comparisons}

Para cada dimensión, el control de tráfico de recorrido compara el texto relevante de la persona, como el puesto, con la descripción de cada recorrido. Utiliza dos métodos:

* **Similitud de significado**: ¿El texto significa algo parecido a la descripción?
* **Coincidencia de palabras clave**: ¿El texto utiliza los mismos términos que la descripción?

El resultado más potente de los dos métodos se convierte en la puntuación del recorrido para esa dimensión.

A continuación, cada dimensión propone su recorrido de mejor puntuación, pero solo si la puntuación supera un umbral de calidad mínimo. Se descartan los recorridos sin una propuesta que cumpla los requisitos. Las ponderaciones que configure clasifican los recorridos restantes según sus puntuaciones ponderadas combinadas. Se selecciona el recorrido con la puntuación más alta. El ganador no es necesariamente el recorrido con la mayor cantidad de propuestas. Una coincidencia sólida en una sola dimensión es más significativa que varias coincidencias más débiles.

Cada registro de decisión almacena la siguiente información:

* El recorrido seleccionado y los recorridos de la competencia
* Las puntuaciones de cada dimensión y la puntuación combinada
* Un valor de confianza
* Nivel de acuerdo de Alto, Medium o Bajo, que muestra cuántas dimensiones admiten el ganador

<!-- CONFIRM with Engineering: whether to describe the fallback when no dimension produces a qualifying match. The source says the person is still enrolled in one eligible journey, selected consistently, with a 0% (Low) confidence decision record. Also confirm how "consistent" should be phrased. -->

## Configuración {#configuration}

Para establecer las ponderaciones de dimensión del control de tráfico de recorrido y simular la puntuación:

1. En el panel de navegación izquierdo, vaya a **[!UICONTROL administración de Recorrido]** > **[!UICONTROL control de tráfico de Recorrido]**.

1. Seleccione la ficha **[!UICONTROL Configuración]**.

![Pestaña Configuración del control de tráfico de Recorrido con cuatro tarjetas de ponderación de dimensión, cada una con Medium al 25% y botón Guardar ponderaciones](./assets/journey-traffic-control-configuration.png){width="800" zoomable="yes"}

### Ajuste de pesos de dimensión {#weights}

De manera predeterminada, las cuatro dimensiones tienen un peso de _Medium_ y contribuyen de manera equitativa, a un 25% cada una. Ajuste las ponderaciones para cambiar en qué medida cada dimensión influye en las decisiones.

1. Para cada dimensión, establezca el nivel de ponderación:

   * **[!UICONTROL Desactivado]**
   * **[!UICONTROL Baja]**
   * **[!UICONTROL Medium]**
   * **[!UICONTROL Alta]**

   El porcentaje de cada tarjeta muestra la cuota de esa dimensión después de combinar los ajustes. Para quitar una dimensión de las decisiones, establézcala en **[!UICONTROL Desactivada]**.

   ![Tarjetas de peso Dimension con Intent establecido en High en 55%, Industry Medium en 27% y Functional fit y Company size Low en 9%](./assets/journey-traffic-control-dimensions.png){width="600"}

   El porcentaje que se muestra en cada tarjeta es la contribución normalizada de esa dimensión después de combinar todas las selecciones, siempre totalizando el 100%. Si eleva una dimensión, el sistema vuelve a normalizar automáticamente las demás para que el total se mantenga en el 100 %.

   Puede hacer clic en **[!UICONTROL Restablecer a igual]** para que todas las dimensiones vuelvan a una ponderación par.

1. Cuando quiera aplicar los pesos ajustados, seleccione **[!UICONTROL Guardar pesos]**.

   >[!NOTE]
   >
   >Para guardar los cambios en los pesos de dimensión, debe tener el _[!UICONTROL permiso de administración de B2B]_ [configuraciones del producto](../admin/user-management.md#b2b-product-permissions).

### Simular puntuación {#simulate-scoring}

Antes de comprometer pesos en la producción, puede simular cómo se comportaría el control de tráfico con esos cambios. La simulación no requiere que esté activado el control de tráfico de recorrido. Evalúa los perfiles que ya están en sus recorridos activos y les aplica la lógica de control de tráfico. Entonces usted puede juzgar si los resultados se ven bien para los ajustes de peso.

Haga clic en **[!UICONTROL Simular puntuación]**.

El encabezado de resultados resume la ejecución:

* **Perfiles evaluados**: cuántos perfiles se puntuaron y en cuántos recorridos.
* **Promedio de conflictos/perfil**: el promedio de recorridos en competencia por perfil.
* **Puntuación media de coincidencia**: la confianza media de los recorridos seleccionados.

![Simular resultados de puntuación con 20 perfiles evaluados en 5 recorridos, 1,0 conflictos promedio y una puntuación de coincidencia promedio del 70 %](./assets/journey-traffic-control-simulate-scoring.png){width="700" zoomable="yes"}

Cada perfil evaluado aparece como una tarjeta que muestra el recorrido seleccionado, la lógica clave, las señales de intención y la puntuación de la coincidencia. Seleccione un perfil con el que abrir una vista de detalles:

* **Puntuación de coincidencia** — La coincidencia general, con un desglose por dimensión codificado por color.
* **Puntuaciones por recorrido**: los recorridos para los que esta persona cumple los requisitos, cuál se seleccionó y por qué.
* **Dimensiones consideradas**: Los datos de dimensión que condujeron la decisión, ampliables para mostrar las señales subyacentes.

![Panel de detalles del perfil con una puntuación de coincidencia del 77 %, puntuaciones por recorrido con un recorrido seleccionado y las dimensiones consideradas](./assets/journey-traffic-control-simulate-scoring-profile-details.png){width="450" zoomable="yes"}

Si es necesario, ajuste los pesos de dimensión y haga clic en **[!UICONTROL Ejecutar de nuevo]** para volver a ejecutar la simulación.

También puede hacer clic en **[!UICONTROL Muestreo de nuevas personas]** para volver a ejecutar la simulación con una nueva muestra aleatoria.

Cuando esté satisfecho con el resultado, puede hacer clic en **[!UICONTROL Guardar pesos]** para confirmar los pesos. Las nuevas decisiones de control de tráfico utilizan la nueva configuración inmediatamente, pero las decisiones anteriores no se ven afectadas. Los pesos que ha probado aparecen en la pestaña principal _[!UICONTROL Configuración]_ y se usan para cualquier recorrido que el control de tráfico esté evaluando en su entorno activo.

También puede salir de la página sin aplicar las ponderaciones.

## Revisar informes {#reporting}

Utilice las vistas de informes para ver cómo el recorrido de tráfico controla las personas inscritas. Revisar las decisiones por recorrido o por ejecución.

### Informes por recorrido {#reporting-by-journey}

La vista **[!UICONTROL Por Recorrido]** resume los recorridos bajo control de tráfico.

| Métrica | Descripción |
|---|---|
| Recorridos gobernados | Recorridos que participan en el control de tráfico. |
| Recorridos impugnados | Recorridos que comparten personas con al menos otro recorrido. |
| Perfiles impugnados | Personas distintas reclamadas por dos o más recorridos. |
| Personas inscritas | Distintas personas inscritas. |

Para cada recorrido, la vista también muestra los siguientes valores:

* **[!UICONTROL Inscrito]**: El número total de personas inscritas.
* **[!UICONTROL No impugnado]**: Personas que calificaron solo para este recorrido.
* **[!UICONTROL Ganó]**: Personas que cumplen los requisitos para varios recorridos y se inscribieron en este.
* **[!UICONTROL Tasa de victorias]**: La frecuencia con la que ganó el recorrido cuando las personas compitieron por él.

![Por vista de informe de Recorrido con métricas de resumen y una tabla de recorridos que muestra los valores de las tasas de inscripción, no impugnada, ganada y ganada](./assets/journey-traffic-control-reporting-by-journey.png){width="700" zoomable="yes"}

Filtrar la lista por [estado del recorrido](./journeys-overview.md#journey-status): [!UICONTROL Activo], [!UICONTROL Finalizado], [!UICONTROL Anulado] o [!UICONTROL Todos].

Para ver dónde terminó la gente disputada de un recorrido, abra el recorrido. La vista de detalles muestra los recorridos en los que se inscribieron las personas. Para ver la puntuación de la coincidencia, los recorridos de la competencia, la puntuación de cada uno y las dimensiones utilizadas, expanda el registro de decisiones de cualquier persona inscrita. Busque por nombre, ID de posible cliente o ID de perfil.

![Vista de detalles de Recorridos con métricas de inscripción, un gráfico de dónde aterrizaron los perfiles impugnados y una tabla de personas inscritas](./assets/journey-traffic-control-reporting-by-journey-detail.png){width="700" zoomable="yes"}

Para comparar la distribución de productos por intención o sector entre recorridos, selecciona **[!UICONTROL Comparar recorridos]** y elige al menos dos y hasta 20 recorridos activos.

<!-- Figure placeholders: By Journey overview, journey detail "Where contested profiles landed", and a decision record. Redact person names and use clean sample journey names without test prefixes. Choose runs with healthy enrollment counts. -->

### Informes por ejecución {#reporting-by-run}

Seleccione **[!UICONTROL Por ejecución]** para ver una lista de cada ejecución de evaluación con la siguiente información:

* El momento de la ejecución
* Cómo se activó la ejecución: *programada*, *al publicar* o *manual*
* El número de personas evaluadas, inscritas y no inscritas

![Por Ejecutar vista de informes con filtros de intervalo de tiempo y déclencheur y una tabla de ejecuciones con recuentos evaluados, inscritos y no inscritos](./assets/journey-traffic-control-reporting-by-run.png){width="700" zoomable="yes"}

Filtre la lista por intervalo de tiempo (24 horas, 7 días, 30 días o todo el tiempo) y tipo de déclencheur.

Para ver un diagrama de flujo desde las personas evaluadas hasta los recorridos en los que se inscribieron, abra una ejecución. Un desglose por cada recorrido muestra cuántas personas estaban **[!UICONTROL No inscritas]**, **[!UICONTROL Inscritas]**, **[!UICONTROL Arbitradas]** (elegidas entre los recorridos de la competencia) y **[!UICONTROL No disputadas]**. Para cualquier recorrido de una carrera, también puede ver las personas evaluadas, sus resultados, los recorridos con los que compitieron y sus puntuaciones de partido.

![Diagrama de flujo que muestra las personas evaluadas y sus resultados de inscripción en los recorridos](./assets/journey-traffic-control-reporting-by-run-flow-chart.png){width="500" zoomable="yes"}

<!-- CONFIRM with Product: what the scheduled and on-publish triggers mean for customers, and the content of the Not enrolled tooltip. -->

## Proceso de ejecución de evaluación {#run-process}

Cada ejecución sigue la misma secuencia. El control de tráfico de recorrido lee solamente los datos que ya están presentes en su entorno [!DNL Journey Optimizer B2B Edition] y no requiere fuentes de datos adicionales.

1. El control de tráfico de recorrido espera a que la persona y la cuenta [actualización de perfil](../data/data-availability-timing.md#daily-refresh) de su entorno se completen correctamente. Si la actualización falla, no se inicia ninguna ejecución con datos antiguos.

1. La pertenencia a audiencias se calcula en [!DNL Adobe Experience Platform] y [se sincroniza](../data/data-availability-timing.md#platform-sync) con [!DNL Journey Optimizer B2B Edition]. Una vez finalizada la segmentación, el sistema espera a que se complete la sincronización durante un máximo de 30 minutos. Si la sincronización finaliza antes, el procesamiento se inicia inmediatamente. Si pasan 30 minutos primero, el procesamiento comienza de todos modos. Si la sincronización termina más tarde, se inicia una nueva ejecución en los datos actualizados.

1. El sistema monta los recorridos candidatos. Solo participan los recorridos activos y habilitados para el control de tráfico. El sistema lee el estado, el nombre y la descripción de cada recorrido.

1. El sistema lee el abono a audiencias y el contexto de perfil en lotes pequeños.

1. El sistema comprueba la idoneidad. Una persona solo es elegible para un recorrido cuando se cumplen todas las condiciones siguientes:

   * El recorrido está activo y habilitado para el control de tráfico.
   * Actualmente, la persona es miembro de la audiencia del recorrido.
   * La persona no se ha inscrito correctamente en ese recorrido anteriormente.
   * La persona no está inscrita actualmente en ese recorrido.

1. El sistema selecciona un recorrido. Se inscribe en él una persona con un recorrido apto. Una persona sin recorrido elegible no está inscrita. Para una persona con varios recorridos aptos, el sistema compara el perfil de la persona con el nombre y la descripción de cada recorrido en las [cuatro dimensiones](#dimensions).

1. El sistema envía la inscripción al recorrido seleccionado mediante el mecanismo de inscripción de recorrido estándar.

1. El sistema guarda cada decisión y resultado de inscripción para la creación de informes y auditorías.

1. Los puntos de comprobación del sistema avanzan a medida que finalizan los lotes, registran el resultado y envían una notificación de finalización.

## Datos utilizados y almacenados {#data}

El control de tráfico de recorrido utiliza los siguientes datos de su entorno.

| Datos | Origen | Utilice |
|---|---|---|
| Estado, nombre y descripción del recorrido | Sus recorridos | Decida qué recorridos participan y para qué sirve cada recorrido. |
| Abono de público | [!DNL Experience Platform] audiencias sincronizadas en [!DNL Journey Optimizer B2B Edition] | Identifique quién cumple los requisitos para cada recorrido. |
| Perfil de persona, como sector, cargo y función y segmento de cliente | Sus datos personales | Proporcionar las dimensiones de industria, ajuste funcional y tamaño de la empresa. |
| Perfil de cuenta vinculado, como sector y tipo de cuenta | Los datos de su cuenta | Rellene el sector cuando falte el valor propio de la persona y proporcione el contexto de la cuenta. |
| Interés del producto | Tus [datos de intención](../admin/intent-data.md) | Proporcione la dimensión de intención. Se utiliza el producto con el interés más reciente y más fuerte. |
| Historial de inscripciones | Registros escritos por ejecuciones anteriores | Evite inscribir a la misma persona en el mismo recorrido repetidamente. |
| Estado de inscripción actual | [!DNL Journey Optimizer B2B Edition] | Evite inscribir a una persona que ya esté en el recorrido. |

Para cada ejecución, el control de tráfico de recorrido almacena un resumen de ejecución. Almacena un registro de decisión de inscripción para cada persona inscrita. Ambos se almacenan en los almacenes de datos del entorno administrados por Adobe. Activa los informes e impide que se repitan las inscripciones.

<!-- 
CONFIRM with Engineering, Security, and Legal before publishing. The source material does not state any of the following data handling commitments:
- Where processing occurs and data residency.
- Whether meaning similarity comparison uses a third-party or externally hosted AI service, and whether profile text leaves the Adobe environment.
- Whether customer data is used to train models shared with other customers.
- The retention period for decision and enrollment records, and how they are deleted when a person is erased (link to privacy requests).
- Encryption in transit and at rest, role-based access to the reports, and tenant isolation. 
-->

## Configuración del control de tráfico de recorrido {#setup}

Puede habilitar el control de tráfico de recorrido directamente en un [recorrido de persona](./create-publish-journey.md) individual cuando esté en estado _Borrador_.

1. Asegúrese de que el recorrido de la persona tenga un nombre y una descripción que proporcionen un propósito y un objetivo claros para el recorrido.

   Estos nombres y descripciones son la base de la coincidencia.

1. Haga clic en **[!UICONTROL ... Más]** en la parte superior derecha del lienzo de recorrido y elige **[!UICONTROL configuración de control de tráfico de Recorrido]**.

   ![Menú de recorrido de persona de borrador Más abierto, que muestra las opciones Duplicar, Eliminar, Control de tráfico de Recorrido y Reentrada](./assets/person-journey-draft-more-menu.png){width="400"}

1. En el cuadro de diálogo, habilite la opción **[!UICONTROL Habilitar el control de tráfico de recorrido]**.

   El cuadro de diálogo de configuración explica el comportamiento: cuando está habilitado, el recorrido se convierte en candidato y el modelo evalúa y recomienda el recorrido más adecuado para una persona que cumple los requisitos para varios recorridos activos.

   ![Cuadro de diálogo Configuración de control de tráfico de Recorrido con la opción Habilitar control de tráfico de recorrido activada, además de los botones Cancelar y Guardar](./assets/journey-traffic-control-enable-dialog.png){width="450"}

   >[!IMPORTANT]
   >
   >La opción se puede cambiar en cualquier momento mientras el recorrido permanezca en el estado _Borrador_. Después de publicar el recorrido con el control de tráfico de recorrido habilitado, se evalúa la entrada en ese recorrido y ya no puede deshabilitar la configuración.

1. Haga clic en **[!UICONTROL Guardar]**.

1. [Publicar](./create-publish-journey.md#publish-a-journey) el recorrido de la persona.

## Limitaciones y dependencias {#limitations}

Las siguientes dependencias afectan a cuándo y cómo funciona el control de tráfico de recorrido:

* **Sincronización de audiencias**: las decisiones dependen de la pertenencia a audiencias actualizadas sincronizadas de [!DNL Experience Platform] a [!DNL Journey Optimizer B2B Edition]. El tiempo de ejecución sigue a la segmentación y finalización de la sincronización. No es un horario fijo.
* **Actualización de perfil**: una ejecución solo se inicia después de que la actualización de perfil de persona y cuenta se haya realizado correctamente.
* **metadatos de Recorrido**: solo participan los recorridos activos habilitados para el control de tráfico. La calidad de la coincidencia depende de los nombres y las descripciones que escriba.
* **Integridad del perfil**: la calidad depende de la persona, la cuenta y los datos de intención que mantenga. Las dimensiones que faltan se omiten.

El control de tráfico de recorrido tiene las siguientes limitaciones:

* **Un recorrido por cada persona**: Una persona está inscrita en un recorrido como máximo por cada ejecución.
* **La selección no garantiza la inscripción**: hasta que se complete la sincronización de [!DNL Experience Platform], algunos perfiles podrían evaluarse sin un ID de persona de Marketo coincidente. El recorrido está seleccionado, pero es posible que la inscripción no se realice correctamente. Estas personas aparecen como *No inscrito* en el informe de ejecución.
* **Sin inscripción repetida**: el control de tráfico de Recorrido no inscribe a una persona en un recorrido en el que estaba inscrita anteriormente. Para permitir que las personas se vuelvan a calificar para un recorrido, use [configuración de reentrada de recorrido](./journey-re-entry.md).
* **No en tiempo real**: las decisiones se toman cuando se produce una ejecución, no cuando cambia un perfil.
* **Cuatro dimensiones fijas**: puede ajustar la importancia de la industria, el ajuste funcional, el tamaño de la empresa y la intención, pero no puede agregar dimensiones.
* **Coincidencia basada en texto**: los nombres y las descripciones de los Recorridos se comparan con el texto del perfil. Los recorridos con descripciones vagas, vacías o similares son más difíciles de distinguir. Los recorridos débilmente diferenciados pueden producir resultados de baja confianza.

El control de tráfico de recorrido solo decide en qué recorrido apto se inscribe una persona. No cambia los recorridos ni las audiencias.

<!-- CONFIRM with Product and Engineering: the maximum number of governed journeys, maximum audience size for each run, supported editions and regions, and any language limitations for text matching. -->
