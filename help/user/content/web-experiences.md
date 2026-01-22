---
title: Experiencias web
description: 'Cree, diseñe y publique experiencias web personalizadas para recorridos de cuentas: envíe modificaciones de contenido de destino a los visitantes de sitios web en Journey Optimizer B2B edition.'
feature: Content, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
source-git-commit: e3c00ab4657c7bf05573e049bbcb4bb3628e751e
workflow-type: tm+mt
source-wordcount: '1497'
ht-degree: 1%

---

# Experiencias web

El canal web de Adobe Journey Optimizer B2B edition le permite crear experiencias personalizadas directamente en el sitio web, lo que le ayuda a conectarse con los clientes de formas significativas. Esta función ofrece un kit de herramientas flexible que puede utilizar para mejorar la participación con contenido personalizado e integrarlo sin problemas con otros canales, como correo electrónico y SMS.

Las experiencias web le permiten:

* Entrega de modificaciones de contenido personalizadas a los visitantes de un sitio web segmentado
* Personalice elementos de sitios web como titulares, texto, imágenes y botones en función de atributos de cuenta
* Páginas específicas de destino o aplicar cambios en varias páginas mediante reglas de coincidencia de URL
* Rastree la participación y monitorice el impacto de sus esfuerzos de personalización web

>[!BEGINSHADEBOX]

## Requisitos previos

Antes de crear experiencias web, asegúrese de que se cumplen los siguientes requisitos:

* Un administrador de productos ha configurado uno o más canales web para definir las direcciones URL (páginas) que se incluirán en una experiencia web. Para obtener más información, vea [Configuraciones del canal Web](../admin/configure-channels-web.md).

* Su sitio web tiene [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementado para la identificación de visitantes y la entrega de contenido. Asegúrese de que la versión de Adobe Experience Platform Web SDK sea 2.16 o superior.

* Tiene los [permisos](../admin/user-management.md#b2b-product-permissions) necesarios para crear y administrar experiencias web en un recorrido:
   * _[!UICONTROL Campañas]_ > _[!UICONTROL Administrar campañas]_: necesario para agregar o actualizar un nodo de acción de personalización web.
   * _[!UICONTROL Campañas]_ > _[!UICONTROL Ver campañas]_ - Necesario para ver detalles de nodos de acción de personalización web.
   * _[!UICONTROL Campañas]_ > _[!UICONTROL Aprobar y publicar campañas]_ - Necesario para publicar un recorrido que tenga uno o más nodos de acción de personalización web.

* Tiene instalada la extensión de explorador [Ayuda de edición visual](#install-the-visual-editing-helper-extension) de Adobe Experience Cloud para su explorador web. Esta extensión es necesaria para abrir, crear y previsualizar las páginas web de forma fiable en el espacio de diseño de contenido de Journey Optimizer B2B edition.

  >[!NOTE]
  >
  >Google Chrome y Microsoft Edge son actualmente los únicos exploradores que admiten la creación de páginas web en Journey Optimizer B2B edition.

>[!ENDSHADEBOX]

## Instale la extensión Ayuda de edición visual

1. Abra una ficha nueva en el explorador ([!DNL Google Chrome] o [!DNL Microsoft Edge]).

1. Vaya a [Google Chrome Web Store](https://chromewebstore.google.com/category/extensions).

   Si usas [!DNL Microsoft Edge], selecciona _Permitir extensiones_ de otras tiendas en el banner superior. Si habilita esta opción, podrá agregar extensiones de [!DNL Chrome Web Store] a [!DNL Microsoft Edge].

1. Busque y vaya a la extensión de explorador _[!DNL Adobe Experience Cloud Visual Editing Helper]_.

   ![Extensión del ayudante de edición visual de Adobe Experience Cloud para Google Chrome](./assets/web-experience-google-chrome-adobe-visual-editing-extension.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Agregar a Chrome]** y, a continuación, haga clic en **[!UICONTROL Agregar extensión]** en el cuadro de diálogo de confirmación.

   Si está usando [!DNL Microsoft Edge], esta acción agrega la extensión a [!DNL Edge].

1. Asegúrese de que la extensión del explorador [!DNL Visual Editing Helper] esté habilitada correctamente en la barra de herramientas del explorador.

   ![Icono de la extensión Ayuda de edición visual de Adobe Experience Cloud en la barra de herramientas de Google Chrome](./assets/web-experience-google-chrome-adobe-visual-editing-extension-icon.png){width="450"}

Ahora, [!DNL Adobe Experience Cloud Visual Editing Helper] se habilita automáticamente al abrir un sitio web en el editor visual de Journey Optimizer B2B edition para experiencias web. La extensión no tiene ninguna configuración condicional y administra todas las configuraciones automáticamente, incluida la configuración de cookies de SameSite.

>[!NOTE]
>
>Es posible que algunos sitios web no se abran de forma fiable en el editor web B2B edition de Journey Optimizer por uno de los siguientes motivos:
>
>* El sitio web tiene estrictas políticas de seguridad.
>* El sitio web se encuentra en un iframe.
>* El control de calidad del cliente o el sitio de fase no están disponibles externamente (el sitio es interno).

## Crear una experiencia web

Puede configurar experiencias web en un recorrido al [agregar un nodo _[!UICONTROL Realizar una acción]_](../journeys/action-nodes.md) y hacer lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.

1. Para la _[!UICONTROL acción sobre personas]_, elige **[!UICONTROL Personalizar experiencia web]**.

   ![Realizar una acción: personalizar la experiencia web](./assets/web-experience-add-journey-node.png){width="500"}

1. Haga clic en **[!UICONTROL Crear experiencia web]**.

1. En el cuadro de diálogo _[!UICONTROL Crear experiencia web]_, escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** útiles (opcionales).

   * Nombre: máximo de 100 caracteres, debe ser único, sin distinción de mayúsculas y minúsculas

   * Descripción: máximo de 300 caracteres

   >[!NOTE]
   >
   >Los campos de nombre y descripción admiten caracteres alfanuméricos y especiales. Los caracteres reservados (`\ / : * ? " < > |`) son **_no permitidos_**.

   ![Crear diálogo de experiencia web](./assets/web-experience-create-dialog.png){width="400"}

<!-- What is this for? 1. Properties? -->

1. En la ficha **[!UICONTROL Propiedades]**, escriba la descripción de la experiencia web.

1. Haga clic en la ficha **[!UICONTROL Acciones]** y seleccione el **[!UICONTROL canal Web]** que desea utilizar para la experiencia Web.

   La configuración del canal web determina dónde se aplican las modificaciones de contenido en función de las reglas de coincidencia de página configuradas. Consulte [configuraciones de canal web](../admin/configure-channels-web.md) para obtener más información.

   ![Configuración seleccionada del canal web](./assets/web-experience-journey-node-actions-tab.png){width="700" zoomable="yes"}

1. Para definir las modificaciones web, haga clic en **[!UICONTROL Editar contenido]**.

   El editor se abre en la pestaña _[!UICONTROL Contenido]_, donde puede definir las modificaciones para la experiencia web. Consulte [Diseño de experiencia web](./web-experience-design.md) para obtener información detallada sobre cómo usar las herramientas de diseño para agregar las modificaciones al contenido de la experiencia web.

1. En el panel derecho, defina las propiedades de la experiencia web según cómo desee definirla y administrarla.

   * **[!UICONTROL Editor visual]**: cambie entre el [editor visual y el no visual](./web-experience-design.md#web-design-tools) para el diseño de modificación de experiencia web.
   * **[!UICONTROL Redirección de visitantes]**: habilita esta opción para [redirigir a los visitantes a otra URL existente](#redirect-to-url) en lugar de crear una nueva variación en la pestaña de contenido.

   ![Alternar propiedades para el editor visual y redirigir URL](./assets/web-experience-journey-node-content-properties.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar página web]** para [diseñar las modificaciones web](./web-experience-design.md).

1. Cuando haya completado las modificaciones, haga clic en la flecha izquierda encima del editor para volver a la pestaña de contenido y a las propiedades del nodo de experiencia web personalizado.

   Puede hacer clic en la flecha izquierda situada en la parte superior para volver al lienzo de recorrido.

## Editar una experiencia web

1. Abra el recorrido y seleccione el nodo de acción **[!UICONTROL Personalizar experiencia web]**.

1. Para realizar cambios en la configuración o el contenido del canal web, haz clic en **[!UICONTROL Editar experiencia web]**.

1. Seleccione la ficha **[!UICONTROL Acciones]** y cambie la configuración web según sea necesario.

1. Seleccione la ficha **[!UICONTROL Contenido]** y use las herramientas de diseño visual según sea necesario.

   * _Editor visual_ - Haga clic en **[!UICONTROL Editar contenido]**.
   * _Editor no visual_ - Haga clic en **[!UICONTROL Agregar una modificación]**.

   Consulte [Diseño de experiencia web](./web-experience-design.md) para obtener información detallada.

1. Cuando haya completado las definiciones de modificación, haga clic en la flecha izquierda encima del editor para volver a la pestaña de contenido y a las propiedades de la experiencia web.

   Puede hacer clic en la flecha izquierda situada en la parte superior para volver al lienzo de recorrido.

## Redirigir a URL

Al crear una experiencia web, puede redirigir a los visitantes a otra URL existente en lugar de crear una nueva variación en el editor de contenido. Esta opción es útil cuando desea ejecutar un experimento de contenido comparando dos experiencias diferentes en lugar de solo cambiar algunos elementos dentro de una página.

Por ejemplo, cree una campaña web con dos tratamientos:

En Tratamiento A, cree una experiencia web con el editor de contenido para la mitad de la población objetivo.

En Tratamiento B, seleccione la opción _[!UICONTROL Redirigir a URL]_ para la otra mitad de la población de destino. Introduzca la dirección URL de una página con un diseño alternativo que haya creado fuera de Journey Optimizer B2B edition.

![Establezca la redirección de visitantes para redirigir a los visitantes a una dirección URL específica](./assets/web-experience-journey-node-content-visitor-redirection.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Con esta opción seleccionada, la vista previa del sitio web no se muestra y la opción _[!UICONTROL Editor visual]_ está deshabilitada.

Cuando la campaña web esté activa, puede realizar un seguimiento del rendimiento de la experiencia web definida en Journey Optimizer B2B edition frente a las experiencias web que utilizaron una redirección a la página alternativa.

## Prueba de la experiencia web

Una vez completado el diseño de contenido para la experiencia web, puede usar la función _Simular contenido_ para obtener una vista previa de las modificaciones en la página web. Si ha insertado contenido personalizado, puede utilizar datos de perfil de prueba para comprobar cómo se procesa el contenido. Las herramientas de simulación están disponibles en la ficha _[!UICONTROL Contenido]_ para la experiencia web o en el editor de diseño visual de contenido.

1. Haga clic en **[!UICONTROL Simular contenido]** en la parte superior derecha.

1. Seleccione un perfil de prueba.

1. Agregue un perfil de prueba para comprobar la página web mediante los datos del perfil de prueba.

<!-- This works differently than emails (rely on Marketo data), currently. Will expand when we figure it out -->

## Activación de la experiencia web

La experiencia web se activa y se hace visible para la audiencia al [publicar el recorrido](../journeys/create-publish-journey.md#publish-a-journey). Antes de activar una experiencia web a través de un recorrido, tenga en cuenta lo siguiente:

* Si publica un recorrido con una experiencia web que afecta a las mismas páginas que otro recorrido que ya está activo, todos los cambios se aplican a las páginas web.

* Si varios recorridos actualizan los mismos elementos del sitio web, el cambio aplicado más recientemente tiene prioridad.

### Requisitos de envío

Para habilitar la entrega de experiencias web, se debe definir la siguiente configuración:

* En la recopilación de datos de Adobe Experience Platform, asegúrese de que tiene un conjunto de datos definido con la opción Adobe Journey Optimizer B2B edition activada en el servicio Adobe Experience Platform.

  Esta configuración garantiza que Adobe Experience Platform Edge pueda gestionar correctamente los eventos entrantes. [Más información](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)

* En Adobe Experience Platform, asegúrese de tener una política de combinación con la opción _[!UICONTROL Política de combinación activa en Edge]_ habilitada.

  Seleccione una política en el menú Experience Platform Cliente > Perfiles > Políticas de combinación. [Más información](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide#configure)

  Los canales entrantes de Journey Optimizer B2B edition utilizan esta política de combinación para activar y publicar correctamente las experiencias web entrantes en Edge. [Más información](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide)

### Resolución de problemas

Puede utilizar la vista de Edge Delivery en Adobe Experience Platform Assurance para solucionar problemas del envío de experiencias web de Journey Optimizer B2B edition. Este complemento le permite inspeccionar las llamadas de solicitud en detalle, comprobar las llamadas perimetrales esperadas y examinar los datos de perfil. Estos datos de perfil incluyen mapas de identidad, suscripciones a segmentos y configuración de consentimiento. También puede revisar las actividades calificadas y no calificadas para la solicitud.

Para obtener más información sobre la vista Edge Delivery en Assurance, consulte la [documentación de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/view/edge-delivery).
