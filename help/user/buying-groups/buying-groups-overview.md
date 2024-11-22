---
title: Grupos de compra
description: Descubra cómo los grupos de compras en Journey Optimizer B2B edition pueden aumentar la eficacia del marketing al identificar y segmentar miembros para sus listas de cuentas.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 02b0e1a50b75dc02afe1b11217729e17583d5f12
workflow-type: tm+mt
source-wordcount: '1257'
ht-degree: 5%

---


# Grupos de compras

Para las actividades de ventas y marketing B2B, las cuentas son clave para cualquier estrategia. Cada cuenta tiene un grupo de personas asociadas a ella y estas personas pueden ser empleados de la cuenta o contratistas que trabajen con la cuenta. Las cuentas son jerárquicas y los productos pueden venderse en diferentes niveles de la jerarquía. Por ejemplo, Adobe Experience Platform podría venderse a nivel corporativo a una cuenta de nivel superior, mientras que Adobe Photoshop podría venderse a una cuenta que represente a una división o departamento dentro de una organización, como un departamento de diseño dentro de una corporación más grande.

![Diagrama de funciones de cuenta](assets/account-roles-diagram.png){width="800"}

En la cuenta podría haber un subconjunto de personas que forman el _grupo comprador_. Estas son las personas que finalmente toman la decisión de compra, por lo que necesitan una atención especial del experto en marketing y podrían necesitar una información diferente que las demás personas asociadas con la cuenta. Los grupos de compra pueden incluir un grupo diferente de personas para diferentes líneas u ofertas de productos. Por ejemplo, un producto de ciberseguridad suele requerir la aprobación de una compra por parte de un director de información o un responsable de seguridad, y un representante del departamento legal, pero un producto de seguimiento de errores suele tener un vicepresidente de ingeniería y un Director de TI como miembros del grupo comprador.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea la descripción general del vídeo](#overview-video)

## Componentes clave

Puede aumentar la eficacia del marketing estableciendo grupos de compras en Journey Optimizer B2B edition que identifiquen a los miembros que faltan en las listas de cuentas de destino en función de las soluciones que deben vender sus equipos de ventas. Antes de que usted y su equipo de marketing empiecen a crear sus grupos de compra, asegúrese de haber definido los componentes clave. Estos componentes son esenciales para alcanzar las metas y objetivos empresariales.

| Componente | Finalidad |
| --------- | ------- |
| Interés de la solución | Este componente proporciona la respuesta a: <ul><li>Como organización de marketing, ¿qué vende?</li><li>¿Qué producto o colección de productos está dirigiendo para vender?</li></ul>  **_Ejemplo:_** Venta cruzada del nuevo producto X a clientes existentes |
| Público de cuenta | Este componente proporciona la respuesta a: <ul><li>¿A quién le estás vendiendo?</li><li>¿Cuál es la lista de cuentas de destino?</li></ul> **_Ejemplo:_** Segmento de cuenta definido por cuentas con el producto Y que tienen ingresos superiores a 1M |
| Comprar plantillas de rol de grupo | Este componente proporciona la respuesta a: <ul><li>¿A qué funciones está dirigiendo?</li><li>¿Qué conjunto de reglas se utiliza para determinar quién está asignado a la compra de funciones de grupo?</li></ul>  **_Ejemplo:_** Asigne una persona con título CMO a la función Responsable de tomar decisiones |
| Fases del grupo de compras | (Opcional) Este componente proporciona la respuesta a: ¿Cómo realiza el seguimiento del grupo de compra de cara al éxito o al fracaso? |

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

## Ver grupos y componentes de compra

En el panel de navegación de la izquierda, expande **[!UICONTROL Cuentas]** y haz clic en **[!UICONTROL Comprar grupos]**.

La página _[!UICONTROL Grupos de compra]_ está organizada en fichas:

| Tabulación | Descripción |
| --- | ----------- |
| Información general de  | Esta ficha es la predeterminada y muestra el [panel Grupos de compra](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Examinar] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compra existentes. </li><li>Busque comprando el nombre del grupo. </li><li>Filtrar por interés de solución. </li><li>Profundice en los detalles del grupo de compra. </li><li>Crear un grupo de compra. Eliminar un grupo de compra.</li></ul> |
| [!UICONTROL Intereses de la solución] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compra existentes. </li><li>Busque comprando el nombre del grupo. </li><li>Acceda y edite las propiedades de interés de la solución. </li><li>Cree un interés de solución. </li><li>Eliminar un interés de solución. </li><li>Ver y eliminar trabajos del grupo de compra. </li></ul> |
| [!UICONTROL Plantillas de roles] | Esta pestaña admite las siguientes actividades: <ul><li>Vea la lista de plantillas de funciones existentes. </li><li>Buscar por nombre de plantilla de funciones. </li><li>Acceda y edite las propiedades y condiciones de la plantilla de funciones. </li><li>Cree una plantilla de funciones. </li><li>Eliminar una plantilla de funciones. </li></ul> |
| [!UICONTROL Fases] | Esta pestaña admite las siguientes actividades: <ul><li>Ver el modelo de fases de grupos de compra existente. </li><li>Acceda y edite el borrador del modelo de fases de grupo de compra. </li><li>Cree el modelo de etapas de grupo de compra. </li></ul> |

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

### Puntuación de participación de grupo de compras

La puntuación de participación en el grupo de compra es un número que determina la participación de los miembros de un grupo de compra, en función de las actividades que realizan. Cualquier actividad entrante realizada por los miembros del grupo comprador en los últimos 30 días se utiliza para calcular la puntuación.

Hay un límite de frecuencia diario de 20 para cada actividad. Si un miembro de un grupo comprador realiza la misma actividad más de 20 veces al día, el recuento de la actividad se limita a 20 y no a un número superior.

La puntuación mostrada se redondea. Por ejemplo, una puntuación de 75,89999 se muestra como 76.

#### Ponderación

Los usuarios pueden asignar _ponderación_ a cada rol en la plantilla de roles para asignar diferentes ponderaciones a un rol a fin de calcular la puntuación de participación.

![Establezca la ponderación en cada rol de la plantilla de roles](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Cada nivel de ponderación se traduce en un valor, que se utiliza para calcular la puntuación de participación:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Menor] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Importante] = 80
* [!UICONTROL Vital] = 100

Una plantilla de roles con tres roles ponderados como _[!UICONTROL Vital]_, _[!UICONTROL Importante]_ y _[!UICONTROL Normal]_ se convierte en los siguientes porcentajes ponderados:

| Función | Ponderación | Valor del sistema | Cálculo del valor | Porcentaje |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Decisionista | Vital | 100 | 100/240 | 41,67 % |
| Influenciador | Importante | 80 | 80/240 | 33,33 % |
| Profesional | Normal | 60 | 60/240 | 25 % |
|               | Total | 240 |                   |           |

#### Ejemplo de cálculo

El siguiente ejemplo ilustra el cálculo de la puntuación de participación utilizando el porcentaje de peso de función descrito, el recuento de actividades entrantes para cada miembro del grupo comprador y un límite diario de 20 para cada evento (si se ha producido varias veces).

| Función | Miembro | Tipo de actividad | Recuento de ayer | Recuento de hoy | Cálculo | Puntuación total |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Decisionista | Adam | Sitio web visitado | 37 | 15 | 20 + 15 | 35 |
|               |          | Correo electrónico clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Marcar | Sitio web visitado | 5 | 3 | 5 + 3 | 8 |
|               |          | Correo electrónico clicado | 1 | 1 | 1 + 1 | 2 |
|               |          | Pub descargado | 3 | 2 | 3 + 2 | 5 |
| **Puntuación total para encargados de tomar decisiones** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Influenciador | John | Sitio web visitado | 19 | 9 | 19 + 9 | 28 |
| **Puntuación total de influenciadores** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Profesional | Bob | Correo electrónico clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Correo electrónico clicado | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Correo electrónico clicado | 1 | 1 | 1 + 1 | 2 |
|               |          | Sitio web visitado | 1 | 7 | 1 + 7 | 8 |
|               |          | Pub descargado | 1 | 2 | 1 + 2 | 3 |
| **Puntuación total de los practicantes** |         |             |                 |             |      | **17** |

La puntuación de participación final se calcula aplicando la ponderación para cada una de las puntuaciones de rol:

| Función | Puntuación total del rol | Peso de rol % | Puntuación X peso % |
|-------------- |---------------- |------------- |---------------- |
| Responsables | 52 | 41,67 % | 21,67 |
| Personas con influencia en medios sociales | 28 | 33,33 % | 9,33 |
| Profesionales | 17 | 25 % | 4,25 |
| **Puntuación de participación final** |                |             | **35,25** |

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
