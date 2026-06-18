---
title: Recursos
description: Administre recursos de imagen desde Journey Optimizer B2B edition para correos electrónicos, plantillas y fragmentos visuales.
feature: Assets, Content
role: User
badge: label="Beta" type="Informative"
autotag-review: '2026-06-18T20:11:57.611Z'
TQID: 'https://experienceleague.adobe.com/Xsl4zqpk4xqXuOS85Z5U08tnbv8GWm3FXdqsegPCBI4'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975fid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0e90250101eef0572af0382cc7d24bca727d2b75
workflow-type: tm+mt
source-wordcount: 495
ht-degree: 3%

---

# Recursos

En [!DNL Adobe Journey Optimizer B2B Prime], los recursos suelen ser las imágenes utilizadas al diseñar contenido para admitir recorridos. Puede utilizar estas imágenes en sus correos electrónicos, plantillas de correo electrónico y fragmentos visuales desde el selector de recursos o una sencilla interfaz de arrastrar y soltar dentro del espacio de diseño visual.

Formatos de archivo compatibles: JPG, JPEG, GIF, PNG, EPS, SVG y RGB


>>
La importación de recursos desde sistemas externos como Marketo Engage DAM y el acceso a una biblioteca de recursos previamente completada aún no están disponibles. Se espera que las futuras versiones incluyan la importación de recursos desde sistemas existentes, compatibilidad con carpetas y capacidades ampliadas de administración de recursos.

<!-- You can [edit these assets using Adobe Express](./image-edit-adobe-express.md), and move them into folders to organize them for use across your emails, templates, and fragments. -->

La biblioteca **Assets** proporciona acceso al repositorio centralizado para almacenar y administrar imágenes y otros recursos creativos. Incluye funciones impulsadas por IA que generan metadatos automáticamente y habilitan la búsqueda en lenguaje natural.

En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de contenido]** y seleccione **[!UICONTROL Assets]**.

>[!NOTE]
>
>En esta versión de Beta, puede elegir imágenes y recursos de una copia única de la biblioteca de recursos de Marketo Engage directamente dentro del lienzo del correo electrónico. También puede cargar recursos de imagen adicionales desde la biblioteca _[!UICONTROL Assets]_ o el espacio de diseño de contenido. Estos recursos cargados solo se pueden usar en la instancia [!DNL Adobe Journey Optimizer B2B Prime].

![Biblioteca de Assets](./assets/dam-asset-library-list-view.png){width="800" zoomable="yes"}

>[!BEGINSHADEBOX]

La primera vez que accedas a la biblioteca _[!UICONTROL Assets]_, revisa las _[!UICONTROL Condiciones de uso de la inteligencia artificial aplicada generativa]_ y haz clic en **[!UICONTROL Aceptar y continuar]**.

![Biblioteca de Assets](./assets/dam-asset-library-gen-ai-agree.png){width="500"}

>[!ENDSHADEBOX]

La biblioteca admite dos opciones de diseño:

* **[!UICONTROL Lista]** — Haga clic en el icono _Vista de lista_ ( ![Icono de vista de lista](../../assets/do-not-localize/icon-falco-list-view.svg) ) para mostrar los recursos en una tabla ordenable con columnas de metadatos.
* **[!UICONTROL Galería]**: haga clic en el icono _Vista de galería_ ( ![icono de Vista de galería](../../assets/do-not-localize/icon-falco-gallery-view.svg) ) para mostrar los recursos como una cuadrícula de miniaturas visual.

## Buscar recursos {#find-assets}

Utilice el campo _[!UICONTROL Buscar]_ para buscar recursos, describiendo lo que necesita en lenguaje natural. Los resultados de la búsqueda se basan en metadatos generados por IA, por lo que no se limita a buscar por nombre de archivo.

**Ejemplos:**

* `team members`
* `nature`
* `exercise`

![Imagen seleccionada de los resultados de búsqueda en la biblioteca Assets](./assets/dam-asset-library-select-image.png){width="700" zoomable="yes"}

## Ver detalles del recurso {#view-details}

Seleccione un recurso para abrir su vista de detalles. La vista de detalles muestra una descripción generada por IA, etiquetas, palabras clave y campos de metadatos adicionales. Esta información se genera automáticamente cuando se carga el recurso.

Seleccione cualquier recurso de la vista de lista o de galería para abrir su vista de detalles a la derecha. Seleccione la pestaña Metadatos de IA para ver la descripción, las etiquetas y los metadatos generados por IA.

![Imagen seleccionada de los resultados de búsqueda en la biblioteca Assets](./assets/dam-asset-library-select-image-metadata.png){width="700" zoomable="yes"}

## Cargar un recurso {#upload}

1. Haga clic en **[!UICONTROL Cargar]** en la parte superior derecha.

1. En el cuadro de diálogo, arrastre y suelte un archivo desde el sistema local.

   ![Cargar un recurso de imagen](./assets/dam-upload-assets-dialog.png){width="450"}

   También puede hacer clic en **[!UICONTROL Seleccionar archivo del equipo]** para usar el sistema de archivos local y buscar y seleccionar el archivo.

1. Haga clic en **[!UICONTROL Cargar archivo]** para confirmar y cargar el archivo en el repositorio.

Una vez finalizada la carga, el sistema genera automáticamente una descripción, asigna etiquetas y palabras clave y extrae atributos visuales como asunto y configuración. No se requiere etiquetado manual. La nueva imagen se mostrará con un estado _[!UICONTROL PROCESANDO]_ hasta que finalice este proceso.

![Nuevo recurso de imagen en estado de procesamiento](./assets/dam-asset-library-upload-processing.png){width="700" zoomable="yes"}
<!-- -->
