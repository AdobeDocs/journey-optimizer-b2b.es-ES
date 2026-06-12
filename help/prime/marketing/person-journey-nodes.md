---
title: Añadir nodos de Recorrido
description: Página de marcador de posición para nodos de recorrido de personas.
autotag-review: '2026-06-12T23:02:52.147Z'
TQID: 'https://experienceleague.adobe.com/sTnrOvrGIrgboPqOMrrkUvNU1y6zZJX42zEJxuUInKQ'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 2%

---

# Adición de nodos de recorrido

Después de crear el recorrido de una persona, añada la audiencia y genere el recorrido con los nodos. El mapa de recorrido proporciona un lienzo en el que puede crear sus casos de uso de marketing B2B de varios pasos.

El nodo _[!UICONTROL Audiencia de persona]_ es automáticamente el primer nodo del recorrido. Después de seleccionar la audiencia, cree su recorrido combinando los diferentes nodos de acción, evento y destino como un escenario de varios pasos y canales. Cada nodo de un recorrido representa un paso a lo largo de una ruta lógica.

## Nodo de audiencia de persona

El nodo de audiencia de persona especifica qué registros de persona entran en el recorrido. Cuando se crea un recorrido de persona, el recorrido siempre comienza con un nodo de audiencia de persona que define su entrada.

1. Haga clic en el nodo para seleccionarlo.
1. En el panel de propiedades del nodo de la derecha, utilice una de las siguientes opciones de entrada para el nodo de recorrido de audiencia de persona:

   * **[!UICONTROL Lista dinámica]**: use una lista de personas dinámica y basada en reglas. Las reglas de la lista se evalúan durante el tiempo de ejecución del recorrido para calificar a los miembros del recorrido. Las personas que posteriormente no cumplan los requisitos para la lista dinámica no se eliminarán del recorrido.

   * **[!UICONTROL Lista estática]**: usa una lista estática de personas como miembro de tu recorrido. La pertenencia a la lista actual se evalúa durante el tiempo de ejecución del recorrido para calificar a los miembros para el recorrido. Las personas que posteriormente se quiten de la lista estática no se quitarán de la recorrido.

## Nodos de acción Personas

En el recorrido de una persona, utilice una acción para las personas cuando desee aplicar un cambio a todas las personas de la ruta del nodo. Para un recorrido de cuentas, este tipo de nodo se puede utilizar dentro de la ruta dividida por personas o por cuentas.

### Acciones y restricciones

| Acción | Restricciones |
| ------ | ---------- |
| **[!UICONTROL Enviar correo electrónico]** | <li>Crear correo electrónico <li>Optimización del tiempo de envío (opcional) |
| **[!UICONTROL Cambiar valor de datos]** | <li>Seleccionar atributo de persona <li>Establecer nuevo valor |

### Añadir un nodo de acción

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Realizar una acción]**.

1. En las propiedades del nodo, a la derecha, seleccione una acción de la lista y establezca los valores para la acción.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL Enviar correo electrónico]

Utilice esta acción para enviar un correo electrónico. Después de crear el correo electrónico para el nodo, puede diseñar, personalizar y previsualizar mensajes de correo electrónico en el espacio de diseño de correo electrónico (consulte [Creación de correo electrónico](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Puede usar [Optimización del tiempo de envío](../marketing/email-send-time-optimization.md) para personalizar el tiempo de envío del correo electrónico mediante la predicción de cuándo es más probable que se involucre cada perfil.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Cambiar valor de datos]

Utilice esta acción para cambiar el valor de un atributo de perfil de persona en la base de datos. Seleccione el atributo y, a continuación, establezca el nuevo valor.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++

## Nodos de eventos

Agregue el nodo _Listen for an event_ para mover la audiencia hacia adelante al siguiente paso del recorrido cuando se produzca un evento.

### Filtros de eventos de personas

| Filtros | Descripción |
| ------- | ----------- |
| Historial de actividades > Correo electrónico | Actividades de correo electrónico basadas en condiciones que se evalúan mediante uno o varios mensajes de correo electrónico seleccionados: <li>Hizo clic en el vínculo del correo electrónico <li>Abrió el email |
| Historial de actividades > Valor de los datos cambiado | Se ha producido un cambio de valor en un atributo de persona seleccionado. Estos tipos de cambio incluyen: <li>Nuevo valor <li>Valor anterior <li>Razón <li>Origen <li>Fecha de la actividad <li> Mín. número de veces |

### Adición de un nodo de evento

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para el tipo de evento.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. Seleccione un evento de la lista.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

>[!NOTE]
>
>La funcionalidad de tiempo de espera para Escuchar para un nodo de evento no funciona actualmente y se habilitará en una fase posterior.

## Dividir nodos de rutas

Utilice los nodos divididos para segmentar a las personas según las condiciones que defina. Cree rutas para la lista de audiencias según las condiciones, defina cada ruta con nodos de acción y evento para el segmento y, a continuación, combine las rutas y continúe con el recorrido.

Un nodo de Rutas divididas define una o más rutas segmentadas en función de los filtros de personas.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_**Funcionamiento de un nodo de ruta dividida por personas**_

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
