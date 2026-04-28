---
user-guide-title: Documentación de la edición B2B de Journey Optimizer
user-guide-description: Obtenga información acerca de la edición B2B de Adobe Journey Optimizer y cómo puede utilizarla para organizar los recorridos de la cuenta y de los grupos de compra mediante la IA generativa integrada y automatización líder del sector.
source-git-commit: 230933fe205b565aa55f4a1fb371704f996d1bb3
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 92%

---


# Guía del usuario de Journey Optimizer B2B Edition {#user}

+ [Documentación de Adobe Journey Optimizer B2B Edition](guide-overview.md)
+ [Notas de la versión](./release-notes/release-notes.md)
+ Introducción {#get-started}
   + [Información general de Journey Optimizer B2B Edition](about-journey-optimizer-b2b-edition.md)
   + Configuración del entorno {#admin-setup}
      + [Configurar lista de comprobación](./setup-ultimate.md)
      + [Espacios de nombres y esquemas](./data/namespaces-schemas.md)
      + [Selección de campo XDM](./admin/xdm-field-management.md)
      + [Campos y eventos de experiencia](./admin/configure-aep-events.md)
      + [Dominios de marca](./start/branding-domains.md)
      + [Seguimiento y envío de correo electrónico](./start/email-protocols.md)
      + [Configuración de correo electrónico](./start/email-setup.md)
      + [Acciones del recorrido de Marketo Engage](./admin/marketo-actions-connect.md)
      + [Administración de usuarios](./admin/user-management.md)
   + [Incorporación del usuario](./start/get-started.md)
   + [Inicio de sesión y página de inicio](home-page.md)
+ Asistente de IA {#ai-assistant}
   + [Información general](./ai-assistant/ai-assistant-overview.md)
   + [Habilitar el acceso al Asistente de IA](./ai-assistant/enable-ai-assistant-access.md)
   + [Guía de preguntas](./ai-assistant/question-guidance.md)
   + [Utilizar el Asistente de IA](./ai-assistant/use-ai-assistant.md)
   + [IA generativa para contenido](./ai-assistant/generative-ai-content.md)
   + Agentes {#ai-agents}
      + [Audience Agent B2B](./agents/audience-agent-b2b.md)
      + [Journey Agent B2B](./agents/journey-agent.md)
      + [Calificador de ventas](./agents/sales-qualifier.md)
+ administración de recorrido {#journeys}
   + [Recorridos de cuenta y persona](./journeys/journeys-overview.md)
   + [Creación y publicación de un recorrido](./journeys/create-publish-journey.md)
   + [reentrada de recorrido](./journeys/journey-re-entry.md)
   + {hide-from-toc}[nodos de Recorrido](./journeys/journey-nodes.md)
   + Nodos del recorrido {#journey-nodes}
      + [Público de cuenta](./journeys/account-audience-nodes.md)
      + [Audiencia de personas (Beta)](./journeys/person-audience-nodes.md)
      + [Iniciar una acción](./journeys/action-nodes.md)
      + [Escuchar un evento](./journeys/listen-for-event-nodes.md)
      + [Dividir y combinar rutas](./journeys/split-merge-paths-nodes.md)
      + [Espera](./journeys/wait-nodes.md)
      + [Nodos externos](./journeys/external-nodes.md)
   + [Detalles del recorrido](./journeys/journey-details.md)
+ Contenido del recorrido {#journey-content}
   + [Canal de SMS](./content/sms-authoring.md)
   + [Canal de WhatsApp](./content/whatsapp-authoring.md)
   + Canal de correo electrónico {#email-channel}
      + [Añadir un correo electrónico](./content/add-email.md)
      + [Optimización del tiempo de envío](./content/email-send-time-optimization.md)
      + [Creación del correo electrónico](./content/email-authoring.md)
      + [Asistente de IA para la creación de correo electrónico](./content/ai-assistant-emails.md)
      + [Flujos de trabajo de GenStudio](./content/genstudio-email-workflow.md)
      + [Modo oscuro para el diseño del correo electrónico](./content/email-dark-mode.md)
      + [Plantillas gobernadas](./content/email-authoring-governance.md)
      + [Correo electrónico de alerta de ventas](./content/sales-alert-email.md)
      + [Deduplicación de correo electrónico](./content/email-deduplication.md)
   + Canal web (Beta) {#web-channel}
      + [Información general](./content/web-experiences.md)
      + [Diseño de experiencia web](./content/web-experience-design.md)
      + [Aplicaciones de una sola página](./content/web-single-page-applications.md)
   + [Tókenes personalizados](./content/personalization-my-tokens.md)
+ Públicos {#audiences}
   + [Audiencias de Experience Platform](./audiences/account-audience-overview.md)
   + [Audiencias externas de destino](./audiences/target-external-audience.md)
   + [Audiencias coincidentes con cuentas de LinkedIn](./data/linkedin-account-matched-audiences.md)
   + [Campos XDM predeterminados](./admin/field-mapping.md)
+ Cuentas {#accounts}
   + Grupos de compras {#buying-groups}
      + [Información general](./buying-groups/buying-groups-overview.md)
      + [Interés de la solución](./buying-groups/solution-interests.md)
      + [Plantillas de funciones](./buying-groups/buying-groups-role-templates.md)
      + [Funciones predeterminadas y personalizadas](./buying-groups/default-custom-roles.md)
      + [Datos de la función](./buying-groups/buying-group-role-insights.md)
      + Puntuación del grupo de compras {#scoring}
         + [Puntuaciones de participación](./buying-groups/engagement-scores.md)
         + [Puntuaciones de integridad](./buying-groups/completeness-scores.md)
      + [Fases del grupo de compras](./buying-groups/buying-group-stages.md)
      + [Creación de los grupos de compra](./buying-groups/buying-groups-create.md)
      + [Exportación de cuentas](./audiences/account-list-export.md)
      + [Filtros del grupo de compras en Marketo Engage](./buying-groups/marketo-engage-smart-list-buying-group-filters.md)
      + [Perspectivas en CRM](./buying-groups/incrm-insights.md)
   + Listas de cuentas {#account-lists}
      + [Información general](./accounts/account-lists.md)
      + [Uso en recorridos y programas](./accounts/account-lists-journeys.md)
   + Experiencia en ventas {#sales-experience}
      + [Detalles de la cuenta](./accounts/account-details.md)
      + [Detalles del grupo de compras](./buying-groups/buying-group-details.md)
      + [Detalles de la persona](./accounts/person-details.md)
      + [Vinculación de CRM](./accounts/crm-linking.md)
+ Administración de contenido {#content-management}
   + Correos electrónicos {#emails}
      + [Trabajo con contenido multilingüe](./content/emails-list.md)
      + Vista previa y validación {#preview}
         + [Simular contenido](./content/email-simulate-content.md)
         + [Prueba de representación de correo electrónico](./content/email-test-rendering.md)
         + [Informe de spam](./content/email-spam-report.md)
      + [Colaboración por correo electrónico](./content/email-collaboration-tools.md)
   + Recursos {#assets}
      + [Información general](./content/assets-overview.md)
      + Activos internos {#internal-dam}
         + [Uso de recursos internos](./content/internal-image-assets.md)
         + [Edición de imágenes con Adobe Express](./content/image-edit-adobe-express.md)
      + [Recursos de imágenes de Experience Manager](./content/aem-assets.md)
   + Plantillas {#templates}
      + [Gobernanza de contenido](./content/template-content-governance.md)
      + Plantillas de correo electrónico {#email-templates}
         + [Información general](./content/email-templates.md)
         + [Creación de plantilla de correo electrónico](./content/email-template-authoring.md)
         + [Edición avanzada de HTML](./content/email-template-advanced-html.md)
         + [Convertir imagen en plantilla](./content/email-template-image-convert.md)
      + Plantillas de la página de destino (beta) {#landing-page-templates}
         + {hide-from-toc}[Información general](./content/landing-page-templates.md)
         + [Diseño de plantilla de la página de destino](./content/landing-page-template-design.md)
   + Fragmentos {#visual-fragments}
      + [Información general](./content/fragments.md)
      + [Creación de fragmentos](./content/fragment-authoring.md)
   + Forms (Beta) {#forms}
      + [Información general](./content/forms.md)
      + [Diseño de formulario](./content/form-design.md)
   + Páginas de aterrizaje (Beta) {#landing-pages}
      + [Información general](./content/landing-pages.md)
      + [Diseño de la página de destino](./content/landing-page-design.md)
      + [Asistente de IA para el contenido de páginas de aterrizaje](./content/ai-assistant-landing-pages.md)
   + Herramientas de diseño de contenido {#content-design}
      + [Componentes de estructura](./content/structure-components.md)
      + [Componentes de contenido](./content/content-components.md)
      + [CSS personalizado](./content/design-custom-css.md)
   + Marcas (Beta) {#brands}
      + [Información general](./content/brands-overview.md)
      + [Administrar y crear](./content/brands-manage-create.md)
      + [Modelos de IA generativa](./content/generative-ai-models.md)
   + [Temáticas de marca](./content/brand-themes.md)
   + [Evaluación de contenido](./content/content-evaluation.md)
   + [Contenido condicional](./content/conditional-content.md)
   + [Accesibilidad de contenido](./content/accessible-content.md)
   + Personalización {#personalization}
      + [Información general](./content/personalization.md)
      + [Sintaxis de personalización](./content/personalization-syntax.md)
      + [Lista de funciones del asistente](./content/personalization-helper-functions.md)
+ Paneles inteligentes {#dashboards}
   + [Panel de perspectivas](./dashboards/intelligent-dashboard.md)
   + [Tablero de participación](./dashboards/engagement-dashboard.md)
   + [Panel de participación web](./dashboards/web-engagement-dashboard.md)
   + [Panel de grupos de compra](./dashboards/buying-groups-dashboard.md)
   + [Panel de Recorridos de cuenta](./dashboards/journeys-dashboard.md)
+ Administración {#admin}
   + [Gobernanza](./admin/governance.md)
   + [Asignación de persona](./admin/persona-mapping.md)
   + Configuraciones {#configurations}
      + [Repositorios de AEM Assets](./admin/configure-aem-repositories.md)
      + [Datos de intención](./admin/intent-data.md)
      + [Ponderación de puntuación de participación](./admin/engagement-score-weighting.md)
      + [Acciones externas](./admin/configure-external-actions.md)
   + Canales {#channels}
      + [Configuraciones de correo electrónico](./admin/configure-channels-emails.md)
      + [Configuración de SMS](./admin/configure-channels-sms.md)
      + [Configuraciones de WhatsApp](./admin/configure-channels-whatsapp.md)
      + [Configuraciones del canal web (Beta)](./admin/configure-channels-web.md)
      + [Configuración de la página de aterrizaje (Beta)](./admin/landing-page-settings.md)
      + {hide-from-toc}[Configurar flujos de datos para la colección de eventos](./data/aep-event-collection.md)
