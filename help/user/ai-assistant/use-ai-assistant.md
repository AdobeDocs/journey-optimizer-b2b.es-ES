---
title: Utilizar el asistente de IA
description: Descubra cómo el Asistente de IA puede ayudarle a sacar el máximo partido a las funciones de Journey Optimizer B2B edition.
feature: AI Assistant
level: Beginner
exl-id: 2d642c34-6f6d-4a0f-98c5-4b9ea1cdaa29
source-git-commit: d19ed2bbe850a14cb0563f6e3563cd8f1c8d3226
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# Uso del asistente de IA en Journey Optimizer B2B edition

En Journey Optimizer B2B edition, el asistente de IA es una función de la interfaz de usuario que puede utilizar para comprender los conceptos del producto, navegar rápidamente por las funciones de Journey Optimizer B2B edition y obtener información operativa para su entorno específico. También está disponible en varios productos de Adobe Experience Cloud.

>[!IMPORTANT]
>
>Se requiere un acuerdo para las Directrices del usuario de IA generativas de Adobe Experience Cloud antes de poder utilizar el asistente de IA. Para obtener más información sobre este contrato y las directrices de uso, consulte [Directrices del usuario de IA generativa de Adobe Experience Cloud](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html).

Para acceder al asistente de IA, haga clic en el icono del encabezado. El asistente de IA se abre en un panel a la derecha.

![Haga clic en el icono para acceder al asistente de IA](./assets/ai-assistant-icon-displayed.png){width="420" zoomable="yes"}{width=&quot;420&quot; zoomable=&quot;yes&quot;}

Aparecerá la interfaz del Asistente de IA, que le proporcionará inmediatamente información para empezar. Puede usar las opciones que se proporcionan en _Ideas para empezar_ a responder preguntas y comandos como los siguientes:

* ¿Cuáles de mis recorridos de cuenta se publicaron?
* ¿Qué intereses de solución se han creado?
* Cuéntame las ventajas clave de Journey Optimizer B2B edition.

En Adobe Journey Optimizer B2B edition, el asistente de IA es compatible con los siguientes casos de uso:

## Conocimiento del producto

Las preguntas de conocimiento del producto se refieren a conceptos de Journey Optimizer B2B edition relacionados con aspectos de Adobe Journey Optimizer. Algunos ejemplos de preguntas sobre el conocimiento del producto son:

* ¿Cómo configuro las cuentas de proveedor de SMS?
* ¿Cómo envío un correo electrónico en un recorrido de cuenta?
* ¿Cómo puedo personalizar el contenido de mi correo electrónico?

Para hacer una pregunta sobre un producto, indíquela en el campo situado en la parte inferior del panel y pulse Intro.

![Escriba una pregunta en el cuadro de texto](./assets/ai-assistant-ask-question.png){width="420" zoomable="yes"}{width=&quot;420&quot; zoomable=&quot;yes&quot;}

Puede verificar las respuestas que devuelve el asistente de IA revisando las citas disponibles con cada respuesta de conocimiento del producto.

Para ver las citas y validar la respuesta del asistente de inteligencia artificial, seleccione **[!UICONTROL Mostrar orígenes]**.

![Resultados de la consulta del Asistente de IA](./assets/ai-assistant-answer.png){width="420" zoomable="yes"}{width=&quot;420&quot; zoomable=&quot;yes&quot;}

El asistente de IA actualiza la interfaz y le proporciona vínculos a documentación que corrobora la respuesta inicial. Además, cuando las citas están habilitadas, el Asistente de IA actualiza la respuesta para incluir notas al pie para indicar las partes específicas de la respuesta que hacen referencia a la documentación proporcionada.

Utilice el pulgar hacia arriba o hacia abajo para valorar la calidad de la respuesta.

## Perspectivas operativas

Las preguntas operativas de insight se refieren a los objetos de recorrido de la zona protegida de su organización. Algunos ejemplos de preguntas o mensajes operativos de insight son los siguientes:

* ¿Cuántos recorridos en directo tengo en Adobe Journey Optimizer B2B edition?
* Dame una lista de todos los recorridos programados
* ¿Cuántos recorridos se han creado en los últimos 7 días?

Debe estar en una zona protegida activa para que AI Assistant proporcione una respuesta suficiente a una pregunta sobre sus perspectivas operativas.

>[!NOTE]
>
>Los únicos objetos de Adobe Journey Optimizer B2B edition compatibles con las preguntas de perspectivas operativas del Asistente de IA se enumeran en la [tabla de dominio de perspectivas operativas](./ai-assistant-overview.md#operational-insights). Solo puede acceder a los datos de la zona protegida en la que se encuentra actualmente.

<!-- Select to view an example of an operational insights question.

In the following example, AI Assistant receives the following query: _Show me dataflows that were created using the Amazon S3 source._

screen

AI Assistant responds with a table list of your dataflows and their corresponding IDs. Click the _Download_ icon ( Download icon ) to download the table as a CSV file. To view the entire table, click the _Expand_ icon ( Expand icon ).

screen

An expanded view of the table appears, providing you with a more comprehensive list of dataflows based on the parameters of your query.

screen

When prompted with an operational insights question, AI Assistant provides an explanation of how it computed the answer. In the following example, AI Assistant outlines the steps it took in order to identify the dataflows that were created using the Amazon S3 source.

screen

You can also provide filters and modifications to your questions, and you can instruct AI Assistant to render its findings based on the filters that you include. For example, you can ask AI Assistant to show you a trend of the count of segment definitions in the order of their created date, remove segment definitions with zero total profiles, and use month names instead of integers when displaying the data.

### Verify operational insights responses

You can verify each response related to operational insights questions using an SQL query that AI Assistant provides.

Select to view example of verifying operational insights responses

After receiving an answer for an operational insights question, click **[!UICONTROL Show sources]** and then select **[!UICONTROL View source query]**.

screen

When queried with an operational insights question, AI Assistant provides an SQL query that you can use to verify the process that it took to compute its answer. This source query is for verification purposes only and is not supported on Query Service.

screen  

 -->
