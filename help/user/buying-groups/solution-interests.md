---
title: Intereses de solución
description: Conozca los intereses de la solución y cómo puede definirlos para usarlos dentro de sus grupos de compra.
feature: Buying Groups, Account Journeys
role: User
exl-id: b7dfddac-ed29-4870-b853-5e520a4cdf12
source-git-commit: 1280bd6a4a889507fcede73a859e943cbe3c0674
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 1%

---

# Interés de la solución

Antes de crear grupos compradores, debes saber qué estás vendiendo y a quién quieres dirigir. Su estrategia de marketing y ventas debe estar alineada para que pueda añadir el interés de la solución para los grupos de compra.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

## Acceder y examinar los intereses de la solución

1. En el panel de navegación izquierdo, haz clic en **[!UICONTROL Comprar grupos]**.

1. En la página _[!UICONTROL Grupos de compra]_, seleccione la pestaña **[!UICONTROL Interés de la solución]**.

   La pestaña proporciona una lista de inventario de todos los intereses de la solución existentes. Muestra la siguiente información en formato de columna: _[!UICONTROL Nombre]_, _[!UICONTROL Plantilla de roles]_, _[!UICONTROL Trabajos de creación de grupos de compras]_, _[!UICONTROL Actualizar grupos de compras]_, _[!UICONTROL Fecha de creación]_, _[!UICONTROL Creado por]_, _[!UICONTROL Última actualización]_ y _[!UICONTROL Última actualización por]_,

   La lista está ordenada de forma predeterminada por la columna _[!UICONTROL Última actualización]_. Haga clic en el título de la columna en el encabezado para alternar el orden entre descendente y ascendente.

   Escriba texto en la herramienta _Buscar_ situada en la parte superior de la lista para filtrar la lista mostrada por nombre.

   ![Ficha Interés de la solución](assets/solution-interest-tab.png){width="700" zoomable="yes"}

## Ver y eliminar trabajos de grupos de compra

En la ficha _[!UICONTROL Interés de la solución]_, la columna **[!UICONTROL Trabajos de creación de grupos de compra]** muestra el recuento de trabajos creados para cada interés de solución. Haga clic en el número para abrir un cuadro de diálogo que muestre la lista de trabajos creados para el interés de la solución.

![Comprando trabajos de grupo por interés de solución](assets/buying-group-jobs-for-solution-interest.png){width="700" zoomable="yes"}

Para eliminar un trabajo de un grupo de compradores, haga clic en los puntos suspensivos (...) junto al nombre del trabajo y elija **[!UICONTROL Eliminar]**.

## Crear un interés de solución

Antes de crear un interés de solución, debe tener una plantilla de funciones activa (publicada) que defina las funciones que desea segmentar. Consulte [Comprar plantillas de rol de grupo](./buying-groups-role-templates.md) para obtener más información sobre cómo crear una plantilla de roles y publicar una plantilla de roles.

1. En la ficha _[!UICONTROL Interés de la solución]_, haga clic en **[!UICONTROL Crear interés de la solución]** en la parte superior derecha.

1. Escriba un **[!UICONTROL Nombre]** único (obligatorio) y una **[!UICONTROL Descripción]** (opcional).

1. Elija una **[!UICONTROL plantilla de roles]** (obligatorio).

   Haga clic en **[!UICONTROL Seleccionar plantilla de roles]** y elija una plantilla de roles activa en la lista del cuadro de diálogo. Solo puede asociar una plantilla de funciones activas con un interés de solución. Haga clic en **[!UICONTROL Guardar]** para volver a la página _[!UICONTROL Crear interés de solución]_, en la que se muestra la plantilla de roles seleccionada.

   ![Agregar una plantilla de funciones al interés de la solución](assets/solution-interest-create.png){width="700" zoomable="yes"}

1. Seleccione el **[!UICONTROL modelo de fase de grupo de compra]** para usar la progresión de fase de grupo de compra (opcional).

   Para obtener más información acerca del uso de fases de grupos de compras para realizar el seguimiento de la progresión de cuentas, consulte [Fases de grupos de compras](./buying-group-stages.md).

1. Habilitar la configuración **[!UICONTROL Actualizar grupos de compras existentes]** (opcional).

   Cuando esta opción está habilitada, todos los grupos de compra existentes asociados con el interés de la solución se actualizan a través del ciclo de sincronización de 7 días.

1. Haga clic en **[!UICONTROL Crear]** en la esquina superior derecha.

   El nuevo interés de la solución se muestra en la lista _[!UICONTROL Intereses de la solución]_.

## Editar el interés de una solución

En cualquier momento, puede cambiar el nombre y la descripción de una solución de interés. La plantilla de funciones no se puede cambiar debido a la dependencia de los grupos de compra en función del emparejamiento de interés de solución y plantilla de función. En este caso, debe crear un nuevo interés de solución utilizando otra plantilla de funciones.

1. En la ficha _[!UICONTROL Interés de la solución]_, utilice uno de los siguientes métodos para abrir las propiedades del interés de la solución que desee editar:

   * Haga clic en el nombre de interés de la solución.
   * Haga clic en los puntos suspensivos (**...**) junto a él y elija **[!UICONTROL Editar]**.

   ![Menú más de interés para la solución](assets/solution-interests-more-menu.png){width="500" zoomable="no"}

1. Realice las actualizaciones necesarias en la configuración de intereses de la solución:

   * Actualice **[!UICONTROL Name]** y **[!UICONTROL Description]**.

   * Seleccione el **[!UICONTROL modelo de fase de grupo de compra]** que se usa para rastrear la progresión de fase de grupo de compra.

     Para obtener más información acerca del uso de fases de grupos de compras para realizar un seguimiento de la progresión de los recorridos en comparación con las ventas, consulte [Fases de grupos de compras](./buying-group-stages.md).

   * Cambiar la configuración de **[!UICONTROL Actualizar grupos de compras existentes]**.

     Cuando esta opción está habilitada, todos los grupos de compra existentes asociados con el interés de la solución se actualizan a través del ciclo de sincronización de 7 días.

1. Haga clic en **[!UICONTROL Guardar]**.

## Eliminar un interés de solución

No se puede eliminar ningún interés de solución que esté actualmente en uso por ningún trabajo de grupo de compra o recorrido de cuenta. Además, no se puede recuperar un interés de solución eliminado.

1. En la ficha _[!UICONTROL Interés de la solución]_, haga clic en los puntos suspensivos (**...**) junto al interés de la solución y elija **[!UICONTROL Eliminar]**.

   Esta acción abre un cuadro de diálogo de confirmación.

   Si un trabajo de grupo de compra o recorrido de cuentas está utilizando actualmente el interés de la solución, la acción generará un aviso que indica que no se puede eliminar. Haga clic en **[!UICONTROL Aceptar]**, lo que anula la eliminación.

1. Haga clic en **[!UICONTROL Eliminar]** para confirmar la eliminación, o bien puede anular el proceso haciendo clic en _[!UICONTROL Cancelar]_.

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3433080/?learn=on)
