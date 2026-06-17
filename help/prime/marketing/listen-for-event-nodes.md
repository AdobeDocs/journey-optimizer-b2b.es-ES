---
title: Escuchar un nodo de evento
description: 'Configuración de la escucha de nodos de evento en Journey Optimizer B2B edition Prime: establezca déclencheur de evento, aplique filtros opcionales y haga avanzar a las personas cuando se produzcan actividades o cambios en los datos.'
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d0031543-532c-4a26-8f90-01af2b91e6d0id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3368f815edc0ce817cb7ed371157b63fa548d848
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 8%

---

# Escucha de un nodo de evento

Agregue el nodo _Listen for an event_ para mover la audiencia hacia adelante al siguiente paso del recorrido cuando se produzca un evento.

## Déclencheur de eventos {#event-triggers}

Obtener lista del PM

## Filtros de eventos {#event-filters}

Obtener lista actualizada del PM

| Filtros | Descripción |
| ------- | ----------- |
| Historial de actividades > Correo electrónico | Actividades de correo electrónico basadas en condiciones que se evalúan mediante uno o varios mensajes de correo electrónico seleccionados: <li>Hizo clic en el vínculo del correo electrónico <li>Abrió el email |
| Historial de actividades > Valor de los datos cambiado | Se ha producido un cambio de valor en un atributo de persona seleccionado. Estos tipos de cambio incluyen: <li>Nuevo valor <li>Valor anterior <li>Razón <li>Origen <li>Fecha de la actividad <li> Mín. número de veces |

## Adición de un nodo de evento {#add-event-node}

1. Navegue hasta el lienzo de recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

   ![Haga clic en agregar icono en la ruta de recorrido](./assets/person-journey-canvas-add-node.png){width="200"}

1. En las propiedades del nodo, a la derecha, haga clic en **[!UICONTROL Agregar criterios de evento]**.

1. En el cuadro de diálogo _[!UICONTROL Editar evento]_, agregue los eventos al déclencheur.

   ![Editar evento: déclencheur de evento](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. (Opcional) Seleccione la ficha **[!UICONTROL Filtros]** en el cuadro de diálogo y agregue criterios de filtrado para los déclencheur.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

   ![Editar evento: filtrado de eventos](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](../../user/journeys/assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>La funcionalidad de tiempo de espera para Escuchar para un nodo de evento no funciona actualmente. Está planificado para una versión posterior.
