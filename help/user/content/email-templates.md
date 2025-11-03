---
title: Plantillas de correo electrónico
description: 'Cree plantillas de correo electrónico reutilizables desde cero, HTML import o diseños existentes: administre plantillas para recorridos de cuenta en Journey Optimizer B2B edition.'
feature: Templates, Email Authoring, Content
role: User
exl-id: 4e146802-e3ef-4528-b581-191e28afe86f
source-git-commit: d97a05899e4fff784924c3db0aa941232d169944
workflow-type: tm+mt
source-wordcount: '1533'
ht-degree: 0%

---

# Plantillas de correo electrónico

Para un proceso de diseño acelerado y mejorado, puede crear plantillas de correo electrónico independientes para reutilizar el contenido personalizado en [!DNL Adobe Journey Optimizer B2B Edition] recorridos de cuenta. A través de las plantillas, los integrantes del equipo orientados al contenido pueden trabajar en el contenido del correo electrónico fuera de los recorridos. Los estrategas de marketing pueden reutilizar y adaptar estas plantillas independientes dentro de sus recorridos de cuenta. Por ejemplo, un miembro del equipo está a cargo solo del contenido, sin acceso a los recorridos de la cuenta. Sin embargo, pueden crear una plantilla de correo electrónico que los especialistas en marketing pueden seleccionar como punto de partida para las comunicaciones por correo electrónico y personalizarla según los requisitos del recorrido.

## Acceso y administración de plantillas de correo electrónico

Para acceder a las plantillas de correo electrónico en [!DNL Journey Optimizer B2B Edition], vaya a la barra de navegación izquierda y haga clic en **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas]**. En el panel lateral, seleccione **[!UICONTROL Plantillas de correo electrónico]**.

Esta acción abre una página de lista con todas las plantillas de correo electrónico creadas en la instancia en formato de tabla.

La lista está ordenada de forma predeterminada por la columna _[!UICONTROL Modificado]_, con las plantillas actualizadas más recientemente en la parte superior. Haga clic en el título de la columna para cambiar entre ascendente y descendente.

Para buscar una plantilla por nombre, escriba una cadena de texto en la barra de búsqueda. Haga clic en el icono _Filtro_ en la parte superior izquierda para filtrar la lista según las fechas de creación o modificación, y las plantillas que haya creado o modificado.

![Acceda a la biblioteca de plantillas de correo electrónico y filtre por nombre y fechas](./assets/templates-list-search-filter.png){width="800" zoomable="yes"}

Personalice las columnas que desee mostrar en la tabla haciendo clic en el icono _Personalizar tabla_ ( ![Personalizar icono de tabla](../assets/do-not-localize/icon-column-settings.svg) ) en la parte superior derecha. Seleccione las columnas que desea mostrar y haga clic en **[!UICONTROL Aplicar]**.

Desde la lista mostrada de plantillas, puede realizar las acciones descritas en las secciones siguientes.

## Creación de una plantilla de correo electrónico

Puede crear una plantilla de correo electrónico a partir de la página de lista de plantillas de correo electrónico haciendo clic en **[!UICONTROL Crear plantilla]** en la parte superior derecha.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** útiles (opcionales).

   ![Introduzca las propiedades iniciales de la nueva plantilla de correo electrónico](./assets/templates-create-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

Se abre la página _[!UICONTROL Diseña tu plantilla]_ y proporciona varias opciones para crearla: _[!UICONTROL Diseña desde cero]_, _[!UICONTROL Importar HTML]_ o _[!UICONTROL Selecciona una plantilla de diseño]_.

![Elija cómo desea comenzar con el diseño de la plantilla de correo electrónico](./assets/templates-create-design.png){width="800" zoomable="yes"}

Después de seleccionar el método que desea usar para iniciar el diseño de la plantilla de correo electrónico, use el espacio de diseño visual para [crear el contenido de la plantilla de correo electrónico](./email-template-authoring.md).

### Diseñe desde cero

Utilice el editor de contenido visual para definir la estructura del contenido del correo electrónico. Al agregar y mover componentes estructurales con sencillas acciones de arrastrar y soltar, puede diseñar la forma del contenido del correo electrónico reutilizable en cuestión de segundos.

>[!NOTE]
>
>Las herramientas de diseño disponibles equivalen a las herramientas utilizadas para la creación de [correos electrónicos](./email-authoring.md). La diferencia es que este contenido se guarda como una plantilla que se puede reutilizar en varios nodos _enviar correo electrónico_ dentro de los recorridos de la cuenta.

1. En la página de inicio de _[!UICONTROL Diseña tu plantilla]_, selecciona la opción **[!UICONTROL Diseñar desde cero]**.

1. En el cuadro de diálogo _[!UICONTROL Crear correo electrónico]_, elija el tipo de contenido de correo electrónico que desea usar para la plantilla.

   * **[!UICONTROL Usar temas]** - Elija esta opción para crear la plantilla de correo electrónico en _Modo de tema_. En este modo, puede utilizar un tema de marca definido para optimizar el proceso de creación de contenido y asegurarse de que el diseño se ajuste a los estándares definidos.

   ![Crear correo electrónico - Usar temas](./assets/create-email-use-theme.png){width="450"}

   * **[!UICONTROL Estilo manual]**: elija esta opción para crear la plantilla de correo electrónico en _modo manual_. En este modo, se establece manualmente el estilo para todos los componentes de estructura y contenido que se añaden al lienzo en blanco.

1. (_Modo de temas_ solamente) Aplicar un tema.

   En el espacio de diseño del correo electrónico, haga clic en el icono _Temas_ ( ![icono Temas](../assets/do-not-localize/icon-design-themes.svg) ) que hay a la derecha.

   ![Espacio de diseño de correo electrónico - Icono de temas seleccionado](./assets/email-design-themes-icon-selected.png){width="600" zoomable="yes"}

   Se muestra la temática predeterminada o la temática aplicada a la plantilla. Puede cambiar entre las variantes de color de esta temática.

   Haga clic en la flecha situada junto a la temática mostrada para ver la lista de temáticas personalizadas y de Adobe disponibles. Seleccione **[!UICONTROL Mis temas]** para usar un tema personalizado creado para su organización.

   Al hacer clic fuera de la lista, la temática seleccionada aplica los estilos. Puede alternar entre las variantes de color.

1. [Agregar estructura y contenido](./email-authoring.md#add-structure-and-content) a la plantilla.

   Si hay una temática aplicada, los componentes añadidos heredan automáticamente los estilos definidos en la temática.

### Importar HTML

Adobe Journey Optimizer B2B edition le permite importar contenido existente de HTML para diseñar sus plantillas de correo electrónico.

{{$include /help/_includes/content-design-import.md}}

![importar contenido html en un archivo zip](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>El uso de una etiqueta `<table>` como primera capa de un archivo HTML puede causar la pérdida de estilo, incluida la configuración del fondo y el ancho en la etiqueta de la capa superior.

Puede personalizar el contenido importado según sea necesario en el espacio de diseño visual.

### Seleccionar una plantilla de diseño

{{$include /help/_includes/content-design-select-template.md}}

## Ver detalles de plantilla de correo electrónico

En la página de lista Plantillas, haga clic en el nombre de una plantilla de correo electrónico para abrir la página de detalles de la plantilla de correo electrónico. Desde aquí puede ver las propiedades básicas de la plantilla de correo electrónico y acceder al editor de contenido visual para realizar cambios en el contenido de la plantilla.

![Acceda a la biblioteca de plantillas de correo electrónico y filtre por nombre y fechas](./assets/template-details.png){width="700" zoomable="yes"}

* Ver los detalles de la plantilla de correo electrónico, como el nombre y la descripción. Esta configuración se puede editar. Haga clic fuera del cuadro de descripción para guardar los cambios automáticamente.

* Vea las propiedades de la plantilla de correo electrónico, como creada por, creada el, actualizada por última vez el y modificada por.

* Haga clic en **[!UICONTROL Más]** en la parte superior derecha para realizar acciones rápidas en la plantilla de correo electrónico, como _Duplicar_ y _Eliminar_.

* Si hay alertas activas (errores y advertencias para la plantilla de correo electrónico), haga clic en **[!UICONTROL Alertas]** en la parte superior derecha para ver la información.

  Estas alertas no prohíben el uso de la plantilla de correo electrónico para la creación de correos electrónicos. La información proporciona a los especialistas en marketing de su equipo visibilidad sobre lo que podría no funcionar y las actualizaciones necesarias antes de poder utilizarlo para la entrega.

## Ver plantilla de correo electrónico utilizada por referencias

En la página de detalles de las plantillas de correo electrónico, haga clic en la ficha **[!UICONTROL Utilizada por]** para ver los detalles de dónde se utiliza esta plantilla de correo electrónico en los correos electrónicos de los recorridos de la cuenta.

![Haga clic en la ficha Utilizado por para comprobar el uso de la plantilla](./assets/template-details-used-by.png){width="400"}

Los correos electrónicos de Journey Optimizer B2B edition están incrustados y creados en recorrido, por lo que el recorrido principal del correo electrónico que utiliza la plantilla se muestra en las referencias.

* Al hacer clic en el vínculo, se le redirige al correo electrónico de recorrido correspondiente donde se utiliza la plantilla de correo electrónico.

* Salga de la vista en cualquier momento haciendo clic en la flecha Atrás, que le devuelve a la página del listado.

## Editar plantillas de correo electrónico

Esta acción se puede realizar desde:

* La página de detalles: haga clic en **[!UICONTROL Editar plantilla de correo electrónico]**.
* La página del listado: haga clic en los puntos suspensivos (**...**) junto a una plantilla de correo electrónico y elija **[!UICONTROL Editar]**.

Esta acción lo lleva a la página _Diseñar su plantilla_ o a la página del editor de contenido visual (según el último estado guardado de la plantilla de correo electrónico). Desde aquí puede editar el contenido de su plantilla de correo electrónico según sea necesario. Consulte [Crear plantillas de correo electrónico](#create-email-templates) para obtener información sobre las opciones de edición.

## Duplicar plantillas de correo electrónico

Puede duplicar una plantilla de correo electrónico mediante cualquiera de los siguientes métodos:

* En los detalles de la plantilla de correo electrónico de la derecha, expanda **[!UICONTROL Más]** y haga clic en **[!UICONTROL Duplicar]**.

  ![Haga clic en Más para acceder a las acciones Eliminar y Duplicar](./assets/template-details-more-menu.png){width="400"}

* En la página de lista _[!UICONTROL Plantillas de correo electrónico]_, haga clic en los puntos suspensivos (...) junto a la plantilla y elija **[!UICONTROL Duplicado]**.

En el cuadro de diálogo, introduzca un nombre útil (único) y una descripción. Haga clic en **[!UICONTROL Duplicar]** para completar la acción.

La plantilla duplicada (nueva) de correo electrónico aparece en el listado de _[!UICONTROL Plantillas de correo electrónico]_.

## Eliminar plantillas de correo electrónico

La eliminación de una plantilla de correo electrónico no se puede deshacer, por lo que debe comprobarla antes de iniciar una acción de eliminación. Puede eliminar una plantilla de correo electrónico mediante cualquiera de los siguientes métodos:

* En los detalles de la plantilla a la derecha, expanda **[!UICONTROL Más]** y haga clic en **[!UICONTROL Eliminar]**.
* En la página de lista _[!UICONTROL Plantillas de correo electrónico]_, haga clic en los puntos suspensivos (...) junto a la plantilla y elija **[!UICONTROL Eliminar]**.

  ![Haga clic... para acceder a las acciones Duplicar y Eliminar](./assets/templates-list-more-menu.png){width="500"}

Esta acción abre un cuadro de diálogo de confirmación. Puede anular el proceso haciendo clic en **[!UICONTROL Cancelar]** o en **[!UICONTROL Eliminar]** para confirmar la eliminación.

## Realizar acciones masivas

En la página de lista de plantillas de correo electrónico, seleccione varias plantillas a la vez seleccionando las casillas de verificación de la izquierda. Aparece un banner en la parte inferior cuando selecciona varias plantillas.

![Un banner muestra el número de plantillas seleccionadas y el icono Eliminar](./assets/templates-multi-select-banner.png){width="600"}

**[!UICONTROL Eliminar]**: puede eliminar hasta un máximo de 20 plantillas al mismo tiempo. Un cuadro de diálogo de confirmación le permite anular la acción o confirmar la eliminación de las plantillas.

## Crear un correo electrónico a partir de una plantilla guardada

Desde la pantalla _Crear tu correo electrónico_, usa la sección _Seleccionar plantilla de diseño_ para empezar a crear tu contenido a partir de una plantilla.

Para empezar a crear contenido con una de las plantillas de correo electrónico creadas, siga estos pasos:

1. Acceda al Designer de correo electrónico desde la página _Editar contenido_.

   En la página _Crear su correo electrónico_, la pestaña _Plantillas de ejemplo_ está seleccionada de forma predeterminada.

1. Para usar una plantilla de correo electrónico personalizada, selecciona la pestaña **[!UICONTROL Plantillas guardadas]**.

   Esta pestaña muestra una lista de todas las plantillas de correo electrónico creadas en la zona protegida. Puede ordenarlos _Por nombre_, _Última modificación_ y _Última creación_.

1. Seleccione la plantilla que desee en la lista.

   Después de la selección, se muestra una previsualización de la plantilla. En el modo de vista previa, puede desplazarse entre todas las plantillas de una categoría (de ejemplo o guardadas, según su selección) utilizando las flechas derecha e izquierda.

1. Haga clic en **[!UICONTROL Usar esta plantilla]** en la parte superior derecha.

1. Desde el espacio de diseño visual, edite el contenido según sea necesario.
