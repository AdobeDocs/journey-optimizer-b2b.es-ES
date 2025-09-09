---
title: Creación de plantilla de correo electrónico
description: Cree plantillas de correo electrónico reutilizables con herramientas de diseño visual, CSS personalizada, fragmentos y personalización para recorridos de cuenta en Journey Optimizer B2B edition.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 3%

---

# Creación de plantilla de correo electrónico

Después de [crear una plantilla de correo electrónico](./email-templates.md#create-an-email-template), use el espacio de diseño visual para crear los componentes estructurales y de contenido en la plantilla de correo electrónico.

## Añadir estructura y contenido {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Añadir CSS personalizado

Puede agregar su propio CSS personalizado directamente en el espacio de diseño de la plantilla de correo electrónico. Utilice CSS personalizado para aplicar un estilo avanzado y específico, para una mayor flexibilidad y control sobre el aspecto del contenido. Se recomienda añadir este estilo de nivel superior antes de incluir componentes como imágenes, botones y texto.

Con al menos un componente de contenido en el lienzo, selecciona el componente **[!UICONTROL Cuerpo]** en el árbol de navegación izquierdo para acceder al editor CSS personalizado.

![Acceder a los estilos del cuerpo](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Añadir fragmentos

>[!NOTE]
>
>Los fragmentos no son compatibles entre el _modo de tema_ y el _modo manual_ del contenido del correo electrónico. Para utilizar un fragmento en el contenido del correo electrónico donde se aplique un tema, el fragmento también debe crearse en _Modo de tema_.

{{$include /help/_includes/content-design-use-fragments.md}}

Una vez guardada la plantilla, aparece en la página de detalles del fragmento al seleccionar la pestaña _[!UICONTROL Utilizado por]_ en el resumen.

### Añadir recursos

{{$include /help/_includes/content-design-assets.md}}

### Desplazamiento por las capas, la configuración y los estilos

{{$include /help/_includes/content-design-navigation.md}}

### Personalización del contenido

{{$include /help/_includes/content-design-personalization-email.md}}

### Editar seguimiento de URL vinculadas

{{$include /help/_includes/content-design-links.md}}

## Ver opciones

Aproveche las opciones de vista y validación de contenido disponibles en el espacio de diseño visual.

* Acercar/alejar el contenido en las opciones de zoom preestablecidas.

* Cambie la visualización del contenido en Escritorio, Móvil o Solo texto/Texto sin formato.
   * Haz clic en el icono _Ojo_ para obtener una vista previa del contenido en varios dispositivos.
   * Seleccione uno de los dispositivos predeterminados o introduzca dimensiones personalizadas para obtener una vista previa del contenido.

### Más opciones

En el menú _[!UICONTROL Más...]_ de la parte superior del espacio de diseño del correo electrónico, puede realizar las siguientes acciones:

![Haga clic en Más para acceder a las acciones de plantilla](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Restablecer plantilla]**: haga clic en esta opción para borrar el lienzo de diseño en una pizarra en blanco y reiniciar la creación de contenido.
* **[!UICONTROL Guardar como fragmento]**: guarde toda la plantilla o partes de ella como un fragmento para reutilizarlo en varios correos electrónicos o plantillas de correo electrónico. Proporcione un nombre y una descripción para el fragmento y guárdelo en la lista de fragmentos disponibles.
* **[!UICONTROL Cambia tu diseño]** - Vuelve a la página _Diseña tu correo electrónico_. Desde allí, puede elegir otra plantilla para reiniciar el proceso de diseño. También puede diseñar el contenido desde cero con un lienzo en blanco (_Modo clásico_) o con un [tema de marca](./brand-themes.md) (_Modo de tema_).
* **[!UICONTROL Exportar HTML]**: descargue el contenido del lienzo visual en su sistema local en formato HTML empaquetado como archivo zip.
