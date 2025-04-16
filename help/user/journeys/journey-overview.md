---
title: Recorridos de cuenta
description: Obtenga información acerca de los recorridos de cuenta y cómo puede crearlos y administrarlos.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: bd6f998b610c6f3a4d7c0e1fce5db4bb72b8a1e3
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 30%

---


# Recorridos de cuenta

With account journeys, you can streamline demand generation and buying group qualification and drive more qualified demand for your acquisition, upsell/cross-sell, and retention programs. Tailor your journeys for each buying group and buying group member using automated engagement across email, SMS, events, and more.

Defina un compromiso basado en las ventas que incluya correo electrónico, SMS y más recorridos de cuenta interna para coordinar el marketing entrante con las actividades de ventas salientes de cada miembro del grupo de compras.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

## Introducción a un recorrido

Para empezar a usar los recorridos de cuenta:

1. [Crear un recorrido](./create-publish-journey.md#create-an-account-journey).
1. [Añada los nodos](./create-publish-journey.md#add-a-node) y [defina el flujo del recorrido](./create-publish-journey.md#add-and-delete-a-path) en el mapa del recorrido.
1. [Publicación del recorrido](./create-publish-journey.md#publish-an-account-journey).

## Acceso y exploración de recorridos de cuenta

1. En la página de inicio de Adobe Experience Platform, haga clic en Adobe Journey Optimizer B2B Edition.

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL recorridos de cuenta]**.

   ![Acceso a recorridos de cuenta](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   La página de recorridos mostrada incluye las siguientes columnas:

   * [!UICONTROL Nombre] (haga clic en el nombre para abrir el recorrido y editarlo)
   * [!UICONTROL Estado]
   * [!UICONTROL Descripción]
   * [!UICONTROL Creado por]
   * [!UICONTROL Última actualización el ]
   * [!UICONTROL Última actualización]
   * [!UICONTROL Publicado el]
   * [!UICONTROL Publicado por]

Use la herramienta _Buscar_ de la parte superior para localizar el recorrido por su nombre. Puede ordenar la lista por _[!UICONTROL Estado]_ al hacer clic en el encabezado de columna.

Puede personalizar las columnas que se muestran en la tabla haciendo clic en el icono _Personalizar tabla_ ( ![Personalizar tabla](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha. Select or clear the checkboxes in the dialog and click **[!UICONTROL Apply]**.

![Elija las columnas que desea mostrar en la lista de recorridos de la cuenta](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Estructura de un recorrido de cuentas

Haga clic en el nombre (mostrado como un vínculo) en la lista _[!UICONTROL recorridos de la cuenta]_ para revisar los detalles, realizar cambios y realizar acciones.

![Espacio de trabajo de recorrido de cuenta](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

The header of each account journey map includes:

* Nombre del recorrido
* Acceso para editar el nombre del recorrido (![Editar icono](../assets/do-not-localize/icon-edit.svg) _Editar_ icono)
* Estado del recorrido

El estado de un recorrido puede cambiar según las acciones que aplique. En función del estado de un recorrido, ciertas acciones no están disponibles en el lado derecho del encabezado.

| Estado | Descripción | Acciones disponibles |
| ------ | ----------- | ----------------- |
| _**Borrador**_ | Un recorrido sin publicar que se puede editar. | <ul><li>[Publicar](./create-publish-journey.md#publish-an-account-journey)</li><li>Duplicado </li><li>Eliminar </li></ul> |
| _**Activo**_ | El estado del recorrido cambia de Borrador a Activo cuando se publica un recorrido. En este estado, ya no se puede editar. | <ul><li>Duplicado </li><li>Cerrar nuevas entradas </li><li>Anular </li></ul> |
| _**Cerrado a nuevas entradas**_ | El estado del recorrido cambia de _Activo_ a _Cerrado a nuevas entradas_ al hacer clic en [!UICONTROL Cerrar a nuevas entradas] en la barra de navegación superior. | <ul><li>Duplicado </li><li>Anular </li></ul> |
| _**Anulado**_ | El estado del recorrido cambia de _Activo_ o _Cerrado a nuevas entradas_ cuando se anula un recorrido. No se puede reiniciar un recorrido anulado. | <ul><li>Duplicado </li><li>Eliminar </li></ul> |
| _**Finalizado**_ | Cuando todas las cuentas de un recorrido completan el recorrido, el estado cambia de Activo o Cerrado a nuevas entradas a Finalizado. | <ul><li>Duplicado </li><li>Eliminar </li></ul> |

## Manage journeys

La lista _Recorridos de cuenta_ incluye todos los recorridos de su instancia de Journey Optimizer B2B edition.

### Abort journey

If you abort (stop) a live or scheduled journey, accounts in the journey immediately stop their progress, and no further journey entrance can happen. No se puede reiniciar un recorrido anulado.

>[!IMPORTANT]
>
>When the account journey is used in another journey from a _Take an action_ node with the _Add Account to (other) Journey_ action, aborting the journey blocks that action from that journey.

1. Click the journey name to open it.

1. Click the **[!UICONTROL More...]** menu at the top right and choose **[!UICONTROL Abort]**.

   ![Haga clic en Más en la parte superior derecha](./assets/account-journey-live-more-menu.png){width="450"}

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Anular]**.

### Cerrar nuevas entradas

Si cierra un recorrido activo, las cuentas que están actualmente en el recorrido continúan su ruta en ese recorrido y no puede ocurrir ninguna otra entrada al recorrido. No se puede reiniciar un recorrido cerrado. Puede duplicar un recorrido cerrado.

>[!IMPORTANT]
>
>Cuando el recorrido de cuenta se usa en otro recorrido desde un nodo _Realizar una acción_ con la acción _Agregar cuenta a (otro) Recorrido_, cerrarla a nuevas entradas bloquea esa acción desde ese recorrido.

1. Haga clic en el nombre del recorrido para abrirlo.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y elija **[!UICONTROL Cerca de las nuevas entradas]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Cerrar a nuevas entradas]**.

### Duplicar recorrido

Una acción de duplicado es similar a una función de clonado, pero un recorrido duplicado no incluye ningún recurso de contenido de recorrido creado. Puede duplicar los detalles del recorrido de la cuenta o simplemente un _esqueleto_ de la estructura de flujo y ruta.s

1. Click the _More_ icon (**...**) next to the journey name and choose **[!UICONTROL Duplicate]**.

   ![Click the ... icon and choose Duplicate](./assets/account-journeys-list-more-menu.png){width="450"}

   Según el estado del recorrido de la cuenta, también puede acceder a la acción duplicar desde los detalles del recorrido o el mapa del recorrido:

   * Para un recorrido de borrador, haz clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y elige **[!UICONTROL Duplicar]**.

   * Para todos los demás estados de recorrido, haz clic en **[!UICONTROL Duplicar]** en la parte superior derecha.

     ![Click Duplicate at the top right](./assets/account-journey-duplicate-button.png){width="450"}

1. In the _Duplicate Journey_ dialog, set the **[!UICONTROL Name]** and **[!UICONTROL Description]** for the new journey.

   By default, the dialog uses the name of the duplicated journey appended with __copy_. Enter another unique name for the journey as needed.

   ![Duplicate Journey dialog](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Choose the duplication **[!UICONTROL Type]**:

   * **[!UICONTROL Duplicación parcial del contenido]**: use este tipo para copiar todo el contenido del recorrido, sin incluir los mensajes de correo electrónico o SMS creados. Los nodos que hacen referencia a un mensaje de correo electrónico o SMS de Marketo Engage están totalmente intactos.

   * **[!UICONTROL Duplicado sin detalles]**: use este tipo para copiar solo la estructura y las rutas del nodo. Todos los ajustes de nodo y las condiciones de ruta no están definidos (predeterminado), por lo que puede reutilizar el flujo básico con diferentes ajustes de segmentación de audiencia, acciones y rutas. Todos los nodos _Wait_ utilizan el valor predeterminado de cinco días.

1. Haga clic en **[!UICONTROL Duplicar]**.

   El recorrido de cuenta duplicado se abre en el mapa de recorrido, donde puede establecer los detalles y crear contenido de recorrido según sea necesario.

### Eliminar recorrido

Use a delete action to delete a journey permanently. You cannot delete a live or scheduled journey.

1. Click the _More_ icon (**...**) next to the journey name and choose **[!UICONTROL Delete]**.

   Depending on the status of the account journey, you can also access the delete action from the journey details or journey map:

   * For a draft journey, click the **[!UICONTROL More...]** menu at the top right and choose **[!UICONTROL Delete]**.

   * For other journey statuses, such as _Finished_ or _Aborted_, click **[!UICONTROL Delete]** at the top right.

1. In the confirmation dialog, click **[!UICONTROL Delete]**.

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
