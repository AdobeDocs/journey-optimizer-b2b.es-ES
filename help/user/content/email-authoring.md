---
title: Creación de correo electrónico
description: Obtenga información sobre cómo crear contenido de correo electrónico personalizado que se utiliza en un Recorrido de cuentas.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '1428'
ht-degree: 10%

---

# Creación de correo electrónico

Utilice Adobe Journey Optimizer B2B edition para enviar mensajes de correo electrónico a sus clientes. Puede crear, personalizar y obtener una vista previa de los mensajes en el diseñador visual.

## Añadir una acción de correo electrónico en un recorrido de cuenta

Puede configurar los envíos de correo electrónico en un Recorrido de cuentas cuando agregue un nodo _[!UICONTROL Realizar una acción]_ y hacer lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.
1. Para la _[!UICONTROL acción sobre personas]_, elige **[!UICONTROL Enviar correo electrónico]**.
1. Para el _[!UICONTROL origen del correo electrónico]_, elija **[!UICONTROL Crear nuevo correo electrónico]**.

   También puede seleccionar la opción _[!UICONTROL Seleccionar correo electrónico de Adobe Marketo Engage]_ para usar uno de los correos electrónicos creados previamente en Marketo Engage y enviarlo como parte del Recorrido de cuentas.

   >[!NOTE]
   >
   >Si crea un correo electrónico por primera vez, asegúrese de que el canal de correo electrónico esté configurado desde Adobe Marketo Engage. Para obtener más información, consulte [Garantizar la entrega de correos electrónicos](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) en la documentación del Marketo Engage.

   ![Realizar una acción: enviar un correo electrónico](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. En la parte inferior del panel _[!UICONTROL Realizar una acción]_, haga clic en **[!UICONTROL Crear correo electrónico]**.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único para el correo electrónico y una **[!UICONTROL Línea de asunto]**.

   ![Crear nuevo cuadro de diálogo de correo electrónico](assets/create-new-email.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

   En la sección _[!UICONTROL Propiedades de correo electrónico]_ de la página de contenido de correo electrónico, los campos _[!UICONTROL De correo electrónico]_ y _[!UICONTROL Responder a dirección]_ ya están configurados. Puede escribir valores para los campos _[!UICONTROL Nombre del formulario]_ y _[!UICONTROL Descripción]_ (opcional).

## Creación de contenido de correo electrónico

Haga clic en **[!UICONTROL Agregar contenido de correo electrónico]** en la parte superior del panel de vista previa de _[!UICONTROL Correo electrónico]_.

![Haga clic en Agregar contenido de correo electrónico ](./assets/add-email-content.png){width="700" zoomable="yes"}

Esta acción inicia el Designer de correo electrónico, donde puede elegir cómo desea diseñar el correo electrónico entre las siguientes opciones:

* [Diseñe su correo electrónico desde cero](#design-your-email-from-scratch) mediante la interfaz de Designer de correo electrónico.

* [Importe contenido existente del HTML](#import-existing-html-content) desde un archivo o una carpeta .zip.

* [Seleccione una plantilla existente](#select-a-template) de una lista de plantillas de correo electrónico integradas o personalizadas.

Para configurar y personalizar la línea de asunto con el editor de expresiones, haga clic en el icono _Personalization_ y agregue cualquiera de los tokens de Marketo Engage.

Después de crear y personalizar el contenido del correo electrónico, puede exportarlo para su validación o uso posterior. Haga clic en **[!UICONTROL HTML de exportación]** para guardar el contenido como archivo .zip que incluye el HTML y los recursos.

>[!TIP]
>
>Utilice el asistente de IA en Adobe Journey Optimizer B2B edition, con tecnología de IA generativa, para elevar el contenido al siguiente nivel. El asistente de IA puede ayudarle a optimizar el impacto de sus envíos generando correos electrónicos completos, contenido de texto de destino y obteniendo recomendaciones del asistente de IA para imágenes que resuenen con su audiencia. [Más información](./ai-assistant-emails.md)

### Diseñe el correo electrónico desde cero {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño de la página de aterrizaje. Arrastre y suelte un componente **Estructura** en el lienzo para empezar a diseñar el contenido de la página de aterrizaje."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de una página de aterrizaje."

Utilice el editor de contenido visual para definir la estructura del contenido del correo electrónico. Al agregar y mover componentes estructurales con sencillas acciones de arrastrar y soltar, puede diseñar la forma del contenido del correo electrónico reutilizable en cuestión de segundos.

1. En la página de inicio de _[!UICONTROL Diseña tu plantilla]_, selecciona la opción **[!UICONTROL Diseñar desde cero]**.

1. [Agregar estructura y contenido](#add-structure-and-content) al mensaje de correo electrónico.
1. [Agregar recursos de imagen](#add-assets) al mensaje de correo electrónico.
1. [Personalizar el contenido del correo electrónico](#personalize-content).
1. [Revisar y actualizar vínculos](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Cuando finalice el contenido, haga clic en **[!UICONTROL Simular contenido]** en la parte superior para comprobar la renderización. Puede elegir la vista de escritorio o la vista móvil.

Cuando esté satisfecho con el contenido, haga clic en **[!UICONTROL Guardar]**.

### Importación de contenido de HTML existente

{{$include /help/_includes/content-design-import.md}}

![importar contenido html en un archivo zip](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>El uso de una etiqueta `<table>` como primera capa en un archivo de HTML puede causar la pérdida de estilo, incluida la configuración del fondo y el ancho en la etiqueta de capa superior.

Puede personalizar el contenido importado según sea necesario con las herramientas visuales del editor de correo electrónico.

### Seleccionar una plantilla

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> Las plantillas guardadas pueden tener configuraciones de gobernanza (bloqueo de contenido) aplicadas a uno o varios componentes. El diseñador visual proporciona directrices sobre los componentes bloqueados cuando [crea un correo electrónico a partir de una plantilla controlada](./email-authoring-governance.md).

## Añadir estructura y contenido {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño del correo electrónico. Arrastre y suelte un componente **Estructura** en el lienzo para empezar a diseñar el contenido del correo electrónico."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de un correo electrónico."

{{$include /help/_includes/content-design-components.md}}

### Añadir fragmentos

En el editor de contenido visual, el icono _Fragmentos_ se muestra a la izquierda. En el siguiente ejemplo se describen los pasos para agregar fragmentos al contenido de la plantilla.

1. Para abrir la lista de fragmentos, haga clic en el icono _Fragmentos_.

   Puede hacer lo siguiente:

   * Ordenar el listado.
   * Examine, busque o filtre la lista.
   * Cambiar entre las vistas Miniaturas y Lista.
   * Actualice la lista para reflejar cualquiera de los fragmentos creados recientemente.

   ![Seleccionar un fragmento de la lista](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Arrastre y suelte cualquiera de los fragmentos en el marcador de posición del componente estructural.

   El editor procesa el fragmento dentro de la sección o el elemento de la estructura de correo electrónico.

El contenido del fragmento se actualiza dinámicamente dentro de la estructura para mostrar cómo aparece el contenido en el correo electrónico.

>[!TIP]
>
>Para agregar el fragmento de modo que ocupe todo el diseño horizontal dentro del correo electrónico, agregue una estructura de columna 1:1 y, a continuación, arrastre y suelte el fragmento en él.

Una vez guardado el correo electrónico, aparecerá en la página de detalles del fragmento al seleccionar la pestaña _[!UICONTROL Utilizado por]_ en el resumen. Los fragmentos agregados a una plantilla de correo electrónico no se pueden editar dentro de la plantilla: el fragmento de origen define el contenido.

### Añadir recursos

{{$include /help/_includes/content-design-assets.md}}

### Desplazamiento por las capas, la configuración y los estilos

{{$include /help/_includes/content-design-navigation.md}}

### Personalizar contenido

{{$include /help/_includes/content-design-personalization.md}}

### Editar seguimiento de URL vinculadas

{{$include /help/_includes/content-design-links.md}}

### Ver opciones

Aproveche las opciones de vista y validación de contenido disponibles en el editor de correo electrónico visual.

* Acercar/alejar el contenido en las opciones de zoom preestablecidas.

* Cambie la visualización del contenido en Escritorio, Móvil o Solo texto/Texto sin formato.
   * Haz clic en el icono _Ver_ para obtener una vista previa del contenido entre dispositivos.
   * Seleccione uno de los dispositivos predeterminados o introduzca dimensiones personalizadas para obtener una vista previa del contenido.

### Más opciones

En el menú _[!UICONTROL Más...]_ de la parte superior del diseñador de correo electrónico, puede realizar las siguientes acciones:

![Haga clic en Más para acceder a las acciones de plantilla](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL Restablecer correo electrónico]**: haga clic en esta opción para borrar el lienzo del diseñador de correo electrónico visual de una pizarra en blanco y reiniciar la creación del contenido.
* **[!UICONTROL Guardar como fragmento]**: guarde todo o parte del correo electrónico como un fragmento para reutilizarlo en varios correos electrónicos o plantillas de correo electrónico. Proporcione un nombre y una descripción para el fragmento y guárdelo en la lista de fragmentos disponibles.
* **[!UICONTROL Cambia tu diseño]** - Vuelve a la página _Diseña tu correo electrónico_. Desde allí, puede elegir otra plantilla para reiniciar el proceso de diseño o elegir diseñar el contenido desde cero en un lienzo negro.\
* **[!UICONTROL Guardar como plantilla de contenido]** - Guarde el cuerpo del correo electrónico como una plantilla de correo electrónico para reutilizarla en varios correos electrónicos o plantillas de correo electrónico. Proporcione un nombre y una descripción para la plantilla y guárdela en la lista de plantillas de correo electrónico guardadas.
* **[!UICONTROL HTML de exportación]**: descargue el contenido del lienzo visual en su sistema local en formato de HTML empaquetado como archivo zip.

## Comprobación de alertas

Al diseñar el contenido del mensaje de correo electrónico, se muestran alertas en la interfaz (parte superior derecha de la página) cuando falta la configuración clave.

Si no ve este botón, no se detectan problemas.

Se pueden detectar dos tipos de alertas:

* **_Advertencias_** que hacen referencia a recomendaciones y prácticas recomendadas, como:

   * `The opt-out link is not present in the email body`: se recomienda agregar un vínculo para darse de baja al cuerpo del correo electrónico.

     >[!NOTE]
     >
     >Los mensajes de correo electrónico de estilo marketing deben incluir un vínculo de no participación, que no es necesario para los mensajes transaccionales.

   * `Text version of HTML is empty`: no olvide definir una versión de texto de su cuerpo del correo electrónico, que se utiliza cuando no se puede mostrar el contenido del HTML.

   * `Empty link is present in email body`: compruebe que todos los vínculos del correo electrónico sean correctos.

   * `Email size has exceeded the limit of 100KB`: para una entrega óptima, asegúrese de que el tamaño del correo electrónico no supere los 100 KB.

* **_Errores_** que impiden probar o activar el recorrido o la campaña siempre y cuando no se resuelvan, como:

   * `The subject line is missing`: la línea de asunto del correo electrónico es obligatoria.

   * `The email version of the message is empty`: este error se muestra cuando no se ha configurado el contenido del correo electrónico.

## Compruebe y pruebe el correo electrónico {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Compruebe cómo se representa el contenido"
>abstract="Una vez definido el contenido, puede previsualizarlo y comprobar si el procesamiento es correcto según el canal que utilice."

Cuando se define el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo, enviar pruebas y controlar su renderización en clientes populares de escritorio, móviles y basados en web. Si ha insertado contenido personalizado, puede obtener una vista previa de cómo se muestra este contenido en el mensaje mediante los datos del perfil de prueba.

Para obtener una vista previa del contenido del correo electrónico, haga clic en **[!UICONTROL Simular contenido]** y, a continuación, agregue un perfil de prueba para comprobar el mensaje mediante los datos del perfil de prueba.

![Simule el contenido del correo electrónico para comprobar su diseño](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
