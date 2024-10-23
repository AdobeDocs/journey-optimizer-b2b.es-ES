---
title: Recursos
description: Obtenga información acerca de la administración de recursos en Journey Optimizer B2B edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 23fb478712f3c6df59e94432bdf16883e6acf70b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Recursos

En Adobe Journey Optimizer B2B edition, los recursos suelen ser las imágenes utilizadas para crear el contenido de recorrido. Puede utilizar estas imágenes dentro de los correos electrónicos, las plantillas de correo electrónico y los fragmentos creados en Journey Optimizer B2B edition a través de un selector de recursos o una sencilla interfaz de arrastrar y soltar dentro del editor de contenido visual.

Adobe Journey Optimizer B2B edition ofrece a los especialistas en marketing acceso a dos tipos de bibliotecas de recursos: Adobe Marketo Engage Design Studio y Adobe Experience Manager Assets as a Cloud Service. Solo puede utilizar Adobe Marketo Engage Design Studio o utilizar ambas bibliotecas configuradas al mismo tiempo (según la licencia de AEM Assets que tenga).

## Administración de recursos

Si se le proporciona una cuenta de Marketo Engage y Adobe Experience Manager como Cloud Service, tiene acceso a los repositorios tanto para el DAM de Marketo Engage como para el as a Cloud Service de Adobe Experience Manager Assets cuando su cuenta de usuario tiene los permisos necesarios. Estos repositorios son independientes y no están sincronizados. Puede utilizar imágenes de cualquier origen, pero solo se puede habilitar una a la vez en el editor de contenido. Un administrador puede hacer que el cambio del DAM de Marketo Engage a Adobe Experience Manager Assets sea as a Cloud Service. El elemento _[!UICONTROL Assets]_ de la navegación izquierda muestra el repositorio establecido actualmente.

### Recursos de Adobe Marketo Engage

El repositorio de recursos de Adobe Marketo Engage Design Studio se proporciona de forma predeterminada con cada suscripción a Journey Optimizer B2B edition. Esto significa que tiene acceso a cualquiera de los recursos de imagen almacenados en Adobe Marketo Engage > [!UICONTROL Design Studio] > [!UICONTROL Imágenes y archivos]. Puede utilizar este repositorio como su biblioteca de recursos local, incluidas las funciones de carga y descarga de recursos. También puede utilizar estos recursos dentro del contenido del recorrido.

Existen protecciones integradas que impiden realizar ediciones en los recursos del Marketo Engage desde Journey Optimizer B2B edition, así como eliminar y mover operaciones. Estas protecciones garantizan que los recursos de origen (Marketo Engage Design Studio) se mantengan, al tiempo que permiten una lectura y reutilización sin problemas en Journey Optimizer B2B edition.

Formatos de archivo admitidos: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Una los flujos de trabajo creativos y de marketing de Adobe Experience Manager Assets. Está integrado de forma nativa con Adobe Journey Optimizer B2B edition, por lo que puede acceder fácilmente a Assets as a Cloud Service para descubrir y utilizar recursos digitales. Proporciona acceso al repositorio de Assets para los recursos que puede utilizar para rellenar los mensajes.

Adobe Experience Manager Assets puede conectarse a Adobe Experience Manager Assets as a Cloud Service para espacios de trabajo de recursos centralizados que amplíen su sistema creativo y unifiquen los recursos digitales para la entrega de experiencias. Adobe Experience Manager Assets as a Cloud Service ofrece una solución en la nube fácil de usar para una administración eficiente de activos digitales y operaciones de Dynamic Media. Incorpora sin problemas funciones avanzadas, como inteligencia artificial y aprendizaje automático.

Obtenga más información en la [documentación de Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/overview).

Se puede acceder a Adobe Experience Manager Assets directamente desde Adobe Journey Optimizer B2B edition desde el elemento **[!UICONTROL Assets]** del menú de navegación de la izquierda. También puede acceder a recursos y carpetas al diseñar un contenido de correo electrónico.

>[!NOTE]
>
>AEM Assets como Cloud Service y las licencias de Dynamic Media son requisitos previos para esta integración.<br/>
>Según el contrato y la configuración, se puede acceder al as a Cloud Service de Adobe Experience Manager Assets directamente desde Adobe Journey Optimizer B2B edition a través del menú izquierdo de la sección de Assets. También puede acceder a recursos y carpetas al diseñar un contenido de correo electrónico.

Actualmente, solo puede utilizar imágenes de Adobe Experience Manager Assets en Adobe Journey Optimizer B2B edition.

## Uso de recursos para la creación de contenido

Utilice recursos a medida que crea sus correos electrónicos, plantillas de correo electrónico y fragmentos visuales. La interfaz de usuario del editor de contenido visual proporciona acceso a las imágenes de los repositorios de recursos conectados.

### Elegir un origen de recursos

Si tiene una suscripción al as a Cloud Service de Experience Manager Assets junto con el Adobe Marketo Engage Design Studio predeterminado, puede elegir recursos de imagen de cualquier origen. Para ello, debe seleccionar el origen de la imagen en el momento de la creación para un nuevo correo electrónico, plantilla de correo electrónico o fragmento visual. O bien, puede seleccionar el origen de la imagen cuando edite el contenido. La selección solo se aplica a la experiencia de edición y puede cambiar el origen de la imagen para acceder a los recursos de otra biblioteca cuando sea necesario.

_**Creación de un recurso de contenido**_: para elegir un origen de imagen al crear un correo electrónico, una plantilla de correo electrónico o un fragmento, establezca el **[!UICONTROL origen de imagen]** en el cuadro de diálogo.

_**Edición de un recurso de contenido**_: para elegir un origen de recurso de imagen en la vista previa visual, use la configuración **[!UICONTROL Origen de imagen]** en el panel de la derecha.

### Añadir recursos al contenido

Puede añadir un recurso de imagen a medida que crea el contenido, según el origen del recurso de imagen seleccionado.

>[!BEGINTABS]

>[!TAB Agregar recursos de imagen de Marketo Engage]

Puede agregar recursos de Marketo Engage mediante cualquiera de los siguientes métodos:

* Agregue un elemento estructural y, a continuación, arrastre y suelte los recursos desde la navegación izquierda al lienzo visual.
* Agregue un elemento estructural y, a continuación, arrastre y suelte el tipo de contenido _image_ en la estructura. En la configuración de propiedades de la derecha, hay dos formas de especificar la imagen:
   * Haga clic en **[!UICONTROL Examinar]** para abrir el selector de recursos, donde puede elegir una imagen de la biblioteca de recursos de Adobe Marketo Engage Design Studio.
   * Haga clic en **[!UICONTROL Importar medios]** para importar un recurso de su sistema local. El recurso importado se almacena en la carpeta raíz de Assets de la biblioteca de Adobe Marketo Engage Design Studio.

Consulte [Usar recursos en el contenido](./marketo-engage-design-studio.md#use-assets-in-your-content) para obtener más información.

Para cambiar la imagen, puede actualizar la dirección URL de origen de la imagen en las propiedades de la derecha.

>[!TAB Agregar imágenes de Experience Manager Assets]

1. Durante la creación del contenido del correo electrónico en el diseñador de correo electrónico, arrastre un elemento de imagen al lienzo.

   Las propiedades de la derecha reflejan la selección del elemento de imagen.

1. Haga clic en **[!UICONTROL Seleccionar un recurso]** para abrir el selector de recursos del Experience Manager.

   Aquí puede buscar, filtrar y acceder al recurso de contenido deseado para añadirlo a su recurso de marketing. Puede consultar esta página para obtener más información sobre cómo utilizar el selector.

   >[!NOTE]
   >
   >Si hay más de un repositorio configurado, puede utilizar el conmutador de repositorios en el Selector de recursos

1. Seleccione el recurso que desee que se inserte en el correo electrónico.

>[!ENDTABS]
