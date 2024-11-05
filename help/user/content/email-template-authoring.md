---
title: Creación de plantillas de correo electrónico
description: Aprenda a crear plantillas de correo electrónico de contenido que se puedan utilizar para los correos electrónicos de recorrido de cuentas a fin de reutilizar sus diseños de forma fácil y eficaz.
feature: Email Authoring, Content
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 10%

---

# Creación de plantillas de correo electrónico

Después de [crear una plantilla de correo electrónico](./email-templates.md#create-an-email-template), use el diseñador visual para crear los componentes estructurales y de contenido en la plantilla de correo electrónico.

## Añadir estructura y contenido {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Adición de componentes de estructura"
>abstract="Los componentes de estructura definen el diseño de la plantilla. Arrastre y suelte un componente de **Estructura** en el lienzo para empezar a diseñar el contenido de la plantilla."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="Acerca de los componentes de contenido"
>abstract="Los componentes de contenido son marcadores de posición de contenido vacíos que se pueden utilizar para crear el diseño de una plantilla."

{{$include /help/_includes/content-design-components.md}}

### Añadir fragmentos

En el editor de contenido visual, el icono _Fragmentos_ se muestra a la izquierda. En el siguiente ejemplo se describen los pasos para agregar fragmentos al contenido de la plantilla.

1. Para abrir la lista de fragmentos, seleccione el icono _Fragmentos_ ( ![icono Fragmentos](../assets/do-not-localize/icon-fragments.svg) ).

   Puede hacer lo siguiente:

   * Ordenar el listado.
   * Examine, busque o filtre la lista.
   * Cambiar entre las vistas Miniaturas y Lista.
   * Actualice la lista para reflejar cualquiera de los fragmentos creados recientemente.

   ![Seleccionar un fragmento de la lista](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Arrastre y suelte cualquiera de los fragmentos en el marcador de posición del componente estructural.

   El editor procesa el fragmento dentro de la sección o el elemento de la estructura de correo electrónico.

El contenido del fragmento se actualiza dinámicamente dentro de la estructura para mostrar cómo aparece el contenido en el correo electrónico.

>[!TIP]
>
>Si desea que el fragmento ocupe todo el diseño horizontal dentro del correo electrónico, agregue una estructura de columna 1:1 y, a continuación, arrastre y suelte el fragmento en él.

Una vez guardado el correo electrónico, aparecerá en la página de detalles del fragmento al seleccionar la pestaña _[!UICONTROL Utilizado por]_ en el resumen. Los fragmentos agregados a una plantilla de correo electrónico no se pueden editar dentro de la plantilla: el fragmento de origen define el contenido.

### Añadir recursos

{{$include /help/_includes/content-design-assets.md}}

### Desplazamiento por las capas, la configuración y los estilos

{{$include /help/_includes/content-design-navigation.md}}

### Personalizar contenido

{{$include /help/_includes/content-design-personalization.md}}

### Editar seguimiento de URL vinculadas

{{$include /help/_includes/content-design-links.md}}

## Ver opciones

Aproveche las opciones de vista y validación de contenido disponibles en el diseñador visual.

* Acercar/alejar el contenido en las opciones de zoom preestablecidas.

* Cambie la visualización del contenido en Escritorio, Móvil o Solo texto/Texto sin formato.
   * Haz clic en el icono _Ojo_ para obtener una vista previa del contenido en varios dispositivos.
   * Seleccione uno de los dispositivos predeterminados o introduzca dimensiones personalizadas para obtener una vista previa del contenido.

### Más opciones

En el menú _[!UICONTROL Más...]_ de la parte superior del diseñador de correo electrónico, puede realizar las siguientes acciones:

![Haga clic en Más para acceder a las acciones de plantilla](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Restablecer plantilla]** - Haga clic en esta opción para borrar el lienzo del diseñador visual en una pizarra en blanco y reiniciar la creación de contenido.
* **[!UICONTROL Guardar como fragmento]**: guarde toda la plantilla o partes de ella como un fragmento para reutilizarlo en varios correos electrónicos o plantillas de correo electrónico. Proporcione un nombre y una descripción para el fragmento y guárdelo en la lista de fragmentos disponibles.
* **[!UICONTROL Cambia tu diseño]** - Vuelve a la página _Diseña tu plantilla_. A partir de ahí, puede elegir diseñar la plantilla desde cero o utilizar una plantilla existente para reiniciar el proceso de diseño.
* **[!UICONTROL HTML de exportación]**: descargue el contenido del lienzo visual en su sistema local en formato de HTML empaquetado como archivo zip.
