---
title: Escuchar un nodo de evento
description: Marcador de posición
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d0031543-532c-4a26-8f90-01af2b91e6d0id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 10%

---

# Escucha de un nodo de evento

Agregue el nodo _Listen for an event_ para mover la audiencia hacia adelante al siguiente paso del recorrido cuando se produzca un evento.

## Filtros de eventos de personas

| Filtros | Descripción |
| ------- | ----------- |
| Historial de actividades > Correo electrónico | Actividades de correo electrónico basadas en condiciones que se evalúan mediante uno o varios mensajes de correo electrónico seleccionados: <li>Hizo clic en el vínculo del correo electrónico <li>Abrió el email |
| Historial de actividades > Valor de los datos cambiado | Se ha producido un cambio de valor en un atributo de persona seleccionado. Estos tipos de cambio incluyen: <li>Nuevo valor <li>Valor anterior <li>Razón <li>Origen <li>Fecha de la actividad <li> Mín. número de veces |

## Adición de un nodo de evento

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para el tipo de evento.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. Seleccione un evento de la lista.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

>[!NOTE]
>
>La funcionalidad de tiempo de espera para Escuchar para un nodo de evento no funciona actualmente y se habilitará en una fase posterior.
