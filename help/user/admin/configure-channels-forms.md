---
title: Configuraciones de Forms
description: Aprenda a configurar los ajustes preestablecidos del formulario.
feature: Setup, Channels
role: Admin
autotag-review: '2026-05-27T16:06:59.553Z'
TQID: 'https://experienceleague.adobe.com/GFW5SZ5Z-phoEIE6jTVD7EgwcT1Vx647mjoLXJejbFg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 955fac784a8f438ec2f9aaf66e9aaeefda58e2a7
workflow-type: tm+mt
source-wordcount: 542
ht-degree: 3%

---

# Configuraciones de Forms

Para que los especialistas en marketing puedan [crear y publicar formularios](../content/forms.md) para usarlos en sus páginas de aterrizaje, un administrador de productos debe crear uno o más ajustes preestablecidos dedicados. Cada ajuste preestablecido define el extremo de conexión utilizado para enviar los datos de envío del formulario y el conjunto de datos utilizado para almacenar los datos capturados.

Cuando los datos aterrizan en el extremo de flujo continuo, se vinculan con la información del conjunto de datos. Mediante las conexiones de origen/destino generadas y el flujo de origen, los datos se insertan en el conjunto de datos.

>[!BEGINSHADEBOX]

## Prerrequisitos

Para usar formularios web, debes tener una o más _&#x200B;**conexiones de streaming de API HTTP**&#x200B;_ definidas en Adobe Experience Platform. Asegúrese de que cada conexión que desea utilizar cumple los siguientes requisitos:

* El tipo de datos debe establecerse en XDM (no en datos sin procesar)
* La autenticación debe estar deshabilitada (conexión no autenticada)

Para obtener información detallada sobre cómo crear conexiones de origen de flujo continuo, consulte la [_documentación de Experience Platform_](https://experienceleague.adobe.com/es/docs/experience-platform/sources/ui-tutorials/create/streaming/http).

La configuración del canal de Forms en Journey Optimizer B2B edition requiere los siguientes [permisos](../admin/user-management.md#b2b-product-permissions):

* _[!UICONTROL Configuraciones de canal B2B]_ > _[!UICONTROL Ver ajustes preestablecidos de Forms]_: necesario para ver las configuraciones preestablecidas de formularios.
* _[!UICONTROL Configuraciones de canal B2B]_ > _[!UICONTROL Administrar ajustes preestablecidos de Forms]_: necesario para crear, actualizar y eliminar configuraciones preestablecidas de formularios.
* _[!UICONTROL Configuraciones de canal B2B]_ > _[!UICONTROL Publicar ajustes preestablecidos de Forms]_: necesario para publicar configuraciones preestablecidas de formularios.

>[!ENDSHADEBOX]

## Directrices de configuración de formularios preestablecidos

Al crear un ajuste preestablecido:

* Puede configurar varios ajustes preestablecidos utilizando diferentes combinaciones de conjuntos de datos y conexiones de flujo continuo.

* Puede reutilizar el mismo conjunto de datos o conexión de flujo continuo en varios ajustes preestablecidos.

* Cada conexión de flujo continuo genera automáticamente recursos como, por ejemplo:

   * _Conexión de Source_ - donde se originan los datos.
   * _Conexión de destino_ - donde se almacenan o consumen los datos.
   * _Flujo de Source_: la canalización que mueve datos de la conexión de origen a Experience Platform. Gestiona la asignación, la transformación y la validación.

## Crear un ajuste preestablecido de un formulario

1. En el panel de navegación izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**.

1. En _[!UICONTROL Configuración de formulario]_ en el panel de navegación, seleccione **[!UICONTROL Ajustes preestablecidos de formulario]**.

   ![Acceder a las configuraciones del formulario](./assets/config-channels-forms.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Crear ajuste preestablecido de formulario]**.

1. Escriba un **[!UICONTROL Nombre]** único (obligatorio) y una **[!UICONTROL Descripción]** (opcional) para la configuración.

   >[!NOTE]
   >
   >Los nombres deben comenzar por una letra (A-Z) y solo pueden contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto `.` y guión `-`.

1. Seleccione la **[!UICONTROL conexión de transmisión]**.

   Esta conexión es el extremo de flujo continuo utilizado para enviar los datos cuando un visor web envía un formulario. Si la conexión de flujo continuo necesaria no aparece en la lista, compruebe que se cumplen los requisitos.

1. Haga clic en el icono _Seleccionar conjunto de datos_ ( ![Seleccionar icono del conjunto de datos](../assets/do-not-localize/icon-select-data.svg) ) para vincular un conjunto de datos con el formulario.

   En el conjunto de datos es donde se almacenan y reflejan las respuestas del formulario. Puede introducir una cadena de texto para buscar un conjunto de datos específico o seleccionarlo en la lista.

   ![Cuadro de diálogo Seleccionar conjuntos de datos](./assets/config-channel-forms-select-datasets.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >Actualmente, solo se pueden seleccionar [conjuntos de datos de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview) habilitados para perfiles y no habilitados para perfiles. Se puede seleccionar un conjunto de datos a la vez. Los conjuntos de datos del sistema no se pueden usar para guardar datos de formulario.

   Seleccione la casilla de verificación del conjunto de datos y haga clic en **[!UICONTROL Seleccionar]**.

1. Haga clic en **[!UICONTROL Guardar como borrador]**.

## Publicar un ajuste preestablecido de formulario

1. Haga clic en el nombre del ajuste preestablecido del formulario para abrir la página de configuración.

   Si es necesario, puede realizar los ajustes necesarios en el borrador.

1. Haga clic en **[!UICONTROL Publicar]**.

   Cuando el ajuste preestablecido del formulario aparece en la lista con el estado _Publicado_, está disponible para su uso durante la creación del formulario.
