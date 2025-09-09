---
title: Grupos de compras
description: 'Optimice el marketing basado en cuentas con grupos de compra: identifique a los responsables de la toma de decisiones, realice un seguimiento de las puntuaciones de participación y automatice la segmentación en Journey Optimizer B2B edition.'
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '1187'
ht-degree: 73%

---


# Grupos de compras

Para las actividades de ventas y marketing B2B, las cuentas son clave para cualquier estrategia. Cada cuenta tiene un grupo de personas asociadas a ella y estas personas pueden ser empleados de la cuenta o contratistas que trabajen con la cuenta. Las cuentas son jerárquicas y los productos pueden venderse en diferentes niveles de jerarquía. Por ejemplo, Adobe Experience Platform podría venderse a nivel corporativo a una cuenta de nivel superior. Y Adobe Photoshop podría venderse a una cuenta que represente a una división o departamento dentro de una organización, como un departamento de diseño dentro de una corporación más grande.

![Diagrama de funciones de cuenta](assets/account-roles-diagram.png){width="800"}

En la cuenta podría haber un subconjunto de personas que forman el _grupo de compras_. Estas son las personas que finalmente toman la decisión de compra, por lo que el experto en marketing debe prestarles una atención especial ya que podrían necesitar una información distinta a la de las demás personas asociadas con la cuenta. Los grupos de compra pueden incluir un grupo diferente de personas para diferentes líneas u ofertas de productos. Por ejemplo, un producto de ciberseguridad puede requerir normalmente que un director de sistemas de información o un director de seguridad, y un representante del departamento jurídico apruebe una compra. Un producto de seguimiento de errores suele tener un vicepresidente de ingeniería y un director de TI como miembros del grupo de compras.

![Icono de vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea la descripción general del vídeo](#overview-video)

## Componentes principales

Puede aumentar la eficacia del marketing mediante el establecimiento de grupos de compra que identifiquen a los miembros de las listas de cuentas objetivo para las soluciones que los equipos de ventas deben vender. Antes de que usted y su equipo de marketing empiecen a crear sus grupos de compras, asegúrese de haber definido los componentes clave. Estos componentes son esenciales para alcanzar las metas y objetivos empresariales.

| Componente | Finalidad |
| --------- | ------- |
| Interés de la solución | Este componente proporciona la respuesta a lo siguiente: <ul><li>Como organización de marketing, ¿qué vende?</li><li>¿Qué producto o colección de productos quiere vender?</li></ul>  **Ejemplo::_** venta cruzada del nuevo producto X a clientes existentes |
| Público de cuenta | Este componente proporciona la respuesta a lo siguiente: <ul><li>¿A quién le está vendiendo?</li><li>¿Cuál es la lista de cuentas que está segmentando?</li></ul> **Ejemplo:_** segmento de cuenta definido por las cuentas con el producto Y que tienen ingresos superiores a un millón |
| Plantillas de función del grupo de compras | Este componente proporciona la respuesta a lo siguiente: <ul><li>¿Qué funciones está segmentando?</li><li>¿Qué conjunto de reglas se utiliza para determinar quién está asignado a la compra de funciones de grupo?</li></ul>  **_Ejemplo:_** asignar una persona con el cargo de director de marketing (CMO) a la función de responsable de tomar decisiones |
| Fases del grupo de compras | (Opcional) Este componente proporciona la respuesta a: ¿Cómo realiza el seguimiento del grupo de compra de cara al éxito o al fracaso? |

## Asignación de miembros

Existen tres formas de asignar o eliminar miembros de un grupo de compras. En la lista siguiente se describen estos métodos de adición y eliminación en orden de prioridad. El método de nivel superior tiene la prioridad más alta y el más bajo no puede anularlo.

1. **_Acción manual_**: una acción manual para añadir o quitar miembros realizada por un usuario de ventas para el grupo de compras
2. **_Acción de recorrido_**: [nodos de acción de recorrido para los miembros del grupo de compras](../journeys/action-nodes.md#add-a-people-based-action) (_Asignar al grupo de compras_ o _Quitar del grupo de compras_)
3. **_Trabajos del sistema_**: trabajos de [creación](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) y mantenimiento del grupo de compras.

Para evitar la anulación incorrecta de una asignación de miembros en un grupo de compra, esta lista tiene el orden de prioridad seguido en el sistema para garantizar una asignación de miembros precisa. Por ejemplo, cuando un usuario de ventas añade manualmente un miembro al grupo de compras, no desea que un trabajo de mantenimiento modifique esa adición. Utilizando el orden de prioridad, se aplican los siguientes escenarios:

* Si un usuario asigna manualmente un miembro a un grupo de compra y va seguido de un trabajo de mantenimiento del grupo de compra que elimina el mismo miembro del grupo de compra, el trabajo de mantenimiento **no elimina** ese miembro y no puede anular la asignación manual.
* Si un usuario asigna manualmente un miembro a un grupo comprador y va seguido de un nodo de recorrido activado que elimina el mismo miembro del grupo comprador, la acción del nodo **no elimina** ese miembro y no puede anular la asignación manual.
* Si un nodo de acción de recorrido activado agrega un miembro a un grupo comprador y va seguido de un trabajo de mantenimiento de grupo comprador que elimina el mismo miembro del grupo comprador, el trabajo de mantenimiento **no elimina** ese miembro y no puede anular la asignación de acción de recorrido.

## Flujo de trabajo del grupo de compras

1. Crear grupos de compra.

   * Definir [interés de solución](./solution-interests.md) y [plantilla de función](./buying-groups-role-templates.md)
   * [Cree el grupo de compras](./buying-groups-create.md#create-buying-groups) y asigne [etapas del grupo de compras](./buying-group-stages.md).

1. Identificar a las personas desaparecidas según la completitud.

   Analice el grupo de compra mediante filtros.

   **Ejemplo::_** falta la función de responsable de la toma de decisiones y la puntuación de completitud es &lt; 50

1. Completar las definiciones de grupos de compra.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Añadir acciones del grupo de compras a los recorridos de la cuenta.

## Ver grupos y componentes de compra

En el panel de navegación de la izquierda, expanda **[!UICONTROL Cuentas]** y haga clic en **[!UICONTROL Comprar grupos]**.

La página _[!UICONTROL Grupos de compras]_ está organizada en pestañas:

| Tabulación | Descripción |
| --- | ----------- |
| [!UICONTROL Información general] | Esta pestaña es la predeterminada y muestra el [panel de control Grupos de compras](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Examinar] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compras existentes. </li><li>Buscar por el nombre del grupo de compras. </li><li>Filtrar por interés de solución. </li><li>Profundizar en los detalles del grupo de compras. </li><li>Cree un grupo de compras. </li></ul> |
| [!UICONTROL Intereses de la solución] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compras existentes. </li><li>Buscar por el nombre del grupo de compras. </li><li>Acceder y editar las propiedades de interés de la solución. </li><li>Crear una solución de interés. </li><li>Eliminar un interés de solución. </li><li>Ver y eliminar trabajos del grupo de compras. </li></ul> |
| [!UICONTROL Plantillas de funciones] | Esta pestaña admite las siguientes actividades: <ul><li>Vea la lista de plantillas de funciones existentes. </li><li>Busque por nombre de plantilla de funciones. </li><li>Acceder y editar las propiedades y condiciones de la plantilla de funciones. </li><li>Crear una plantilla de funciones. </li><li>Eliminar una plantilla de funciones. </li></ul> |
| [!UICONTROL Fases] | Esta pestaña admite las siguientes actividades: <ul><li>Ver el modelo de fases de grupos de compras existente. </li><li>Acceder y editar el borrador del modelo de fases de grupo de compras. </li><li>Crear el modelo de fases de grupo de compras. </li></ul> |

## Búsqueda y filtro del grupo de compras

Utilice la pestaña _[!UICONTROL Examinar]_ para acceder a la lista de todos los grupos de compras. Puede buscar por nombre y filtrar la lista por interés de solución.

![Página de exploración del grupo de compras](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Detalles del grupo de compras

Para acceder a los detalles de un grupo de compras, haga clic en el nombre del grupo de compras en la pestaña _[!UICONTROL Examinar]_. [Más información](./buying-group-details.md)

![Detalles del grupo de compras](assets/buying-group-details.png){width="600" zoomable="yes"}

### Puntuación de integridad del grupo de compras

La puntuación de integridad se utiliza para determinar si el grupo comprador tiene los miembros adecuados asignados a las funciones y está listo para utilizarse en un recorrido de cuentas. Esta puntuación es un porcentaje basado en el número de funciones dentro del grupo de compras y en cuántas funciones se han asignado con al menos un posible cliente.

Por ejemplo, si hay cuatro funciones dentro de un grupo de compras y tres de cuatro están asignadas al menos a un posible cliente, el grupo de compras está completado en un 75 %.

La puntuación de integridad del grupo de compras se vuelve a calcular cada vez que se crea o actualiza un grupo de compras.

### Puntuación de participación de grupo de compras {#engagement-score}

La puntuación de participación se basa en las actividades de los miembros del grupo comprador, las acciones ponderadas y los roles ponderados. La puntuación resultante se normaliza dentro del inquilino/instancia para habilitar una comparación coherente y permitir perspectivas procesables.

El cálculo de la puntuación de participación inicial comienza en cuanto crea el grupo comprador y se vuelve a calcular diariamente.

Consulte [Puntuaciones de participación](./engagement-scores.md) para obtener información detallada acerca de las actividades y los cálculos de puntuación de participación.

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
