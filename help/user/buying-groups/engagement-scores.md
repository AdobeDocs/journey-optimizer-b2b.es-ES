---
title: Puntuaciones de participación para grupos compradores
description: Obtenga información sobre la compra de puntuaciones de participación de grupos y personas, incluida la lógica de cálculo y los tipos de actividades que determinan la puntuación.
feature: Buying Groups
role: User
exl-id: 424d9598-92dd-42de-8447-3c7cebc71a73
source-git-commit: 75a53661fdfbb65e2652f3365f4c1e907f948bd7
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 24%

---

# Puntuaciones de participación {#engagement-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score"
>title="Puntuación de participación"
>abstract="Las puntuaciones de participación determinan el nivel de participación para comprar miembros del grupo."

Una puntuación de participación es un número que indica el nivel de participación de los miembros de un grupo comprador. Estas puntuaciones se basan en las actividades de los miembros del grupo comprador, las acciones ponderadas y los roles ponderados. Las puntuaciones resultantes se normalizan dentro de un inquilino (instancia) para permitir una comparación coherente y perspectivas procesables. El cálculo de puntuación comienza en cuanto se crea el grupo comprador. El sistema del centro de datos de Journey Optimizer B2B edition calcula las puntuaciones diariamente y las carga en el sistema MySQL de marketing de varios niveles (MLM) mediante el servicio de ingesta.

Existen dos tipos de puntuaciones de participación:

* **Puntuación de participación de grupo de compra**: la puntuación de participación de grupo de compra es una puntuación normalizada entre 0 y 100 y se basa en la puntuación de participación calculada a nivel de persona.

  La puntuación de participación del grupo comprador se muestra en la página [Detalles del grupo comprador](./buying-group-details.md). También puede ver los grupos de compra más comprometidos en el panel Inteligente.

  ![Grupos de compradores más comprometidos](./assets/person-engagement-score-attribute-filtering.png){width="700" zoomable="yes"}

* **Puntuación de participación de persona** - La puntuación de participación de persona se basa en las actividades de un miembro individual del grupo de compra.

  La puntuación de participación de la persona para cada miembro del grupo comprador se muestra en la página de detalles del grupo comprador [_[!UICONTROL Miembros ]_tab](./buying-group-details.md#buying-group-members). Estas puntuaciones también se muestran en páginas y paneles que incluyen miembros de mayor participación e información de contactos superpuestos.

  ![Miembros del grupo de compras más comprometidos](./assets/top-engaged-buying-group-members.png){width="550" zoomable="yes"}

>[!BEGINSHADEBOX]

La puntuación de participación de personas es un atributo que está disponible para usar para filtrar en [plantillas de roles](./buying-groups-role-templates.md#add-the-template-roles) y [nodos de división de ruta de acceso de recorrido por personas](../journeys/split-merge-paths-nodes.md#people-path-conditions).

![Acceder a las definiciones de eventos configuradas](./assets/most-engaged-buying-groups.png){width="550" zoomable="yes"}

>[!ENDSHADEBOX]

Cualquier actividad ponderada por participación realizada por los miembros del grupo comprador en los últimos 30 días se utiliza para calcular las puntuaciones. Con la ventana de 30 días, las ocurrencias de actividad caducan y las puntuaciones pueden moverse hacia abajo (la puntuación disminuye). Las puntuaciones mostradas se redondean (por ejemplo, una puntuación de 75,89999 se muestra como 76).

## Actividades utilizadas para la puntuación de participación

La puntuación del grupo de compra no es _basada en desencadenadores_. Es un proceso diario que evalúa la actividad en todos los miembros del grupo comprador y vuelve a calcular la puntuación. Las actividades usan _weights_ para informar la puntuación del grupo de compra de acuerdo con el modelo de ponderación activo, que determina cómo se ponderará cada actividad.

Hay un límite de frecuencia diario de 20 para cada actividad. Si un miembro de un grupo comprador realiza la misma actividad más de 20 veces en un solo día, el recuento de la actividad se limita a 20.

{{engagement-activities}}

<!-- old list

| Activity name | Description | Engagement type | Max daily frequency count | Activity weight |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visit Webpage]| A member visits a web page | Web | 20 | 40 |
| [!UICONTROL Fill Out Form]| A member fills and submits a form on a web page | Web | 20 | 40 |
| [!UICONTROL Click Link] | A member clicks a link on a web page | Web | 20 | 40 |
| [!UICONTROL Open Email] | A member opens an email | Email | 20 | 30 |
| [!UICONTROL Click Email] | A member clicks a link in an email | Email | 20 | 30 |
| [!UICONTROL Open Sales Email] | A member opens a sales email | Email | 20 | 30 |
| [!UICONTROL Click Sales Email] | A member clicks a link in a sales email | Email | 20 | 30 |
| [!UICONTROL Interesting Moment] | A member has an interesting moment | Curated | 20 | 60 |
| [!UICONTROL Tap Push Notification] | A member receives a push notification | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Activity] | A member performs an activity on a mobile app | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Session] | A member is active on a mobile app session | Mobile | 20 | 30 |
| [!UICONTROL Fill Out Facebook Lead Ads Form] | A member fills and submits a Lead Ads form on a Facebook page | Social | 20 | 30 |
| [!UICONTROL Click RTP Call to Action] | A member clicks a personalized call to action | Web | 20 | 60 |
| [!UICONTROL View In-App Message] | A member views an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Tap In-App Message] | A member taps an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Subscribe SMS] | A member subscribes to SMS communications | SMS | 20 | 90 |
| [!UICONTROL Reply to Sales Email] | A member replies to a sales email | Email | 20 | 30 |
| [!UICONTROL Engaged with a Dialogue] | A member engages with a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Dialogue] | A member interacts with a document in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Dialogue] | A member schedules an appointment in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Reached Dialogue Goal] | A member reaches a goal in a Dynamic Chat dialogue |  |20 | 90 |
| [!UICONTROL Responded to a poll in webinar] | A member responds to a poll in a webinar event | Chat | 20 | 90 |
| [!UICONTROL Call to action clicked in webinar] | A member clicks a call-to-action link in a webinar event | Call | 20 | 30 |
| [!UICONTROL Asset downloads in webinar] | A member downloads a file/asset in a webinar event | Event | 20 | 60 |
| [!UICONTROL Asks questions in webinar] | A member asks questions in a webinar event | Event | 20 | 60 |
| [!UICONTROL Has attended event] | A member attended an event | Event | 20 | 60 |
| [!UICONTROL Engaged with an Agent in Dialogue] | A member engages with an agent in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Dialogue] | A member clicks a link in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Engaged with a Conversational Flow] | A member engages with a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Conversational Flow] | A member schedules an appointment in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Reached Conversational Flow Goal] | A member reaches a goal in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Conversational Flow] | A member interacts with a document in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Engaged with an Agent in Conversational Flow] | A member engages with an Agent in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Conversational Flow] | A member clicks a link in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Click Link in SMS V2] | A member clicks a link in an SMS message | SMS | 20 | 90 | -->

>[!NOTE]
>
>Las actividades de puntuación de participación se registran en el registro de actividades de Marketo Engage de una persona. Puede acceder a este registro en la instancia de Marketo Engage conectada. Para obtener más información, consulte [Buscar el registro de actividad de una persona](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} en la documentación de Marketo Engage.

## Ponderación de la plantilla de función {#engagement-score-weighting}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score_weighting"
>title="Ponderación de la función de puntuación de participación"
>abstract="Use la ponderación de función para personalizar el cálculo de la puntuación de participación."

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

## Ejemplo de cálculo de puntuación

El siguiente ejemplo ilustra el cálculo de la puntuación de participación. Utiliza el porcentaje de peso de función esbozado, el recuento de actividades entrantes para cada miembro del grupo comprador y un límite diario de 20 para cada ocurrencia de evento.

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

## Lógica de puntuación

Además de la lógica de cálculo descrita en el ejemplo de cálculo, existe una normalización considerablemente compleja de las puntuaciones que se produce en el sistema, en todas las personas, en los grupos de compra y en las cuentas de la instancia. Una puntuación de participación de grupo de compra depende de las puntuaciones de participación de la persona, según la siguiente lógica ordenada:

### Lógica de cálculo de puntuación de participación de persona

1. Identifique todos los tipos de actividad _ponderados por participación_ que tengan un peso y una cuota diaria asociados, como visitas a sitios web, clics en correos electrónicos y asistencia a seminarios web.

1. Identifique todas las acciones _ponderadas en la participación_ de la persona realizadas dentro de la ventana retrospectiva de actividad, que actualmente está codificada en 30 días.

1. Normalice las ponderaciones de tipo de actividad en todas las ponderaciones de tipo de actividad _ponderadas por participación_ identificadas en el paso 1, ignorando las que no se produjeron dentro de la ventana retrospectiva.

   Este paso aprovecha la normalización de _Min-Max_ y reduce significativamente la dilución artificial del peso del tipo de actividad para un inquilino que no aprovecha la mayoría de ellos.

1. Aplique el filtrado de cuota diario por persona y tipo de actividad.

   Este paso mitiga el hecho de tener valores periféricos muy grandes al evitar que las actividades de menor valor o gran volumen distorsionen las puntuaciones.

1. Calcule la puntuación de participación de la persona sin procesar sumando la actividad diaria por tipo de actividad, multiplicándola por el peso asociado y sumando los resultados de todos los días de la ventana retrospectiva.

1. Use una transformación de _Transformación de energía_ (Raíz cuadrada) para estabilizar la variación mediante la reducción de posibles periféricos.

   Estas transformaciones ayudan a reducir la asimetría y a hacer que los patrones de los datos sean más lineales.

1. Aplique una transformación adicional de _normalización escalada_ para asegurarse de que las puntuaciones aprovechan todo el intervalo de 0 a 100.

### Lógica de cálculo de puntuación de participación del grupo comprador

1. Aplique un peso normalizado a cada miembro del grupo comprador por función, según el peso configurado en la plantilla de funciones.

1. Normalice el peso de rol del grupo comprador para cada grupo comprador.

   Esta normalización evita una dilución innecesaria de la ponderación de función si un grupo comprador no utiliza todas las funciones.

1. Sume todas las puntuaciones de participación de personas de miembros de grupos compradores multiplicando la puntuación de participación de personas por el peso de rol normalizado de la persona y sume todas ellas.

1. Aplique una transformación _Power Transformation_ (Square Root) para estabilizar la variación mediante la reducción de posibles periféricos, especialmente para grupos de compra muy grandes.

1. Aplique una transformación adicional de _normalización escalada_ para asegurarse de que las puntuaciones aprovechan todo el intervalo de 0 a 100.
