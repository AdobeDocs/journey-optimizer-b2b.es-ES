---
title: Listas de personas estáticas
description: Agregar y quitar miembros de listas de personas estáticas en Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 2%
---

# Listas de personas estáticas

Una [lista de personas](./people-lists.md) estática es una colección de perfiles de persona cuya pertenencia cambia solamente cuando agrega o quita personas. Los filtros simples que hacen referencia a atributos y actividades de personas definen la pertenencia a listas estáticas. La pertenencia sólo cambia cuando se agregan o se quitan miembros. Puede hacer lo siguiente:

* [Agregar personas](#static-list-add-members) al aplicar un conjunto de filtros que se evalúa una vez, cuando lo aplica.
* Agregar y quitar personas mediante un recorrido de cuenta o persona, con las acciones [!UICONTROL Agregar a la lista de personas] y [!UICONTROL Quitar de la lista de personas]. (Ver [Usar listas de personas en recorridos](./people-lists-journeys.md))
<!-- * [Activate the list to a destination](#static-list-activate) to sync its membership downstream. -->

>[!NOTE]
>
>Las definiciones de filtros de listas estáticas se aplican una vez, cuando se agregan miembros a la lista. El filtro definido no está disponible posteriormente. Si desea mantener una definición de audiencia coherente mediante filtros, use una [lista dinámica](./people-lists-dynamic.md).

## Añadir miembros {#static-list-add-members}

>[!NOTE]
>
>Si desea que una lista estática empiece a estar vacía, no aplique filtros. Una lista estática vacía resulta útil cuando planea agregar miembros mediante recorridos.

1. Abra la lista estática y haga clic en **[!UICONTROL Agregar personas]** en la parte superior derecha.

   ![Agregar personas a una lista de personas estática](./assets/people-list-static-add-people.png){width="700" zoomable="yes"}

1. En el cuadro de diálogo _[!UICONTROL Agregar personas]_, defina las reglas para calificar perfiles arrastrando filtros desde el panel izquierdo.

   Filtre perfiles con cualquier combinación de:

   * Historial de actividad
   * Campos de persona habilitados para Experience Platform
   * Campos personalizados
   * Datos de intención
   * Atributos de la persona
   * Filtros especiales, como abono a recorridos

   Los filtros están anidados en carpetas de categoría. Expanda cada carpeta y desplácese por los filtros disponibles, o use el campo _Buscar_ de la parte superior para encontrar el filtro que necesita. Para cada filtro que agregue:

   * Arrastre el filtro desde el panel izquierdo al espacio de definición del filtro.
   * Complete la definición de evaluación de coincidencias.
   * Haga clic en **[!UICONTROL Agregar restricciones]** para restringir los criterios coincidentes.

   Ajuste las condiciones aplicando la **[!UICONTROL lógica de filtro]** en la parte superior. Puede elegir hacer coincidir todas las condiciones, cualquier condición o definir una lógica avanzada.

   ![Agregar filtros con restricciones para agregar personas a la lista estática](./assets/people-list-static-add-people-filters.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Listo]** para guardar los cambios.

   El sistema procesa la solicitud y muestra un mensaje de confirmación cuando se añaden personas. El tiempo de procesamiento depende del número de personas que se evalúen y de los criterios de filtro seleccionados. A medida que la lista se siga rellenando, use **[!UICONTROL Actualizar miembros]** en el menú _[!UICONTROL Más]_ para actualizar la lista.

   Los miembros que cumplen los requisitos aparecen en la lista después de un breve retraso. El conjunto de filtros se evalúa una vez, por lo que las personas que posteriormente coincidan con los filtros no se añaden automáticamente. Puede repetir este proceso en cualquier momento para agregar más personas a la lista.

   ![Miembros para una lista de personas estática](./assets/people-list-static-members.png){width="700" zoomable="yes"}

## Quitar miembros {#static-list-remove-members}

Puede quitar personas de una lista estática automáticamente mediante un recorrido con la acción [!UICONTROL Quitar de la lista de personas]. (Ver [Usar listas de personas en recorridos](./people-lists-journeys.md))

<!--
TODO: Restore this section when the activate to a destination function is released.

## Activate to a destination {#static-list-activate}

Activating a static people list sends its membership to a connected destination, with ongoing sync instead of a one-time export. This is useful for paid media targeting, suppression, and downstream orchestration.

* The static list acts as a container for the people.
* The activation sends and syncs that membership to a destination.
* People added to the list later are propagated automatically.
* People removed later are deactivated automatically.

>[!PREREQUISITES]
>
>You must have one or more configured destinations for your [!DNL Journey Optimizer B2B Edition] sandbox before you can activate a static list to a destination. See [Destinations](./destinations.md).

1. Select the **[!UICONTROL Static lists]** tab.

1. Locate the static list that you want to activate, click the _More menu_ ( **...** ) icon next to the list, and choose **[!UICONTROL Activate to destination]**.

   ![Access the More menu for a static people list](./assets/people-lists-static-more-menu.png){width="450"}

   You can also open the static list and use the **[!UICONTROL More]** menu at the top right.

1. Select the check box for the configured destination connection.

   ![Configured destinations available for activation](./assets/people-list-activate-destination-select.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

1. In the _[!UICONTROL Activate list to destination]_ dialog, click **[!UICONTROL Activate]** to confirm.

When activation completes, a confirmation message appears and the destination shows as **[!UICONTROL Active]** on the **[!UICONTROL Destinations]** tab of the list. You can activate a static list to more than one destination at a time. Membership syncs to all of them.

To review the destinations that a static list is activated to, open the list and select the **[!UICONTROL Destinations]** tab.

### Deactivate a destination {#deactivate-destination}

Remove a destination connection from a static list when you no longer want its membership synced downstream.

1. Open the static list and select the **[!UICONTROL Destinations]** tab.

1. Use the row action to remove the destination that you want to disconnect.

1. Confirm in the _[!UICONTROL Deactivate destination]_ dialog.

Deactivating removes the destination from the list. The people in the list are also removed from the connected destination audience.

-->
