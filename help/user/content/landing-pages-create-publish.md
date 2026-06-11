---
title: Crear y publicar de páginas de aterrizaje
description: 'Cree, diseñe y publique páginas de aterrizaje para recorridos: genere desde cero, importe HTML, añada formularios, personalice contenido y vincule desde correos electrónicos en Journey Optimizer B2B edition.'
feature: Landing Pages, Content
role: User
autotag-review: '2026-05-27T16:10:09.537Z'
TQID: 'https://experienceleague.adobe.com/e-tguY-9v6CPOehYL7vI22fzQBk3L0h1EOpa-e54q7A'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e4bd5f48-22a4-465d-a046-5ffb52e27856
source-git-commit: 144848cff6a37691ccbe7a83b78f9db33d8a2b3d
workflow-type: tm+mt
source-wordcount: 1719
ht-degree: 5%

---

# Creación y publicación de páginas de destino

Como especialista en marketing, puede definir y publicar páginas que desee incorporar en los recorridos de cuenta y persona. Cuando se agrega una nueva página de aterrizaje, se configura la página principal y las subpáginas, se diseña el contenido, se prueba y se publica.

![Diagrama del flujo de trabajo de la página de aterrizaje](./assets/landing-page-work-flow-diagram-no-subpages.svg)

>[!BEGINSHADEBOX]

## Requisitos previos de página de aterrizaje {#landing-page-prerequisites}

Para que los especialistas en marketing puedan crear páginas de aterrizaje que admitan sus recorridos y campañas, deben haberse configurado las siguientes configuraciones y recursos:

* [Subdominio de página de aterrizaje](../admin/configure-channels-landing-pages.md#lp-subdomains): configure un subdominio dedicado a alojar sus páginas de aterrizaje.
* [Ajuste preestablecido de página de aterrizaje](../admin/configure-channels-landing-pages.md#lp-presets): un ajuste preestablecido define el subdominio y otra configuración aplicada a sus páginas de aterrizaje.
* [Formulario](./forms.md) (para casos de uso de captura de datos): requerido cuando desee incrustar un formulario en una página de aterrizaje y enviar datos a Experience Platform.
  <!-- * Subscription list (for subscription use cases) - Required if you want customers to subscribe to or unsubscribe from a specific service. This is in AJO B2C-->

>[!ENDSHADEBOX]

## Creación de una página de destino {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_create"
>title="Definir y configurar la página de destino"
>abstract="Para crear una página de destino, debe seleccionar un ajuste preestablecido, configurar la página principal y las subpáginas y, por último, probar la página antes de publicarla."

1. Vaya a la navegación de la izquierda y seleccione **[!UICONTROL Administración de contenido]** > **[!UICONTROL Páginas de aterrizaje]**.

1. Haga clic en **[!UICONTROL Crear página de aterrizaje]** en la parte superior derecha.

1. En la página, escriba un **[!UICONTROL Título]** (obligatorio) y una **[!UICONTROL Descripción]** (opcional) que sean útiles.

   Título y criterios de descripción:

   * Título: máximo de 100 caracteres, debe ser único, sin distinción de mayúsculas y minúsculas

   * Descripción: máximo de 300 caracteres

   * Se permiten caracteres Alpha, numéricos y especiales

   * Los caracteres reservados **_no se permiten_**: `\ / : * ? " < > |`

   ![Crear página de aterrizaje](./assets/landing-page-create.png){width="600"}

1. Seleccione un **[!UICONTROL ajuste preestablecido]**.

   Un administrador de productos [configura un ajuste preestablecido](../admin/configure-channels-landing-pages.md#lp-presets) para definir el subdominio y otras opciones de configuración utilizadas para las páginas de aterrizaje. Puede seleccionar un ajuste preestablecido y, a continuación, hacer clic en **[!UICONTROL Ver ajuste preestablecido]** para abrir los detalles del ajuste preestablecido y comprobar su configuración para asegurarse de que coincida con los requisitos de su página de aterrizaje.

1. Haga clic en **[!UICONTROL Crear]**.

   Se muestran la página principal y sus propiedades.

   ![Nueva página de aterrizaje - propiedades de la página principal](./assets/landing-page-primary-new-properties.png){width="700" zoomable="yes"}

## Configuración de la página principal {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_primary_page"
>title="Definir la configuración de la página principal"
>abstract="Defina la página principal, que se muestra inmediatamente cuando un destinatario hace clic en el vínculo de la página de aterrizaje, como desde un correo electrónico o un sitio web."

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_access_settings"
>title="Definir la dirección URL de la página de destino"
>abstract="En esta sección, defina una dirección URL de página de destino única. La primera parte de la URL requiere que haya configurado previamente un subdominio de página de aterrizaje como parte del ajuste preestablecido que ha seleccionado."

1. Cambie **[!UICONTROL Page Name]** según sus necesidades, que es _Primary page_ de forma predeterminada.

1. Defina la parte final de la dirección URL de la página.

   El ajuste preestablecido que ha seleccionado determina la primera parte de la dirección URL.

   >[!CAUTION]
   >
   >La dirección URL de la página de aterrizaje debe ser única.
   >
   >No puede acceder a la página de aterrizaje simplemente copiando y pegando esta URL en un explorador web, aunque esté publicada. Pruébelo con la función de previsualización.

1. Si desea una página de aterrizaje anónima, deshabilite la opción **[!UICONTROL Requerir usuarios identificados]**.

   <!-- The option 'Require identified users' would be visible in both AJO & AJOB2B when the Landing page is of type 'Data capture' -->

1. Haga clic en el icono _Calendario_ ( ![Icono de calendario](../assets/do-not-localize/icon-calendar.svg) ) para establecer la **[!UICONTROL caducidad de la página]**.

   Después de seleccionar una fecha de caducidad, elija la acción tras la caducidad de la página:

   * **[!UICONTROL URL de redireccionamiento]**: introduzca la URL de la página que se utilizará como redireccionamiento.

     ![Caducidad de la página de aterrizaje: URL de redireccionamiento](./assets/landing-page-expiry-redirect-url.png){width="400"}

     <!-- * **[!UICONTROL Custom page]** - Configure a subpage and select it from the list. -->
   * **[!UICONTROL Error del explorador]**: escriba el texto del error que se mostrará en lugar de la página.

     ![Caducidad de la página de aterrizaje: error del explorador](./assets/landing-page-expiry-browser-error.png){width="400"}

## Elija el tipo de diseño de contenido {#choose-design-type}

Para agregar _[!UICONTROL Contenido]_ para la página, haga clic en **[!UICONTROL Abrir Designer]**. La página de inicio _[!UICONTROL Crear tu página de aterrizaje principal]_ se carga y el proceso de diseño comienza con la elección de cómo quieres iniciar el diseño:

* [[!UICONTROL Diseñar desde cero]](#design-from-scratch)
* [[!UICONTROL Codifique usted mismo]](#code-your-own)
* [[!UICONTROL Importar HTML]](#import-html)
* [Uso de una plantilla de página de aterrizaje](#select-template)

![Elige cómo deseas iniciar el diseño de tu página de aterrizaje](./assets/landing-page-create-design.png){width="800" zoomable="yes"}

Después de seleccionar el método preferido para iniciar el diseño de la página de aterrizaje, usa las herramientas de diseño visual para [completar el contenido de la página](./landing-page-design.md).

### Diseñe desde cero {#design-from-scratch}

Utilice el editor de contenido visual para definir la estructura del contenido de la página de aterrizaje. Al agregar y mover componentes estructurales con sencillas acciones de arrastrar y soltar, puede diseñar la forma del contenido de la página en cuestión de segundos.

1. En la página de inicio _[!UICONTROL Crear su página de aterrizaje principal]_, seleccione la opción **[!UICONTROL Diseñar desde cero]**.

1. Elija cómo desea administrar el estilo del contenido de la página:

   * **[!UICONTROL Usar temas]** - Elija esta opción para crear el contenido de la página en _Modo de temas_. En este modo, puede usar un [tema de marca](./brand-themes.md) definido para optimizar el proceso de creación de contenido y asegurarse de que el diseño se ajuste a los estándares definidos.

   * **[!UICONTROL Estilo manual]**: elija esta opción para crear el contenido de la página en _modo manual_. En este modo, se establece manualmente el estilo para todos los componentes de estructura y contenido que se añaden al lienzo en blanco.

1. Haga clic en **[!UICONTROL Confirmar]**.

1. [Agregar estructura y contenido](./landing-page-design.md#structure-content-landing-page) a la página.

### Codifique su propio código {#code-your-own}

_Codifique su propio código_ le permite escribir o pegar HTML sin procesar para crear el contenido de la página directamente en el espacio de diseño. Utilice este modo cuando necesite un control total sobre el marcado. El uso de este modo requiere habilidades con HTML.

Después de elegir este modo, permanece en el editor de código; no puede cambiar al editor visual.

1. En la página de inicio _[!UICONTROL Crear su página de aterrizaje principal]_, seleccione la opción **[!UICONTROL Codifique su propia página]**.

1. Introduzca o pegue el código de HTML sin procesar.

Si quieres borrar el contenido de tu página y comenzar desde un nuevo diseño, selecciona **[!UICONTROL Cambiar tu diseño]** en el menú de opciones.

### Importar HTML {#import-html}

Adobe Journey Optimizer B2B edition le permite importar contenido existente de HTML para diseñar sus páginas de aterrizaje.

{{$include /help/_includes/content-design-import.md}}

![Importar contenido html en un archivo zip](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>El uso de una etiqueta `<table>` como primera capa de un archivo HTML puede causar la pérdida de estilo, incluida la configuración del fondo y el ancho en la etiqueta de la capa superior.

Puede personalizar el contenido importado según sea necesario con el espacio de diseño visual.

### Seleccionar una plantilla {#select-template}

[!BADGE Beta]{type=Informative tooltip="Función Beta"}

Si desea utilizar una plantilla de página de aterrizaje, puede elegir entre:

* **Plantillas de ejemplo**. La interfaz de B2B edition de Journey Optimizer ofrece una colección de plantillas de página de aterrizaje integradas que puede utilizar como punto de partida para el diseño de páginas de aterrizaje.

* **Plantillas guardadas**. Usar una plantilla personalizada guardada creada por un miembro de su organización mediante el menú _[!UICONTROL Plantillas]_ <!-- or the _[!UICONTROL Save as content template]_ option when designing a landing page. -->

Utilice la sección _[!UICONTROL Seleccionar plantilla de diseño]_ para empezar a crear contenido a partir de una plantilla. Puede utilizar una plantilla de ejemplo o una plantilla de página de aterrizaje personalizada guardada desde la instancia de Journey Optimizer B2B edition.

>[!BEGINTABS]

>[!TAB Plantillas guardadas]

La página de inicio _Crear su página de aterrizaje principal_ muestra la ficha _Plantillas de muestra_ de forma predeterminada. Para usar una plantilla personalizada, selecciona la pestaña **[!UICONTROL Plantillas guardadas]**.

Se muestra la lista de todas las plantillas de página de aterrizaje guardadas. Puede ordenarlos por _[!UICONTROL Nombre]_, _[!UICONTROL Última modificación]_ y _[!UICONTROL Última creación]_.

![Elegir una plantilla guardada](./assets/landing-page-design-saved-templates-sort-by.png){width="700" zoomable="yes"}

Seleccione una miniatura de plantilla para mostrar una previsualización. En el modo de vista previa, puede desplazarse entre todas las plantillas de una categoría (de ejemplo o guardadas, según su selección) utilizando las flechas derecha e izquierda.

![Vista previa de la plantilla guardada](./assets/landing-page-design-saved-template-preview.png){width="800" zoomable="yes"}

Cuando la pantalla coincida con lo que desea usar, haga clic en **[!UICONTROL Usar esta plantilla]** en la parte superior derecha de la ventana de vista previa.

Esta acción copia el contenido en el espacio de diseño visual, donde puede editarlo según sea necesario.

<!-- 
>[!NOTE]
>
>Saved templates may have governance (content locking) settings applied to one or more components. The design tools provide guidelines about locked components when you [author content from a governed template](./email-authoring-governance.md). 
-->

>[!TAB Plantillas de muestra]

Adobe Journey Optimizer B2B edition ofrece una selección de _plantillas de página de aterrizaje predeterminadas_, que se pueden usar para crear sus propias páginas de aterrizaje y plantillas de página de aterrizaje.

<!-- ![Choose a sample template provided by Adobe](../assets/content-design-shared/templates-design-samples.png){width="800" zoomable="yes"} -->

>[!ENDTABS]

## Comprobación de alertas {#check-alerts}

Al diseñar el contenido de la página de aterrizaje, las alertas aparecen en la parte superior derecha cuando falta la configuración clave.

![Alertas por problemas con el contenido de la página](./assets/alerts-button.png){width="250"}

Si no ve este botón, no se detectan problemas.

Existen dos tipos de alertas:

* **_Advertencias_** que hacen referencia a recomendaciones y prácticas recomendadas, como:

   * `Placeholder links are present in the landing page body`: no olvide reemplazar los marcadores de posición con vínculos válidos.

   * `Text version of HTML is empty`: no se olvide de definir una versión de texto del cuerpo de la página, que se utilizará cuando no se pueda mostrar el contenido de HTML.

   * `Empty link is present in page body`: compruebe que todos los vínculos de la página sean correctos.

* **_Errores_** que impiden probar o activar el recorrido o la campaña siempre y cuando no se resuelvan, como:

   * `The landing page content is empty`: el contenido de la página es obligatorio.

## Prueba de la página de destino {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_preview_lp_profiles"
>title="Previsualizar y probar la página de destino"
>abstract="Después de definir la configuración y el contenido de la página de aterrizaje, utilice perfiles de prueba para previsualizar la página."

Cuando se definen la configuración y el contenido de la página de aterrizaje, puede utilizar perfiles de prueba para previsualizar la página. Si ha insertado [contenido personalizado](./personalization.md), puede comprobar cómo se muestra este contenido en la página de aterrizaje mediante los datos del perfil de prueba.

>[!PREREQUISITES]
>
>Para obtener una vista previa y probar páginas de aterrizaje, debe tener el permiso **[!UICONTROL Publicar mensajes]** y un conjunto de datos definido que contenga [perfiles de prueba](../audiences/test-profiles.md).

1. Haga clic en **[!UICONTROL Previsualizar y probar]** para abrir la selección del perfil de prueba.

   >[!NOTE]
   >
   >También puede usar **[!UICONTROL Simular contenido]** cuando se encuentre en el espacio de diseño visual.

1. En la pantalla _[!UICONTROL Simular]_, seleccione un perfil de prueba.

   ![Simular contenido de página de aterrizaje para el perfil seleccionado](./assets/landing-page-simulate.png){width="700" zoomable="yes"}

   Si los perfiles que necesita no aparecen en la lista, haga clic en **[!UICONTROL Administrar perfiles de prueba]** para usar una dirección de correo electrónico conocida de [perfil de prueba](../audiences/test-profiles.md) y agregarla a la lista.

   +++Añadir perfiles de prueba

   Para el área de nombres de identidad **[!UICONTROL Identity]**, haga clic en el icono _Seleccionar_ ( ![Seleccionar icono](../assets/do-not-localize/icon-select-data.svg) ) y elija el área de nombres `Email` que se utilizará para probar los perfiles.

   ![Administrar conjunto de perfiles de prueba Área de nombres de identidad de correo electrónico](./assets/manage-test-profiles.png){width="700" zoomable="yes"}

   En el campo **[!UICONTROL Valor de identidad]**, escriba la dirección de correo electrónico para identificar el perfil de prueba y haga clic en **[!UICONTROL Agregar perfil]**. Puede repetir esto para agregar varios perfiles.

   ![Administrar perfiles de prueba y agregar perfiles](./assets/manage-test-profiles-add.png){width="700" zoomable="yes"}

   Haga clic en la flecha hacia atrás en la parte superior izquierda para regresar a la página _[!UICONTROL Simular]_.

   +++

1. Seleccione **[!UICONTROL Abrir vista previa]** para probar la página de aterrizaje.

   La vista previa de la página de aterrizaje se abre en una nueva pestaña. Los datos del perfil de prueba seleccionados reemplazan a los elementos personalizados.

   ![Vista previa de la página de aterrizaje con datos de perfil](assets/landing-page-preview.png){width="600"}

1. Seleccione otros perfiles de prueba para previsualizar el procesamiento de cada variante de la página de aterrizaje.

## Publicación de la página {#publish-landing-page}

>[!PREREQUISITES]
>
>Para publicar páginas de aterrizaje, debe tener el permiso **[!UICONTROL Publicar mensajes]**.  Antes de publicar, [compruebe y resuelva todas las alertas](#check-alerts).

Cuando la página de borrador cumpla con sus criterios y desee que la página esté disponible para vincularla desde mensajes de recorrido, haga clic en **[!UICONTROL Publicar]** en la parte superior derecha. Y en el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Publicar]**.

![Cuadro de diálogo de confirmación para publicar](./assets/landing-page-publish-confirm.png){width="250"}

Cuando se publica la página de aterrizaje, se muestra en la lista de la página de aterrizaje con el estado **_[!UICONTROL Publicado]_**. Esto significa que está activo y listo para utilizarse en un mensaje de correo electrónico, SMS o WhatsApp enviado a través de un recorrido.

No puede acceder a la página de aterrizaje publicada copiando y pegando la URL en un explorador web. Puede probarlo en cualquier momento con la [función de vista previa](#test-landing-page).

Puede monitorizar el impacto de su página de aterrizaje a través de informes específicos.
