---
title: Recursos
description: Administre recursos de imagen desde Journey Optimizer B2B edition y AEM Assets para correos electrónicos, plantillas y fragmentos.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 9c4f2fd95d60eb98deb256cbbb382da694a1a1cf
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 70%

---

# Recursos

En [!DNL Adobe Journey Optimizer B2B Edition], los recursos suelen ser las imágenes utilizadas al diseñar contenido para admitir recorridos de cuenta. Puede utilizar estas imágenes en sus correos electrónicos, plantillas de correo electrónico y fragmentos desde el selector de recursos o desde una sencilla interfaz de arrastrar y soltar dentro del espacio de diseño visual.

[!DNL Journey Optimizer B2B Edition] ofrece a los diseñadores y a los especialistas en marketing acceso a dos tipos de bibliotecas de recursos: un repositorio de recursos [!DNL Journey Optimizer B2B Edition] interno y [!DNL Adobe Experience Manager Assets as a Cloud Service]. Puede usar solamente el repositorio integrado o ambos tipos de biblioteca al mismo tiempo (según la licencia de [!DNL Experience Manager Assets] que tenga).

## Administración de recursos

Si se le ha proporcionado [!DNL Adobe Experience Manager as a Cloud Services] y está configurado como origen de recursos en [!DNL Journey Optimizer B2B Edition], tendrá acceso a ambos tipos de repositorio cuando su cuenta de usuario tenga los permisos necesarios. Estos repositorios son independientes y no están sincronizados. Puede utilizar imágenes de cualquier origen.

### Activos internos

El repositorio de recursos interno se proporciona de manera predeterminada con cada suscripción de [!DNL Journey Optimizer B2B Edition]. Esto significa que tiene acceso a cualquiera de los recursos de imagen almacenados en el sistema de archivos de recursos de [!DNL Adobe Marketo Engage] conectado. Puede utilizar este repositorio como su biblioteca de recursos local, incluidas las funciones de carga y descarga de recursos. También puede utilizar estos recursos dentro del contenido del recorrido.

Puede [editar estos recursos mediante Adobe Express](./image-edit-adobe-express.md) y moverlos a carpetas para organizarlos y usarlos en sus correos electrónicos, plantillas y fragmentos.

Formatos de archivo compatibles: JPG, JPEG, GIF, PNG, EPS, SVG y RGB

### Adobe Experience Manager Assets as a Cloud Service

Una los flujos de trabajo creativos y de marketing usando [!DNL Adobe Experience Manager Assets]. Está integrado de forma nativa con [!DNL Journey Optimizer B2B Edition], por lo que puede acceder fácilmente a Assets as a Cloud Service para descubrir y utilizar recursos digitales. Proporciona un único repositorio centralizado de recursos que puede utilizar para completar los mensajes.

[!DNL Adobe Journey Optimizer B2B Edition] puede conectarse a [!DNL Adobe Experience Manager Assets as a Cloud Service] para una administración de recursos centralizada que amplíe su sistema creativo y unifique los recursos digitales para la entrega de experiencias. [!DNL Adobe Experience Manager Assets as a Cloud Service] ofrece una solución de nube fácil de usar para una administración de recursos digitales eficiente y operaciones de Dynamic Media. Incorpora sin problemas funciones avanzadas, como inteligencia artificial y aprendizaje automático.

Obtenga más información en la [documentación de Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Acceda a [!DNL Adobe Experience Manager Assets] directamente en [!DNL Journey Optimizer B2B Edition] desde el elemento **[!UICONTROL Experience Manager Assets]** en la navegación izquierda del diseño de contenido. También puede acceder a recursos y carpetas al diseñar el correo electrónico, la plantilla de correo electrónico y el contenido de los fragmentos visuales.

Actualmente, solo puede utilizar imágenes de Adobe Experience Manager Assets en Adobe Journey Optimizer B2B Edition.

## Uso de recursos para la creación de contenido

Utilice recursos a medida que crea sus correos electrónicos, plantillas de correo electrónico y fragmentos visuales. El editor de contenido visual proporciona acceso a las imágenes de los repositorios de recursos conectados. Si también tiene una suscripción para Experience Manager Assets as a Cloud Service, puede elegir recursos de imagen de cualquiera de las fuentes. También puede cargar un recurso de imagen, que lo coloca en el repositorio de recursos interno.

Puede elegir el origen de la imagen al editar la configuración de un componente de imagen o directamente en el lienzo.

* **_Configuración del componente de imagen_**: cuando tenga seleccionado un componente de imagen en el espacio de diseño visual, podrá ver y editar la configuración en el panel derecho. Para añadir o cambiar el archivo de imagen que se muestra en el componente, elija el tipo de origen y seleccione un archivo de imagen.

  ![Edite la configuración del componente de imagen en el panel derecho](./assets/content-assets-image-settings.png){width="350"}

* **_Componente vacío_**: cuando se añade un componente de imagen en el espacio de diseño visual, está vacío y proporciona fácil acceso para elegir un origen y seleccionar un archivo de imagen.

  ![Elija un origen para seleccionar un archivo de imagen para el componente de imagen vacío](./assets/content-assets-image-component-empty.png){width="500"}

* **_Barra de herramientas del componente de imagen_**: cuando tiene un componente de imagen seleccionado en el espacio de diseño visual, la barra de herramientas proporciona un acceso fácil para elegir un origen y seleccionar el archivo de imagen.

  ![Use la barra de herramientas para elegir un origen y seleccionar un archivo de imagen para el componente de imagen](./assets/content-assets-image-toolbar-settings.png){width="500"}

Puede añadir un recurso de imagen a medida que crea el contenido, según el origen del recurso de imagen. También puede elegir un recurso de imagen en la configuración de fondo para un componente de estructura.

>[!BEGINTABS]

>[!TAB Seleccionar recurso]

Haga clic en **[!UICONTROL Seleccionar recurso]** para abrir el selector de recursos, donde podrá elegir una imagen del repositorio de recursos de Journey Optimizer B2B edition.

![Seleccionar un recurso de imagen](./assets/content-assets-internal-image-selected.png){width="700" zoomable="yes"}

Puede utilizar la búsqueda y los filtros para localizar el recurso de imagen deseado. Seleccione el recurso y haga clic en **[!UICONTROL Seleccionar]** para utilizarlo en el componente de imagen.

Para obtener información más detallada sobre cómo usar recursos de imagen internos, consulte [Usar recursos en el contenido](./internal-image-assets.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Haga clic en **[!UICONTROL Experience Manager Assets]** para abrir el selector de recursos, donde podrá elegir una imagen del repositorio de Experience Manager Assets.

![Seleccione un recurso de imagen del repositorio de AEM Assets](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Puede utilizar la búsqueda y los filtros para localizar el recurso de imagen deseado. Seleccione el recurso y haga clic en **[!UICONTROL Seleccionar]** para utilizarlo en el componente de imagen.

Para obtener información más detallada sobre el uso de archivos de imagen de [!DNL Experience Manager Assets], consulte [Acceso a imágenes de AEM Assets](./aem-assets.md#access-aem-assets-images).

>[!TAB Importar medios]

Haga clic en **[!UICONTROL Importar medios]** para seleccionar un archivo de imagen e importarlo como un recurso que se pueda usar para el contenido de Journey Optimizer B2B Edition.

![Seleccione su propio archivo de imagen para importarlo como recurso](./assets/content-assets-image-import-file-selected.png){width="450" zoomable="yes"}

Después de arrastrar y soltar el archivo o seleccionarlo en el sistema de archivos, haga clic en **[!UICONTROL Importar]**. El recurso importado se almacena dentro del repositorio de recursos [!DNL Journey Optimizer B2B Edition].

>[!ENDTABS]
