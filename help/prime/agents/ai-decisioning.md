---
title: AI Decisioning
description: Comprenda la toma de decisiones de IA en Journey Optimizer B2B Prime, la capa de inteligencia detrás del control de tráfico de recorrido, la siguiente mejor ruta, la optimización del tiempo de envío y otras funcionalidades que reemplazan las reglas estáticas con la automatización basada en resultados.
autotag-review: '2026-07-23T00:13:49.629Z'
TQID: 'https://experienceleague.adobe.com/vAu9C6Erjr-0TIJ18jQnR209Ed2xfLl9P3Nq2fPTs9c'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c3d6e661-d372-4e98-9fd9-eac771e7e4eeid: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 120afb1109e550fc65c2fc5a01680f2d7d2e2345
workflow-type: tm+mt
source-wordcount: 814
ht-degree: 2%

---


# decisiones de IA

La toma de decisiones de IA es la capa de inteligencia detrás de Adobe Journey Optimizer B2B Prime. En lugar de crear previamente cada rama como regla estática, AI Decisioning evalúa continuamente el contexto de un perfil, incluida la pertenencia al recorrido, el historial de participación, las puntuaciones de intención y la conducta en tiempo real, para determinar la siguiente mejor acción o ruta para esa persona.

Esta evaluación continua mueve la orquestación de las reglas estáticas a la automatización impulsada por resultados: en lugar de definir cada condición por adelantado, se describe el resultado que se desea y el sistema determina cómo llegar allí para cada persona.

## Competencias {#capabilities}

La toma de decisiones de IA se compone de las siguientes capacidades:

| Capacidad | Lo que decide |
|---|---|
| [control de tráfico de Recorrido](../marketing/journey-traffic-control.md) | En qué recorrido debería estar una persona en este momento. Cuando una persona cumple los requisitos para más de un recorrido, el control de tráfico de recorrido los redirige en el momento en que cambia su perfil o conducta, en lugar de dejarlos en un camino que ya no encaja. |
| [Siguiente mejor ruta](../marketing/next-best-path.md) | La ruta más adecuada para una persona dentro de un recorrido. En lugar de codificar las condiciones de filtro, se describe la intención en lenguaje natural, y el sistema enruta a cada persona a la ruta que mejor coincida en el momento adecuado. |
| [Optimización del tiempo de envío](../marketing/email-send-time-optimization.md) | La mejor ventana de envío para cada destinatario, en función de la participación histórica, en lugar de una programación fija para todos. |
| Contenido contextual | Variantes de correo electrónico personalizadas generadas automáticamente a partir de una información breve de contenido, para usarlas como un único recurso de correo electrónico personalizado dentro de recorrido. _Próximamente._ |
| [Brand Concierge](https://experienceleague.adobe.com/es/docs/brand-concierge/content/home){target="_blank"} | Enrutamiento y respuesta conversacional en tiempo real, como chat y asistencia en vivo. Brand Concierge requiere derechos de producto adicionales. |

Algunas de estas funcionalidades solucionan diferentes problemas dentro del mismo recorrido. El control de tráfico de recorrido decide qué recorrido gana la prioridad cuando varios recorridos compiten para atraer a la misma persona al mismo tiempo. Las otras capacidades deciden qué sucede después de que una persona ya está en un recorrido.

## Dividir rutas y la siguiente mejor ruta {#split-paths-next-best-path}

[Las rutas divididas](../marketing/split-merge-paths-nodes.md) le permiten definir ramas de recorrido con condiciones de filtro explícitas: si una puntuación está por encima de un umbral, envíe a una persona por una ruta o, en caso contrario, envíe a otra. Esta lógica basada en reglas es precisa y totalmente auditable, pero cada nueva condición requiere una nueva rama.

El nodo [Siguiente mejor ruta](../marketing/next-best-path.md) aplica la toma de decisiones de IA al mismo problema. En lugar de un umbral fijo, el modelo evalúa la participación, el perfil, el interés del producto y la fase de funnel juntos, predice el mejor resultado para cada persona y selecciona la ruta óptima automáticamente.

## Entradas de datos {#data-inputs}

La toma de decisiones de IA se basa en las siguientes categorías de datos:

| Categoría | Ejemplos |
|---|---|
| Demográfico y firmográfico | Cargo, sector y tamaño de la empresa |
| Psicográfico | Puntuación, urgencia y prioridad de posibles clientes |
| Participación | Puntuación, nivel, tendencia, última actividad y canal |
| Intención | Intento de producto o palabra clave, agrupados en bloques altos, medios o bajos |
| Persona | Función en el trato, el cargo y la personalidad |

## Cadencia de evaluación {#evaluation-cadence}

La toma de decisiones de IA utiliza dos horarios de evaluación diferentes. El perfil subyacente de una persona se vuelve a calcular en un lote nocturno. La decisión en sí se aplica en tiempo real en cada interacción, utilizando lo que indique el perfil nocturno más reciente. Por lo tanto, la parte continua de la toma de decisiones de IA describe el momento de la decisión, no la velocidad de actualización del perfil.

## Protecciones y reglas {#guardrails-rules}

Las reglas solo cubren condiciones que alguien escribió explícitamente. Cuando la realidad cae fuera de ese árbol, como una personalidad híbrida o una combinación de señales que nadie anticipó, las reglas no hacen nada hasta que alguien agrega una nueva rama. La toma de decisiones de IA puntúa a cada persona continuamente y genera una mejor acción basada en la confianza en su lugar, por lo que gestiona combinaciones para las que nadie está programado explícitamente, y mejora a medida que ve más resultados, lo que una regla nunca hace.

Las reglas son explicables e instantáneas para la auditoría, mientras que la toma de decisiones de IA tiene una puntuación de confianza en lugar de ser determinista. Por esta razón, las reglas siguen siendo la mejor herramienta cuando:

* Nunca se debe cruzar un límite de cumplimiento estricto, como suprimir los contactos de exclusión.
* No hay suficiente volumen o historial para que un modelo aprenda todavía.
* Cada decisión debe ser plenamente explicable cuando se solicite.

La mayoría de las configuraciones maduras funcionan ambas juntas: reglas como protecciones y decisiones de IA que administran todo lo que hay entre medias.

## Ventajas {#benefits}

* Menos complejidad de recorrido manual, con menos ramas de reglas que mantener.
* Experiencias más relevantes sin construir cientos de reglas.
* Mayor eficiencia en la calificación.
* Identificación más rápida de la siguiente mejor participación para cada perfil.

>[!BEGINSHADEBOX]

**Ámbito futuro: contexto de cuenta y grupo de compra**

No disponible hoy en día en Journey Optimizer B2B Prime. La toma de decisiones de IA está planificada para extenderse más allá del perfil individual a:

* Contexto de cuenta: las señales a nivel de compañía y cuenta como entrada de toma de decisiones.
* Señales de grupo de compra: función en el acuerdo, estado del responsable de la toma de decisiones o del profesional y participación acumulada en todos los participantes en una decisión de compra.
* Organización de recorridos a nivel de cuenta: decisiones de enrutamiento y contenido tomadas para la cuenta o el grupo de compra como unidad, con control de tráfico de recorrido coordinado entre las distintas personas involucradas.

>[!ENDSHADEBOX]
