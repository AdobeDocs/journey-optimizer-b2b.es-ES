---
title: Nodo de Recorrido de Audiencia de persona
description: Página de marcador de posición para recorridos de persona.
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ba367494-9862-4596-bd6f-299c7e10a46bid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: b7cb8c2a43b8a562e55923d709f518b8f1d74b2a
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Nodo de audiencia de persona

El nodo _audiencia de persona_ especifica qué perfiles de persona entran en el recorrido. Cuando [crea un recorrido de persona](./person-journeys.md), el recorrido siempre comienza con un nodo de audiencia de persona que define su entrada. El nodo de audiencia de persona puede tener uno de estos dos tipos de entrada de audiencia: una lista de personas estática o una lista de personas dinámica.

Si la lista de personas que necesita para el recorrido de personas aún no existe, [cree la lista de personas](../audiences/audience-management.md#create-a-people-list) y, a continuación, configure el nodo de audiencia Persona.

## Definición de la audiencia para el nodo de audiencia de la persona

1. Haga clic en el nodo **[!UICONTROL Audiencia de personas]**.

   Esta acción muestra las propiedades del nodo a la derecha.

   <!-- ![Person audience journey node](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"} -->

1. En el panel de propiedades del nodo de la derecha, utilice una de las siguientes opciones de entrada para el nodo de recorrido de audiencia de persona:

   * **[!UICONTROL Lista dinámica]**: use una lista de personas dinámica y basada en reglas. Las reglas de la lista se evalúan durante el tiempo de ejecución del recorrido para calificar a los miembros del recorrido. Las personas que posteriormente no cumplan los requisitos para la lista dinámica no se eliminarán del recorrido.

   * **[!UICONTROL Lista estática]**: usa una lista estática de personas como miembro de tu recorrido. La pertenencia a la lista actual se evalúa durante el tiempo de ejecución del recorrido para calificar a los miembros para el recorrido. Las personas que posteriormente se quiten de la lista estática no se quitarán de la recorrido.

