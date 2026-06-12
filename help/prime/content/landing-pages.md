---
title: Páginas de destino
description: 'Cree, diseñe y publique páginas de aterrizaje para recorridos de personas: genere desde cero, importe HTML, añada formularios, personalice contenido y vincule desde correos electrónicos en Journey Optimizer B2B Prime.'
autotag-review: '2026-06-12T22:53:39.337Z'
TQID: 'https://experienceleague.adobe.com/BvtB0i5CzlVutPA6HAzZy-Gfymw7ppZwthyBauyciLc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 1461
ht-degree: 6%

---

# Páginas de aterrizaje

Una página de aterrizaje es una página web independiente en la que puede dirigir a contactos y clientes después de hacer clic en un elemento vinculado en un correo electrónico, un mensaje SMS o cualquier ubicación digital. Puede incorporar estas páginas en los recorridos de su cuenta para que sus clientes potenciales y clientes vean sus mensajes en la web y progresen en los recorridos de su cuenta. Puede crear, personalizar y previsualizar páginas de aterrizaje en el espacio de diseño visual de la página de aterrizaje.

Casos de uso comunes de las páginas de aterrizaje:

* Proporcione comunicaciones de marketing de inclusión o exclusión para un servicio específico. Utilice un vínculo en un correo electrónico u otra comunicación para enviar una lista de destino.
* Recopile el consentimiento antes de enviar comunicaciones y envíe un correo electrónico de confirmación tras la inclusión o la exclusión.
* Capture o actualice datos de perfil (perfil progresivo, preferencias, registros y escenarios similares) mediante formularios en páginas de aterrizaje.
* Dirija a las personas a información específica de la campaña diseñada para su orquestación de recorrido.
* Redirija a las personas a un formulario web específico sin crear una página externa fuera de Journey Optimizer B2B Prime.

<!-- 
## Landing page workflow

To direct members of a journey audience to a defined web page when they click a specific link, create a landing page in Journey Optimizer B2B Edition: 


1. [Create the page](./landing-pages-create-publish.md) - Select a preset, set up the primary page, and add any required subpages.
1. [Design the landing page content](./landing-page-design.md) - Build the page content using drag-and-drop visual design components.
1. [Test and publish the landing page](./landing-pages-create-publish.md) - Preview the page, test form behavior, and then publish to make it live.
1. [Link to the page from your journey](#link-to-a-landing-page) - Add the landing page URL to an email, SMS, or journey action so that recipients can reach it.


For example, you can create and design landing pages to direct your users to online information. The page could include a form where they can opt in or opt out from receiving your communications. Or it could be an opportunity to subscribe to a recurring communications, such as a newsletter. 

You can create, personalize, and preview landing pages in the visual design space.
-->
## Acceso y administración de páginas de aterrizaje

Para acceder a las páginas de aterrizaje de Journey Optimizer B2B Prime, vaya a la navegación izquierda y haga clic en **[!UICONTROL Administración de contenido]** > **[!UICONTROL Páginas de aterrizaje]**. Esta acción muestra una lista de todas las páginas de aterrizaje creadas en la instancia.

La lista se ordena según la columna _[!UICONTROL Modificado]_, con los elementos actualizados más recientemente en la parte superior. Haga clic en el título de la columna para cambiar entre ascendente y descendente.

### Filtrado de la lista de páginas de aterrizaje

Para buscar una página de aterrizaje por nombre, introduzca una cadena de texto en la barra de búsqueda para buscar una coincidencia. Haga clic en el icono _Filtro_ <!-- ( ![Show or hide filters icon](../assets/do-not-localize/icon-filter.svg) ) --> para mostrar las opciones de filtro disponibles y cambiar la configuración para filtrar los elementos mostrados según los criterios especificados.

![Filtrar las páginas de aterrizaje mostradas](./assets/landing-pages-list-filtered.png){width="800" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### Estado de la página de aterrizaje y ciclo vital

El estado de la página de aterrizaje determina su disponibilidad para la vinculación en el contenido del correo electrónico y SMS, y los cambios que puede realizar en él.

| Estado | Descripción |
| -------------------- | ----------- |
| Borrador | Cuando crea una página de aterrizaje, está en estado de borrador. Permanece en este estado a medida que define o edita el contenido visual y hasta que lo publica como una página alojada. Acciones disponibles:<br/><ul><li>Editar nombre o descripción<li>Editar URL del vínculo<li>Editar en el espacio de diseño visual<li>Publicación<li>Duplicado<li>Eliminar |
| Publicadas | Al publicar una página de aterrizaje, esta se aloja en la instancia de Journey Optimizer B2B Prime y está disponible para vincularse en el contenido de un mensaje de correo electrónico o SMS. Acciones disponibles:<br/><ul><li>Editar nombre o descripción<li>Editar URL del vínculo<li>Añadir vínculo en el contenido del correo electrónico o del mensaje SMS<li>Crear versión de borrador<li>Duplicado<li>Eliminar |
| Publicado con borrador | Cuando crea un borrador a partir de una página de aterrizaje publicada, la versión publicada se mantiene y el contenido del borrador se puede modificar en el espacio de diseño visual. Si publica la versión de borrador, reemplazará la versión publicada actual y el contenido se actualizará en la página alojada. Acciones disponibles:<br/><ul><li>Editar nombre o descripción<li>Editar URL del vínculo<li>Añadir vínculo en el contenido del correo electrónico o del mensaje SMS<li>Editar versión de borrador en el espacio de diseño visual<li>Publicar versión de borrador<li>Duplicado<li>Eliminar (elimina ambas versiones)<li>Descartar borrador (vuelve al estado publicado) |

<!-- ![Landing page status lifecycle](./assets/status-lifecycle-diagram.png){zoomable="yes"} -->

## Creación de una página de destino {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="Definir y configurar la página de destino"
>abstract="Para crear una página de destino, debe seleccionar un ajuste preestablecido, configurar la página principal y las subpáginas y, por último, probar la página antes de publicarla."

Por determinar

## Configuración de la página principal {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="Definir la configuración de la página principal"
>abstract="Defina la página principal, que se muestra inmediatamente cuando un destinatario hace clic en el vínculo de la página de aterrizaje, como desde un correo electrónico o un sitio web."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="Definir la dirección URL de la página de destino"
>abstract="En esta sección, defina una dirección URL de página de destino única. La primera parte de la URL requiere que haya configurado previamente un subdominio de página de aterrizaje como parte del ajuste preestablecido que ha seleccionado."

Por determinar

## Prueba de la página de destino {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="Previsualizar y probar la página de destino"
>abstract="Después de definir la configuración y el contenido de la página de aterrizaje, utilice perfiles de prueba para previsualizar la página."

Por determinar

## Edición de una página de aterrizaje

Las ediciones realizadas en una página de aterrizaje dependen de su estado actual:

* Cuando una página de aterrizaje se encuentra en estado **_Borrador_**, puede editar cualquiera de sus detalles, la dirección URL y el contenido visual.
* Cuando una página de aterrizaje se encuentra en estado **_Publicado_**, puede editar la descripción, pero no el nombre. Para cambiar el contenido visual, debe crear una versión de borrador de la página.
* Cuando una página de aterrizaje se encuentra en **_Publicado con el estado Borrador_**, la edición de los detalles se limita a la descripción. También puede editar el contenido visual de la versión de borrador.

>[!BEGINTABS]

>[!TAB Borrador]

1. En la página de listado _[!UICONTROL Páginas de aterrizaje]_, haga clic en el nombre de la página de aterrizaje para abrirla.

   Se muestra una previsualización del contenido visual, con los detalles de la página de aterrizaje a la derecha.

1. Modifique cualquiera de los detalles, como el nombre y la descripción.

   <!-- ![Details for landing page with Draft status](./assets/landing-page-draft-details.png){width="700" zoomable="yes"} -->

1. Para realizar cambios en el contenido en el espacio de diseño visual, haga clic en **[!UICONTROL Editar página de aterrizaje]**.

   <!-- 
   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. Haga clic en **[!UICONTROL Guardar]** o **[!UICONTROL Guardar y cerrar]** para volver a los detalles de la página de aterrizaje.

1. Cuando la página cumpla sus criterios y desee que esté disponible para su visualización, haga clic en **[!UICONTROL Publicar]**.

>[!TAB Publicado]

1. En la página de listado _[!UICONTROL Páginas de aterrizaje]_, haga clic en el nombre de la página para abrirla.

   Se muestra una previsualización del contenido visual, con los detalles de la página de aterrizaje a la derecha.

1. Modifique la descripción, si es necesario.

   No se pueden cambiar todos los demás detalles de una página de aterrizaje publicada.

1. Si desea actualizar el contenido, haga clic en **[!UICONTROL Editar página de aterrizaje]** a la derecha.

   Haga clic en **[!UICONTROL Crear versión de borrador]** en el cuadro de diálogo para abrir la versión de borrador en el espacio de diseño visual.

   <!-- 
   ![Create draft version dialog](./assets/landing-page-create-draft-version.png){width="300"} 

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)
   -->

1. Haga clic en **[!UICONTROL Guardar]** o **[!UICONTROL Guardar y cerrar]** para volver a los detalles de la página de aterrizaje.

1. Si el borrador de la página de aterrizaje cumple los criterios y desea que los cambios estén disponibles en la página publicada, haga clic en **[!UICONTROL Publicar]**.

   Cuando publica la versión de borrador, reemplaza la versión publicada actual y el contenido se actualiza para la dirección URL de la página.

>[!TAB Publicado con borrador]

Al abrir la página de aterrizaje, se muestra la versión en borrador. Las pestañas de la parte superior del espacio de vista previa permiten alternar la visualización entre las versiones publicadas y las de borrador. Las acciones de borrador y los detalles se muestran a la derecha.

<!-- ![Preview and details for the landing page draft version](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"} -->

Para actualizar el contenido:

1. Haga clic en **[!UICONTROL Editar página de aterrizaje]** en la parte superior derecha.

   <!--

   Use the visual design tools as needed:

   * [Add structure and content](./landing-page-design.md#structure-content-landing-page)
   * [Add Assets](./landing-page-design.md#add-assets)
   * [Navigate the layers, settings, and styles](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [Personalize content](./landing-page-design.md#personalize-content)
   * [Edit linked URL tracking](./landing-page-design.md#edit-linked-url-tracking)

   -->

1. Haga clic en **[!UICONTROL Guardar]** o **[!UICONTROL Guardar y cerrar]** para volver a los detalles de la página de aterrizaje.

1. Cuando la página de borrador cumpla sus criterios y desee que los cambios estén disponibles, haga clic en **[!UICONTROL Publicar]**.

   Cuando publica la versión de borrador, reemplaza la versión publicada actual y el contenido se actualiza en la página alojada.

>[!ENDTABS]

## Duplicación de una página de aterrizaje

Puede duplicar una página de aterrizaje mediante cualquiera de los siguientes métodos:

* En la página de listado de _[!UICONTROL Página de aterrizaje]_, haga clic en el icono _Más_ (**...**) junto al nombre de la página de aterrizaje y elija **[!UICONTROL Duplicate]**.
* En la parte superior derecha de la página de aterrizaje, haga clic en **[!UICONTROL ... Más]** y elige **[!UICONTROL Duplicar]**.

<!-- ![Duplicate the landing page](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"} -->

En el cuadro de diálogo, introduzca un nombre útil (único) y una descripción (opcional). Haga clic en **[!UICONTROL Duplicar]** para completar la acción.

<!-- ![Enter a name and description for the duplicated landing page](./assets/landing-page-duplicate-dialog.png){width="350"} -->

La página duplicada (nueva) aparece en el listado de _páginas de aterrizaje_.

## Eliminación de una página de aterrizaje

Puede eliminar una página de aterrizaje mediante cualquiera de los siguientes métodos:

* En la página de listado de _[!UICONTROL Página de aterrizaje]_, haga clic en el icono _Más_ (**...**) junto al nombre de la página de aterrizaje y elija **[!UICONTROL Eliminar]**.
* En la parte superior derecha de la página de aterrizaje, haga clic en **[!UICONTROL ... Más]** y elige **[!UICONTROL Eliminar]**.

Esta acción abre un cuadro de diálogo de confirmación. Puede anular el proceso haciendo clic en **[!UICONTROL Cancelar]** o en **[!UICONTROL Eliminar]** para confirmar la eliminación.

<!-- ![Delete landing page dialog](./assets/landing-page-delete-dialog.png){width="400"} -->

## Vínculo a una página de aterrizaje

Como experto en marketing o creativo que produce contenido de correo electrónico, fragmentos y páginas, puede incrustar vínculos a las páginas de aterrizaje publicadas (activas) que se crean en la instancia de Journey Optimizer B2B Prime.

1. Cuando trabaje en el espacio de diseño visual para un fragmento, correo electrónico, página de aterrizaje o plantilla, seleccione un extracto de texto, un componente de botón o un componente de imagen para el vínculo.

   Las opciones de **[!UICONTROL Link]** se muestran en el panel derecho.

1. Para la opción **[!UICONTROL Type]**, elija **[!UICONTROL Página de aterrizaje]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"} -->

1. Para la opción **[!UICONTROL Página de aterrizaje]**, haga clic en el icono _Seleccionar página_ <!-- ( ![Show links icon](/help/assets/do-not-localize/icon-landing-page-select.svg) ) -->.

1. En el cuadro de diálogo Seleccionar página de aterrizaje, establezca **[!UICONTROL Origen de la página de aterrizaje]** como **[!UICONTROL Journey Optimizer B2B edition]**, seleccione la casilla de verificación de la página de aterrizaje en la lista de páginas publicadas y haga clic en **[!UICONTROL Seleccionar]**.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"} -->

1. Para la opción **[!UICONTROL Target]**, elija el comportamiento de destino del vínculo:

   * **[!UICONTROL Ninguno]**: abre el vínculo con el comportamiento predeterminado del explorador.
   * **[!UICONTROL En blanco]**: abre el vínculo en una nueva ventana o ficha.
   * **[!UICONTROL Self]**: abre el vínculo en el mismo fotograma.
   * **[!UICONTROL Principal]**: abre el vínculo en el marco principal.
   * **[!UICONTROL Superior]**: abre el vínculo en todo el cuerpo de la ventana.

1. (Solo vínculo de texto) Si desea subrayar el texto vinculado, active la casilla de verificación **[!UICONTROL Subrayar vínculo]**.

   Puede establecer un estilo adicional para el texto del vínculo, incluido el color del vínculo, seleccionando la ficha **[!UICONTROL Estilos]** en el panel derecho.
