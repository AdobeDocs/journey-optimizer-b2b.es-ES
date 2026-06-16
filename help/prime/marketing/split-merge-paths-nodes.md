---
title: Dividir y combinar nodos de rutas
description: Marcador de posición
autotag-review: '2026-06-12T23:04:27.208Z'
TQID: 'https://experienceleague.adobe.com/TZlkuuES1Q2ZlG-ND-tIu6cVBRA65hIfotDcroER9Mc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 569
ht-degree: 0%

---

# Dividir y combinar nodos de rutas



## Dividir nodos de rutas

Utilice los nodos divididos para segmentar a las personas según las condiciones que defina. Cree rutas para la lista de audiencias según las condiciones, defina cada ruta con nodos de acción y evento para el segmento y, a continuación, combine las rutas y continúe con el recorrido.

Un nodo de Rutas divididas define una o más rutas segmentadas en función de los filtros de personas.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_&#x200B;**Funcionamiento de un nodo de ruta dividida por personas**&#x200B;_

* La evaluación de cada ruta es de arriba abajo. Si una persona coincide para la primera y la segunda ruta, solo continúa por la primera ruta.
* El nodo admite la definición de una ruta de acceso de _Otras personas_, donde puede agregar acciones o eventos para las personas que no coincidan con uno de los segmentos o rutas definidos.

### Filtros coincidentes

Para cada ruta definida para el nodo, utilice los siguientes tipos de filtros para hacer coincidir personas según una o más condiciones:

* Historial de actividades: puede definir una ruta según la actividad de la persona relacionada con lo siguiente:

   * Mensajes de correo electrónico
   * Cambio en el valor de los datos

* Atributos de persona: defina una condición según los atributos de una persona, como el país, el puesto o la pertenencia a una lista.

### Adición de un nodo de rutas divididas

<!--
>[!NOTE]
>
>When you split paths by people, a _Close split paths_ node is automatically inserted to end the split. A split-by-people path allows only _Take an action_ on people nodes.
-->

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Dividir rutas]**.

   <!-- ![Add journey node - split paths](./assets/add-node-split.png){width="300" zoomable="no"} -->

1. Para definir una condición aplicable a _[!UICONTROL Ruta 1]_, haga clic en **[!UICONTROL Aplicar condición]**.

1. En el editor de condiciones, añada uno o más filtros para definir la ruta dividida.

   * Arrastre y suelte cualquiera de los filtros de personas desde la navegación izquierda y complete la definición de la coincidencia.

   * Ajuste las condiciones aplicando la **[!UICONTROL lógica de filtro]** en la parte superior. Puede elegir hacer coincidir todas las condiciones o cualquier condición.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * Haga clic en **[!UICONTROL Finalizado]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]** y repita los pasos anteriores para agregar las condiciones aplicables a la ruta.

   También puede etiquetar cada ruta en función de estas condiciones o utilizar las etiquetas predeterminadas.

1. Si es necesario, reordene las rutas según la prioridad que desee para la división.

   El filtrado de rutas se evalúa en orden descendente. Cada persona continúa por el primer camino que coincida.

   Haga clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista de rutas.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. Habilite la opción **[!UICONTROL Otras personas]** para agregar una ruta predeterminada para las personas que no coinciden con las rutas definidas.

   Cuando esta opción no está habilitada, las personas que no coinciden con un segmento o ruta definida pasan la división y continúan con el siguiente paso del recorrido.

Cuando haya definido condiciones para cada ruta, puede añadir nodos de acción o de evento que desee aplicar a las personas de una ruta.

## Combinar nodos de rutas

1. Vaya al mapa de recorrido y busque el nodo de rutas divididas con dos o más rutas.

   Cada ruta debe tener una combinación de acciones y eventos en cada ruta.

1. Haga clic en el icono de signo más ( **+** ) al final de cualquiera de estas rutas y elija **[!UICONTROL Combinar rutas]** entre las opciones que se muestran.

   <!-- ![Journey node - merge paths](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"} -->

1. En las propiedades del nodo a la derecha, seleccione las rutas que desee combinar.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   En este punto, las rutas se combinan para que las personas de las rutas seleccionadas se combinen en una sola ruta que pueda continuar avanzando a través del recorrido.

1. Si es necesario, puede anular la combinación de rutas volviendo a las propiedades del nodo de rutas de combinación y desactivando la casilla de verificación de las rutas que desee eliminar.