---
title: Configuraciones de canal de correo electrónico
description: Configure las opciones de entrega de correo electrónico, los límites de comunicación y los protocolos de autenticación para optimizar la entrega en Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
exl-id: fb16b5e5-f1a5-4e59-b8c6-56985f03225a
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 0%

---

# Configuraciones de canal de correo electrónico

Adobe Journey Optimizer B2B edition aprovecha las funciones de canal y el seguimiento de eventos en Marketo Engage. Los administradores deben asegurarse de que las configuraciones de entrega y seguimiento estén implementadas para habilitar la entrega a través del canal para los especialistas en marketing. Para obtener información sobre los protocolos necesarios para la entrega y el seguimiento de correo electrónico mediante Marketo Engage, consulte [Protocolos para el seguimiento y la entrega de correo electrónico](../start/email-protocols.md).

## Configuración de envío

La configuración de correo electrónico predeterminada se utiliza cuando los especialistas en marketing crean un correo electrónico en un recorrido de cuenta. Para revisar la configuración de envío de correo electrónico, ve a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**. En _[!UICONTROL Correo electrónico]_ en el panel de navegación, seleccione **[!UICONTROL Configuración de envío]**.

![Acceder a la configuración de envío de correo electrónico](./assets/config-email-delivery-email-header.png){width="800" zoomable="yes"}

La configuración es de solo lectura en Journey Optimizer B2B edition. Haga clic en **[!UICONTROL Editar configuración]** en la parte superior derecha para acceder a las opciones de configuración de la instancia de Marketo Engage conectada.

>[!NOTE]
>
>Para acceder y editar esta configuración en Adobe Marketo Engage, debe tener permisos de administrador de productos.

Seleccione cada una de las siguientes pestañas para revisar la configuración actual.

### [!UICONTROL Parámetros de encabezado de correo electrónico] {#email-header}

Los parámetros de encabezado del correo electrónico definen los valores predeterminados para lo siguiente:

* **[!UICONTROL De correo electrónico]** - La dirección de correo electrónico que aparece en el campo _De_ del encabezado del correo electrónico.

* **[!UICONTROL Etiqueta de origen]**: nombre mostrado para la dirección del remitente del correo electrónico.

* **[!UICONTROL Cancelar la suscripción a HTML]**: HTML (para clientes de correo electrónico admitidos) que se muestra en correos electrónicos no operativos para explicar las acciones de cancelación de suscripción al destinatario. Este texto y los vínculos se anexan a la parte inferior.

* **[!UICONTROL Texto para cancelar la suscripción]**: texto sin formato que se muestra en correos electrónicos que no funcionan para explicar las acciones de cancelación de suscripción al destinatario. Este texto y los vínculos se anexan a la parte inferior.

* **[!UICONTROL Ver como página web HTML]**: HTML (para clientes de correo electrónico admitidos) utilizó para _Ver como página web_, que proporciona un vínculo para mostrar un correo electrónico en un explorador.

* **[!UICONTROL Ver como texto de página web]**: texto sin formato utilizado para _Ver como página web_, que proporciona un vínculo para mostrar un correo electrónico en un explorador.

### [!UICONTROL Dominios de marca] {#branding-domains}

Para revisar los dominios de personalización de marca, haga clic en la ficha **[!UICONTROL Dominios de personalización de marca]**.

![Acceder a la configuración de dominios de personalización de marca](./assets/config-email-delivery-branding-domains.png){width="700" zoomable="yes"}

Esta configuración define el dominio principal de uno o varios espacios de trabajo en la instancia de Marketo Engage conectada. Los nuevos correos electrónicos usan este dominio como predeterminado, pero los especialistas en marketing pueden [anularlo por correo electrónico](../content/add-email.md#define-the-email-settings). Para obtener más información sobre cómo definir el dominio de personalización de marca predeterminado, consulte la [documentación de Marketo Engage](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain){target="_blank"}.

>[!NOTE]
>
>Si está comercializando varias marcas y desea que cada una tenga sus propios vínculos de seguimiento de marca, puede agregar un dominio de marca adicional. Para obtener más información sobre cómo agregar varios dominios de promoción de la marca, consulte la [documentación de Marketo Engage](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain){target="_blank"}.

### [!UICONTROL Opciones de encabezado personalizado] {#custom-header-options}

Para revisar las opciones de encabezado personalizado, haga clic en la ficha **[!UICONTROL Opciones de encabezado personalizadas]**.

![Acceder a las opciones de encabezado personalizado](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

Cuando _[!UICONTROL Strict Transport Security]_ está habilitado, garantiza que los vínculos de seguimiento se proporcionen a través de HTTPS (solo para suscripciones con vínculos de seguimiento protegidos por SSL).

## Límites de comunicación

Los límites de comunicación controlan la cantidad de correo electrónico que envía su organización. Se recomienda establecer límites para que no sobrecargue a los destinatarios con demasiados correos electrónicos de su organización.

Para revisar la configuración actual, ve a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**. En _[!UICONTROL Correo electrónico]_ en el panel de navegación, seleccione **[!UICONTROL Límites de comunicación]**.

![Acceder a la configuración de límites de comunicación](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

La configuración es de solo lectura en Journey Optimizer B2B edition. Haga clic en **[!UICONTROL Editar configuración]** en la parte superior derecha para acceder a las opciones de configuración de la instancia de Marketo Engage conectada.

>[!NOTE]
>
>Para acceder y editar esta configuración en Adobe Marketo Engage, debe tener permisos de administrador de productos.

Para obtener más información sobre cómo configurar los límites de comunicación, consulte la [documentación de Marketo Engage](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits){target="_blank"}.

## SPF/DKIM

Mejore las tasas de envío de correo electrónico incorporando SPF (Marco de Política del Remitente) y DKIM (Domain Keys Identified Mail) en la configuración DNS. Estas tecnologías garantizan a los destinatarios que los correos electrónicos no son spam. Para evitar que los filtros de correo no deseado de los destinatarios rechacen correos electrónicos, asegúrese de que SPF y DKIM estén configurados para sus dominios.

Para revisar la configuración actual, ve a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**. En _[!UICONTROL Correo electrónico]_ en el panel de navegación, seleccione **[!UICONTROL SPF/DKIM]**.

![Acceder a la configuración de SPF/DKIM](./assets/config-email-spf-dkim.png){width="700" zoomable="yes"}

La configuración es de solo lectura en Journey Optimizer B2B edition. Haga clic en **[!UICONTROL Editar configuración]** en la parte superior derecha para acceder a las opciones de configuración de la instancia de Marketo Engage conectada.

>[!NOTE]
>
>Para acceder y editar esta configuración en Adobe Marketo Engage, debe tener permisos de administrador de productos.

### Configuración de SPF

El administrador de red debe agregar la siguiente línea a las entradas DNS:

`[domain] IN TXT v=spf1 mx ip4:[corpIP] include:mktomail.com ~all`

En esta entrada, reemplace `[domain]` por el dominio principal del sitio web (como `company.com`) y `[corpIP]` por la dirección IP del servidor de correo electrónico corporativo (como `255.255.255.255`). Si envía correos electrónicos desde varios dominios a través de Marketo Engage, agregue esta entrada para cada dominio en una sola línea.

Si ya tiene un registro SPF en la entrada DNS, agréguele lo siguiente:

`include:mktomail.com`

### Configuración de DKIM

DKIM es un protocolo de autenticación que utilizan los receptores de correo electrónico para validar el remitente del mensaje. A menudo mejora la capacidad de entrega de correos electrónicos a la bandeja de entrada porque un destinatario puede estar seguro de que el mensaje no es una falsificación.

Cuando tiene la clave pública en el registro DNS y el dominio de envío activado en la instancia de Marketo Engage conectada, se utiliza la firma personalizada de DKIM para los mensajes salientes. La firma personalizada de DKIM incluye una firma digital cifrada con cada correo electrónico que se envía. Los receptores pueden descifrar la firma digital buscando la _clave pública_ en el DNS del dominio de envío. Si la clave del correo electrónico corresponde a la clave del registro DNS, es más probable que el servidor de correo receptor acepte el correo electrónico enviado a través de Marketo Engage.

Para obtener más información sobre cómo configurar una firma de DKIM personalizada para el envío por correo electrónico, consulte la [documentación de Marketo Engage](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}.

## Actividad de bots

La actividad de bots de correo electrónico puede inflar erróneamente los datos de aperturas de correos electrónicos y clics.

Marketo Engage utiliza dos métodos para confirmar la actividad de bots:

* **Coincidir con la lista Interactive Advertising Bureau (IAB)**: las actividades que coinciden con cualquier elemento de la lista IAB UA/IP (agente de usuario/dirección IP) están marcadas como bots.

* **Coincidencia con el patrón de proximidad**: cuando ocurren dos o más actividades al mismo tiempo (en un segundo), se identifican como bots. Este método tiene en cuenta los siguientes atributos para la comparación:

   * ID de posible cliente (debe ser el mismo)
   * Recurso de correo electrónico (debe ser el mismo)
   * Clic en vínculo o correo electrónico abierto
   * Diferencia horaria (debe ser inferior a un segundo)

Para las actividades de clic en vínculo de correo electrónico y de apertura de correo electrónico, los nuevos atributos se rellenan con los siguientes valores:

* Las actividades identificadas como bots tienen _Actividad de bots_ como `True` y _Patrón de actividad de bots_ como patrón/método identificado.
* Las actividades que se han identificado como no bots tienen _Actividad de bots_ como `False` y _Patrón de actividad de bots_ como `N/A`.
* Las actividades que suceden antes de que se introduzcan los atributos tienen _Actividad de bots_ vacía (nula) y _Patrón de actividad de bots_ vacío (nulo)

Para revisar la configuración actual, ve a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**. En _[!UICONTROL Correo electrónico]_ en el panel de navegación, seleccione **[!UICONTROL Actividad de bots]**.

![Acceda a la configuración de actividad de bots para la entrega de correo electrónico](./assets/config-email-bot-activity.png){width="700" zoomable="yes"}

La configuración es de solo lectura en Journey Optimizer B2B edition. Haga clic en **[!UICONTROL Editar configuración]** en la parte superior derecha para acceder a las opciones de configuración de la instancia de Marketo Engage conectada.

>[!NOTE]
>
>Para acceder y editar esta configuración en Adobe Marketo Engage, debe tener permisos de administrador de productos.

Para obtener más información sobre cómo configurar las opciones de actividad de bots, consulte la [documentación de Marketo Engage](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type){target="_blank"}.
