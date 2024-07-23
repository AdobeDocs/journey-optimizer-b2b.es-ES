---
title: Recorridos de cuenta
description: Obtenga información acerca de los recorridos de cuenta y cómo puede crearlos y administrarlos.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 07198448d168e66023fada332f38099890ba4a1b
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 1%

---


# Recorridos de cuenta

Defina un compromiso basado en las ventas que incluya correo electrónico, SMS y más recorridos de cuenta interna para coordinar el marketing entrante con las actividades de ventas salientes de cada miembro del grupo comprador.

## Acceso y exploración de recorridos de cuenta

1. En la página de inicio de Adobe Experience Platform, haga clic en Adobe Journey Optimizer B2B Edition.

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL recorridos de cuenta]**.

   ![recorridos de cuenta de acceso](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   La página de recorridos mostrada incluye las siguientes columnas:

   * [!UICONTROL Nombre] (haga clic en el nombre para abrir el recorrido de la cuenta y editarlo)
   * [!UICONTROL Estado]
   * [!UICONTROL Descripción]
   * [!UICONTROL Creado por]
   * [!UICONTROL Última actualización el]
   * [!UICONTROL Última actualización por]
   * [!UICONTROL Publicado el]
   * [!UICONTROL Publicado por]

Esta tabla incluye la capacidad de búsqueda por nombre y creado por. Ordenar no está disponible actualmente.

Puede personalizar la tabla mostrada si hace clic en el icono _Columnas_ en la esquina superior derecha y activa o desactiva las casillas de verificación.

![Elija las columnas que desea mostrar en la lista de recorridos de la cuenta](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Estructura de un recorrido de cuentas

Haga clic en el nombre (mostrado como un vínculo) en la lista _[!UICONTROL recorridos de la cuenta]_ para revisar los detalles, realizar cambios y realizar acciones.

![Espacio de trabajo de recorrido de cuenta](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

El encabezado del editor de cada recorrido de cuenta incluye:

* nombre del recorrido
* Capacidad para editar el nombre (icono _Editar_)
* Estado del recorrido

Las siguientes acciones están disponibles en el encabezado:

* **Publish**: puede publicar un recorrido si no hay errores de bloqueador. Cuando se publique, el estado del Recorrido cambiará a _Activo_. Si el recorrido tiene errores, el botón aparece atenuado con información de contenido: `Resolve errors before publishing`.
* **Duplicado**: esta acción es similar a una función de clonación, pero el recorrido duplicado no incluye ningún recurso.
* **Cerca de nuevas entradas**: si cierra un recorrido, las cuentas que se encuentran actualmente en el recorrido continuarán su ruta de acceso en el recorrido y no podrá haber más entradas al recorrido. No se puede reiniciar un recorrido cerrado. Puede duplicar un recorrido cerrado.
* **Anular**: si detiene un recorrido, las cuentas del recorrido detienen inmediatamente su progreso y no puede producirse ninguna otra entrada al recorrido. Un recorrido detenido no se puede reiniciar. Si bloquea nuevas entradas sin detener el progreso de la gente, considere en su lugar cerrar el recorrido.
* **Eliminar**: esta acción elimina permanentemente el recorrido.

El estado de un Recorrido cambia según las acciones que aplique. En función del estado de un recorrido, ciertas acciones no están disponibles en el encabezado.

| Estado | Descripción | Acciones disponibles |
| ------ | ----------- | ----------------- |
| _**Borrador**_ | Un recorrido sin publicar editable. | <ul><li>Publicar</li><li>Duplicado </li><li>Eliminar </li></ul> |
| _**Activo**_ | El estado del recorrido cambia de Borrador a Activo cuando se publica un recorrido. En este estado, ya no se puede editar. | <ul><li>Duplicado </li><li>Cerca de nuevas entradas </li><li>Anular </li></ul> |
| _**Cerrado a nuevas entradas**_ | El estado del recorrido cambia de _Activo_ a _Cerrado a nuevas entradas_ al hacer clic en [!UICONTROL Cerca de nuevas entradas] en la barra de navegación superior. | <ul><li>Duplicado </li><li>Anular </li></ul> |
| _**Anulado**_ | El estado del recorrido cambia de _Activo_ o _Cerrado a nuevas entradas_ cuando se anula un recorrido. No se puede reiniciar un recorrido anulado. | <ul><li>Duplicado </li><li>Eliminar </li></ul> |
| _**Finalizado**_ | Cuando todas las cuentas de un recorrido completan el recorrido, el estado cambia de Activo o Cerrado a nuevas entradas a Finalizado. | <ul><li>Duplicado </li><li>Eliminar </li></ul> |

## Introducción a un recorrido

Para empezar con un recorrido de cuentas, cree el recorrido y, a continuación, construya los nodos y el flujo de recorrido en el editor de recorridos.

### Crear un recorrido de cuenta

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL recorridos de cuenta]**.

1. Haga clic en **[!UICONTROL Crear Recorrido de cuenta]** en la parte superior derecha de la página.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único (obligatorio) y **[!UICONTROL Descripción]** (opcional).

   ![Cuadro de diálogo Crear Recorrido de cuenta](./assets/account-journey-create-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

### Añada la audiencia de la cuenta para su recorrido

El recorrido de una cuenta siempre comienza con la Audiencia de la cuenta, donde puede agregar entradas al recorrido.

1. Haga clic en el nodo **[!UICONTROL Audiencia de la cuenta]** para mostrar las propiedades del nodo a la derecha.

   ![Nodo de audiencia de cuenta](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Agregar audiencia de cuenta]**.

   Puede seleccionar un segmento de audiencia seleccionado anteriormente haciendo clic en _[!UICONTROL Agregar audiencias]_.

1. Para crear un nuevo segmento de audiencia, seleccione **[!UICONTROL Audiencias de cuenta]** en el panel de navegación izquierdo.

1. Haga clic en **[!UICONTROL Crear audiencia]** y siga los pasos descritos en la [guía del servicio de segmentación](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.

### Componentes básicos de un recorrido

El _lienzo de recorrido_ es la zona central del diseñador de recorridos. Es en esta zona donde puede agregar nodos de recorrido y configurarlos. Haga clic en un nodo para abrir su panel de propiedades a la derecha del lienzo y establecerlo según el diseño.

Puede crear su recorrido utilizando cualquiera de estos tipos de nodos:

* [Escuchar un evento](journey-nodes.md#listen-for-an-event)
* [Realizar una acción](journey-nodes.md#take-an-action)
* [Dividir rutas](journey-nodes.md#split-paths)
* [Espera](journey-nodes.md#wait)
* [Combinar rutas](journey-nodes.md#merge-paths)

### Barandillas de protección

Para ayudarle a crear un recorrido sin que se produzcan errores, se han implementado los siguientes carriles de protección:

* _Eliminando un nodo de ruta dividida_: no puede eliminar un nodo sin eliminar todos los nodos subsiguientes de cada ruta.
* _Eliminando un nodo de combinación_: un nodo de combinación solo se puede eliminar cuando hay una ruta conectada a él. Para eliminar un nodo de combinación, deje solo una ruta seleccionada.
* _Cambio entre cuentas y personas_: no puede cambiar la selección de cuentas a personas sin eliminar todos los nodos subsiguientes de cada ruta.

### Añadir un nodo

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en la ruta y seleccione el tipo de nodo.

1. Establezca las propiedades del nodo a la derecha.

### Eliminación de un nodo

1. Vaya al editor de recorrido.

1. En las propiedades del nodo, a la derecha, haga clic en el icono _Eliminar_ (papelera).

1. En el cuadro de diálogo de conformación, haga clic en **[!UICONTROL Eliminar]**.

### Adición y eliminación de una ruta

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en la ruta y agregue el nodo de ruta dividida.

1. En las propiedades del nodo a la derecha, seleccione **[!UICONTROL Cuenta]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]**.

   Con cada ruta creada en el recorrido, aparece una nueva tarjeta de ruta en las propiedades.

1. Vaya a una de las rutas del recorrido y añada nodos de acción o evento a esta ruta mediante el icono más.

1. Seleccione el nodo de ruta dividida para abrir las propiedades a la derecha.

   Tenga en cuenta que las rutas que tienen nodos en ellas no se pueden eliminar.

1. Para eliminar estas rutas, primero debe eliminar todos los nodos de esa ruta.

### Programar un recorrido

Cuando publica un recorrido, puede comenzar inmediatamente o en una fecha futura programada. La fecha de finalización puede ser un máximo de tres años desde la fecha de inicio. Después de publicar un recorrido (estado _Activo_), puede actualizar la fecha de finalización del recorrido, pero no la fecha de inicio.

1. Vaya al editor de recorrido.

1. Programe su recorrido haciendo clic en [!UICONTROL Configuración de Recorrido] en el encabezado.

1. En el cuadro de diálogo, defina las opciones de programación:

   * Elija un tipo de programación.

     Para activar el recorrido en el momento de la publicación, elija **[!UICONTROL Inmediatamente]**.

     Para activar el recorrido en una fecha futura, elige **[!UICONTROL En una fecha específica]** y haz clic en el icono _Calendario_ para seleccionar la fecha.

     ![cuadro de diálogo de configuración de Recorrido](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Especifique la **[!UICONTROL fecha de finalización]** del recorrido. Puede ser un máximo de tres años desde la fecha de inicio (este campo es obligatorio).

1. Haga clic en **[!UICONTROL Guardar]**.

   Cuando estés listo para publicar tu recorrido, puedes revisar esta configuración cuando hagas clic en _[!UICONTROL Publish]_.
