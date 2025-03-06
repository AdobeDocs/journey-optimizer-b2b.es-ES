---
title: Creación de fragmentos
description: Aprenda a crear fragmentos de contenido que se puedan reutilizar para sus correos electrónicos y diseños de plantilla para lograr una mayor eficacia y mantener los estándares de diseño y marca.
feature: Content
source-git-commit: 1f551b636ef347fd65aa39a809dedba8372c3ac4
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 14%

---

# Creación de fragmentos

Después de [crear un fragmento](./fragments.md#create-fragments), use el editor visual para crear los componentes estructurales y de contenido en el fragmento.

## Añadir estructura y contenido {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño del fragmento. Arrastre y suelte un componente **Estructura** en el lienzo para empezar a diseñar el contenido del fragmento."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de un fragmento."

{{$include /help/_includes/content-design-components.md}}

## Añadir recursos

{{$include /help/_includes/content-design-assets.md}}

## Desplazamiento por las capas, la configuración y los estilos

{{$include /help/_includes/content-design-navigation.md}}

## Personalizar contenido

{{$include /help/_includes/content-design-personalization.md}}

## Habilitar campos personalizados

Cuando un autor de correo electrónico o de plantillas de correo electrónico agrega el fragmento, su contenido se bloquea de forma predeterminada. Cualquier cambio en el fragmento publicado se propaga automáticamente a todos los recursos de contenido donde se utiliza el fragmento. Al designar un parámetro para un componente del fragmento como editable, el autor del correo electrónico o la plantilla puede especificar un valor de campo personalizado que sea específico para sus necesidades. Este indicador de personalización se limita a los componentes visuales de imagen, texto y botones.

Por ejemplo, si diseña un banner reutilizable que incluya un botón en el que se puede hacer clic, puede designar el parámetro de URL del botón como editable. Los autores de correo electrónico pueden utilizar una dirección URL más específica para su campaña de correo electrónico. Con estos campos personalizables, los especialistas en marketing pueden administrar y personalizar el contenido sin necesidad de crear bloques de contenido completamente nuevos o interrumpir las actualizaciones heredadas del fragmento original.

1. En el editor de contenido visual, seleccione la imagen, el texto o el elemento de botón donde desee habilitar la personalización.

1. En los detalles del componente a la derecha, seleccione la pestaña **[!UICONTROL Campos editables]**.

1. Haga clic en la opción **[!UICONTROL Habilitar edición]** y establezca los campos editables.

   ![Habilitar campos editables para un componente de imagen de fragmento](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   Puede habilitar la personalización para los campos mostrados, que dependen del tipo de componente y de los parámetros definidos en el fragmento.

   Cambie el conmutador a un estado habilitado para cada campo donde desee permitir la personalización.

1. Haga clic en **[!UICONTROL Información general]** para revisar todos los campos editables y sus valores predeterminados.

   ![Revise los campos editables y sus valores predeterminados](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. Guarde los cambios.

## Editar seguimiento de URL vinculadas

{{$include /help/_includes/content-design-links.md}}
