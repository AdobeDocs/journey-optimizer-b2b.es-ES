---
title: Creación de WhatsApp
description: Cree mensajes de WhatsApp para recorridos de cuenta con plantillas de Meta aprobadas, tokens de personalización y configuraciones de entrega en Journey Optimizer B2B edition.
feature: Content, Channels, Account Journeys
role: User
exl-id: 36c7e377-1f51-4d68-9e00-c6ce994e9909
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: f01b5556-e951-40ba-8625-2e3001864f2bid: a4b836d9-ffdd-4df3-a62a-f78b830cf059
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 94a8ed9584459cf85a72448cd698740ef450ddb2
workflow-type: tm+mt
source-wordcount: 828
ht-degree: 1%

---

# Creación de WhatsApp

Utiliza Adobe Journey Optimizer B2B edition para enviar mensajes de WhatsApp a los miembros de la cuenta en sus dispositivos móviles. Puede crear, personalizar y previsualizar mensajes utilizando plantillas de mensaje de Meta aprobadas desde el editor de WhatsApp. <!-- Test your WhatsApp messages before publishing the account journey to ensure your intended rendering, accurate personalization, and proper configuration of all settings. -->

Antes de crear mensajes de WhatsApp para recorridos de cuenta, asegúrate de que tienes el [canal de WhatsApp configurado](../admin/configure-channels-whatsapp.md) necesario en la configuración de _[!UICONTROL Administrator]_.

>[!NOTE]
>
>Solo se admiten _elementos de mensaje de WhatsApp de salida_ en Journey Optimizer B2B edition.

+++ Elementos de mensaje compatibles y opciones de llamadas a la acción

WhatsApp admite los siguientes tipos de mensajes:

| Elemento de mensaje | Descripción |
| - | - |
| Encabezados | Texto opcional que aparece encima del cuerpo del mensaje. |
| Texto | Admite contenido dinámico mediante parámetros. |
| Imágenes (JPEG, PNG) | Debe tener un formato RGB o RGBA de 8 bits y un tamaño inferior a 5 MB. |
| Vídeos | Debe ser 3GPP o MP4, de menos de 16 MB y alojado por una dirección URL. |
| Audio | Solo disponible para mensajes de respuesta. Debe tener el formato AAC, AMR, MP3, MP4 audio u OGG, alojado en una dirección URL y inferior a 16 MB. |
| Documentos | Debe tener menos de 100 MB, estar alojado en una dirección URL y tener uno de los siguientes formatos: `.txt`, `.xls`/`.xlsx`, `.doc`/`.docx`, `.ppt`/`.pptx` o `.pdf`. |
| Texto independiente | Admite contenido dinámico mediante parámetros. |
| Texto del pie | Admite contenido dinámico mediante parámetros. |

Las siguientes opciones de call-to-action están disponibles para tus mensajes de WhatsApp:

| Call to action | Descripción |
| - | - |
| Visitar sitio web | Solo se permite un botón, con parámetros de variable incluidos. |
| Llamar en WhatsApp | Proporciona un botón que abre un chat de WhatsApp con el número de teléfono especificado directamente desde el mensaje. |
| Número de teléfono de llamada | Proporciona un botón que inicia una llamada telefónica al número especificado cuando el usuario lo pulsa. |

+++

## Añadir una acción de WhatsApp en un recorrido de cuenta

Puede configurar los envíos de mensajes de WhatsApp en un recorrido de cuenta al [agregar un nodo _[!UICONTROL Realizar una acción]_](../journeys/action-nodes.md) y hacer lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.

1. Para la _[!UICONTROL Acción sobre personas]_, elige **[!UICONTROL Enviar WhatsApp]**.

   ![Realizar una acción: enviar WhatsApp](./assets/whatsapp-journey-node.png){width="500" zoomable="yes"}

## Creación del mensaje de WhatsApp

1. En la parte inferior del panel _[!UICONTROL Realizar una acción]_, haz clic en **[!UICONTROL Crear WhatsApp]**.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único (obligatorio) y **[!UICONTROL Descripción]** (opcional) para el mensaje de WhatsApp.

   ![Crear nuevo diálogo de mensaje de WhatsApp](./assets/whatsapp-create-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

   Se abre el _espacio de diseño de WhatsApp_, donde puedes definir las acciones de WhatsApp y crear el contenido para enviar el mensaje.

### Seleccione la configuración de acciones

1. En el _espacio de diseño de WhatsApp_, selecciona la pestaña **[!UICONTROL Acciones]**.

1. Para la **[!UICONTROL configuración de WhatsApp]**, selecciona la [configuración](../admin/configure-channels-whatsapp.md#create-channel-configuration) que admite las acciones de marketing y la configuración de envío de mensajes según tus necesidades.

   ![Crear WhatsApp: ficha Acciones](./assets/whatsapp-create-actions-tab.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar contenido]** para pasar a los parámetros y al texto del mensaje.

### Seleccione una plantilla de mensaje

>[!IMPORTANT]
>
>**Administración de consentimientos de WhatsApp**: De acuerdo con las políticas de Meta y las regulaciones aplicables, todos los mensajes de marketing de WhatsApp deben enviarse únicamente a los destinatarios que se hayan suscrito para recibir comunicaciones. Los destinatarios de WhatsApp pueden excluirse en cualquier momento respondiendo con una palabra clave de exclusión. Las respuestas de exclusión se respetan automáticamente y los perfiles correspondientes se eliminan de las futuras audiencias de mensajes de marketing. Para obtener detalles sobre cómo se evalúan las preferencias de consentimiento de WhatsApp en el momento de la entrega, consulte [Preferencias de consentimiento](./channels-consent-preferences.md).

Los mensajes de WhatsApp se envían utilizando plantillas de mensaje aprobadas previamente desde su cuenta de Meta WhatsApp Business. **Meta debe revisar y aprobar las plantillas** para poder usarlas en Journey Optimizer B2B edition. Trabaje con el administrador de su cuenta de [!DNL Meta Business Manager] para administrar y enviar las plantillas para su aprobación.

1. Para **[!UICONTROL Seleccionar categoría de plantilla]**, elija una de las siguientes opciones:

   * Marketing
   * Utilidad
   * Autenticación

1. Para **[!UICONTROL Seleccionar la plantilla de WhatsApp]**, elige una plantilla aprobada para la cuenta de configuración del negocio.

   El contenido de la plantilla se carga en el editor de mensajes, mostrando la estructura de la plantilla y los campos de variables disponibles para la personalización.

   ![Plantilla de mensaje de WhatsApp seleccionada con mensaje cargado en la ventana de vista previa](./assets/whatsapp-create-select-template.png){width="700" zoomable="yes"}

   Las plantillas están organizadas por categoría (_Marketing_, _Utilidad_ y _Autenticación_) y estado. Solo hay **_plantillas aprobadas_** disponibles para su selección. Para obtener más información sobre cómo crear plantillas de WhatsApp, consulta [_Crear plantillas de mensajes para tu cuenta de WhatsApp Business_](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343) en la documentación de Meta.

### URL de imagen

Si la plantilla incluye imágenes, use el campo **[!UICONTROL URL de imagen]** para agregar URL de medios y reemplazar los marcadores de posición en la plantilla. Los medios de plantilla de Meta solo son marcadores de posición. Para mostrar imágenes, audio o vídeo correctamente, debe utilizar direcciones URL externas de Adobe Experience Manager u otras fuentes.

### Personalización del contenido del mensaje

Las plantillas de WhatsApp aprobadas pueden incluir marcadores de posición variables que se definen con datos de perfil o valores dinámicos.

Para cada campo de variable mostrado en la plantilla, haga clic en el icono _Personalizar_ ( ![Personalizar icono](../assets/do-not-localize/icon-personalize.svg) ) junto al campo.

![Variables en la plantilla de WhatsApp](./assets/whatsapp-create-variables.png){width="700" zoomable="yes"}

El cuadro de diálogo proporciona acceso a los tokens de cuenta, tokens de persona y tokens del sistema. Se incluyen tokens estándar y personalizados. Puede usar la barra _Buscar_ para encontrar el token que necesita, o navegar por el árbol de carpetas para buscar y seleccionar cualquiera de los tokens.

Para obtener información detallada sobre el uso de tokens para la personalización, consulte [Personalización de contenido](./personalization.md).

Cuando se definan los tokens de personalización, haz clic en **[!UICONTROL Guardar]** para guardar los cambios y volver al área de trabajo principal de mensajes de WhatsApp.
