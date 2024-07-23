---
title: Fragmentos
description: Aprenda a crear y utilizar fragmentos de contenido visual como componentes reutilizables para correos electrónicos y plantillas de correo electrónico en Adobe Journey Optimizer B2B Edition.
feature: Content, Email Authoring
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '1701'
ht-degree: 0%

---

# Fragmentos

Un fragmento es un componente reutilizable al que se puede hacer referencia en uno o varios correos electrónicos y plantillas de correo electrónico en Adobe Journey Optimizer B2B Edition. Normalmente es un bloque de contenido (texto, imagen o ambos) que se puede crear previamente e insertar rápidamente en un correo electrónico o plantilla de correo electrónico. Con esta funcionalidad, puede generar varios bloques de contenido personalizados que los miembros de su equipo de marketing pueden utilizar para ensamblar contenido de correo electrónico para un proceso de diseño mejorado. Los casos de uso comunes incluyen bloques de contenido de encabezado/pie de página para correo electrónico, banners de invitación a eventos y saludos de temporada.

Para aprovechar al máximo los fragmentos de sus flujos de trabajo:

* _Cree sus propios fragmentos_: cree fragmentos visuales desde cero o guarde contenido como fragmento en cualquier momento desde el editor de contenido visual.
* _Reutilizar los fragmentos: utilícelos tantas veces como sea necesario en el contenido.

## Fragmentos visuales

Los fragmentos visuales son bloques visuales predefinidos creados con el editor de contenido visual que se pueden reutilizar en varios correos electrónicos o plantillas de correo electrónico. El ámbito actual de Journey Optimizer B2B Edition y esta documentación son solo los fragmentos visuales. Los fragmentos basados en expresiones aún no son compatibles con Journey Optimizer B2B Edition.

## Acceso y administración de fragmentos

Para acceder a los fragmentos visuales en Adobe Journey Optimizer edición B2B, vaya a la navegación izquierda y haga clic en **[!UICONTROL Administración de contenido]** > **[!UICONTROL Fragmentos]**. Esta acción abre una página de lista con todos los fragmentos creados en la instancia enumerados en una tabla.

![Acceder a la biblioteca de fragmentos](./assets/fragments-list.png){width="700" zoomable="yes"}

La tabla está ordenada por la columna _[!UICONTROL Modificado]_, con los fragmentos actualizados más recientemente en la parte superior de la lista de forma predeterminada. Haga clic en el título de la columna para cambiar entre ascendente y descendente.

Busque cualquier fragmento introduciendo una cadena de texto en la barra de búsqueda para una coincidencia por nombre de fragmento. Haga clic en el icono _Filtrar_ para filtrar los elementos mostrados según los criterios especificados.

![Filtrar los fragmentos mostrados](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

Personalice las columnas que desee mostrar en la tabla haciendo clic en el icono _Personalizar tabla_ de la parte superior derecha. Seleccione las columnas que desea mostrar y haga clic en **[!UICONTROL Aplicar]**.

## Creación de fragmentos

Puede crear nuevos fragmentos visuales en Journey Optimizer B2B Edition haciendo clic en **[!UICONTROL Crear fragmento]** en la parte superior derecha.

1. En el cuadro de diálogo _[!UICONTROL Crear fragmento]_, escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** útiles (opcional).

   Requisitos de fragmento:

   * Nombre: máximo de 100 caracteres, debe ser único, sin distinción de mayúsculas y minúsculas

   * Descripción: máximo de 300 caracteres

   * Se permiten caracteres Alpha, numéricos y especiales

   * No se permiten los caracteres reservados: `\ / : * ? " < > |`

   ![Cuadro de diálogo Crear fragmento](./assets/assets-fragments-create-dialog.png){width="500"}

1. Haga clic en **[!UICONTROL Crear]**.

   El editor de contenido visual se abre con un lienzo vacío. Para crear un fragmento con el editor de contenido visual, consulte los temas de creación de contenido:

<!-- To be linked to the corresponding sections on this page: Adobe Journey Optimizer B2B Edition - Email Templates

Adding structure & content
Adding assets
Navigating the layers
Previewing & editing URLs
View options
More options -->

## Ver detalles del fragmento

Haga clic en el nombre de cualquier fragmento de la página de lista para abrir la página de detalles del fragmento.

Desde aquí puede editar el fragmento, cambiarle el nombre o actualizar su descripción (realice actualizaciones y haga clic fuera del cuadro de nombre/descripción para guardar automáticamente los cambios).

Haga clic en **[!UICONTROL Editar]** para abrir el fragmento en el editor de contenido visual.

Salga de la vista en cualquier momento haciendo clic en la flecha _Atrás_ en la parte superior izquierda, que le devuelve a la página de lista _Fragmentos_.

## Ver fragmento utilizado por referencias

En la página de detalles del fragmento, haga clic en la ficha **[!UICONTROL Utilizado por]** para ver los detalles de dónde se utiliza actualmente el fragmento en Journey Optimizer B2B Edition, en correos electrónicos, plantillas de correo electrónico y fragmentos.

>[!IMPORTANT]
>
>No se puede eliminar ningún fragmento que esté en uso actualmente en ningún correo electrónico o plantilla de correo electrónico.

Las referencias se muestran según la categoría: _Correo electrónico_ o _Plantilla de correo electrónico_. Los correos electrónicos de Journey Optimizer B2B Edition están incrustados y creados en recorridos de cuenta, por lo que el recorrido principal del correo electrónico que utiliza el fragmento se muestra en las referencias.

Haga clic en el vínculo para abrir el correo electrónico o la plantilla de correo electrónico correspondiente donde se utiliza el fragmento.

## Eliminar fragmentos

No se puede eliminar ningún fragmento que esté en uso actualmente en ninguna plantilla de correo electrónico o correo electrónico, por lo que asegúrese de comprobar las referencias de _usado por_ antes de iniciar la eliminación de un fragmento. Además, una eliminación no se puede deshacer, por lo que debe comprobarla antes de iniciar una acción de eliminación.

Puede eliminar un fragmento mediante cualquiera de los siguientes métodos:

* En los detalles del fragmento a la derecha, haga clic en **[!UICONTROL Eliminar]**.
* En la página de lista _[!UICONTROL Fragmentos]_, haga clic en los puntos suspensivos junto al fragmento y elija **[!UICONTROL Eliminar]**.

Esta acción abre un cuadro de diálogo de confirmación. Puede anular el proceso haciendo clic en **[!UICONTROL Cancelar]** o en **[!UICONTROL Eliminar]** para confirmar la eliminación.

Si el fragmento está en uso, la acción abre un cuadro de diálogo informativo que le advierte de que no se puede eliminar. Haga clic en **[!UICONTROL Aceptar]**, lo que anula la eliminación.

## Editar fragmentos

Puede editar un fragmento mediante cualquiera de los siguientes métodos:

* En los detalles del fragmento a la derecha, haga clic en **[!UICONTROL Editar]**.
* En la página de lista _[!UICONTROL Fragmentos]_, haga clic en los puntos suspensivos junto al fragmento y elija **[!UICONTROL Editar]**.

Esta acción abre el fragmento en un editor de contenido visual, donde puede editarlo con cualquiera de las características de [creando un fragmento](#create-fragments).

## Duplicar fragmentos

Puede duplicar un fragmento mediante cualquiera de los siguientes métodos:

* En los detalles del fragmento a la derecha, haga clic en **[!UICONTROL Duplicar]**.
* En la página de lista _[!UICONTROL Fragmentos]_, haga clic en los puntos suspensivos junto al fragmento y elija **[!UICONTROL Duplicar]**.

En el cuadro de diálogo, introduzca un nombre útil (único) y una descripción. Haga clic en **[!UICONTROL Duplicar]** para completar la acción.

El fragmento duplicado (nuevo) aparece en la lista _Fragmentos_.

## Guardar un fragmento desde el correo electrónico o el editor de plantillas

Siempre que esté en el editor de contenido visual para crear o editar un correo electrónico o una plantilla de correo electrónico, puede elegir guardar todo o parte del contenido como un fragmento para que esté disponible para reutilizarlo.

1. Cuando tenga contenido para guardar como fragmento, haga clic en **[!UICONTROL Más]** y elija **[!UICONTROL Guardar como fragmento]**.

1. Seleccione los diferentes elementos que desea incluir en el fragmento.

   Seleccione varias estructuras manteniendo pulsado el botón CTRL

   Solo se pueden seleccionar estructuras adyacentes entre sí y la interfaz no permite seleccionar elementos no adyacentes.

1. Con el contenido seleccionado, haz clic en **[!UICONTROL Crear]** en la parte superior derecha.

1. En el cuadro de diálogo, introduzca un nombre y una descripción útiles para el fragmento. Luego haga clic en **[!UICONTROL Crear]**.

   A continuación, el nuevo fragmento se mostrará en la página de lista _Fragmentos_ y también estará disponible para su uso en correos electrónicos y plantillas de correo electrónico.

## Añadir fragmentos visuales a un correo electrónico o plantilla

Los fragmentos están diseñados para su reutilización y se pueden insertar para la creación de plantillas de correo electrónico y correo electrónico. Puede añadir hasta 30 fragmentos en un correo electrónico o plantilla determinados. Los fragmentos se pueden anidar hasta un solo nivel.

>[!BEGINTABS]

>[!TAB Agregar fragmentos a un correo electrónico]

1. Vaya a Recorridos de cuenta y abra un recorrido recorrido existente o cree uno nuevo.

1. Cree un nodo &quot;Realizar una acción > People action > Send Email&quot;.

1. Cree o edite el contenido del correo electrónico para el nodo.

1. Arrastre y suelte un elemento del menú Componentes para proporcionar una _estructura_ para el fragmento.

1. Para abrir la lista de fragmentos, haga clic en el icono _Fragmentos_.

   Puede:
   * Ordenar el listado.
   * Examinar, buscar y filtrar el listado.
   * Cambiar entre las vistas Miniaturas y Lista.
   * Actualice la lista para reflejar cualquiera de los fragmentos creados recientemente.

1. Arrastre y suelte cualquier fragmento en el marcador de posición del componente de estructura.

   El editor procesa el fragmento dentro de la sección o el elemento de la estructura de correo electrónico.

El contenido del fragmento se actualiza dinámicamente dentro de la estructura para procesar una representación visual de cómo aparece el contenido en el correo electrónico.

Si desea agregar el fragmento para que ocupe todo el diseño horizontal dentro del correo electrónico, agregue una estructura de columna 1:1 y, a continuación, arrastre y suelte el fragmento en él.

Una vez guardado el correo electrónico, aparece en la página de detalles del fragmento > Utilizado por. Los fragmentos agregados a un correo electrónico no se pueden editar dentro del correo electrónico; el contenido se define mediante el fragmento de origen.

>[!TAB Agregar fragmentos a una plantilla de correo electrónico]

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas]**.

1. Cree una nueva plantilla o abra una plantilla de correo electrónico existente y haga clic en **[!UICONTROL Editar plantilla de correo electrónico]**.

1. Arrastre y suelte un elemento del menú Componentes para proporcionar una _estructura_ para el fragmento.

1. Para abrir la lista de fragmentos, haga clic en el icono _Fragmentos_.

   Puede:
   * Ordenar el listado.
   * Examinar, buscar y filtrar el listado.
   * Cambiar entre las vistas Miniaturas y Lista.
   * Actualice la lista para reflejar cualquiera de los fragmentos creados recientemente.

1. Arrastre y suelte cualquier fragmento en el marcador de posición del componente de estructura.

   El editor procesa el fragmento dentro de la sección o el elemento de la estructura de la plantilla de correo electrónico.

1. Arrastre y suelte cualquier fragmento en el marcador de posición del componente de estructura.

   El editor procesa el fragmento dentro de la sección o el elemento de la estructura de la plantilla de correo electrónico.

Si desea agregar el fragmento para que ocupe todo el diseño horizontal dentro de la plantilla de correo electrónico, agregue una estructura de columna 1:1 y, a continuación, arrastre y suelte el fragmento en él.

Una vez guardada la plantilla de correo electrónico, aparece en la página de detalles del fragmento > _[!UICONTROL Utilizado por]_. Los fragmentos agregados a una plantilla de correo electrónico no se pueden editar dentro de la plantilla (el contenido se define mediante el fragmento de origen).

>[!ENDTABS]

## Acciones de fragmento durante la creación

Después de agregar un fragmento a un correo electrónico o a una plantilla de correo electrónico, el contenido del fragmento no se puede editar dentro del correo electrónico o la plantilla. Sin embargo, puede aplicar las siguientes acciones:

* **[!UICONTROL Eliminar]**: esta acción elimina el fragmento del contenido actual del correo electrónico o de la plantilla de correo electrónico (el origen del fragmento no se ve afectado).
* **[!UICONTROL Actualizar]**: esta acción actualiza el contenido del fragmento en el correo electrónico o la plantilla de correo electrónico actual. Esto resulta útil cuando desea reflejar cualquier edición reciente en el fragmento después de agregarlo al correo electrónico o a la plantilla de correo electrónico.
* **[!UICONTROL Duplicado]**: esta acción duplica el fragmento dentro del mismo correo electrónico o plantilla de correo electrónico dentro del editor, con las mismas dimensiones y se agrega justo debajo de él.
* **[!UICONTROL Abrir fragmento]**: esta acción abre una nueva pestaña del explorador con la página del editor de fragmentos y los detalles.
* **[!UICONTROL Romper herencia]**: esta acción interrumpe la herencia del fragmento (y sus cambios) del origen. Utilice esta acción para que el contenido del fragmento esté disponible como contenido independiente y editable dentro del correo electrónico o la plantilla de correo electrónico. Esta acción también quita el correo electrónico o la plantilla de correo electrónico de la referencia _Utilizada por_ para el fragmento original.

Al seleccionar el fragmento en la página del editor, estas acciones están disponibles en la barra de herramientas contextual y en el panel de propiedades de la derecha.
