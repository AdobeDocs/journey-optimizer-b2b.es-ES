---
title: Compañeros de trabajo en Adobe Journey Optimizer B2B Edition
description: Aprenda a utilizar CX Enterprise Coworker para buscar, crear y configurar recorridos de cuenta y persona, revisar vistas previas de borradores y aprobar la creación de recorridos.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
level: Beginner
autotag-review: '2026-11-24T23:47:29.469Z'
TQID: 'https://experienceleague.adobe.com/gkizS-MB6qEMoG1pMqD3tSCBtcEuv-m-GMD5H6Z4JsY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: 9b63d357-750f-5558-9208-62fc8a356785
    internal-label: Approval
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c2f21a5c-bae4-56c6-97e3-2fc9a0e6c120
    internal-label: Use Cases
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 81b4844bc7b333baaa2218639a542fefd512102f
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 2%
---

# [!DNL CX Enterprise Coworker] en [!DNL Adobe Journey Optimizer B2B Edition] {#coworker-overview}

Use el chat de [!DNL Adobe CX Enterprise Coworker] para completar tareas en [!DNL Adobe Journey Optimizer B2B Edition]. Describa un objetivo en lenguaje sencillo. [!DNL Coworker] planifica el trabajo, lo lleva a cabo, valida los resultados y presenta el trabajo para su aprobación.

Busque los recorridos de cuenta y persona existentes, cree nuevos recorridos de borrador o actualice los borradores guardados. [!DNL Coworker] convierte su informe en un recorrido de trabajo validado y lo previsualiza antes de crear el borrador. Debe aprobar explícitamente la vista previa antes de que [!DNL Coworker] cree el recorrido.

[!DNL Coworker] respeta los [permisos de productos](../admin/user-management.md#b2b-product-permissions) existentes de su organización. Solo puede realizar las acciones que ya tiene permiso para realizar. Los administradores controlan cuándo tiene acceso de escritura. Para conocer los requisitos de acceso, consulte [Habilitar el acceso de IA](../ai-coworker/enable-ai-access.md).

[!DNL Coworker] funciona en todo el ecosistema de Adobe, no solo en [!DNL Journey Optimizer B2B Edition]. Para conocer sus capacidades más amplias, consulte la [descripción general de Adobe CX Enterprise Coworker Chat](https://experienceleague.adobe.com/es/docs/coworker/content/chat/overview){target="_blank"}. Para obtener instrucciones sobre cómo abrir la aplicación e iniciar conversaciones, usa la [guía de la interfaz del colaborador](https://experienceleague.adobe.com/es/docs/coworker/content/chat/ui-guide){target="_blank"}.

## aptitudes de recorrido {#skills}

Utilice estas tres aptitudes para inspeccionar recorridos, crear recorridos y configurar nodos. Los identificadores de aptitud son nombres técnicos exactos.

| Habilidad | Lo que le ayuda a hacer | Fuera del ámbito de la aptitud |
| --- | --- | --- |
| `journey-lookup-ajob2b` | Enumere, cuente, busque y explique los recorridos de cuenta y persona. Inspeccione los nodos, la configuración de reentrada y las actividades, atributos o audiencias de evento que utiliza un recorrido. Esta aptitud no cambia los recorridos. | Cree o cambie recorridos, configure reglas, cree mensajes, administre plantillas de grupos de compra, publique o elimine. |
| `journey-creation-ajob2b` | Convierta un informe en un recorrido. Seleccione el tipo de recorrido, resuelva la audiencia según su ID de audiencia [!DNL Adobe Experience Platform], valide el gráfico y previsualícelo. Cree el borrador después de una aprobación explícita. Edite el gráfico de un borrador guardado y la configuración de reentrada. | Busque recorridos existentes, configure reglas, cree mensajes, administre plantillas de grupos de compra, descubra audiencias, publique o elimine. |
| `journey-rules-ajob2b` | Configure condiciones de división, acciones, eventos y la audiencia de lista dinámica en los nodos no configurados de un recorrido guardado. | Cambie el gráfico, busque recorridos, cree correos electrónicos o SMS, descubra audiencias o publique. |

Para obtener más información, consulte [Aptitudes de Recorrido para B2B](./journey-skills.md). Para trabajar con audiencias de persona y cuenta, consulte [Aptitudes de audiencia para personas y cuentas B2B](./audience-skills-b2b.md).

## Ejemplos de casos de uso {#use-cases}

Utilice solicitudes independientes para crear un borrador, configurar sus nodos e inspeccionar los recorridos existentes.

### Crear un recorrido de cuenta {#build-account-journey}

Cree un recorrido de nutrición de cuentas a partir de una breve y, a continuación, configure sus nodos.

Mensaje de ejemplo: _Cree un recorrido de cuenta para la audiencia de cuentas de Enterprise Target que envíe un correo electrónico de bienvenida, espere tres días y envíe un correo electrónico de caso práctico._

1. Describir el flujo de audiencia y recorrido en el chat de [!DNL Coworker].
1. Revise el gráfico de recorridos validado y previsualice. [!DNL Coworker] resuelve la audiencia con nombre en su ID de audiencia [!DNL Experience Platform].
1. Aprobar explícitamente la previsualización. [!DNL Coworker] crea el borrador y devuelve su vínculo.
1. Pida a [!DNL Coworker] que configure los nodos no configurados del borrador.
1. Abra el borrador en [!DNL Journey Optimizer B2B Edition] para agregar una copia del mensaje y revisar el recorrido.

El resultado es un borrador de recorrido, no un recorrido publicado. Complete los [pasos de revisión y publicación del recorrido](../journeys/create-publish-journey.md) en la aplicación.

### Inspeccionar y actualizar recorridos {#inspect-update-journeys}

Revise el inventario de recorridos y, a continuación, perfeccione las condiciones de división y la configuración de reentrada de un borrador guardado.

Ejemplo de solicitud de búsqueda: _¿Cuántos recorridos de la cuenta están activos? Mostrarme dónde el 14251 de recorrido tiene cuentas en espera._

1. Pida a [!DNL Coworker] recuentos de recorridos por estado o busque un recorrido por nombre o identificador.
1. Revise los detalles del recorrido y los recuentos de cuentas en cada nodo.
1. Identifique el borrador guardado que desee actualizar.
1. Pida a [!DNL Coworker] que configure su condición de división. Por ejemplo: _Para los 14252 de recorrido de borrador, haga que la rama de intención alta requiera una visita a la página de precios._
1. Solicite el cambio de reentrada. Por ejemplo: _Para 14252 de recorrido de borrador, evite que las cuentas vuelvan a entrar durante 30 días._

Los cambios se aplican al borrador guardado. La publicación es un paso independiente. Para obtener detalles de configuración, consulte [Dividir y combinar rutas](../journeys/split-merge-paths-nodes.md) y [reentrada al Recorrido](../journeys/journey-re-entry.md).

## Herramientas de MCP {#mcp-tools}

[!DNL Coworker] utiliza las siguientes herramientas de MCP (Model Context Protocol) para las tareas de recorrido. Las herramientas de lectura inspeccionan la información existente, la herramienta de comprobación valida un gráfico y las herramientas de escritura cambian la configuración del recorrido o los borradores.

| Herramienta | Acción admitida | Tipo |
| --- | --- | --- |
| `list_account_journeys` | Devuelve una lista paginada de recorridos de cuenta. | Lectura |
| `list_person_journeys` | Devuelve una lista paginada de recorridos de persona. | Lectura |
| `count_account_journeys` | Contar recorridos de cuenta por estado. | Lectura |
| `count_person_journeys` | Contar recorridos de personas por estado. | Lectura |
| `get_journey` | Leer los nodos de recorrido y la configuración de reentrada. | Lectura |
| `get_journey_rules` | Lea los destinos de configuración de los nodos no configurados de un recorrido. | Lectura |
| `get_journey_node_catalog` | Devolver `ruleset_types`, que son entradas válidas para los datos de regla. | Lectura |
| `validate_journey_graph` | Valide un borrador de gráfico creado. | Marque |
| `create_journey` | Vista previa del recorrido con `confirm=false`. Después de la aprobación explícita, cree el borrador y devuelva su vínculo. | Escritura |
| `update_journey` | Cambie el gráfico de un recorrido de borrador guardado. | Escritura |
| `set_journey_reentry` | Cambie la configuración de reentrada. | Escritura |
| `set_journey_split_conditions` | Establecer condiciones de bifurcación dividida. | Escritura |
| `apply_journey_rules` | Aplique `rule_data` para condiciones, acciones, eventos y la audiencia de lista dinámica a un recorrido. | Escritura |
