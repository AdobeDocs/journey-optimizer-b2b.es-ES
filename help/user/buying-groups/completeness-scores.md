---
title: Puntuaciones de integridad para grupos compradores
description: Calcule las puntuaciones de integridad del grupo de compra mediante umbrales basados en funciones, requisitos de miembro personalizables y configuración de integridad en Journey Optimizer B2B edition.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 3%

---


# Puntuaciones de integridad {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="Puntuación de integridad"
>abstract="Las puntuaciones de integridad reflejan la alineación de la pertenencia al grupo de compra para un grupo de compra preparado para las ventas."

Una puntuación de integridad es un porcentaje que indica la forma en que un grupo de compra se rellena con los miembros necesarios en sus funciones definidas. Estas puntuaciones se basan en los umbrales de miembros de rol que configure en la plantilla roles y en el número real de miembros asignados a cada rol en el grupo comprador. Las puntuaciones resultantes ayudan a los especialistas en marketing a evaluar la preparación de las ventas e identificar lagunas en la composición del grupo de compra. El cálculo de puntuación se produce automáticamente cuando cambia la pertenencia al grupo comprador.

![Puntuaciones de finalización del grupo de compra](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

Existen dos tipos de puntuaciones de integridad:

* **Puntuación de integridad del grupo de compra** - La puntuación de integridad del grupo de compra es un porcentaje entre 0% y 100% y representa la integridad general del grupo de compra en función de los cálculos de integridad a nivel de rol.

  La puntuación de integridad del grupo de compra se muestra en la página [Detalles del grupo de compra](./buying-group-details.md). Esta puntuación proporciona una visión rápida de si el grupo comprador dispone de las partes interesadas necesarias para la participación en las ventas.

* **Puntuación de integridad de rol** - La puntuación de integridad de rol es un porcentaje para cada rol individual dentro de un grupo de compra, basado en el número de miembros asignados a ese rol.

  La puntuación de integridad de cada rol se muestra en la página de detalles del grupo de compra al editar roles y ajustar la configuración de integridad. Estas puntuaciones le ayudan a identificar qué funciones específicas necesitan miembros adicionales para alcanzar el umbral de ventas preparadas.

  La página de detalles muestra las dos primeras puntuaciones de integridad de funciones con un vínculo n_+ para cualquier función adicional. Haga clic en el vínculo para ver las puntuaciones de integridad de funciones adicionales.

Las puntuaciones de integridad reflejan el estado actual de la compra de miembros del grupo y se actualizan automáticamente a medida que se agregan o eliminan miembros. Las puntuaciones mostradas se muestran como porcentajes enteros (por ejemplo, una puntuación del 66,67 % se muestra como 67 %).

## Evaluar preparación de ventas

Adobe Journey Optimizer B2B edition equipa a los especialistas en marketing con herramientas que garantizan que los grupos de compra se alineen con los procesos de toma de decisiones reales. Puede definir grupos de compra completos utilizando umbrales de miembros de función personalizables que reflejen la metodología de ventas de su organización. Al establecer los requisitos de miembros mínimos y máximos para cada función, se establecen criterios claros para lo que constituye un grupo de compra preparado para las ventas.

La puntuación de integridad del grupo de compra proporciona una medida precisa de la preparación de ventas para el grupo. Por ejemplo, para completar una oportunidad para una solución específica, es posible que necesite al menos dos responsables de la toma de decisiones, un influenciador y al menos un profesional. El cálculo de la puntuación de integridad tiene en cuenta cada uno de estos requisitos específicos de función, y proporciona una vista de la preparación general del grupo de compra.

## Medir la efectividad del recorrido

La integridad del grupo de compra actúa como un indicador clave de rendimiento (KPI) para la eficacia del recorrido. El objetivo de un recorrido específico puede ser aumentar la integridad del grupo de compra en un determinado porcentaje o alcanzar un umbral mínimo antes de activar alertas listas para ventas.

En una empresa grande, puede identificar una persona por función. Sin embargo, es posible que esa persona no sea el contacto correcto para la venta o que necesite varios contactos en funciones críticas. Por ejemplo, una organización grande puede tener varios responsables de la toma de decisiones en tecnología de la información (TI) distribuidos entre departamentos o unidades empresariales. La identificación de un responsable de la toma de decisiones puede no ser suficiente para una venta empresarial compleja.

Después de analizar la integridad actual del grupo de compra, puede ajustar el número necesario de contactos para cada rol en la plantilla de roles. Estos ajustes le permiten ajustar su estrategia de grupo de compra en función de patrones reales y resultados de ventas.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## Cálculo de integridad de roles {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="Cálculo de integridad de roles"
>abstract="Las puntuaciones de integridad de roles se calculan como un porcentaje basado en el número de miembros asignados a un rol."

Journey Optimizer B2B edition calcula la puntuación de integridad de cada función de grupo de compra individual como un porcentaje. Base esta puntuación en la cantidad de miembros asignados al rol, en comparación con [el número requerido en la plantilla de roles](./buying-groups-role-templates.md#change-the-completeness-score-settings) para la finalización.

El cálculo de integridad de roles es un porcentaje lineal entre cero y el umbral especificado (se requieren miembros):

* Si el número de miembros asignados es **cero**, la integridad de la función es **0%**.
* Si el número de miembros asignados es **por encima o por encima del umbral**, la integridad de la función es de **100%**.
* Si el número de miembros asignados es **entre uno y el umbral**, la integridad se calcula proporcionalmente.

### Fórmula de integridad de roles

El porcentaje de finalización de la función se calcula mediante la fórmula siguiente:

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

Donde:

* `Assigned Members` = Número actual de miembros en el rol
* `Threshold` = Se ha establecido el valor necesario de los miembros en la plantilla de funciones

### Ejemplos de integridad de funciones

Los siguientes ejemplos ilustran los cálculos de integridad de funciones con diferentes configuraciones de umbral:

| Función | Miembros necesarios | Miembros asignados | Cálculo | Integridad de funciones |
|------|------------------|------------------|-------------|-------------------|
| Persona responsable de la toma de decisiones | 3 | 0 | Ninguna | 0 % |
|  |  | 1 | 1/3 × 100 | 33 % |
|  |  | 2 | 2/3 × 100 | 66 % |
|  |  | 3 | En el umbral | 100 % |
|  |  | 4 | Por encima del umbral | 100 % |
| Marcador de tendencias | 5 | 0 | Ninguna | 0 % |
|  |   | 1 | 1/5 × 100 | 20 % |
|  |   | 2 | 2/5 × 100 | 40 % |
|  |   | 3 | 3/5 × 100 | 60 % |
|  |   | 4 | 4×50 % | 80 % |
|  |   | 5 | En el umbral | 100 % |
|  |   | 6 | Por encima del umbral | 100 % |

## Cálculo de integridad del grupo de compra {#buying-group-completeness-calculation}

La puntuación de integridad del grupo de compra agrega las puntuaciones de integridad de rol individuales. Este cálculo proporciona una vista integral de la preparación del grupo de compra en todas las funciones definidas.

### Fórmula de integridad del grupo de compra

El porcentaje de finalización del grupo de compra se calcula mediante la fórmula siguiente:

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

Donde:

* `Role Completeness %` = Porcentaje de finalización de función individual (0-100%)
* `Σ` = Suma de todos los roles del grupo comprador

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->