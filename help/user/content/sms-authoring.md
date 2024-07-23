---
title: Creación de SMS
description: Aprenda a enviar mensajes de texto (SMS) a sus clientes en sus dispositivos móviles y a personalizar y previsualizar mensajes en formato de texto desde el editor de SMS.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e0d9359560f31b3e66f593426c66e64d31044d54
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%

---

# Creación de SMS

Utilice Adobe Journey Optimizer B2B Edition para enviar mensajes de texto (SMS) a sus clientes en sus dispositivos móviles. Puede crear, personalizar y previsualizar mensajes en formato de texto desde el editor de SMS.

## Configuraciones de SMS

Adobe Journey Optimizer B2B Edition envía mensajes de texto a través de proveedores de servicios SMS (o proveedores de pasarela SMS). Antes de crear el mensaje SMS, configure el proveedor de servicios desde la Configuración de administrador.

### Proveedores de servicios de pasarela SMS

Adobe Journey Optimizer B2B Edition se integra actualmente con proveedores de terceros que ofrecen servicios de mensajería de texto de forma independiente. Los proveedores admitidos para los mensajes de texto son Sinch, Twilio e Infobip.

Antes de configurar un canal SMS en Adobe Journey Optimizer B2B Edition, debe crear una cuenta con uno de estos proveedores para obtener el token de API y el ID de servicio. Estas credenciales son necesarias para configurar la conexión entre Adobe Journey Optimizer B2B Edition y el proveedor aplicable.

>[!IMPORTANT]
>
>El uso de los servicios de mensajería de texto está sujeto a términos y condiciones adicionales del proveedor correspondiente. Como soluciones de terceros, Sinch, Twilio e Infobip están disponibles para los usuarios de Adobe Journey Optimizer B2B Edition a través de una integración. El Adobe no controla y no es responsable de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con los servicios de mensajería de texto (SMS), póngase en contacto con su proveedor.

### Verificar una configuración de API de SMS existente

>[!NOTE]
>
>Los ajustes descritos solo son accesibles para los usuarios con privilegios de administrador de SMS.

En el panel de navegación izquierdo, expanda la sección **[!UICONTROL Administrador]** y haga clic en **[!UICONTROL Configuración]**.

![Acceder a la configuración de credenciales de API de AMA](./assets/config-sms-api.png){width="800" zoomable="yes"}

La página lista las configuraciones de API disponibles para su instancia. Puede filtrar las credenciales de la API mostradas por el proveedor de servicios SMS o el creador.

![Haga clic en el icono de filtro para filtrar la lista de credenciales de la API](./assets/config-sms-api-filter.png){width="500"}

### Creación de nuevas credenciales de API para un proveedor de servicios SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Para configurar Sinch como su proveedor de SMS con Adobe Journey Optimizer B2B Edition:_

1. En el panel de navegación izquierdo, expanda la sección **[!UICONTROL Administrador]** y haga clic en **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** en la parte superior derecha de la lista _[!UICONTROL Credenciales de API]_.

1. Configure las credenciales de la API de SMS:

   ![Configurar las credenciales de la API de SMS de Sinch](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL Proveedor de SMS]**: elige `Sinch` como proveedor de SMS.

   * **[!UICONTROL Nombre]** - Escriba un nombre para su credencial de API.

   * **[!UICONTROL ID de servicio]** y **[!UICONTROL token de API]**: accede a la página de API desde tu cuenta de Sinch (puedes encontrar tus credenciales en la pestaña SMS).

   Para obtener más información sobre cómo encontrar esta información en tu cuenta de Sinch, consulta la [documentación para desarrolladores de Sinch](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Haga clic en **[!UICONTROL Enviar]** cuando se hayan completado los detalles de configuración de las credenciales de la API.

>[!TAB Twilio]

_Para configurar Twilio como su proveedor de SMS con Adobe Journey Optimizer B2B Edition:_

1. En el panel de navegación izquierdo, expanda la sección **[!UICONTROL Administrador]** y haga clic en **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** en la parte superior derecha de la lista _[!UICONTROL Credenciales de API]_.

1. Configure las credenciales de la API de SMS:

   ![Configurar las credenciales de la API de Twilio SMS](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL Proveedor de SMS]**: elige `Twilio` como proveedor de SMS.

   * **[!UICONTROL Nombre]** - Escriba un nombre para su definición de credencial de API.

   * **[!UICONTROL SID de cuenta]** y **[!UICONTROL token de autenticación]**: acceda al panel _Información de cuenta_ de la página del panel de la consola de Twilio para encontrar sus credenciales.

   Para obtener más información acerca de cómo encontrar esta información para su cuenta de Twilio, consulte el [Centro de ayuda de Twilio](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Haga clic en **[!UICONTROL Enviar]** en la parte superior derecha de la página cuando se hayan completado los detalles de configuración de las credenciales de la API.

>[!TAB Infobip]

_Para configurar Infobip como su proveedor de SMS con Adobe Journey Optimizer B2B Edition:_

1. En el panel de navegación izquierdo, expanda la sección **[!UICONTROL Administrador]** y haga clic en **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** en la parte superior derecha de la lista _[!UICONTROL Credenciales de API]_.

1. Configure las credenciales de la API de SMS:

   ![Configurar las credenciales de la API de SMS de Infobip](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL Proveedor de SMS]**: elige `Infobip` como proveedor de SMS.

   * **[!UICONTROL Nombre]** - Escriba un nombre para su definición de credencial de API.

   * **[!UICONTROL URL base de API]** y **[!UICONTROL clave de API]**: accede a la página de inicio de la interfaz web o a la página de administración de claves de API de tu cuenta de Infobip para encontrar tus credenciales.

   Para obtener más información acerca de cómo encontrar esta información para su cuenta de Infobip, consulte la [documentación de Infobip](https://www.infobip.com/docs/api/_blank).

1. Haga clic en **[!UICONTROL Enviar]** en la parte superior derecha de la página cuando se hayan completado los detalles de configuración de las credenciales de la API.

>[!ENDTABS]

Al hacer clic en _[!UICONTROL Enviar]_, las credenciales se validan y guardan inmediatamente, lo que le redirige a la página del listado de _[!UICONTROL credenciales de la API]_. Si las credenciales enviadas no son válidas, el sistema muestra un mensaje de error en la página del listado. En este caso, puede optar por cancelar la configuración o actualizarla y enviarla de nuevo.

## Añadir una acción SMS en un recorrido de cuenta

Puede configurar envíos de mensajes de texto en un Recorrido de cuentas cuando agregue un nodo _[!UICONTROL Realizar una acción]_ y haga lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.

1. Para la _[!UICONTROL acción sobre personas]_, elige **[!UICONTROL Enviar SMS]**.

   ![Realizar una acción - enviar sms](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. En la parte inferior del panel _[!UICONTROL Realizar una acción]_, haga clic en **[!UICONTROL Crear SMS]**.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único para el correo electrónico y una **[!UICONTROL Línea de asunto]**.

   ![Crear nuevo cuadro de diálogo de SMS](assets/create-new-sms.png){width="500"}

## Creación del mensaje SMS

>[!IMPORTANT]
>
>**Administración de consentimiento de SMS**<br/>
><br/>
>De acuerdo con las normas y regulaciones del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. Se admiten y se respetan todas las palabras clave de inclusión y exclusión estándar. Además, se admiten y respetan todas las palabras clave personalizadas configuradas para la cuenta del proveedor de servicios SMS.

1. Escriba el texto que desee enviar en el campo **[!UICONTROL Mensaje]**.

   Puede crear un mensaje de hasta 1600 caracteres, y considerar cada 160 caracteres como un solo mensaje SMS.

1. **Personalice el mensaje de texto**.

   En cualquier momento durante la creación del mensaje de texto, haga clic en el icono _Personalizar_ a la derecha del cuadro de mensaje de texto.

   ![Haga clic en el icono Personalizar para agregar tokens al mensaje](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   La página mostrada proporciona acceso a los tokens de cliente potencial y de sistema de Adobe Marketo Engage. Se incluyen tokens estándar y personalizados. Puede utilizar la barra de búsqueda para localizar el token que necesita o navegar por el árbol de carpetas para buscar y seleccionar cualquiera de los tokens de cliente potencial/sistema.

   Coloque el cursor en la ubicación del mensaje donde desee agregar el token. Agregue un token haciendo clic en el símbolo más ( **+** ) que hay junto a él. Si desea agregar el token con una reserva (valor predeterminado que aparece en caso de que el campo no esté disponible para un posible cliente), haga clic en los puntos suspensivos ( **...** ) y elija **[!UICONTROL Insertar con texto de reserva]**.

   ![Haga clic en los puntos suspensivos para utilizar una reserva para el token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

   En el cuadro de diálogo _[!UICONTROL Introducir valor de reserva]_, escriba el texto que aparece como reserva y, a continuación, haga clic en **[!UICONTROL Agregar]**.

   ![Escriba el texto de reserva para el token](./assets/sms-message-personalize-fallback-text.png){width="400"}

   Cuando se coloquen los tokens de personalización, haga clic en **[!UICONTROL Guardar]** para guardar los cambios y volver al espacio de trabajo principal de creación de SMS. Puede seguir editando el mensaje con los tokens según sea necesario.

<!-- 1. **Add URLs to text message**.

   After defining your content, you can add URLs to your message by clicking the _Link_ icon.
   
   You can add two types of URLs: 

   External URLs - This is ANY external URL that can be directly typed into/ pasted into the input text box
   Adobe Marketo Engage Design Studio Landing Pages - Selecting this option, you will see a 'Landing Page picker' from which you can select any of the listed approved Landing Pages from Marketo Engage

   You can choose to 'shorten' either of these URLs by selecting the checkbox
   Note that the URL shortening function, uses the Marketo subdomain for shortening
   The shortened URL appears as a read-only field within the modal
   You can optionally track clicks on the URL
   You can also choose to include 'mkt_tok' for tracking activity against a user
   Click on Add to save changes & add the chosen URL to the SMS message
-->

## Configuración de las propiedades del SMS

1. En la sección _[!UICONTROL Propiedades de SMS]_, escriba un **[!UICONTROL Nombre]** (obligatorio, máximo de 100 cha\racter) y **[!UICONTROL Descripción]** (opcional, máximo de 300 caracteres) para el mensaje.

   Se permiten caracteres Alpha, numéricos y especiales en estos campos. Los siguientes caracteres reservados son **no permitidos**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` y `|`.

1. Elija el **[!UICONTROL tipo de SMS]**:

   * Use `Marketing` para mensajes de texto promocionales, que requieren el consentimiento del usuario.
   * Use `Transactional` para mensajes no comerciales, como confirmaciones de pedidos, notificaciones de restablecimiento de contraseña o información de envío.

1. Para **[!UICONTROL configuración de SMS]**, elija una de las configuraciones de API predefinidas.

   Esta configuración determina qué cuenta y proveedor de servicios de puerta de enlace SMS se utiliza para enviar el mensaje.

1. Escriba el **[!UICONTROL número de remitente]** &#x200B;que desee usar para sus comunicaciones.

   ![Realizar una acción - enviar sms](./assets/sms-properties.png){width="700" zoomable="yes"}

   El número de destinatario siempre está asignado al campo `Lead.MainPhone` del Marketo Engage.

<!-- ## Preview the text message content

When your message content is defined, you can use test profiles to preview its content. If you inserted personalized content, you can check how this content is displayed in the message, using test profile data.

1. Click **[!UICONTROL Simulate Content]** at the top of the SMS authoring workspace.

1. From the _[!UICONTROL Simulate Content]_ page, click **[!UICONTROL Add People]**.

1. Use the # page to manage the leads used for your test profile.

   In the displayed list, you can search for and add any of the leads (up to 10 leads at a time) from the Marketo Engage lead database.

   To search, enter the whole email address and click enter. The corresponding lead profile shows up for selection.

   The preview updated to the personalization fields for the selected profile.

   All the added leads appear on the left rail of the 'Simulate Content' page

   You can manage this list by adding more people and deleting individual leads from the profile listing (it does not remove them from the database).

1. Simulate content for a lead.

   Select any of the leads listed on the left rail of the Simulate Content page and the SMS preview on the page updates for the corresponding lead.

   You can also select a lead from the 'drop-down' box above the preview space and the SMS preview on the page updates for the corresponding lead

1. To exit the _[!UICONTROL Simulate Content]_ page and return back to the SMS authoring workspace, click Close. -->
