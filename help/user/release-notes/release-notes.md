---
title: Notas de la versión de Journey Optimizer B2B Edition
description: Obtenga información sobre las últimas funciones y mejoras de Adobe Journey Optimizer B2B Edition.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: dfd426f6d658a9340c531231e7180cbc215b65f9
workflow-type: tm+mt
source-wordcount: '2552'
ht-degree: 87%

---

# Notas de la versión de Journey Optimizer B2B Edition

Adobe Journey Optimizer B2B Edition ofrece continuamente correcciones de errores, nuevas funciones, mejoras en las existentes.

Journey Optimizer B2B Edition está desarrollado de forma nativa sobre [!DNL Adobe Experience Platform] y hereda de él sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/latest){target="_blank"}.

Revise la [descripción del producto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=es){target="_blank"} para obtener información sobre los derechos, las protecciones del rendimiento y las limitaciones.
<!-- hold for 2025.8 release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## Notas de la versión 2025.6

**Fecha de implementación**: miércoles, 15 de julio de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Integración con GenStudio for Performance Marketing | (Disponibilidad limitada) Ahora puede integrar las experiencias de correo electrónico de GenStudio for Performance Marketing con Journey Optimizer B2B Edition para mejorar la eficacia del marketing y mantener la coherencia de la marca. Con esta integración, puede combinar la creación de contenido con tecnología de IA de GenStudio con las funciones de orquestación avanzadas de Journey Optimizer B2B Edition. [Más información](../content/genstudio-email-workflow.md) |
| Función | Informes de detección de spam | Para evitar los filtros de correo no deseado y asegurarse de que los mensajes se envíen a las bandejas de entrada de la audiencia, puede generar un _informe de correo no deseado_ directamente en el espacio de diseño del correo electrónico. [Más información](../content/email-spam-report.md) |
| Función | Página de detalles de persona | Ahora puede hacer clic en el nombre de una persona cuando se muestre (como hipervínculo) en las páginas Panel inteligente, Detalles del grupo de compra y Detalles de la cuenta. Esta acción abre la página de detalles de la persona asociada, que contiene información sobre el contacto, su actividad y los grupos de compra más comprometidos. [Más información](../accounts/person-details.md) |
| Función | Acciones de cuenta y grupo de compra | Realice acciones directamente desde las páginas de detalles de la cuenta y de compra del grupo para lograr una participación oportuna e intencional. <li>Use la acción _Enviar correo electrónico_ para enviar un correo electrónico de Marketo Engage aprobado a los contactos de la cuenta seleccionada o a los miembros del grupo de compra. [Más información](../accounts/account-details.md#send-emails) <li>De los detalles del grupo de compras, las acciones también incluyen _Asignar un nuevo miembro_, _Quitar un miembro_ y _Editar un rol_. [Más información](../buying-groups/buying-group-details.md#members-tab) |
| Función | Acceso en CRM a páginas de detalles | Ahora puede configurar vínculos directos a las páginas de detalles de Journey Optimizer B2B edition para cuentas, contactos y posibles clientes en su herramienta de administración de la relación con los clientes (CRM), como Salesforce o Microsoft Dynamics. [Más información](../accounts/crm-linking.md) |
| Función | Compatibilidad con CSS personalizado para el diseño de contenido | Ahora puede agregar su propio CSS personalizado al crear contenido de correo electrónico y de página de aterrizaje en el espacio de diseño. [Más información](../content/design-custom-css.md) |
| Función | Configuración de asignación de palabra clave por intención | Para activar y gestionar el modelo de detección de intención, ahora puede cargar una hoja de cálculo para definir una categoría de asignación de datos por intención. [Más información](../admin/intent-data.md) |
| Mejora | Simular contenido del resumen del correo electrónico | Ahora puede acceder a las herramientas _Simular contenido_ desde el resumen del correo electrónico (detalles y propiedades) al abrir un mensaje de correo electrónico desde la lista Correos electrónicos. Este acceso se suma al espacio de diseño de correo electrónico. [Más información](../content/email-simulate-content.md#display-the-email-preview) |
| Mejora | Visualización del recuento total para la lista de plantillas de roles | La página de lista _[!UICONTROL Plantillas de roles]_ se ha mejorado con la visualización del recuento total junto a la barra de búsqueda. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## Notas de la versión 2025.5

**Fecha de implementación**: 3 de junio de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Pruebas de correo electrónico con Litmus | Con una cuenta de [Litmus Enterprise](https://www.litmus.com/email-testing){target="_blank"}, ahora puede obtener una vista previa del procesamiento de correo electrónico en clientes de correo electrónico populares desde Journey Optimizer B2B edition. Esta integración le ayuda a garantizar que el contenido del correo electrónico tenga un aspecto impecable y funcione según lo diseñado en cada bandeja de entrada de correo electrónico. [Más información](../content/email-test-rendering.md) |
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
| Mejora | Filtro de páginas web visitadas | Organice los recorridos en función de la actividad de las páginas web visitadas asociadas con las campañas y programas de Marketo Engage. <a href="../journeys/split-merge-paths-nodes.md#people-path-conditions">Más información</a> |
| Mejora | Lista de correos electrónicos | Vea una lista global de correos electrónicos activos y borrador para buscar, revisar y actualizar los correos en los recorridos de cuenta asociados. <a href="../content/emails-list.md">Más información</a> |

## Notas de la versión 2025.3

**Fecha de implementación**: 1 de abril de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Duplicar recorridos de cuenta | Ya está disponible una acción duplicada para recorridos de cuenta. Puede duplicar los detalles del recorrido de cuenta, o sencillamente un simple esqueleto de la estructura del flujo y la ruta. <a href="../journeys/journey-overview.md#duplicate-journey">Más información</a> |
| Función | Mis tokens para los recorridos de la cuenta | Ahora puede definir un conjunto de tokens personalizados con valores que sean específicos del recorrido de la cuenta. Este conjunto de tokens personalizados se denomina _Mis tokens_ y cualquiera de estos tokens personalizados son para la personalización cuando se crean correos electrónicos del recorrido. <a href="../content/personalization-my-tokens.md">Más información</a> |
| Función | Eliminar fases del grupo de compras | Puede eliminar el modelo de fases del grupo de compras cuando esté en estado borrador o publicado. Si se publica (está activo), solo podrá eliminarlo si no está asociado a un interés de solución. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Más información</a> |
| Mejora | Recuentos del nodos del recorrido | Mayor visibilidad de los recuentos de miembros del recorrido publicados en el nivel de nodo. En el _Mapa del recorrido_, los nodos muestran el _[!UICONTROL Total de cuentas introducidas]_. Al seleccionar un nodo de acción, los detalles situados a la derecha también incluyen _[!UICONTROL Cuentas en las que aún no se ha actuado]_. Y los detalles del nodo _Escuchar un evento_ incluyen _[!UICONTROL Cuentas en este paso]_. Utilice esta información para validar la progresión de la cuenta en sus recorridos activos, finalizados y anulados. |

## Notas de la versión 2025.2

**Fecha de implementación**: 11 de marzo de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Campos personalizables: fragmentos de contenido | Durante el diseño de fragmentos visuales, puede designar parámetros para un componente del fragmento como editables. Esta función permite al autor del correo electrónico o la plantilla especificar un valor de campo personalizado específico para sus necesidades. Este indicador de personalización se limita a los componentes visuales de imagen, texto y botones. <a href="../content/fragment-authoring.md#enable-fragment-customization">Más información</a> |
| Función | Tipos de duplicación del recorrido | Cuando duplica el recorrido de una cuenta, puede incluir detalles del nodo, excluyendo los correos electrónicos y mensajes de SMS creados en Journey Optimizer B2B Edition. Como alternativa, puede crear una copia esqueleto de la estructura y los flujos de ruta, sin detalles del nodo ni ajustes. <a href="../journeys/journey-overview.md#duplicate-journey">Más información</a> |
| Mejora | Cuatro plantillas de correo electrónico de muestra adicionales | La biblioteca de plantillas de correo electrónico de ejemplo ahora incluye cuatro plantillas de SecureFinancial como ejemplos para volver a participar, informar, alimentar y dar ejemplos de contenido de comentarios |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Notas de la versión 2025.1 {#Jan-2025}

**Fecha de implementación**: 6 de febrero de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Reenvío de eventos de experiencia | Los administradores pueden configurar definiciones de eventos basadas en Adobe Experience Platform (AEP). Estas configuraciones permiten a los especialistas en marketing crear recorridos de cuenta que reaccionan a los eventos de experiencia de AEP.  <a href="../admin/configure-aep-events.md">Más información</a> |
| Función | Destinos de medios de pago | Capacite a personas conocidas para campañas de medios de pago desde un recorrido de cuentas, de modo que pueda participar en plataformas de publicidad como LinkedIn. Utilice un nodo de rutas divididas en un recorrido de cuenta para segmentar los públicos de las cuentas en función de comportamientos específicos e identificar cuentas que garanticen una participación adicional. A continuación, añada personas de esas cuentas a una audiencia de cliente externa a través de Real-Time CDP a un destino de medios de pago admitido. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Más información</a> |
| Función | Panel de control inteligente | Vea la progresión de la compra de grupos a través de los recorridos de su cuenta, incluidas las perspectivas generadas por IA para un análisis más inteligente y una priorización precisa de la cuenta. <a href="../dashboards/intelligent-dashboard.md">Más información</a> |
| Función | Grupo de compras y detalles de la cuenta | Vea perspectivas en el nivel de grupo de compras y de cuenta para tener más contexto y datos históricos cuando empiece a interactuar con un cliente.<p>Los detalles del grupo de compras incluyen cualquier intención de origen que se detecte. <a href="../buying-groups/buying-group-details.md">Más información</a><p>Las cuentas de detalles de la cuenta resaltan el aumento en la participación detectada por intención, de modo que puede alertar a las ventas sobre cuentas que están listas para una participación personalizada centrada en las ventas.  <a href="../accounts/account-details.md">Más información</a> |
| Función | Información general sobre recorridos | Al acceder a los recorridos de la cuenta, la pestaña Información general ofrece una instantánea completa de los recorridos de la cuenta activa, en la que se detalla el progreso de la cuenta mediante diagramas de círculos y barras que categorizan y cuantifican las finalizaciones y las actividades de participación.  <a href="../dashboards/journeys-dashboard.md">Más información</a> |
| Función | Edición de imágenes en Adobe Express | Las acciones rápidas de Adobe Express le permiten realizar ediciones sencillas (como recortar y cambiar el tamaño) en imágenes para conseguir un aspecto más pulido en el contenido. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Más información</a>  <p>Para obtener un conjunto más completo de herramientas de diseño, esta integración permite obtener una licencia completa de Adobe Express en Journey Optimizer B2B Edition. Con esta configuración, se puede acceder a la interfaz de usuario completa de Adobe Express desde el espacio de trabajo de recursos local. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Más información</a> |
| Función | Filtros de intención para comprar funciones de grupo | Al enviar las palabras clave por intención, el modelo de detección de intención predice una solución o producto de interés con una confianza lo suficientemente alta según la actividad de un posible cliente. <a href="../admin/intent-data.md">Más información</a> <p>Estos datos de intención están disponibles para definir las condiciones de función de grupo de compra <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a> |
| Mejora | Compatibilidad con eventos de Marketo Engage en recorridos | El nodo de recorrido _Escuchar evento_ ahora admite dos eventos de Marketo Engage en el nivel de personas: _Visita la página web_ y _Rellena el formulario_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Más información</a> |
| Mejora | Compra de filtros de grupo de compras para las listas inteligentes de Marketo Engage | Vea y cree listas inteligentes con filtros de grupo de compras en Marketo Engage. Estos filtros añadidos le permiten suprimir e incluir miembros del grupo de compra en campañas y programas de Marketo Engage desde recorridos de cuenta en Journey Optimizer B2B Edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Más información</a> |
| Mejora | Filtro de abono a listas de Marketo Engage para recorridos y funciones | En Journey Optimizer B2B, compruebe el abono a la lista Marketo Engage como condición para un nodo _split path by people_ para eliminar la duplicación en las actividades de recorrido. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Más información</a> <p> Para las plantillas de funciones de grupo de compras, utilice el abono a las listas como condición de función. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a> |
| Mejora | Panel de información general de participación | Este panel se actualiza para proporcionar una vista completa de la participación. Muestra métricas en tiempo real de interacciones de cuenta e individuales a través de gráficos de círculos de instantáneas y gráficos de líneas de tendencia reveladora a lo largo del tiempo. <a href="../dashboards/engagement-dashboard.md">Más información</a> |

## Versiones de 2024

Amplíe las siguientes listas para las funciones y mejoras de Journey Optimizer B2B Edition publicadas en 2024.

+++Notas de la versión de octubre de 2024

**Fecha de implementación**: 29 de octubre de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Contenido condicional en plantillas de correo electrónico | Personalice el contenido del correo electrónico en función del comportamiento del destinatario y las características del perfil, tanto a nivel de cuenta como de posible cliente. <p>A medida que crea un correo electrónico para el recorrido de la cuenta en el espacio de diseño visual de correo electrónico, utilice reglas condicionales para definir varias variantes para cualquier componente de contenido. <a href="../content/conditional-content.md">Más información</a> |
| Función | _Añada a la lista_ y _Quite de la lista_ acciones de personas en recorridos | Personalice el contenido del correo electrónico en función del comportamiento del destinatario y las características del perfil, tanto a nivel de cuenta como de posible cliente. <a href="../journeys/action-nodes.md">Más información</a> |
| Función | Gobernanza de contenido y bloqueo de componentes | Para garantizar el cumplimiento de los diseños de contenido aprobados, utilice las funciones de control de contenido para bloquear los componentes de contenido de plantillas de correo electrónico. Con la gobernanza de contenido activada en la plantilla de correo electrónico, los especialistas en marketing solo pueden modificar los elementos permitidos para mantenerla alineada con la estrategia de contenido. <a href="../content/template-content-governance.md">Más información</a> |
| Función | Fases del grupo de compras | Al definir y publicar un modelo de ensayo de grupos de compra personalizado, puede realizar un seguimiento de la progresión del grupo de compras a través de las fases del ciclo de vida del grupo de compras. Utilice estas fases para identificar las siguientes mejores acciones para miembros del grupo de compras. Puede configurar las reglas de transición y los nodos de recorrido que determinan la progresión de la fase y activan acciones en función de los cambios. <a href="../buying-groups/buying-group-stages.md">Más información</a> |
| Mejora | Nuevas plantillas de correo electrónico listas para usar | La biblioteca de plantillas de ejemplo ahora incluye plantillas de correo electrónico adicionales diseñadas para los especialistas en marketing B2B. Utilice estas plantillas de ejemplo como punto de partida y añada su propia personalización de marca y mensajería. <a href="../content/email-templates.md#select-a-design-template">Más información</a> |
| Mejora | Campos personalizados como atributos de persona | Si tiene campos de persona personalizados definidos en el esquema de audiencia de cuenta en Experience Platform, estos campos también están disponibles para usarlos como atributos de persona en condiciones. Utilice estos atributos personalizados en lo siguiente: <li>Plantillas de funciones <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a></li><li>Dividir rutas por nodos de recorrido de personas <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Más información</a></li> |
| Mejora | Configuración del canal de correo electrónico | La configuración de correo electrónico ahora está visible en la interfaz de Journey Optimizer B2B Edition. Puede revisar rápidamente las configuraciones actuales y los administradores pueden hacer clic en _[!UICONTROL Editar configuración]_ para ir directamente a la configuración en Marketo Engage y actualizarla según los requisitos de su organización. <a href="../admin/configure-channels-emails.md">Más información</a> |

+++

+++Notas de la versión de septiembre de 2024

**Fecha de implementación**: 7 de octubre de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Mejora | Biblioteca de recursos central | La _biblioteca de recursos central_ mejorada le permite usar todos los recursos de imagen de su instancia de Marketo Engage en los espacios de trabajo de Design Studio. Existen protecciones integradas que impiden realizar ediciones en los recursos de Marketo Engage desde Journey Optimizer B2B Edition, así como eliminar y mover operaciones. Estas protecciones garantizan que los recursos de origen (Marketo Engage Design Studio) se mantengan, al tiempo que permiten una lectura y reutilización sin problemas en Journey Optimizer B2B Edition.<p>Para los recursos que se utilizan exclusivamente en Journey Optimizer B2B Edition, un espacio de trabajo específico proporciona funciones completas de administración de recursos. <a href="../content/marketo-engage-design-studio.md">Más información</a> |
| Función | Recursos a los que se ha accedido recientemente | La página de inicio de la aplicación Journey Optimizer B2B Edition ahora incluye la sección _[!UICONTROL Se ha accedido recientemente]_, que proporciona una lista de los recursos a los que ha accedido más recientemente el experto en marketing o el administrador. Puede utilizar esta lista para ir directamente al recurso en el que ha trabajado recientemente sin navegar por una serie de páginas de recursos y búsquedas. <p>La lista proporciona información adicional sobre la modificación para que pueda tomar la decisión sobre cuál de los recursos necesita más modificaciones desde la última sesión. Para los recursos de correo electrónico, muestra el recorrido de la cuenta en el que se utiliza el recurso de correo electrónico. <a href="../home-page.md">Más información</a> |
| Mejora | Nodo dividido en recorrido: reordenar rutas | En los nodos de ruta dividida, el filtrado de ruta se evalúa en orden descendente. Cada persona o cuenta avanza por la primera ruta que coincida. Puede reordenar las rutas definidas haciendo clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Más información</a> |
| Mejora | Nodo dividido en recorrido: atributos de condición del historial de actividades adicionales | Cuando se utilizan condiciones para definir el filtrado de ruta de acceso de un nodo dividido por personas, existen dos atributos adicionales: _Correo electrónico abierto_ y _Correo electrónico enviado_. Estas adiciones proporcionan una mayor flexibilidad para filtrar personas en recorridos en función de la actividad de correo electrónico. <a href="../journeys/journey-nodes.md#split-paths">Más información</a> |

+++

 +++Notas de la versión de agosto de 2024

**Fecha de implementación**: 29 de agosto de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Función | Audiencias coincidentes de cuenta de LinkedIn | Genere audiencias de publicidad de LinkedIn mediante Audiencias coincidentes con la cuenta para completar funciones vacías en sus grupos de compras. Al definir un conjunto de filtros de grupo de compras, puede mantener una audiencia coincidente de LinkedIn para segmentar a los posibles clientes que coincidan con los parámetros del grupo de compras. <p>Esta función aprovecha los destinos de Experience Platform para administrar algunos aspectos de la integración. <a href="../data/linkedin-account-matched-audiences.md">Más información</a> |
| Mejora | Ciclo de vida de estado para fragmentos de contenido visual | Los fragmentos visuales ahora se administran mediante un ciclo vital de estado. El estado del fragmento determina su disponibilidad para utilizarlo en un correo electrónico o plantilla de correo electrónico, y los cambios que puede realizar en él. <p>Este flujo de trabajo mejorado facilita la administración del contenido reutilizado según el calendario promocional y de comunicaciones. <a href="../content/fragments.md#fragment-status-and-lifecycle">Más información</a> |

 +++
