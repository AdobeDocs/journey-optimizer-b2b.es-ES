---
title: Recorridos de cuenta
description: 'Optimice la generación de demanda con recorridos de cuenta: cree, publique y administre la participación del grupo de compras en correos electrónicos, SMS y eventos de Journey Optimizer B2B Edition.'
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 5ba2531a287143bd1111f764aa9eba8089111bc9
workflow-type: ht
source-wordcount: '1130'
ht-degree: 100%

---


# Recorridos de la cuenta

Con los recorridos de cuenta, puede agilizar la generación de demanda y la calificación del grupo de compras, así como impulsar una demanda más cualificada para sus programas de adquisición, impulso de ventas/ventas cruzadas y retención. Personalice sus recorridos para cada grupo de compras y miembro del grupo de compras mediante la participación automatizada a través de correos electrónicos, SMS, eventos y mucho más. 

Defina un compromiso basado en las ventas que incluya correo electrónico, SMS y más recorridos de cuenta interna para coordinar el marketing entrante con las actividades de ventas salientes de cada miembro del grupo de compras.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

## Introducción a un recorrido

Para empezar a usar los recorridos de cuenta:

1. [Crear un recorrido](./create-publish-journey.md#create-an-account-journey).
1. [Añada los nodos](./create-publish-journey.md#add-a-node) y [defina el flujo del recorrido](./create-publish-journey.md#add-and-delete-a-path) en el mapa del recorrido.
1. [Publicación del recorrido](./create-publish-journey.md#publish-an-account-journey).

## Acceso y exploración de recorridos de cuenta

En el panel de navegación de la izquierda, expanda **[!UICONTROL Administración de cuentas]** y haga clic en **[!UICONTROL Recorridos de cuenta]**.

Escriba el texto en la herramienta _Búsqueda_ situada en la parte superior de la lista para filtrar la lista mostrada por el nombre.

![Filtrar la lista de recorridos de la cuenta](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

La página de la lista _[!UICONTROL Recorridos de cuenta]_ incluye las siguientes columnas:

* [!UICONTROL Nombre] (haga clic en el nombre para abrir el recorrido de la cuenta y editarlo)
* [!UICONTROL Estado]
* [!UICONTROL Descripción]
* [!UICONTROL Creado por]
* [!UICONTROL Última actualización el ]
* [!UICONTROL Última actualización]
* [!UICONTROL Publicado el]
* [!UICONTROL Publicado por]

Puede ordenar la lista por el _[!UICONTROL Estado]_ haciendo clic en el encabezado de columna.

Puede personalizar las columnas que se muestran en la tabla haciendo clic en el icono _Personalizar tabla_ (![Personalizar tabla](../assets/do-not-localize/icon-column-settings.svg)) en la esquina superior derecha. Seleccione o desactive las casillas de verificación en el cuadro de diálogo y haga clic en **[!UICONTROL Aplicar]**.

![Elija las columnas que desea mostrar en la lista de recorridos de la cuenta](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Estructura de un recorrido de cuentas

Haga clic en el nombre (mostrado como un vínculo) en la lista _[!UICONTROL recorridos de la cuenta]_ para revisar los detalles, realizar cambios y realizar acciones.

![Espacio de trabajo de recorrido de cuenta](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

El encabezado de cada mapa de recorrido de cuenta incluye lo siguiente:

* Nombre del recorrido
* Herramienta de edición para el nombre del recorrido (![icono Editar](../assets/do-not-localize/icon-edit.svg) icono _Editar_)
* Estado del recorrido

El estado de un recorrido puede cambiar según las acciones que se apliquen. En función del estado de un recorrido, determinadas acciones no estarán disponibles en el lado derecho del encabezado.

| Estado | Descripción | Acciones disponibles |
| ------ | ----------- | ----------------- |
| _**Borrador**_ | Un recorrido sin publicar que se puede editar. | <li>[Publicar](./create-publish-journey.md#publish-an-account-journey)<li>[Duplicar](#duplicate-journey) <li>[Eliminar](#delete-journey) |
| _**Activo**_ | El estado del recorrido cambia de Borrador a Activo cuando se publica un recorrido. En este estado, ya no se puede editar. | <li>[Duplicar](#duplicate-journey)<li>[Cerrar a nuevas entradas](#close-to-new-entries) <li>[Anular](#abort-journey) |
| _**Cerrado a nuevas entradas**_ | El estado del recorrido cambia de _Activo_ a _Cerrado a nuevas entradas_ al hacer clic en [!UICONTROL Cerrar a nuevas entradas] en la barra de navegación superior. | <li>[Duplicar](#duplicate-journey) <li>[Anular](#abort-journey) |
| _**Anulado**_ | El estado del recorrido cambia de _Activo_ o _Cerrado a nuevas entradas_ cuando se anula un recorrido. No se puede reiniciar un recorrido anulado. | <li>[Duplicar](#duplicate-journey) <li>[Eliminar](#delete-journey) |
| _**Finalizado**_ | Cuando todas las cuentas de un recorrido completan el recorrido, el estado cambia de _Activo_ o _Cerrado a nuevas entradas_ a _Finalizado_. | <li>[Duplicar](#duplicate-journey) <li>[Eliminar](#delete-journey) |

## Administrar recorridos

La lista _Recorridos de cuenta_ incluye todos los recorridos de su instancia de Journey Optimizer B2B Edition.

### Anular recorrido

Si anula (detiene) un recorrido activo o planificado , las cuentas del recorrido detienen inmediatamente su progreso y no puede producirse ninguna otra entrada al recorrido. No se puede reiniciar un recorrido anulado.

>[!IMPORTANT]
>
>Cuando el recorrido de la cuenta se usa en otro recorrido desde un nodo _Iniciar una acción_ con la acción _[!UICONTROL Añadir cuenta a (otro) recorrido]_, al anular el recorrido se bloqueará esa acción en ese recorrido.

1. Haga clic en el nombre del recorrido para abrirlo.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y seleccione **[!UICONTROL Anular]**.

   ![Haga clic en Más en la parte superior derecha](./assets/account-journey-live-more-menu.png){width="450"}

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Anular]**.

### Cerrar nuevas entradas

Si se cierra un recorrido activo, las cuentas que se encuentran actualmente en el recorrido continuarán su ruta en ese recorrido y no puede haber más entradas al recorrido. No se puede reiniciar un recorrido cerrado. Puede duplicar un recorrido cerrado.

>[!IMPORTANT]
>
>Cuando el recorrido de la cuenta se utiliza en otro recorrido desde un nodo _Iniciar una acción_ con la acción _[!UICONTROL Añadir cuenta a (otro) recorrido]_, al cerrarlo a nuevas entradas se bloqueará esa acción de ese recorrido.

1. Haga clic en el nombre del recorrido para abrirlo.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y seleccione **[!UICONTROL Cerrar nuevas entradas]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Cerrar nuevas entradas]**.

### Duplicar recorrido

Una acción de duplicado es similar a una función de clonado, pero el recorrido duplicado no incluye ningún recurso de contenido de recorrido creado. Puede duplicar los detalles del recorrido de cuenta, o simplemente un simple _esqueleto_ de la estructura del flujo y la ruta.

1. Haga clic en el icono Más __ (**...**) junto al nombre del recorrido y seleccione **[!UICONTROL Duplicar]**.

   ![Haga clic en el icono de... y seleccione Duplicar](./assets/account-journeys-list-more-menu.png){width="450"}

   Dependiendo del estado del recorrido de la cuenta, también puede acceder a la acción de duplicado desde los detalles del recorrido o desde el mapa del recorrido:

   * Para un borrador de recorrido, haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y seleccione **[!UICONTROL Duplicar]**.

   * Para todos los demás estados de recorrido, haga clic en **[!UICONTROL Duplicar]** en la parte superior derecha.

     ![Haga clic en Duplicar en la parte superior derecha](./assets/account-journey-duplicate-button.png){width="450"}

1. En el cuadro de diálogo _Duplicar recorrido_, defina el **[!UICONTROL Nombre]** y la **[!UICONTROL Descripción]** del nuevo recorrido.

   De forma predeterminada, el cuadro de diálogo utiliza el nombre del recorrido duplicado con __copy_. Introduzca otro nombre único para el recorrido si es necesario.

   ![Cuadro de diálogo Duplicar recorrido](./assets/account-journey-duplicate-dialog.png){width="400"}.

1. Elija el **[!UICONTROL Tipo]** de duplicación:

   * **[!UICONTROL Duplicación parcial del contenido]**: use este tipo para copiar todo el contenido del recorrido, sin incluir los mensajes de correo electrónico o SMS creados. Los nodos que hacen referencia a un mensaje de correo electrónico o SMS de Marketo Engage están totalmente intactos.

   * **[!UICONTROL Duplicado sin detalles]**: use este tipo para copiar solo la estructura y las rutas del nodo. Todos los ajustes de nodo y las condiciones de la ruta están sin definir (valor predeterminado), de modo que puede reutilizar el flujo básico con diferentes públicos, acciones y configuraciones de segmentación de la ruta. Todos los nodos de _espera_ utilizan el valor predeterminado de cinco días.

1. Haga clic en **[!UICONTROL Duplicar]**.

   El recorrido de la cuenta duplicada se abre en el mapa de recorrido, donde puede establecer los detalles y crear contenido del recorrido según sea necesario.

### Eliminar recorrido

Utilice una acción de eliminación para eliminar un recorrido de forma permanente. No puede eliminar un recorrido activo o programado.

1. Haga clic en el icono _Más_ (**...**) que está junto al nombre del recorrido y seleccione **[!UICONTROL Eliminar]**.

   Según el estado del recorrido de la cuenta, también puede acceder a la acción de eliminación desde los detalles del recorrido o la asignación del recorrido:

   * Para un recorrido de borrador, haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y seleccione **[!UICONTROL Eliminar]**.

   * Para otros estados de recorrido, como _Finalizado_ o _Anulado_, haga clic en **[!UICONTROL Eliminar]** en la parte superior derecha.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Revisar progresión de cuenta

Para un recorrido publicado con el estado _Activo_, _Cerrado a nuevas entradas_, _Anulado_ o _Finalizado_, puede abrir el mapa del recorrido para revisar la progresión de la cuenta en los nodos de recorrido. Cada nodo del mapa muestra el número de cuentas que se van a alcanzar y, para los recorridos activos, el número de cuentas que hay actualmente en ese nodo.

![Información de progresión de cuenta de nodo de Recorrido](./assets/node-account-progression-observability.png){width="400"}

Cuando seleccione el nodo, haga clic en el número para ver una lista de cuentas que hayan introducido el nodo o que se encuentren actualmente en ese paso del recorrido.

![Información de progresión de cuenta de nodo de Recorrido](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Vídeo resumen

>[!VIDEO](https://video.tv.adobe.com/v/3443210/?captions=spa&learn=on)
