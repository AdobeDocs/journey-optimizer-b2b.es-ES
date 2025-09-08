---
title: Guía de preguntas para el asistente de IA
description: Escriba preguntas eficaces del asistente de IA con prácticas recomendadas, ejemplos y sugerencias de redacción para obtener respuestas óptimas en Journey Optimizer B2B edition.
feature: AI Assistant
role: User
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: 4fdd89bf32cb9d68b4cdc347f1fd09df8eabe24d
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 1%

---

# Guía de preguntas para el asistente de IA en Journey Optimizer B2B edition

Revise el siguiente conjunto de preguntas de ejemplo para consultar el Asistente de IA en Journey Optimizer B2B edition. Esta información también incluye sugerencias para formular preguntas y obtener respuestas óptimas del asistente de IA.

## Preguntas basadas en objetivos

Las siguientes preguntas de ejemplo se agrupan según los objetivos que puede lograr al utilizar el Asistente para IA:

| Objetivo | Descripción | Ejemplo |
| --- | --- | --- |
| Conceptos de aprendizaje y flujos de trabajo continuos | Como usuario novato, puede utilizar el asistente de IA para aprender los conceptos de Real-Time CDP y Adobe Journey Optimizer B2B edition, e incorporarse a productos y funciones con los que no está familiarizado. <br>Como usuario experimentado, puede utilizar el Asistente de IA para resolver un caso límite que pueda estar bloqueando el flujo de trabajo. | <li>Dime algunos casos de uso para Real-Time CDP. <li>Explícame el concepto de Grupo de Compra. |
| Resolución de problemas | Utilice el Asistente de IA para aprender a depurar los errores básicos que pueden producirse en el flujo de trabajo. | <li>¿Qué significa este error &lt;ERROR_MESSAGE>? <li>¿Por qué no puedo eliminar la audiencia llamada &quot;...&quot;? |
| Higiene de zona protegida | Utilice el asistente de IA para identificar duplicados u objetos que no se utilicen, de modo que pueda mantener de forma eficaz la zona protegida. | <li>¿Puede mostrarme audiencias de cuenta similares? <li>¿Hay algún esquema que no tenga un conjunto de datos asociado? |
| Análisis de valor | Utilice el asistente de IA para identificar los objetos de datos más utilizados, evaluar cualquier indicador de rendimiento o encontrar los objetos de datos más valiosos. | <li>¿Cuántas cuentas hay en nuestra definición de segmento &quot;...&quot;? <li>¿Cuándo se activaron las audiencias en el destino de Audiencias de Experience Cloud? |
| Buscar | Utilice el asistente de IA para encontrar objetos Experience Platform y Adobe Journey Optimizer B2B edition compatibles, como audiencias de cuenta, conjuntos de datos, destinos, esquemas, fuentes, recorridos de cuenta, plantillas de grupo de compra e intereses de soluciones | <li>Enumere las audiencias que contienen &quot;Luma&quot; en el nombre y que se utilizaron en los recorridos de la cuenta. <li>¿Qué atributos hay en el esquema XDM &quot;Luma: Custom Actions&quot;? |
| Análisis de impacto | Utilice el asistente de IA para identificar objetos de datos que se han utilizado en determinados flujos de trabajo y así poder evaluar el impacto de cualquier cambio. | <li>¿Qué audiencias de cuenta utilizan `workEmail.address` en el esquema &quot;Persona B2B&quot;? <li>¿En qué conjuntos de datos se almacenan los ... `jobTitle`? |

## Formulación de preguntas

Debe formular sus preguntas al asistente de IA con claridad y contexto para obtener una respuesta lo más precisa posible. Consulte la siguiente lista de sugerencias para obtener instrucciones sobre cómo hacer una pregunta clara con contexto:

* Exponga su tarea y/o pregunta de forma concisa.
* Evite el lenguaje ambiguo o la sintaxis demasiado compleja para facilitar la comprensión.
* Proporcione un contexto relevante con respecto a su tarea o pregunta, ya que el contexto puede ayudar al Asistente de IA a generar respuestas más relevantes.

En las tablas siguientes se proporcionan algunas prácticas recomendadas que puede seguir al utilizar el Asistente para IA:

| Hacer | Ejemplo |
| --- | --- |
| <li>Sea específico sobre el objeto o la información que desea recuperar o analizar. <li>Intente poner los nombres de los objetos de datos entre comillas. <li>Si sólo conoce una parte del nombre del objeto, también puede especificarlo en la pregunta. | <li>¿Qué conjuntos de datos utilizan el esquema &quot;Cuenta B2B&quot;? <li>Muéstreme las audiencias activadas que tienen &quot;Cuenta&quot; en sus nombres. Clasificarlos por recuento de miembros. |
| <li>Evite la ambigüedad y utilice un lenguaje claro. <li>Utilice una terminología precisa para garantizar una mejor claridad en la consulta. <li>Cuando haga preguntas sobre Adobe Experience Platform y Adobe Journey Optimizer B2B edition, intente utilizar una terminología específica de Experience Platform o Adobe Journey Optimizer B2B edition para mejorar la relevancia de las respuestas. | <li>¿Cuántos miembros tengo en &quot;Audiencia de mi cuenta&quot;? <li>¿Cuántos recorridos de cuenta utilizan la Audiencia de cuenta &quot;Audiencia de mi cuenta&quot;? |
| <li>Proporcione contexto o especifique un criterio para filtrar los resultados. <li>Utilice un criterio de filtro en las preguntas para limitar el volumen de datos en la respuesta. | <li>Mostrar las audiencias de cuenta que no se han activado y que se crearon hace más de 6 meses y que no se han modificado nunca. <li>Mostrarme los recorridos de cuenta publicados en los últimos siete días y utiliza una audiencia de cuenta con más de 1000 miembros |

| No lo hagas | Ejemplo |
| --- | --- |
| Utilice un lenguaje vago o ambiguo. | <li>Proporcionarme información sobre conjuntos de datos. <li>¿Qué hace el recorrido x? <li>¿Cuántos usuarios tengo en &quot;Audiencia ACME&quot;? <li>Mostrar segmentos. <li>Atributos de lista. |
| Realizar solicitudes incompletas. | <li>&quot;Luma: Conjunto de datos de fidelización&quot; |
| Asumir el conocimiento sin contextos. | <li>Audiencias en los últimos 6 meses. <li>Cree una consulta para mí. <li>Crear un recorrido para mí |
| Formular consultas demasiado complejas. | <li>Proporcionar un análisis completo del linaje de datos en todos los objetos y sus dependencias. |
| Omitir criterios o parámetros. | <li>Mostrar conjuntos de datos. |

## Ejemplos de preguntas no admitidas

La siguiente lista incluye ejemplos de preguntas que el Asistente de IA de Journey Optimizer B2B edition no admite actualmente:

* ¿Qué audiencias de cuenta utilizan el campo workEmail.address del grupo de campos... en su condición? 
* Mostrar el número de recorridos activos que utilizan audiencias de cuenta de un tamaño superior a 10 000, 5000-10 000, 1000-5000 e inferior a 1000 en un elemento visual de distribución
* ¿Quién realizó la última actualización del recorrido de la cuenta x?
* ¿Cuántos recorridos activos añaden miembros del grupo comprador al interés de la solución x?
* ¿Qué recorridos activos añaden miembros del grupo comprador al interés de la solución x?
* ¿Cuál es el título más común del responsable de la toma de decisiones al comprar plantillas de grupo?
* ¿Quiénes son los encargados de tomar decisiones para comprar la plantilla de grupo x?

## Próximos pasos

Para obtener información sobre cómo usar las funciones del Asistente de IA durante los flujos de trabajo, consulte [Usar el Asistente de IA en Journey Optimizer B2B edition](./use-ai-assistant.md).
