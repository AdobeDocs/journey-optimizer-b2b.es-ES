---
title: Nodo de Recorrido de Audiencia de persona
description: Configure el nodo de audiencia de persona en Journey Optimizer B2B para especificar qué perfiles introducen un recorrido mediante listas dinámicas de personas o audiencias basadas en eventos.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a48a12635d2ba4f14dda49e25e79a5496ebbdecf
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 4%

---

# Nodo de audiencia de persona

El nodo _audiencia de persona_ especifica qué perfiles de persona entran en el recorrido. Cuando [crea un recorrido de persona](./person-journeys.md), el recorrido siempre comienza con un nodo de audiencia de persona que define su entrada. El nodo de audiencia de persona puede tener uno de estos dos tipos de entrada de audiencia: una lista de personas estática o una lista de personas dinámica.

Si la lista de personas dinámicas que necesita para el recorrido de personas no existe, [cree la lista de personas](../audiences/people-lists.md#create-a-people-list) y, a continuación, configure el nodo de audiencia de persona.

_Para configurar la audiencia de recorrido :_

1. Haga clic en el nodo **[!UICONTROL Audiencia de personas]**.

   Esta acción muestra las propiedades del nodo a la derecha.

   ![Nodo de recorrido de audiencia de persona](./assets/person-audience-node-properties.png){width="500" zoomable="yes"}

1. Utilice una de las siguientes opciones de configuración de audiencia para la audiencia de persona:

   * **[!UICONTROL Lista dinámica]**: use una lista de personas dinámica y basada en reglas. Las reglas de la lista se evalúan durante el tiempo de ejecución del recorrido para calificar a los miembros del recorrido. Las personas que posteriormente no cumplan los requisitos para la lista dinámica no se eliminarán del recorrido. Consulte _[Listas dinámicas](../audiences/people-lists.md#dynamic-lists)_.

   * **[!UICONTROL Audiencia de eventos]**: use una audiencia de eventos para definir la audiencia de recorrido en función de los eventos calificados. Defina los miembros de la audiencia mediante el filtrado de perfil de persona y la entrada de recorrido de déclencheur mediante criterios de evento. Ver _[audiencias basadas en eventos](../audiences/event-based-audiences.md)_.
