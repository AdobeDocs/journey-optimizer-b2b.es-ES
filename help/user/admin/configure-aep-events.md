---
title: Configuración de eventos de Experience Platform
description: Obtenga información acerca del tipo de nodo Espera que puede utilizar para organizar las recorridos de la cuenta en Journey Optimizer B2B edition.
feature: Setup, Integrations
role: Admin
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 1eaaf92fdec538bec4f3d70cc65dee141971b0c5
workflow-type: tm+mt
source-wordcount: '1779'
ht-degree: 1%

---

# Configuración de definiciones de eventos de Experience Platform

Los administradores pueden configurar definiciones de eventos basadas en Adobe Experience Platform (AEP), que permiten a los especialistas en marketing crear recorridos de cuenta que reaccionen a [Eventos de experiencia de AEP](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"}.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea la descripción general del vídeo](#overview-video)

El uso de eventos de experiencia de AEP en recorridos de cuenta es un proceso de dos pasos:

1. Cree y publique una definición de evento de AEP.

2. En un recorrido de cuenta, agrega un nodo _Escuchar un evento_ y [selecciona una definición de evento de AEP como evento de personas](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

Cada definición de evento requiere las siguientes entradas de Experience Platform:

* **_Esquema_**: esquema XDM que define la estructura de datos del evento de experiencia. Debe basarse en un evento de experiencia y estar habilitado para el perfil.

  >[!NOTE]
  >
  >Para asegurarse de que se han definido los esquemas necesarios, debe coordinarse con el equipo de ingeniería. [La creación de esquemas XDM](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"} es un proceso complejo realizado por ingenieros de datos en función de los requisitos de casos de uso de su organización.

* **_Tipos de eventos_**: eventType de XDM ExperienceEvent (máximo de 20 por definición de evento).

* **_Campos_**: campos XDM que están presentes en el esquema (máximo de 20 por definición de evento)

* **_Nombre_** - Un nombre único para la definición del evento.

* **_Descripción_**: una descripción para la definición del evento.

## Limitaciones y barreras

Cuando cree y administre definiciones de eventos para satisfacer sus objetivos organizativos, tenga en cuenta lo siguiente:

* Journey Optimizer B2B edition admite un máximo de 50 definiciones de eventos.

* Los recorridos de cuenta pueden detectar eventos de experiencia de AEP que se incorporan mediante las funciones de flujo continuo de AEP, como Web SDK o la API HTTP.

* Solo una definición de evento de AEP puede utilizar un esquema combinado y un conjunto de tipos de evento. Cuando crea una definición de evento utilizando un esquema (por ejemplo, `My Schema`) y un tipo de evento (por ejemplo, `Web Webpagedetails Page Views`), ninguna otra definición de evento puede utilizar la combinación de `My Schema` y `Web Webpagedetails Page Views`.

* Una definición de evento se puede utilizar en más de un recorrido de cuentas.

* Los eventos de experiencia de AEP se pueden utilizar con fines de toma de decisiones dentro de un recorrido de cuenta, pero no se conservan. Por lo tanto, no se puede aprovechar ningún registro histórico de eventos de experiencia de AEP en Journey Optimizer B2B edition.

* No se admiten las restricciones de _fecha de la actividad_ y _número mínimo de veces_.

* Una vez publicada una definición de evento, no se pueden modificar el esquema y el nombre. Sin embargo, puede agregar tipos de eventos y campos creando una versión de borrador y publicando de nuevo.

* Las definiciones de eventos utilizadas en los recorridos publicados no se pueden eliminar.

## Acceso y administración de definiciones de eventos

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en **[!UICONTROL Eventos]** en el panel intermedio para mostrar la lista de definiciones de eventos.

   Desde esta página, puedes [crear](#create-an-event-definition), [publicar](#publish-an-event-defintion), [editar](#edit-an-event-definition) y [eliminar](#delete-an-event-definition) definiciones de eventos.

   ![Acceder a las definiciones de eventos configuradas](./assets/configuration-events-defs-list.png){width="800" zoomable="yes"}

   La tabla está ordenada por la columna _[!UICONTROL Modificado]_, con las definiciones actualizadas más recientemente en la parte superior como predeterminadas.<!-- Click the column title to change between ascending and descending.-->

1. Para acceder a los detalles de una definición de evento, haga clic en el nombre.

### Estado y ciclo de vida de definición de evento

En la lista _[!UICONTROL Definiciones de eventos]_, la columna **[!UICONTROL Estado]** indica el estado actual de cada definición. El estado determina su disponibilidad para utilizarlo en recorridos de cuenta y los cambios que puede realizar en él.

| Estado | Descripción |
| -------------------- | ----------- |
| Borrador | Cuando se crea una definición de evento, está en estado de borrador. Permanece en este estado hasta que se publica para su uso en recorridos de cuenta. Acciones disponibles: <br/><li>Editar todos los detalles<li>Publicación<li>Eliminar |
| Publicadas | Al publicar una definición de evento, pasa a estar disponible para su uso en recorridos de cuenta. No se pueden modificar los detalles. Acciones disponibles: <br/><li>Disponible para _escuchar un nodo de recorrido de evento_<li>Crear versión de borrador<li>Eliminar (si no está en uso) |
| Publicado (con borrador) | Cuando se crea un borrador a partir de una definición de evento publicada, la versión publicada permanece disponible para su uso en recorridos de cuenta y la versión de borrador se puede modificar. Si publica la versión de borrador, reemplazará la versión publicada actual y la definición del evento se actualizará para los recorridos de cuenta en los que aún no se haya ejecutado. Acciones disponibles: <br/><li>Editar todos los detalles<li>Publicar versión de borrador<li>Descartar versión de borrador<li>Eliminar (si no está en uso) |

![Ciclo de vida del estado del fragmento](../assets/status-lifecycle-diagram.png){zoomable="yes"}

### Filtrado de la lista de definiciones de eventos

Para buscar una definición de evento por nombre, introduzca una cadena de texto en la barra de búsqueda para buscar una coincidencia.

![Filtrar las definiciones de eventos mostradas](./assets/configuration-events-defs-list-filtered.png){width="700" zoomable="yes"}

## Creación de una definición de evento

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Eventos]** en el panel intermedio para mostrar la lista de definiciones de eventos.

1. Haga clic en **[!UICONTROL Crear evento]** en la parte superior derecha.

1. Escriba **[!UICONTROL Nombre]** (obligatorio) y **[!UICONTROL Descripción]** (opcional).

   ![Crear definición de evento](./assets/configuration-events-create.png){width="600" zoomable="yes"}

1. Establezca el **[!UICONTROL Esquema]** que se usará para la definición del evento.

   El esquema que seleccione determina los campos disponibles para agregar a la definición. Los campos que agregue estarán disponibles como restricciones para un nodo _Escuchar un evento_ en un recorrido de cuentas.

   * Haga clic en **[!UICONTROL Seleccionar esquema]**.
   * En el cuadro de diálogo, seleccione un esquema de la lista de esquemas basados en Experience Event.
   * Haga clic en **[!UICONTROL Seleccionar]**.

   ![Seleccione el esquema para la definición del evento](./assets/configuration-events-create-select-schema.png){width="600" zoomable="yes"}

1. Seleccione los **[!UICONTROL tipos de evento]** que se usarán para la definición del evento.

   Los [tipos de eventos](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent#eventType){target="_blank"} que seleccione determinan los eventos que están disponibles como restricciones para un nodo _Escuchar un evento_ en un recorrido de cuentas.

   * Haga clic en **[!UICONTROL Seleccionar tipos de eventos]**.
   * En el cuadro de diálogo, seleccione uno o varios tipos de eventos de la lista (un máximo de 20).
   * Haga clic en **[!UICONTROL Seleccionar]**.

   ![Seleccione los tipos de eventos para la definición del evento](./assets/configuration-events-create-select-event-types.png){width="600" zoomable="yes"}

1. Seleccione los **[!UICONTROL campos]** que se usarán para la definición del evento.

   Los campos que seleccione determinan las restricciones que están disponibles cuando el evento se usa para un nodo _Escuchar un evento_ en un recorrido de cuentas.

   >[!NOTE]
   >
   >El campo `eventType` es obligatorio y se selecciona automáticamente.

   * Haga clic en **[!UICONTROL Seleccionar campos]**.
   * En el cuadro de diálogo, seleccione uno o varios campos de la lista (un máximo de 20).
   * Haga clic en **[!UICONTROL Seleccionar]**.

   ![Seleccione los campos para la definición del evento](./assets/configuration-events-create-select-fields.png){width="600" zoomable="yes"}

1. Una vez completados el esquema, los tipos de eventos y los campos, haga clic en **[!UICONTROL Crear]**.

   Tras la creación, se mostrará la página de la lista y el nuevo evento se colocará en la parte superior de la lista con el estado _Borrador_.

   ![La nueva definición de evento de borrador aparece en la página](./assets/configuration-events-create-new-draft.png){width="700" zoomable="yes"}

## Publicación de una definición de evento

Cuando esté seguro de que la definición del evento de borrador está completa y es correcta según sus necesidades, puede publicarla. La definición de evento publicada está disponible para su uso en recorridos de cuenta. Una vez publicada la definición del evento, puede crear una versión de borrador si necesita realizar cambios en ella. Sin embargo, no puede cambiar el esquema y solo puede agregar tipos de eventos y campos (no puede eliminarlos).

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Eventos]** en el panel intermedio para mostrar la lista de definiciones de eventos.

1. En la lista _[!UICONTROL Definiciones de eventos]_, haga clic en el nombre de la definición de evento de borrador para abrir la página de detalles.

   ![Abrir la definición de evento de borrador](./assets/configuration-events-publish-draft.png){width="600" zoomable="yes"}

   Si es necesario, revise la configuración antes de publicar. Puede [editar el borrador](#edit-an-event-definition) si no cumple con sus requisitos.

1. Haga clic en **[!UICONTROL Publicar]** en la parte superior derecha.

1. En el diálogo de confirmación, haga clic en **[!UICONTROL Publicar]**.

   ![Cuadro de diálogo de evento de publicación](./assets/configuration-events-publish-dialog.png){width="300"}

   El estado de la definición del evento cambia a _Publicado_ y ahora está [disponible para su uso en recorridos de cuenta](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   ![El estado de la definición del evento se ha actualizado en la página](./assets/configuration-events-create-new-draft.png){width="700" zoomable="yes"}

## Edición de una definición de evento

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Eventos]** en el panel intermedio para mostrar la lista de definiciones de eventos.

   Las ediciones realizadas en una definición de evento dependen de su estado actual:

   * Cuando una definición de evento se encuentra en estado _Borrador_, puede editar cualquiera de sus detalles.
   * Cuando una definición de evento se encuentra en el estado _Publicado_, no puede editarla. Puede crear una versión de borrador editable y, a continuación, reemplazar la versión publicada.
   * Cuando una definición de evento se encuentra en estado _Publicado (con borrador)_, puede cambiar la versión de borrador (editar la descripción y agregar tipos de eventos y campos).

   ![La nueva definición de evento de borrador aparece en la página](./assets/configuration-events-create-new-draft.png){width="700" zoomable="yes"}

1. En la página de lista _[!UICONTROL Definiciones de eventos]_, haga clic en el nombre de la definición de evento para abrirla.

Siga los pasos según el estado:

>[!BEGINTABS]

>[!TAB Borrador]

1. Cambie cualquiera de los detalles de definición del evento según sea necesario.

   ![Detalles de una definición de evento con el estado Borrador](./assets/configuration-events-publish-draft.png){width="600" zoomable="yes"}

   Siga las mismas directrices que se usan para [crear una definición de evento](#create-an-event-definition).

   Los cambios se guardan automáticamente en el borrador.

1. Cuando la definición del evento cumpla sus criterios y desee que esté disponible para las recorridos de la cuenta de usuario, haga clic en **[!UICONTROL Publicar]**.

1. En el diálogo de confirmación, haga clic en **[!UICONTROL Publicar]**.

   El estado de la definición del evento cambia a _Publicado_ y ahora está disponible para su uso en recorridos de cuenta.

>[!TAB Publicado]

1. Para actualizar la definición del evento, haga clic en **[!UICONTROL Crear versión de borrador]** en la parte superior derecha.

   ![Detalles de definición de evento publicado](./assets/configuration-events-published-details.png){width="600" zoomable="yes"}

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Crear borrador]** para abrir la versión de borrador.

   ![Cuadro de diálogo Crear versión de borrador](./assets/configuration-events-published-create-draft-dialog.png){width="300"}

   Esta acción crea la versión de borrador y vuelve a la página de lista, donde la definición del evento está ahora en estado _Publicado (con borrador)_.

1. Haga clic en el nombre de la definición del evento para abrirla.

   Para una definición de evento _Publicado (con borrador)_, la ficha de versión _[!UICONTROL Publicado]_ está seleccionada como predeterminada.

1. Seleccione la ficha Versión **[!UICONTROL Borrador]**.

   ![Seleccione la versión de borrador para editar los detalles](./assets/configuration-events-published-draft-tab.png){width="600" zoomable="yes"}

1. Cambie cualquiera de los detalles editables (**[!UICONTROL Descripción]**, **[!UICONTROL Tipos de eventos]** y **[!UICONTROL Campos]**) según sea necesario.

   Siga las mismas directrices que se usan para [crear una definición de evento](#create-an-event-definition).

   Los cambios se guardan automáticamente en el borrador.

1. Cuando la definición del evento de borrador cumpla sus criterios y desee reemplazar la versión publicada actual para usarla en los recorridos de cuenta, haga clic en **[!UICONTROL Publicar borrador]**.

1. En el diálogo de confirmación, haga clic en **[!UICONTROL Publicar]**.

   ![Cuadro de diálogo Publicar borrador](./assets/configuration-events-publish-draft-dialog.png){width="300"}

   Cuando publica la versión de borrador, reemplaza la versión publicada actual y la definición del evento se actualiza para los recorridos de cuenta en los que ya está en uso, pero que aún no se han ejecutado.

>[!TAB Publicado (con borrador)]

Al abrir una definición de evento _Publicado (con borrador)_, la ficha Versión _[!UICONTROL Publicado]_ está seleccionada como predeterminada.

1. Seleccione la ficha Versión **[!UICONTROL Borrador]**.

   ![Seleccione la versión de borrador para editar los detalles](./assets/configuration-events-published-draft-tab.png){width="600" zoomable="yes"}

1. Cambie cualquiera de los detalles editables (**[!UICONTROL Descripción]**, **[!UICONTROL Tipos de eventos]** y **[!UICONTROL Campos]**) según sea necesario.

   Siga las mismas directrices que se usan para [crear una definición de evento](#create-an-event-definition).

   Los cambios se guardan automáticamente en el borrador.

1. Cuando la definición del evento de borrador cumpla sus criterios y desee reemplazar la versión publicada actual para usarla en los recorridos de cuenta, haga clic en **[!UICONTROL Publicar borrador]**.

1. En el diálogo de confirmación, haga clic en **[!UICONTROL Publicar]**.

   ![Cuadro de diálogo Publicar borrador](./assets/configuration-events-publish-draft-dialog.png){width="300"}

   Cuando publica la versión de borrador, reemplaza la versión publicada actual y la definición del evento se actualiza para los recorridos de cuenta en los que ya está en uso, pero que aún no se han ejecutado.

>[!ENDTABS]

## Eliminación de una definición de evento

Puede eliminar una definición de evento si un recorrido de cuentas publicado no la está utilizando.

>[!CAUTION]
>
>Utilice esta acción con precaución. No se puede deshacer la eliminación de una definición de evento.

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Eventos]** en el panel intermedio para mostrar la lista de definiciones de eventos.

1. Busque la definición del evento en la lista y haga clic en el icono _Eliminar_ ( ![Eliminar icono](../assets/do-not-localize/icon-delete.svg) ) que aparece a la derecha del nombre.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

   ![Confirme que desea eliminar la definición del evento](./assets/configuration-events-delete-confirm-dialog.png){width="300"}

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on)