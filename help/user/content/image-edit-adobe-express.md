---
title: Editar imágenes con Adobe Express
description: Obtenga información sobre el uso del Adobe Express para editar imágenes en Journey Optimizer B2B edition Workspace.
feature: Assets, Content
exl-id: 16909f8f-77db-40f8-acd6-e18ac50c0af9
source-git-commit: cb8196a8bb33c326476ddc9d99103d5fea6d10bd
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 3%

---

# Edición de imágenes con Adobe Express {#edit-images-adobe-express}

>[!CONTEXTUALHELP]
>id="ajo-b2b_assets_edit_adobe_express"
>title="Edición de imágenes en Adobe Express"
>abstract="Las herramientas de edición de imágenes sencillas e intuitivas, con tecnología de Adobe Express, están disponibles directamente en Adobe Journey Optimizer B2B Edition para aumentar la velocidad de contenido."

Adobe Journey Optimizer B2B edition se integra de forma nativa con Adobe Express y le permite acceder a un conjunto de herramientas de edición de imágenes de Adobe Express. Puede utilizar estas herramientas para modificar las imágenes almacenadas en Journey Optimizer B2B edition Workspace para el repositorio de recursos del Marketo Engage conectado. La integración ofrece las siguientes ventajas clave:

* Se ha aumentado la reutilización del contenido mediante la edición y el guardado de nuevos recursos de imagen en Journey Optimizer B2B edition.

* Se ha reducido el tiempo y el esfuerzo para actualizar los recursos de imagen o crear nuevas versiones de los recursos de imagen existentes.

>[!NOTE]
>
>Los derechos para las funciones de edición de Adobe Express se incluyen en todas las suscripciones a Journey Optimizer B2B edition.

Las funciones de Adobe Express admiten los formatos de archivo de imagen PNG y JPEG.

_Para modificar una imagen:_

1. Vaya a la navegación de la izquierda y haga clic en **[!UICONTROL Administración de contenido]** > **[!UICONTROL Assets]**.

Esta acción abre una página de lista con todos los recursos enumerados. El área de trabajo _[!UICONTROL Journey Optimizer B2B edition]_ está seleccionada de forma predeterminada.

1. Busque la imagen que desea modificar o utilizar como original para crear un nuevo recurso.

   * Para ver los recursos por área de trabajo y carpeta, abra la estructura haciendo clic en el icono _Mostrar carpetas_ en la parte superior izquierda.

   * Para ordenar la tabla por cualquiera de las columnas, haga clic en el título de la columna. La flecha de la fila de título indica la columna de ordenación y el orden actuales.

   * Para buscar un recurso de imagen dentro del espacio de trabajo o la carpeta seleccionados, introduzca una cadena de texto en la barra de búsqueda.

   ![Examinar recursos en el espacio de trabajo de Journey Optimizer B2B edition](./assets/assets-native-workspace-filtered.png){width="800" zoomable="yes"}

1. Haga clic en el nombre del recurso de imagen para abrirlo y ver sus detalles.

   >[!TIP]
   >
   >Se recomienda seleccionar [la ficha _[!UICONTROL Utilizada por]_](./marketo-engage-design-studio.md#view-asset-used-by-references) en los detalles de la imagen y revisar el contenido donde se utiliza actualmente la imagen antes de continuar con las ediciones en el archivo de imagen.

1. En la imagen _[!UICONTROL Detalles]_ de la derecha, haga clic en **[!UICONTROL Editar con Adobe Express]**.

   ![Abrir la imagen en el editor de Adobe Express](./assets/assets-edit-adobe-express.png){width="600" zoomable="yes"}

   Si la imagen está en uso, aparecerá un cuadro de diálogo de alerta para informarle de que cualquier cambio que realice afectará a ese contenido. Haga clic en **[!UICONTROL Continuar]** para continuar con el editor de Adobe Express.

   ![Una alerta proporciona información sobre el uso de imágenes](./assets/assets-edit-adobe-express-usage-alert.png){width="300"}

## Licencia de Adobe Express Enterprise

Si tiene una licencia Enterprise para Adobe Express, puede acceder y utilizar el editor Express. Estas funciones de edición incluyen operaciones para ajustes de imagen, como color, brillo, nitidez, contrastes y recorte. También incluyen _magia de IA_ operaciones, como quitar fondos, insertar y quitar objetos y borrar partes de la imagen.

>[!NOTE]
>
>La licencia de Adobe Express Enterprise debe adquirirse en la misma organización de IMS para acceder a estas funciones completas de editor para Journey Optimizer B2B edition. Como miembro individual de la organización IMS, necesita una licencia asignada en la instancia de Adobe Express. De lo contrario, su acceso al Adobe Express está restringido a [acciones rápidas en el Adobe Express](#quick-actions-in-adobe-express) desde Journey Optimizer B2B edition.

![Abrir la imagen en el editor Enterprise de Adobe Express](./assets/assets-edit-adobe-express-enterprise-editor.png){width="600" zoomable="yes"}

La [Guía del usuario de Adobe Express](https://helpx.adobe.com/es/express/user-guide.html){target="_blank"} proporciona información detallada acerca de las capacidades de edición disponibles.

## Acciones rápidas en el Adobe Express

Si no dispone de una licencia de Adobe Express Enterprise, puede acceder al editor de acciones rápidas de Adobe Express.

1. En el editor de acciones rápidas de Adobe Express, seleccione cualquiera de las funciones de modificación de imagen para modificar la imagen.

   * [**[!UICONTROL Cambiar tamaño de imagen]**](#resize-image)
   * [**[!UICONTROL Quitar fondo]**](#remove-background)
   * [**[!UICONTROL Recortar imagen]**](#crop-image)
   * [**[!UICONTROL Convertir a PNG]**](#convert-file-format) (cuando se carga una imagen de JPEG)
   * [**[!UICONTROL Convertir en JPEG]**](#convert-file-format) (cuando se carga una imagen PNG)

   ![Seleccione un tipo de edición para modificar la imagen](./assets/assets-edit-adobe-express-left-menu.png){width="600" zoomable="yes"}

1. Cuando vuelva al editor de acciones rápidas del Adobe Express principal, haga clic en **[!UICONTROL Guardar]** para guardar el archivo de imagen modificado en el área de trabajo de recursos de Journey Optimizer B2B edition con el mismo nombre de archivo.

## Redimensionar imagen

1. Utilice la configuración de cambio de tamaño para reducir o expandir la imagen:

   * Seleccione una opción **[!UICONTROL Proporción de aspecto]**. Use un tamaño estándar para el contenido digital o elija **[!UICONTROL Personalizado]** si desea introducir valores para **[!UICONTROL Anchura]** y **[!UICONTROL Altura]** para satisfacer sus necesidades.

   * Los _[!UICONTROL tamaños originales]_ y _[!UICONTROL tamaños comprimidos]_ mostrados muestran los cambios de tamaño que se producen si aplica los cambios. La herramienta **[!UICONTROL Zoom y recorte]** permite inspeccionar más de cerca partes de la imagen mostrada.

   * Si desea devolver la imagen a su estado original, haga clic en **[!UICONTROL Restablecer]**.

   ![Editar con Adobe Express- cambiar tamaño de imagen](./assets/assets-edit-adobe-express-resize-image.png){width="600" zoomable="yes"}

1. Cuando esté satisfecho con el resultado, haga clic en **[!UICONTROL Aplicar]**.

## Quitar fondo

![Editar con Adobe Express: quitar fondo](./assets/assets-edit-adobe-express-remove-background.png){width="600" zoomable="yes"}

El Adobe Express realiza una eliminación automática del fondo para aislar el objeto principal de la imagen. Si está satisfecho con el resultado, haga clic en **[!UICONTROL Aplicar]**.

## Recortar imagen

1. Arrastre los controladores de las esquinas de la imagen para eliminar las áreas exteriores que no desee incluir en el recurso de imagen.

   ![Editar con Adobe Express- recortar imagen](./assets/assets-edit-adobe-express-crop-image.png){width="600" zoomable="yes"}

1. Cuando esté satisfecho con el resultado, haga clic en **[!UICONTROL Aplicar]**.

## Convertir formato de archivo

* **[!UICONTROL Convertir en JPEG]**: para una imagen PNG, puede convertir la imagen en un archivo de imagen de JPEG y guardarla como un nuevo recurso en el área de trabajo.
* **[!UICONTROL Convertir a PNG]**: para una imagen de JPEG, puede convertir la imagen en un archivo de imagen PNG y guardarla como un nuevo recurso en el área de trabajo.

![Editar con Adobe Express- convertir a PNG](./assets/assets-edit-adobe-express-convert-to-png.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Aplicar]**.
