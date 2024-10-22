---
title: Creación de SMS
description: Aprenda a enviar mensajes de texto (SMS) a sus clientes en sus dispositivos móviles y a personalizar y previsualizar mensajes en formato de texto desde el editor de SMS.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e38ec0f128e811fd4ac21c624d9018854b91c78b
workflow-type: tm+mt
source-wordcount: '2041'
ht-degree: 2%

---

# Creación de SMS

Utilice Adobe Journey Optimizer B2B Edition para enviar mensajes de texto (SMS) a sus clientes en sus dispositivos móviles. Puede crear, personalizar y previsualizar mensajes en formato de texto desde el editor de SMS.

## Configuraciones de SMS

Adobe Journey Optimizer B2B Edition envía mensajes de texto a través de proveedores de servicios SMS (o proveedores de pasarela SMS). Antes de crear tu mensaje SMS, configura tu proveedor de servicios desde la configuración de _Administrador_.

### Proveedores de servicios de pasarela SMS

Adobe Journey Optimizer B2B Edition se integra actualmente con proveedores de terceros que ofrecen servicios de mensajería de texto de forma independiente. Los proveedores admitidos para los mensajes de texto son Sinch, Twilio e Infobip.

Antes de configurar un canal SMS en Adobe Journey Optimizer B2B edition, debe crear una cuenta con uno de estos proveedores para obtener el token de API y el ID de servicio. Estas credenciales son necesarias para configurar la conexión entre Adobe Journey Optimizer B2B edition y el proveedor aplicable.

>[!IMPORTANT]
>
>El uso de los servicios de mensajería de texto está sujeto a términos y condiciones adicionales del proveedor correspondiente. Como soluciones de terceros, Sinch, Twilio e Infobip están disponibles para los usuarios de Adobe Journey Optimizer B2B Edition a través de una integración. El Adobe no controla y no es responsable de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con los servicios de mensajería de texto (SMS), póngase en contacto con su proveedor.

### Verificar una configuración de API de SMS existente

>[!NOTE]
>
>Los ajustes descritos solo son accesibles para los usuarios con privilegios de administrador de SMS.

1. En el panel de navegación izquierdo, expanda la sección **[!UICONTROL Administrador]** y haga clic en **[!UICONTROL Canales]**.

   ![Acceder a la configuración de credenciales de API de SMS](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. En el panel de navegación, seleccione **[!UICONTROL Credenciales de API]**.

   La página lista las configuraciones de API disponibles para su instancia.

1. Si es necesario, haga clic en el icono _Filtro_ ( ![Mostrar u ocultar el icono de filtros](../assets/do-not-localize/icon-filter.svg) ) y seleccione las opciones para mostrar la lista de credenciales de API configuradas por el proveedor de servicios SMS o el creador.

   ![Haga clic en el icono Filtro para restringir la lista de credenciales de la API](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

### Creación de nuevas credenciales de API para un proveedor de servicios SMS

>[!BEGINTABS]

>[!TAB Sinch]

_Para configurar Sinch como su proveedor de SMS con Adobe Journey Optimizer B2B edition:_

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

_Para configurar Twilio como su proveedor de SMS con Adobe Journey Optimizer B2B edition:_

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

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único para el mensaje SMS.

   ![Crear nuevo cuadro de diálogo de SMS](assets/create-new-sms.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

   Se abre _el diseñador de contenido de Recorrido_; puede crear el mensaje y establecer las propiedades de SMS para enviarlo.

### Creación del mensaje SMS

>[!IMPORTANT]
>
>**Administración de consentimiento de SMS**<br/>
>
>De acuerdo con las normas y regulaciones del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. Se admiten y se respetan todas las palabras clave de inclusión y exclusión estándar. Además, se admiten y respetan todas las palabras clave personalizadas configuradas para la cuenta del proveedor de servicios SMS.

Escriba el texto que desee enviar en el campo **[!UICONTROL Mensaje]**.

Puede crear un mensaje de hasta 1600 caracteres, y considerar cada 160 caracteres como un solo mensaje SMS.

![Haga clic en el icono Personalizar para agregar tokens al mensaje](./assets/sms-message-compose.png){width="800" zoomable="yes"}

#### Personalización del mensaje de texto

1. En cualquier momento durante la creación del mensaje de texto, haga clic en el icono _Personalizar_ ( ![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) a la derecha del cuadro de mensaje de texto.

   La página mostrada proporciona acceso a los tokens de cliente potencial y de sistema de Adobe Marketo Engage. Se incluyen tokens estándar y personalizados. Puede usar la barra _Buscar_ para encontrar el token que necesita, o navegar por el árbol de carpetas para buscar y seleccionar cualquiera de los tokens de cliente potencial/sistema.

1. Coloque el cursor en la ubicación del mensaje donde desee agregar el token.

1. Agregue un token haciendo clic en el símbolo más ( **+** ) que hay junto a él.

   Si desea agregar el token con una reserva (valor predeterminado que aparece en caso de que el campo no esté disponible para un posible cliente), haga clic en el icono _Más_ ( **...** ) y elija **[!UICONTROL Insertar con texto de reserva]**.

   ![Haga clic en los puntos suspensivos para utilizar una reserva para el token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

1. En el cuadro de diálogo _[!UICONTROL Introducir valor de reserva]_, escriba el texto que aparece como reserva y, a continuación, haga clic en **[!UICONTROL Agregar]**.

   ![Escriba el texto de reserva para el token](./assets/sms-message-personalize-fallback-text.png){width="400"}

1. Cuando se coloquen los tokens de personalización, haga clic en **[!UICONTROL Guardar]** para guardar los cambios y volver al espacio de trabajo principal de creación de SMS.

   Puede seguir editando el mensaje con los tokens según sea necesario.

#### Añadir vínculos (URL) al mensaje de texto

1. Después de escribir el texto del mensaje, haga clic en el icono _Vínculo_ ( ![Icono de vínculo](../assets/do-not-localize/icon-link.svg) ) a la derecha del cuadro de mensaje de texto.

1. En el cuadro de diálogo, elija el tipo de URL que desea vincular:

   * **[!UICONTROL Página de aterrizaje]**: elija esta opción para seleccionar cualquiera de las páginas de aterrizaje de Adobe Marketo Engage Design Studio aprobadas en la instancia de Marketo Engage. Seleccione el espacio de trabajo y, a continuación, la página de aterrizaje.

   * **[!UICONTROL Dirección URL externa]**: este tipo es cualquier dirección URL externa que escriba en el cuadro de texto.

1. Si decide utilizar una página de aterrizaje, defina las opciones de seguimiento.

   * **[!UICONTROL Habilitar seguimiento]** - Seleccione esta casilla de verificación para habilitar el seguimiento, lo que requiere _acortar_ la dirección URL. Para una página de aterrizaje, utiliza el subdominio Marketo Engage para la URL abreviada. Se muestra un ejemplo del formato de URL abreviado. La dirección URL real se crea cuando se envía el SMS al destinatario.

   * **[!UICONTROL Incluir mkt_tok]** - Seleccione esta casilla de verificación para rastrear la actividad en un usuario.

     >[!NOTE]
     >
     >Cuando permite el seguimiento pero deshabilita _[!UICONTROL Incluir mkt_tok]_, la dirección URL de destino no incluye el parámetro de cadena de consulta `mkt_tok` después del redireccionamiento. Este parámetro lo utilizan las páginas de aterrizaje de Marketo Engage y Munchkin para garantizar que el seguimiento de las actividades de la persona (como cuando una persona cancela la suscripción de un correo electrónico). No deshabilite esta opción a menos que el parámetro esté causando problemas en el sitio web.<br/>
     >Para obtener más información sobre el uso de los códigos de seguimiento de Munchkin en el sitio web, consulte la [documentación del Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website){target="_blank"}.

   ![Cuadro de diálogo Agregar vínculo para mensaje SMS](./assets/sms-add-link-dialog.png){width="470"}

1. Cuando se hayan completado las opciones del vínculo, haga clic en **[!UICONTROL Agregar]** para guardar los cambios y agregar el vínculo de la dirección URL al mensaje SMS.

### Configuración de las propiedades del SMS

1. En la sección _[!UICONTROL Propiedades de SMS]_, escriba un **[!UICONTROL Nombre]** (obligatorio, máximo de 100 caracteres) y **[!UICONTROL Descripción]** (opcional, máximo de 300 caracteres) para el mensaje.

   Se permiten caracteres Alpha, numéricos y especiales en estos campos. Los siguientes caracteres reservados son **no permitidos**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` y `|`.

1. Elija el **[!UICONTROL tipo de SMS]**:

   * Use `Marketing` para mensajes de texto promocionales, que requieren el consentimiento del usuario.
   * Use `Transactional` para mensajes no comerciales, como confirmaciones de pedidos, notificaciones de restablecimiento de contraseña o información de envío.

1. Para **[!UICONTROL configuración de SMS]**, elija una de las configuraciones de API predefinidas.

   Esta configuración determina qué cuenta y proveedor de servicios de puerta de enlace SMS se utiliza para enviar el mensaje.

1. Escriba el **[!UICONTROL número de remitente]** &#x200B;que desee usar para sus comunicaciones.

   ![Realizar una acción - enviar sms](./assets/sms-properties.png){width="700" zoomable="yes"}

   El número de destinatario siempre está asignado al campo `Lead.mobilePhone` del Marketo Engage.

### Simule el contenido del mensaje de texto {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Compruebe cómo se procesa el contenido"
>abstract="Una vez definido el contenido, puede previsualizarlo y comprobar el renderizado según el canal que utilice."

Cuando se define el contenido del mensaje, puede utilizar perfiles de prueba para simular (previsualizar) su contenido. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este en el mensaje mediante los datos del perfil de prueba.

>[!IMPORTANT]
>
>Asegúrese de guardar el mensaje SMS antes de simular el mensaje de texto.

1. Haga clic en **[!UICONTROL Simular contenido]** en la parte superior del área de trabajo de creación de SMS.

1. En la página _[!UICONTROL Simular contenido]_, haga clic en **[!UICONTROL Agregar personas]**.

1. Utilice la página _Simular contenido_ para administrar los posibles clientes que se usan en el perfil de prueba.

   En la lista mostrada, puede buscar y agregar cualquiera de los posibles clientes (hasta 10 posibles clientes a la vez) de la base de datos de posibles clientes de Marketo Engage.

   Para buscar, escribe toda la dirección de correo electrónico y presiona _Intro_. Se muestra el perfil de posible cliente correspondiente para la selección.

   La vista previa se actualiza a los campos de personalización del perfil seleccionado.

   Todos los posibles clientes añadidos aparecen a la izquierda.

   Puede administrar esta lista agregando más personas y eliminando posibles clientes individuales de la lista de perfiles (no se eliminan de la base de datos).

1. Simular contenido para un posible cliente seleccionado.

   Seleccione cualquiera de los posibles clientes enumerados a la izquierda. La vista previa de SMS en la página se actualiza para el posible cliente seleccionado.

   También puede seleccionar un posible cliente del selector sobre el espacio de vista previa para actualizar la vista previa del SMS en la página para el posible cliente correspondiente.

1. Para salir de la página _[!UICONTROL Simular contenido]_ y volver al área de trabajo de creación de SMS, haz clic en **[!UICONTROL Cerrar]** en la parte superior derecha.

## Administración de consentimiento de SMS

Proporcionar a los destinatarios la capacidad de cancelar la suscripción a la recepción de comunicaciones de una marca y cumplir con esta opción es un requisito legal. El incumplimiento de estas regulaciones conlleva riesgos legales para su marca. Esta función también le ayuda a evitar enviar comunicaciones no solicitadas a sus destinatarios, lo que podría hacer que marquen sus mensajes como correo no deseado y dañar su reputación.

Cuando proporciona esta opción, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. Se admiten y respetan todas las palabras clave de inclusión y exclusión estándar, así como cualquier palabra clave personalizada que se haya configurado en el proveedor de servicios SMS. Al cancelar la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing.

Journey Optimizer B2B edition permite administrar la exclusión en mensajes SMS mediante la siguiente lógica:

* De forma predeterminada, si un posible cliente ha optado por no recibir comunicaciones de su parte, el perfil correspondiente se excluye de los envíos de SMS posteriores

* Este consentimiento de posible cliente proveniente de diferentes fuentes (como AEP o el proveedor de servicios SMS) se sincroniza con Journey Optimizer B2B Edition. Actualmente, solo admite un estado de consentimiento único por posible cliente a nivel de instancia (un posible cliente &quot;John Doe&quot; se suscribe o cancela la suscripción a todos los SMS promocionales en la instancia). Actualmente no admite la doble inclusión en el consentimiento a nivel de marca/lista de suscripción individual.
