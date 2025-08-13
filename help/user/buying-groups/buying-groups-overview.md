---
title: Grupos de compras
description: Descubra cómo los grupos de compras en Journey Optimizer B2B Edition pueden aumentar la eficacia del marketing al identificar y segmentar miembros para sus listas de cuentas.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: a2917ea8c389c35129a77d427528051be499addf
workflow-type: tm+mt
source-wordcount: '2170'
ht-degree: 97%

---


# Grupos de compras

Para las actividades de ventas y marketing B2B, las cuentas son clave para cualquier estrategia. Cada cuenta tiene un grupo de personas asociadas a ella y estas personas pueden ser empleados de la cuenta o contratistas que trabajen con la cuenta. Las cuentas son jerárquicas y los productos pueden venderse en diferentes niveles de jerarquía. Por ejemplo, Adobe Experience Platform podría venderse a nivel corporativo a una cuenta de nivel superior. Y Adobe Photoshop podría venderse a una cuenta que represente a una división o departamento dentro de una organización, como un departamento de diseño dentro de una corporación más grande.

![Diagrama de funciones de cuenta](assets/account-roles-diagram.png){width="800"}

En la cuenta podría haber un subconjunto de personas que forman el _grupo de compras_. Estas son las personas que finalmente toman la decisión de compra, por lo que el experto en marketing debe prestarles una atención especial ya que podrían necesitar una información distinta a la de las demás personas asociadas con la cuenta. Los grupos de compra pueden incluir un grupo diferente de personas para diferentes líneas u ofertas de productos. Por ejemplo, un producto de ciberseguridad puede requerir normalmente que un director de sistemas de información o un director de seguridad, y un representante del departamento jurídico apruebe una compra. Un producto de seguimiento de errores suele tener un vicepresidente de ingeniería y un director de TI como miembros del grupo de compras.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea la descripción general del vídeo](#overview-video)

## Componentes principales

Puede aumentar la eficacia del marketing estableciendo grupos de compras en Journey Optimizer B2B Edition que identifiquen a los miembros que faltan en las listas de cuentas de destino en función de las soluciones que sus equipos de ventas se encargan de vender. Antes de que usted y su equipo de marketing empiecen a crear sus grupos de compras, asegúrese de haber definido los componentes clave. Estos componentes son esenciales para alcanzar las metas y objetivos empresariales.

| Componente | Finalidad |
| --------- | ------- |
| Interés de la solución | Este componente proporciona la respuesta a lo siguiente: <ul><li>Como organización de marketing, ¿qué vende?</li><li>¿Qué producto o colección de productos quiere vender?</li></ul>  **Ejemplo::_** venta cruzada del nuevo producto X a clientes existentes |
| Público de cuenta | Este componente proporciona la respuesta a lo siguiente: <ul><li>¿A quién le está vendiendo?</li><li>¿Cuál es la lista de cuentas a las que se dirige?</li></ul> **Ejemplo:_** segmento de cuenta definido por las cuentas con el producto Y que tienen ingresos superiores a un millón |
| Plantillas de función del grupo de compras | Este componente proporciona la respuesta a lo siguiente: <ul><li>¿A qué funciones se está dirigiendo?</li><li>¿Qué conjunto de reglas se utiliza para determinar quién está asignado a la compra de funciones de grupo?</li></ul>  **_Ejemplo:_** asignar una persona con el cargo de director de marketing (CMO) a la función de responsable de tomar decisiones |
| Fases del grupo de compras | (Opcional) Este componente proporciona la respuesta a: ¿Cómo realiza el seguimiento del grupo de compra de cara al éxito o al fracaso? |

## Asignación de miembros

Existen tres formas de asignar o eliminar miembros de un grupo de compras. En la lista siguiente se describen estos métodos de adición y eliminación en orden de prioridad. El método de nivel superior tiene la prioridad más alta y el más bajo no puede anularlo.

1. **_Acción manual_**: una acción manual para añadir o quitar miembros realizada por un usuario de ventas para el grupo de compras
2. **_Acción de recorrido_**: [nodos de acción de recorrido para los miembros del grupo de compras](../journeys/action-nodes.md#add-a-people-based-action) (_Asignar al grupo de compras_ o _Quitar del grupo de compras_)
3. **_Trabajos del sistema_**: trabajos de [creación](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) y mantenimiento del grupo de compras.

Para garantizar que la asignación de miembros en un grupo de compras no se anule incorrectamente, esta lista tiene el orden de prioridad establecido en el sistema para garantizar una asignación de miembros precisa. Por ejemplo, cuando un usuario de ventas añade manualmente un miembro al grupo de compras, no desea que un trabajo de mantenimiento modifique esa adición. Utilizando el orden de prioridad, se aplican los siguientes escenarios:

* Si un usuario asigna manualmente un miembro a un grupo de compras, y esto va seguido de un trabajo de mantenimiento del grupo de compras que elimina al mismo miembro del grupo de compras, el trabajo de mantenimiento **no elimina** ese miembro y no puede anular la asignación manual.
* Si un usuario asigna manualmente un miembro a un grupo de compras y esto va seguido de un nodo de recorrido activado que elimina al mismo miembro del grupo de compras, la acción del nodo **no elimina** ese miembro y no puede anular la asignación manual.
* Si un nodo de acción de recorrido activado añade un miembro a un grupo de compras, y esto va seguido de un trabajo de mantenimiento de un grupo de compras que elimina al mismo miembro del grupo de compras, el trabajo de mantenimiento **no elimina** ese miembro y no puede anular la asignación de la acción de recorrido.

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
| [!UICONTROL Información general] | Esta pestaña es la predeterminada y muestra el [panel Grupos de compras](../dashboards/buying-groups-dashboard.md). |
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

La puntuación de integridad se utiliza para determinar si el grupo de compras está completo, lo que significa que tiene los miembros adecuados asignados a las funciones y está listo para utilizarse en un recorrido de cuentas. Esta puntuación es un porcentaje basado en el número de funciones dentro del grupo de compras y en cuántas funciones se han asignado con al menos un posible cliente.

Por ejemplo, si hay cuatro funciones dentro de un grupo de compras y tres de cuatro están asignadas al menos a un posible cliente, el grupo de compras está completado en un 75 %.

La puntuación de integridad del grupo de compras se vuelve a calcular cada vez que se crea o actualiza un grupo de compras.

### Puntuación de participación de grupo de compras {#engagement-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score"
>title="Puntuación de participación"
>abstract="Las puntuaciones de participación determinan el nivel de participación para comprar miembros del grupo."

La puntuación de participación en el grupo de compras es un número que determina la participación de los miembros de un grupo de compras, en función de las actividades que realizan.

* El cálculo de puntuación de participación comienza en cuanto se genera el grupo de compras.
* Cualquier actividad entrante realizada por los miembros del grupo de compras en los últimos 30 días se utiliza para calcular la puntuación.
* Con la ventana de 30 días y a medida que las actividades caduquen, la puntuación podría bajar.
* Hay un límite de frecuencia diario de 20 para cada actividad. Si un miembro de un grupo de compras realiza la misma actividad más de 20 veces al día, el recuento de la actividad se limita a 20 y no a un número superior.
* La puntuación mostrada se redondea. Por ejemplo, una puntuación de 75,89999 se muestra como 76.

+++Actividades utilizadas para la puntuación

| Nombre de la actividad | Descripción | Tipo de participación | Recuento máximo de frecuencia diaria | Peso de la actividad |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visitar página web] | Un miembro visita una página web | Web | 20 | 40 |
| [!UICONTROL Rellenar formulario] | Un miembro rellena y envía un formulario en una página web | Web | 20 | 40 |
| [!UICONTROL Hacer clic en vínculo] | Un miembro hace clic en un vínculo de una página web | Web | 20 | 40 |
| [!UICONTROL Abrir correo electrónico] | Un miembro abre un correo electrónico | Correo electrónico | 20 | 30 |
| [!UICONTROL Hacer clic en correo electrónico] | Un miembro hace clic en un vínculo de un correo electrónico | Correo electrónico | 20 | 30 |
| [!UICONTROL Abrir correo electrónico de ventas] | Un miembro abre un correo electrónico de ventas | Correo electrónico | 20 | 30 |
| [!UICONTROL Hacer clic en correo electrónico de ventas] | Un miembro hace clic en un vínculo de un correo electrónico de ventas | Correo electrónico | 20 | 30 |
| [!UICONTROL Momento interesante] | Un miembro experimenta un momento interesante | Revisado | 20 | 60 |
| [!UICONTROL Pulsación de notificación push] | Un miembro recibe una notificación push | Dispositivo móvil | 20 | 30 |
| [!UICONTROL Actividad de aplicación móvil] | Un miembro realiza una actividad en una aplicación móvil | Dispositivo móvil | 20 | 30 |
| [!UICONTROL Sesión de aplicación móvil] | Un miembro está activo en una sesión de aplicación móvil | Dispositivo móvil | 20 | 30 |
| [!UICONTROL Completar formulario de anuncios de posibles clientes en Facebook] | Un miembro rellena y envía un formulario de anuncios de posibles clientes en una página de Facebook | Social | 20 | 30 |
| [!UICONTROL Hacer clic en llamada a la acción RTP] | Un miembro hace clic en una llamada a la acción personalizada | Web | 20 | 60 |
| [!UICONTROL Ver mensaje en la aplicación] | Un miembro ve un mensaje en la aplicación | Dispositivo móvil | 20 | 30 |
| [!UICONTROL Pulsación de un mensaje en la aplicación] | Un miembro pulsa un mensaje en la aplicación | Dispositivo móvil | 20 | 30 |
| [!UICONTROL Suscribirse a SMS] | Un miembro se suscribe a las comunicaciones por SMS | SMS | 20 | 90 |
| [!UICONTROL Responder a correo electrónico de ventas] | Un miembro responde a un correo electrónico de ventas | Correo electrónico | 20 | 30 |
| [!UICONTROL Ha participado en un diálogo] | Un miembro ha participado en un diálogo de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha interactuado con un documento en un diálogo] | Un miembro interactúa con un documento en un diálogo de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha programado una reunión en un diálogo] | Un miembro programa una cita en un diálogo de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha alcanzado la meta del diálogo] | Un miembro alcanza una meta en un diálogo de Dynamic Chat |  | 20 | 90 |
| [!UICONTROL Ha respondido a una encuesta del seminario web] | Un miembro responde a una encuesta en un evento del seminario web | Chat | 20 | 90 |
| [!UICONTROL Ha hecho clic en la llamada a la acción en un seminario web] | Un miembro hace clic en un vínculo de llamada a la acción en un evento de seminario web | Llamar | 20 | 30 |
| [!UICONTROL Descargas de recursos en el seminario web] | Un miembro descarga un archivo o un recurso en un evento de seminario web | Evento | 20 | 60 |
| [!UICONTROL Formula preguntas en un seminario web] | Un miembro formula preguntas en un evento de un seminario web | Evento | 20 | 60 |
| [!UICONTROL Ha asistido a un evento] | Un miembro asistió a un evento | Evento | 20 | 60 |
| [!UICONTROL Ha entablado un diálogo con un agente] | Un miembro entabla un diálogo de Dynamic Chat con un agente | Chat | 20 | 90 |
| [!UICONTROL Ha hecho clic en un vínculo en el chat de un diálogo] | Un miembro hace clic en un vínculo de un diálogo de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha participado en un flujo conversacional] | Un miembro participa en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha programdo una reunión en un flujo conversacional] | Un miembro programa una cita en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Se ha alcanzado una meta del flujo conversacional] | Un miembro alcanza una meta en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha interactuado con un documento en un flujo conversacional] | Un miembro interactúa con un documento en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha interactuado con un agente en un flujo conversacional] | Un miembro interactúa con un agente en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Ha hecho clic en un vínculo del chat en un flujo conversacional] | Un miembro hace clic en un vínculo de un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Hacer clic en vínculo en SMS V2] | Un miembro hace clic en un vínculo de un mensaje SMS | SMS | 20 | 90 |

>[!NOTE]
>
>Las actividades de puntuación de la participación se registran en el [registro de actividades de una persona](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} de Marketo Engage.

+++

#### Ponderación {#engagement-score-weighting}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score_weighting"
>title="Ponderación de puntuación de participación"
>abstract="Use la ponderación para personalizar el cálculo de la puntuación de participación."

Los usuarios pueden asignar _ponderación_ a cada rol en la [plantilla de roles](./buying-groups-role-templates.md) para asignar diferentes ponderaciones a un rol.

![Establezca la ponderación en cada función de la plantilla de funciones](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Cada nivel de ponderación se traduce en un valor, que se utiliza para calcular la puntuación de participación:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Menor] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Importante] = 80
* [!UICONTROL Vital] = 100

Una plantilla de funciones con tres funciones ponderadas como _[!UICONTROL vitales]_, _[!UICONTROL importantes]_ y _[!UICONTROL normales]_ se convierte en los siguientes porcentajes ponderados:

| Función | Ponderación | Valor del sistema | Cálculo del valor | Porcentaje |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Persona responsable de la toma de decisiones | Vital | 100 | 100/240 | 41,67 % |
| Marcador de tendencias | Importante | 80 | 80/240 | 33,33 % |
| Profesional | Normal | 60 | 60/240 | 25 % |
|               | Total | 240 |                   |           |

#### Ejemplo de cálculo

El siguiente ejemplo ilustra el cálculo de la puntuación de participación utilizando el porcentaje de ponderación de función descrito, el recuento de actividades entrantes para cada miembro del grupo de compras y un límite diario de 20 para cada evento (si se ha producido varias veces).

| Función | Miembro | Tipo de actividad | Recuento de ayer | Recuento de hoy | Cálculo | Puntuación total |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Persona responsable de la toma de decisiones | Adam | Sitio web visitado | 37 | 15 | 20 + 15 | 35 |
|               |          | Se hizo clic en el correo electrónico | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Marcar | Sitio web visitado | 5 | 3 | 5 + 3 | 8 |
|               |          | Se hizo clic en el correo electrónico | 1 | 1 | 1 + 1 | 2 |
|               |          | Pub. descargada | 3 | 2 | 3 + 2 | 5 |
| **Puntuación total de encargados de tomar decisiones** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Marcador de tendencias | John | Sitio web visitado | 19 | 9 | 19 + 9 | 28 |
| **Puntuación total de marcadores de tendencias** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Profesional | Bob | Se hizo clic en el correo electrónico | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Se hizo clic en el correo electrónico | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Se hizo clic en el correo electrónico | 1 | 1 | 1 + 1 | 2 |
|               |          | Sitio web visitado | 1 | 7 | 1 + 7 | 8 |
|               |          | Pub. descargada | 1 | 2 | 1 + 2 | 3 |
| **Puntuación total de los profesionales** |         |             |                 |             |      | **17** |

La puntuación de participación final se calcula aplicando la ponderación para cada una de las puntuaciones de función:

| Función | Puntuación total de funciones | Ponderación de la función % | % de puntuación de ponderación X |
|-------------- |---------------- |------------- |---------------- |
| Personas responsables de la toma de decisiones | 52 | 41,67 % | 21,67 |
| Personas con influencia en medios sociales | 28 | 33,33 % | 9,33 |
| Profesionales | 17 | 25 % | 4,25 |
| **Puntuación de participación final** |                |             | **35,25** |

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
