---
title: Diseño de experiencia web
description: 'Diseñe experiencias web con editores visuales y no visuales: añada modificaciones, administre actualizaciones de contenido, habilite el rastreo de clics y personalice contenido en Journey Optimizer B2B edition.'
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# Diseño de experiencia web

Después de [crear una experiencia web](./web-experiences.md#create-a-web-experience), usa el espacio de diseño de contenido para definir las modificaciones que deseas aplicar a tus páginas web.

>[!BEGINSHADEBOX]

**Requisitos previos**

Antes de diseñar experiencias web, asegúrese de que se cumplen los siguientes requisitos:

* Un administrador de productos ha configurado uno o más canales web para definir las direcciones URL (páginas) que se incluirán en una experiencia web. Para obtener más información, vea [Configuraciones del canal Web](../admin/configure-channels-web.md).

* Su sitio web tiene [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementado para la identificación de visitantes y la entrega de contenido. Se requiere Adobe Experience Platform Web SDK versión 2.16 o superior.

* Tiene los [permisos](../admin/user-management.md#b2b-product-permissions) necesarios para crear y administrar experiencias web en un recorrido:
   * _[!UICONTROL Campañas]_ > _[!UICONTROL Administrar campañas]_: necesario para agregar o actualizar un nodo de acción de personalización web.
   * _[!UICONTROL Campañas]_ > _[!UICONTROL Ver campañas]_ - Necesario para ver detalles de nodos de acción de personalización web.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Antes de diseñar una experiencia web, asegúrese de tener instalada la extensión del explorador Ayuda de edición visual de Adobe Experience Cloud para su explorador web. Esta extensión es necesaria para abrir, crear y obtener una vista previa de las páginas web de forma fiable en el espacio de diseño de la experiencia web de Journey Optimizer B2B edition.<br/>
>
>Google Chrome y Microsoft Edge son actualmente los únicos exploradores que admiten la extensión y la creación de experiencias web en Journey Optimizer B2B edition. Para obtener más información, consulte [Instalar la extensión Ayuda de edición visual](./web-experiences.md#install-the-visual-editing-helper-extension).

## Editores de experiencia web

Journey Optimizer B2B edition proporciona dos tipos de editores para diseñar modificaciones web:

| Editor | Descripción | Mejor para |
| ------ | ----------- | -------- |
| [Editor visual](#visual-editor) | Editor de WYSIWYG (_What You See Is What You Get_) que muestra el sitio web y permite seleccionar y modificar elementos directamente. Requiere la [extensión Ayuda de edición visual](./web-experiences.md#install-the-visual-editing-helper-extension) en el explorador web Google Chrome o Microsoft Edge. | Realizar cambios visuales en elementos de página visibles, como texto, imágenes, botones y banners. |
| [Editor no visual](#non-visual-editor) | Un editor basado en código para aplicar modificaciones que no se pueden realizar mediante el editor visual. | Segmentación de elementos que son difíciles de seleccionar visualmente, aplicación de cambios CSS avanzados o modificación de elementos ocultos. |

En las propiedades de la experiencia web, use la opción **[!UICONTROL Editor visual]** para determinar el tipo de editor. Habilite la opción para utilizar el editor visual o desactívela para utilizar el editor no visual.

![Opción del editor visual habilitada](./assets/web-experience-design-visual-editor-option.png){width="400"}

## Editor visual {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="Uso del modo Examinar"
>abstract="En este modo, puede navegar a la página exacta que desee personalizar para la configuración del canal Web seleccionada."

El editor visual carga las páginas web dentro de un iframe, donde puede seleccionar elementos y aplicar modificaciones directamente en la vista previa de la página. Complete los siguientes pasos para utilizar el editor visual para diseñar la experiencia web:

1. Con la ficha _[!UICONTROL Contenido]_ mostrada en la página de detalles de la experiencia web, haga clic en **[!UICONTROL Editar experiencia web]** en el panel derecho.

   El editor visual carga el sitio web en función de la configuración del canal web.

   ![Editor visual de experiencia web](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. Si es necesario, haz clic en **[!UICONTROL Examinar]** en la parte superior derecha y usa la barra de navegación del sitio para cargar la página específica que deseas modificar.

   También puede introducir la dirección URL de la página en el campo de la parte superior.

   >[!NOTE]
   >
   >Asegúrese de que la página cargada coincida con los patrones de URL definidos en la configuración del canal web. Haga clic en **[!UICONTROL Ver detalles de configuración]** en la parte superior derecha para ver la URL o las reglas de coincidencia de página para la configuración del canal web seleccionado.

   ![Modo de exploración en el editor visual](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   Haga clic en **[!UICONTROL Diseño]** en la parte superior derecha para cargar la página en el espacio de diseño.

1. Para definir cómo desea que se modifique la página mostrada para la experiencia web, puede:

   * [Inserte nuevos componentes](#insert-new-components) (divisor, HTML, imagen, encabezado, párrafo o vínculo) en la página para la experiencia web.

   * Seleccione cualquier elemento existente de la página, como una imagen, un botón, un párrafo, un texto, un contenedor, un encabezado o un vínculo, y [modifíquelo para la experiencia web](#modify-elements).

   * [Agregar rastreo de clics](#click-tracking-for-web-experiences) para que los elementos midan la participación y recopilen información.

1. Repita el paso 2 para cargar otras páginas que desee incluir en la experiencia web y el paso 3 para definir las modificaciones de la página.

1. [Revise sus modificaciones](#manage-modifications) y realice los ajustes necesarios.

1. Cuando haya completado las modificaciones, haga clic en la flecha izquierda encima del editor para volver a las propiedades de la experiencia web.

### Modificar elementos

Haga clic en un elemento de la página mostrada para seleccionarlo. Un borde azul indica el elemento seleccionado y aparece una barra de herramientas contextual con opciones de modificación.

![Seleccione un elemento para modificar](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

Las opciones de la barra de herramientas dependen del tipo de componente seleccionado:

| Acción | Descripción |
| ------ | ----------- |
| **[!UICONTROL Opciones de texto]** | Cambie la clase o el estilo del elemento de texto seleccionado. |
| **[!UICONTROL Elegir imagen]** | Reemplace el origen de la imagen o agregue una imagen al elemento. |
| **[!UICONTROL Editar vínculo / Agregar vínculo]** | Modifique o añada una URL de vínculo. |
| **[!UICONTROL Organizar]** | Mover el elemento seleccionado hacia atrás o hacia adelante dentro de la pantalla. |
| **[!UICONTROL Adición de personalización]** | Inserte personalización. |
| **[!UICONTROL Elemento de rastreo de clics]** | Añada el rastreo de clics para el elemento. |
| **[!UICONTROL Eliminar]** | Quitar el elemento seleccionado de la página. |

Para un elemento seleccionado, las propiedades del panel derecho cambian para reflejar el estilo y las acciones disponibles. Haga clic en un icono de acción en la parte superior del panel para duplicar, rastrear clics, eliminar u ocultar el elemento seleccionado.

![haga clic en un icono de acción para el elemento seleccionado](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++Elementos de texto

1. Seleccione un elemento de texto en la página.

1. Introduzca el nuevo contenido de texto o seleccione una cadena de texto e introduzca el texto de sustitución.

1. (Opcional) Use las [opciones de formato de texto](./content-components.md#text), como negrita, cursiva y alineación.

1. Haga clic fuera del elemento de texto para aplicar el cambio.

Para obtener más información acerca de las opciones de estilo de texto para los componentes de texto, vea [Componentes de contenido](./content-components.md#text).

+++

+++Elementos de imagen

1. Seleccione un elemento de imagen en la página.

1. Haga clic en el icono _[!UICONTROL Elegir imagen]_ en la barra de herramientas contextual o en el panel derecho.

1. Examine y seleccione una imagen de la biblioteca de recursos.

1. Use las [opciones de estilo de imagen](./content-components.md#image) del panel derecho según sea necesario.

+++

+++Elementos Button

1. Seleccione un elemento de botón en la página.

1. (Opcional) Escriba texto nuevo para el botón o seleccione la cadena de texto e introduzca el texto de reemplazo.

   Puede utilizar la personalización para modificar el texto del botón mediante los datos de perfiles de cuenta o persona.

1. Utilice las [opciones de estilo de botón](./content-components.md#button) del panel derecho según sea necesario.

+++

+++ Elementos de contenedor

1. Seleccione un elemento contenedor en la página.

1. Use las [opciones de estilo de contenedor](./content-components.md#container) en el panel derecho según sea necesario.

+++

### Insertar nuevos componentes

Al seleccionar el icono **+** en el diseño de navegación izquierda para el editor visual, puede agregar los siguientes tipos de componentes a la página como una modificación de la experiencia web:

* **[!UICONTROL Divisor]**: utilice este componente para insertar una línea divisoria y organizar el diseño y el contenido del correo electrónico. Puede ajustar atributos de estilo como el color de línea, el estilo y la altura desde las propiedades del panel derecho. Consulte [Divisor](./content-components.md#divider) en _Componentes de contenido_ para obtener más información.
* **[!UICONTROL HTML]**: use este componente para copiar y pegar código HTML en la estructura existente. Permite crear componentes modulares de HTML gratuitos para reutilizar contenido externo. Consulte [HTML](./content-components.md#html) en _Componentes de contenido_ para obtener más información.
* **[!UICONTROL Imagen]**: utilice este componente para insertar un archivo de imagen en la página. Puede ajustar atributos de estilo como la anchura y la altura desde las propiedades del panel derecho. Consulte [Imagen](./content-components.md#image) en _Componentes de contenido_ para obtener más información.
* **[!UICONTROL Encabezado]**: utilice este componente para insertar texto de clase de encabezado. Puede ajustar atributos de estilo como el color, el estilo, la fuente y el tamaño del texto desde las propiedades del panel derecho. Consulte [Texto](./content-components.md#text) en _Componentes de contenido_ para obtener más información.
* **[!UICONTROL Párrafo]**: utilice este componente para insertar un elemento de texto estándar. Puede ajustar atributos de estilo como el color, el estilo, la fuente y el tamaño del texto desde las propiedades del panel derecho. Consulte [Texto](./content-components.md#text) en _Componentes de contenido_ para obtener más información.
* **[!UICONTROL Vínculo]**: utilice este componente para insertar un vínculo de texto independiente en una dirección URL especificada. Puede ajustar atributos de estilo como el color, el estilo, la alineación y el tamaño del texto desde las propiedades del panel derecho.

Seleccione un tipo de componente a la izquierda y, a continuación, pase el ratón sobre un elemento adyacente a donde desee agregarlo.

![Interfaz de editor visual: nuevo componente](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

Haga clic en uno de los botones mostrados para colocar el componente:

* ***[!UICONTROL Insertar antes]**: inserte el componente antes del elemento seleccionado.
* ***[!UICONTROL Insertar después]**: inserte el componente después del elemento seleccionado.

Para anular la selección de un tipo de componente para su inserción, haga clic en **[!UICONTROL ESC]** en el titular azul contextual que se muestra en la parte superior de la página.

## Editor no visual {#non-visual-editor}

Utilice el editor no visual cuando necesite realizar modificaciones que no se puedan realizar fácilmente en el editor visual. Este enfoque basado en código le proporciona un control preciso sobre la segmentación y modificación de elementos. Complete los siguientes pasos para utilizar el editor no visual para diseñar la experiencia web:

1. Con la ficha _[!UICONTROL Contenido]_ mostrada en la página de detalles de la experiencia web, haga clic en **[!UICONTROL Agregar modificación]** en el panel derecho.

   El editor no visual carga una página basada en la configuración del canal web.

   ![Interfaz de editor no visual](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. Defina la primera modificación que desee realizar.

   El panel lateral izquierdo muestra una lista de las modificaciones existentes (si las hay). Haga clic en **[!UICONTROL Agregar]** para definir una nueva modificación. Si no hay modificaciones definidas, el panel toma como valor predeterminado las opciones _[!UICONTROL Agregar modificación]_.

   * Elija **[!UICONTROL tipo de modificación]**:

     | Tipo | Descripción |
     | ---- | ----------- |
     | [**[!UICONTROL Selector de CSS]**](#css-selector-modifications) | Elementos de destino que utilizan una cadena de selector de CSS. |
     | [**[!UICONTROL Página]**](#page-modifications) | Inserte HTML, CSS o JavaScript personalizados en elementos de nivel de página, como `<head>` o `<body>`. |

   * Configure los parámetros de modificación según el tipo:

      * **[!UICONTROL Selector de CSS]**: escriba un selector de CSS válido para dirigirse a elementos específicos.
      * **[!UICONTROL Tipo de acción]**: elija la acción que desea realizar (editar, ocultar, eliminar, insertar, reemplazar).
      * **[!UICONTROL Contenido]**: proporcione el contenido o el estilo que se aplicará.

1. Haga clic en **[!UICONTROL Guardar]** para aplicar la modificación.

### Modificaciones del selector CSS

Las modificaciones del selector de CSS le permiten segmentar elementos con precisión mediante la sintaxis del selector de CSS estándar.

1. Elija **[!UICONTROL Selector de CSS]** como tipo de modificación.

1. Introduzca el selector en el campo **[!UICONTROL Selector de elementos CSS]**.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **Selectores de ejemplo:**
    
    | Selector | Objetivos |
    | -------- | ------- |
    | #hero-banner. | Elemento con ID `hero-banner` |
    | `.cta-button` | Todos los elementos con la clase &quot;cta-button&quot; |
    | `header nav a` | Vínculos dentro de la navegación, dentro del encabezado |
    | &quot;[data-offer=&quot;premium&quot;]&quot; | Elementos con un atributo de datos específico |

1. Elija un **[!UICONTROL Tipo de acción]** y especifique la información o el contenido necesarios.

   * **[!UICONTROL Establecer contenido]** - Escriba el texto en el campo **[!UICONTROL Contenido]** para el elemento identificado por el valor _[!UICONTROL Selector de elementos CSS]_.

   * **[!UICONTROL Establecer atributo]**: especifique un atributo que se asociará con el selector CSS actual para que este atributo pueda identificar el elemento. Escriba un nombre en el campo **[!UICONTROL Nombre de atributo]** y un valor en el campo **[!UICONTROL Contenido]**. Si el atributo ya existe, el valor se actualiza; de lo contrario, se agrega un nuevo atributo con el nombre y valor especificados.

   ![Modificación del selector css del editor no visual](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (Opcional) Haga clic en **[!UICONTROL Agregar personalización]** y use el [editor de personalización](./personalization.md#personalization-editor) para crear una personalización personalizada para el contenido.

### Modificaciones de página

Puede agregar código personalizado utilizando el tipo de modificación Página `<head>`. El elemento `<head>` es un contenedor de metadatos (datos sobre datos) y se coloca entre la etiqueta `<html>` y la etiqueta `<body>`. En este caso, el código no espera eventos body o page-load: se ejecuta al principio de la carga de la página.

El elemento `<head>` se utiliza comúnmente para agregar código JavaScript o CSS al principio de la página. Los selectores para las acciones visuales posteriores dependen de los elementos de HTML agregados en esta pestaña.

>[!NOTE]
>
>El código personalizado se ejecuta en el explorador del visitante. Asegúrese de que el código sea seguro, se haya probado y no afecte negativamente al rendimiento de la página ni a la experiencia del usuario.

1. Elija **[!UICONTROL Página`<head>`]** como tipo de modificación.

1. Agregue su código personalizado en el cuadro **[!UICONTROL Contenido]**.

   >[!CAUTION]
   >
   >Solo puede agregar elementos `<script>` y `<style>` a la sección `<head>`. Si se agregan etiquetas de `<div>` y otros elementos, es posible que `<head>` elementos restantes se rellenen en `<body>`.

   ![Modificación del encabezado de página del editor no visual](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (Opcional) Haga clic en **[!UICONTROL Agregar personalización]** y use el [editor de personalización](./personalization.md#personalization-editor) para crear una personalización personalizada para el contenido.

## Administración de modificaciones {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="Administrar fácilmente todos los cambios"
>abstract="Con este panel, puede navegar y administrar todos los ajustes y adiciones definidos para la página web."

Todas las modificaciones que cree se rastrearán y se podrán administrar desde el panel **[!UICONTROL Modificaciones]** tanto del editor visual como del no visual. Haga clic en el icono _[!UICONTROL Modificaciones]_ <!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) -->de la barra de herramientas izquierda para ver todas las modificaciones.

Cada registro de modificación incluye:

* El elemento o selector de destino
* El tipo de modificación (como editar, ocultar o insertar)
* Una previsualización del cambio

![Panel de modificaciones](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### Edición de una modificación

1. En la lista _[!UICONTROL Modificaciones]_, busque la modificación que desea editar.

1. Haga clic en el icono _Más menú_ ( **...** ) y elija **[!UICONTROL Editar]**.

1. Actualice las propiedades de modificación según sea necesario.

1. Haga clic en **[!UICONTROL Guardar]** para guardar los cambios.

### Eliminación de una modificación

1. En la lista _[!UICONTROL Modificaciones]_, busque la modificación que desea quitar.

1. Haga clic en el icono _Menú más_ ( **...** ) y elija **[!UICONTROL Eliminar modificación]**.

1. Confirme la eliminación cuando se le solicite.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## Previsualización de las modificaciones

Antes de publicar, obtenga una vista previa del aspecto de las modificaciones para los visitantes.

Utilice las opciones de vista previa del dispositivo en la parte superior del editor visual para ver las modificaciones en:

* Escritorio
* Tableta
* Dispositivo móvil

![Cambiar el tamaño del dispositivo para la vista previa](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

La vista previa se actualiza para mostrar cómo se representan las modificaciones en cada tamaño de dispositivo.

Utilice la barra URL para navegar a diferentes páginas dentro de la configuración del canal web. A continuación, compruebe que las modificaciones se aplican correctamente a las páginas de destino según las reglas de coincidencia de URL.

## Rastreo de clics para experiencias web {#web-click-tracking}

Rastree las interacciones del usuario con los elementos para medir la participación y recopilar perspectivas. Los datos de rastreo de clics están disponibles en los informes de participación y se pueden utilizar para medir la eficacia de las modificaciones de la experiencia web.

Cuando se activa la experiencia web (activa), también puede crear informes con Adobe Customer Journey Analytics (que requiere una suscripción al producto). Para mejorar la monitorización de la experiencia web, también puede rastrear los clics en cualquier elemento específico del sitio web. El seguimiento permite mostrar el número de clics de ese elemento en los informes web.

Para obtener más información sobre Customer Journey Analytics y la generación de informes web, consulte la [documentación de Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing).

1. Seleccione un elemento en el editor de experiencia web, como, por ejemplo, una imagen o un vínculo.

1. En las propiedades del elemento o en la barra de herramientas contextual, haga clic en el icono _[!UICONTROL Hacer clic en rastrear elemento]_.

   ![Habilitar el rastreo de clics para los elementos de experiencia web](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. Abra la lista Rastreo de clics en el panel izquierdo y modifique el valor de **[!UICONTROL Acciones rastreadas]** para identificar esta interacción en sus informes.

   ![Establecer la identificación del rastreo de clics para la experiencia web](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
