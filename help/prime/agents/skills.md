---
title: Aptitudes de asistente de IA
description: 'Revise las habilidades del asistente de IA en Journey Optimizer B2B Prime: flujos de trabajo empaquetados para programas, recorridos, audiencias, puntuación, contenido y optimización del tiempo de envío.'
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-24T23:55:36.649Z'
TQID: 'https://experienceleague.adobe.com/iIi07OBWKxxa-oW-A6VrlkoTS02kmCx8kfMaCe-C-4o'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 4632a06ce5a17713fdcaecf6eac8c051bc984e28
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 7%

---

# Aptitudes de asistente de IA

Una _aptitud_ es un flujo de trabajo empaquetado que el agente sabe cómo ejecutar: los componentes básicos del menú `/` y de las solicitudes en lenguaje natural. Cada aptitud agrupa instrucciones paso a paso y las herramientas específicas necesarias para un trabajo (por ejemplo, &quot;publicar un recorrido&quot;, &quot;comparar dos listas de personas&quot;, &quot;crear un modelo de puntuación&quot;).

>[!NOTE]
>
>Cada aptitud se clasifica de acuerdo con si la aptitud muta el estado [!DNL Journey Optimizer B2B Prime] o [!DNL Marketo Engage] (**Write**), solo genera/analiza (**Read**) o si tiene funciones de consulta y mutación de igual a igual (**Read+Write**).

## Programas y planificación {#programs-planning}

| Aptitud | Qué hace | Acceso | Superficie del producto | Impacto / Flujo de datos |
|---|---|---|---|---|
| `falco-program-creation` | Creación de programas de [!DNL Journey Optimizer B2B Prime] de extremo a extremo: programas, subcarpetas, tokens, listas y recorridos. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime]. Ver _[Crear un programa a partir de una breve](./program-from-brief.md)_. |
| `adapt-program` | Generar historias de migración de [!DNL Marketo Engage] programas para la adaptación [!DNL Journey Optimizer B2B Prime]. | Lectura | [!DNL Journey Optimizer B2B Prime] | Lee [!DNL Marketo Engage], escribe [!DNL Journey Optimizer B2B Prime] |
| `folder-creation` | Cree carpetas organizativas en el árbol de recursos. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `program-creation` *(Programas de compilación)* | Cree programas de Marketo a partir de una información de campaña. | Escritura | [!DNL Marketo Engage] | Lee y escribe [!DNL Marketo Engage] |
| `program-planning` *(Planificar campañas)* | Transforme informes en documentos de configuración/implementación. | Lectura | [!DNL Marketo Engage] | Lee [!DNL Marketo Engage] |
| `program-qa` *(Validar programas)* | Validar/auditar programas (solo reglas, plan de prueba o resumen). | Lectura | [!DNL Marketo Engage] | Lee [!DNL Marketo Engage] |

## Recorridos {#journeys}

| Aptitud | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `journey-creation` | Cree y edite recorridos de persona a partir del lenguaje natural. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `journey-edit-dates` | Cambiar la fecha de inicio o finalización de un recorrido sin publicarlo. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `journey-publish` | Publicar/iniciar/programar recorridos de personas. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `journey-stop` | Abortar, cerrar, parar, detener o matar recorridos. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `journey-reentry` | Configurar la reentrada: permitir/no permitir, reutilización, máximo de entradas. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `journey-trafficcontrol` | Ejecute una simulación de control de tráfico que muestre el enrutamiento de perfiles. | Lectura | [!DNL Journey Optimizer B2B Prime] | Lee [!DNL Journey Optimizer B2B Prime] (simulación) |
| `journey-observability` | Depuración/monitorización de la progresión: rutas, tiempo, divisiones, paradas, permanencia. | Lectura | [!DNL Journey Optimizer B2B Prime] | Lee [!DNL Journey Optimizer B2B Prime] + [!DNL Marketo Engage] (comprobación de lista estática) |

## Audiencias y personas {#audiences-people}

| Aptitud | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `audience-creation` | Adaptar una lista inteligente [!DNL Marketo Engage], crear una lista de personas o agregar o actualizar reglas. | Escritura | [!DNL Journey Optimizer B2B Prime] | Lee [!DNL Marketo Engage] + lee/escribe [!DNL Journey Optimizer B2B Prime].  Ver _[Crear audiencias para programas](./audience-creation.md)_. |
| `people-list-comparison` | Comparar listas de dos personas y mostrar miembros superpuestos. | Lectura | [!DNL Journey Optimizer B2B Prime] | Lee [!DNL Journey Optimizer B2B Prime] |
| `import-leads` | Inspeccionar la calidad de los datos CSV y confirmar las importaciones en [!DNL Marketo Engage]. | Lectura y escritura | Ambos | Lee y escribe [!DNL Marketo Engage] |
| `lead-investigation` *(investigar posibles clientes)* | Investigue la actividad, puntuación, calificación y ciclo de vida de un posible cliente. | Lectura | [!DNL Marketo Engage] | Lee [!DNL Marketo Engage] |

## Contenido y canales {#content-channels}

| Aptitud | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `content-personalization` | Examinar/previsualizar plantillas y editar contenido/generar variantes. | Lectura y escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `asset-tokens` | Token completo CRUD en programas/carpetas/recorridos. | Lectura y escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `fcs-channels` | Búsquedas de canal y CRUD + publicar/detener/eliminar. | Lectura y escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |

## Puntuación y señales {#scoring-signals}

| Aptitud | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `scoring-studio` | Enumere u obtenga modelos de puntuación y créelos o publíquelos. | Lectura y escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] (servicio de puntuación); lee [!DNL Marketo Engage] campos de posible cliente/tipos de actividad. Ver _[Crear modelos de puntuación personalizados](./lead-scoring-model.md)_. |
| `engagementconfiguration` | Mostrar configuración de participación y editar/actualizar ponderaciones. | Lectura y escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `intentconfiguration` | Mostrar configuración por intención y establecer/actualizar pesos. | Lectura y escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `intent-query` | Consultar y explicar las puntuaciones por intención por persona/segmento/lista. | Lectura | [!DNL Journey Optimizer B2B Prime] | Lee [!DNL Journey Optimizer B2B Prime] |

## Optimización del tiempo de envío {#sto}

| Aptitud | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `send-time-optimization` | Compruebe el estado de STO y habilite/deshabilite en un nodo de correo electrónico. | Lectura y escritura | [!DNL Journey Optimizer B2B Prime] | Lee y escribe [!DNL Journey Optimizer B2B Prime] |
| `send-time-report` | Buscar/mostrar el informe de rendimiento de STO. | Lectura | [!DNL Journey Optimizer B2B Prime] | Lee [!DNL Journey Optimizer B2B Prime] |

## Conocimiento {#knowledge}

| Aptitud | Qué hace | Acceso | Producto | Back-end (flujo de datos) |
|---|---|---|---|---|
| `product-knowledge` | Responda preguntas sobre procedimientos y conceptos a partir de la documentación de [!DNL Journey Optimizer B2B Prime] en Experience League. | Lectura | Ambos | Lee documentos externos sin datos del producto |

## Cross-back-end {#cross-backend}

Estas aptitudes abarcan más de un servidor:

- **`adapt-program`** — `gather_program_assets` lee [!DNL Marketo Engage] (`get_program`, `get_smart_campaign`, `list_emails`) y luego escribe a través de `falcomcp_create_journey` — backend clásico.
- **`audience-creation`** — lee [!DNL Marketo Engage] listas inteligentes (`get_smart_list` / `get_smart_campaign`) y luego escribe [!DNL Journey Optimizer B2B Prime] listas de personas.
- **`journey-observability`** — [!DNL Journey Optimizer B2B Prime] lecturas más `check_lead_in_marketo_static_list` [!DNL Marketo Engage] lecturas.
- **`scoring-studio`** — lee [!DNL Marketo Engage] campos de posible cliente/tipos de actividad junto con el servicio de puntuación [!DNL Journey Optimizer B2B Prime].

Todas las herramientas `falco-mcp_*` y recorrido/token/puntuación/STO/FCS llegan a [!DNL Journey Optimizer B2B Prime] servicios; CSV/programa/herramientas de posible cliente llegan a [!DNL Marketo Engage].

