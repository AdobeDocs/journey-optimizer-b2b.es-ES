---
title: Añadir un correo electrónico al Recorrido
description: Aprenda a añadir, definir y optimizar las acciones de correo electrónico en Adobe Journey Optimizer B2B. Mejore los recorridos de su cuenta con comunicaciones por correo electrónico de destino.
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
source-git-commit: 4bbe641305065888a59b3e77357e9b39fa6d402e
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 0%

---

# Añadir un correo electrónico al recorrido

Utilice Adobe Journey Optimizer B2B edition para enviar mensajes de correo electrónico a sus clientes a través de los recorridos de cuenta. Puede elegir crear, personalizar y previsualizar mensajes en el espacio de diseño de correo electrónico. También puede elegir enviar un correo electrónico que ya esté definido en la instancia de Marketo Engage conectada.

>[!NOTE]
>
>Si envía un correo electrónico por primera vez, asegúrese de que el canal de correo electrónico esté configurado desde Adobe Marketo Engage. Para obtener más información, consulte [Protocolos para el seguimiento y la entrega por correo electrónico](../start/email-protocols.md).

## Adición de un nodo de acción de correo electrónico en un recorrido

Puede configurar los envíos de correo electrónico en un recorrido cuando [agregue un nodo _[!UICONTROL Realizar una acción]_](../journeys/action-nodes.md) y hacer lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.

1. Para la _[!UICONTROL acción sobre personas]_, elige **[!UICONTROL Enviar correo electrónico]**.

1. Para el _[!UICONTROL origen del correo electrónico]_, elija el origen del correo electrónico que desea enviar.

   ![Realizar una acción: enviar un correo electrónico](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Elija **[!UICONTROL Crear nuevo correo electrónico]** para crear el correo electrónico de forma nativa en Journey Optimizer B2B edition.

     Esta opción le permite administrar el contenido del correo electrónico de forma nativa en Journey Optimizer B2B edition. Haga clic en **[!UICONTROL Crear correo electrónico]** para abrir el cuadro de diálogo _Crear nuevo correo electrónico_. Puede crear un nuevo recurso de contenido de correo electrónico o duplicar un recurso de contenido de correo electrónico existente.

     +++Nuevo correo electrónico

     Si desea crear un mensaje de correo electrónico utilizando un lienzo vacío o una plantilla de correo electrónico, use la opción _[!UICONTROL Nuevo correo electrónico]_.

      1. En el cuadro de diálogo, elija **[!UICONTROL Nuevo correo electrónico]**.

      1. Escriba un **[!UICONTROL Nombre]** único para el correo electrónico y una **[!UICONTROL Línea de asunto]**.

         ![Crear nuevo cuadro de diálogo de correo electrónico - nuevo correo electrónico](assets/create-new-email.png){width="400"}

      1. Haga clic en **[!UICONTROL Crear]**.

         En la sección _[!UICONTROL Propiedades de correo electrónico]_ de la página de contenido de correo electrónico, los campos _[!UICONTROL De correo electrónico]_ y _[!UICONTROL Responder a dirección]_ ya están configurados. Puede escribir valores para los campos _[!UICONTROL Nombre del formulario]_ y _[!UICONTROL Descripción]_ (opcional).

      1. Haga clic en **[!UICONTROL Editar correo electrónico]** para definir la [configuración](#define-the-email-settings) del correo electrónico y diseñar el [contenido](./email-authoring.md).

     +++

     +++Duplicar correo electrónico existente

     Si desea crear un mensaje de correo electrónico utilizando un mensaje existente del recorrido actual o de otro recorrido, use la opción _[!UICONTROL Duplicar correo electrónico existente]_. Puede realizar cambios en el correo electrónico duplicado según el objetivo para el nodo de recorrido.

      1. En el diálogo _[!UICONTROL Crear nuevo correo electrónico]_, elija **[!UICONTROL Duplicar correo electrónico existente]**.

      1. Para que **[!UICONTROL el correo electrónico existente duplique]**, haga clic en el icono _Selección_ ( ![Icono de Selección](../assets/do-not-localize/icon-email-select.svg) ) y seleccione el correo electrónico que desea duplicar y usar para el nodo de recorrido.

         Puede filtrar la lista de correos electrónicos introduciendo una cadena de texto en el campo de búsqueda para que coincida con el nombre del correo electrónico.

         ![Seleccionar correo electrónico](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

         Seleccione la casilla de verificación del correo electrónico que desea duplicar y haga clic en **[!UICONTROL Seleccionar]**.

      1. Escriba un **[!UICONTROL Nombre]** único para el correo electrónico y una **[!UICONTROL Línea de asunto]**.

         ![Crear nuevo cuadro de diálogo de correo electrónico: duplicar correo electrónico existente](assets/create-new-email-duplicate.png){width="400"}

      1. Haga clic en **[!UICONTROL Crear]**.

         En la sección _[!UICONTROL Propiedades de correo electrónico]_ de la página de contenido de correo electrónico, los campos _[!UICONTROL De correo electrónico]_ y _[!UICONTROL Responder a dirección]_ ya están configurados. Puede escribir valores para los campos _[!UICONTROL Nombre del formulario]_ y _[!UICONTROL Descripción]_ (opcional).

      1. Si es necesario, haz clic en **[!UICONTROL Editar correo electrónico]** para modificar el correo electrónico [configuración](#define-the-email-settings) y el [contenido](./email-authoring.md).

     +++

   * Elija **[!UICONTROL Seleccionar correo electrónico de Adobe Marketo Engage]** para usar uno de los correos electrónicos creados previamente en Marketo Engage y enviarlo como parte del recorrido.

     Si tiene más de un espacio de trabajo disponible en la instancia de Market Engage conectada, seleccione el espacio de trabajo. A continuación, seleccione el correo electrónico aprobado que desea enviar para el nodo de recorrido.

     ![Seleccionar correo electrónico de Marketo Engage](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Con esta opción, el nodo se configura y el contenido del correo electrónico no necesita más definición en el recorrido.

## Definir la configuración de correo electrónico

Con la pestaña **[!UICONTROL Detalles]** seleccionada en el panel _Resumen_ de la derecha, desplácese hacia abajo para ver y definir la configuración de correo electrónico.

![Configuración de correo electrónico](./assets/email-summary-details-settings.png){width="700" zoomable="yes"}

| Opción | Descripción |
| ------ | ----------- |
| [!UICONTROL De nombre] | El nombre del remitente utilizado en el encabezado del correo electrónico. Introduzca el nombre del remitente tal como desea que aparezca al destinatario. Haga clic en el icono _Personalizar_ ( ![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) para usar un token de personalización en el campo. |
| [!UICONTROL Del correo electrónico] | La dirección del remitente utilizada en el encabezado del correo electrónico. El valor predeterminado se rellena desde la [configuración de envío del canal de correo electrónico](../admin/configure-channels-emails.md#delivery-settings). Haga clic en el icono _Personalizar_ ( ![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) para usar un token de personalización en el campo. |
| [!UICONTROL Dirección de respuesta] | La dirección del remitente utilizada en el encabezado del correo electrónico. El valor predeterminado se rellena desde la [configuración de envío del canal de correo electrónico](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL de la etiqueta]). Introduzca la dirección de correo electrónico que desea rellenar si el destinatario utiliza la función de respuesta (puede ser diferente o igual a la dirección del remitente). Haga clic en el icono _Personalizar_ ( ![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) para usar un token de personalización en el campo. |
| [!UICONTROL Línea de asunto] | Texto mostrado en el campo de asunto del correo electrónico. El valor predeterminado se rellena a partir del texto que ingresó en el cuadro de diálogo _[!UICONTROL Crear nuevo correo electrónico]_. Puede cambiar el texto si es necesario. Haga clic en el icono _Personalizar_ (![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) para usar un token de personalización en el campo.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Dominio de marca] | Si tiene más de un [dominio de personalización de marca](../admin/configure-channels-emails.md#branding-domains) definido en el sistema, seleccione el dominio de personalización de marca que se utilizará para enviar el correo electrónico. Utilice un dominio de promoción de la marca específico para enviar correos electrónicos que parezcan provenir de su marca en lugar de la compañía en su conjunto. Crea confianza con la marca, personaliza la experiencia de correo electrónico y aumenta las tasas de apertura y respuesta. |
| [!UICONTROL IP dedicada] | Si tiene más de una dirección IP dedicada definida, seleccione una dirección IP dedicada para utilizar para enviar el correo electrónico. Al utilizar una IP específica para sus programas, puede realizar un seguimiento y una monitorización de la capacidad de entrega de forma más estrecha y responder rápidamente a cualquier cambio en las métricas de entrega. Para obtener más información sobre cómo agregar una IP dedicada para la instancia de Marketo Engage conectada, consulte la [documentación de Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/use-your-dedicated-ip-addresses-to-send-emails){target="_blank"}. |
| Resolución de problemas: es más fácil investigar, comprender y resolver los problemas de entrega. |
| [!UICONTROL Correo electrónico operativo] | Seleccione la casilla de verificación si desea designar el correo electrónico como operativo. Los correos electrónicos operativos se excluyen de las listas de exclusión/cancelación de suscripción y de los límites de comunicación. Seleccione esta opción únicamente cuando el destinatario no pueda considerar que el mensaje de correo electrónico es un mensaje comercial no solicitado (SPAM). |
| [!UICONTROL Incluir vista como página web] | Seleccione la casilla de verificación para incluir un vínculo a una página web que se genera a partir del contenido del mensaje de correo electrónico. Los mensajes de correo electrónico tienen capacidades más limitadas que las páginas web, por lo que son útiles para JavaScript, CSS extendido y formularios. El texto usado para generar el vínculo está configurado en la [configuración de envío del canal de correo electrónico](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL Ver como página web HTML] y [!UICONTROL Ver como texto de página web]). |
| [!UICONTROL Deshabilitar seguimiento de aperturas] | Seleccione la casilla de verificación cuando no desee rastrear la actividad de apertura de correo electrónico. Con la función desactivada, los recuentos de actividades abiertas de correo electrónico solo se incrementan cuando una persona única abre el correo electrónico. Puede [administrar el seguimiento de los vínculos de contenido de correo electrónico](./email-authoring.md#content-authoring---link-tracking) al diseñar el contenido del cuerpo del correo electrónico. |
| [!UICONTROL Encabezado previo] | Seleccione la casilla de verificación para incluir un encabezado previo. Un preencabezado es el texto de resumen corto que se muestra después de la línea de asunto en algunos clientes de correo electrónico. Generalmente proporciona un breve resumen del correo electrónico y, por lo general, es una sola frase. Escriba el texto de resumen en el campo <!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |
| [!UICONTROL Campos usados como direcciones CC] | Si está disponible, seleccione hasta 25 campos de posible cliente o compañía que se hayan configurado en Marketo Engage con el tipo `Email`. |

## Comprobación de alertas

Al diseñar el contenido del mensaje de correo electrónico, se muestran alertas en la interfaz (parte superior derecha de la página) cuando falta la configuración clave. Si no ve este botón, no se detectan problemas.

![Alertas por correo electrónico](./assets/email-alerts.png){width="600" zoomable="yes"}

Se pueden detectar dos tipos de alertas:

* **_Advertencias_** que hacen referencia a recomendaciones y prácticas recomendadas, como:

   * `The opt-out link is not present in the email body`: se recomienda agregar un vínculo para darse de baja al cuerpo del correo electrónico.

     >[!NOTE]
     >
     >Los mensajes de correo electrónico de estilo marketing deben incluir un vínculo de no participación, que no es necesario para los mensajes transaccionales.

   * `Text version of HTML is empty`: no olvide definir una versión de texto de su cuerpo del correo electrónico, que se utiliza cuando no se puede mostrar el contenido de HTML.

   * `Empty link is present in email body`: compruebe que todos los vínculos del correo electrónico sean correctos.

   * `Email size has exceeded the limit of 100KB`: para una entrega óptima, asegúrese de que el tamaño del correo electrónico no supere los 100 KB.

* **_Errores_** que impiden probar o activar el recorrido o la campaña siempre y cuando no se resuelvan, como:

   * `From name is empty`: el campo _De_ del correo electrónico (obligatorio) no está definido.

   * `The subject line is missing`: la línea de asunto del correo electrónico (obligatorio) no está definida.

   * `The email version of the message is empty`: el contenido del correo electrónico no está definido.
