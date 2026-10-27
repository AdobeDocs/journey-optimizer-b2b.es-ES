---
title: Documentación de Adobe Journey Optimizer B2B Edition
description: 'Documentación completa de Journey Optimizer B2B Edition: explore los recursos disponibles para la incorporación, la creación de grupos de compras, la creación de recorridos de cuenta y la administración de contenido.'
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
autotag-review: 2026-03-27T22:18:45.397Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
    internal-label: Onboarding
TQID: https://experienceleague.adobe.com/BK-uFYGIZyqRNy4Gx-vJB-oy3q8zpjERIoJwBvgofUY
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 26%
---
# Documentación de Adobe Journey Optimizer B2B Edition

[!DNL Adobe Journey Optimizer B2B Edition] es una aplicación única que permite a los equipos de marketing y ventas organizar experiencias basadas en cuentas y calificar grupos de compra para productos específicos en todo el ciclo de vida del cliente. Utiliza IA para atraer y calificar a los grupos de compra dentro de las cuentas de destino, lo que ayuda a sus equipos a generar un flujo de trabajo de mayor calidad y a diseñar mejores estrategias de adquisición, expansión y retención. También permite compartir perspectivas entre los equipos de ventas y marketing.

Esta documentación proporciona información para dominar la aplicación. Está diseñado para especialistas en marketing, representantes de desarrollo empresarial, analistas de datos y administradores operativos.

## Novedades

Revise este ejemplo de las últimas adiciones y mejoras en la aplicación y documentación de [!DNL Journey Optimizer B2B Edition].

>[!BEGINTABS]

>[!TAB recorridos de personas]

Orqueste marketing basado en posibles clientes con recorridos de persona, que utilizan audiencias y datos de [!DNL Adobe Experience Platform] para atraer a personas individuales. Los recorridos de personas ahora admiten _Escuchar un evento_, acciones externas, nodos de rutas divididas externas y reentrada de recorrido. Utilícelos junto con los recorridos de la cuenta y los grupos de compra para organizar el recorrido completo de compra.

[!BADGE Más información]{type=Informative url="/help/user/journeys/journeys-overview.md" tooltip="Más información sobre los recorridos de persona"}

>[!TAB Rutas divididas de variante]

Pruebe las variaciones dentro de un recorrido de cuenta o persona asignando cuentas o personas a diferentes rutas de recorrido en función de los porcentajes definidos. En los recorridos de las personas, la asignación es determinista, por lo que cada persona siempre sigue el mismo camino, lo que permite realizar experimentos controlados.

[!BADGE Más información]{type=Informative url="/help/user/journeys/variant-split-paths-nodes.md" tooltip="Obtenga información sobre las rutas divididas de variante"}

>[!TAB Canal de WhatsApp]

Cuando los desarrolladores y los administradores de productos configuran una integración con una cuenta de Meta Business Manager, los especialistas en marketing pueden incluir mensajes de WhatsApp como un canal de contenido en los recorridos de cuenta mediante la API de Meta Cloud. WhatsApp se une al correo electrónico y los SMS como un canal disponible para enviar contenido de recorrido directamente a los miembros de la cuenta.

[!BADGE Más información]{type=Informative url="/help/user/admin/configure-channels-whatsapp.md" tooltip="Más información sobre el canal de WhatsApp"}

>[!TAB Modelos de IA generativa]

Los diseñadores de correo electrónico ahora pueden seleccionar entre modelos estándar de [!DNL Firefly], modelos personalizados de [!DNL Firefly] formados en recursos específicos de marca y modelos de imagen de terceros aprobados al generar imágenes para contenido de correo electrónico. Esta selección proporciona a los equipos control sobre qué modelo se adapta a su escenario de diseño específico, desde las necesidades de contenido general hasta los casos de uso especializados o de marca.

[!BADGE Más información]{type=Informative url="/help/user/content/generative-ai-models.md" tooltip="Obtenga información acerca de la selección de modelos de IA generativa"}

>[!TAB Optimización del tiempo de envío]

Para _Enviar correo electrónico_ nodos de acción en recorridos de persona, ahora puede utilizar la optimización del tiempo de envío para personalizar el tiempo de envío del correo electrónico. El sistema predice cuándo es más probable que interactúe cada persona y programa la entrega en consecuencia, en lugar de enviarlo a todos los destinatarios al mismo tiempo.

[!BADGE Más información]{type=Informative url="/help/user/content/email-send-time-optimization.md" tooltip="Obtenga información acerca de la optimización del tiempo de envío"}

>[!TAB reentrada de Recorrido]

Ahora puede enviar cuentas o personas a través de un recorrido de cuenta o persona varias veces. La reentrada aborda varios escenarios, como la reevaluación de los criterios de cualificación y los flujos de trabajo de nutrición reutilizables. Utilice la configuración de reentrada para establecer criterios, límites y tiempos de espera para que las cuentas o personas se vuelvan a calificar para el recorrido de forma controlada.

[!BADGE Más información]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="Obtenga información acerca de la reentrada al recorrido"}

>[!ENDTABS]

## Empiece a explorar {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=es)

Últimas notas de la versión

Manténgase al día con las últimas notas de la versión, las nuevas características y las mejoras de [!DNL Adobe Journey Optimizer B2B Edition].

[Ver notas de la versión](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=es)

Introducción

Revise la guía de incorporación de [!DNL Journey Optimizer B2B Edition] para administradores y especialistas en marketing.

[Administradores](./setup-ultimate.md)
[Usuarios](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

Administrar sus datos

Active los esquemas XDM y los campos que desee utilizar en [!DNL Adobe Journey Optimizer B2B Edition] y aprenda cómo funcionan sus datos en [!DNL Adobe Experience Platform].

[Ver administración de campos XDM](./admin/xdm-field-management.md)
[Conjuntos de datos exportados](./data/aep-exported-datasets.md)
[Consultas de conjuntos de datos](./data/aep-query-examples.md)
[Disponibilidad de datos y tiempo de sincronización](./data/data-availability-timing.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=es)

Canales de comunicación

Configure y administre correo electrónico, SMS, WhatsApp y otros canales para interacciones personalizadas con los clientes.

[Configurar canal de correo electrónico](./admin/configure-channels-emails.md)
[Configurar el canal SMS](./admin/configure-channels-sms.md)
[Configurar el canal de WhatsApp](./admin/configure-channels-whatsapp.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=es)

Creación de un recorrido

Diseñe, organice, administre y optimice recorridos personalizados de cuenta y persona.

[Explorar Recorridos](./journeys/journeys-overview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg?lang=es)

Comprender la compra de grupos

Directrices detalladas sobre la creación, gestión y optimización de grupos de compra para una segmentación eficaz.

[Más información sobre la compra de grupos](./buying-groups/buying-groups-overview.md)
:::

::::

<!--
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg?lang=es)

Design Content

Learn how to author and manage content for personalized customer experiences orchestrated through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## Demostración general

Obtenga información acerca de los componentes de un grupo de compras y los conceptos básicos para crear un recorrido de cuenta.

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## Explorar la documentación

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px" alt="Introducción"><br/>
      <strong>Introducción</strong><br/><a href="home-page.md">Inicio de sesión y página de inicio</a><br/><a href="./start/get-started.md">Guía de incorporación</a> <br/><a href="./ai-coworker/ai-overview.md">Funciones de IA</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon_audience.svg" width="35px" alt="Grupos de compras"><br/>
      <strong>Grupos de compras</strong><br/><a href="./buying-groups/buying-groups-overview.md">Información general de los grupos de compra</a><br/><a href="./buying-groups/buying-groups-role-templates.md">Plantillas de funciones</a><br/><a href="./buying-groups/solution-interests.md">Intereses de la solución</a><br/><a href="./buying-groups/buying-groups-create.md">Crear grupos de compras</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-paths.svg" width="35px" alt="Recorridos de la cuenta"><br/>
      <strong>Recorridos de cuenta</strong><br/><a href="./journeys/journeys-overview.md">Información general de recorridos</a><br/><a href="./journeys/create-publish-journey.md#create-a-journey">Crear un recorrido de cuenta</a><br/><a href="./journeys/journey-nodes.md">Nodos de recorrido</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-campaign.svg" width="35px" alt="Contenido del recorrido"><br/>
      <strong>Contenido de Recorrido</strong><br/><a href="./content/add-email.md">Canal de correo electrónico</a><br/><a href="./content/generate-content-emails.md">Generar contenido de correo electrónico</a><br/><a href="./content/genstudio-email-workflow.md">Experiencias de correo electrónico de GenStudio</a><br/><a href="./content/sms-authoring.md">Canal de SMS</a>
    </td>
        <td>
      <img src="../assets/do-not-localize/icon_assets.svg" width="35px" alt="Administración de contenido"><br/>
      <strong>Administración de contenido</strong><br/><a href="./content/assets-overview.md">Información general de Assets</a><br/><a href="./content/email-templates.md">Plantillas de correo electrónico</a><br/><a href="./content/fragments.md">Fragmentos visuales</a><br/><a href="./content/conditional-content.md">Contenido condicional</a><br/><a href="./content/brand-themes.md">Temas de marca</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-offer.svg" width="35px" alt="Información y paneles de control"><br/>
      <strong>Información</strong><br/><a href="./dashboards/intelligent-dashboard.md">Panel inteligente</a><br/><a href="./dashboards/engagement-dashboard.md">Panel de participación</a><br/><a href="./dashboards/buying-groups-dashboard.md">Panel de grupos de compras</a><br/><a href="./dashboards/journeys-dashboard.md">Panel de Recorridos</a><br/><a href="./buying-groups/incrm-insights.md">Información en CRM</a>
    </td>

</tr>
</table>

>[!BEGINSHADEBOX]

## [!DNL Marketo Qualifier]

[!DNL Adobe Marketo Qualifier] es una aplicación controlada por IA que puede usar con [!DNL Journey Optimizer B2B Edition]. Implementa la aptitud de la calificación de la cuenta y está diseñado para optimizar los flujos de trabajo para los representantes del desarrollo empresarial (BDR). [!DNL Marketo Qualifier] automatiza los flujos de trabajo de cualificación de clientes potenciales, alcance y participación del comprador en todos los canales. Reduce la carga manual de BDR y acelera la velocidad de la canalización para las empresas B2B empresariales.

Para obtener más información, consulte la [documentación de Marketo Qualifier](https://experienceleague.adobe.com/es/docs/marketo-qualifier/using/home){target="_blank"}.

>[!ENDSHADEBOX]

## Recursos adicionales

<table style="table-layout:fixed">
<tr><td><strong>Adobe Journey Optimizer B2B Edition</strong><br/>
<a href="https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">Vídeos y tutoriales</a> - <a href="https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=es" target="_blank">Descripción del producto</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=es" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/es/docs/experience-platform/landing/home" target="_blank">Documentación</a> - <a href="https://business.adobe.com/es/products/experience-platform/documentation-and-developer-resources.html" target="_blank">Recursos para desarrolladores</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/es/docs/experience-platform/rtcdp/home" target="_blank">Documentación</a> - <a href="https://experienceleague.adobe.com/es/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">Tutoriales para desarrolladores</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/es/docs/marketo/using/home" target="_blank">Documentación del usuario</a> - <a href="https://experienceleague.adobe.com/es/docs/marketo-developer/marketo/home" target="_blank">Documentación para desarrolladores</a>
</td>
</tr></table>
