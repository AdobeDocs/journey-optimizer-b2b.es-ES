---
title: Recorridos de cuenta
description: Obtenga información acerca de los recorridos de cuenta y cómo puede crearlos y administrarlos.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---


# Recorridos de cuenta

Cree y ejecute recorridos personalizados para cada grupo comprador y miembro del grupo comprador mediante la participación automatizada en correos electrónicos, SMS, eventos y mucho más. Con los recorridos de cuenta, puede optimizar la generación de demanda y la calificación del grupo de compra, así como impulsar una demanda más cualificada para sus programas de adquisición, ampliación de ventas/ventas cruzadas y retención.

Defina un compromiso basado en las ventas que incluya correo electrónico, SMS y más recorridos de cuenta interna para coordinar el marketing entrante con las actividades de ventas salientes de cada miembro del grupo comprador.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

## Acceso y exploración de recorridos de cuenta

1. En la página de inicio de Adobe Experience Platform, haga clic en Adobe Journey Optimizer B2B edition.

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

* **Publicar**: puede publicar un recorrido si no hay errores de bloqueador. Cuando se publique, el estado del recorrido cambiará a _Activo_. Si el recorrido tiene errores, el botón aparece atenuado con información de contenido: `Resolve errors before publishing`.
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

Para empezar a usar las recorridos de cuenta:

1. [Crear un recorrido](./create-publish-journey.md#create-an-account-journey).
1. [Agregue los nodos](./create-publish-journey.md#add-a-node) y [defina el flujo de recorrido](./create-publish-journey.md#add-and-delete-a-path) en el mapa de recorrido.
1. [Publicar el recorrido](./create-publish-journey.md#publish-an-account-journey).

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
