---
title: Journey Agent B2B
description: Aprenda a utilizar Journey Agent con tecnología de IA y sus habilidades para crear, administrar y observar recorridos B2B sólidos.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
exl-id: 5d2945ab-4f6c-4d9c-b0a1-1a93dc1849f3
autotag-review: '2026-06-05T16:42:46.785Z'
TQID: 'https://experienceleague.adobe.com/SgjavYf2Tp5yO8s3f0DQexRCUILQRsD5bM6UwmbcgyE'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2: id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: b43117c1e47f698d62b29f56b4713ac776c497a0
workflow-type: tm+mt
source-wordcount: 1165
ht-degree: 0%

---

# Journey Agent B2B

Journey Agent B2B es un asistente con tecnología de IA en Adobe Journey Optimizer B2B edition que le ayuda a diseñar, ejecutar, optimizar y supervisar los recorridos B2B a través del lenguaje natural. Reduce el tiempo y la complejidad implicados en la creación y administración de recorridos de clientes combinando automatización, recomendaciones basadas en datos y observabilidad en tiempo real.

![Mensaje B2B De Journey Agent](./assets/journey-agent-prompt.png)

Journey Agent B2B ofrece un conjunto de habilidades de IA, cada una centrada en una característica diferente del ciclo de vida del recorrido B2B. Las aptitudes disponibles actualmente son:

* **[Recorrido Build skill](#journey-build-skill)** - Crear, actualizar y optimizar recorridos a partir de mensajes en lenguaje natural
* **[Aptitud para observar el Recorrido](#journey-observability-skill)** - Haga preguntas sobre cómo se mueven las cuentas y las personas a través de los recorridos activos

## Recorrido Generar aptitud

La aptitud para crear Recorridos traduce sus objetivos de marketing, estrategia de participación y KPI en recorridos completos de clientes B2B. Aborda tres desafíos clave a los que se enfrentan los especialistas en marketing B2B en la actualidad:

* Hacer frente a recorridos de clientes cada vez más complejos (complejidad de audiencia, contenido y mensajería, y omnicanal)
* Mayor eficiencia a la luz de presupuestos más ajustados
* Averiguar cómo se debe estructurar el recorrido óptimo del cliente

Como especialista en marketing, puede utilizar esta aptitud para lo siguiente:

* **Crear**: traduzca sus objetivos de marketing, productos, estrategia de participación y KPI a un recorrido personalizado del cliente con automatización y condiciones
* **Recomendar**: aproveche la participación de marketing anterior y otros datos históricos para optimizar la creación de recorridos
* **Optimizar**: analiza, ajusta y optimiza los recorridos activos según las predicciones o el rendimiento real
* **Administrar**: dé prioridad, administre y organice recorridos y envíos de mensajes superpuestos

### Uso básico

Para utilizar la aptitud de Journey Agent Build, escriba en la ventana de mensajes lo que desea crear, utilizando lenguaje natural:

&quot;Cree un recorrido B2B para invitar a los responsables de la toma de decisiones a un roadshow en cuentas comprometidas que probablemente abra una nueva canalización&quot;.

![Solicitud B2B del agente de Recorrido para la aptitud de compilación](./assets/journey-agent-tasks.png)

Cuantos más detalles proporcione, mejor será la respuesta. Si ya dispone de material de marketing que describe el evento, el producto, etc., péguelo en el mensaje para que el agente comprenda mejor el objetivo.

&quot;Actúe como estratega de recorrido B2B para crear un recorrido de cuentas de cliente de varias fases que nutra y involucre a los responsables de la toma de decisiones y a los profesionales de marketing en la fase de exploración temprana de `<Solution Name>`. El objetivo es convertir a los visitantes anónimos en contactos conocidos, profundizar la participación con contenido relevante en `<domain>`.com y crear posibles clientes cualificados para el alcance de ventas de `<Product Name>`. Utilice canales como correo electrónico y medios de pago, aprovechando los segmentos de audiencia y el contenido existentes. Estructurar el recorrido a través de las etapas de sensibilización, consideración y evaluación durante 4-6 semanas, con déclencheur, acciones y objetivos claros para cada etapa. Incluya KPI como tasas de conversión, puntuaciones de participación y solicitudes de demostración, y devuelva el resultado como un flujo de recorrido estructurado&quot;.

Esta solicitud detallada proporciona lo siguiente:

* **Borrar intención**: ¿Qué desea que haga la IA? Sea específico sobre la tarea o el resultado.
* **Enriquecido con contexto**: Proporcione los antecedentes o restricciones relevantes. Incluya ejemplos o referencias, si es posible.
* **Formato estructurado**: use viñetas, pasos numerados o plantillas.
* **Asignación de funciones**: especifique la función de AI - &#39;Actuar como analista de datos...&#39;

Utilice el agente para repetir el refinamiento: Inicie simple y, a continuación, perfeccione el mensaje en función de los resultados. Los bucles de comentarios mejoran los resultados con el tiempo.

### Creación de recorridos B2B de extremo a extremo

La aptitud para crear Recorridos puede generar un flujo de recorridos de extremo a extremo (recorrido de cuenta o persona) a partir de mensajes de texto y metadatos en lenguaje natural, a través de una experiencia de conversación en lugar de una interfaz de usuario tradicional.

Ejemplos de mensajes de Recorrido de extremo a extremo:

* Cree un recorrido en canales múltiples para nutrir cuentas que no hayan participado en mi contenido en los últimos 30 días.
* Cree un recorrido para realizar ventas cruzadas de una solución a cuentas que muestren una alta intención sin canalizaciones abiertas, proporcionando contenido personalizado para las funciones de grupo de compra más importantes.
* Cree un recorrido B2B para invitar a los responsables de la toma de decisiones a un roadshow en cuentas comprometidas que probablemente abra una nueva canalización.
* Cree un recorrido para cuentas de espacio en blanco con la intención de usar mi solución, centrado en las personas que participan con contenido en el sitio web.

### Recorridos de varias etapas

Puede actuar como diseñador de recorridos B2B para crear un recorrido de cuentas de cliente de varias fases que informe a los responsables de la toma de decisiones y a las personas de marketing al principio de la fase de exploración. El objetivo es convertir a los visitantes anónimos en contactos conocidos, profundizar la participación con contenido relevante y crear posibles clientes cualificados para el alcance de las ventas.

* Use canales como `Email`, `Paid media`, `Personalized web experiences` para aprovechar el contenido y los segmentos de audiencia existentes.
* Estructurar el recorrido en `awareness`, `consideration` y `evaluation` etapas durante 4-6 semanas, con déclencheur, acciones y objetivos claros para cada etapa.
* Incluya KPI, como `conversion rates`, `engagement scores` y `demo requests`, y devuelva el resultado como un flujo de recorrido estructurado.

## Recorrido Aptitud de observación

La habilidad Observabilidad del Recorrido le permite hacer preguntas en lenguaje natural sobre cómo se mueven las cuentas y las personas a través de sus recorridos B2B, sin necesidad de explorar los mapas de recorrido, los registros o los paneles. Cubre dos áreas principales: progresión del recorrido y observabilidad de la sincronización de datos.

Puede acceder a él en dos lugares dentro de Journey Optimizer B2B edition:

* **Asistente de carril derecho en el mapa del recorrido**: haga preguntas específicas del recorrido directamente desde el mapa del recorrido. El nombre del recorrido se inserta automáticamente en el contexto.

* **Página del Asistente de pantalla completa**: una vista conversacional más grande adecuada para preguntas complejas o de varias cuentas y para explorar múltiples recorridos.

### Insight de recorrido de nivel de cuenta

Rastree cómo una cuenta específica fluyó a través de un recorrido haciendo preguntas como:

* &quot;Dame información básica de la cuenta de ACME Industries&quot;.
* &quot;Cuéntame cómo pasó la cuenta Northstar Services por la Estrategia de Nutrición ABM del recorrido&quot;.
* &quot;¿Cuándo comenzó este recorrido la cuenta Contoso LLC?&quot;

### Razonamiento y recuentos de rutas de nodos divididos

Comprenda por qué se tomó una sucursal y cuántas personas o cuentas siguieron cada ruta:

* &quot;¿Por qué la cuenta QiDemoAccount24 fue a la pequeña ruta tecnológica de California en Estados Unidos en el nodo dividido c764a9?&quot;
* &quot;Dame el recuento de personas para cada ruta en el nodo dividido node-459c7c&quot;.
* &quot;Muéstrame gente en la ruta de San José para la Cuenta8&quot;.

El agente inspecciona la lógica dividida, los atributos de cuenta y las actividades para explicar las decisiones de enrutamiento y devolver recuentos por ruta o listas de personas.

### Resultados del recorrido a nivel de personas

Analice los resultados individuales dentro de una cuenta o en todo un recorrido, lo que resulta especialmente útil para comprar análisis de grupo y rastrear la conducta del responsable de la toma de decisiones en comparación con la del influenciador:

* &quot;Dame recuento de personas en cada ruta para este nodo dividido para Account123&quot;.
* &quot;Enumerar personas en la ruta de omisión oculta&quot;.
* &quot;Muéstrame a las personas en la ruta de ubicación de San Diego para esta cuenta&quot;.

### Ciclo de vida y tiempo del recorrido

Recupere marcas de tiempo clave para un recorrido o cuentas específicas:

* &quot;¿Cuándo se lanzó este recorrido?&quot;
* &quot;¿Cuándo entró la primera cuenta en este recorrido?&quot;
* &quot;¿Cuándo inició este recorrido la cuenta QiDemoAccount50?&quot;

### Audiencia externa y visibilidad de la activación

En el caso de los recorridos que llevan a canales externos como LinkedIn, puede comprobar el estado de activación:

* &quot;¿Está bsmith@acme.com en la audiencia externa?&quot;
* &quot;Enumerar todas las personas activadas en LinkedIn mediante ObservabilityExtAudience01&quot;.

### Sincronización de datos y observabilidad de canalización

La habilidad Observabilidad también puede mostrar información de estado de sincronización de datos para ayudar a solucionar el problema de por qué una cuenta o posible cliente no se incluyó en un recorrido:

* Métricas y estado del trabajo de exportación de audiencias externas
* Programaciones de segmentación por lotes y horas de finalización
* Horario de mantenimiento del grupo de compra
* Estadísticas del administrador de trabajos (completadas/fallidas)