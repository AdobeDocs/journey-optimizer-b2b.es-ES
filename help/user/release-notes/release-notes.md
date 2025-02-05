---
title: Notas de la versión
description: Últimas notas de la versión de Adobe Journey Optimizer edición B2B
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 9438b1472df38eddc3e1fa6cd5bc3992af0c9eec
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 10%

---

# Notas de la versión de Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition ofrece continuamente nuevas funciones, mejoras en las funciones existentes y correcciones de errores.

Journey Optimizer B2B edition se creó de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/latest){target="_blank"}.

Revise la [descripción del producto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} para obtener información sobre los derechos, las protecciones de rendimiento y las limitaciones.

## Notas de la versión de octubre de 2024 {#Oct-2024}

**Fecha de la versión**: 29 de octubre de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Nueva función | Contenido condicional en plantillas de correo electrónico | Personalice el contenido del correo electrónico en función del comportamiento del destinatario y las características del perfil, tanto a nivel de cuenta como de posible cliente. <p>A medida que crea un correo electrónico para el recorrido de la cuenta en el diseñador de correo electrónico, utilice reglas condicionales para definir varias variantes para cualquier componente de contenido. <a href="../content/conditional-content.md">Más información</a> |
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
| Mejora | Biblioteca de recursos central | La _biblioteca de recursos central_ mejorada le permite utilizar todos los recursos de imagen de su instancia de Marketo Engage en los espacios de trabajo de Design Studio. Existen protecciones integradas que impiden realizar ediciones en los recursos del Marketo Engage desde Journey Optimizer B2B edition, así como eliminar y mover operaciones. Estas protecciones garantizan que los recursos de origen (Marketo Engage Design Studio) se mantengan, al tiempo que permiten una lectura y reutilización sin problemas en Journey Optimizer B2B edition.<p>Para los recursos que se utilizan exclusivamente en Journey Optimizer B2B edition, un espacio de trabajo específico proporciona funciones completas de administración de recursos. <a href="../content/marketo-engage-design-studio.md">Más información</a> |
| Nueva función | Recursos a los que se ha accedido recientemente | La página de inicio de la aplicación Journey Optimizer B2B edition ahora incluye la sección _[!UICONTROL A la que se ha accedido recientemente]_, que proporciona una lista de los recursos a los que ha accedido más recientemente el experto en marketing o el administrador. Puede utilizar esta lista para ir directamente al recurso en el que ha trabajado recientemente sin navegar por una serie de páginas de recursos y búsquedas. <p>La lista proporciona información adicional sobre la modificación para que pueda tomar la decisión sobre cuál de los recursos necesita más modificaciones desde la última sesión. Para los recursos de correo electrónico, muestra el recorrido de la cuenta en el que se utiliza el recurso de correo electrónico. <a href="../home-page.md">Más información</a> |
| Mejora | nodo dividido en recorrido: reordenar rutas | En los nodos de ruta dividida, el filtrado de ruta se evalúa en orden descendente. Cada persona o cuenta procede por la primera ruta que coincida. Puede reordenar las rutas definidas haciendo clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Más información</a> |
| Mejora | Nodo dividido en recorrido: atributos de condición del historial de actividades adicionales | Cuando se utilizan condiciones para definir el filtrado de ruta de acceso de un nodo dividido por personas, existen dos atributos adicionales: _Correo electrónico abierto_ y _Correo electrónico enviado_. Estas adiciones proporcionan una mayor flexibilidad para filtrar personas en recorridos en función de la actividad de correo electrónico. <a href="../journeys/journey-nodes.md#split-paths">Más información</a> |

## Notas de la versión de agosto de 2024 {#Aug-2024}

**Fecha de lanzamiento**: 29 de agosto de 2024

Esta versión incorpora las siguientes nuevas funciones y mejoras:

| Tipo | Elemento | Descripción |
| ---- | ---- | ----------- |
| Nueva función | Audiencias coincidentes con cuentas de linkedIn | Genere audiencias de LinkedIn Ad mediante Audiencias coincidentes con la cuenta para que pueda desempeñar funciones vacías en sus grupos de compra. Al definir un conjunto de filtros de grupo de compra, puede mantener una audiencia coincidente con LinkedIn para segmentar a los posibles clientes que coincidan con los parámetros del grupo de compra. <p>Esta función aprovecha Destinos de Experience Platform para administrar algunos aspectos de la integración. <a href="../data/linkedin-account-matched-audiences.md">Más información</a> |
| Mejora | Ciclo de vida de estado para fragmentos de contenido visual | Los fragmentos visuales ahora se administran mediante un ciclo vital de estado. El estado del fragmento determina su disponibilidad para utilizarlo en un correo electrónico o plantilla de correo electrónico, y los cambios que puede realizar en él. <p>Este flujo de trabajo mejorado facilita la administración del contenido reutilizado según el calendario promocional y de comunicaciones. <a href="../content/fragments.md#fragment-status-and-lifecycle">Más información</a> |
