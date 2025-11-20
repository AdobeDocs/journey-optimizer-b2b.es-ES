---
title: Seleccionar eventos y campos de experiencia
description: Seleccione eventos y campos de Experience Platform para almacenar en déclencheur la toma de decisiones en tiempo real en recorrido en función del comportamiento del cliente.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Esta función se encuentra actualmente en versión beta"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Seleccionar eventos de experiencia y campos

Los administradores pueden seleccionar [Eventos de experiencia de AEP](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} específicos y sus campos asociados dentro del esquema de unión de eventos de experiencia. Después de la selección, los usuarios pueden configurar reglas de toma de decisiones para escuchar esos eventos de experiencia y habilitar acciones de campaña dinámicas y segmentadas basadas en datos de eventos casi en tiempo real.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
El uso de eventos de experiencia de AEP en recorrido es un proceso de dos pasos:

1. Un administrador [agrega eventos y campos de experiencia de AEP](#add-an-event) en las configuraciones de Journey Optimizer B2B edition.

2. En un recorrido, un experto en marketing agrega un nodo _Escuchar un evento_ y [selecciona un Evento de experiencia](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Selecciona el evento que se va a utilizar en el nodo.
   * Selecciona los campos que se van a utilizar como restricciones.

>[!BEGINSHADEBOX]

## Directrices y limitaciones

A medida que seleccione eventos para cumplir con sus objetivos organizativos, tenga en cuenta lo siguiente:

* Puede seleccionar hasta 50 eventos y hasta 100 campos por evento.

* Los recorridos pueden escuchar los eventos de experiencia que se incorporan mediante las funciones de flujo continuo de Experience Platform, como Web SDK o la API HTTP.

* Puede utilizar eventos de experiencia para la toma de decisiones dentro de un recorrido, pero no se conservan. Por lo tanto, no puede aprovechar un registro histórico de eventos de experiencia en Journey Optimizer B2B edition.

* Cuando se utiliza un evento de experiencia y se publica el recorrido, se pueden añadir más campos, pero no se pueden eliminar los seleccionados anteriormente.

* Puede hacer referencia a un evento de experiencia en varios recorridos o utilizar uno más de una vez dentro del mismo recorrido.

>[!ENDSHADEBOX]

## Administrar eventos de experiencia

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en **[!UICONTROL Clases XDM]** en el panel intermedio y, a continuación, haga clic en la pestaña **[!UICONTROL Eventos]** para mostrar la lista de los eventos disponibles.

   ![Acceder a los eventos de experiencia seleccionados](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   La tabla está ordenada por la columna _[!UICONTROL Última actualización]_, con los eventos actualizados más recientemente en la parte superior de forma predeterminada.

   Desde esta página, puede [seleccionar](#add-an-event) y [editar](#edit-an-event) eventos para usarlos en recorridos.

   Para acceder a los detalles de un evento seleccionado, haga clic en el nombre del evento.

### Filtrado de la lista de eventos

Escriba texto en el campo _[!UICONTROL Buscar]_ para filtrar los eventos mostrados y buscar una coincidencia en el nombre del evento.

![Filtrar la lista de eventos seleccionados por nombre](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Añadir un evento

Para que un evento de experiencia esté disponible para un nodo _Escuchar un evento_ en un recorrido, seleccione el evento y los campos admitidos.

>[!NOTE]
>
>En la versión beta, no se pueden eliminar eventos de la lista. Asegúrese de que cada evento que agregue esté pensado para su uso por parte de su organización.

1. Haga clic en **[!UICONTROL Seleccionar evento de experiencia]** en la parte superior derecha.

   Se muestra la página de detalles del evento. Desde esta página, puede elegir el tipo de evento y los campos.

   ![Detalles del evento para un nuevo evento](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Elija el tipo de evento.

   * Haga clic en **[!UICONTROL Seleccionar tipo de evento]**.

   * En el cuadro de diálogo, elija el tipo de evento.

     Utilice el campo _[!UICONTROL Buscar]_ para filtrar la lista mostrada por nombre. Use el control deslizante **[!UICONTROL Mostrar solo los campos seleccionados]** para revisar las selecciones actuales.

     ![Seleccionar cuadro de diálogo de tipo de evento](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Haga clic en **[!UICONTROL Seleccionar]**.

1. Elija uno o varios campos para el tipo de evento.

   * Haga clic en **[!UICONTROL Seleccionar campos]**.

   * En el cuadro de diálogo, seleccione los campos que desee utilizar como restricciones para eventos coincidentes.

     Utilice el campo _[!UICONTROL Buscar]_ para filtrar la lista mostrada por nombre. Use el control deslizante **[!UICONTROL Mostrar solo los campos seleccionados]** para revisar las selecciones actuales.

     ![Cuadro de diálogo Seleccionar campos](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Haga clic en **[!UICONTROL Seleccionar]**.

1. En la página de detalles del evento, haga clic en **[!UICONTROL Guardar]**.

El evento guardado se muestra en la lista de la ficha _[!UICONTROL Eventos]_.

### Edición de un evento

Edite los detalles del evento para cambiar los campos.

1. Haga clic en el nombre del evento o haga clic en el icono _Más menú_ ( **...** ) y elija **[!UICONTROL Editar]**.

   ![Haga clic en el icono del menú Más](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar campos]** para agregar más campos o eliminar las selecciones existentes en el cuadro de diálogo _[!UICONTROL Seleccionar campos]_.

1. Haga clic en **[!UICONTROL Seleccionar]** para guardar las selecciones.

### Eliminar un evento

>[!NOTE]
>
>Para la versión de Beta de esta función, no se puede quitar un evento de la lista de eventos seleccionados. Se ha planificado la eliminación de eventos para la versión de GA.

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->