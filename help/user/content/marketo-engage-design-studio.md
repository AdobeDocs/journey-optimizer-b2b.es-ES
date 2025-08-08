---
title: Trabajo con Marketo Engage Assets
description: Obtenga información sobre el uso de la integración de administración de recursos de Marketo Engage Design Studio en Journey Optimizer B2B edition.
feature: Assets, Content
role: User
exl-id: 430ae5b7-2691-454c-bbd2-5a0b7a8843fb
source-git-commit: 9abb6443a0761070d9864a4bd2243baa9568cdc9
workflow-type: tm+mt
source-wordcount: '2022'
ht-degree: 1%

---

# Trabajar con recursos de Marketo Engage

Marketo Engage Design Studio es la fuente de recursos predeterminada para Journey Optimizer B2B edition y puede administrar y utilizar fácilmente los recursos disponibles para diseñar contenido compatible con los recorridos de su cuenta.

En Marketo Engage, las organizaciones de marketing utilizan espacios de trabajo para organizar sus recursos de contenido y ayudar a los equipos a acceder al recurso correcto. Los espacios de trabajo bien definidos son especialmente útiles para las grandes empresas que tienen una gran cartera de ofertas de productos o que operan a nivel mundial con diferentes requisitos para la comercialización en diferentes regiones.

## Administración central de activos

De manera predeterminada, hay un área de trabajo de **_[!UICONTROL Journey Optimizer B2B edition]_** que puede usar específicamente para el contenido de recorrido de su cuenta. Los recursos que agrega a este espacio de trabajo no están visibles ni disponibles para su uso en Marketo Engage. Para los recursos que residen en esta área de trabajo, tiene la gama completa de funciones de administración de recursos en Journey Optimizer B2B edition. Estas funciones incluyen:

* [Reemplazar](#replace-assets)
* [Eliminar](#delete-assets)
* [Mover](#create-a-folder)
* [Editar con Adobe Express](./image-edit-adobe-express.md)

Assets que reside en los espacios de trabajo de Marketo Engage está limitado al acceso de solo lectura para su uso en correos electrónicos, plantillas de correo electrónico y fragmentos. Puede añadir nuevos recursos a estos espacios de trabajo y descargar una copia de un recurso.

## Examen y acceso a recursos

Para acceder a los recursos de Adobe Marketo Engage desde Journey Optimizer B2B edition, vaya a la navegación izquierda y haga clic en **[!UICONTROL Administración de contenido]** > **[!UICONTROL Assets]**. Esta acción abre una página de lista con todos los recursos enumerados.

![Examinar recursos de Marketo Engage](assets/assets-list-page.png){width="800" zoomable="yes"}

El espacio de trabajo de Journey Optimizer B2B edition está seleccionado de forma predeterminada. Los demás espacios de trabajo se enumeran a continuación.

* Para ver los recursos por área de trabajo y carpeta, abra la estructura haciendo clic en el icono _Mostrar carpetas_ en la parte superior izquierda.

* Para ordenar la tabla por cualquiera de las columnas, haga clic en el título de la columna. La flecha de la fila de título indica la columna de ordenación y el orden actuales.

* Para buscar un recurso de imagen dentro del espacio de trabajo o la carpeta seleccionados, introduzca una cadena de texto en la barra de búsqueda.

* Para personalizar las columnas que se muestran en la tabla, haga clic en el icono _Personalizar tabla_ ( ![Personalizar tabla](../assets/do-not-localize/icon-column-settings.svg) ) en la parte superior derecha.

  Seleccione las columnas que desee mostrar en el listado y haga clic en **[!UICONTROL Aplicar]**.

## Ver detalles del recurso

Haga clic en el nombre de cualquier recurso para abrir la página de detalles del recurso.

![Acceder a los detalles del recurso](assets/assets-details.png){width="700" zoomable="yes"}

## Ver recursos utilizados por referencias

En la página de detalles del recurso, haga clic en la ficha **[!UICONTROL Utilizado por]** para ver los detalles de dónde se utiliza actualmente el recurso en Journey Optimizer B2B edition, en correos electrónicos, plantillas de correo electrónico y fragmentos.

>[!IMPORTANT]
>
>Cualquier recurso que esté _EN USO_ en cualquiera de los correos electrónicos, plantillas de correo electrónico o fragmentos **no se puede** eliminar.

El panel muestra las referencias por categoría: _Correo electrónico_, _Plantilla de correo electrónico_ o _Fragmento_. Los correos electrónicos de Journey Optimizer B2B edition están incrustados y creados en recorrido, por lo que el recorrido principal del correo electrónico que utiliza el recurso se muestra en las referencias.

Al hacer clic en el vínculo, se le redirige al correo electrónico, la plantilla de correo electrónico o el fragmento correspondiente donde se utiliza el recurso.

![Ver los elementos de contenido que utilizan el recurso](assets/assets-used-by.png){width="700" zoomable="yes"}

## Añadir recursos

Desde la página de lista _Assets_, puede agregar recursos de imagen al espacio de trabajo de Journey Optimizer B2B edition o a un espacio de trabajo de Marketo Engage.

1. Haga clic en **[!UICONTROL Agregar Assets]** en la parte superior derecha.

1. En el cuadro de diálogo _[!UICONTROL Agregar recursos]_, arrastre y suelte uno o más archivos del sistema en el cuadro de archivo.

   ![Agregar recursos a un área de trabajo](./assets/assets-add-dialog.png){width="500"}

   También puede hacer clic en el vínculo _[!UICONTROL Seleccionar un archivo del equipo]_ para usar el sistema de archivos local y buscar y seleccionar archivos.

   Puede cargar recursos desde el sistema local de hasta 10 archivos a la vez. El tamaño máximo de archivo es 100 MB.

   Los nombres de archivo de las imágenes seleccionadas se muestran en el cuadro de diálogo. Los nombres de los archivos de recursos deben ser únicos (en todas las carpetas) y, si ya existe un archivo con el nombre, se muestra un mensaje. Los nombres pueden tener un máximo de 100 caracteres y no pueden contener caracteres especiales (como `;`, `:`, `\` y `|`).

1. Seleccione el espacio de trabajo o la carpeta de destino para almacenar los recursos.

   >[!NOTE]
   >
   >Si selecciona una ubicación en el área de trabajo de _[!UICONTROL Journey Optimizer B2B edition]_, podrá administrar el recurso en la aplicación. Si agrega el recurso a un espacio de trabajo de Marketo Engage, las funciones de administración de recursos solo están disponibles en Marketo Engage Design Studio.

1. Para sobrescribir (reemplazar) archivos al cargar uno o más archivos con un nombre de archivo existente, active la casilla de verificación **[!UICONTROL Sobrescribir archivos existentes]**.

1. Haga clic en **[!UICONTROL Agregar]**.

## Eliminar recursos

Cualquier recurso que esté actualmente en uso en cualquiera de los correos electrónicos, plantillas de correo electrónico o fragmentos no se puede eliminar. Compruebe las referencias de utilizadas antes de iniciar una eliminación de recursos. Además, una acción de eliminación no se puede deshacer, por lo que debe comprobarla antes de iniciar una acción de eliminación.

Utilice cualquiera de los siguientes métodos para eliminar un recurso que resida en el espacio de trabajo _[!UICONTROL Journey Optimizer B2B edition]_:

* Vaya a los detalles del recurso, haga clic en **[!UICONTROL ... Más]** en la parte superior derecha y elige **[!UICONTROL Eliminar]** de las opciones.

  ![Acciones de acceso para el recurso](./assets/assets-details-more-menu.png){width="600" zoomable="yes"}

* En la página de listado de _[!UICONTROL Assets]_, haga clic en el icono _Más_ (**[!UICONTROL ...]**) que está junto al elemento del recurso y elija **[!UICONTROL Eliminar]** de las opciones.

  ![Acciones de acceso para el recurso](./assets/assets-list-file-more-menu.png){width="600" zoomable="yes"}

  >[!NOTE]
  >
  >Solo los recursos que residen en el área de trabajo _[!UICONTROL Journey Optimizer B2B edition]_ tienen funciones de administración de recursos disponibles en el menú _Más_.

Esta acción abre un cuadro de diálogo de confirmación. Puede anular el proceso haciendo clic en **[!UICONTROL Cancelar]** o en **[!UICONTROL Eliminar]** para confirmar la eliminación.

Si el recurso está en uso, la acción abre un cuadro de diálogo informativo que le advierte de que no se puede eliminar. Haga clic en **[!UICONTROL Aceptar]**, lo que anula la eliminación.

## Reemplazar recursos

Utilice cualquiera de los siguientes métodos para reemplazar un recurso que reside en el espacio de trabajo _[!UICONTROL Journey Optimizer B2B edition]_:

* Vaya a los detalles del recurso, haga clic en **[!UICONTROL ... Más]** en la parte superior derecha y elige **[!UICONTROL Reemplazar]** de las opciones.

* En la página de listado de _[!UICONTROL Assets]_, haga clic en el icono _Más_ (**[!UICONTROL ...]**) que está junto al elemento del recurso y elija **[!UICONTROL Reemplazar]** entre las opciones.

En el cuadro de diálogo _[!UICONTROL Reemplazar recurso]_, arrastre y suelte el archivo de reemplazo desde el sistema al cuadro de archivo. También puede hacer clic en el vínculo _[!UICONTROL Seleccionar un archivo del equipo]_ para usar el sistema de archivos local y seleccionar un archivo. (Si selecciona varios archivos en el sistema local, se utilizará el primer archivo seleccionado para el reemplazo.)

![Reemplazar cuadro de diálogo de recursos](./assets/assets-replace-dialog.png){width="500"}

Para continuar, haga clic en **[!UICONTROL Reemplazar]**. Puede anular el proceso haciendo clic en **[!UICONTROL Cancelar]**.

Si el archivo que se va a reemplazar está en uso, un cuadro de diálogo informativo le avisará de que el nuevo archivo de imagen reemplazará a la imagen en todos los lugares en los que se utilice (correos electrónicos, plantillas de correo electrónico y fragmentos).

## Descarga de recursos

Puede descargar un recurso mediante cualquiera de los siguientes métodos:

* Vaya a los detalles del recurso y haga clic en **[!UICONTROL Descargar]** en la parte superior derecha.

* En la página de listado de _[!UICONTROL Assets]_, haga clic en los _puntos suspensivos_ (**[!UICONTROL ...]**) junto al elemento del recurso y elija **[!UICONTROL Descargar]** de las opciones.

En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Descargar]** para iniciar la descarga del recurso en su sistema local. Puede anular el proceso haciendo clic en **[!UICONTROL Cancelar]**.

## Aplicar acciones masivas a los recursos seleccionados

En la página del listado (_[!UICONTROL Administración de contenido]_ > _[!UICONTROL Assets]_), seleccione varios recursos a la vez seleccionando cada casilla de verificación a la izquierda. Aparece un banner de mensaje en la parte inferior al seleccionar varios recursos.

![Recursos seleccionados](./assets/assets-list-selected.png){width="700" zoomable="yes"}

Puede realizar las siguientes acciones masivas con los recursos seleccionados que residen en el espacio de trabajo de _[!UICONTROL Journey Optimizer B2B edition]_:

+++Mover recursos

1. En el banner de selección, haga clic en **[!UICONTROL Mover]**.

   Esta acción abre el cuadro de diálogo _[!UICONTROL Mover Assets]_, que muestra los nombres de los recursos seleccionados y le permite seleccionar la carpeta _destino_ a la que desea mover estos recursos.

1. Seleccione una carpeta.

   La ruta de acceso junto a _[!UICONTROL los recursos seleccionados se moverán a:]_ refleja el cambio.

1. Haga clic en **[!UICONTROL Mover]**.

+++

+++Eliminar recursos

>[!NOTE]
>
>Puede aplicar una eliminación masiva para un máximo de 20 recursos seleccionados.

1. En el banner de selección, haga clic en **[!UICONTROL Eliminar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

   Si alguno de los recursos seleccionados está en uso, se anula la eliminación de ese recurso y se muestra un mensaje de alerta.

+++

## Crear una carpeta

1. En la página del listado de _[!UICONTROL Assets]_, haga clic en **[!UICONTROL Crear carpeta]** en la parte superior derecha.

1. En el cuadro de diálogo, introduzca el nombre de la carpeta y seleccione la carpeta de destino (principal) para la nueva carpeta.

   Los nombres de carpeta deben ser únicos, con un máximo de 100 caracteres, y no pueden contener caracteres especiales, como `;`, `:`, `\`, `|`.

   ![Cuadro de diálogo Crear carpeta](./assets/assets-create-folder-dialog.png){width="500"}

1. Haga clic en **[!UICONTROL Agregar]**.

## Aplicar acciones de nivel de carpeta

En el área de trabajo de _[!UICONTROL Journey Optimizer B2B edition]_, puede aplicar acciones a una carpeta o recursos dentro de la carpeta. Haga clic en el icono _Más_ (**...**) que se encuentra junto a la carpeta para mostrar las acciones que puede aplicarle.

![Aplicar acciones a una carpeta o recursos de la carpeta](./assets/assets-folder-menu-options.png){width="700" zoomable="yes"}

Puede realizar las siguientes acciones en el nivel de carpeta:

+++Añadir recursos

1. Elija **[!UICONTROL Agregar recursos]** para cargar archivos de imagen en la carpeta.

1. En el cuadro de diálogo _[!UICONTROL Agregar recursos]_, arrastre y suelte los archivos del sistema. También puede hacer clic en el vínculo para utilizar el sistema de archivos y seleccionar los archivos.

   Puede agregar recursos desde el sistema local de hasta 10 archivos a la vez. Tiene la opción de sobrescribir archivos al cargar uno o más archivos con un nombre de archivo existente.

   Los nombres de archivo de las imágenes seleccionadas se muestran en el cuadro de diálogo. Los nombres de los archivos de recursos deben ser únicos (en todas las carpetas) y, si ya existe un archivo con el nombre, se muestra un mensaje de error. Los nombres pueden tener un máximo de 100 caracteres y no pueden contener caracteres especiales (como `;`, `:`, `\` y `|`).

1. Haga clic en **[!UICONTROL Agregar]**.

+++

+++Crear una subcarpeta

1. Elija **[!UICONTROL Crear carpeta]**.

1. En el cuadro de diálogo, introduzca el nombre de la carpeta.

   Los nombres de carpeta deben ser únicos, con un máximo de 100 caracteres, y no pueden contener caracteres especiales, como `;`, `:`, `\`, `|`.

1. Haga clic en **[!UICONTROL Agregar]**.

+++

+++Cambie el nombre de la carpeta

1. Elija **[!UICONTROL Cambiar nombre]**.

1. En el cuadro de diálogo, introduzca el nuevo nombre de carpeta.

   Los nombres de carpeta deben ser únicos, con un máximo de 100 caracteres, y no pueden contener caracteres especiales, como `;`, `:`, `\`, `|`.

1. Haga clic en **[!UICONTROL Guardar]**.

+++

+++Mover la carpeta

1. Para mover la carpeta a otra carpeta principal, elige **[!UICONTROL Mover]**.

1. En el cuadro de diálogo, seleccione la carpeta de destino como el nuevo elemento principal de la subcarpeta.

1. Haga clic en **[!UICONTROL Mover]**.

   Si intenta mover una carpeta a una de sus subcarpetas (dentro de la estructura de la carpeta seleccionada), se muestra un mensaje de error y se cancela el movimiento.

+++

+++Elimine la carpeta

1. Elija **[!UICONTROL Eliminar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

Si alguno de los recursos de la carpeta está actualmente en uso, la acción abre un cuadro de diálogo de alerta para informarle de que no se puede eliminar. Haga clic en **[!UICONTROL Aceptar]**, lo que anula la eliminación.

+++

+++Convertir en una carpeta de archivo

Al archivar una carpeta, no se puede buscar en los archivos que contiene. Utilice la función de archivado para los archivos de recursos que no desee que utilicen los integrantes del equipo en adelante, como un distintivo promocional de evento obsoleto o contenido de temporada. Posteriormente, puede desarchivar una carpeta si desea que el contenido vuelva a estar disponible.

* Elija **[!UICONTROL Convertir en carpeta de archivo]**. Se muestra un banner de confirmación para confirmar que el estado de la carpeta cambia a archivado.

* Elija **[!UICONTROL Desarchivar carpeta]**. Se muestra un banner de confirmación para confirmar que el estado de la carpeta cambia a sin archivar.

+++

## Uso de recursos en el contenido

Assets se puede utilizar en el correo electrónico de su equipo, en la creación de plantillas de correo electrónico o en la creación de fragmentos visuales desde el editor de contenido visual.

En la interfaz de usuario del diseñador visual, seleccione el icono _Marketo Engage Assets_ ( ![Marketo Engage Assets icon](../../assets/do-not-localize/icon-assets-me.svg) ) en la barra lateral izquierda.

Esta acción cambia el panel Herramientas, que muestra una lista estructurada de los recursos disponibles en el espacio de trabajo seleccionado. Seleccione el espacio de trabajo que desea mostrar para elegir un recurso.

![Recursos seleccionados](./assets/asset-design-workspace-select.png){width="700" zoomable="yes"}

Existen varios métodos para agregar un recurso de imagen al lienzo visual:

* Arrastre y suelte una miniatura de imagen desde el panel de navegación izquierdo.

* Agregue un componente de imagen al lienzo y haga clic en **[!UICONTROL Marketo Engage Assets]** para abrir el cuadro de diálogo _[!UICONTROL Seleccionar recurso de Adobe Marketo Engage]_.

  ![Use los filtros y el campo de búsqueda para encontrar el recurso que necesita](./assets/assets-select-dialog-marketo.png){width="700" zoomable="yes"}

  En el cuadro de diálogo, puede elegir una imagen del repositorio seleccionado. Haga clic en **[!UICONTROL Seleccionar]** para agregar el recurso.

  Hay herramientas disponibles para ayudarle a localizar el recurso que necesita:

   * Haga clic en el icono _Filtrar_ en la parte superior izquierda para filtrar los elementos mostrados según sus criterios.

   * Escriba texto en el campo _Buscar_ para filtrar los elementos mostrados y buscar una coincidencia del nombre del recurso.

  ![Use los filtros y el campo de búsqueda para encontrar el recurso que necesita](./assets/assets-select-dialog-marketo-filtered.png){width="700" zoomable="yes"}
