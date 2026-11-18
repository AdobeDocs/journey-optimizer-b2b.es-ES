---
title: Creación y publicación de un Recorrido
description: Cree recorridos de cuenta y persona en el lienzo visual, agregue nodos de acción y evento, configure la programación y publique para la orquestación en directo en Journey Optimizer B2B Edition.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
autotag-review: 2026-03-30T23:14:46.843Z
TQID: 'https://experienceleague.adobe.com/-emMaxlrae40JXP0tThacD3xA27d5OzO8tX6o-mOnfg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 9d5641659907d61be992ed218088a023a5211c56
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 5%
---
# Creación y publicación de un recorrido

Para comenzar un nuevo recorrido, cree el recorrido y, a continuación, construya los nodos y el flujo de recorrido en el mapa de recorrido.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

## Crear un recorrido

En **[!UICONTROL Administración de Recorrido]** en el panel de navegación izquierdo, seleccione el tipo de recorrido que desea crear:

* **[!UICONTROL recorridos de cuenta]**
* **[!UICONTROL recorridos de personas]**

_Para agregar un nuevo recorrido :_

+++Recorrido de cuenta

1. Haga clic en **[!UICONTROL Crear Recorrido de cuenta]** en la parte superior derecha de la página.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único (obligatorio) y **[!UICONTROL Descripción]** (opcional).

   ![Cuadro de diálogo Crear Recorrido de cuenta](./assets/account-journey-create-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

+++

+++Recorrido de la persona

1. Haga clic en **[!UICONTROL Crear Recorrido]** en la parte superior derecha de la página.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único (obligatorio) y **[!UICONTROL Descripción]** (opcional).

   ![Crear cuadro de diálogo de Recorrido](./assets/person-journey-create-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

+++

## Componentes para el diseño de recorridos

El _mapa de recorrido_ es la zona central del área de trabajo de recorrido. Es en esta zona donde puede agregar nodos de recorrido y configurarlos. Haga clic en un nodo para abrir su panel de propiedades a la derecha del lienzo y establecerlo según el diseño. Un recorrido siempre comienza con un nodo de audiencia, donde puede definir la entrada para el recorrido:

* [Nodo de audiencia de cuenta](./account-audience-nodes.md)
* [Nodo de audiencia de persona](./person-audience-nodes.md)

Después de crear un recorrido de cuentas y agregar la audiencia, diseñe el recorrido con los nodos. El mapa de recorrido proporciona un lienzo en el que puede crear sus casos de uso de marketing B2B de varios pasos utilizando los siguientes tipos de nodos para crear un recorrido de cuentas:

* [Iniciar una acción](./action-nodes.md)
* [Escuchar un evento](./listen-for-event-nodes.md)
* [Dividir rutas](./split-merge-paths-nodes.md)
* [Rutas divididas de variantes](./variant-split-paths-nodes.md)
* [Siguiente mejor ruta](./next-best-path-node.md)
* [Espera](./wait-nodes.md)
* [Combinar rutas](./split-merge-paths-nodes.md)

## Guardas

Para ayudarle a crear un recorrido sin encontrar errores, existen las siguientes protecciones:

* _Eliminando un nodo de ruta dividida_: para eliminar un nodo se deben eliminar todos los nodos subsiguientes de cada ruta.
* _Eliminando un nodo de combinación_: un nodo de combinación solo se puede eliminar cuando hay una ruta conectada a él. Para eliminar un nodo de combinación, deje solo una ruta seleccionada.
* _Cambiar entre cuentas y personas_: al cambiar la selección de cuentas a personas se eliminan todos los nodos subsiguientes de cada ruta.

## Añadir un nodo

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en la ruta y elija el tipo de nodo.

   ![Haga clic en + y elija el tipo para agregar el nodo de recorrido a la ruta](./assets/node-add-menu.png){width="400" zoomable="no"}

   Los tipos de nodo disponibles dependen del tipo de recorrido y del contexto de la ruta. Consulte [_nodos de Recorrido_](./journey-nodes.md) para obtener más información.

1. Establezca las propiedades del nodo a la derecha.

   Las propiedades dependen del tipo de nodo.

## Etiqueta de un nodo {#label-a-node}

En [!DNL Adobe Journey Optimizer B2B Edition], cada nodo del mapa de recorrido muestra su nombre predeterminado, como _Esperar_ o _Enviar correo electrónico_. Añada etiquetas de visualización para distinguir nodos del mismo tipo e identificar el propósito de cada paso. Por ejemplo, use _tiempo de reutilización de 48 horas_ o _correo electrónico de bienvenida_.

Puede agregar una etiqueta de visualización a cualquier nodo de un recorrido de cuenta o de persona.

1. En el mapa de recorrido, seleccione el nodo que desea etiquetar.

1. En las propiedades del nodo, escriba el texto en el campo **[!UICONTROL Mostrar etiqueta]**.

   La etiqueta puede incluir hasta 255 caracteres.

1. Haga clic fuera del campo para aplicar la etiqueta.

   ![Agregue una etiqueta de visualización para distinguir el nodo dentro del recorrido](./assets/node-display-label.png){width="500" zoomable="no"}

   La etiqueta reemplaza el nombre predeterminado en el nodo del mapa de recorrido.

Para restaurar el nombre predeterminado, borre el campo **[!UICONTROL Mostrar etiqueta]** y haga clic fuera del campo.

Al publicar el recorrido, la etiqueta de visualización de cada nodo se guarda con el recorrido publicado.

>[!NOTE]
>
>Las etiquetas de visualización no están disponibles para los nodos de recorridos creados antes de que esta capacidad estuviera disponible.

Las etiquetas de nodo están disponibles en el esquema `AJOB2B - 1.5.4 - journey node` y en el conjunto de datos `AJOB2B-1_5_4-journey_node`. Puede consultar etiquetas en [!DNL Adobe Experience Platform] y utilizarlas para generar informes en [!DNL Adobe Customer Journey Analytics]. Para obtener más información acerca de cómo consultar los datos exportados, revise los [requisitos previos de consulta del conjunto de datos](../data/aep-query-examples.md#prerequisites).

## Eliminación de un nodo

1. Vaya al mapa del recorrido.

1. En las propiedades del nodo, a la derecha, haga clic en el icono _Eliminar_ ( ![Icono Eliminar](../assets/do-not-localize/icon-delete.svg) ).

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Adición y eliminación de una ruta

1. En el mapa de recorrido, haga clic en el icono más ( **+** ) de la ruta y agregue el [nodo de ruta dividida](./split-merge-paths-nodes.md#split-paths).

1. En las propiedades del nodo a la derecha, seleccione **[!UICONTROL Cuenta]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]**.

   Para cada ruta creada en el recorrido, aparece una nueva tarjeta de ruta en las propiedades.

1. Vaya a una de las rutas de acceso del recorrido y agregue los nodos [action](./action-nodes.md) o [event](./listen-for-event-nodes.md) a esa ruta mediante el icono más.

1. Seleccione el nodo [ruta dividida](./split-merge-paths-nodes.md) para abrir las propiedades a la derecha.

   Las rutas que tienen nodos no se pueden eliminar.

1. Para eliminar una ruta, primero debe eliminar todos los nodos de esa ruta.

## Programar un recorrido

Cuando publica un recorrido, puede comenzar inmediatamente o en una fecha futura programada. La fecha de finalización puede ser un máximo de tres años desde la fecha de inicio. Después de publicar un recorrido (estado _Activo_), puede actualizar la fecha de finalización del recorrido, pero no la fecha de inicio.

1. Vaya al mapa del recorrido.

1. Programe su recorrido haciendo clic en **[!UICONTROL Configuración de Recorrido]** en el encabezado.

1. En el cuadro de diálogo, defina las opciones de programación:

   * Elija un tipo de programación.

     Para activar el recorrido en el momento de la publicación, elija **[!UICONTROL Inmediatamente]**.

     Para activar el recorrido en una fecha futura, elige **[!UICONTROL En una fecha específica]** y haz clic en el icono _Calendario_ para seleccionar la fecha.

     ![cuadro de diálogo de configuración de Recorrido](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Especifique la **[!UICONTROL fecha de finalización]** del recorrido. Puede ser un máximo de tres años desde la fecha de inicio (este campo es obligatorio para publicar).

1. Haga clic en **[!UICONTROL Guardar]**.

   Cuando esté listo para publicar el recorrido, puede revisar esta configuración al hacer clic en _[!UICONTROL Publicar]_.

## Publicación de un recorrido

Puede publicar un recorrido si no hay errores de bloqueador. Cuando se publique, el estado del recorrido cambiará a _Activo_. Si el recorrido tiene errores, el botón _[!UICONTROL Publicar]_ aparece atenuado con información de contenido: `Resolve errors before publishing`.

>[!NOTE]
>
>Después de publicar un recorrido de cuenta, hay un retraso de hasta 24 horas para que las cuentas que cumplen los requisitos ingresen al recorrido.

1. En la parte superior derecha del mapa de recorrido, haga clic en **[!UICONTROL Publicar]**.

1. En el cuadro de diálogo _[!UICONTROL Revisar configuración de recorrido]_, establezca las opciones de inicio de recorrido.

   Si ya ha establecido la configuración de recorrido para definir una programación, revise la configuración.

   Si necesita configurar la activación del recorrido, elija un tipo de programación:

   * Para activar el recorrido en el momento de la publicación, elija **[!UICONTROL Inmediatamente]**.

   * Para activar el recorrido en una fecha futura, elige **[!UICONTROL En una fecha específica]** y haz clic en el icono _Calendario_ para seleccionar la fecha.

1. Si es necesario, especifique la **[!UICONTROL fecha de finalización]** del recorrido.

   ![cuadro de diálogo de configuración de Recorrido](./assets/journey-publish-dialog.png){width="400" zoomable="no"}

   Puede ser un máximo de tres años desde la fecha de inicio (este campo es obligatorio para publicar).

1. Haga clic en **[!UICONTROL Next]**.

1. En el diálogo de confirmación, haga clic en **[!UICONTROL Publicar]**.

## Vídeo resumen

>[!VIDEO](https://video.tv.adobe.com/v/3443222/?captions=spa&learn=on)
