---
title: Grupos de compras
description: Descubra cómo los grupos de compras en Journey Optimizer B2B Edition pueden aumentar la eficacia del marketing al identificar y segmentar miembros para sus listas de cuentas.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 08c8684d138005d4560941c7d89d6771472bcd60
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Grupos de compras

Para las actividades de ventas y marketing B2B, las cuentas son clave para cualquier estrategia. Cada cuenta tiene un grupo de personas asociadas a ella y estas personas pueden ser empleados de la cuenta o contratistas que trabajen con la cuenta. Las cuentas son jerárquicas y los productos pueden venderse en diferentes niveles de jerarquía. Por ejemplo, Adobe Experience Platform podría venderse a nivel corporativo a una cuenta de nivel superior, mientras que Adobe Photoshop podría venderse a una cuenta que represente a una división o departamento dentro de una organización, como un departamento de diseño dentro de una corporación más grande.

![Diagrama de funciones de cuenta](assets/account-roles-diagram.png){width="800"}

En la cuenta podría haber un subconjunto de personas que forman el _grupo de compras_. Estas son las personas que finalmente toman la decisión de compra, por lo que necesitan una atención especial del experto en marketing y podrían necesitar una información diferente que las demás personas asociadas con la cuenta. Los grupos de compra pueden incluir un grupo diferente de personas para diferentes líneas u ofertas de productos. Por ejemplo, un producto de ciberseguridad suele requerir la aprobación de una compra por parte de un director de información o de seguridad, y un representante del departamento jurídico, pero un producto de seguimiento de errores suele tener como miembros del grupo de compras a un vicepresidente de ingeniería y un director de TI.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea la descripción general del vídeo](#overview-video)

## Componentes principales

Puede aumentar la eficacia del marketing estableciendo grupos de compras en Journey Optimizer B2B Edition que identifiquen a los miembros que faltan en las listas de cuentas de destino en función de las soluciones que deben vender sus equipos de ventas. Antes de que usted y su equipo de marketing empiecen a crear sus grupos de compra, asegúrese de haber definido los componentes clave. Estos componentes son esenciales para alcanzar las metas y objetivos empresariales.

| Componente | Finalidad |
| --------- | ------- |
| Interés de la solución | Este componente proporciona la respuesta a lo siguiente: <ul><li>Como organización de marketing, ¿qué vende?</li><li>¿Qué producto o colección de productos quiere vender?</li></ul>  **_Ejemplo:_** Venta cruzada del nuevo Producto X a clientes existentes |
| Público de cuenta | Este componente proporciona la respuesta a lo siguiente: <ul><li>¿A quién le está vendiendo?</li><li>¿Cuál es la lista de cuentas a las que se dirige?</li></ul> **_Ejemplo:_** Segmento de cuenta definido por cuentas con el Producto Y que tienen ingresos superiores a 1M |
| Plantillas de función del grupo de compras | Este componente proporciona la respuesta a lo siguiente: <ul><li>¿A qué funciones se está dirigiendo?</li><li>¿Qué conjunto de reglas se utiliza para determinar quién está asignado a la compra de funciones de grupo?</li></ul>  **_Ejemplo:_** Asigne una persona con título CMO a la función Responsable de tomar decisiones |
| Fases del grupo de compras | (Opcional) Este componente proporciona la respuesta a: ¿Cómo realiza el seguimiento del grupo de compra de cara al éxito o al fracaso? |

## Flujo de trabajo del grupo de compras

1. Crear grupos de compra.

   * Definir [interés de solución](./solution-interests.md) y [plantilla de rol](./buying-groups-role-templates.md)
   * [Cree el grupo comprador](./buying-groups-create.md#create-buying-groups) y asigne [etapas del grupo comprador](./buying-group-stages.md).

1. Identificar personas desaparecidas.

   Analice el grupo de compra mediante filtros.

   **_Ejemplo:_** Falta la función de responsable de la toma de decisiones y la puntuación de integridad es &lt; 50

1. Completar las definiciones de grupos de compra.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Utiliza el grupo de compras y tus recorridos de cuenta.

## Ver grupos y componentes de compra

En el panel de navegación de la izquierda, expanda **[!UICONTROL Cuentas]** y haga clic en **[!UICONTROL Comprar grupos]**.

La página _[!UICONTROL Grupos de compras]_ está organizada en pestañas:

| Tabulación | Descripción |
| --- | ----------- |
| [!UICONTROL Información general] | Esta pestaña es la predeterminada y muestra el [panel Grupos de compras](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Examinar] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compras existentes. </li><li>Buscar por nombre de grupo de compras. </li><li>Filtrar por interés de solución. </li><li>Profundizar en los detalles del grupo de compras. </li><li>Cree un grupo de compras. </li></ul> |
| [!UICONTROL Intereses de la solución] | Esta pestaña admite las siguientes actividades: <ul><li>Ver la lista de grupos de compras existentes. </li><li>Buscar por nombre de grupo de compras. </li><li>Acceder y editar las propiedades de interés de la solución. </li><li>Crear una solución de interés. </li><li>Eliminar un interés de solución. </li><li>Ver y eliminar trabajos del grupo de compras. </li></ul> |
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

### Puntuación de participación de grupo de compras

La puntuación de participación en el grupo de compras es un número que determina la participación de los miembros de un grupo de compras, en función de las actividades que realizan.

* El cálculo de puntuación de participación comienza en cuanto se genera el grupo de compras.
* Cualquier actividad entrante realizada por los miembros del grupo de compras en los últimos 30 días se utiliza para calcular la puntuación.
* Con la ventana de 30 días y a medida que las actividades caduquen, la puntuación podría bajar.
* Hay un límite de frecuencia diario de 20 para cada actividad. Si un miembro de un grupo de compras realiza la misma actividad más de 20 veces al día, el recuento de la actividad se limita a 20 y no a un número superior.
* La puntuación mostrada se redondea. Por ejemplo, una puntuación de 75,89999 se muestra como 76.

+++Actividades utilizadas para la puntuación

| Nombre de la actividad | Descripción | Tipo de participación | Recuento máximo de frecuencia diaria | Peso de la actividad |
| --- | --- | --- | --- | --- |
| Registrarse para el evento | Registra un evento asociado a una campaña | Evento | 20 | 60 |
| Asistir a un evento | Asiste a un evento de campaña | Evento | 20 | 90 |
| Abrir correo electrónico | Abre un correo electrónico | Correo electrónico | 20 | 30 |
| Hacer clic en el correo electrónico | Hace clic en un vínculo de un correo electrónico | Correo electrónico | 20 | 30 |
| Abrir correo electrónico de ventas | Abre un correo electrónico de ventas | Correo electrónico | 20 | 30 |
| Hacer clic en el correo electrónico de ventas | Hace clic en un vínculo de un correo electrónico de ventas | Correo electrónico | 20 | 30 |
| Momento interesante | Tiene un momento interesante | Revisado | 20 | 60 |
| Pulsar la notificación de inserción | Recibe una notificación push | Dispositivo móvil | 20 | 30 |
| Actividad en la aplicación móvil | Realiza una actividad en una aplicación móvil | Dispositivo móvil | 20 | 30 |
| Sesión en la aplicación móvil | Está activo en la sesión de la aplicación móvil | Dispositivo móvil | 20 | 30 |
| Completar formulario de anuncios de Facebook para clientes potenciales | Rellena y envía un formulario de anuncios de posibles clientes en una página de Facebook | Social | 20 | 30 |
| Haga clic en la llamada a la acción de RTP | Hace clic en una llamada a la acción personalizada | Web | 20 | 60 |
| Ver mensaje dentro de la aplicación | Visualiza un mensaje en la aplicación | Dispositivo móvil | 20 | 30 |
| Pulsar mensaje dentro de la aplicación | Pulsa un mensaje dentro de la aplicación | Dispositivo móvil | 20 | 30 |
| Suscribirse a SMS | Se suscribe a las comunicaciones por SMS | SMS | 20 | 90 |
| Responder al correo electrónico de ventas | Responde al correo electrónico de ventas | Correo electrónico | 20 | 30 |
| Participó en un diálogo | Interactúa con un cuadro de diálogo de Dynamic Chat | Chat | 20 | 90 |
| Interactuó con un documento en el diálogo | Interactúa con un documento en un diálogo de Dynamic Chat | Chat | 20 | 90 |
| Programó una reunión en el diálogo | Programa una cita en un diálogo de Dynamic Chat | Chat | 20 | 90 |
| Alcanzó el objetivo del diálogo | Alcanza un objetivo en un cuadro de diálogo de Dynamic Chat |  | 20 | 90 |
| Ha respondido a una encuesta en el seminario web | Responde a una encuesta en un evento del seminario web | Chat | 20 | 90 |
| Ha hecho clic en llamada a la acción en el seminario web | Hace clic en un vínculo de llamada a la acción en un evento de seminario web | Llamar | 20 | 30 |
| Descargas de recursos en el seminario web | Descarga un archivo o recurso en un evento de seminario web | Evento | 20 | 60 |
| Realiza preguntas en el seminario web | Hace preguntas en un evento de seminario web | Evento | 20 | 60 |
| Asistió al evento | No ha asistido a un evento | Evento | 20 | 60 |
| Interactuó con un agente en el diálogo | Interactúa con un agente en un cuadro de diálogo de Dynamic Chat | Chat | 20 | 90 |
| Ha hecho clic en un vínculo del chat en el diálogo | Hace clic en un vínculo de un cuadro de diálogo de Dynamic Chat | Chat | 20 | 90 |
| Ha participado en un flujo conversacional | Interactúa con un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| Ha programado una reunión en el flujo conversacional | Programa una cita en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| Se ha alcanzado el objetivo del flujo conversacional | Alcanza un objetivo en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| Ha interactuado con un documento en el flujo conversacional | Interactúa con un documento en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| Ha interactuado con un agente en el flujo conversacional | Se involucra con un agente en un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| Ha hecho clic en un vínculo del chat en el flujo conversacional | Hace clic en un vínculo de un flujo conversacional de Dynamic Chat | Chat | 20 | 90 |
| Hacer clic en vínculo SMS V2 | Hace clic en un vínculo de un mensaje SMS | SMS | 20 | 90 |

>[!NOTE]
>
>Las actividades de puntuación de la participación se registran en el [registro de actividades de una persona](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} de Marketo Engage.

+++

#### Ponderación

Los usuarios pueden asignar una _ponderación_ a cada función en la plantilla de funciones para asignar diferentes ponderaciones a una función a fin de calcular la puntuación de participación.

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

>[!VIDEO](https://video.tv.adobe.com/v/3452931/?learn=on&captions=spa)
