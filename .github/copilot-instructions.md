---
source-git-commit: 1b4d8ad802265b537eb09439cfe34b97a3e61448
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%
---
# Instrucciones del repositorio de GitHub Copilot

Cuando las directrices generales de las instrucciones copiadas de Claude entren en conflicto con las convenciones específicas del repositorio o con las instrucciones específicas de la tarea, siga las instrucciones específicas del repositorio o de la tarea.

## Finalidad

Utilice estas instrucciones del repositorio para el trabajo de documentación en este repositorio. Mantenga las ediciones concisas, técnicamente precisas y alineadas con los estándares de documentación de Adobe Experience League.

## Escriba en el estilo de documentación del repositorio

- Prefiere un lenguaje claro, directo y centrado en el usuario.
- Utilice frases cortas y analizables.
- Preferir un idioma específico y procesable sobre el texto de marketing o de relleno.
- Evite secciones de plantillas como &quot;Temas relacionados&quot;, &quot;Preguntas frecuentes&quot; o bloques de resumen genéricos a menos que se requieran explícitamente.
- Utilice vínculos cruzados en contexto en lugar de bloques de navegación al final de la página.
- No agregue una lista de referencias o una sección &quot;Temas relacionados&quot; al final de un artículo. Introduzca vínculos relacionados donde sean relevantes en el contenido y explique cómo se relaciona cada destino con el tema actual.
- No utilice lenguajes espaciales como &quot;abajo&quot; o &quot;arriba&quot; para describir el orden del documento; utilice &quot;siguiente&quot;, &quot;anterior&quot; o &quot;en la sección siguiente&quot; en su lugar.

## Reglas de nomenclatura de documentación externa

- No utilice las siglas de producto de Adobe en la documentación externa.
- La primera mención de los nombres de productos de Adobe debe utilizar el nombre completo del producto, incluido &quot;Adobe&quot; cuando corresponda.
- Utilice etiquetas DNL para nombres de productos en el contenido, por ejemplo:
  - [!DNL Adobe Experience Platform]
  - [!DNL Adobe Journey Optimizer B2B Edition]
  - [!DNL Experience Platform]
  - [!DNL Journey Optimizer B2B Edition]
- Reemplace las referencias solo de acrónimo como &quot;AEP&quot; y &quot;AJO B2B&quot; con sus nombres de producto completos en la documentación del usuario.
- Cuando se introduce un producto por primera vez, escriba el nombre completo. Las menciones posteriores pueden utilizar el nombre de producto más corto sin el acrónimo y mantener la etiqueta DNL cuando el nombre del producto aparece en la interfaz de usuario o en el texto de los documentos.
- Aplique estos términos de forma coherente en el título de la página, el primer párrafo y cualquier etiqueta o vínculo cruzado visible para los lectores.

## Convenciones de nomenclatura específicas del repositorio

- Utilice &quot;Adobe Journey Optimizer B2B Edition&quot; para el nombre del producto en los documentos del usuario.
- Utilice &quot;Adobe Experience Platform&quot; para el nombre de la plataforma en los documentos del usuario.
- Utilice el nombre completo del producto en la primera mención y luego haga que las referencias posteriores sean cortas y coherentes.
- Para las referencias de conjuntos de datos, conserve los nombres e ID reales del conjunto de datos exactamente como aparecen en el contrato de origen, incluso cuando incluyan prefijos heredados como `AJOB2B-`.

## Guía de marcado y formato

- Escriba un Markdown válido con sabor a GitHub.
- Mantenga los encabezados concisos y descriptivos.
- Utilice tablas solo cuando ayuden a los lectores a analizar los detalles técnicos.
- Use vínculos relativos para referencias repo-locales.
- Mantenga los bloques de código y las rutas de campo exactos y copiables.
- Evite referencias de productos redundantes en los encabezados si el título de la página ya las indica.

## Lista de comprobación de validación antes de finalizar

- Asegúrese de que no haya acrónimos para productos de Adobe en el contenido orientado al usuario.
- Asegúrese de que las primeras menciones utilicen el nombre completo del producto.
- Asegúrese de que los nombres de los productos estén etiquetados con [!DNL ...] donde el estilo del repositorio lo requiera.
- Asegúrese de que el documento evita problemas de plantillas y de redacción espacial.
- Asegúrese de que el contenido técnico sigue siendo preciso y de que se conservan los vínculos cruzados en contexto.
