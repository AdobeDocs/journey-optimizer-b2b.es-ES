---
title: Gobernanza de contenido de plantilla
description: Aprenda a bloquear los elementos de contenido en las plantillas de correo electrónico para que pueda controlar cómo se pueden modificar para usarlos en los recorridos de cuenta.
feature: Templates, Email Authoring, Content
role: User
exl-id: 0cf852cd-491c-4478-8d5e-51fd2cc2625a
source-git-commit: 4905346d8160147f7d71b7b1131ea33f26d3bba0
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# Gobernanza de contenido de plantilla

Dentro de muchas organizaciones de marketing, hay profesionales de contenido que diseñan campañas de correo electrónico. Un diseño determinado se puede utilizar como base para recorridos de cuentas personalizadas en toda la organización. Para garantizar el cumplimiento de los diseños de contenido aprobados, puede utilizar las funciones de control de contenido para bloquear los componentes de plantilla. Con el bloqueo de contenido activado en la plantilla de correo electrónico, los especialistas en marketing solo pueden modificar los elementos permitidos para mantenerlo alineado con la estrategia de contenido.

Por ejemplo, puede bloquear el encabezado y el pie de página diseñados para la continuidad de las comunicaciones de marca. También puede bloquear la columna que contiene la sección del cuerpo principal, pero permitir que los autores modifiquen el texto para que cumpla su propósito dentro del diseño del recorrido de cuentas.

## Activar el control de contenido para la plantilla

Después de usar el diseñador visual para [crear los componentes estructurales y de contenido](./email-template-authoring.md) para la plantilla de correo electrónico, habilite el control y aplique un bloqueo de contenido específico según sea necesario.

1. En el diseñador visual, obtenga acceso a las capas, contenedores y elementos mediante el _árbol de navegación_.

   Haga clic en el icono _Árbol de navegación_ ( ![Icono de vínculo](../assets/do-not-localize/icon-navigation-tree.svg) ) a la izquierda del lienzo para mostrar el árbol.

1. En el árbol, seleccione el componente raíz **[!UICONTROL Cuerpo]**.

   El panel de propiedades situado a la derecha del lienzo muestra la ficha _[!UICONTROL Configuración]_ de forma predeterminada.

1. Habilite la opción **[!UICONTROL Gobernanza]**.

   ![Habilitar el control para una plantilla de correo electrónico](./assets/governance-template-enable.png){width="800" zoomable="yes"}

   Con esta opción habilitada, el _[!UICONTROL modo]_ predeterminado es **[!UICONTROL de solo lectura]**. Con este modo establecido en el nivel raíz, todos los elementos de la plantilla se bloquean. La estructura de árbol de la izquierda muestra el icono _Solo lectura_ ( ![Icono de solo lectura](../assets/do-not-localize/icon-tree-lock.svg) ) junto a la raíz y todos los elementos secundarios.

1. Para habilitar el bloqueo de contenido específico en la plantilla, cambie **[!UICONTROL Modo]** a **[!UICONTROL Bloqueo de contenido]**.

   Con este modo establecido en el nivel raíz, todos los elementos de la plantilla se desbloquean. La estructura de árbol de la izquierda muestra el icono _Bloqueo de contenido_ ( ![Icono de bloqueo de contenido](../assets/do-not-localize/icon-tree-content-lock.svg) ) junto al elemento raíz. Aplique el bloqueo de contenido a los componentes de contenido (estructurales) e individuales según sea necesario.

   Para permitir que los autores de correo electrónico de recorrido agreguen elementos estructurales o de contenido, active **[!UICONTROL Habilitar la adición de contenido]**. Elija el tipo de adiciones que desea permitir:

   * **[!UICONTROL Permitir adición de estructura y contenido]** - Elija esta opción si desea permitir que los autores agreguen elementos estructurales y de contenido.

   * **[!UICONTROL Permitir solo la adición de contenido]** - Elija esta opción si desea permitir que los autores agreguen solo elementos de contenido.

   ![Habilitar adiciones de contenido](./assets/governance-template-content-additions.png){width="600" zoomable="yes"}

   Con este modo establecido en el nivel raíz, todos los elementos de la plantilla se bloquean. La estructura de árbol de la izquierda muestra el icono _Solo lectura_ ( ![Icono de solo lectura](../assets/do-not-localize/icon-tree-lock.svg) ) junto a la raíz y todos los elementos secundarios.
<!-- 

   
- ![Link icon](../assets/do-not-localize/icon-navigation-tree.svg)
- ![Read only icon](../assets/do-not-localize/icon-tree-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-content-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-edit-text.svg)
- ![Edit element](../assets/do-not-localize/icon-edit.svg) -->

## Aplicar bloqueo a una estructura

Con el modelo de herencia estructural, planifique el diseño y la estructura de la plantilla de correo electrónico según el control que desee aplicar. Utilice los componentes estructurales como contenedores para agrupar los elementos de manera que sean fáciles de designar como bloqueados o editables. Cuando el diseño de la plantilla de correo electrónico esté listo, revise la estructura y aplique las funciones de bloqueo según su plan.

La aplicación de un tipo de bloqueo en el nivel de estructura proporciona una configuración predeterminada para sus componentes secundarios. A continuación, puede aplicar una configuración de bloqueo específica en el nivel de columna o elemento de contenido según sea necesario.

1. Haga clic en el icono _Árbol de navegación_ ( ![Icono de vínculo](../assets/do-not-localize/icon-navigation-tree.svg) ) a la izquierda del lienzo para mostrar el árbol.

1. Seleccione la estructura en el árbol.

   El panel de propiedades situado a la derecha del lienzo muestra la ficha _[!UICONTROL Configuración]_ de forma predeterminada.

1. Establecer el **[!UICONTROL tipo de bloqueo]**:

   * **[!UICONTROL Bloqueado]**: con esta configuración, todos los componentes secundarios están bloqueados de forma predeterminada. La estructura de árbol de la izquierda muestra el icono _Solo lectura_ ( ![Icono de solo lectura](../assets/do-not-localize/icon-tree-lock.svg) ) junto a todos los componentes secundarios.

   * **[!UICONTROL Editable]**: con esta configuración, todos los componentes secundarios se pueden editar de forma predeterminada. La estructura de árbol de la izquierda no muestra iconos junto a los componentes secundarios.

   ![Aplicar bloqueo de contenido a un componente estructural](./assets/governance-template-structure-locking.png){width="800" zoomable="yes"}

## Establecer el bloqueo de un componente secundario

1. Seleccione el componente en el árbol.

   El panel de propiedades situado a la derecha del lienzo muestra la ficha _[!UICONTROL Configuración]_ de forma predeterminada.

1. Habilitar la opción **[!UICONTROL Usar bloqueo específico]**.

1. Elija el tipo de gobernanza que desea aplicar:

   * **[!UICONTROL Editable]**: permite el control editorial completo del componente durante la creación de correo electrónico.
   * **[!UICONTROL Solo contenido editable]**: permite a los autores de correo electrónico cambiar el contenido, pero no el componente en sí.
   * **[!UICONTROL Bloqueado]**: evita cualquier cambio en el componente durante la creación de correo electrónico.

     Para un componente bloqueado, puede permitir la eliminación del componente durante la creación del correo electrónico activando la opción **[!UICONTROL Permitir eliminación]**.

   ![Aplicar bloqueo de contenido a un componente secundario](./assets/governance-template-component-locking.png){width="800" zoomable="yes"}
