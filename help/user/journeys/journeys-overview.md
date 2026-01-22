---
title: administración de recorrido
description: 'Optimice la generación de demanda con recorridos: cree, publique y administre la participación del grupo comprador mediante correo electrónico, SMS y eventos en Journey Optimizer B2B edition.'
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 6511f40329df34db665ed6f971fa20670be0ae32
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 44%

---


# administración de recorrido

En Journey Optimizer B2B edition, los recorridos son planes de marketing automatizados y basados en cuentas de varios pasos que organizan experiencias personalizadas en varios canales en respuesta a la participación, los eventos comerciales o las campañas programadas. Defina un acuerdo basado en las ventas que incluya correo electrónico, SMS y mucho más en para coordinar el marketing entrante con las actividades de ventas salientes de cada miembro del grupo comprador.

Journey Optimizer B2B edition admite dos tipos de recorrido:

* **recorridos de cuenta**: optimice la generación de demanda y la calificación de grupos de compra y genere una demanda más calificada para sus programas de adquisición, ampliación de ventas/ventas cruzadas y retención. Personalice sus recorridos para cada grupo de compras y miembro del grupo de compras mediante la participación automatizada a través de correos electrónicos, SMS, eventos y mucho más. 

  ![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general sobre el recorrido de la cuenta](#overview-video)

* **recorridos de personas**: (Beta) organice marketing basado en posibles clientes mediante audiencias y datos de Experience Platform. Con los recorridos de persona, las operaciones de marketing no dependen de Marketo Engage ni de soluciones alternativas para las cadenas de herramientas de Adobe Campaign/B2C, de modo que puedan trabajar con casos de uso B2B.

  Cuando se utiliza de forma conjunta con los recorridos de la cuenta y los grupos de compra, un recorrido de persona puede proporcionar a los especialistas en marketing el poder de aplicar una orquestación completa al recorrido de compra.

  +++Limitaciones actuales de los recorridos de personas

  Existen limitaciones que podrían bloquear ciertos casos de uso o dificultar la creación de recorridos de persona. Muchos problemas son el resultado de la implementación inicial del programa beta, que se abordarán en el futuro.

   * Los eventos no se pueden combinar con atributos de perfil para reducir las definiciones de audiencia.
   * El contexto del evento que califica a un perfil para un recorrido no se puede utilizar para la personalización ni la orquestación.
   * Actualmente, los recorridos no pueden tener un evento y criterios de entrada de segmentos de perfil.
   * Los oyentes de eventos no pueden escuchar varios eventos.
   * Actualmente, los nodos de espera no tienen un conjunto completo de opciones para los criterios de salida del día de la semana u hora del día.
   * El editor de correo electrónico hace referencia de forma incorrecta a funciones y atributos que solo están disponibles para Recorridos de cuenta
   * La compatibilidad con tokens de recorrido personalizados (_Mis tokens_) aún no está disponible.
   * Los nodos de recorrido Agregar y Quitar de la persona no están disponibles actualmente en ninguno de los tipos de recorrido.
   * El historial de eventos no puede utilizarse para orquestación o personalización.
   * Los objetos relacionados (como cuenta, grupo de compra, oportunidad y objetos personalizados) no se pueden utilizar para orquestación o personalización.
   * Actualmente no se admiten canales web, SMS ni de plataforma de publicidad.

  +++

## Introducción a un recorrido

Para empezar con su primer recorrido:

1. [Crear un recorrido](./create-publish-journey.md#create-a-journey).
1. [Añada los nodos](./create-publish-journey.md#add-a-node) y [defina el flujo del recorrido](./create-publish-journey.md#add-and-delete-a-path) en el mapa del recorrido.
1. [Publicación del recorrido](./create-publish-journey.md#publish-a-journey).

## Acceder y examinar sus recorridos

>[!BEGINTABS]

>[!TAB recorridos de cuenta]

En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de Recorrido]** y haga clic en **[!UICONTROL recorridos de cuenta]**.

Escriba el texto en la herramienta _Búsqueda_ situada en la parte superior de la lista para filtrar la lista mostrada por el nombre.

![Filtrar la lista de recorridos de la cuenta](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!TAB recorridos de personas (Beta)]

[!BADGE Beta]{type=Informative tooltip="Disponible como función beta en la arquitectura simplificada"}

En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de Recorrido]** y haga clic en **[!UICONTROL recorridos de persona]**.

Escriba texto en la herramienta _Buscar_ situada en la parte superior de la lista para filtrar la lista mostrada por nombre.

![Filtrar la lista de recorridos de personas](./assets/person-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!ENDTABS]

### Columnas de lista de recorrido

La página de lista recorridos incluye las siguientes columnas:

* [!UICONTROL Nombre] (haga clic en el nombre para abrir el recorrido de la cuenta y editarlo)
* [!UICONTROL Estado]
* [!UICONTROL Fecha de creación]
* [!UICONTROL Creado por]
* [!UICONTROL Última actualización]
* [!UICONTROL Última actualización]
* [!UICONTROL Publicado el]
* [!UICONTROL Publicado por]
* [!UICONTROL Fecha de inicio]
* [!UICONTROL Fecha de finalización]

Puede ordenar la lista por _[!UICONTROL Estado]_, _[!UICONTROL Fecha de creación]_ o _[!UICONTROL Última actualización]_ al hacer clic en el encabezado de la columna.

Para personalizar (mostrar/ocultar) las columnas que se muestran en la tabla, haga clic en el icono _Personalizar tabla_ ( ![Personalizar tabla](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha. Seleccione o desactive las casillas de verificación en el cuadro de diálogo y haga clic en **[!UICONTROL Aplicar]**.

![Elija las columnas que desea mostrar en la lista de recorridos](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

### Estado del recorrido

El estado de un recorrido puede cambiar según las acciones que se apliquen. En función del estado de un recorrido, determinadas acciones no estarán disponibles en el lado derecho del encabezado.

| Estado | Descripción | Acciones disponibles |
| ------ | ----------- | ----------------- |
| _**Borrador**_ | Un recorrido sin publicar que se puede editar. | <li>[Publicar](./create-publish-journey.md#publish-a-journey)<li>[Duplicar](#duplicate-journey) <li>[Eliminar](#delete-journey) |
| _**Activo**_ | El estado del recorrido cambia de _Draft_ a _Live_ cuando se publica un recorrido. En este estado, ya no se puede editar. | <li>[Duplicar](#duplicate-journey)<li>[Cerrar a nuevas entradas](#close-to-new-entries) <li>[Anular](#abort-journey) |
| _**Cerrado a nuevas entradas**_ | El estado del recorrido cambia de _Activo_ a _Cerrado a nuevas entradas_ al hacer clic en [!UICONTROL Cerrar a nuevas entradas] en la barra de navegación superior. | <li>[Duplicar](#duplicate-journey) <li>[Anular](#abort-journey) |
| _**Anulado**_ | El estado del recorrido cambia de _Activo_ o _Cerrado a nuevas entradas_ cuando se anula un recorrido. No se puede reiniciar un recorrido anulado. | <li>[Duplicar](#duplicate-journey) <li>[Eliminar](#delete-journey) |
| _**Finalizado**_ | Cuando todos los miembros de audiencia de persona o cuenta de un recorrido completan el recorrido, el estado cambia de _Activo_ o _Cerrado a nuevas entradas_ a _Finalizado_. | <li>[Duplicar](#duplicate-journey) <li>[Eliminar](#delete-journey) |

## mapas de recorrido

Haga clic en el nombre (mostrado como vínculo) en la lista recorridos para revisar los detalles, realizar cambios y realizar acciones.

![Espacio de trabajo de recorrido de cuenta](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

El encabezado de cada mapa de recorrido incluye:

* Nombre del recorrido
* Herramienta de edición para el nombre del recorrido (![icono Editar](../assets/do-not-localize/icon-edit.svg) icono _Editar_)
* [Estado](#journey-status) del recorrido

Desde el mapa de recorrido, puede [agregar los nodos](./create-publish-journey.md#add-a-node) y [definir el flujo de recorrido](./create-publish-journey.md#add-and-delete-a-path).

## acciones de recorrido

La página de lista recorridos incluye todos los recorridos de cuenta o persona de la instancia de Journey Optimizer B2B edition. Desde la página de lista, puede aplicar una serie de acciones a un recorrido.

### Anular recorrido

Si anula (detiene) un recorrido en directo o programado, las cuentas o personas en el recorrido detienen inmediatamente su progreso y no se puede producir ninguna otra entrada al recorrido. No se puede reiniciar un recorrido anulado.

>[!IMPORTANT]
>
>Cuando el recorrido se usa en otro recorrido desde un nodo _Take an action_ con la acción _[!UICONTROL Add Account to (other) Recorrido]_, al anular el recorrido se bloquea esa acción en ese recorrido.

1. Haga clic en el nombre del recorrido para abrirlo.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y seleccione **[!UICONTROL Anular]**.

   ![Haga clic en Más en la parte superior derecha](./assets/account-journey-live-more-menu.png){width="450"}

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Anular]**.

### Cerrar nuevas entradas

Si se cierra un recorrido activo, las cuentas que se encuentran actualmente en el recorrido continuarán su ruta en ese recorrido y no puede haber más entradas al recorrido. No se puede reiniciar un recorrido cerrado. Puede duplicar un recorrido cerrado.

>[!IMPORTANT]
>
>Cuando el recorrido se usa en otro recorrido desde un nodo _Take an action_ con la acción _[!UICONTROL Add Account to (other) Recorrido]_, cerrarlo a nuevas entradas bloquea esa acción desde ese recorrido.

1. Haga clic en el nombre del recorrido para abrirlo.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y seleccione **[!UICONTROL Cerrar nuevas entradas]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Cerrar nuevas entradas]**.

### Duplicación de un recorrido

Una acción de duplicado es similar a una función de clonado, pero el recorrido duplicado no incluye ningún recurso de contenido de recorrido creado. Puede duplicar los detalles del recorrido o simplemente un _esqueleto_ de la estructura de flujo y ruta.

>[!NOTE]
>
>Esta acción no está disponible actualmente para recorridos de persona.

1. Haga clic en el icono Más __ (**...**) junto al nombre del recorrido y seleccione **[!UICONTROL Duplicar]**.

   ![Haga clic en el icono de... y seleccione Duplicar](./assets/account-journeys-list-more-menu.png){width="450"}

   Según el estado del recorrido, también puede acceder a la acción de duplicado desde los detalles del recorrido o el mapa del recorrido:

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

   El recorrido duplicado se abre en el mapa de recorrido, donde puede establecer los detalles y crear contenido de recorrido según sea necesario.

### Eliminación de un recorrido

Utilice una acción de eliminación para eliminar un recorrido de forma permanente. No puede eliminar un recorrido activo o programado.

1. Haga clic en el icono _Más_ (**...**) que está junto al nombre del recorrido y seleccione **[!UICONTROL Eliminar]**.

   Según el estado del recorrido, también puede acceder a la acción de eliminación desde los detalles del recorrido o el mapa del recorrido:

   * Para un recorrido de borrador, haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y seleccione **[!UICONTROL Eliminar]**.

   * Para otros estados de recorrido, como _Finalizado_ o _Anulado_, haga clic en **[!UICONTROL Eliminar]** en la parte superior derecha.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Revisar progresión de cuenta

Para un recorrido de cuenta publicado que se encuentra en estado _Activo_, _Cerrado a nuevas entradas_, _Anulado_ o _Finalizado_, puede abrir el mapa de recorrido para revisar la progresión de la cuenta para los nodos de recorrido. Cada nodo del mapa muestra el número de cuentas que se van a alcanzar y, para los recorridos activos, el número de cuentas que hay actualmente en ese nodo.

![Información de progresión de cuenta de nodo de Recorrido](./assets/node-account-progression-observability.png){width="400"}

Cuando seleccione el nodo, haga clic en el número para ver una lista de cuentas que hayan introducido el nodo o que se encuentren actualmente en ese paso del recorrido.

![Información de progresión de cuenta de nodo de Recorrido](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Vídeo de información general sobre el recorrido de cuentas {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
