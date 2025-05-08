---
title: Trabajar con Experience Manager Assets
description: Descubra cómo puede utilizar recursos de imagen de un repositorio de AEM Assets conectado al crear contenido en Adobe Journey Optimizer B2B edition.
feature: Assets, Content
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 2%

---

# Uso de recursos de Experience Manager

Cuando Adobe Experience Manager Assets as a Cloud Service está integrado con Adobe Journey Optimizer B2B edition, puede descubrir fácilmente recursos digitales y acceder a ellos para utilizarlos en su contenido de marketing. A medida que crea su contenido, se puede acceder a los recursos desde el elemento _Experience Manager Assets_ en el panel de navegación izquierdo y durante la creación de contenido de correo electrónico para un recorrido de cuenta.

{{aem-assets-licensing-note}}

Cuando se utilizan estos recursos digitales, los cambios más recientes en Assets as a Cloud Service se propagan automáticamente a las campañas de correo electrónico en directo a través de referencias vinculadas. Si las imágenes se eliminan en Adobe Experience Manager Assets as a Cloud Service, aparecerán con una referencia rota en los correos electrónicos. Cuando se modifican o eliminan recursos que se utilizan actualmente en recorridos de cuenta, se notifica a los autores del recorrido sobre los cambios de imagen y la lista de recorridos que utilizan la imagen. Todos los cambios en los recursos deben realizarse en el repositorio central de Adobe Experience Manager Assets.

Cuando su entorno tiene una o más [conexiones de repositorios de Assets](../admin/configure-aem-repositories.md), los autores de contenido pueden usar AEM Assets como fuente de recursos al crear un correo electrónico, una plantilla de correo electrónico o un fragmento visual.

>[!IMPORTANT]
>
>Un administrador debe añadir usuarios que necesiten acceder a Assets a los perfiles de producto Usuarios consumidores de Assets y Usuarios de Assets. [Más información](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console){target="_blank"}

## Imágenes de AEM Assets de acceso

En el editor de contenido visual, haga clic en el icono _Experience Manager Assets_ ( ![Experience Manager Assets icon](../../assets/do-not-localize/icon-assets-aem.svg) ) en la barra lateral izquierda. Esto cambia el panel Herramientas a una lista de recursos disponibles en el repositorio seleccionado.

![Haga clic en el icono del selector de Assets para acceder a los recursos de imagen](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Actualmente, solo se admiten recursos de imagen de Adobe Experience Manager Assets en Adobe Journey Optimizer B2B edition. Los cambios en los recursos deben realizarse desde el repositorio central de Adobe Experience Manager Assets. [Más información](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets){target="_blank"}

### Cambiar el repositorio mostrado

Si tiene más de un repositorio de AEM conectado, haga clic en la flecha de menú de **[!UICONTROL Repositorio]** para elegir el repositorio que desea mostrar en el panel izquierdo.

![Elija un repositorio de AEM Assets para acceder a los recursos de imagen](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Existen varios métodos para agregar un recurso de imagen al lienzo visual.

### Arrastrar y soltar una imagen

1. Examine las miniaturas de imagen que se muestran en el panel izquierdo.

1. Arrastre la miniatura de la imagen y suéltela en el lienzo donde desee añadir el nuevo componente de imagen.

   ![Arrastrar y soltar un recurso de imagen](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

## Buscar y seleccionar una imagen

1. Agregue un componente de imagen al lienzo y haga clic en **[!UICONTROL Experience Manager Assets]** para abrir el cuadro de diálogo _[!UICONTROL Seleccionar Assets]_.

   ![Seleccione un recurso para el componente de imagen](./assets/content-image-component-empty.png){width="600" zoomable="yes"}

1. En el cuadro de diálogo, elija una imagen con las herramientas disponibles para localizar el recurso que necesita:

   * Cambie **[!UICONTROL Repositorio]** en la parte superior derecha.

   * Haga clic en **[!UICONTROL Administrar recursos]** en la parte superior derecha para abrir el repositorio de Assets en otra pestaña del explorador y usar las herramientas de administración de AEM Assets.

   * Haga clic en el selector _Tipo de vista_ en la parte superior derecha para cambiar la pantalla a **[!UICONTROL Vista de lista]**, **[!UICONTROL Vista de cuadrícula]**, **[!UICONTROL Vista de galería]** o **[!UICONTROL Vista de cascada]**.

   * Haga clic en el icono _Orden_ para cambiar el orden de clasificación entre ascendente y descendente.

     ![Use herramientas en el cuadro de diálogo Seleccionar Assets para buscar y seleccionar un recurso de imagen](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Haga clic en la flecha de menú **[!UICONTROL Ordenar por]** para cambiar los criterios de ordenación a **[!UICONTROL Nombre]**, **[!UICONTROL Tamaño]** o **[!UICONTROL Modificado]**.

   * Haga clic en el icono _Filtrar_ en la parte superior izquierda para filtrar los elementos mostrados según sus criterios.

   * Introduzca texto en el campo Buscar para filtrar los elementos mostrados para buscar una coincidencia del nombre del recurso.

   ![Use los filtros y el campo de búsqueda para localizar el recurso](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Seleccionar]**.
<!-- 

## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.
-->
