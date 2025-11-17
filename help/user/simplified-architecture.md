---
title: Configuración de arquitectura simplificada
description: Configure Journey Optimizer B2B edition en la arquitectura simplificada. Configure esquemas XDM, canales de correo electrónico/SMS, acciones de recorrido de Marketo Engage y usuarios.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: 3f91b2cc92a1ce42d2c62dcfe7eb9de332116023
workflow-type: tm+mt
source-wordcount: '1385'
ht-degree: 6%

---

# Configuración de arquitectura simplificada

Adobe Journey Optimizer B2B Edition ya está disponible con una arquitectura simplificada. Con esta arquitectura actualizada, Journey Optimizer B2B Edition y Marketo Engage ya no están en el mismo sistema y en el mismo almacén de datos. Journey Optimizer B2B Edition solamente recibe datos de Adobe Experience Platform. Sin embargo, sigue dependiendo de los derechos de Marketo Engage y algunas funciones de configuración para aprovisionar y configurar el sistema.

La arquitectura simplificada es la base que desbloquea las nuevas funciones en Adobe Journey Optimizer B2B edition:

* **Unifique y escale fácilmente sus datos:** La nueva plataforma admite modelos de datos complejos, incluidos objetos personalizados, grupos de compra y eventos de cuenta. 

* **Conectar varias instancias de Adobe Marketo Engage:** Administrar y unificar datos de varios entornos de Adobe Marketo Engage en un solo lugar.

* **Mantiene tus datos seguros:** Funciones avanzadas de privacidad y seguridad que ayudan a proteger la información de tus clientes. (_Próximamente_)

* **Creada para el futuro:** Esta actualización le prepara para recibir mejoras e innovaciones continuas. 

Para los entornos aprovisionados para esta arquitectura, utilice las siguientes directrices para la configuración.

## Espacios de nombres y esquemas

Consulte [Esquemas y áreas de nombres B2B](https://experienceleague.adobe.com/es/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces) en la documentación de Experience Platform para obtener una descripción general.

### Configuración del entorno

Configure un entorno de Postman para admitir el espacio de nombres B2B y la utilidad de generación automática de esquemas.

* Puede descargar la colección de utilidades de generación automática de esquemas y áreas de nombres desde el [repositorio de GitHub](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility).

* Para obtener información sobre el uso de las API de Experience Platform, incluidos detalles sobre cómo recopilar valores para los encabezados necesarios y leer llamadas de API de ejemplo, consulte la guía de [introducción a las API de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/platform-apis/api-guide?lang=es).

* Para obtener información sobre cómo generar tus credenciales para las API de Experience Platform, consulta el tutorial sobre [autenticación y acceso a las API de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/platform-apis/api-authentication).

* Para obtener información sobre la configuración de las API de Postman para Experience Platform, consulte los pasos detallados en [Postman en Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/platform-apis/postman).

Con una consola para desarrolladores de Experience Platform y una configuración de Postman, ahora puede empezar a aplicar los valores de entorno adecuados al entorno de Postman.

### Ejecutar los scripts

Con la colección de Postman y la configuración del entorno, puede ejecutar el script a través de la interfaz de Postman.

En la interfaz de Postman, seleccione la carpeta raíz de la utilidad autogenerador y, a continuación, seleccione **Ejecutar** en el encabezado superior.

Cuando se muestre la interfaz Runner, asegúrese de que todas las casillas de verificación estén seleccionadas y, a continuación, seleccione **Ejecutar la utilidad de generación automática de espacios de nombres y esquemas**.

Una solicitud correcta crea los espacios de nombres y esquemas necesarios para B2B.

## Selección de campo XDM

Puede administrar los campos XDM disponibles en toda la aplicación en la interfaz de usuario de Journey Optimizer B2B edition. Estos campos ayudan a optimizar la instancia al exponer solo los campos relevantes para la generación de **_recorridos_**, **_grupos de compras_** o **_personalizaciones de correo electrónico_**.

### Clases XDM

#### Clases estándar

Siga los pasos a continuación para definir campos para clases XDM estándar:

1. Vaya a **[!UICONTROL Administración] > [!UICONTROL Configuraciones]**.

1. En el panel de navegación, seleccione **[!UICONTROL Clases XDM]**.

1. Seleccione la pestaña **[!UICONTROL Standard]** para ver las clases XDM disponibles:

   * Perfil individual de XDM

   * Cuenta empresarial de XDM

#### Campos administrados

Defina qué campos están disponibles en toda la aplicación.

1. Haga clic en el icono _Menú más_ (**...**) y seleccione **[!UICONTROL Editar campos administrados]**.

1. Revise la lista de campos disponibles (haga clic en el icono _Información_ para los metadatos de campo).

1. Seleccione los campos que desee incluir y borre las selecciones de los campos que no necesite.

1. Use el control deslizante **[!UICONTROL Mostrar solo los campos seleccionados]** para revisar sus selecciones.

1. Haga clic en **[!UICONTROL Guardar]**.

#### Campos actualizables

Elija qué campos se pueden modificar mediante las acciones de recorrido **[!UICONTROL Actualizar perfil de cuenta]** o **[!UICONTROL Actualizar perfil de persona]**.

1. Haga clic en el icono _Menú más_ (**...**) y seleccione **[!UICONTROL Editar campos actualizables]**.

1. Seleccione **[!UICONTROL Esquema]** y luego **[!UICONTROL Conjunto de datos]**.

   Su organización proporciona estos esquemas y conjuntos de datos.

1. Revise la lista de campos actualizables (haga clic en el icono _Información_ para ver los metadatos).

   Solo se pueden editar los campos administrados.

1. Seleccione los campos que desea que estén disponibles para la actualización desde recorrido.

1. Haga clic en **Guardar**.

### Esquemas relacionales

Seleccione [esquemas relacionales](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/schema/relational) para usarlos en **_decisiones de recorrido_** y **_personalización_**. Actualmente, estos esquemas son para casos de uso de objetos personalizados. En el futuro, los esquemas relacionales también se pueden utilizar para otros casos de uso de objetos.

1. Seleccione la ficha **[!UICONTROL Relacional]**.

1. Haga clic en **[!UICONTROL Seleccionar clase XDM relacional]**.

   Actualmente, solo se admite el objeto personalizado varios a uno de cuenta.

1. Revise la lista de campos de esquema (haga clic en el icono _information_ para ver los metadatos).

1. Seleccione los campos que desea incluir.

1. Use el control deslizante **[!UICONTROL Mostrar solo los campos seleccionados]** para revisar sus selecciones.

1. Haga clic en **[!UICONTROL Guardar]**.

>[!NOTE]
>
>Tenga en cuenta que los esquemas relacionales deben tener las siguientes configuraciones:
>
><li>Comportamiento: Registro
>&gt; <li>Segmentación: habilitada
>&gt; <li>Tipo de relación: varios a uno
>&gt; <li>Esquema de referencia: <a href="https://experienceleague.adobe.com/es/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data">Cuenta B2B - Esquema de cuenta empresarial de XDM</a>
>&gt; <li>Campos obligatorios: Clave principal, Clave externa y Descriptor de la versión
>&gt; <li>Conjunto de datos asociado: definido y asignado al esquema

### Eventos

Seleccione los eventos de experiencia que se usarán en **_toma de decisiones de recorrido_**.

1. Seleccione la ficha **[!UICONTROL Eventos]**.

1. Haga clic en **[!UICONTROL Seleccionar evento de experiencia]**.

1. Haga clic en **[!UICONTROL Seleccionar tipo de evento]**, elija el tipo de evento y haga clic en **[!UICONTROL Seleccionar]**.

1. Haga clic en **[!UICONTROL Seleccionar campos]**, elija los campos que necesita y haga clic en **[!UICONTROL Seleccionar]**.

1. Haga clic en **[!UICONTROL Guardar]**.

## Configuración de correo electrónico

Se debe configurar lo siguiente para enviar correos electrónicos desde Journey Optimizer B2B edition.  

[https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### Protocolos para el seguimiento y el envío de correos electrónicos

1. [Crear registros DNS para correo electrónico](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [Configurar SPF y DKIM](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [Configurar DMARC](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [Configurar registros MX para su dominio](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. [Agregar direcciones IP de salida a listas de permitidos](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. Si necesita compartir el grupo de IP dedicado, póngase en contacto con el equipo de entrega para conocer la viabilidad y la configuración asistida.

### Configuraciones de canal de correo electrónico

En la arquitectura simplificada, la configuración del correo electrónico se establece desde la interfaz de usuario de Marketo Engage. Complete los pasos de configuración relacionados con el correo electrónico: [https://experienceleague.adobe.com/es/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/es/docs/marketo/using/getting-started/initial-setup/setup-steps)

[https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### Límites de comunicación

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Canales]**.

1. En el panel de navegación, seleccione **[!UICONTROL Límite de comunicación]**.

1. Cree un conjunto de reglas de límite de comunicación global (este conjunto de reglas se crea de forma predeterminada en todas las instancias de Journey Optimizer B2B edition).

   No hay límite de comunicación si no se crea el conjunto de reglas global.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/es/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### Límites de comunicación compartida

Dentro de la nueva arquitectura, Journey Optimizer B2B edition y Marketo Engage tienen límites de comunicación independientes de forma predeterminada.

Si desea que la instancia de Marketo Engage comparta el límite de comunicación establecido en la instancia de Journey Optimizer B2B edition, póngase en contacto con el Soporte técnico de Adobe para obtener ayuda sobre la configuración o abra un ticket de soporte. Si se solicita, el equipo de ingeniería puede habilitar el uso compartido de límites de comunicación entre Journey Optimizer B2B edition y una o más instancias de Marketo Engage.

Actualmente, el límite de comunicaciones compartidas en la instancia de Marketo Engage debe configurarse mediante una llamada de API.

Por ejemplo, cuando:

* El munchkinId de la instancia de B2B edition de Journey Optimizer es `JKL-567-MNO`.
* El munchkinId de la instancia de Marketo Engage es `ABC-123-DEF` y se encuentra en el centro de datos JS

La solicitud de API debe tener un aspecto similar al siguiente:

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```

## Configuración del canal SMS

Consulte [_Configuraciones de SMS_](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms) para obtener información detallada.

## Acciones de Marketo Engage de recorrido

Puede configurar una o más instancias remotas de **_Marketo Engage_** para usarlas con las siguientes acciones de recorrido:

* Añadir a la lista de Marketo
* Eliminar de la lista de Marketo
* Añadir a campaña de solicitud de Marketo

Complete los siguientes pasos para configurar estas conexiones:

1. Vaya a **[!UICONTROL Administración] > [!UICONTROL Configuraciones]**.

1. En el panel de navegación, seleccione **[!UICONTROL Clases XDM]**.

1. Seleccione la ficha **[!UICONTROL Integraciones]**.

1. Haga clic en **[!UICONTROL Crear conexión]**.

1. Escriba **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]**.

1. Seleccione **[!UICONTROL Actualizar directiva]** para los registros de persona coincidentes.

1. Escriba **[!UICONTROL Munchkin ID]**, **[!UICONTROL ID de cliente]**, **[!UICONTROL Secreto de cliente]** y haga clic en **[!UICONTROL Conectarse a Marketo]**.

1. Haga clic en **[!UICONTROL Crear]**.

## Incorporación del usuario

Consulte la página [Administración de usuarios](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/admin/user-management) para obtener una descripción general.

### Grupos de usuarios existentes

Si todos los usuarios de Journey Optimizer B2B edition existentes necesitan acceder a la nueva arquitectura, utilice el grupo de usuarios de Journey Optimizer B2B edition existente. Un administrador del sistema o de productos puede realizar los siguientes pasos.

1. Cree un perfil de producto en la Marketo Engage específica.

1. Agregue un grupo de usuarios existente al perfil de productos creado.

Los perfiles otorgan todas las funciones y permisos ya asignados a ese grupo de usuarios, que ya deben configurarse para que los usuarios accedan a Journey Optimizer B2B edition. Si solo un subconjunto de usuarios debe acceder a la nueva arquitectura, complete los pasos descritos a continuación. Más detalles en la [documentación actual](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/admin/user-management).

### Crear un nuevo grupo de usuarios

1. Cree un perfil de producto en la instancia de Marketo Engage específica.
1. Cree un grupo de usuarios para los nuevos usuarios.
1. Seleccione y asigne los perfiles de producto necesarios al grupo de usuarios:

   * Perfil de Marketo Engage que ha creado
   * Perfiles de Adobe Experience Platform
      * AEP-Default-All-Users
      * Recopilación de datos de Adobe Experience Platform
      * Recopilación de datos: todo el acceso

1. Agregue los usuarios al grupo de usuarios.
1. Agregue un nuevo grupo de usuarios a las funciones de Journey Optimizer B2B edition en Experience Platform.
