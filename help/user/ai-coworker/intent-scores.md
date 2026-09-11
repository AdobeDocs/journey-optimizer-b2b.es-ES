---
title: Puntuaciones por intención
description: Comprenda cómo Journey Optimizer B2B edition calcula las puntuaciones de intención a partir de la participación de la persona y la relevancia del contenido, y cómo se acumulan las puntuaciones en las cuentas.
feature: Dashboards, Intent, Intelligent Insights
role: User
autotag-review: '2026-09-11T14:56:32.307Z'
TQID: 'https://experienceleague.adobe.com/ajtUdNKafSoE1BC08imOpyflpDeAsXaQ3tdlbeYT6NU'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: e388c29d-df1e-4b47-ad27-1b14ae45776e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 2da5c7bbbadde4bbb5df82a81398ecb970165da2
workflow-type: tm+mt
source-wordcount: 1445
ht-degree: 0%

---


# Puntuaciones por intención {#intent-scores}

La puntuación por intención mide el interés que tiene una persona o cuenta por una palabra clave, un producto o una categoría de producto. Adobe Journey Optimizer B2B edition calcula la puntuación mediante aprendizaje automático que mide la similitud de significado, en lugar de utilizar reglas manuales o un sistema de puntos fijos. Cada puntuación se normaliza de 0 a 1, con números más altos que indican una intención más fuerte.

La relevancia del contenido se actualiza aproximadamente cada 12 horas y las puntuaciones por intención se vuelven a calcular diariamente. Las puntuaciones se acumulan de palabra clave a producto y de persona a cuenta. Las puntuaciones de intención aparecen en [Tablero inteligente](../dashboards/intelligent-dashboard.md) y en las páginas [detalles de la cuenta](../accounts/account-details.md), [_detalles del grupo de compra_, &#x200B;](../buying-groups/buying-group-details.md) y [detalles de la persona](../accounts/person-details.md).

![Visualización de datos por intención](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

En las siguientes secciones se explican los conceptos principales subyacentes a la puntuación por intención, el proceso continuo que mantiene las puntuaciones actualizadas, la lógica de cálculo detrás de cada puntuación y la configuración que puede configurar.

## Conceptos principales {#core-concepts}

La detección de intención mide en qué medida lo que interactúa una persona con coincide con sus productos y palabras clave, y luego valora esa similitud según la cantidad de participación de la persona. Este modelo se compone de tres entidades.

| Entidad | Descripción |
|--------|--------------|
| Persona | Persona que interactúa con el contenido abriendo correos electrónicos, visitando páginas web e interactuando con el paso del tiempo. |
| Contenido | Los correos electrónicos y las páginas web con las que se involucra una persona. Con el tiempo se agregan otros formatos, como seminarios web y campañas. |
| Taxonomía | Estructura de palabras clave, productos y categorías de productos que representa los intereses que desea medir. |

### taxonomía y actualizaciones predeterminadas {#taxonomy}

Su taxonomía, las palabras clave, los productos y las categorías con los que se mide la intención están disponibles para su uso sin necesidad de configuración.

Puede revisar y actualizar las asignaciones de taxonomía en cualquier momento en la página _[!UICONTROL Asignación por intención]_. Consulte [Datos de intención](../admin/intent-data.md) para ver el proceso de configuración de taxonomía.

### Relevancia de contenido {#content-relevance}

Journey Optimizer B2B edition traduce el contenido y la taxonomía en una representación matemática de su significado y, a continuación, utiliza un modelo de similitud para medir cuánto se alinean. El contenido que coincida estrechamente con una palabra clave o un producto recibe una puntuación de alta relevancia. El contenido no relacionado recibe una puntuación baja.

El modelo de similitud está preparado en un idioma general, por lo que no se requiere formación específica del cliente para comenzar.

## Proceso de puntuación {#scoring-process}

Un proceso continuo convierte la participación sin procesar en una puntuación de intención finalizada. Cada etapa se basa en lo que produjo la etapa anterior.

![Diagrama de flujo de cinco etapas de puntuación: captura de participación, extracción de contenido, puntuación de relevancia, cálculo de intención diaria y entrega de puntuación.](./assets/intent-scores-pipeline.svg){width="700"}

### Captura de participación {#engagement-capture}

Cada punto de contacto significativo que una persona tiene se captura a medida que se produce y se vincula al contenido involucrado.

* Las visitas a la página, las aperturas y los clics por correo electrónico, los envíos de formularios y actividades similares se registran como eventos de participación.
* Cada fragmento único de contenido también se anota para que se pueda analizar en la siguiente etapa.
* **Actualizar cadencia** - Continua, a medida que se produce la interacción.

### Extracción de contenido {#content-extraction}

Antes de poder puntuar el contenido para su relevancia, Journey Optimizer B2B edition extrae y lee su texto.

* Para cada nuevo fragmento de contenido, el sistema extrae el texto subyacente, ya sea que se encuentre en una página web o en un correo electrónico.
* Algunos tipos de actividades, como los rellenos de formulario, ya incluyen su propio contenido descriptivo y omiten este paso.
* El contenido que no se puede recuperar, como un vínculo roto o eliminado, se registra y excluye a partir de ahora.
* **Actualizar cadencia** - A medida que se descubre contenido nuevo.

### Puntuación de relevancia {#relevance-scoring}

Todos los recursos se miden según su taxonomía, independientemente de quién haya participado en ellos.

* Cada correo electrónico y página web se analiza y compara con sus palabras clave, productos y categorías mediante el modelo de similitud.
* El resultado es una puntuación de relevancia entre 0 y 1 para ese recurso respecto a cada palabra clave o producto relacionado.
* **Actualizar cadencia** - Cada 12 horas.

### Cálculo de intención diario {#daily-intent-calculation}

La participación y la relevancia del contenido se combinan en una puntuación de intención diaria por persona, palabra clave o producto.

* Cada tipo de actividad lleva una ponderación configurable. Por ejemplo, un envío de formulario puede contar mucho más que una vista de página.
* La actividad reciente importa más que la actividad anterior, por lo que las puntuaciones favorecen lo que alguien hizo esta semana sobre lo que hizo hace un mes.
* Una medida de confianza refleja la coherencia con la que se ha comprometido una persona, no solo el volumen.
* **Actualizar cadencia** - A diario.

### Entrega de puntuación {#score-delivery}

Las puntuaciones diarias se acumulan, reciben un nivel de intención y se envían al panel.

* Cada puntuación está etiquetada con un nivel por intención de Alta, Medium o Baja.
* Las puntuaciones se vinculan a la cuenta correcta para que los equipos de ventas y marketing puedan ver la intención a nivel de persona y de cuenta.
* Solo se actualizan las personas cuyo nivel de intención ha cambiado, por lo que el panel refleja el último cambio significativo.
* **Actualizar cadencia** - A diario.

## Lógica de cálculo de puntuación {#score-calculation-logic}

El cálculo consta de cinco capas, cada una de las cuales agrega más contexto a la relevancia sin procesar y a los datos de participación.

### Relevancia de contenido para un tema {#relevance-to-topic}

Cada parte del contenido y cada tema, es decir, una palabra clave, un producto o una categoría, se traduce en una representación matemática de su significado. El contenido con un significado similar a un tema se encuentra más cerca en esta representación. La relevancia es una medida de proximidad en el significado, no una coincidencia exacta de la palabra.

### Ponderación de participación diaria {#engagement-weighting}

En un día determinado, la puntuación de una persona es un promedio ponderado de la relevancia de todo lo que interactuó con. Las actividades de mayor valor cuentan para más.

>[!BEGINSHADEBOX &quot;Ejemplo&quot;]

Una persona se involucra con tres fragmentos de contenido en un día. Las vistas de página tienen una ponderación de uno, y los envíos de formularios tienen una ponderación de cinco.

Dado que el envío de un formulario cuenta cinco veces más que una vista de página, influye significativamente en su puntuación diaria aunque interactuaran con tres elementos en total.

La puntuación diaria resultante para ese tema es de aproximadamente 0,70 en una escala de 0 a 1.

>[!ENDSHADEBOX]

### Deterioro de actualización {#recency-decay}

La puntuación de una persona refleja una combinación de los últimos días, con una actividad reciente ponderada mucho más que la actividad anterior. Después de aproximadamente una semana, la actividad antigua tiene un impacto mínimo, por lo que la puntuación siempre refleja el interés actual. En la práctica, una visita hoy supera a una de ayer, que supera a una de hace 10 días.

### Normalización de puntuación y niveles de intención {#normalization-intent-levels}

Cada puntuación ajustada se coloca en una escala coherente de 0 a 1 en relación con otras personas de su instancia y, a continuación, se agrupa en un nivel de intención.

| Puntuación final | Nivel de intención |
|-------------|--------------|
| Superior a 0,6 | Alto |
| 0,2 a 0,6 | Medio |
| Por debajo de 0,2 | Bajo |

### Agregación de puntuación {#score-aggregation}

Las puntuaciones individuales se suman para que pueda revisar la intención en el nivel que importa para una decisión, no solo en el nivel más granular.

* **Palabra clave en el producto**: las puntuaciones calculadas en el nivel de palabra clave se agregan para mostrar interés en un producto, no solo un término de búsqueda.
* **Persona a cuenta**: una puntuación de cuenta agrega las puntuaciones de todas sus personas, para que pueda ver cuándo todo un grupo de compra muestra intención.

![Diagrama que muestra puntuaciones de palabras clave agregadas a puntuaciones de productos y puntuaciones de personas agregadas a puntuaciones de cuentas.](./assets/intent-scores-aggregation.svg){width="500"}

Utilice la vista de nivel de producto para ver qué productos aumentan en interés general, en lugar de qué palabras clave individuales son tendencias. Utilice la vista a nivel de cuenta para ver cuándo todo un grupo comprador muestra un mayor interés juntos, en lugar de reaccionar ante una sola persona comprometida.

## Ajustes configurables {#configurable-settings}

La mayor parte de la lógica de puntuación se fija para mantener los resultados fiables y comparables a lo largo del tiempo. Un administrador de productos puede personalizar dos configuraciones para satisfacer sus necesidades:

* **Pesos de actividad**: para aplicar un mayor impacto a las puntuaciones por intención, aumente el peso de las actividades de alto valor, como una solicitud de demostración o una visita a la página de precios. Para excluir una actividad por completo, establezca su peso en cero, lo que resulta útil para acciones como cancelar suscripciones que no contribuyen a la intención. Las ponderaciones de actividad para el cálculo de intención utilizan el mismo modelo de ponderación que también genera [puntuaciones de participación](../buying-groups/engagement-scores.md). Consulte [_Configurar la ponderación de la puntuación de participación_](../admin/engagement-score-weighting.md) para cambiar las ponderaciones de la actividad.

* **Asignaciones de taxonomía**: las palabras clave, los productos y las categorías en los que se basa la puntuación están disponibles para su uso. Revíselos y actualícelos en cualquier momento en la página _[!UICONTROL Asignación por intención]_. Consulte [_Datos de intención_](../admin/intent-data.md) para ver el proceso de configuración.

Todo lo demás, incluida la relevancia del contenido, el deterioro de la actividad y los umbrales _Alto_, _Medium_ y _Bajo_, se ha corregido para que las puntuaciones sean coherentes y comparables a lo largo del tiempo.

## Principios de puntuación {#scoring-principles}

Tenga en cuenta los siguientes principios al revisar y actuar en las puntuaciones de intención.

### Puntuación impulsada por modelo {#model-driven}

No hay asignaciones de puntos ni reglas de palabras clave que mantener. El modelo aprende relevancia directamente del contenido y la taxonomía, lo que mantiene la coherencia de la puntuación a medida que la biblioteca de contenido crece y cambia, sin una configuración continua.

### Puntuación relativa {#relative-scoring}

Una puntuación indica dónde se encuentra una persona o cuenta entre sus otros contactos hoy y el sistema la recalcula diariamente en función de la población actual. Utilice puntuaciones para comparar personas y cuentas dentro de su propia instancia, en lugar de como un número fijo y universal. Las puntuaciones no son directamente comparables de una empresa a otra.

### Actualización de datos {#data-freshness}

La relevancia del contenido se actualiza aproximadamente cada 12 horas a medida que aparece nuevo contenido. Las puntuaciones por intención se vuelven a calcular una vez al día, por lo que el panel refleja la actividad del día anterior cada mañana.
