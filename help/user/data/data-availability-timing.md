---
title: Disponibilidad de datos y tiempo de sincronización
description: Descubra la rapidez con la que aparecen los cambios de datos en [!DNL Journey Optimizer B2B Edition] recorridos y las escalas de tiempo que son normales.
feature: Journeys, Data Management
role: User
autotag-review: '2026-10-08T18:36:33.252Z'
TQID: 'https://experienceleague.adobe.com/PA1IeRHnGWHmBtDpffzveoWIHOn99-Ctt4Y0OQb7CwE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: 095e8119-1425-57eb-9d8c-9e684f2c9771
    internal-label: Audiences
  - id: 33ca0c14-7e3b-55a1-8fd7-8a61b47da4e1
    internal-label: B2B
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: a50ad69b-1331-40e9-b634-531a085a6a54
    internal-label: Identities
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: eec185bd-7d60-4193-ba3f-da427569936a
    internal-label: Destinations
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
source-git-commit: 827c313f032d482ac2b0a5fa8f41d6506e67b9cb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%
---
# Disponibilidad de datos y tiempo de sincronización {#data-availability}

Utilice este tema para comprender la rapidez con la que aparecen los cambios de datos en los recorridos de [!DNL Adobe Journey Optimizer B2B Edition] y las escalas de tiempo que son normales. Conocer el tiempo esperado le ayuda a diseñar los recorridos en consecuencia y a reconocer cuándo se espera un retraso.

## Tiempos de espera previstos

| Tipo de datos | Disponibilidad típica |
| --- | --- |
| [Pertenencia a audiencia](#daily-refresh) | Hasta 24 horas (ciclo diario) |
| [Cambios en la cuenta y la relación con la persona](#daily-refresh) | Hasta 24 horas (ciclo diario) |
| [Datos de [!DNL Experience Platform] a [!DNL Journey Optimizer B2B Edition]](#platform-sync) | Hasta 30 minutos (tiempo casi real) |
| [Datos de [!DNL Journey Optimizer B2B Edition] a [!DNL Experience Platform]](#platform-sync) | Hasta cuatro horas (microlotes) |
| [Eventos de actividad, como clics y aperturas](#activity-and-actions) | Hasta cuatro horas |
| [[!DNL Marketo Engage] agregar o quitar lista](#activity-and-actions) | En 30 minutos (tiempo casi real) |
| [Eventos generados por Journey Optimizer B2B Edition](#activity-and-actions) | Solo se puede usar en audiencias por lotes |
| [Población de audiencia de LinkedIn](#linkedin-timing) | Mismo día a 36-40 horas (peor caso) |

## Datos de audiencias y relaciones {#daily-refresh}

[!DNL Journey Optimizer B2B Edition] evalúa el abono a audiencia de persona y cuenta una vez al día, activado por un programador de trabajos por lotes. Como resultado:

* Las cuentas o personas que hayan cumplido los requisitos para una audiencia pueden participar en un recorrido en un plazo de 24 horas desde que cumplen los requisitos.
* Los cambios en los criterios de audiencia se aplican en el siguiente ciclo diario de evaluación.
* Si una cuenta cumple los requisitos para una audiencia hoy pero aún no ha entrado en el recorrido, espere hasta que se complete el siguiente ciclo diario antes de investigar.
* Cuando cambia la asociación de cuentas de una persona, por ejemplo cuando un contacto se mueve a una cuenta diferente, la actualización de la relación se propaga en un plazo de 24 horas a través del ciclo de sincronización diario. Los recorridos que dependen de la pertenencia a una cuenta reflejan la relación actualizada después del siguiente ciclo diario. No es necesario realizar ninguna acción.

>[!TIP]
>
>Diseñe recorridos con el entendimiento de que el abono a audiencias se actualiza diariamente, no en tiempo real. Si necesita respuestas casi en tiempo real, use [déclencheur basados en eventos](../journeys/listen-for-event-nodes.md) en lugar de entradas basadas en audiencias.

## Sincronización de datos con [!DNL Experience Platform] {#platform-sync}

[!DNL Experience Platform] es el almacén de datos principal para cuentas, personas y oportunidades, y [!DNL Journey Optimizer B2B Edition] posee recorridos, compra grupos y compra roles de grupo. [Más información sobre la arquitectura](../about-journey-optimizer-b2b-edition.md#high-level-architecture).

Los datos se mueven entre los dos sistemas en cada dirección a un ritmo diferente:

* **[!DNL Experience Platform]a[!DNL Journey Optimizer B2B Edition]**: los datos se sincronizan en tiempo casi real y pueden tardar hasta 30 minutos.
* **[!DNL Journey Optimizer B2B Edition]a[!DNL Experience Platform]**: los datos se sincronizan en microlotes y pueden tardar hasta cuatro horas.

## Eventos de actividad y acciones de recorrido {#activity-and-actions}

El tiempo para los datos de actividad y las acciones de recorrido depende de cómo se muevan los datos entre sistemas:

* **Datos de actividad**: los registros de actividad de la persona, como aperturas de correo electrónico, clics en vínculos y rellenos de formularios, pueden tardar aproximadamente cuatro horas en aparecer en [!DNL Journey Optimizer B2B Edition]. Este tiempo se aplica a los datos de actividad por lotes; los déclencheur de evento de experiencia [!DNL Experience Platform] utilizan datos de flujo continuo y pueden reaccionar casi en tiempo real.
* **[!DNL Marketo Engage]acciones** - las acciones de Recorrido que llaman a [!DNL Marketo Engage] están casi en tiempo real porque son llamadas API. Por ejemplo, cuando un paso de recorrido agrega o quita una persona de una lista [!DNL Marketo], la acción suele completarse en un plazo de 30 minutos. [Más información sobre las acciones de recorrido](../journeys/action-nodes.md).
* **Acciones que pasan por[!DNL Experience Platform]**: cualquier acción que vuelva a [!DNL Experience Platform] primero se procesa por lotes, por lo que está sujeta a la temporización por lotes en lugar de a la temporización casi en tiempo real.
* **Los eventos generados por[!DNL Journey Optimizer B2B Edition]** - Eventos que [!DNL Journey Optimizer B2B Edition] genera en [!DNL Experience Platform] solo se pueden usar en audiencias por lotes.

## [!DNL LinkedIn] destinos de audiencia {#linkedin-timing}

Si el recorrido incluye una acción de destino [!DNL LinkedIn], espere la siguiente cronología después de publicar el recorrido.

| Escenario | Espera esperada |
| --- | --- |
| Las cuentas ya estaban en la audiencia cuando se publicó el recorrido | El mismo día, si el procesamiento se completa antes de la medianoche (hora local) |
| Las cuentas llegaron después de la publicación del recorrido | Hasta 24 horas |
| Las cuentas llegaron después de la primera ventana de sincronización diaria | Hasta 36-40 horas |

Es posible que los recuentos de público de [!DNL LinkedIn] no se actualicen inmediatamente. Este retardo es esperado mientras [!DNL Experience Platform] procesa y envía el archivo de audiencia a [!DNL LinkedIn]. Si el recuento de público sigue siendo 0 después de 48 horas, investigue. [Más información sobre las Audiencias coincidentes con la cuenta de LinkedIn](./linkedin-account-matched-audiences.md).
