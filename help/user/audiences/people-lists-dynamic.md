---
title: Listas dinámicas de personas
description: Defina reglas de pertenencia y duplique listas dinámicas de personas en Journey Optimizer B2B Edition.
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
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 2%
---

# Listas de personas dinámicas

Una [lista de personas](./people-lists.md) dinámica es una colección de perfiles de personas definidos por reglas (filtros). La pertenencia a listas dinámicas se define mediante filtros simples que hacen referencia a atributos y actividades de la persona. La pertenencia se mantiene automáticamente tal y como califican y descalifican los perfiles según la lógica del filtro.

No puede agregar ni quitar personas individuales de una lista dinámica. Para cambiar el abono a la lista, actualice sus reglas. Si necesita administrar la suscripción manualmente o mediante un recorrido, use una [lista estática](./people-lists-static.md).

## Establecer reglas de pertenencia {#set-membership-rules}

>[!NOTE]
>
>Una lista dinámica sin reglas no tiene miembros. Para rellenar la lista, añada al menos un filtro.

1. Abra la lista dinámica y seleccione la ficha **[!UICONTROL Reglas]**.

1. Haga clic en **[!UICONTROL Editar reglas]**.

   ![Reglas de acceso para crear una lista dinámica de personas](./assets/people-list-dynamic-rules-edit.png){width="700" zoomable="yes"}

1. En el cuadro de diálogo _[!UICONTROL Editar reglas]_, defina las reglas para calificar perfiles arrastrando filtros desde el panel izquierdo.

   Califique perfiles para la lista utilizando cualquier combinación de:

   * Historial de actividad
   * [!DNL Experience Platform] campos de persona habilitados
   * Campos personalizados
   * Datos de intención
   * Atributos de la persona
   * Filtros especiales, como abono a recorridos

   Para cada filtro que agregue, haga clic en **[!UICONTROL Agregar restricciones]** para restringir los criterios coincidentes. Ajuste las condiciones aplicando la **[!UICONTROL lógica de filtro]** en la parte superior. Puede elegir hacer coincidir todas las condiciones, cualquier condición o definir una lógica avanzada.

   ![Agregar filtros con restricciones para rellenar la lista dinámica](./assets/people-list-dynamic-rules-edit-filter.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Listo]** para guardar los cambios.

   La ficha **[!UICONTROL Reglas]** muestra los filtros y la lógica de filtro de la lista, y la ficha **[!UICONTROL Miembros]** se actualiza para reflejar la pertenencia actualizada. Para encontrar las cualificaciones de audiencia más actualizadas, usa **[!UICONTROL Actualizar miembros]** en el menú **[!UICONTROL Más]**.

1. Seleccione la ficha **[!UICONTROL Miembros]**.

   Los miembros que cumplen los requisitos aparecen en la lista después de un breve retraso.

   ![Miembros generados para una lista dinámica de personas](./assets/people-list-dynamic-members.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Para cambiar las reglas de la lista en cualquier momento, puede repetir estos pasos. La inscripción a la lista se actualiza en función de los filtros guardados.

<!--

## Duplicate a dynamic list {#duplicate-dynamic-list}

Duplicating a dynamic list replicates its membership filtering so that you can reuse it in a different context.

1. In the _[!UICONTROL Dynamic lists]_ tab, click the _More menu_ ( **...** ) icon next to the list and choose **[!UICONTROL Duplicate]**.

1. Enter a unique **[!UICONTROL Name]** (required) and a **[!UICONTROL Description]** (optional).

   By default, the dialog appends `_copy` to the name of the originating list. Enter a different unique name as needed.

   ![Duplicate list dialog](./assets/people-list-duplicate-dialog.png){width="375"}

1. Click **[!UICONTROL Duplicate]**.
-->
