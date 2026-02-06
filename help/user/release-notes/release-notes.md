---
title: Notas de la versión de Journey Optimizer B2B Edition
description: Descubra las últimas funciones, mejoras y correcciones de errores de Adobe Journey Optimizer B2B edition. Manténgase actualizado de las nuevas funciones y mejoras del producto.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 204b293d3bc526b139f68766ed45ff549a74ed34
workflow-type: tm+mt
source-wordcount: '4085'
ht-degree: 86%

---

# Notas de la versión de Journey Optimizer B2B Edition

Adobe Journey Optimizer B2B Edition ofrece continuamente correcciones de errores, nuevas funciones, mejoras en las existentes.

Journey Optimizer B2B Edition está desarrollado de forma nativa sobre [!DNL Adobe Experience Platform] y hereda de él sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/latest){target="_blank"}.

Revise la [descripción del producto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=es){target="_blank"} para obtener información sobre los derechos, las protecciones del rendimiento y las limitaciones.

## Funciones de la IA agéntica

Las siguientes funciones de IA agéntica ya están disponibles en Journey Optimizer B2B edition en la interfaz del asistente de IA:

| Agente | Actualización | Descripción |
| ----- | ------ | ----------- |
| Journey Build Agent | Nuevo y actualizado | Journey Build Agent analiza, idea y crea recorridos de forma conjunta en tiempo real, lo que permite a los especialistas en marketing iniciar sesión más rápido, mejorar la participación y generar tasas de conversión más altas. [Más información](../agents/journey-agent.md) |
| Audience Agent | Nuevo | Audience Agent identifica y crea automáticamente grupos de compra con datos estructurados y no estructurados. Ayuda a los especialistas en marketing a dirigirse a las personas adecuadas de forma más rápida y precisa. [Más información](../agents/audience-agent-b2b.md) |
| Calificador de ventas | Nuevo | El cualificador de ventas es una aplicación complementaria de Adobe Journey Optimizer B2B edition basada en IA que contiene Account Qualification Agent y que está diseñada para optimizar los flujos de trabajo de los representantes de desarrollo empresarial (BDR). Automatiza los flujos de trabajo de calificación de clientes potenciales, alcance y participación del comprador en todos los canales [Más información](../agents/sales-qualifier.md) |

## Notas de la versión 2026.1

**Fecha de implementación**: miércoles, 03 de febrero de 2026

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Kits de marca | (Beta) Defina una marca en Journey Optimizer B2B edition para proporcionar la fuente fiable que su equipo creativo pueda utilizar cuando cree contenido visual o escrito. Cuando se compilan estas directrices y se comparten los recursos de marca, cualquier miembro del equipo o colaborador puede crear contenido sin marca para el producto. |
| Función | Marcas para la generación de contenido de correo electrónico | Puede definir las directrices de marca y utilizar esta información para generar contenido de correo electrónico. Con esta función, el contenido del correo electrónico se alinea con las directrices de redacción, los estilos y el tono específicos de la marca. |
| Mejora | Recorrido _Esperar_ nodo - configuración avanzada | Para un nodo _Wait_ en un recorrido, ahora puede especificar días y horas de salida y seleccionar zonas horarias. Esta mejora le permite un mejor control de la orquestación de recorrido y el tiempo de campaña. |
| Mejora | Filtro especial Miembro del grupo de compra - Se ha eliminado la restricción | El filtro especial _[!UICONTROL Miembro del grupo de compra]_ ahora incluye la restricción _Se ha eliminado_. Cuando se añade esta restricción al filtro, se pueden incluir o excluir los miembros del grupo comprador que se han eliminado. También se admite en las listas inteligentes de Marketo Engage, donde puede utilizar esta nueva restricción en el filtro _[!UICONTROL Miembro del grupo de compra]_. |
| Mejora | Diseño de correo electrónico: viñetas de varios niveles | Las herramientas del espacio de diseño de contenido de correo electrónico ahora admiten subviñetas (niveles de viñeta). |

<!--
| Feature | Custom external actions for journeys | [!BADGE Simplfified architecture]{type=Informative tooltip="Available for simplified architecture"} (Beta) Developers can now use APIs to  build integrations with their first-party systems. | 
| -->

>[!NOTE]
>
>Los cambios en la versión comienzan a implementarse el miércoles, 03 de febrero de 2026, con un despliegue gradual de cada función. Las fechas de lanzamiento de las funciones y mejoras están sujetas a cambios.

## Notas de la versión 2025.10

**Fecha de implementación**: 31 de octubre de 2025

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Activar en destino para recorridos | Use la nueva acción _Activar en la cuenta de compañía de destino_ para activarla directamente en empresas, en lugar de en personas. (Limitado en esta versión a las empresas de LinkedIn). [Más información](../journeys/action-nodes.md#activate-to-a-linkedin-destination) |
| Función | Temáticas de marca | Con los temáticas de marca, los usuarios no técnicos ahora pueden crear contenido reutilizable que se ajuste a una marca y un lenguaje de diseño específicos añadiendo un estilo personalizado sobre las plantillas estándar. [Más información](../content/brand-themes.md) |
| Función | Plantillas de correo electrónico: convertir imagen a HTML | Ahora puede utilizar los archivos de diseño almacenados como archivos de imagen JPG o PNG y generar automáticamente plantillas de correo electrónico. [Más información](../content/email-template-image-convert.md) |
| Función | Asignación de persona | Asocie miembros de cuenta con personas establecidas con asignación de atributos. [Más información](../admin/persona-mapping.md) |
| Función | Perspectivas de ventas para Salesforce y Dynamics | Los integrantes del equipo de ventas ahora pueden ver los grupos de compras de vencimiento y las perspectivas relacionadas dentro de una integración de Salesforce o Dynamics para identificar nuevas oportunidades. Se incluyen los detalles del grupo comprador, como etapa, puntuación y miembros relacionados. [Más información](../buying-groups/incrm-insights.md) |
| Función | Activar audiencia en [!DNL Adobe Target] | Ahora puede activar una audiencia de un recorrido de cuenta a una audiencia de cliente externa y enviarla a [!DNL Adobe Target]. Con esta integración, puede ofrecer una audiencia cualificada mediante una secuencia de recorrido para una experiencia web diseñada en [!DNL Target]. [Más información](../audiences/target-external-audience.md) |
| Función | Panel de participación web | Un nuevo tablero que proporciona perspectivas sobre cómo los visitantes web interactúan con el contenido clave. Segmenta los datos en los sectores y regiones de las cuentas para ayudarle a comprender las tendencias de participación. [Más información](../dashboards/web-engagement-dashboard.md) |
| Función | Panel de perspectivas de rol | El nuevo panel _[!UICONTROL Perspectivas de funciones]_ proporciona información sobre cómo las campañas y los recorridos influyen en la adquisición de roles de grupo y en la participación. [Más información](../buying-groups/buying-group-role-insights.md) |
| Mejora | Puntuación de integridad del grupo de compra mejorada | Ahora puede asegurarse de que los grupos de compra reflejen la toma de decisiones real con umbrales de miembros de roles personalizables para la puntuación de integridad.  [Más información](../buying-groups/completeness-scores.md) |
| Mejora | Trabajos de mantenimiento de grupos de compras | La frecuencia del trabajo de mantenimiento del grupo de compras se actualiza semana a semana o día a día. |
| Mejora | Progreso del recorrido de cuenta | Para un recorrido publicado con el estado _Activo_, _Cerrado a nuevas entradas_, _Anulado_ o _Finalizado_, puede abrir el mapa del recorrido para revisar una lista de cuentas de cada nodo de recorrido. |

>[!NOTE]
>
>Los cambios en la versión comienzan a implementarse el 31 de octubre de 2025, con un despliegue gradual de cada función. Las fechas de lanzamiento de las funciones y mejoras están sujetas a cambios.

### Arquitectura simplificada

Adobe Journey Optimizer B2B Edition ya está disponible con una arquitectura simplificada. Con esta arquitectura actualizada, Journey Optimizer B2B Edition y Marketo Engage ya no están en el mismo sistema y en el mismo almacén de datos. Journey Optimizer B2B Edition solamente recibe datos de Adobe Experience Platform. Sin embargo, sigue dependiendo de los derechos de Marketo Engage y algunas funciones de configuración para aprovisionar y configurar el sistema.

Esta arquitectura actualizada ofrece varias ventajas:

* **Unifique y escale fácilmente sus datos**: la plataforma actualizada admite modelos de datos complejos, incluidos objetos personalizados, grupos de compra y eventos de cuenta.
* **Conecte varias instancias de Adobe Marketo Engage**: administre y unifique datos de varios entornos de Adobe Marketo Engage en un solo lugar.
* **Mantenga sus datos seguros**: las características avanzadas de privacidad y seguridad ayudan a proteger la información de sus clientes.
* **Creada para el futuro**: esta actualización prepara a su organización para recibir mejoras e innovaciones continuas.

>[!NOTE]
>
>Si su entorno está aprovisionado en esta arquitectura, revise las [directrices para la configuración](../simplified-architecture.md).

Con la arquitectura simplificada, las siguientes nuevas funciones y mejoras están disponibles en la versión 2025.10:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Modelo de datos relacionales | Aproveche los datos relacionales vinculados a cuentas B2B para filtrar cuentas dentro de un recorrido de cuentas o personalizar el contenido del correo electrónico. Estos datos relacionales pueden representar entidades comerciales reales, como registros de compras, registros de eventos, licencias de software, suscripciones a servicios o reservas. [Más información](../admin/xdm-field-management.md#relational-schemas) |
| Función | Varias activaciones de Marketo Engage | Configure conexiones a instancias de Marketo Engage remotas y utilice esas conexiones para configurar acciones de Marketo Engage para recorridos. Estas acciones, como añadir o eliminar personas de listas o añadir personas a una campaña de solicitud, se aplican a la instancia de Marketo Engage designada. [Más información](../admin/marketo-actions-connect.md) |
| Función | Deduplicación de fatiga del correo electrónico | Ahora puede habilitar la deduplicación de correos electrónicos para garantizar que el mismo correo electrónico no se envíe varias veces a la misma dirección en un recorrido. Las direcciones duplicadas se bloquean hasta que el primer registro con esa dirección de correo electrónico complete el recorrido.  [Más información](../content/email-deduplication.md) |
| Mejora | Límites de comunicación | El sistema ahora respeta los límites de comunicación combinados de Marketo Engage y Journey Optimizer B2B edition. [Más información](../admin/configure-channels-emails.md#communication-limits) |

<!-- There are additional functional changes with the simplified architecture:

| Item | Description |
| ---- | ----------- |
| Asset management | The system supports an internal asset repository where you can organize folders, edit images, import images, and remove images. It does not support Marketo Engage Design Studio workspaces for asset management. |
| | | -->

<!-- hold for later release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## Notas de la versión 2025.9

**Fecha de implementación**: 30 de septiembre de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Colaboración en el contenido de un correo electrónico | Ahora puede realizar comentarios sobre la colaboración con otros usuarios de Journey Optimizer B2B Edition en el contexto de un recurso de correo electrónico. Puede etiquetar a los integrantes del equipo para que reciban una notificación por correo electrónico con los detalles del comentario. La notificación también está disponible como notificación por pulsos. [Más información](../content/email-collaboration-tools.md) |
| Función | Modo oscuro para el diseño del correo electrónico | El espacio de diseño del correo electrónico ahora incluye la posibilidad de cambiar al _modo oscuro_. En el modo oscuro, puede obtener una vista previa del contenido del correo electrónico y definir la configuración personalizada que se mostrará específicamente para los destinatarios que visualicen sus correos electrónicos en el modo oscuro. [Más información](../content/email-dark-mode.md) |
| Mejora | Recorridos: dividir la ruta por el número de personas de la función | Utilice una ruta dividida por el nodo de cuenta para dirigirse a una cuenta con el número de personas en una o más funciones del grupo de compras. En la ruta, puede evaluar la preparación del grupo de compras en cuanto a las alertas de ventas y otras participaciones en función de la profundidad de la función. [Más información](../journeys/split-merge-paths-nodes.md#buying-group-filtering-for-accounts) |
| Mejora | Recorridos: filtros de personas para eventos | Utilice los filtros de personas para escuchar eventos relacionados con personas. Estos filtros incluyen la posibilidad de dirigirse a una función específica de un grupo de compras coincidente. [Más información](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) |

>[!NOTE]
>
>Los cambios en la versión comienzan a implementarse el 30 de septiembre de 2025, con un despliegue gradual de cada función. Las fechas de lanzamiento de las funciones y mejoras están sujetas a cambios.

## Notas de la versión 2025.8

**Fecha de implementación**: 26 de agosto de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Filtros de puntuación de participación de personas para plantillas de funciones y recorridos | Ahora puede usar la _puntuación de participación de personas_ como filtro en las plantillas de funciones que se usan para crear grupos de compras y en los nodos de recorrido de rutas divididas. [Más información](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| Función | Configuración de funciones personalizadas de grupos de compras | Ahora tiene la flexibilidad para configurar funciones personalizadas para grupos de compras, lo que le permite definir las funciones específicas de sus casos de uso. [Más información](../buying-groups/default-custom-roles.md) |
| Función | Configuración de ponderación de puntuación de participación | Ahora puede asignar un peso a las actividades que influyen en la puntuación de participación del grupo de compras. Esta función incluye la definición de sus propios modelos de puntuación personalizados y el cambio del modelo activo que influye en los cálculos de puntuación de participación. [Más información](../admin/engagement-score-weighting.md) |
| Mejora | Contenido condicional para fragmentos | Ahora puede utilizar las herramientas de contenido condicional para el diseño de fragmentos visuales. [Más información](../content/conditional-content.md) |
| Mejora | Actualizaciones de puntuación de participación | La lógica de puntuación de participación del grupo de compras se actualiza para normalizar las puntuaciones. Además, puede trabajar con puntuaciones de participación de nivel de miembro, así como puntuaciones de participación colectiva para todo el grupo de compras. [Más información](../buying-groups/engagement-scores.md) |
| Mejora | Observabilidad activa del recorrido: cuentas en cada nodo | Para un recorrido de cuentas activo, puede acceder a una lista de las cuentas que han llegado a cada nodo de cuenta del recorrido. |

## Notas de la versión 2025.6

**Fecha de implementación**: 15 de julio de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Integración con GenStudio for Performance Marketing | (Disponibilidad limitada) Ahora puede integrar las experiencias de correo electrónico de GenStudio for Performance Marketing con Journey Optimizer B2B Edition para mejorar la eficacia del marketing y mantener la coherencia de la marca. Con esta integración, puede combinar la creación de contenido con tecnología de IA de GenStudio con las funciones de orquestación avanzadas de Journey Optimizer B2B Edition. [Más información](../content/genstudio-email-workflow.md) |
| Función | Informes de detección de spam | Para evitar los filtros de spam y asegurarse de que los mensajes se envíen a las bandejas de entrada del público, puede generar un _informe de spam_ directamente en el espacio de diseño del correo electrónico. [Más información](../content/email-spam-report.md) |
| Función | Página de detalles de la persona | Ahora puede hacer clic en el nombre de una persona cuando se muestre (como hipervínculo) en el panel de control inteligente, la página de detalles del grupo de compras y la página de detalles de la cuenta. Esta acción abre la página de detalles de la persona asociada, con información sobre el contacto, su actividad y los grupos de compras más activos. [Más información](../accounts/person-details.md) |
| Función | Acciones de la cuenta y del grupo de compras | Realice acciones directamente desde las páginas de detalles de la cuenta y del grupo de compras para lograr una participación oportuna e intencional. <li>Use la acción _Enviar correo electrónico_ para enviar un correo electrónico de Marketo Engage aprobado a los contactos de la cuenta seleccionada o a miembros del grupo de compras. [Más información](../accounts/account-details.md#send-emails) <li>De los detalles del grupo de compras, las acciones también incluyen _Asignar un nuevo miembro_, _Quitar un miembro_ y _Editar una función_. [Más información](../buying-groups/buying-group-details.md#members-tab) |
| Función | Acceso en CRM a las páginas de detalles | Ahora puede configurar vínculos directos a las páginas de detalles de Journey Optimizer B2B Edition para cuentas, contactos y posibles clientes en su herramienta CRM (Customer Relationship Management) como Salesforce o Microsoft Dynamics. [Más información](../accounts/crm-linking.md) |
| Función | Compatibilidad con CSS personalizado para el diseño de contenido | Ahora puede añadir su propio CSS personalizado cuando cree contenido para correos electrónicos y páginas de destino en el espacio de diseño. [Más información](../content/design-custom-css.md) |
| Función | Más información sobre la configuración de asignación de palabras clave de intenciones | Para activar y gestionar el modelo de detección de intenciones, ahora puede cargar una hoja de cálculo para definir una categoría de asignación de datos de intenciones. [Más información](../admin/intent-data.md) |
| Mejora | Simular contenido desde el resumen del correo electrónico | Ahora puede acceder a las herramientas _Simular contenido_ desde el resumen del correo electrónico (detalles y propiedades) al abrir un mensaje de correo electrónico desde la lista de correos electrónicos. Este acceso se suma al espacio de diseño del correo electrónico. [Más información](../content/email-simulate-content.md#display-the-email-preview) |
| Mejora | Visualización del recuento total para la lista de plantillas de funciones | La página de la lista _[!UICONTROL Plantillas de las funciones]_ se ha mejorado con la visualización del recuento total junto a la barra de búsqueda. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## Notas de la versión 2025.5

**Fecha de implementación**: 3 de junio de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Pruebas de correo electrónico con Litmus | Con una [cuenta Litmus Enterprise](https://www.litmus.com/email-testing){target="_blank"}, ahora puede obtener una vista previa de la representación de su correo electrónico en clientes de correo electrónico populares desde Journey Optimizer B2B Edition. Esta integración le ayuda a garantizar que el contenido del correo electrónico tenga un aspecto impecable y funcione según lo diseñado en cada bandeja de entrada de correo electrónico. [Más información](../content/email-test-rendering.md) |
| Mejora | Duplicar correo electrónico | Al añadir un correo electrónico para un nodo de recorrido, ahora puede duplicar un correo electrónico existente. Modifique la configuración o el contenido del correo electrónico duplicado o déjelo intacto.  [Más información](../content/add-email.md#add-an-email-to-your-journey) |
| Mejora | Formato del token de Handlebar para correo electrónico | Los tokens de personalización para el contenido del correo electrónico ahora utilizan un formato actualizado que es totalmente compatible con los scripts de Handlebar. Este formato usa _palabras compuestas de mayúsculas y minúsculas_ o guiones bajos, lo que elimina espacios. [Más información](../content/email-authoring.md#content-authoring---personalization) |
| Mejora | Visualización del recuento total de listas | Las páginas de la lista _[!UICONTROL Intereses de la solución]_ y _[!UICONTROL Recorridos de cuenta]_ se han mejorado con la visualización del recuento total junto a la barra de búsqueda. |

## Notas de la versión 2025.4

**Fecha de implementación**: martes, 29 de abril de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Listas de cuentas | Ahora puede crear un lista de cuentas estáticas o dinámicas para identificar cuentas con nombre según sus criterios definidos, como el sector, la ubicación o el tamaño del compañía. <a href="../accounts/account-lists.md">Más información</a> |
| Función | Orquestación de recorrido de la lista de cuentas | Utilice los nodos de acción del recorrido para añadir y quitar cuentas para listas de cuentas estáticas. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">Más información</a> |
| Mejora | Filtrar abono de recorrido en Marketo Engage | Use las listas de cuentas de Adobe Journey Optimizer B2B Edition para el público del recorrido y luego use el filtro _Abonado de una lista de cuentas_ en las listas inteligentes de Marketo Engage. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">Más información</a> |
| Función | Filtros de inactividad | Organice los recorridos en función de la inactividad dentro de las campañas y programas de Marketo Engage, incluida la inactividad del correo electrónico, los momentos interesantes, los cambios en el valor de los datos y las páginas web visitadas. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">Más información</a> |
| Mejora | Filtro de páginas web visitadas | Organice los recorridos en función de la actividad de las páginas web visitadas asociadas con las campañas y programas de Marketo Engage. <a href="../journeys/split-merge-paths-nodes.md#people-path-filters">Más información</a> |
| Mejora | Lista de correos electrónicos | Vea una lista global de correos electrónicos activos y borrador para buscar, revisar y actualizar los correos en los recorridos de cuenta asociados. <a href="../content/emails-list.md">Más información</a> |

## Notas de la versión 2025.3

**Fecha de implementación**: 1 de abril de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Duplicar recorridos de cuenta | Ya está disponible una acción duplicada para recorridos de cuenta. Puede duplicar los detalles del recorrido de cuenta, o sencillamente un simple esqueleto de la estructura del flujo y la ruta. <a href="../journeys/journeys-overview.md#duplicate-journey">Más información</a> |
| Función | Mis tokens para los recorridos de la cuenta | Ahora puede definir un conjunto de tokens personalizados con valores que sean específicos del recorrido de la cuenta. Este conjunto de tokens personalizados se denomina _Mis tokens_ y cualquiera de estos tokens personalizados son para la personalización cuando se crean correos electrónicos del recorrido. <a href="../content/personalization-my-tokens.md">Más información</a> |
| Función | Eliminar fases del grupo de compras | Puede eliminar el modelo de fases del grupo de compras cuando esté en estado borrador o publicado. Si se publica (está activo), solo podrá eliminarlo si no está asociado a un interés de solución. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Más información</a> |
| Mejora | Recuentos del nodos del recorrido | Mayor visibilidad de los recuentos de abonos del recorrido publicados en el nivel de nodo. En el _Mapa del recorrido_, los nodos muestran el _[!UICONTROL Total de cuentas introducidas]_. Al seleccionar un nodo de acción, los detalles situados a la derecha también incluyen _[!UICONTROL Cuentas en las que aún no se ha actuado]_. Y los detalles del nodo _Escuchar un evento_ incluyen _[!UICONTROL Cuentas en este paso]_. Utilice esta información para validar la progresión de la cuenta en sus recorridos activos, finalizados y anulados. |

## Notas de la versión 2025.2

**Fecha de implementación**: 11 de marzo de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Campos personalizables: fragmentos de contenido | Durante el diseño de fragmentos visuales, puede designar parámetros para un componente del fragmento como editables. Esta función permite al autor del correo electrónico o la plantilla especificar un valor de campo personalizado específico para sus necesidades. Este indicador de personalización se limita a los componentes visuales de imagen, texto y botones. <a href="../content/fragment-authoring.md#enable-fragment-customization">Más información</a> |
| Función | Tipos de duplicación del recorrido | Cuando duplica el recorrido de una cuenta, puede incluir detalles del nodo, excluyendo los correos electrónicos y mensajes de SMS creados en Journey Optimizer B2B Edition. Como alternativa, puede crear una copia esqueleto de la estructura y los flujos de ruta, sin detalles del nodo ni ajustes. <a href="../journeys/journeys-overview.md#duplicate-journey">Más información</a> |
| Mejora | Cuatro plantillas de correo electrónico de muestra adicionales | La biblioteca de plantillas de correo electrónico de ejemplo ahora incluye cuatro plantillas de SecureFinancial como ejemplos para volver a participar, informar, alimentar y dar ejemplos de contenido de comentarios |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Notas de la versión 2025.1 {#Jan-2025}

**Fecha de implementación**: 6 de febrero de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Reenvío de eventos de experiencia | Los administradores pueden configurar definiciones de eventos basadas en Adobe Experience Platform (AEP). Estas configuraciones permiten a los especialistas en marketing crear recorridos de cuenta que reaccionan a los eventos de experiencia de AEP.  <a href="../admin/configure-aep-events.md">Más información</a> |
| Función | Destinos de medios de pago | Capacite a personas conocidas para campañas de medios de pago desde un recorrido de cuentas, de modo que pueda participar en plataformas de publicidad como LinkedIn. Utilice un nodo de rutas divididas para segmentar los públicos de cuenta en función de comportamientos específicos y para identificar cuentas que garanticen una participación adicional. A continuación, añada personas de esas cuentas a un público de cliente externo a través de Real-Time CDP a un destino de medios de pago admitido. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Más información</a> |
| Función | Panel de control inteligente | Vea la progresión de la compra de grupos a través de los recorridos de su cuenta, incluidas las perspectivas generadas por IA para un análisis más inteligente y una priorización precisa de la cuenta. <a href="../dashboards/intelligent-dashboard.md">Más información</a> |
| Función | Grupo de compras y detalles de la cuenta | Vea perspectivas en el nivel de grupo de compras y de cuenta para tener más contexto y datos históricos cuando empiece a interactuar con un cliente.<p>Los detalles del grupo de compras incluyen cualquier intención de origen que se detecte. <a href="../buying-groups/buying-group-details.md">Más información</a><p>Las cuentas de detalles de la cuenta resaltan el aumento en la participación detectada por intención, de modo que puede alertar a las ventas sobre cuentas que están listas para una participación personalizada centrada en las ventas.  <a href="../accounts/account-details.md">Más información</a> |
| Función | Información general sobre recorridos | Al acceder a los recorridos de la cuenta, la pestaña Información general ofrece una instantánea completa de los recorridos de la cuenta activa, en la que se detalla el progreso de la cuenta mediante diagramas de círculos y gráficos de barras que categorizan y cuantifican las finalizaciones y las actividades de participación.  <a href="../dashboards/journeys-dashboard.md">Más información</a> |
| Función | Edición de imágenes en Adobe Express | Las acciones rápidas de Adobe Express le permiten realizar ediciones sencillas (como recortar y cambiar el tamaño) en imágenes para conseguir un aspecto más pulido en el contenido. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Más información</a>  <p>Para obtener un conjunto más completo de herramientas de diseño, esta integración permite obtener una licencia completa de Adobe Express en Journey Optimizer B2B Edition. Con esta configuración, se puede acceder a la interfaz de usuario completa de Adobe Express desde el espacio de trabajo de recursos local. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Más información</a> |
| Función | Filtros de intención para funciones de grupo de compras | Al enviar las palabras clave por intención, el modelo de detección de intención predice una solución o producto de interés con una confianza lo suficientemente alta según la actividad de un posible cliente. <a href="../admin/intent-data.md">Más información</a> <p>Estos datos de intención están disponibles para definir las condiciones de función de grupo de compra <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a> |
| Mejora | Compatibilidad con eventos de Marketo Engage en recorridos | El nodo de recorrido _Escuchar evento_ ahora admite dos eventos de Marketo Engage en el nivel de personas: _Visita la página web_ y _Rellena el formulario_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Más información</a> |
| Mejora | Compra de filtros de grupo de compras para las listas inteligentes de Marketo Engage | Vea y cree listas inteligentes con filtros de grupo de compras en Marketo Engage. Estos filtros añadidos le permiten suprimir e incluir miembros del grupo de compra en campañas y programas de Marketo Engage desde recorridos de cuenta en Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Más información</a> |
| Mejora | Filtro de abono a listas de Marketo Engage para recorridos y funciones | En Journey Optimizer B2B, compruebe el abono a la lista Marketo Engage como condición para un nodo _split path by people_ para eliminar la duplicación en las actividades de recorrido. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Más información</a> <p> Para las plantillas de funciones de grupo de compras, utilice el abono a las listas como condición de función. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a> |
| Mejora | Panel de control de información general de participación | Este panel de control se actualiza para proporcionar una vista completa de la participación. Muestra métricas en tiempo real de interacciones de cuenta e individuales a través de gráficos de círculos de instantáneas y gráficos de líneas de tendencia reveladora a lo largo del tiempo. <a href="../dashboards/engagement-dashboard.md">Más información</a> |

## Versiones de 2024

Amplíe las siguientes listas para las funciones y mejoras de Journey Optimizer B2B Edition publicadas en 2024.

+++Notas de la versión de octubre de 2024

**Fecha de implementación**: 29 de octubre de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Contenido condicional en correos electrónicos | Personalice el contenido del correo electrónico en función del comportamiento del destinatario y las características del perfil, tanto a nivel de cuenta como de posible cliente. <p>A medida que crea un correo electrónico para el recorrido de la cuenta en el espacio de diseño visual de correo electrónico, utilice reglas condicionales para definir varias variantes para cualquier componente de contenido. <a href="../content/conditional-content.md">Más información</a> |
| Función | _Añada a la lista_ y _Quite de la lista_ acciones de personas en recorridos | Personalice el contenido del correo electrónico en función del comportamiento del destinatario y las características del perfil, tanto a nivel de cuenta como de posible cliente. <a href="../journeys/action-nodes.md">Más información</a> |
| Función | Gobernanza de contenido y bloqueo de componentes | Para garantizar el cumplimiento de los diseños de contenido aprobados, utilice las funciones de control de contenido para bloquear los componentes de contenido de plantillas de correo electrónico. Con la gobernanza de contenido activada en la plantilla de correo electrónico, los especialistas en marketing solo pueden modificar los elementos permitidos para mantenerla alineada con la estrategia de contenido. <a href="../content/template-content-governance.md">Más información</a> |
| Función | Fases del grupo de compras | Al definir y publicar un modelo de ensayo de grupos de compra personalizado, puede realizar un seguimiento de la progresión del grupo de compras a través de las fases del ciclo de vida del grupo de compras. Utilice estas fases para identificar las siguientes mejores acciones para miembros del grupo de compras. Puede configurar las reglas de transición y los nodos de recorrido que determinan la progresión de la fase y activan acciones en función de los cambios. <a href="../buying-groups/buying-group-stages.md">Más información</a> |
| Mejora | Nuevas plantillas de correo electrónico listas para usar | La biblioteca de plantillas de ejemplo ahora incluye plantillas de correo electrónico adicionales diseñadas para los especialistas en marketing B2B. Utilice estas plantillas de ejemplo como punto de partida y añada su propia personalización de marca y mensajería. <a href="../content/email-templates.md#select-a-design-template">Más información</a> |
| Mejora | Campos personalizados como atributos de persona | Si tiene campos de persona personalizados definidos en el esquema de público de cuenta en Experience Platform, estos campos también están disponibles para usarlos como atributos de persona en condiciones. Utilice estos atributos personalizados en lo siguiente: <li>Plantillas de funciones <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a></li><li>Dividir rutas por nodos de recorrido de personas <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Más información</a></li> |
| Mejora | Configuración del canal de correo electrónico | La configuración de correo electrónico ahora está visible en la interfaz de Journey Optimizer B2B Edition. Puede revisar rápidamente las configuraciones actuales y los administradores pueden hacer clic en _[!UICONTROL Editar configuración]_ para ir directamente a la configuración en Marketo Engage y actualizarla según los requisitos de su organización. <a href="../admin/configure-channels-emails.md">Más información</a> |

+++

+++Notas de la versión de septiembre de 2024

**Fecha de implementación**: 7 de octubre de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Mejora | Biblioteca de recursos central | La _biblioteca de recursos central_ mejorada le permite usar todos los recursos de imagen de su instancia de Marketo Engage en los espacios de trabajo de Design Studio. Existen protecciones integradas que impiden realizar ediciones en los recursos de Marketo Engage desde Journey Optimizer B2B Edition, así como eliminar y mover operaciones. Estas protecciones garantizan que los recursos de origen (Marketo Engage Design Studio) se mantengan, al tiempo que permiten una lectura y reutilización sin problemas en Journey Optimizer B2B Edition.<p>Para los recursos que se utilizan exclusivamente en Journey Optimizer B2B Edition, un espacio de trabajo específico proporciona funciones completas de administración de recursos. <a href="../content/internal-image-assets.md">Más información</a> |
| Función | Recursos a los que se ha accedido recientemente | La página de inicio de la aplicación Journey Optimizer B2B Edition ahora incluye la sección _[!UICONTROL Se ha accedido recientemente]_, que proporciona una lista de los recursos a los que ha accedido más recientemente el experto en marketing o el administrador. Puede utilizar esta lista para ir directamente al recurso en el que ha trabajado recientemente sin navegar por una serie de páginas de recursos y búsquedas. <p>La lista proporciona información adicional sobre la modificación para que pueda tomar la decisión sobre cuál de los recursos necesita más modificaciones desde la última sesión. Para los recursos de correo electrónico, muestra el recorrido de la cuenta en el que se utiliza el recurso de correo electrónico. <a href="../home-page.md">Más información</a> |
| Mejora | Nodo dividido en recorrido: reordenar rutas | En los nodos de ruta dividida, el filtrado de ruta se evalúa en orden descendente. Cada persona o cuenta avanza por la primera ruta que coincida. Puede reordenar las rutas definidas haciendo clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Más información</a> |
| Mejora | Nodo dividido en recorrido: atributos de condición del historial de actividades adicionales | Cuando se utilizan condiciones para definir el filtrado de ruta de acceso de un nodo dividido por personas, existen dos atributos adicionales: _Correo electrónico abierto_ y _Correo electrónico enviado_. Estas adiciones proporcionan una mayor flexibilidad para filtrar personas en recorridos en función de la actividad de correo electrónico. <a href="../journeys/journey-nodes.md#split-paths">Más información</a> |

+++

+++Notas de la versión de agosto de 2024

**Fecha de implementación**: 29 de agosto de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Públicos coincidentes de cuenta de LinkedIn | Genere públicos de publicidad de LinkedIn mediante públicos coincidentes con la cuenta para completar funciones vacías en sus grupos de compras. Al definir un conjunto de filtros de grupo de compras, puede mantener un público coincidente de LinkedIn para segmentar a los posibles clientes que coincidan con los parámetros del grupo de compras. <p>Esta función aprovecha los destinos de Experience Platform para administrar algunos aspectos de la integración. <a href="../data/linkedin-account-matched-audiences.md">Más información</a> |
| Mejora | Ciclo de vida de estado para fragmentos de contenido visual | Los fragmentos visuales ahora se administran mediante un ciclo vital de estado. El estado del fragmento determina su disponibilidad para utilizarlo en un correo electrónico o plantilla de correo electrónico, y los cambios que puede realizar en él. <p>Este flujo de trabajo mejorado facilita la administración del contenido reutilizado según el calendario promocional y de comunicaciones. <a href="../content/fragments.md#fragment-status-and-lifecycle">Más información</a> |

+++
