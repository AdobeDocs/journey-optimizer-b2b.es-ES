---
title: Intereses de solución
description: Obtenga información acerca de los intereses de las soluciones y cómo puede definirlos para usarlos en sus grupos de compra.
feature: Buying Groups, Account Journeys
exl-id: b7dfddac-ed29-4870-b853-5e520a4cdf12
source-git-commit: 92f28ab633cc1f6e5e0172dff69869fcc718e2e8
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Intereses de solución

Antes de crear grupos de compra, debes saber qué estás vendiendo y a quién quieres dirigir. Su estrategia de marketing y ventas debe estar alineada para que pueda añadir el interés de la solución para los grupos de compra.

## Acceder y examinar los intereses de la solución

1. En la página de inicio de Adobe Experience Platform, haga clic en Adobe Journey Optimizer B2B Edition.

1. En el panel de navegación izquierdo, haz clic en **[!UICONTROL Comprar grupos]**.

1. En la página Grupos de compra, seleccione la pestaña **[!UICONTROL Interés de la solución]**.

   ![Ficha Interés de la solución](assets/solution-interest-tab.png){width="700" zoomable="yes"}

   La pestaña proporciona una lista de inventario de todos los intereses de la solución existentes. Proporciona información como _[!UICONTROL Nombre]_, _[!UICONTROL Plantilla de roles]_, _[!UICONTROL Comprar trabajos de creación de grupos]_, _[!UICONTROL Última actualización el]_, _[!UICONTROL Actualizado el]_, _[!UICONTROL Creado el]_ y _[!UICONTROL Creado el]_ en formato de columna.

   La lista está ordenada de forma predeterminada por la columna _[!UICONTROL Última actualización el]_. Haga clic en el título de la columna en el encabezado para alternar el orden entre descendente y ascendente.

## Ver y eliminar trabajos de grupos de compra

Desde la pestaña _[!UICONTROL Interés de la solución]_, la columna **[!UICONTROL Trabajos de creación de grupos de compra]** muestra el recuento de trabajos creados para cada interés de solución. El número es un vínculo y, al hacer clic en él, se abre un cuadro de diálogo que muestra la lista de trabajos creados para el interés de la solución.

![Comprando trabajos de grupo por interés de solución](assets/buying-group-jobs-for-solution-interest.png){width="700" zoomable="yes"}

Para eliminar un trabajo de un grupo de compradores, haga clic en los puntos suspensivos (...) junto al nombre del trabajo y elija **[!UICONTROL Eliminar]**.

## Crear un interés de solución

Antes de crear un interés de solución, debe tener una plantilla de funciones activa (publicada) que defina las funciones que desea segmentar. Consulte [Comprar plantillas de rol de grupo](./buying-groups-role-templates.md) para obtener más información sobre cómo crear una plantilla de roles y publicar una plantilla de roles.

1. En la ficha _[!UICONTROL Interés de la solución]_, haga clic en **[!UICONTROL Crear interés de la solución]** en la parte superior derecha.

1. Escriba un **[!UICONTROL Nombre]** único (obligatorio) y una **[!UICONTROL Descripción]** (opcional).

1. Elija una **[!UICONTROL plantilla de roles]** (obligatorio).

   Haga clic en el selector y elija una plantilla de funciones activa en la lista mostrada. Solo puede asociar una plantilla de roles activa con un interés de solución.

   ![Ficha Interés de la solución](assets/solution-interest-create.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Crear]** en la esquina superior derecha.

   El nuevo interés de la solución se muestra en Intereses de la solución

## Editar el interés de una solución

En cualquier momento, puede cambiar el nombre y la descripción de una solución de interés. La plantilla de funciones no se puede cambiar debido a la dependencia de los grupos de compra en función del emparejamiento de interés de solución y plantilla de función. En este caso, debe crear un nuevo interés de solución utilizando otra plantilla de funciones.

1. En la ficha _[!UICONTROL Interés de la solución]_, utilice uno de los siguientes métodos para abrir las propiedades del interés de la solución que desee editar:

   * Haga clic en el nombre de interés de la solución.
   * Haga clic en los puntos suspensivos (**...**) junto a él y elija **[!UICONTROL Editar]**.

   ![Menú más de interés para la solución](assets/solution-interests-more-menu.png){width="500" zoomable="no"}

1. Si es necesario, actualice el nombre (obligatorio y único) y la descripción (opcional).

1. Si es necesario, cambia la configuración **[!UICONTROL Actualizar grupos de compras existentes]**.

   Cuando esta opción está habilitada, todos los grupos de compra existentes vinculados con el interés de la solución se actualizan a través del ciclo de sincronización de 24 horas.

1. Haga clic en **[!UICONTROL Guardar]**.

## Eliminar un interés de solución

No se puede eliminar ningún interés de solución que esté actualmente en uso por ningún trabajo de grupo de compra o recorrido de cuenta. Además, no se puede recuperar un interés de solución eliminado.

1. En la ficha _[!UICONTROL Interés de la solución]_, haga clic en los puntos suspensivos (**...**) junto al interés de la solución y elija **[!UICONTROL Eliminar]**.

   Esta acción abre un cuadro de diálogo de confirmación.

   Si un recorrido de cuentas o un trabajo de grupo de compra está utilizando actualmente el interés de la solución, la acción abre un cuadro de diálogo informativo que le advierte de que no se puede eliminar. Haga clic en [!UICONTROL Aceptar], lo que anula la eliminación.

1. Haga clic en **[!UICONTROL Eliminar]** para confirmar la eliminación, o bien puede anular el proceso haciendo clic en _[!UICONTROL Cancelar]_.
