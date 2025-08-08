---
title: Puntuación de la alineación de marca
description: Aprenda a crear, validar y administrar contenido en la marca mediante una puntuación de alineación de marca.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
hide: true
hidefromtoc: true
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: c95323936f48a595a74c469c201b19daf1ee95e5
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 17%

---

# Puntuación de la alineación de marca {#brand-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Selección de la marca"
>abstract="Seleccione su marca para asegurarse de que el contenido se crea de acuerdo con sus directrices, estándares e identidad específicos, manteniendo la coherencia y la integridad de la marca."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Puntuación de la alineación de marca"
>abstract="La puntuación de alineación de su marca mide el grado de cumplimiento de su contenido con las directrices de la marca, lo que garantiza la coherencia en los colores, las fuentes, los logotipos, las imágenes y el estilo de redacción."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors"
>title="Puntuación de colores"
>abstract="Puntuación de colores"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts"
>title="Puntuación de fuentes"
>abstract="Puntuación de fuentes"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos"
>title="Puntuación de logotipos"
>abstract="Puntuación de logotipos"

La evaluación y las puntuaciones de alineación de marca le ayudan a crear, revisar y administrar contenido que se adhiera a las directrices [definidas en la marca seleccionada](./brands-manage-create.md#brand-definitions). Garantiza coherencia en el tono, la mensajería y la identidad visual en todas las campañas de correo electrónico, a la vez que sirve como una comprobación de calidad antes de que el contenido se publique.

>[!AVAILABILITY]
>
>Actualmente, esta funcionalidad está disponible como una versión beta privada, con una disponibilidad progresiva planificada para todos los clientes en futuras versiones.
>
>Se requiere un [acuerdo de usuario](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para poder usar las funciones con tecnología de IA en Adobe Journey Optimizer B2B edition. Para obtener más información, contacte con su representante de Adobe.
>
>Consulte [Permisos relacionados con la marca](./brands-overview.md#brand-related-permissions) para obtener información sobre cómo los administradores de productos pueden habilitar estas características.

## Validar la alineación de marca

Cuando la marca esté bien definida y publicada, evalúe la puntuación de alineación de marca directamente dentro del espacio de diseño del correo electrónico para asegurarse de que el contenido se ajuste a las directrices de la marca:

1. Después de crear el contenido del correo electrónico, haga clic en el icono _Alineación de marca_ ( ![icono de alineación de marca](../assets/do-not-localize/icon-brand-compliance.svg) ) que hay a la derecha para abrir el panel derecho _Alineación de marca_ en el espacio de diseño de correo electrónico.

   La [marca predeterminada](./brands-manage-create.md#default-brand) se selecciona automáticamente.

   ![Acceder a las herramientas de alineación de marca](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Puede hacer clic en el icono _Pantalla completa_ (![icono de pantalla completa](../assets/do-not-localize/icon-full-screen.svg) ) en la parte superior del panel para mostrar las herramientas de alineación de marca en modo de pantalla completa.

1. Si es necesario, haga clic en la flecha de menú **[!UICONTROL Marca]** ( ![Flecha abajo](../assets/do-not-localize/icon-down-menu.svg) ) para elegir otra marca publicada.

1. Haga clic en **[!UICONTROL Evaluar puntuación]** para puntuar la alineación del contenido con la marca seleccionada.

   El sistema evalúa el contenido con respecto a las directrices para la marca seleccionada y muestra la puntuación resultante.

   ![Puntuación de evaluación de alineación de marca](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Revise la evaluación

La puntuación se calcula según las infracciones identificadas en el contenido de correo electrónico evaluado:

* 100 = Perfecto - No se han encontrado infracciones
* 80-99 = Bueno: solo infracciones menores
* 60-79 = Justo - Algunas violaciones significativas
* Menos de 60 = Pobre - Las violaciones importantes requieren atención

Puede revisar los resultados de la evaluación con más detalle para identificar infracciones y mejorar las puntuaciones de alineación de la categoría (_Alta_, _Medium_ y _Baja_), así como los detalles. Para el **[!UICONTROL estilo de escritura]** o **[!UICONTROL contenido visual]**, haga clic en la flecha de _Expandir_ ( ![Expandir flecha](../assets/do-not-localize/icon-expand-right.svg) ) para mostrar los detalles de la evaluación.

![Detalles de evaluación de alineación de marca](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Seleccione cualquier directriz marcada para ver comentarios y sugerencias específicos.

Puede hacer cambios en el contenido y hacer clic en **[!UICONTROL Volver a evaluar puntuación]** para ejecutar otra evaluación y comprobar si hay un resultado mejorado.
