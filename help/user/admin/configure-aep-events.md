---
title: Seleccionar eventos y campos de experiencia
description: Seleccione eventos y campos de Experience Platform para almacenar en déclencheur la toma de decisiones en tiempo real en recorrido en función del comportamiento del cliente.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Esta función se encuentra actualmente en versión beta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: adf04a6a-050f-44bc-a52c-db79ccb22ebf
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: 2026-03-27T22:58:08.848Z
TQID: https://experienceleague.adobe.com/vmRXmmc19LjpJf6EQ0BipW8oXn5GdKT3r-boHLd-XmQ
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 1476
ht-degree: 13%

---

# Seleccionar eventos de experiencia y campos

Los administradores pueden seleccionar [Eventos de experiencia de AEP](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} específicos y sus campos asociados dentro del esquema de unión de eventos de experiencia. Después de la selección, los usuarios pueden configurar reglas de toma de decisiones para escuchar esos eventos de experiencia y habilitar acciones de campaña dinámicas y segmentadas basadas en datos de eventos casi en tiempo real.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
El uso de eventos de experiencia de AEP en recorrido es un proceso de dos pasos:

1. Un administrador [agrega eventos y campos de experiencia de AEP](#add-an-event) en las configuraciones de Journey Optimizer B2B edition.

2. En un recorrido, un experto en marketing agrega un nodo _Escuchar un evento_ y [selecciona un Evento de experiencia](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Selecciona el evento que se va a utilizar en el nodo.
   * Selecciona los campos que se van a utilizar como restricciones.

>[!BEGINSHADEBOX]

## Directrices y limitaciones

A medida que seleccione eventos para satisfacer sus objetivos organizativos, tenga en cuenta lo siguiente:

* Puede seleccionar hasta 50 eventos y hasta 100 campos por evento.

* Los recorridos pueden escuchar los eventos de experiencia que se incorporan mediante las funciones de flujo continuo de Experience Platform, como Web SDK o la API HTTP.

* Puede utilizar eventos de experiencia para la toma de decisiones dentro de un recorrido, pero no se conservan. Por lo tanto, no puede aprovechar un registro histórico de eventos de experiencia en Journey Optimizer B2B edition.

* Cuando se utiliza un evento de experiencia y se publica el recorrido, se pueden añadir más campos, pero no se pueden eliminar los seleccionados anteriormente.

* Puede hacer referencia a un evento de experiencia en varios recorridos o utilizar uno más de una vez dentro del mismo recorrido.

>[!ENDSHADEBOX]

## Administrar eventos de experiencia

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en **[!UICONTROL Clases XDM]** en el panel intermedio y, a continuación, haga clic en la pestaña **[!UICONTROL Eventos]** para mostrar la lista de los eventos disponibles.

   ![Acceder a los eventos de experiencia seleccionados](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   La lista se muestra de acuerdo con la columna _[!UICONTROL Última actualización]_, con los eventos actualizados más recientemente en la parte superior de forma predeterminada.

   Desde esta página, puede [seleccionar](#add-an-event) y [editar](#edit-an-event) eventos para usarlos en recorridos.

   Para acceder a los detalles de un evento seleccionado, haga clic en el nombre del evento.

### Filtrado de la lista de eventos

Escriba texto en el campo _[!UICONTROL Buscar]_ para filtrar los eventos mostrados y buscar una coincidencia en el nombre del evento.

![Filtrar la lista de eventos seleccionados por nombre](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Añadir un evento

Para que un evento de experiencia esté disponible para un nodo _Escuchar un evento_ en un recorrido, seleccione el evento y los campos admitidos.

>[!NOTE]
>
>En la versión beta, no se pueden eliminar eventos de la lista. Asegúrese de que cada evento que agregue sea uno que su organización pretenda utilizar.

1. Haga clic en **[!UICONTROL Seleccionar evento de experiencia]** en la parte superior derecha.

   Se muestra la página de detalles del evento. Desde esta página, puede elegir el tipo de evento y los campos.

   ![Detalles del evento para un nuevo evento](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Elija el tipo de evento.

   * Haga clic en **[!UICONTROL Seleccionar tipo de evento]**.

   * En el cuadro de diálogo, elija el tipo de evento.

     Utilice el campo _[!UICONTROL Buscar]_ para filtrar la lista mostrada por nombre. Use el control deslizante **[!UICONTROL Mostrar solo los campos seleccionados]** para revisar las selecciones actuales.

     ![Seleccionar cuadro de diálogo de tipo de evento](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Haga clic en **[!UICONTROL Seleccionar]**.

1. Elija uno o varios campos para el tipo de evento.

   * Haga clic en **[!UICONTROL Seleccionar campos]**.

   * En el cuadro de diálogo, seleccione los campos que desee utilizar como restricciones para eventos coincidentes.

     Utilice el campo _[!UICONTROL Buscar]_ para filtrar la lista mostrada por nombre. Use el control deslizante **[!UICONTROL Mostrar solo los campos seleccionados]** para revisar las selecciones actuales.

     ![Cuadro de diálogo Seleccionar campos](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Haga clic en **[!UICONTROL Seleccionar]**.

1. En la página de detalles del evento, haga clic en **[!UICONTROL Guardar]**.

El evento guardado se muestra en la lista de la ficha _[!UICONTROL Eventos]_.

### Edición de un evento

Edite los detalles del evento para cambiar los campos.

1. Haga clic en el nombre del evento o haga clic en el icono _Más menú_ ( **...** ) y elija **[!UICONTROL Editar]**.

   ![Haga clic en el icono del menú Más](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar campos]** para agregar más campos o eliminar las selecciones existentes en el cuadro de diálogo _[!UICONTROL Seleccionar campos]_.

1. Haga clic en **[!UICONTROL Seleccionar]** para guardar las selecciones.

### Eliminar un evento

>[!NOTE]
>
>Para la versión de Beta de esta función, no se puede quitar un evento de la lista de eventos seleccionados. Se ha planificado la eliminación de eventos para la versión de GA.

## Eventos y campos

Para [!DNL Journey Optimizer B2B Edition], ciertas actividades a nivel de personas se capturan como [!DNL Experience Platform] eventos de experiencia. Estos eventos se almacenan en un conjunto de datos del sistema que utiliza el esquema de evento de experiencia XDM e incluye grupos de campos específicos del recorrido. Puede usar estos eventos en [!UICONTROL Journey Optimizer B2B edition] como cualquier otro evento de experiencia.

Cada evento expone un conjunto definido de campos que se pueden utilizar en el recorrido _Escuchar un evento_ nodos (toma de decisiones basada en eventos). Revise los tipos de evento disponibles y sus campos para determinar qué evento y campos utilizar en estos nodos de recorrido:

### Se envió el email

Este evento rastrea cuándo se envió un correo electrónico de marketing a una persona.

Tipo de evento: `directMarketing.emailSent`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de correo electrónico | `directMarketing.emailSent.mailingKey.sourceID` |
| Tipo de origen de correo electrónico | `directMarketing.emailSent.mailingKey.sourceType` |
| ID de instancia de correo electrónico | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| Clave de origen de correo electrónico | `directMailing.emailSent.mailingKey.sourceKey` |
| Nombre de correo | `directMarketing.emailSent.mailingName` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Correo electrónico entregado

Este evento rastrea cuándo se entregó correctamente un correo electrónico al servicio de correo electrónico de una persona.

Tipo de evento: `directMarketing.emailDelivered `

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de correo | `directMarketing.mailingKey.sourceID` |
| Tipo de origen de correo | `directMarketing.mailingKey.sourceType` |
| ID de instancia de origen de correo | `directMarketing.mailingKey.sourceInstanceID` |
| Clave de origen de correo | `directMarketing.mailingKey.sourceKey` |
| Nombre de correo | `directMarketing.mailingName` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Se abrió el email

Este evento rastrea cuándo una persona ha abierto un correo electrónico de marketing.

Tipo de evento: `directMarketing.emailOpened`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de correo | `directMarketing.mailingKey.sourceID` |
| Tipo de origen de correo | `directMarketing.mailingKey.sourceType` |
| ID de instancia de origen de correo | `directMarketing.mailingKey.sourceInstanceID` |
| Clave de origen de correo | `directMarketing.mailingKey.sourceKey` |
| Nombre de correo | `directMarketing.mailingName` |
| Es un dispositivo móvil | `device.isMobileDevice` |
| Modelo de dispositivo | `device.model` |
| Agente de usuario | `environment.browserDetails.userAgent` |
| Sistema operativo | `environment.operatingSystem` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Correo electrónico clicado

Este evento rastrea cuándo una persona hizo clic en un vínculo en un correo electrónico de marketing.

Tipo de evento: `directMarketing.emailClicked`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de correo | `directMarketing.mailingKey.sourceID` |
| Tipo de origen de correo | `directMarketing.mailingKey.sourceType` |
| ID de instancia de origen de correo | `directMarketing.mailingKey.sourceInstanceID` |
| Clave de origen de correo | `directMarketing.mailingKey.sourceKey` |
| Nombre de correo | `directMarketing.mailingName` |
| URL del vínculo | `directMarketing.linkURL` |
| Es un dispositivo móvil | `device.isMobileDevice` |
| Modelo | `device.model` |
| Agente de usuario | `environment.browserDetails.userAgent` |
| Sistema operativo | `environment.operatingSystem` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### El email se rechazó

Este evento rastrea cuándo rebotó un correo electrónico a una persona.

Tipo de evento: `directMarketing.emailBounced`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de correo | `directMarketing.mailingKey.sourceID` |
| Tipo de origen de correo | `directMarketing.mailingKey.sourceType` |
| ID de instancia de origen de correo | `directMarketing.mailingKey.sourceInstanceID` |
| Clave de origen de correo | `directMarketing.mailingKey.sourceKey` |
| Nombre de correo | `directMarketing.mailingName` |
| Correo electrónico | `directMarketing.email` |
| Código de correo electrónico rechazado | `directMarketing.emailBouncedCode` |
| Detalles de correos electrónicos rechazados | `directMarketing.emailBouncedDetails` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Se rechazó el email temporalmente

Este evento rastrea cuándo ha rebotado suavemente un correo electrónico a una persona.

Tipo de evento: `directMarketing.emailBouncedSoft`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de correo | `directMarketing.mailingKey.sourceID` |
| Tipo de origen de correo | `directMarketing.mailingKey.sourceType` |
| ID de instancia de origen de correo | `directMarketing.mailingKey.sourceInstanceID` |
| Clave de origen de correo | `directMarketing.mailingKey.sourceKey` |
| Nombre de correo | `directMarketing.mailingName` |
| Correo electrónico | `directMarketing.email` |
| Código de correo electrónico rechazado | `directMarketing.emailBouncedCode` |
| Detalles de correos electrónicos rechazados | `directMarketing.emailBouncedDetails` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Correo electrónico cancelado

Este evento rastrea cuándo una persona canceló la suscripción a un correo electrónico de marketing.

Tipo de evento: `directMarketing.emailUnsubscribed `

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de correo | `directMarketing.mailingKey.sourceID` |
| Tipo de origen de correo | `directMarketing.mailingKey.sourceType` |
| ID de instancia de origen de correo | `directMarketing.mailingKey.sourceInstanceID` |
| Clave de origen de correo | `directMarketing.mailingKey.sourceKey` |
| Nombre de correo | `directMarketing.mailingName` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Visite la página web

Este tipo de evento es el método estándar para marcar la visita como una vista de página.

Tipo de evento: `web.webpagedetails.pageViews`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de página web | `web.webPageDetails.webPageKey.sourceID` |
| Tipo de origen de página web | `web.webPageDetails.webPageKey.sourceType` |
| ID de instancia de origen de página web | `web.webPageDetails.webPageKey.sourceInstanceID` |
| Clave de origen de página web | `web.webPageDetails.webPageKey.sourceKey` |
| Nombre de página web | `web.webPageDetails.name` |
| URL de página web | `web.webPageDetails.URL` |
| Parámetros de consulta de página web | `web.webPageDetails.queryParameters` |
| ID de página web | `web.webPageDetails.webPageID` |
| Agente de usuario | `environment.browserDetails.userAgent` |
| URL del remitente | `web.webReferrer.URL` |

+++

### Formulario rellenado

Este evento rastrea cuándo una persona ha rellenado un formulario en una página web.

Tipo de evento: `web.formFilledOut`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de formulario web | `web.fillOutForm.webFormKey.sourceID` |
| Tipo de origen de formulario web | `web.fillOutForm.webFormKey.sourceType` |
| ID de instancia de origen de formulario web | `web.fillOutForm.webFormKey.sourceInstanceID` |
| Clave de origen de formulario web | `web.fillOutForm.webFormKey.sourceKey` |
| ID del formulario web | `web.fillOutForm.webFormID` |
| Nombre del formulario web | `web.fillOutForm.webFormName` |
| Parámetros de consulta de página web | `web.webPageDetails.queryParameters` |
| ID de página web | `web.webPageDetails.webPageID` |
| Agente de usuario | `environment.browserDetails.userAgent` |
| URL del remitente | `web.webReferrer.URL` |

+++

### Vínculo web pulsado

El evento indica que Web SDK registró automáticamente un clic en vínculo.

Tipo de evento: `web.webinteraction.linkClicks`

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| ID de origen de interacción web | `web.webInteraction.webInteractionKey.sourceID` |
| Tipo de origen de interacción web | `web.webInteraction.webInteractionKey.sourceType` |
| ID de instancia de origen de interacción web | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| Clave de origen de interacción web | `web.webInteraction.webInteractionKey.sourceKey` |
| ID del vínculo de interacción web | `web.webInteraction.linkID` |
| URL del vínculo de interacción web | `web.webInteraction.linkURL` |
| Parámetros de consulta de página web | `web.webPageDetails.queryParameters` |
| ID de página web | `web.webPageDetails.webPageID` |
| Agente de usuario | `environment.browserDetails.userAgent` |
| URL del remitente | `web.webReferrer.URL` |

+++

### Momento interesante

Este evento rastrea cuándo se grabó un momento interesante para una persona.

Tipo de evento: `leadOperation.interestingMoment `

+++Campos

| Nombre para mostrar | Ruta |
| ------------ | ---- |
| Identificador | `_id` |
| Tipo de evento | `eventType` |
| Marca de tiempo | `timestamp` |
| ID de persona | `personID` |
| ID de origen de persona | `personKey.sourceID` |
| Tipo de origen de persona | `personKey.sourceType` |
| ID de instancia de origen de persona | `personKey.sourceInstanceID` |
| Clave de origen de persona | `personKey.sourceKey` |
| Fecha del momento | `leadOperation.interestingMoment.date` |
| Descripción del momento | `leadOperation.interestingMoment.description` |
| Origen del momento | `leadOperation.interestingMoment.source` |
| Tipo de momento | `leadOperation.interestingMoment.type` |
| ID de recorrido | `_experience.journeyOrchestration.stepEvents.journeyID` |
| ID de nodo | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!--
 ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) 
-->