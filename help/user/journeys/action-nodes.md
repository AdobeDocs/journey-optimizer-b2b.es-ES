---
title: Realizar una acción
description: 'Configure nodos de acción para acciones de cuenta y personas: envíe correos electrónicos, actualice grupos de compra, cambie puntuaciones e integre con Marketo Engage en Journey Optimizer B2B edition.'
feature: Account Journeys
role: User
exl-id: 167cb627-96ee-42a8-8657-bb8040bb4bfe
source-git-commit: 3013da8c7178c68ec07bf8d8b56f4ca06c043486
workflow-type: tm+mt
source-wordcount: '1674'
ht-degree: 2%

---

# Iniciar una acción

En el recorrido de su cuenta, puede agregar un nodo _[!UICONTROL Realizar una acción]_ para ejecutar una acción, como enviar un mensaje de correo electrónico, cambiar una puntuación, asignar a un grupo comprador, etc. Las acciones suelen ser lo que desea que ocurra como resultado de algún tipo de déclencheur, como un evento o una acción anterior.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

## Acciones de cuenta

Utilice una acción en las cuentas cuando desee aplicar un cambio a todas las personas que forman parte de cuentas en la ruta del nodo.

### Acciones y restricciones {#account-action-constraints}

| Acción | Restricciones |
| ------ | ----------- |
| [!UICONTROL Momento interesante de la cuenta] | Escriba (correo electrónico, hito o web)<br/>Descripción (opcional) |
| [!UICONTROL Activar en destino] | Seleccione un destino |
| [!UICONTROL Agregar cuenta a (otro) Recorrido] | Seleccionar recorrido de cuenta activa |
| [!UICONTROL Agregar a la lista de cuentas] | Seleccionar lista de cuentas estáticas activas |
| [!UICONTROL Quitar cuenta del Recorrido] | Seleccionar recorrido de cuenta activa |
| [!UICONTROL Quitar de la lista de cuentas] | Seleccione una lista de cuentas estáticas activas |
| [!UICONTROL Enviar alerta de ventas] | Seleccionar interés de solución<br/>Enviar correo electrónico a |
| [!UICONTROL Actualizar perfil de cuenta] | Seleccionar atributo<br/>Nuevo valor |
| [!UICONTROL Actualizar fase del grupo de compra] | Seleccione el interés de la solución<br/>Seleccione la fase de compra del grupo |
| [!UICONTROL Actualizar estado del grupo de compra] | Seleccione el interés de la solución<br/>Estado (obligatorio, máximo 50 caracteres) |

>[!NOTE]
>
>La acción _[!UICONTROL Valor de datos de cambio de cuenta]_ está obsoleta para la versión 2025.10. Se ha reemplazado por _[!UICONTROL Actualizar perfil de cuenta]_ para la [arquitectura simplificada](../simplified-architecture.md).<br/>
>
>Un administrador puede configurar los atributos disponibles para la cuenta empresarial de XDM actualizando los campos de las _[!UICONTROL clases XDM]_ > _[!UICONTROL clases estándar]_. Para obtener más información, vea [Clases estándar](../admin/xdm-field-management.md#standard-classes).

### Añadir una acción basada en cuentas

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Realizar una acción]**.

   ![Agregar nodo de recorrido - realizar una acción](./assets/add-node-action.png){width="400"}

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Cuentas]** para la acción.

1. Seleccione una acción de la lista y defina los valores que desee para la acción.

   ![nodo de Recorrido: realice una acción en una cuenta](./assets/node-take-action-account.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX]

### Activar en un destino de LinkedIn

Use la acción _Activar en destino_ para que las cuentas activen cuentas en destinos de Experience Platform directamente desde su recorrido. Esta acción le permite insertar cuentas cualificadas (según los filtros de grupo de compra, las puntuaciones de participación y otros criterios) en audiencias coincidentes en destinos admitidos. It

A partir de la versión 2025.10, **_LinkedIn_** es el primer tipo de destino admitido. Utilice la acción para un destino de LinkedIn para optimizar la ejecución de la campaña eliminando los traslados de varios sistemas y reduciendo la latencia. Por ejemplo, como experto en marketing, puede activar automáticamente cuentas de alta intención en LinkedIn para volver a segmentar cuando falten funciones de compra clave o volver a activar cuentas inactivas basadas en filtros de inactividad.

Para obtener más información sobre el uso de audiencias coincidentes con la cuenta para un destino de LinkedIn, consulte [Audiencias coincidentes con la cuenta de LinkedIn](../data/linkedin-account-matched-audiences.md).

+++ Establecer la activación de cuentas en un destino de LinkedIn

1. Con el nodo _Realizar una acción_ seleccionado en el lienzo de recorrido, establezca **[!UICONTROL Acción en las cuentas]** en **[!UICONTROL Activar en destino]**.

1. Haga clic en **[!UICONTROL Seleccionar destino]**.

   ![nodo de Recorrido - realizar una acción en las cuentas - activar en destino](./assets/node-activate-destination-select-destination.png){width="600" zoomable="yes"}

1. En el cuadro de diálogo, seleccione el destino configurado de LinkedIn y haga clic en **[!UICONTROL Guardar]**.

![nodo de Recorrido - realizar una acción en las cuentas - activar en destino - seleccionar cuadro de diálogo de destino](./assets/node-activate-destination-select-destination-dialog.png){width="700" zoomable="yes"}

1. Escriba el **[!UICONTROL nombre de audiencia]** que se usa para identificar la audiencia activada en el destino.

   ![nodo de Recorrido - realizar una acción en las cuentas - activar en destino - configuración completada](./assets/node-activate-destination-settings.png){width="550" zoomable="yes"}

+++

>[!ENDSHADEBOX]

## Acciones de personas

Utilice una acción en personas cuando desee aplicar un cambio a todas las personas de la ruta del nodo. Este tipo de nodo se puede utilizar dentro de la ruta dividida por personas o por cuentas.

### Acciones y restricciones {#people-action-constraints}

| Contexto | Acción | Restricciones |
| ------- | ------ | ----------- |
| [Journey Optimizer B2B](#journey-optimizer-b2b-actions) | [!UICONTROL Agregar a la audiencia de cliente externa] | Seleccionar el público externo del cliente |
| | [!UICONTROL Asignar a grupo de compra] | Seleccionar interés de solución<br/>Seleccionar rol |
| | [!UICONTROL Cambiar puntuación] | Nombre de puntuación<br/>Cambio en la puntuación |
| | [!UICONTROL Momento interesante para la persona] | Escriba<br/>Descripción |
| | [!UICONTROL Quitar del grupo de compra] | Seleccionar interés de la solución |
| | [!UICONTROL Enviar correo electrónico] | Crear nuevo correo electrónico<br/>Seleccione un correo electrónico de Marketo Engage |
| | [!UICONTROL Enviar SMS] | Creación de un SMS |
| | [!UICONTROL Actualizar perfil de persona] | Seleccionar atributo de persona<br/>Establecer nuevo valor |
| [Marketo Engage](#marketo-engage-actions) | [!UICONTROL Agregar a la campaña de solicitudes de Marketo Engage] | Seleccione el espacio de trabajo de Marketo Engage<br/>Seleccionar campaña de solicitud |
| | [!UICONTROL Agregar a la lista de Marketo] | Seleccionar nombre de conexión Marketo externa <br/>Nombre de lista |
| | [!UICONTROL Quitar de la lista de Marketo] | Seleccionar nombre de conexión Marketo externa <br/>Nombre de lista |

>[!NOTE]
>
>La acción _[!UICONTROL Cambiar partición de personas en Marketo Engage]_ está obsoleta para la versión 2025.10 y no está disponible en la [arquitectura simplificada](../simplified-architecture.md) para Journey Optimizer B2B edition.<br/>
>
>La acción _[!UICONTROL Cambiar valor de datos]_ está obsoleta para la versión 2025.10. Se reemplaza con _[!UICONTROL Actualizar perfil de persona]_ en la arquitectura simplificada.

### Añadir una acción basada en personas

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Realizar una acción]**.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para la acción.

1. Seleccione una acción de la lista y defina los valores que desee para la acción.

![nodo de Recorrido: realice una acción con personas](./assets/node-take-action-people.png){width="700" zoomable="yes"}

### Acciones B2B de Journey Optimizer

Las acciones basadas en personas de Journey Optimizer B2B están diseñadas para administrar las comunicaciones a través de los canales configurados y administrar la categorización de personas dentro de los grupos y cuentas de compra. El recorrido aplica la acción cuando una cuenta correspondiente con perfiles de persona llega al nodo.

+++[!UICONTROL Agregar a la audiencia de cliente externa]

Utilice esta acción para dirigir a las personas a una audiencia externa que se puede activar en un canal de medios de pago para dirigirse aún más a los miembros de los grupos compradores. Esta acción se ejecuta mediante Real-Time CDP B2B/P Edition.

>[!NOTE]
>
>Cuando una cuenta correspondiente con perfiles de persona alcanza el nodo _Agregar a la audiencia de cliente externa_ en un recorrido publicado, esos perfiles pueden tardar hasta 48 horas en rellenarse en la audiencia externa.

![Realizar una acción: agregar a la audiencia de clientes externos](./assets/node-action-add-to-external-audience-options.png){width="300"}

Al seleccionar esta acción basada en personas, puede crear una audiencia externa nueva o seleccionar una de ellas. Para las audiencias existentes, puede elegir entre audiencias de clientes externos creadas únicamente en Journey Optimizer B2B edition. Cuando cree una audiencia y la utilice para esta acción de recorrido, asegúrese de conectar el destino. Para obtener más información, consulte [Crear una nueva conexión de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} y [Descripción general de la activación](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activation-overview#activate-audiences-from-the-destinations-catalog){target="_blank"} en la documentación de Experience Platform.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea un vídeo de información general sobre la orquestación de medios de pago](../data/linkedin-account-matched-audiences.md#orchestrate-paid-media-engagement)

_Para crear una audiencia externa :_

1. Elija **[!UICONTROL Crear nuevo]**.

1. Haga clic en **[!UICONTROL Crear audiencia de cliente externa]**.

1. Escriba **[!UICONTROL Name]** (obligatorio) y **[!UICONTROL Description]** (opcional) para la nueva audiencia externa.

   ![Agregar a audiencia de cliente externa - Crear audiencia](./assets/node-action-add-to-external-create-new.png){width="300"}

1. Haga clic en **[!UICONTROL Crear]**.

   El sistema crea la nueva audiencia y muestra un mensaje de confirmación. A continuación, puede utilizarla como audiencia existente para la acción del nodo.

   >[!NOTE]
   >
   >Cuando se crea una nueva audiencia de cliente externa desde Journey Optimizer B2B edition, se predefine con un registro ficticio (`test@email.com`). Este registro se sobrescribe en cuanto se añade el primer perfil real a la audiencia externa desde el recorrido.

_Para usar una audiencia existente :_

1. Haga clic en **[!UICONTROL Seleccionar audiencia de cliente externo]**.

1. En el cuadro de diálogo, seleccione la audiencia que desee utilizar.

   ![Agregar a audiencia de cliente externa - Agregar audiencia](./assets/node-action-add-to-external-audience-select.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Agregar audiencia]**.

+++

+++[!UICONTROL Asignar a grupo de compra]

Utilice esta acción para agregar perfiles de personas a un [grupo de compra](../buying-groups/buying-groups-overview.md) según el rol y el interés de una solución seleccionados.

![Realizar una acción - Agregar a grupo de compra](./assets/node-action-add-to-buying-group.png){width="300"}

+++

+++[!UICONTROL Cambiar puntuación]

Utilice esta acción para cambiar la puntuación de la persona en Marketo Engage. [Más información](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-learn){target="_blank"}

![Realizar una acción - Cambiar puntuación](./assets/node-action-change-score.png){width="300"}

+++

+++[!UICONTROL Momento interesante para la persona]

Utilice esta acción para registrar un momento interesante para las personas. Elija un tipo (correo electrónico, hito o web) y añada una descripción (opcional).

![Realizar una acción - Momento interesante de la persona](./assets/node-action-person-interesting-moment.png){width="300"}

+++

+++[!UICONTROL Quitar del grupo de compra]

Utilice esta acción para quitar perfiles de personas de un [grupo de compra](../buying-groups/buying-groups-overview.md) según el interés de una solución seleccionada.

![Realizar una acción - Agregar a grupo de compra](./assets/node-action-remove-from-buying-group.png){width="300"}

+++

+++[!UICONTROL Enviar correo electrónico]

Utilice esta acción para enviar un correo electrónico. Después de [crear el correo electrónico](../content/add-email.md#add-an-email-to-your-journey) para el nodo, puede diseñar, personalizar y previsualizar mensajes de correo electrónico en el espacio de diseño de correo electrónico (consulte [Creación de correo electrónico](../content/email-authoring.md)). También puedes enviar un [correo electrónico desde Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/creating-an-email/create-an-email){target="_blank"}. Seleccione el espacio de trabajo de Marketo Engage y, a continuación, el correo electrónico que desea enviar.

![Realizar una acción - Enviar correo electrónico](./assets/node-action-send-email-from-marketo.png){width="300"}

+++

+++[!UICONTROL Enviar SMS]

Utilice esta acción para enviar un mensaje SMS. Puede crear, personalizar y previsualizar mensajes SMS en el espacio de diseño visual (consulte [Creación de SMS](../content/sms-authoring.md)).

![Realizar una acción - Enviar SMS](./assets/node-action-send-sms.png){width="300"}

+++

+++[!UICONTROL Actualizar perfil de persona]

Utilice esta acción para cambiar el valor de un atributo de perfil de [personas](../admin/field-mapping.md#xdm-business-person-attributes). Seleccione el atributo y, a continuación, establezca el nuevo valor.

![Realizar una acción: actualizar el perfil de la persona](./assets/node-action-update-person-profile.png){width="300"}

>[!NOTE]
>
>El _[!UICONTROL perfil de persona de actualización]_ reemplaza la acción _[!UICONTROL Cambiar valor de datos]_ en la [arquitectura simplificada](../simplified-architecture.md).<br/>
>
>Un administrador puede configurar los atributos disponibles para el perfil individual de XDM actualizando los campos en las _[!UICONTROL clases XDM]_ > [!UICONTROL clases estándar]. Para obtener más información, vea [Clases estándar](../admin/xdm-field-management.md#standard-classes).

+++

### Acciones de Marketo Engage

Las acciones basadas en personas de Marketo Engage están diseñadas para coordinar la orquestación de marketing basada en cuentas en Journey Optimizer B2B edition con los esfuerzos de marketing basados en posibles clientes en Marketo Engage. Utilice estas acciones para organizar la pertenencia a listas y solicitar campañas.

>[!NOTE]
>
>Las acciones de Marketo Engage requieren la integración configurada con una o más instancias de Marketo Engage externas. <!-- For detailed information about configuring these connections, see #. -->

Por ejemplo: es posible que desee suprimir las campañas de Marketo Engage para personas que forman parte de grupos compradores en Journey Optimizer B2B edition. En este caso, puede crear una lista estática en Marketo Engage específicamente para la solución que le interese. A continuación, en una ruta dividida al comprar un grupo, use la acción _Agregar a la lista de Marketo_ desde un nodo de recorrido. Esta acción añade miembros del grupo de compra a una lista estática concreta de una instancia de Marketo Engage conectada. A continuación, utilice la lista estática centrada en el interés de la solución para un filtro de lista inteligente en Marketo Engage.

+++[!UICONTROL Agregar a la campaña de solicitudes de Marketo Engage]

Utilice esta acción para agregar perfiles de personas a una [campaña de solicitudes](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/request-campaign){target="_blank"} en Marketo Engage.

En primer lugar, seleccione una instancia de Marketo Engage conectada. A continuación, seleccione el nombre de la campaña de solicitud.

![Realizar una acción: agregar a la campaña de solicitudes de Marketo Engage](./assets/node-action-add-to-request-campaign-options.png){width="300"}

+++

+++[!UICONTROL Agregar a la lista de Marketo]

Utilice esta acción para agregar personas a una [lista estática](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"} en Marketo Engage.

En primer lugar, seleccione una instancia de Marketo Engage conectada. A continuación, seleccione el nombre de la lista.

![Realizar una acción - Agregar a la lista de Marketo](./assets/node-action-add-to-list-options.png){width="300"}

+++

+++[!UICONTROL Quitar de la lista de Marketo]

Use esta acción para quitar personas de una [lista estática](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"} en Marketo Engage.

En primer lugar, seleccione una instancia de Marketo Engage conectada. A continuación, seleccione el nombre de la lista.

![Realizar una acción: eliminar de la lista de Marketo](./assets/node-action-remove-from-list-options.png){width="300"}

+++

## Vídeo resumen

>[!VIDEO](https://video.tv.adobe.com/v/3443207/?learn=on)
