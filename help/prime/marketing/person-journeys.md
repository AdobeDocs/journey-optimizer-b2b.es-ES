---
title: Recorridos de la persona
description: Página de marcador de posición para recorridos de persona.
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 21%

---

# Recorridos de la persona

En Journey Optimizer B2B edition Prime, los recorridos de personas son planes de marketing automatizados y basados en posibles clientes en varios pasos que utilizan datos de Marketo Engage y que organizan experiencias personalizadas en varios canales en respuesta a participación, eventos empresariales o campañas programadas.

Para empezar con el recorrido en primera persona:

1. Cree un recorrido de persona.
1. Añada los nodos y defina el flujo de recorrido en el mapa de recorrido.
1. Publique el recorrido.

## Acceso y exploración de recorridos de persona

En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de mercadotecnia]** y seleccione **[!UICONTROL recorridos de personas]**.

Puede escribir texto en la herramienta _Buscar_ situada en la parte superior de la lista para filtrar la lista mostrada por nombre.

### Columnas de lista de recorrido

La página de lista recorridos incluye las siguientes columnas:

Nombre (haga clic en el nombre para abrir el mapa de recorrido y editarlo)
Estado
Fecha de creación
Creado por
Última actualización
Última actualización de
Publicado el
Publicado por
Fecha de inicio
Fecha de finalización

Puede ordenar la lista por estado, fecha de creación o última actualización haciendo clic en el encabezado de la columna.

Para personalizar (mostrar/ocultar) las columnas que se muestran en la tabla, haga clic en el icono Personalizar tabla ( ) en la esquina superior derecha. Active o desactive las casillas de verificación en el cuadro de diálogo y haga clic en Aplicar.

### Estado del recorrido

El estado de un recorrido puede cambiar según las acciones que se apliquen. En función del estado de un recorrido, determinadas acciones no estarán disponibles en el lado derecho del encabezado.

| Estado | Descripción | Acciones disponibles |
| ------ | ----------- | ----------------- |
| Borrador | Un recorrido sin publicar que se puede editar. | <li>Publicar <li>Duplicado <li>Eliminar |
| En vivo | El estado del recorrido cambia de Borrador a Activo cuando se publica un recorrido. En este estado, ya no se puede editar. | <li>Duplicar |
| Finalizado | Cuando todos los miembros de la audiencia de una persona o cuenta de un recorrido completan el recorrido, el estado cambia de Activo o Cerrado a nuevas entradas y pasa a Finalizado. | <li>Duplicado <li>Eliminar |

## Crear un recorrido de persona

1. Haga clic en **[!UICONTROL Crear Recorrido]** en la parte superior derecha de la lista de recorrido.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único (obligatorio) y **[!UICONTROL Descripción]** (opcional).

<!-- 
   ![Create Journey dialog](./assets/person-journey-create-dialog.png){width="400"}
-->

1. Haga clic en **[!UICONTROL Crear]**.

### Diseño de recorrido

El _mapa de recorrido_ es la zona central del área de trabajo de recorrido. Es donde puede agregar nodos de recorrido y configurarlos. Haga clic en un nodo para abrir sus propiedades en el panel situado a la derecha del diseño y configúrelas según su diseño. El recorrido de personas siempre comienza con un nodo _[!UICONTROL Audiencia de personas]_, donde puede definir la entrada del recorrido.

<!--
   ![Journey map for newly created journey](./assets/person-journey-create-dialog.png){width="400"}
-->

Después de crear un recorrido de persona y agregar la audiencia de persona, genere el recorrido con nodos. El mapa de recorrido proporciona un lienzo en el que puede crear sus casos de uso de marketing B2B de varios pasos utilizando los siguientes tipos de nodos para construir el recorrido:

* [Iniciar una acción](./action-nodes.md)
* [Escuchar un evento](./listen-for-event-nodes.md)
* [Espera](./wait-nodes.md)
* [Dividir rutas](./split-merge-paths-nodes.md)
* [Siguiente mejor ruta](./next-best-path.md)
* [Combinar rutas](./split-merge-paths-nodes.md)


## administración de recorrido



## Mapa del recorrido

Haga clic en el nombre (mostrado como vínculo) en la lista recorridos para revisar los detalles, realizar cambios y realizar acciones.

El encabezado de cada mapa de recorrido incluye:

Nombre del recorrido
Herramienta de edición del nombre del recorrido (icono Editar )
Estado del recorrido
Desde el mapa de recorrido, puede Añadir los nodos y definir el flujo de recorrido.

### acciones de recorrido

La página de lista recorridos incluye todos los recorridos de cuenta o persona de la instancia de Journey Optimizer B2B edition. Desde la página de lista, puede aplicar una serie de acciones a un recorrido.



#### Duplicación de un recorrido

Una acción de duplicado es similar a una función de clonado, pero el recorrido duplicado no incluye ningún recurso de contenido de recorrido creado. Puede duplicar los detalles del recorrido o simplemente un esqueleto de la estructura de flujo y ruta.

NOTA

Haga clic en el icono Más (...) junto al nombre del recorrido y seleccione Duplicar.

Según el estado del recorrido, también puede acceder a la acción de duplicado desde los detalles del recorrido o el mapa del recorrido:

Para un recorrido de borrador, haga clic en el menú More... en la parte superior derecha y seleccione Duplicate.
Para todos los demás estados de recorrido, haga clic en Duplicar en la parte superior derecha.
En el cuadro de diálogo Duplicar Recorrido, establezca el Nombre y la Descripción para el nuevo recorrido.
De forma predeterminada, el cuadro de diálogo utiliza el nombre del recorrido duplicado anexado con _copy. Introduzca otro nombre único para el recorrido, según sea necesario.

Elija el tipo de duplicación:
Duplicación parcial del contenido: utilice este tipo para copiar todo el contenido del recorrido, excluyendo los correos electrónicos o mensajes SMS creados. Los nodos que hacen referencia a un mensaje de correo electrónico o SMS de Marketo Engage están totalmente intactos.
Duplicar sin detalles: utilice este tipo para copiar solo la estructura y las rutas del nodo. Todos los ajustes de nodo y las condiciones de ruta no están definidos (predeterminado), por lo que puede reutilizar el flujo básico con diferentes ajustes de segmentación de audiencia, acciones y rutas. Todos los nodos de espera utilizan el valor predeterminado de cinco días.
Haga clic en Duplicate.
El recorrido duplicado se abre en el mapa de recorrido, donde puede establecer los detalles y crear contenido de recorrido según sea necesario.

Eliminación de un recorrido

Utilice una acción de eliminación para eliminar un recorrido de forma permanente. No puede eliminar un recorrido activo o programado.

Haga clic en el icono Más (...) junto al nombre del recorrido y seleccione Eliminar.
Según el estado del recorrido, también puede acceder a la acción de eliminación desde los detalles del recorrido o el mapa del recorrido:

Para un recorrido de borrador, haga clic en el menú More... en la parte superior derecha y seleccione Delete.
Para otros estados de recorrido, como Finalizado o Anulado, haga clic en Eliminar en la parte superior derecha.
En el cuadro de diálogo de confirmación, haga clic en Eliminar.






