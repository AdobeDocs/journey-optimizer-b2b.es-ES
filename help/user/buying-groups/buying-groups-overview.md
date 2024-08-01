---
title: Grupos de compra
description: Obtenga información sobre la compra de grupos y sus componentes.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 6%

---


# Comprar grupos

Para las actividades de ventas y marketing B2B, las cuentas son clave para cualquier estrategia. Cada cuenta tiene un grupo de personas asociadas a ella y estas personas pueden ser empleados de la cuenta o contratistas que trabajen con la cuenta. Las cuentas son jerárquicas y los productos pueden venderse en diferentes niveles de la jerarquía. Por ejemplo, Adobe Experience Platform podría venderse a nivel corporativo a una cuenta de nivel superior, mientras que Adobe Photoshop podría venderse a una cuenta que represente a una división o departamento dentro de una organización, como un departamento de diseño dentro de una corporación más grande.

![Diagrama de funciones de cuenta](assets/account-roles-diagram.png){width="800"}

En la cuenta podría haber un subconjunto de personas que forman el _grupo comprador_. Estas personas son las que en última instancia toman la decisión de compra, por lo que necesitan una atención especial del experto en marketing y es posible que necesiten que se les entregue información diferente a la de las demás personas asociadas con la cuenta. Los grupos de compra pueden incluir un grupo diferente de personas para diferentes líneas u ofertas de productos. Por ejemplo, un producto de ciberseguridad suele requerir la aprobación de una compra por parte de un director de información o un responsable de seguridad, y un representante del departamento legal, pero un producto de seguimiento de errores suele tener un vicepresidente de ingeniería y un Director de TI como miembros del grupo comprador.

## Componentes clave

Puede aumentar la eficacia del marketing estableciendo grupos de compra en Journey Optimizer B2B Edition que identifiquen a los miembros que faltan en las listas de cuentas de destino en función de las soluciones que deben vender sus equipos de ventas. Antes de que usted y su equipo de marketing empiecen a crear sus grupos de compra, asegúrese de haber definido los componentes clave. Estos componentes son esenciales para alcanzar las metas y objetivos empresariales.

| Componente | Finalidad |
| --------- | ------- |
| Interés de la solución | Este componente proporciona la respuesta a: <ul><li>Como organización de marketing, ¿qué vende?</li><li>¿Qué producto o colección de productos está dirigiendo para vender?</li></ul>  **_Ejemplo:_** Venta cruzada del nuevo producto X a clientes existentes |
| Público de cuenta | Este componente proporciona la respuesta a: <ul><li>¿A quién le estás vendiendo?</li><li>¿Cuál es la lista de cuentas de destino?</li></ul> **_Ejemplo:_** Segmento de cuenta definido por cuentas con el producto Y que tienen ingresos superiores a 1M |
| Comprar plantillas de rol de grupo | Este componente proporciona la respuesta a: <ul><li>¿A qué funciones está dirigiendo?</li><li>¿Qué conjunto de reglas se utiliza para determinar quién está asignado a la compra de funciones de grupo?</li></ul>  **_Ejemplo:_** Asigne una persona con título CMO a la función Responsable de tomar decisiones |

## Flujo de trabajo del grupo de compra

1. Crear grupos de compra.

   Opciones:
   * Usar [interés de solución](./solution-interests.md) y [plantilla de rol](./buying-groups-role-templates.md)
   * Usar importación de terceros
   * Generar desde AI/ML

1. Identificar personas desaparecidas.

   Analice el grupo de compra mediante filtros.

   **_Ejemplo:_** Falta la función de responsable de la toma de decisiones y la puntuación de integridad es &lt; 50

1. Completar las definiciones de grupos de compra.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Se utiliza en un recorrido de cuentas a través del interés de solución asociado.

## Acceso a grupos y componentes de compra

En el panel de navegación de la izquierda, expande **[!UICONTROL Cuentas]** y haz clic en **[!UICONTROL Comprar grupos]**.

La página _[!UICONTROL Grupos de compra]_ está organizada en fichas:

| Tabulación | Descripción |
| --- | ----------- |
| Información general de  | Esta ficha es la predeterminada y muestra el [panel Grupos de compra](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Examinar] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compra existentes. </li><li>Busque comprando el nombre del grupo. </li><li>Filtrar por interés de solución. </li><li>Profundice en los detalles del grupo de compra. </li><li>Crear un grupo de compra. Eliminar un grupo de compra.</li></ul> |
| [!UICONTROL Intereses de la solución] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compra existentes. </li><li>Busque comprando el nombre del grupo. </li><li>Acceda y edite las propiedades de interés de la solución. </li><li>Cree un interés de solución. </li><li>Eliminar un interés de solución. </li><li>Ver y eliminar trabajos del grupo de compra. </li></ul> |
| [!UICONTROL Plantillas de roles] | Esta pestaña admite las siguientes actividades: <ul><li>Vea la lista de plantillas de funciones existentes. </li><li>Buscar por nombre de plantilla de funciones. </li><li>Acceda y edite las propiedades y condiciones de la plantilla de funciones. </li><li>Cree una plantilla de funciones. </li><li>Eliminar una plantilla de funciones. </li></ul> |

## Búsqueda y filtro del grupo de compra

Use la ficha _[!UICONTROL Examinar]_ para ver la lista de grupos compradores. Puede buscar por nombre y filtrar la lista por interés de solución.

![Comprando página de exploración de grupo](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Detalles del grupo de compra

Para acceder a los detalles de un grupo comprador, haz clic en el nombre del grupo comprador en la pestaña _[!UICONTROL Examinar]_.

![Detalles del grupo de compra](assets/buying-group-details.png){width="600" zoomable="yes"}

### Puntuación de integridad del grupo comprador

La puntuación de integridad se utiliza para determinar si el grupo de compra es completo, lo que significa que tiene los miembros adecuados asignados a las funciones y está listo para utilizarse en un recorrido de cuentas. Esta puntuación es un porcentaje basado en el número de funciones dentro del grupo de compra y en cuántas funciones se han asignado con al menos un posible cliente.

Por ejemplo, si hay cuatro funciones dentro de un grupo comprador y tres de las cuatro funciones están asignadas al menos a un posible cliente, el grupo comprador está completado en un 75 %.

La puntuación de integridad del grupo de compra se vuelve a calcular cada vez que se crea o actualiza un grupo de compra.

### Puntuación de participación del grupo comprador

La puntuación de participación se utiliza para evaluar la eficacia de sus programas de marketing en función de las actividades de comportamiento de grupo de compra rastreadas a través de los recorridos. Esta puntuación se deriva de la actividad durante los últimos 30 días. Cualquier cambio de función en una plantilla requiere volver a calcular la puntuación de participación para todos los grupos compradores creados con esa plantilla. En el cálculo de la puntuación de participación solo se evalúan las actividades entrantes.

La puntuación mostrada se redondea (por ejemplo, una puntuación de 75,89999 se muestra como 76), no hay límite superior para la puntuación para GA y hay un límite de frecuencia diario de 20.

Los siguientes ejemplos ilustran el cálculo de la puntuación de participación:

**Grupo de compra 1** - puntuación de participación = 22.15

| Usuario | Función | Peso de rol | Acción | Hoy | ayer | Peso de acción | Puntuación |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Adam | Decisionista | 80 % | Sitio web visitado | 1000 | 2 | 1 | 22 |
| | | | Se hizo clic en el correo electrónico | 1 | 0 | 1 | 1 |
| | | | Pub descargado | 1 | 3 | 1 | 4 |
| Bob | Influenciador | 15 % | Sitio web visitado | 1 | 2 | 1 | 3 |
| Calvin | Profesional | 5 % | Sitio web visitado | 1 | 1 | 1 | 2 |

**Grupo de compra 2** - puntuación de participación = 8,55

| Usuario | Función | Peso de rol | Acción | Hoy | ayer | Peso de acción | Puntuación |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Alvin | Decisionista | 80 % | Sitio web visitado | 3 | 2 | 1 | 5 |
| | | | Se hizo clic en el correo electrónico | 1 | 0 | 1 | 1 |
| | | | Pub descargado | 1 | 3 | 1 | 4 |
| Bret | Influenciador | 15 % | Sitio web visitado | 1 | 2 | 1 | 3 |
| Leva | Profesional | 5 % | Sitio web visitado | 1 | 1 | 1 | 2 |
