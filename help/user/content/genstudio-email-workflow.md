---
title: Creación de contenido de correo electrónico con GenStudio for Performance Marketing
description: Aprenda a integrar con flujos de trabajo de GenStudio para optimizar el diseño de experiencias de correo electrónico.
feature: Email Authoring, Content, Integrations
topic: Content Supply Chain
level: Intermediate
role: User
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: fe54f7eba982a29461aa922b408e6b4d68e6b0e2
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 4%

---

# Creación de contenido de correo electrónico con GenStudio for Performance Marketing {#genstudio-workflow}

>[!CONTEXTUALHELP]
>id="ajo-b2b_genstudio_button"
>title="Uso de una plantilla creada con GenStudio"
>abstract="Utilice la integración con Adobe GenStudio for Performance Marketing para importar una plantilla de GenStudio mejorada con la tecnología de IA de Adobe."

>[!AVAILABILITY]
>
>La integración de GenStudio en [!DNL Adobe Journey Optimizer B2B Edition] no está disponible actualmente para su uso con las ofertas de complementos de **Healthcare Shield** o **Privacy and Security Shield**.
>
>Esta integración solo está disponible para el canal de correo electrónico.

Para mejorar la eficacia del flujo de trabajo y mantener la coherencia de la marca, puede combinar experiencias de GenStudio for Performance Marketing con la orquestación por correo electrónico de Adobe Journey Optimizer B2B edition. Este flujo de trabajo ampliado le permite aprovechar las herramientas de creación de contenido con potencia de IA de GenStudio para expandir y maximizar las comunicaciones por correo electrónico mediante los recorridos de cuenta.

Por ejemplo, un experto en marketing técnico que utilice Journey Optimizer B2B edition para desarrollar y automatizar las comunicaciones por correo electrónico a cuentas clave puede colaborar con un experto en marketing que cree contenido mediante GenStudio. Con este flujo de trabajo, ambos pueden trabajar juntos para combinar contenido de marca de GenStudio en la automatización de marketing basada en cuentas de Journey Optimizer B2B edition, lo que proporciona correos electrónicos atractivos dirigidos a grupos de compra específicos e impulsan las ventas.

>[!BEGINSHADEBOX]

## Funciones de generación de contenido de GenStudio

[Adobe GenStudio for Performance Marketing](https://business.adobe.com/products/genstudio-for-performance-marketing.html?lang=es){target="_blank"} es una aplicación generativa de IA-First que permite a los equipos de marketing crear anuncios y correos electrónicos impactantes y personalizados que se ajusten a los estándares de marca y cumplan con sus políticas empresariales. Al aprovechar la tecnología de IA de Adobe, proporciona un conjunto completo de herramientas que simplifican las complejidades de la creación y administración de contenido para que los creativos puedan centrarse en la innovación.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Crear correos electrónicos de marketing en la marca](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing-learn/tutorials/creating-experiences/creating-on-brand-emails){target="_blank"}

Obtenga más información acerca de las funcionalidades de GenStudio for Performance Marketing en la [documentación](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"}

>[!ENDSHADEBOX]

## Exportar HTML desde Journey Optimizer B2B edition

En primer lugar, en Journey Optimizer B2B edition, exporte HTML desde un correo electrónico que incluya las directrices de su marca.

1. En Journey Optimizer B2B edition, acceda al contenido del correo electrónico en el espacio de diseño visual.

1. En el menú _[!UICONTROL Más...]_ de la parte superior del espacio de diseño del correo electrónico, elija **[!UICONTROL Exportar HTML]**.

   ![Haga clic en Más y elija Exportar HTML](./assets/email-export-html.png){width="600"}

   Esta acción genera un archivo .zip descargado que contiene los archivos de imagen y HTML.

## Uso del HTML exportado en GenStudio for Performance Marketing

GenStudio for Performance Marketing reconoce ciertos elementos dentro de la HTML de correo electrónico importada cuando se identifican con un nombre de campo reconocido. Agregue nombres de campo en la HTML exportada mediante la sintaxis Handlebars, donde necesita que GenStudio for Performance Marketing genere un determinado tipo de contenido.

| Campo | Tipo de contenido |
| ----------------- | ------------------------- |
| `{{pre_header}}` | Preencabezado |
| `{{headline}}` | Encabezado |
| `{{sub_headline}}` | Subtítulo |
| `{{body}}` | Texto independiente |
| `{{cta}}` | Call to action (botón) |
| `{{image}}` | Imagen |
| `{{link}}` | Call to action en la imagen |

### Creación de la plantilla

Utilice el archivo HTML para crear una plantilla en GenStudio for Performance Marketing.

Para obtener información detallada sobre cómo cargar una plantilla de HTML en GenStudio en Adobe GenStudio for Performance Marketing, consulte [Agregar una plantilla](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#add-a-template) en la documentación de GenStudio for Performance Marketing.

Al cargar la HTML exportada como plantilla, GenStudio for Performance Marketing busca en el archivo HTML campos reconocidos. Utilice la vista previa para revisar los elementos de plantilla y confirmar que los ha identificado correctamente con los nombres de campo reconocidos.

### Generar experiencias de correo electrónico

En GenStudio for Performance Marketing, utilice la plantilla para crear varias variaciones de experiencia de correo electrónico y guardarlas.

Para obtener información detallada sobre cómo generar experiencias de correo electrónico de marca, consulte [Crear una experiencia de correo electrónico](https://experienceleague.adobe.com/es/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience) en la documentación de GenStudio for Performance Marketing.

## Añadir experiencias de correo electrónico generadas a Journey Optimizer B2B edition

>[!NOTE]
>
>La integración de GenStudio for Performance Marketing solo está disponible para crear correos electrónicos y no para crear plantillas.

Para utilizar las variaciones de correo electrónico de GenStudio creadas a partir del archivo de HTML de correo electrónico de Journey Optimizer B2B edition exportado, siga estos pasos:

1. En Journey Optimizer B2B edition, [agregue un correo electrónico](./add-email.md) al recorrido de una cuenta mediante un nodo _[!UICONTROL Realizar una acción]_.

   * Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.

   * Para la _[!UICONTROL acción sobre personas]_, elige **[!UICONTROL Enviar correo electrónico]**.

     ![Realizar una acción: enviar un correo electrónico](./assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Para el _[!UICONTROL origen del correo electrónico]_, elija **[!UICONTROL Crear nuevo correo electrónico]** para crear el correo electrónico de forma nativa en Journey Optimizer B2B edition.

1. En la página _Crear tu correo electrónico_, selecciona **[!UICONTROL Importar HTML]**.

1. En el cuadro de diálogo _[!UICONTROL Importar tu correo electrónico]_, haz clic en **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![Importar HTML desde GenStudio for Performance Marketing](./assets/email-import-html-genstudio.png){width="500" zoomable="yes"}

1. Examine las experiencias publicadas.

   Puede filtrar las experiencias según varios criterios, como _Plantilla_ y _Creada por_.

   ![Importar HTML desde GenStudio for Performance Marketing](./assets/email-import-select-gen-studio-experience.png){width="600" zoomable="yes"}

1. Seleccione una experiencia y haga clic en **[!UICONTROL Usar]** para comenzar a crear el contenido del correo electrónico.

   >[!NOTE]
   >
   >Las experiencias de GenStudio creadas a partir de una plantilla de Journey Optimizer B2B edition o Marketo Engage se importan directamente en el espacio de diseño de correo electrónico. Las experiencias creadas sin una plantilla de Journey Optimizer B2B edition se importan en modo de compatibilidad.

1. Use [el contenido del correo electrónico y las herramientas de personalización](./email-authoring.md) para editar su correo electrónico según sea necesario y guardarlo.

   ![Importar HTML desde GenStudio for Performance Marketing](./assets/email-imported-experience.png){width="800" zoomable="yes"}
