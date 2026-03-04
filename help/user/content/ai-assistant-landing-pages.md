---
title: Asistente de IA para contenido de página de aterrizaje
description: 'Generar contenido de página de aterrizaje con el asistente de IA: cree texto e imágenes de página con sus recursos de referencia y compre la segmentación de funciones de grupo en Journey Optimizer B2B edition.'
feature: Generative AI, Landing Pages, Content
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
topic: Artificial Intelligence
role: User
level: Beginner
exl-id: d1e818fb-7450-4c13-bc6c-24da5fb71285
source-git-commit: ce4df9a2726cf842c088738521b3e5dd88dd768f
workflow-type: tm+mt
source-wordcount: '2659'
ht-degree: 0%

---

# Asistente de IA para contenido de página de aterrizaje {#generative-full-content}

El Asistente de IA para el contenido de páginas de aterrizaje en [!DNL Adobe Journey Optimizer B2B Edition] utiliza las capacidades de generación de contenido de Adobe con tecnología de IA y revoluciona la forma en que los especialistas en marketing crean contenido de página de aterrizaje profesional y coherente con la marca. Con modelos de IA generativos avanzados y una comprensión profunda de las directrices de marca, el asistente de IA genera automáticamente contenido personalizado, atractivo y eficaz. Utiliza su objetivo de marketing y optimiza el contenido para los estilos, diseños, tonos y mucho más descritos de la marca. El asistente de IA hace que la creación y ejecución de campañas y programas sea más intuitiva, sencilla y sencilla. Añadir esta capacidad a los flujos de trabajo le permite ahorrar tiempo, mejorar la eficacia y obtener mejores resultados.

Puede generar experiencias de contenido completas para sus páginas de aterrizaje, incluidos texto e imágenes. Esta sólida funcionalidad le ayuda a crear contenido atractivo y de marca que se conecta con su audiencia.

>[!NOTE]
>
>Esta funcionalidad está disponible en su versión de Beta y sujeta a cambios sin previo aviso.

>[!IMPORTANT]
>
>Para tener acceso a estas características en [!DNL Journey Optimizer B2B Edition], debe tener el permiso _[!UICONTROL Asistente de IA]_ > _[!UICONTROL Generar contenido]_. Para obtener más información sobre cómo un administrador de productos puede conceder permisos de características, consulte [Editar roles para permisos de productos](../admin/user-management.md#edit-roles-for-product-permissions).

## Directrices y limitaciones

Antes de empezar a usar esta capacidad, revise las [directrices y limitaciones](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations). [También se requiere la aceptación del acuerdo de usuario &#x200B;](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} para poder usar las capacidades de IA en [!DNL Journey Optimizer B2B Edition]. Para obtener más información, contacte con su representante de Adobe.

Con el compromiso de Adobe de promover la transparencia en el uso de herramientas de IA generativa en la creación de medios, Adobe aplica [credenciales de contenido](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} para cualquier contenido o proyecto que incluya un recurso generado por Firefly cuando se descarga o exporta.

Las siguientes limitaciones y directrices se aplican a las funciones del Asistente de IA utilizadas para generar contenido de páginas de aterrizaje en [!DNL Journey Optimizer B2B Edition]:

* El inglés es el único idioma admitido.
* El contenido generado puede no ser preciso: comparta sus comentarios para que los ingenieros de Adobe puedan refinar los modelos.
* Puede cargar varios recursos de referencia de contenido, pero solo puede aprovechar uno para una generación específica.
* Utilice una plantilla personalizada o específica de la marca para generar contenido para una página de aterrizaje completa. Se recomiendan plantillas de página de aterrizaje con hasta 8-10 imágenes.
* Asegúrese de informar de cualquier salida problemática mediante los iconos de miniatura hacia arriba, miniatura hacia abajo o indicador al seleccionar variantes generadas.

## Entrada y configuración para la generación de contenido

Puede generar contenido completo para una página de aterrizaje o para componentes seleccionados de la página. Cuando utilice las herramientas del Asistente de IA para generar el contenido que necesita, proporcione la entrada, incluidos los mensajes y el contenido de referencia, y la configuración para texto e imágenes.

### Indicadores

Utilice peticiones de datos bien definidas para que el modelo de IA generativa interprete con precisión. El objetivo/mensaje de marketing que proporcione afecta fuertemente a la calidad del contenido generado.

![Campo de solicitud](./assets/gen-ai-prompt.png){width="320"}

Para obtener más información acerca de cómo crear mensajes efectivos, vea _[Prácticas recomendadas de mensajes](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

>[!BEGINSHADEBOX]

**Biblioteca de mensajes**

Un aviso eficaz es esencial para generar el mejor contenido posible. Si desea ayuda para redactar el mensaje, haga clic en el icono _Biblioteca de mensajes_ ![Icono de biblioteca de mensajes](../assets/do-not-localize/icon-library.svg) para acceder a una biblioteca de ideas de mensajes organizadas según los objetivos. Introduzca texto en el campo de búsqueda para buscar una solicitud basada en una cadena de palabra clave.

![Ayudante de IA: acceda a la biblioteca de mensajes](./assets/gen-ai-prompt-library.png){width="600" zoomable="no"}

Seleccione la solicitud que mejor se ajuste a sus metas y haga clic en **[!UICONTROL Probar esta solicitud]**. En el campo _[!UICONTROL Preguntar]_, reemplace cualquier marcador de posición (como `[Key Feature/Information]`) con los valores necesarios que especifiquen su marca, oferta, campaña y casos de uso.

>[!ENDSHADEBOX]

### Configuración de texto

Expanda **[!UICONTROL Configuración de texto]** en el panel derecho y establezca las opciones para el texto generado.

* **[!UICONTROL Grupo de compra]** - Elige la función de [grupo de compra](../buying-groups/buying-groups-role-templates.md) que se usará para segmentar tu mensaje.
* **[!UICONTROL Fase de recorrido de marketing]**: elige la [fase de grupo de compra](../buying-groups/buying-group-stages.md) que se usará para dirigir los mensajes.
* **[!UICONTROL Estrategia de comunicación]**: elige el estilo de comunicación más adecuado para el texto generado.
* **[!UICONTROL Idioma]**: elige el idioma del contenido generado.
* **[!UICONTROL Tono]**: el tono debería interesar a su audiencia. Por ejemplo, puede ajustar el mensaje para que suene informativo, lúdico o persuasivo.

![Panel de configuración de texto que muestra el grupo de compra, la fase de recorrido de marketing, la estrategia de comunicación, el idioma y las opciones de tono](./assets/gen-ai-text-settings.png){width="350" zoomable="yes"}

Haga clic en la flecha izquierda para volver a la _[!UICONTROL configuración]_ principal.

### Configuración de imagen

Para incluir imágenes en el contenido generado, expanda **[!UICONTROL Configuración de imagen]** en el panel derecho y establezca las opciones.

La opción **[!UICONTROL Generar imágenes mediante IA]** está deshabilitada de manera predeterminada. Active esta función y defina las siguientes opciones para incluir las imágenes generadas en las variaciones de contenido propuestas:

<!-- * **[!UICONTROL Generative model]**: Select from available built-in models, custom Firefly models trained on your brand assets, or third-party image generation providers to create images that align with your specific needs and brand requirements. -->
* **[!UICONTROL Proporción de aspecto]**: cuando se selecciona un componente de imagen, esta configuración determina la anchura y la altura del recurso. Tiene la opción de elegir entre proporciones comunes como 16:9, 4:3, 3:2 o 1:1, o bien puede especificar un tamaño personalizado.
* **[!UICONTROL Tipo de contenido]**: El tipo categoriza la naturaleza del elemento visual, distinguiendo entre diferentes formas de representación visual, como fotografías, gráficos o arte.
* **[!UICONTROL Intensidad visual]**: controla el impacto de la imagen ajustando su intensidad. Un ajuste más bajo (por ejemplo, 2) crea un aspecto más suave y restringido, mientras que un ajuste más alto (por ejemplo, 10) hace que la imagen sea más vibrante y visualmente potente.
* **[!UICONTROL Color y tono]**: El aspecto general de los colores de una imagen y el estado de ánimo o atmósfera que transmite.
* **[!UICONTROL Iluminación]**: estilo de iluminación utilizado para la imagen, que da forma a su atmósfera y resalta elementos específicos.
* **[!UICONTROL Composición]**: La disposición de elementos dentro del marco de una imagen.

![El panel de configuración de imagen muestra las opciones Tipo de contenido, Intensidad visual, Color y tono, Iluminación y Composición](./assets/gen-ai-image-settings.png){width="350" zoomable="yes"}

Haga clic en la flecha izquierda para volver a la _[!UICONTROL configuración]_ principal.

### Contenido de referencia

Cargue recursos de contenido de referencia para generar contenido preciso y de marca. De lo contrario, el contenido generado se basa en información disponible públicamente. El contenido de referencia sirve como fuente para la generación de contenido y las recomendaciones de imágenes. Para obtener instrucciones y prácticas recomendadas, vea _[Contenido de referencia optimizado](../ai-assistant/generative-ai-content.md#reference-content)_.

En la configuración de **[!UICONTROL Contenido de referencia]**, haga clic en **[!UICONTROL Cargar archivo]** para agregar cualquier recurso que contenga contenido que desee usar para contexto adicional.

![Cargar archivo para utilizarlo como contenido de referencia](./assets/gen-ai-reference-content-upload.png){width="350" zoomable="yes"}

El archivo que se va a cargar puede tener los siguientes formatos: PDF, JPEG, PNG o archivos ZIP (con los formatos de archivo compatibles). El tamaño máximo de un recurso de marca cargado es de 50 MB. Pueden funcionar archivos más grandes o un gran número de imágenes, pero esto aumenta el tiempo de procesamiento.

Si desea seleccionar un archivo cargado anteriormente, expanda la lista **[!UICONTROL Contenido de referencia cargado]** y habilite el recurso que desee usar para la generación de contenido.

![Habilitar el contenido de referencia existente para usar](./assets/gen-ai-reference-content-select.png){width="350" zoomable="yes"}

## Uso de las herramientas de IA generativa {#gen-ai-tools}

Para empezar a generar contenido, abra el editor de contenido de la página de aterrizaje y acceda a las herramientas de IA generativa en el carril exterior del panel derecho. Seleccione _AI Assistant_ ( ![AI Assistant para alternar contenido](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) para mostrar las herramientas de generación de contenido disponibles para la selección de contenido actual.

Siga estos pasos según el tipo de generación de contenido de página de aterrizaje que desee utilizar:

>[!BEGINTABS]

>[!TAB Página completa]

Siga estos pasos para utilizar el Asistente de IA para generar una página de aterrizaje completa refinando una plantilla de página de aterrizaje existente:

1. Después de [crear la página de aterrizaje](./landing-pages.md#create-a-landing-page), haga clic en **[!UICONTROL Editar página de aterrizaje]**.

1. Seleccione una plantilla.

   La generación completa de contenido requiere una plantilla. Puede ser una plantilla estándar proporcionada por Adobe o una plantilla guardada. También puede usar la opción _[!UICONTROL Importar HTML]_ para importar una plantilla.

   Para obtener más información acerca de cómo usar una plantilla de página de aterrizaje, vea _[Seleccionar una plantilla guardada o de ejemplo](./landing-pages.md#select-a-saved-or-sample-template)_.

1. En el carril exterior del panel derecho, seleccione el icono _Asistente de IA_ ( ![Asistente de IA para alternar contenido](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ).

   ![Alternar el asistente de IA en el espacio de diseño de la página de aterrizaje](./assets/gen-ai-full-landing-page-ai-panel.png){width="600" zoomable="yes"}

   La configuración del Asistente de IA de la derecha refleja la configuración de generación de la página de aterrizaje completa.

1. (Beta) Seleccione su **[!UICONTROL Marca]** para asegurarse de que el contenido generado por IA se ajuste a las especificaciones de su marca.

   Si no hay marcas publicadas, haga clic en **[!UICONTROL Crear una marca]** para definir las [directrices de marca reutilizables](./brands-overview.md).

1. En el campo **[!UICONTROL Preguntar]**, escriba una descripción de lo que desea generar.

   Use la [Biblioteca de mensajes](#prompt-library) si necesita ayuda para crear un mensaje eficaz.

   ![Asistente de IA: solicitar biblioteca para generar contenido de página de aterrizaje](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Si no tiene experiencia previa para solicitar contenido generado, consulte _[Prácticas recomendadas sobre solicitudes](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

1. Complete la configuración de la guía de contenido para adaptar el contenido generado:

   * [**[!UICONTROL Configuración de texto]**](#text-settings): proporcione instrucciones para el contenido de texto generado.
   * [**[!UICONTROL Configuración de imagen]**](#image-settings): si desea incluir imágenes en el contenido generado, habilite la generación de imágenes y proporcione instrucciones.
   * [**[!UICONTROL Contenido de referencia]**](#reference-content): proporcione el recurso de contenido que sirve como origen para la generación de contenido.

1. Cuando la solicitud y la configuración estén listas, haga clic en **[!UICONTROL Generar]**.

1. Desplácese hacia abajo en el panel Asistente de IA y examine las variaciones generadas para determinar cuál es la mejor opción.

   * Haga clic en el icono _Pantalla completa_ (![Icono de pantalla completa](../assets/do-not-localize/icon-full-screen.svg) ) para abrir el cuadro de diálogo _[!UICONTROL Generar página de aterrizaje]_

   * Si es necesario, usa las [acciones de refinamiento](#refine-a-variation) para ajustar la variación y asegurarte de que cumplan tus requisitos exactos.

   * [Envíe comentarios](#submit-variation-feedback) sobre las variantes generadas haciendo clic en los iconos _Pulgares arriba_, _Pulgares abajo_ o _Marca_ y elija el motivo que mejor resuma sus comentarios.

1. Haga clic en **[!UICONTROL Seleccionar]** para reemplazar el contenido de la plantilla por la variante seleccionada y regresar al espacio de diseño de la página de aterrizaje.

   Puede utilizar las herramientas de edición y formato del lienzo para modificar el contenido generado, así como las opciones _[!UICONTROL Settings]_ y _[!UICONTROL Style]_ de la derecha.

>[!TAB Solo texto]

Siga estos pasos para utilizar el Asistente de IA para refinar o mejorar el contenido de texto de una página de aterrizaje existente:

1. En el espacio de diseño de la página de aterrizaje, seleccione un componente _Texto_ para segmentar el contenido específico.

1. En el carril exterior del panel derecho, seleccione el icono _Asistente de IA_ ( ![Asistente de IA para alternar contenido](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ).

   ![Alternar el asistente de IA en el espacio de diseño de la página de aterrizaje](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   La configuración de la derecha refleja la configuración de generación de contenido para el componente de texto.

1. (Beta) Seleccione su **[!UICONTROL Marca]** para asegurarse de que el contenido generado por IA se ajuste a las especificaciones de su marca.

   Si no hay marcas publicadas, haga clic en **[!UICONTROL Crear una marca]** para [definir las directrices de marca reutilizables](./brands-overview.md).

1. En el campo **[!UICONTROL Preguntar]**, escriba una descripción de lo que desea generar.

   ![Asistente de IA - configuración de texto](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   Use la [Biblioteca de mensajes](#prompt-library) si necesita ayuda para crear un mensaje eficaz.

1. Complete la configuración de la guía de contenido para adaptar el contenido generado:

   * [**[!UICONTROL Configuración de texto]**](#text-settings): proporcione instrucciones para el contenido de texto generado.

   * [**[!UICONTROL Contenido de referencia]**](#reference-content): proporcione los recursos de contenido que sirven como origen para la generación de contenido.

1. Cuando la solicitud y la configuración estén listas, haga clic en **[!UICONTROL Generar]**.

1. Desplácese hacia abajo en el panel Asistente de IA y examine las variaciones generadas para determinar cuál es la mejor opción.

   * Haga clic en el icono _Pantalla completa_ (![Icono de pantalla completa](../assets/do-not-localize/icon-full-screen.svg) ) para abrir el cuadro de diálogo _[!UICONTROL Generar texto]_

   * Si es necesario, usa las [acciones de refinamiento](#refine-a-variation) para ajustar la variación y asegurarte de que cumplan tus requisitos exactos.

   * [Envíe comentarios](#submit-variation-feedback) sobre las variantes generadas haciendo clic en los iconos _Pulgares arriba_, _Pulgares abajo_ o _Marca_ y elija el motivo que mejor resuma sus comentarios.

1. Cuando tenga el contenido que desee, haga clic en **[!UICONTROL Seleccionar]** para reemplazar el texto con la variante seleccionada y volver al espacio de diseño de la página de aterrizaje.

   Puede usar las herramientas de edición y formato del lienzo para modificar el texto, así como las opciones _[!UICONTROL Settings]_ y _[!UICONTROL Style]_ de la derecha.

>[!TAB Solo imagen]

Siga estos pasos para utilizar el Asistente de IA para refinar o mejorar el contenido de la imagen para una página de aterrizaje existente:

1. En el espacio de diseño de la página de aterrizaje, seleccione un componente _Image_ para segmentar el contenido específico.

1. En el carril exterior del panel derecho, seleccione el icono _Asistente de IA_ ( ![Asistente de IA para alternar contenido](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ).

   ![Alternar el asistente de IA en el espacio de diseño de la página de aterrizaje](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   La configuración del Asistente de IA de la derecha refleja la configuración de generación del componente de imagen.

1. (Beta) Seleccione su **[!UICONTROL Marca]** para asegurarse de que el contenido generado por IA se ajuste a las especificaciones de su marca.

   Si no hay marcas publicadas, haga clic en **[!UICONTROL Crear una marca]** para [definir las directrices de marca reutilizables](./brands-overview.md).

1. Escriba una descripción de lo que desea en el campo **[!UICONTROL Preguntar]**.

   ![Asistente de IA - configuración de texto](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   Use la [Biblioteca de mensajes](#prompt-library) si necesita ayuda para crear un mensaje eficaz.

1. Complete la configuración de la guía de contenido para adaptar el contenido generado:

   * [**[!UICONTROL Configuración de imagen]**](#image-settings): si desea incluir imágenes en el contenido generado, habilite la generación de imágenes y proporcione instrucciones.

   * [**[!UICONTROL Contenido de referencia]**](#reference-content): proporcione los recursos de contenido que sirven como origen para la generación de contenido.

1. Cuando esté satisfecho con la solicitud y la configuración, haga clic en **[!UICONTROL Generar]**.

   El asistente de IA procesa la solicitud y genera las imágenes más adecuadas en función del mensaje y otras entradas.

   >[!IMPORTANT]
   >
   >Si no hay imágenes en el contenido de referencia o no hay imágenes relevantes para el mensaje de entrada, la salida está vacía.

1. Examine las variaciones generadas o haga clic en el icono _Pantalla completa_ ( ![icono de pantalla completa](../assets/do-not-localize/icon-full-screen.svg) ) para abrir el cuadro de diálogo _[!UICONTROL Generar imagen]_.

   El cuadro de diálogo proporciona espacio adicional para comparar las variaciones, ajustar la imagen y la configuración del contenido de referencia (si es necesario) y regenerar las variaciones.

   Puede seleccionar una variación y hacer clic en **[!UICONTROL Generar similares]** para generar imágenes adicionales similares a la variante seleccionada. O bien, haz clic en **[!UICONTROL Editar en Adobe Express]** para realizar tus propios cambios en la imagen. Consulte [Acciones rápidas en Adobe Express](./image-edit-adobe-express.md#quick-actions-in-adobe-express) para obtener más información sobre cómo usar Adobe Express para restringir las imágenes.

   ![Vista previa del Asistente de IA de las opciones de variación y refinamiento de texto](./assets/email-designer-ai-assistant-image-refine.png){width="700" zoomable="yes"}

   También puede [enviar comentarios](#submit-variation-feedback) sobre las variaciones generadas.

1. Resalte la imagen que desee y haga clic en **[!UICONTROL Seleccionar]** para reemplazar la imagen o el marcador de posición por el elemento seleccionado y volver al espacio de diseño de la página de aterrizaje.

   Puede usar las herramientas de edición y formato del lienzo para modificar la imagen, así como las opciones _[!UICONTROL Settings]_ y _[!UICONTROL Style]_ de la derecha.

>[!ENDTABS]

## Previsualización y refinamiento de contenido {#refine-finalize}

Después de generar variaciones de contenido, puede ajustar los resultados para asegurarse de que cumplan con sus requisitos exactos. Revise la alineación de la marca, ajuste el tono y el idioma y prepare el contenido para un borrador revisable. También puede enviar comentarios sobre una variación para ayudar a formar al asistente de IA y mejorar el resultado futuro.

### Abrir la vista de pantalla completa

1. Después de la generación inicial del contenido, examine **[!UICONTROL Variaciones]**.

1. Identifique la variación que mejor se ajuste a sus objetivos y haga clic en el icono _Pantalla completa_ ( ![Icono de pantalla completa](../assets/do-not-localize/icon-full-screen.svg) ) para abrir el cuadro de diálogo.

   ![Acceder al cuadro de diálogo Generar](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

1. Cuando esté satisfecho con la variación seleccionada, haga clic en **[!UICONTROL Seleccionar]** para aplicarla al lienzo.

### Refinamiento de una variación

Haga clic en la opción **[!UICONTROL Refinar]** para obtener acceso a características de personalización adicionales para variaciones de texto y páginas de aterrizaje:

* **[!UICONTROL Elaborar]**: el asistente de IA puede ayudarle a ampliar temas específicos y proporcionar detalles adicionales para una mejor comprensión y participación.

* **[!UICONTROL Resumir]**: la información larga puede sobrecargar los visores de la página. Utilice el asistente de IA para condensar los puntos clave en resúmenes claros y concisos que llamen la atención y los animen a leer más.

* **[!UICONTROL Reformular]**: vuelva a escribir el mensaje conservando su significado. Esta opción le ayuda a generar frases alternativas, mejorar el flujo o ajustar el estilo sin cambiar el mensaje principal.

* **[!UICONTROL Use un lenguaje más sencillo]**: simplifique el lenguaje y garantice la claridad y accesibilidad para una audiencia más amplia.

* **[!UICONTROL Traducir]** - Traduzca el texto a otro idioma. (Actualmente, el inglés es el único idioma admitido).

* **[!UICONTROL Cambiar tono]**: ajuste el tono del mensaje para que se ajuste a su estilo de comunicación, por ejemplo, para que sea más cordial, profesional, urgente o inspirador.

* **[!UICONTROL Cambiar estrategia de comunicación]**: modifique el enfoque de mensajería en función de sus objetivos, como crear urgencia o enfatizar atractivo interesante.

<!-- * **[!UICONTROL Use as reference content]** - Select this option to use the variant as the reference content for generating other results. -->

![Refinar el menú que muestra las opciones para refinar el contenido](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

### Enviar comentarios de variación

Proporcione comentarios sobre las variantes generadas haciendo clic en los iconos _Pulgares arriba_, _Pulgares abajo_ o _Marca_ y elija el motivo que mejor resuma sus comentarios.

![Asistente de IA: previsualizar las variaciones generadas](./assets/gen-ai-preview-feedback-thumbs-up.png){width="700" zoomable="yes"}

### Compruebe la alineación de su marca (Beta)

<!-- Are we surfacing scoring here in the future, or will it be a separate post-creation task? 1. Click the percentage icon to view your **[!UICONTROL Brand Alignment Score]** and identify any misalignments with your brand. -->

La evaluación y la puntuación de alineación de marca le ayudan a garantizar la coherencia en el tono, la mensajería y la identidad visual de sus campañas, a la vez que sirven como una comprobación de calidad antes de que el contenido se publique. Cuando finalice el contenido de la página de aterrizaje, haga clic en el icono _Alineación de marca_ ( ![icono de alineación de marca](../assets/do-not-localize/icon-brand-compliance.svg) ) que aparece a la derecha para abrir el panel derecho _Alineación de marca_ en el espacio de diseño de la página de aterrizaje.

![Acceder a las herramientas de alineación de marca](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

Para obtener información detallada, consulte [Validar la alineación de marca](./brand-alignment.md#validate-your-brand-alignment)
