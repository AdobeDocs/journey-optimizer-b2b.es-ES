---
title: Aptitudes de recorrido para B2B
description: Aprenda a preparar informes de recorrido, revisar borradores de gráficos validados, configurar borradores guardados e inspeccionar los recorridos de cuenta y persona a través del chat de Coworker.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
exl-id: 5d2945ab-4f6c-4d9c-b0a1-1a93dc1849f3
autotag-review: '2026-06-05T16:42:46.785Z'
TQID: 'https://experienceleague.adobe.com/SgjavYf2Tp5yO8s3f0DQexRCUILQRsD5bM6UwmbcgyE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 876251dd1b69fc768c790daf0b9b1482015d69af
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%
---
# Aptitudes de recorrido para B2B

Use el chat de [!DNL Adobe CX Enterprise Coworker] para buscar, crear y configurar recorridos en [!DNL Adobe Journey Optimizer B2B Edition]. Cree borradores validados a partir de una descripción breve, cambie los borradores de gráficos guardados y la configuración de reentrada, y configure los nodos no configurados. Los cambios de recorrido se aplican a los borradores guardados, no a los recorridos activos.

Para ver los identificadores de aptitudes de búsqueda, creación y reglas y sus acciones admitidas, consulte la [Referencia de aptitudes del recorrido de trabajo con colaboradores](./coworker-overview.md#skills). Este artículo proporciona una breve guía de preparación y ejemplos de observabilidad de recorrido:

* [Guía de creación de Recorridos](#journey-creation-skills): prepare un informe y revise un borrador antes de crearlo.
* [Guía de observabilidad de Recorrido](#journey-observability-skills): haga preguntas sobre cómo se mueven las cuentas y las personas a través de los recorridos activos.

Para obtener instrucciones sobre cómo abrir la aplicación e iniciar conversaciones, usa la [guía de la interfaz del colaborador](https://experienceleague.adobe.com/es/docs/coworker/content/chat/ui-guide){target="_blank"}.

## aptitudes de creación de recorridos {#journey-creation-skills}

La aptitud para crear recorridos convierte un informe en un gráfico de recorridos de personas o cuentas validadas. Resuelve la audiencia con nombre en su ID de audiencia [!DNL Adobe Experience Platform] y previsualiza el gráfico antes de crear un borrador.

Debe aprobar explícitamente la vista previa antes de que [!DNL Coworker] cree el borrador. La aptitud de creación no detecta audiencias, ni configura reglas de nodos, crea mensajes, copia, publica ni elimina recorridos.

### Preparar un informe {#basic-usage}

Describa el borrador del recorrido que desea en lenguaje natural. Incluya los siguientes detalles:

* Tipo de recorrido: Cuenta o persona.
* Audiencia existente: nombre o ID de la audiencia que se va a utilizar.
* Flujo de recorrido: Las acciones, esperas y ramas que se van a incluir.
* Configuración de reentrada: Si las cuentas o las personas pueden volver a entrar, y cuándo.

Incluya detalles relevantes de su informe de campaña para que [!DNL Coworker] pueda interpretar el objetivo. Refine la solicitud si la previsualización no coincide con el flujo deseado.

![Mensaje de solicitud de creación de Recorrido en Coworker Chat.](./assets/coworker-chat-b2b-journey-prompt.png){width="800" zoomable="yes"}

### Revisar y crear un borrador {#end-to-end-b2b-journey-creation}

Revise el tipo de recorrido, la audiencia resuelta, los nodos y las rutas en la vista previa validada. Apruebe la creación solo cuando el gráfico coincida con la información breve.

Después de la aprobación, [!DNL Coworker] crea el borrador y devuelve su vínculo. Utilice una solicitud de seguimiento para configurar sus nodos no configurados mediante la aptitud de reglas. Agregue una copia del mensaje en la aplicación y, a continuación, complete los [pasos de revisión y publicación del recorrido](../journeys/create-publish-journey.md).

Para ver un ejemplo completo, vea [Crear un recorrido de cuentas](./coworker-overview.md#build-account-journey).

### Recorridos de varias etapas

Para un recorrido con varias fases, describa las acciones, esperas y ramas de cada fase en la descripción breve. Distingue la estructura de gráficos de las reglas y la copia de mensaje que configure después de la creación del borrador.

Para revisar un borrador guardado, solicite un gráfico o cambios de reentrada mediante la aptitud de creación. Utilice la aptitud de reglas para condiciones de división, acciones, eventos y la audiencia de lista dinámica en nodos no configurados.

## Habilidades de observabilidad de recorrido {#journey-observability-skills}

Las habilidades de observabilidad del recorrido le permiten hacer preguntas en lenguaje natural sobre cómo las cuentas y las personas se mueven a través de sus recorridos B2B, sin necesidad de explorar los mapas de recorrido, los registros o los paneles. Cubren dos áreas principales: progresión del recorrido y observabilidad de la sincronización de datos.

![Solicitud y respuesta de observabilidad de Recorrido en [!DNL CX Coworker]](./assets/journey-observability-prompt-response.png){width="800" zoomable="yes"}

### Insight de recorrido de nivel de cuenta

Rastree cómo una cuenta específica fluyó a través de un recorrido haciendo preguntas como:

* &quot;Dame información básica sobre las cuentas de Bodea Cloud&quot;.
* &quot;Cuéntame cómo pasó la cuenta Northstar Services por la Estrategia de Nutrición ABM del recorrido&quot;.
* &quot;¿Cuándo comenzó este recorrido la cuenta Contoso LLC?&quot;

### Razonamiento y recuentos de rutas divididas

Comprenda por qué se tomó una sucursal y cuántas personas o cuentas siguieron cada ruta:

* &quot;¿Por qué la cuenta QiDemoAccount24 fue a la pequeña ruta tecnológica de California en Estados Unidos en el nodo dividido c764a9?&quot;
* &quot;Dame el recuento de personas para cada ruta en el nodo dividido node-459c7c&quot;.
* &quot;Muéstrame gente en la ruta de San José para la Cuenta8&quot;.

Las aptitudes de observación de recorridos analizan la lógica dividida, los atributos de cuenta y las actividades para explicar las decisiones de enrutamiento y los recuentos de devoluciones por ruta o listas de personas.

### Resultados del recorrido a nivel de personas

Analice los resultados individuales dentro de una cuenta o en todo un recorrido, lo que resulta especialmente útil para comprar análisis de grupo y rastrear la conducta del responsable de la toma de decisiones en comparación con la del influenciador:

* &quot;Dame gente cuenta en cada ruta dividida para el recorrido de Bodea Next Web Engagement&quot;.
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

Las habilidades de observabilidad del recorrido también pueden mostrar información de estado de sincronización de datos para ayudar a solucionar por qué una cuenta o posible cliente no se incluyó en un recorrido:

* Métricas y estado del trabajo de exportación de audiencias externas
* Programaciones de segmentación por lotes y horas de finalización
* Horario de mantenimiento del grupo de compra
* Estadísticas del administrador de trabajos (completadas/fallidas)