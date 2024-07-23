---
title: Trabajo con Experience Manager Assets
description: Descubra cómo puede utilizar recursos de imagen de un repositorio de AEM Assets conectado al crear contenido en Adobe Journey Optimizer B2B Edition.
feature: Assets, Content
source-git-commit: 0bdf0da4db0cbfc781d16f1c50716b1fc8ea4db9
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Uso de recursos de Experience Manager

Cuando Adobe Experience Manager Assets as a Cloud Service está integrado con Adobe Journey Optimizer B2B Edition, puede descubrir fácilmente recursos digitales y acceder a ellos para utilizarlos en su contenido de marketing. A medida que crea su contenido, se puede acceder a los recursos desde el elemento _[!UICONTROL Assets]_ en el panel de navegación izquierdo y durante la creación de contenido de correo electrónico para un recorrido de cuenta. También puede cargar recursos en el repositorio as a Cloud Service de AEM Assets conectado directamente desde Adobe Journey Optimizer B2B Edition.

>[!NOTE]
>
>Actualmente, solo se admiten recursos de imagen de Adobe Experience Manager Assets en Adobe Journey Optimizer B2B Edition. Los cambios en los recursos deben realizarse desde el repositorio central de Adobe Experience Manager Assets. [Más información](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets)

Al utilizar estos recursos digitales, los cambios más recientes en Assets as a Cloud Service se propagan automáticamente a las campañas de correo electrónico en directo a través de referencias vinculadas. Si las imágenes se eliminan en Adobe Experience Manager Assets as a Cloud Service, estas aparecerán con una referencia rota en los correos electrónicos. Cuando se modifican o eliminan recursos que se utilizan actualmente en recorridos de cuenta, se notifica a los autores del recorrido sobre los cambios de imagen y la lista de recorridos que utilizan la imagen. Todos los cambios en los recursos deben realizarse en el repositorio central de Adobe Experience Manager Assets.

## Usar AEM Assets como origen de imagen

Si su entorno tiene una o más [conexiones de repositorios de Assets](../admin/configure-aem-repositories.md), puede designar AEM Assets como el origen de los recursos al crear o ver los detalles de un correo electrónico, una plantilla de correo electrónico o un fragmento visual.

* Cuando cree contenido nuevo, elija `AEM Assets` como el elemento **[!UICONTROL Image Source]** del cuadro de diálogo.

  ![Seleccione AEM Assets como origen de imagen en el cuadro de diálogo de creación](./assets/create-dialog-aem-assets.png){width="500"}

* Cuando abra un recurso de contenido existente, elija `AEM Assets` en el panel _[!UICONTROL Cuerpo]_ de la derecha.

  ![Seleccione AEM Assets como origen de imagen en las propiedades](./assets/content-source-aem-assets.png){width="700" zoomable="yes"}

## Acceso a recursos para la creación

>[!IMPORTANT]
>
>Un administrador debe añadir usuarios que necesiten acceder a Assets a los perfiles de producto Usuarios consumidores de Assets y Usuarios de Assets. [Más información](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console)

En el editor de contenido visual, haga clic en el icono _Selector de recursos_ en la barra lateral izquierda. Esto cambia el panel Herramientas a una lista de recursos disponibles en el repositorio seleccionado.

![Haga clic en el icono del selector de Assets para acceder a los recursos de imagen](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

AEM Si tiene más de un repositorio conectado, haga clic en la flecha de menú de **[!UICONTROL Repositorio]** para elegir el repositorio que desea utilizar.

![Elija un repositorio de AEM Assets para acceder a los recursos de imagen](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Existen varios métodos para agregar un recurso de imagen al lienzo visual:

* Arrastre y suelte una miniatura de imagen desde el panel de navegación izquierdo.

  ![Elija un repositorio de AEM Assets para acceder a los recursos de imagen](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

* Agregue un componente de imagen al lienzo y haga clic en **[!UICONTROL Examinar]** para abrir el cuadro de diálogo _[!UICONTROL Seleccionar Assets]_.

  En el cuadro de diálogo, puede elegir una imagen del repositorio seleccionado.

  Hay varias herramientas disponibles para ayudarle a localizar el recurso que necesita.

  ![use la herramienta en el cuadro de diálogo Seleccionar Assets para buscar y seleccionar un recurso de imagen](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Cambie **[!UICONTROL Repositorio]** en la parte superior derecha.

   * Haga clic en **[!UICONTROL Administrar recursos]** en la parte superior derecha para abrir el repositorio de Assets en otra pestaña del explorador y usar las herramientas de administración de AEM Assets.

   * Haga clic en el selector _Tipo de vista_ en la parte superior derecha para cambiar la pantalla a **[!UICONTROL Vista de lista]**, **[!UICONTROL Vista de cuadrícula]**, **[!UICONTROL Vista de galería]** o **[!UICONTROL Vista de cascada]**.

   * Haga clic en el icono _Orden_ para cambiar el orden de clasificación entre ascendente y descendente.

   * Haga clic en la flecha de menú **[!UICONTROL Ordenar por]** para cambiar los criterios de ordenación a **[!UICONTROL Nombre]**, **[!UICONTROL Tamaño]** o **[!UICONTROL Modificado]**.

   * Haga clic en el icono _Filtrar_ en la parte superior izquierda para filtrar los elementos mostrados según sus criterios.

   * Introduzca texto en el campo Buscar para filtrar los elementos mostrados para buscar una coincidencia del nombre del recurso.

  ![Use los filtros y el campo de búsqueda para localizar el recurso](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

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