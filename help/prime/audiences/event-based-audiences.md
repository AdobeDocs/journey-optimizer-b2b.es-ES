---
title: Audiencias basadas en eventos
description: Utilice audiencias basadas en eventos en Journey Optimizer B2B Prime para almacenar en déclencheur la entrada de recorrido de personas en tiempo casi real según las actividades de Marketo Engage.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-25T17:59:01.953Z'
TQID: 'https://experienceleague.adobe.com/04J58rjKw0hCoTOeYheZIPaX-YR8GwP-k6-Wn3XCetU'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a48a12635d2ba4f14dda49e25e79a5496ebbdecf
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 3%

---

# Audiencias basadas en eventos

En [!DNL Adobe Journey Optimizer B2B Prime], las _audiencias basadas en eventos_ le permiten agregar miembros de audiencia a un [recorrido de personas](../marketing/person-journeys.md) en tiempo casi real cuando se produce una actividad de [!DNL Marketo Engage]. Las audiencias basadas en eventos se configuran en el nodo Audiencia del lienzo de recorrido:

* Seleccione una o más actividades de Marketo (estándar o personalizadas) como eventos calificados.
* Si lo desea, puede añadir filtros de perfil de persona (como sector, región o fase del ciclo vital) para reducir el número de personas que pueden acceder.
* Si lo desea, puede definir restricciones de atributo de actividad (como un formulario, una URL o un programa específicos) para reducir los eventos de cada actividad que cumplen los requisitos.

Cuando una actividad correspondiente se registra en [!DNL Marketo Engage] para un posible cliente y se replica en [!DNL Adobe Journey Optimizer B2B Prime], el sistema evalúa el registro de persona correspondiente en función de los filtros y restricciones configurados. Si se cumplen las condiciones, la persona entra en el recorrido inmediatamente a través del nodo Audience.

_Para definir una audiencia basada en eventos para el recorrido de una persona :_

1. Seleccione el nodo [_Audiencia de persona_](../marketing/person-audience-node.md).

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Audiencia de eventos]** como tipo de entrada.

   ![Nodo de recorrido de audiencia de persona establecido en audiencia basada en evento](./assets/event-based-audience-node.png){width="400"}

1. Haga clic en **[!UICONTROL Agregar criterios de evento]**.

1. En el cuadro de diálogo _[!UICONTROL Editar criterios del evento]_, agregue una o más actividades [!DNL Marketo Engage] como eventos calificadores, como:

   * _Asiste al seminario web_
   * _Se ha entregado el correo electrónico_
   * _Clics en el vínculo del correo electrónico_

   >[!NOTE]
   >
   >También puede seleccionar actividades personalizadas definidas en la instancia [!DNL Marketo Engage] asociada.

   Establezca el operador y los valores coincidentes para cada actividad.

   ![déclencheur de actividad para una audiencia basada en eventos](./assets/event-based-audience-triggers.png){width="700" zoomable="yes"}

   Una persona se califica para el recorrido cuando cualquiera de esas actividades configuradas se registra para ese posible cliente.

1. (Opcional) Para utilizar una combinación de eventos y filtros para la calificación de audiencias, agregue filtros de nivel de persona.

   * Seleccione la ficha **[!UICONTROL Filtros]**.
   * Arrastre cada filtro y defina los criterios coincidentes.

   ![Filtros de persona para una audiencia basada en eventos](./assets/event-based-audience-filters.png){width="700" zoomable="yes"}

   Si agrega filtros, la persona debe satisfacer al menos una condición de actividad configurada y los filtros configurados.

1. Haga clic en **[!UICONTROL Guardar]**.
