---
title: Notas de la versión
description: Últimas notas de la versión de Adobe Journey Optimizer edición B2B
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 228837741f3373ee2b8423515b7412564281f8ea
workflow-type: tm+mt
source-wordcount: '1818'
ht-degree: 9%

---

# Notas de la versión de Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition ofrece continuamente nuevas funciones, mejoras en las funciones existentes y correcciones de errores.

Journey Optimizer B2B edition se creó de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/latest){target="_blank"}.

Revise la [descripción del producto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} para obtener información sobre los derechos, las protecciones de rendimiento y las limitaciones.

## Notas de la versión 2025.3

**Fecha de la versión**: miércoles, 01 de abril de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Nueva función | Listas de cuentas | Ahora puede crear una lista de cuentas estáticas o dinámicas para segmentar cuentas con nombre según los criterios definidos, como el sector, la ubicación o el tamaño de la compañía. <a href="../accounts/account-lists.md">Más información</a> |
| Nueva función | Mis tokens para recorridos de cuenta | Ahora puede definir un conjunto de tokens personalizados con valores específicos del recorrido de la cuenta. Este conjunto de tokens personalizados se denomina _Mis tokens_ y cualquiera de ellos es para personalizar al crear correos electrónicos de recorrido. <a href="../content/personalization-my-tokens.md">Más información</a> |
| Nueva función | Eliminar etapas de grupo de compra | Puede eliminar el modelo de fases de grupo de compra cuando esté en estado de borrador o publicado. Si se publica (activo), solo puede eliminarse cuando no esté asociado a un interés de solución. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Más información</a> |
| Mejora | Recuentos de nodos de recorrido | Se ha mejorado la visibilidad de los recuentos de miembros del recorrido en el nivel de nodo. Utilice esta información para validar la progresión de la cuenta en un recorrido. |

## Notas de la versión 2025.2

**Fecha de la versión**: 11 de marzo de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Nueva función | Campos personalizables: fragmentos de contenido | Como diseñador de fragmentos de contenido, puede designar un parámetro para un componente del fragmento como editable. Esto permite al autor del correo electrónico o la plantilla especificar un valor de campo personalizado específico para sus necesidades. Este indicador de personalización se limita a los componentes visuales de imagen, texto y botones. <a href="../content/fragment-authoring.md#enable-custom-fields">Más información</a> |
| Nueva función | Funciones integradas y permisos del producto B2B | Experience Platform ahora incluye un conjunto de funciones integradas (predeterminadas) que puede utilizar para administrar el acceso a las funciones de los productos B2B. <a href="../admin/user-management.md#b2b-built-in-roles">Más información</a> <br/>Los administradores ahora pueden definir funciones personalizadas en Adobe Experience Platform para incluir permisos de productos de Journey Optimizer B2B edition.  <a href="../admin/user-management.md#b2b-product-permissions">Más información</a> |
| Nueva función | Tipos de duplicación de recorrido | Al duplicar un recorrido de cuenta, puede incluir detalles del nodo, excluyendo los correos electrónicos y mensajes SMS creados en Journey Optimizer B2B edition. Como alternativa, puede crear una copia esquemática de la estructura y los flujos de ruta, sin detalles ni configuración de nodo. <a href="../journeys/journey-overview.md#duplicate-journey">Más información</a> |
| Mejora | Cuatro plantillas de correo electrónico de muestra adicionales | La biblioteca de plantillas de correo electrónico de ejemplo ahora incluye cuatro plantillas de SecureFinancial como ejemplos para volver a participar, informar, alimentar y dar ejemplos de contenido de comentarios |

## Notas de la versión 2025.1 {#Jan-2025}

**Fecha de lanzamiento**: 6 de febrero de 2025

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Nueva función | Reenvío de eventos de experiencia | Los administradores pueden configurar definiciones de eventos basadas en Adobe Experience Platform (AEP). Estas configuraciones permiten a los especialistas en marketing crear recorridos de cuenta que reaccionan a los eventos de experiencia de AEP.  <a href="../admin/configure-aep-events.md">Más información</a> |
| Nueva función | Destinos de medios de pago | Capacite a personas conocidas para campañas de medios de pago desde un recorrido de cuentas, de modo que pueda participar en plataformas de publicidad como LinkedIn. Utilice un nodo de rutas divididas en un recorrido de cuentas para segmentar las audiencias de cuentas en función de comportamientos específicos e identificar cuentas que garanticen una participación adicional. A continuación, añada personas de esas cuentas a una audiencia de cliente externa a través de Real-Time CDP a un destino de medios de pago admitido. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Más información</a> |
| Nueva función | Panel de control inteligente | Vea la progresión de la compra de grupos a través de los recorridos de su cuenta, incluidas las perspectivas generadas por IA para un análisis más inteligente y una priorización precisa de la cuenta. <a href="../dashboards/intelligent-dashboard.md">Más información</a> |
| Nueva función | Grupo de compra y detalles de la cuenta | Vea perspectivas en el nivel de grupo de compra y de cuenta para tener más contexto y datos históricos cuando empiece a interactuar con un cliente.<p>Los detalles del grupo de compra incluyen cualquier intención de origen que se detecte. <a href="../buying-groups/buying-group-details.md">Más información</a><p>Las cuentas de detalles de la cuenta resaltan el aumento en la participación detectada por intención, de modo que puede alertar a las ventas sobre cuentas que están listas para una participación personalizada centrada en las ventas.  <a href="../accounts/account-details.md">Más información</a> |
| Nueva función | Información general sobre Recorrido | Al acceder a los recorridos de la cuenta, la pestaña Información general ofrece una instantánea completa de los recorridos de la cuenta activa, en la que se detalla el progreso de la cuenta mediante diagramas de círculos y barras que categorizan y cuantifican las finalizaciones y las actividades de participación.  <a href="../dashboards/journeys-dashboard.md">Más información</a> |
| Nueva función | Edición de imágenes en Adobe Express | Las acciones rápidas de Adobe Express le permiten realizar ediciones sencillas (como recortar y cambiar el tamaño) en imágenes para conseguir un aspecto más pulido en el contenido. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Más información</a>  <p>Para obtener un conjunto más completo de herramientas de diseño, esta integración permite obtener una licencia completa de Adobe Express en Journey Optimizer B2B edition. Con esta configuración, se puede acceder a la interfaz de usuario completa de Adobe Express desde el espacio de trabajo de recursos local. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Más información</a> |
| Nueva función | Filtros de intención para comprar funciones de grupo | Al enviar las palabras clave por intención, el modelo de detección de intención predice una solución o producto de interés con una confianza lo suficientemente alta según la actividad de un posible cliente. <a href="../admin/intent-data.md">Más información</a> <p>Estos datos de intención están disponibles para definir las condiciones de función de grupo de compra <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a> |
| Mejora | Compatibilidad con eventos de Marketo Engage en recorrido | El nodo de recorrido _Escuchar evento_ ahora admite dos eventos de Marketo Engage en el nivel de personas: _Visita la página web_ y _Rellena el formulario_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Más información</a> |
| Mejora | Compra de filtros de grupo para las listas inteligentes de Marketo Engage | Vea y cree listas inteligentes con filtros de grupo de compra en Marketo Engage. Estos filtros añadidos le permiten suprimir e incluir miembros del grupo de compra en campañas y programas de Marketo Engage desde recorridos de cuenta en Journey Optimizer B2B edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Más información</a> |
| Mejora | Filtro de pertenencia a listas de Marketo Engage para recorridos y funciones | En Journey Optimizer B2B, compruebe la pertenencia a la lista Marketo Engage como condición para un nodo _split path by people_ para ayudar a eliminar la duplicación en las actividades de recorrido. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Más información</a> <p> Para comprar plantillas de roles de grupo, utilice la pertenencia a listas como condición de rol. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a> |
| Mejora | Panel de información general de participación | Este tablero se actualiza para proporcionar una vista completa de la participación. Muestra métricas en tiempo real de interacciones de cuenta e individuales a través de gráficos de círculos de instantáneas y gráficos de líneas de tendencia reveladora a lo largo del tiempo. <a href="../dashboards/engagement-dashboard.md">Más información</a> |


## Notas de la versión de octubre de 2024 {#Oct-2024}

**Fecha de la versión**: 29 de octubre de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Nueva función | Contenido condicional en plantillas de correo electrónico | Personalice el contenido del correo electrónico en función del comportamiento del destinatario y las características del perfil, tanto a nivel de cuenta como de posible cliente. <p>A medida que crea un correo electrónico para el recorrido de la cuenta en el espacio de diseño visual de correo electrónico, utilice reglas condicionales para definir varias variantes para cualquier componente de contenido. <a href="../content/conditional-content.md">Más información</a> |
| Nueva función | _Agregar a lista_ y _Quitar de la lista_ acciones de personas en recorridos | Personalice el contenido del correo electrónico en función del comportamiento del destinatario y las características del perfil, tanto a nivel de cuenta como de posible cliente. <a href="../journeys/action-nodes.md">Más información</a> |
| Nueva función | Gobernanza de contenido y bloqueo de componentes | Para garantizar el cumplimiento de los diseños de contenido aprobados, utilice las funciones de control de contenido para bloquear los componentes de contenido de plantillas de correo electrónico. Con la gobernanza de contenido activada en la plantilla de correo electrónico, los especialistas en marketing solo pueden modificar los elementos permitidos para mantenerla alineada con la estrategia de contenido. <a href="../content/template-content-governance.md">Más información</a> |
| Nueva función | Fases del grupo de compras | Al definir y publicar un modelo de ensayo de grupos de compra personalizado, puede realizar un seguimiento de la progresión del grupo de compra a través de las fases del ciclo de vida del grupo de compra. Utilice estas fases para identificar las siguientes mejores acciones para comprar miembros del grupo. Puede configurar las reglas de transición y los nodos de recorrido que determinan la progresión de la fase y las acciones de déclencheur en función de los cambios. <a href="../buying-groups/buying-group-stages.md">Más información</a> |
| Mejora | Nuevas plantillas de correo electrónico listas para usar | La biblioteca de plantillas de ejemplo ahora incluye plantillas de correo electrónico adicionales diseñadas para los especialistas en marketing B2B. Utilice estas plantillas de ejemplo como punto de partida y añada su propia marca y mensajería. <a href="../content/email-templates.md#select-a-design-template">Más información</a> |
| Mejora | Campos personalizados como atributos de persona | Si tiene campos de persona personalizados definidos en el esquema de audiencia de cuenta en Experience Platform, estos campos también están disponibles para usarlos como atributos de persona en condiciones. Utilice estos atributos personalizados en: <li>Plantillas de roles <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Más información</a></li><li>Dividir rutas por nodos de recorrido de personas <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Más información</a></li> |
| Mejora | Configuración de canal de correo electrónico | La configuración de correo electrónico ahora está visible en la interfaz de B2B edition de Journey Optimizer. Puede revisar rápidamente las configuraciones actuales y los administradores pueden hacer clic en _[!UICONTROL Editar configuración]_ para ir directamente a la configuración en Marketo Engage y actualizarla según los requisitos de su organización. <a href="../admin/configure-channels-emails.md">Más información</a> |

## Notas de la versión de septiembre de 2024 {#Sept-2024}

**Fecha de la versión**: 7 de octubre de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Mejora | Biblioteca de recursos central | La _biblioteca de recursos central_ mejorada le permite usar todos los recursos de imagen de su instancia de Marketo Engage en los espacios de trabajo de Design Studio. Existen protecciones integradas que impiden realizar ediciones en los recursos de Marketo Engage desde Journey Optimizer B2B edition, así como eliminar y mover operaciones. Estas protecciones garantizan que los recursos de origen (Marketo Engage Design Studio) se mantengan, al tiempo que permiten una lectura y reutilización sin problemas en Journey Optimizer B2B edition.<p>Para los recursos que se utilizan exclusivamente en Journey Optimizer B2B edition, un espacio de trabajo específico proporciona funciones completas de administración de recursos. <a href="../content/marketo-engage-design-studio.md">Más información</a> |
| Nueva función | Recursos a los que se ha accedido recientemente | La página de inicio de la aplicación Journey Optimizer B2B edition ahora incluye la sección _[!UICONTROL A la que se ha accedido recientemente]_, que proporciona una lista de los recursos a los que ha accedido más recientemente el experto en marketing o el administrador. Puede utilizar esta lista para ir directamente al recurso en el que ha trabajado recientemente sin navegar por una serie de páginas de recursos y búsquedas. <p>La lista proporciona información adicional sobre la modificación para que pueda tomar la decisión sobre cuál de los recursos necesita más modificaciones desde la última sesión. Para los recursos de correo electrónico, muestra el recorrido de la cuenta en el que se utiliza el recurso de correo electrónico. <a href="../home-page.md">Más información</a> |
| Mejora | nodo dividido en recorrido: reordenar rutas | En los nodos de ruta dividida, el filtrado de ruta se evalúa en orden descendente. Cada persona o cuenta procede por la primera ruta que coincida. Puede reordenar las rutas definidas haciendo clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Más información</a> |
| Mejora | Nodo dividido en recorrido: atributos de condición del historial de actividades adicionales | Cuando se utilizan condiciones para definir el filtrado de ruta de acceso de un nodo dividido por personas, existen dos atributos adicionales: _Correo electrónico abierto_ y _Correo electrónico enviado_. Estas adiciones proporcionan una mayor flexibilidad para filtrar personas en recorridos en función de la actividad de correo electrónico. <a href="../journeys/journey-nodes.md#split-paths">Más información</a> |

## Notas de la versión de agosto de 2024 {#Aug-2024}

**Fecha de lanzamiento**: 29 de agosto de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Nueva función | Audiencias coincidentes con cuentas de LinkedIn | Genere audiencias de publicidad de LinkedIn mediante Audiencias coincidentes con la cuenta para ayudarle a completar funciones vacías en sus grupos de compra. Al definir un conjunto de filtros de grupo de compra, puede mantener una audiencia coincidente de LinkedIn para segmentar a los posibles clientes que coincidan con los parámetros del grupo de compra. <p>Esta función aprovecha los destinos de Experience Platform para administrar algunos aspectos de la integración. <a href="../data/linkedin-account-matched-audiences.md">Más información</a> |
| Mejora | Ciclo de vida de estado para fragmentos de contenido visual | Los fragmentos visuales ahora se administran mediante un ciclo vital de estado. El estado del fragmento determina su disponibilidad para utilizarlo en un correo electrónico o plantilla de correo electrónico, y los cambios que puede realizar en él. <p>Este flujo de trabajo mejorado facilita la administración del contenido reutilizado según el calendario promocional y de comunicaciones. <a href="../content/fragments.md#fragment-status-and-lifecycle">Más información</a> |
