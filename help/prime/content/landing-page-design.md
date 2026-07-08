---
title: Diseño de página de aterrizaje
description: 'Diseñe páginas de aterrizaje con herramientas visuales: añada componentes de contenido, formularios, CSS personalizado, personalización y previsualización de dispositivos para recorridos de persona en Journey Optimizer B2B Prime.'
badgeBeta: label="Beta" type="informative" tooltip="Esta función forma parte de una versión beta limitada."
feature: Landing Pages, Content Design Tools
role: User
autotag-review: '2026-07-08T20:36:05.221Z'
TQID: 'https://experienceleague.adobe.com/M8OA0CPihuuX5h9J-ZrGJOPHkHLwatX5VhBa8co4r4Y'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: a96755d6-1f54-4f3f-a971-d31f83705ab7
  - id: e7bdffdc-2950-4be5-8c23-84240a995090
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 75a4fec07c880f52ac1e8981b5f4416a2f69afe9
workflow-type: tm+mt
source-wordcount: 568
ht-degree: 2%

---

# Diseño de la página de destino

Después de [crear una página de aterrizaje](./landing-pages-create-publish.md#create-landing-page), use el espacio de diseño visual para crear los componentes estructurales y de contenido en su página.

## Añadir estructura y contenido {#structure-content-landing-page}

{{$include /help/_includes/content-design-components-prime.md}}

### Añadir CSS personalizado {#add-custom-css}

Puede agregar su propio CSS personalizado directamente en el espacio de diseño de la página de aterrizaje. Utilice CSS personalizado para aplicar un estilo avanzado y específico, para una mayor flexibilidad y control sobre el aspecto del contenido. Se recomienda añadir este estilo de nivel superior antes de incluir componentes como imágenes, botones y texto.

Con al menos un componente de contenido en el lienzo, selecciona el componente **[!UICONTROL Cuerpo]** en el árbol de navegación izquierdo para acceder al editor CSS personalizado.

![Acceder a los estilos del cuerpo](../../user/content/assets/landing-page-body-styles-css.png){width="800" zoomable="yes"}

Consulte [Agregar CSS personalizado para el contenido](./design-custom-css.md) para ver los pasos, las reglas de sintaxis y la solución de problemas.

### Añadir recursos {#add-assets}

En el espacio de diseño visual, seleccione el icono _Assets_ ( ![Assets icon](../../assets/do-not-localize/icon-assets-me.svg) ) en la barra de navegación izquierda para examinar y seleccionar recursos de imagen de la biblioteca de recursos [!DNL Journey Optimizer B2B Prime].

Para ver los pasos para seleccionar, reemplazar o cargar recursos de imagen, consulte [Usar recursos para la creación de contenido](./digital-asset-management.md#assets-authoring).

### Añadir formularios {#add-forms}

{{$include /help/_includes/content-design-add-forms.md}}

### Desplazamiento por las capas, la configuración y los estilos {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

### Personalización del contenido {#personalize-content}

[!DNL Journey Optimizer B2B Prime] utiliza la sintaxis de Handlebars para la personalización. Los tokens se sustituyen por valores de los datos de perfil de cada visitante cuando se visualiza la página de aterrizaje.

_Para agregar personalización :_

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ ( ![Icono de personalización](../../user/assets/do-not-localize/icon-personalize.svg) ) de la barra de herramientas.
1. En el cuadro de diálogo de personalización, examine el árbol de esquema de la izquierda y seleccione un atributo. El editor inserta la expresión Handlebars correspondiente.
1. Agregue un valor de reserva para gestionar los datos que faltan, si es necesario.
1. Haga clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]**. La expresión aparece en línea en el campo.

Para obtener más información sobre las herramientas y la sintaxis del editor de expresiones, consulte [Editor de Personalization](./personalization-expressions.md).

### Editar seguimiento de URL vinculadas {#linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}

![Haga clic en el icono Editar para acceder al seguimiento de vínculos](../../user/content/assets/landing-page-link-tracking.png){width="400"}

Use **[!UICONTROL Tipo de seguimiento]** para controlar el seguimiento del vínculo:

* **[!UICONTROL Rastreado]**: activa el seguimiento en la dirección URL del vínculo.
* **[!UICONTROL Nunca]**: Nunca activa el seguimiento de la dirección URL del vínculo.

### Guarde el trabajo {#save-your-work}

Haga clic en **[!UICONTROL Guardar]** en cualquier momento para guardar el borrador de la página de aterrizaje.

Puede seguir editando en la página de borrador. Cuando esté listo para mostrar la página y permitir su vinculación en un mensaje de correo electrónico o SMS, puede publicar la página.

### Ver opciones {#view-options}

Aproveche las opciones de vista y validación de contenido disponibles en el espacio de diseño visual.

* Acercar/alejar el contenido en las opciones de zoom preestablecidas.

* Cambie la visualización del contenido en Escritorio, Móvil o Solo texto/Texto sin formato.
   * Haz clic en el icono _Ver_ para obtener una vista previa del contenido entre dispositivos.
   * Seleccione uno de los dispositivos predeterminados o introduzca dimensiones personalizadas para obtener una vista previa del contenido.

### Más opciones {#more-options}

En el menú _[!UICONTROL Más...]_ de la parte superior del espacio de diseño visual, puede realizar las siguientes acciones:

![Haga clic en más para acceder a las acciones de la página de aterrizaje](../../user/content/assets/landing-page-designer-more-menu.png){width="500"}

* **[!UICONTROL Restablecer página de aterrizaje]**: haga clic en esta opción para borrar el lienzo de diseño visual de una pizarra en blanco y reiniciar la creación del contenido de la página.
* **[!UICONTROL Cambia tu diseño]** - Vuelve a la página de inicio de _[!UICONTROL Crear tu página de aterrizaje principal]_. Desde allí, puede elegir otra plantilla para reiniciar el proceso de diseño o elegir diseñar la página desde cero en un lienzo en blanco.
* **[!UICONTROL Exportar HTML]**: descargue el contenido del lienzo visual en su sistema local en formato HTML empaquetado como archivo zip.
