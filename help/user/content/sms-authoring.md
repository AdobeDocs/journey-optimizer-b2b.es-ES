---
title: Creación de SMS
description: 'Cree mensajes SMS para recorridos de cuenta con personalización, vínculos y administración de consentimientos: obtenga una vista previa del contenido y configure las opciones de entrega en Journey Optimizer B2B edition.'
feature: SMS Authoring, Content, Channels
role: User
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: 9a97682590d779c8b5f5b385efd912ee1f56ed31
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 3%

---

# Creación de SMS

Utilice Adobe Journey Optimizer B2B edition para enviar mensajes de texto (SMS) a sus clientes en sus dispositivos móviles. Puede crear, personalizar y previsualizar mensajes en formato de texto desde el editor de SMS.

Antes de crear mensajes SMS para recorridos de cuenta, asegúrate de que el [proveedor de servicio SMS está configurado](../admin/configure-channels-sms.md) desde la configuración de _[!UICONTROL Administrador]_.

## Añadir una acción SMS en un recorrido de cuenta

Puede configurar envíos de mensajes de texto en un recorrido de cuentas cuando agregue un nodo _[!UICONTROL Realizar una acción]_ y haga lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.

1. Para la _[!UICONTROL acción sobre personas]_, elige **[!UICONTROL Enviar SMS]**.

   ![Realizar una acción - enviar sms](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. En la parte inferior del panel _[!UICONTROL Realizar una acción]_, haga clic en **[!UICONTROL Crear SMS]**.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único para el mensaje SMS.

   ![Crear nuevo cuadro de diálogo de SMS](assets/create-new-sms.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

   Se abre el _mapa de Recorrido_. Puede crear el mensaje y establecer las propiedades de SMS para enviarlo.

### Creación del mensaje SMS

>[!IMPORTANT]
>
>**Administración de consentimiento de SMS**<br/>
>
>De acuerdo con las normas y regulaciones del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. Se admiten y se respetan todas las palabras clave de inclusión y exclusión estándar. Además, se admiten y respetan todas las palabras clave personalizadas configuradas para la cuenta del proveedor de servicios SMS.

Escriba el texto que desee enviar en el campo **[!UICONTROL Mensaje]**.

Puede crear un mensaje de hasta 1600 caracteres, y considerar cada 160 caracteres como un solo mensaje SMS.

![Escribir el mensaje SMS](./assets/sms-message-compose.png){width="800" zoomable="yes"}

#### Personalización del mensaje de texto

1. Coloque el cursor en la ubicación del mensaje donde desee agregar el token de personalización.

1. Haga clic en el icono _Personalizar_ ( ![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) a la derecha del cuadro de mensaje de texto.

   El cuadro de diálogo proporciona acceso a los tokens de cuenta, tokens de persona y tokens del sistema. Se incluyen tokens estándar y personalizados. Puede usar la barra _Buscar_ para encontrar el token que necesita, o navegar por el árbol de carpetas para buscar y seleccionar cualquiera de los tokens.

1. Agregue un token haciendo clic en el símbolo más ( **+** ) que hay junto a él.

   Si desea agregar el token con una reserva (valor predeterminado que aparece en caso de que el campo no esté disponible para un posible cliente), haga clic en el icono _Más_ ( **...** ) y elija **[!UICONTROL Insertar con texto de reserva]**.

   ![Haga clic en los puntos suspensivos para utilizar una reserva para el token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

1. En el cuadro de diálogo _[!UICONTROL Introducir valor de reserva]_, escriba el texto que aparece como reserva y, a continuación, haga clic en **[!UICONTROL Agregar]**.

   ![Escriba el texto de reserva para el token](./assets/sms-message-personalize-fallback-text.png){width="450"}

1. Cuando se coloquen los tokens de personalización, haga clic en **[!UICONTROL Guardar]** para guardar los cambios y volver al espacio de trabajo principal de creación de SMS.

   Puede seguir editando el mensaje con los tokens según sea necesario.

#### Añadir vínculos (URL) al mensaje de texto

1. Después de escribir el texto del mensaje, haga clic en el icono _Vínculo_ ( ![Icono de vínculo](../assets/do-not-localize/icon-link.svg) ) a la derecha del cuadro de mensaje de texto.

1. Escriba la **[!UICONTROL URL]** para el vínculo.
<!--    
1. In the dialog, choose the type of URLs to link:

   * **[!UICONTROL Landing Page]** - Choose this option to select any of the approved Adobe Marketo Engage landing pages from your Marketo Engage instance. Select the workspace, and then select the landing page.

   * **[!UICONTROL External URL]** - This type is any external URL that you enter in the text box. -->

1. Si decide utilizar una página de aterrizaje de Marketo Engage, configure las opciones de seguimiento.

   * **[!UICONTROL Habilitar seguimiento]** - Seleccione esta casilla de verificación para habilitar el seguimiento, lo que requiere _acortar_ la dirección URL. Para una página de aterrizaje, utiliza el subdominio de Marketo Engage para la URL abreviada. Se muestra un ejemplo del formato de URL abreviado. La dirección URL real se crea cuando se envía el SMS al destinatario.

   * **[!UICONTROL Incluir mkt_tok]** - Seleccione esta casilla de verificación para rastrear la actividad en un usuario.</br>

     >[!NOTE]
     >
     >Cuando permite el seguimiento pero deshabilita _[!UICONTROL Incluir mkt_tok]_, la dirección URL de destino no incluye el parámetro de cadena de consulta `mkt_tok` después del redireccionamiento. Este parámetro lo utilizan las páginas de aterrizaje de Marketo Engage y Munchkin para garantizar que el seguimiento de las actividades personales (como cuando una persona cancela la suscripción de un correo electrónico). No deshabilite esta opción a menos que el parámetro esté causando problemas en el sitio web.<br/>
     >Para obtener más información sobre cómo usar los códigos de seguimiento de Munchkin en tu sitio web, consulta la [documentación de Marketo Engage](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website){target="_blank"}.

   ![Cuadro de diálogo Agregar vínculo para mensaje SMS](./assets/sms-add-link-dialog.png){width="470"}

1. Cuando se hayan completado las opciones del vínculo, haga clic en **[!UICONTROL Agregar]** para guardar los cambios y agregar el vínculo de la dirección URL al mensaje SMS.

### Configuración de las propiedades del SMS

1. En la sección _[!UICONTROL Propiedades de SMS]_, escriba un **[!UICONTROL Nombre]** (obligatorio, máximo de 100 caracteres) y **[!UICONTROL Descripción]** (opcional, máximo de 300 caracteres) para el mensaje.

   Se permiten caracteres Alpha, numéricos y especiales en estos campos. Los siguientes caracteres reservados son **no permitidos**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` y `|`.

1. Elija el **[!UICONTROL tipo de SMS]**:

   * Use `Marketing` para mensajes de texto promocionales, que requieren el consentimiento del usuario.
   * Use `Transactional` para mensajes no comerciales, como confirmaciones de pedidos, notificaciones de restablecimiento de contraseña o información de envío.

1. Para la **[!UICONTROL configuración de SMS]**, elija una de las [configuraciones de API de SMS](../admin/configure-channels-sms.md#create-new-api-credentials-for-an-sms-service-provider) predefinidas.

   Esta configuración determina qué cuenta y proveedor de servicios de puerta de enlace SMS se utiliza para enviar el mensaje.

1. Escriba el **[!UICONTROL número de remitente]** &#x200B;que desee usar para sus comunicaciones.

   ![Propiedades del mensaje SMS](./assets/sms-properties.png){width="500" zoomable="yes"}

   El número de destinatario siempre está asignado al campo `profile.mobilePhone.number` en Experience Platform.

### Simule el contenido del mensaje de texto {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Compruebe cómo se renderiza el contenido"
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

Cuando proporciona esta opción, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. Se admiten y respetan todas las palabras clave de inclusión y exclusión estándar, así como cualquier palabra clave personalizada que se haya configurado con el proveedor de servicios SMS. Al cancelar la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing.

Journey Optimizer B2B edition permite administrar la exclusión en mensajes SMS mediante la siguiente lógica:

* De forma predeterminada, si un posible cliente ha optado por no recibir comunicaciones de su parte, el perfil correspondiente se excluye de los envíos de SMS posteriores

* Este consentimiento de posible cliente proveniente de diferentes fuentes (como AEP o el proveedor de servicios SMS) se sincroniza con Journey Optimizer B2B edition. Actualmente, solo admite un estado de consentimiento único por posible cliente a nivel de instancia (un posible cliente &quot;John Doe&quot; se suscribe o cancela la suscripción a todos los SMS promocionales en la instancia). Actualmente no admite la doble inclusión en el consentimiento a nivel de marca/lista de suscripción individual.
