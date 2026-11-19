---
title: Módulos de contenido
description: Aprenda a añadir y personalizar módulos para correos electrónicos, páginas de aterrizaje, fragmentos visuales y plantillas. Utilice diseños preparados para crear diseños de contenido coherentes.
feature: Content Design Tools
role: User
autotag-review: '2026-11-18T23:28:40.828Z'
TQID: https://experienceleague.adobe.com/XvVb6-slJV1UyOdfC2CRqYY8V0VzzRLFG-G8m0jYz2I
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: d61088ff-4bd9-5d5c-a987-455c8e1943f8
    internal-label: Content Design Tools
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d105cc868fa0555a60013e358569a7ec556e9426
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 1%
---
# Módulos de contenido

Use módulos en [!DNL Adobe Journey Optimizer B2B Edition] para ensamblar contenido de diseños preparados. Cada módulo combina [estructura](./structure-components.md) y [componentes de contenido](./content-components.md) con contenido predeterminado que reemplaza por su propio texto, imágenes y vínculos.

A diferencia de los componentes de contenido individuales, los módulos proporcionan secciones completas como encabezados, banners, tarjetas y pies de página. Agregue un módulo al lienzo y, a continuación, personalice sus componentes en lugar de crear cada sección a partir de un espacio vacío.

Los módulos son diferentes de [fragmentos visuales](./fragments.md). Un módulo forma parte del contenido que está diseñando. Un fragmento visual es un recurso de contenido guardado que puede reutilizar en correos electrónicos y plantillas de correo electrónico.

## Pestaña Módulos

Use la ficha **[!UICONTROL Módulos]** en el espacio de diseño visual para cualquiera de los siguientes tipos de contenido:

* Correo electrónico: consulte [_Creación de contenido de correo electrónico_](./email-authoring.md).
* Página de aterrizaje: consulte [_Diseño de página de aterrizaje_](./landing-page-design.md).
* Fragmento visual: consulte [_Creación de fragmentos_](./fragment-authoring.md).
* Plantilla de correo electrónico: consulte [_Creación de plantillas de correo electrónico_](./email-template-authoring.md).
* Plantilla de página de aterrizaje: consulte [_Diseño de plantilla de página de aterrizaje_](./landing-page-template-design.md).

![Categorías de módulos mostradas junto al lienzo de diseño visual](./assets/modules-left-panel.png){width="600" zoomable="yes"}

## Categorías de módulo

Expanda una categoría para elegir un diseño. Estos diseños proporcionan diferentes disposiciones para el contenido de la sección, como una, dos o tres columnas.

| Categoría | Utilice |
| --- | --- |
| [!UICONTROL Encabezados] | Introduzca su contenido con un logotipo, vínculos de navegación y texto introductorio. |
| [!UICONTROL Héroe] | Resalte un anuncio o una promoción con una sección de banner. |
| [!UICONTROL Testimonio] | Presente las comillas del cliente en una sección con estilo. |
| [!UICONTROL Tarjetas] | Organizar productos, artículos u otros elementos de contenido en una cuadrícula. |
| [!UICONTROL Equipos] | Presente a los integrantes del equipo, autores o oradores con fotos, nombres y funciones. |
| [!UICONTROL Pies de página] | Finalice el contenido con vínculos de navegación, vínculos sociales y texto legal. |

## Añadir y personalizar módulos

Comience con un módulo que coincida con la sección que desea crear y, a continuación, adapte su contenido y estilo. Reemplace los vínculos y el texto predeterminados por el contenido apropiado para su canal.

>[!NOTE]
>
>Para los correos electrónicos de marketing, incluya un vínculo de no participación y [compruebe las alertas por correo electrónico](./add-email.md#check-alerts) antes de publicar el recorrido.

1. Abra el correo electrónico, la página de aterrizaje, el fragmento visual o la plantilla en el espacio de diseño visual.

   La ficha **[!UICONTROL Módulos]** se muestra de forma predeterminada.

1. Para revisar los diseños disponibles, expanda una categoría.

   También puede utilizar el campo de búsqueda para buscar un módulo por su nombre.

1. Arrastre un módulo al lienzo.

   ![La lista de módulos se filtra mediante la búsqueda y se arrastra un módulo al lienzo.](./assets/modules-search-drag.png){width="600" zoomable="yes"}

1. Revise los elementos dentro del módulo.

   Cada módulo incluye contenido predeterminado que puede editar. Haga clic en el icono _Árbol de navegación_ ( ![Icono del árbol de navegación](../assets/do-not-localize/icon-navigation-tree.svg) ) a la izquierda del lienzo para mostrar la estructura y los elementos en el módulo.

   ![El árbol de navegación muestra la estructura y los elementos del módulo seleccionado.](./assets/modules-navigation-tree.png){width="600" zoomable="yes"}

1. Seleccione un elemento en el módulo para personalizarlo.

   Puede reemplazar el texto predeterminado, elegir imágenes de los recursos y actualizar los vínculos del contenido.

   Use las fichas **[!UICONTROL Configuración]** y **[!UICONTROL Estilos]** para ajustar el componente seleccionado.

   ![Componente de texto seleccionado en el módulo con las opciones de estilos mostradas](./assets/modules-select-element-styles.png){width="600" zoomable="yes"}

1. Para agregar otro elemento, seleccione la ficha **[!UICONTROL Componentes]** y arrastre un [componente de contenido](./content-components.md) al módulo.

   Si agrega un componente a la estructura del módulo, heredará el estilo del módulo de forma predeterminada. Ajuste sus estilos según sea necesario.

   ![Componente de texto arrastrado a la estructura del módulo con texto de marcador de posición con formato mostrado](./assets/modules-select-element-add-component.png){width="800" zoomable="yes"}

1. Seleccione **[!UICONTROL Guardar]** para guardar los cambios.

>[!NOTE]
>
>Cuando se aplica un tema de marca al contenido del correo electrónico, los módulos heredan sus estilos. Para configurar temas y anular estilos, consulte [Usar un tema para crear contenido de correo electrónico](./brand-themes.md#use-email-theme).

## Reutilización del contenido de módulo personalizado

Para reutilizar un módulo personalizado de un correo electrónico o una plantilla de correo electrónico, [guarde el contenido como un fragmento visual](./fragments.md#save-a-new-fragment-from-email-or-template-content). A continuación, inserte el fragmento en otros correos electrónicos o plantillas de correo electrónico.

Para los módulos agregados al crear un fragmento visual, guarde y [publique el fragmento](./fragments.md#create-fragments). Esto lo hace disponible para su reutilización.
