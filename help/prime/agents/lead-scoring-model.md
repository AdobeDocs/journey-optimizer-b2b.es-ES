---
title: Crear modelos de puntuación personalizados
description: Cree, previsualice y publique modelos de puntuación de posibles clientes personalizados en Journey Optimizer B2B Prime con la habilidad Scoring Studio en la interfaz de chat del Ayudante de IA.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-25T21:20:26.754Z'
TQID: 'https://experienceleague.adobe.com/-D5EaJ-3GQ5iwaE6hChscZGEdflKmZ3tdp6VUNuPjWk'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 95f506e5ec59996bf4af53151cd0553d23b19082
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 7%

---

# Crear modelos de puntuación personalizados

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_scoring_studio"
>title="Puntuación de Studio"
>abstract="Utilice la habilidad de puntuación de Studio para crear, configurar y publicar modelos de puntuación de posibles clientes personalizados a través de la interfaz de chat del Asistente de IA."

La aptitud [_Scoring Studio_](./skills.md#scoring-signals) en [!DNL Adobe Journey Optimizer B2B Prime] proporciona una solución de puntuación de posibles clientes nativa de IA que le permite crear, configurar y publicar modelos de puntuación de posibles clientes. El estudio combina un flujo de trabajo impulsado por el agente con una interfaz de usuario visual: puede crear modelos de puntuación mediante mensajes en lenguaje natural en la [interfaz de chat del Ayudante de IA](./chat-interface.md) o interactuando directamente con los controles de la interfaz de usuario.

* **Habilidad** - `scoring-studio`
* **Invocación**: use un comando de barra para abrir Scoring Studio. Por ejemplo: _&quot;abrir Scoring Studio.&quot;_
* **Lee/escribe en** - servicio de puntuación [!DNL Journey Optimizer B2B Prime]; lee [!DNL Marketo Engage] campos de posibles clientes y tipos de actividades

Al iniciar, el asistente de IA recupera automáticamente el contexto relevante, incluidos los tipos de actividades, los campos de posibles clientes, las listas de personas y las listas de puntuación existentes, para fundamentar sus sugerencias en los datos.

Se inició ![Scoring Studio en la interfaz de chat del Asistente de IA](./assets/scoring-studio.png){width="700" zoomable="yes"}

## Crear un modelo de puntuación {#create-model}

Al abrir Scoring Studio, el asistente de IA propone un modelo de puntuación de ejemplo relevante previamente rellenado con una lista estática y un conjunto de actividades puntuadas. Puede aceptar este punto de partida sugerido o proporcionar su propio indicador para definir un modelo personalizado.

### Previsualización del modelo {#preview-model}

Después de enviar un mensaje, el Ayudante de IA genera una vista previa del modelo antes de realizar cambios. Las superficies de previsualización:

* Dimensiones de puntuación en uso
* Atributos y actividades que se clasifican
* Listas estáticas o listas inteligentes aplicadas como segmentos
* Resumen de la meta del modelo, el segmento de destinatario y las señales principales

Puede revisar la vista previa y elegir crear el modelo basado en él, o continuar refinando a través del chat antes de finalizar.

### Estructura del modelo {#model-structure}

El modelo creado está organizado en _dimensiones_ y _señales_. Puede configurar cada señal mediante el panel de propiedad en la interfaz de usuario de:

* **Tipo de señal** — Basada en actividades o en atributos
* **Actividad o atributo**: El elemento específico que se va a puntuar
* **Parámetros de señal** — Ajustes ajustables para la señal

Puede crear y configurar modelos completamente mediante el Asistente de IA utilizando lenguaje natural, o interactuar directamente con los controles de la interfaz de usuario.

## Publicar un modelo de puntuación {#publish-model}

Cuando finalice el modelo, indique al asistente de IA que lo publique. El proceso de publicación gestiona automáticamente lo siguiente:

| Paso | ¿Qué sucede? |
|---|---|
| **Compilación de reglas** | Todas las reglas de puntuación se compilan y validan |
| **Creación de tarea de puntuación** | Se crea una tarea de puntuación programada y se configura para ejecutarse diariamente |

Después de la publicación, también tiene la opción de almacenar en déclencheur una ejecución manual para procesar las puntuaciones inmediatamente.

## Ver resultados de puntuación {#view-results}

Cuando finaliza una ejecución de puntuación, las puntuaciones se vuelven a escribir en [!DNL Marketo Engage] mediante el proceso de importación de posibles clientes. Una vez completada la importación, las puntuaciones actualizadas se pueden comprobar directamente en [!DNL Marketo Engage].

Después de cada ejecución, puede ver un resumen de los resultados que muestra lo siguiente:

* Cuántas personas se puntuaron
* La puntuación individual cambia por persona

Hay disponible un registro de auditoría para revisar los detalles adicionales de la ejecución.
