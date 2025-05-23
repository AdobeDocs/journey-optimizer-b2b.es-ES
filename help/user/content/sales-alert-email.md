---
title: Correo electrónico de alerta de ventas
description: Aprenda a incluir un correo electrónico de alerta de ventas automatizado en los recorridos de la cuenta.
feature: Email Authoring, Account Journeys
role: User
exl-id: 01bffbce-6c73-483a-8731-de4e5569cf61
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 6%

---

# Correo electrónico de alerta de ventas

Un _correo electrónico de alerta de ventas_ indica la transferencia de grupos de compra a Ventas. El correo electrónico contiene un resumen del grupo de compra e información sobre los miembros del grupo de compra y sus actividades.

Como experto en marketing, puede configurar un nodo de correo electrónico de alerta de ventas en los recorridos de su cuenta para avisar al equipo de ventas sobre la finalización del recorrido para grupos de compra específicos. En el nodo, puede especificar las direcciones de correo electrónico del equipo de ventas o un alias de distribución que llegue a un conjunto de cuentas.

>[!IMPORTANT]
>
>Asegúrese de que la lista de permitidos de su organización se actualiza para que se pueda enviar un correo electrónico de alerta de ventas. Para obtener más información, consulte [Protocolos de seguimiento y envío de correo electrónico](../start/email-protocols.md).

## Contenido de correo electrónico

+++Ejemplo de correo electrónico de alerta de ventas
![Ejemplo de un correo electrónico de alerta de ventas con la plantilla predeterminada](./assets/sales-alert-email-example.png){width="500" zoomable="yes"}

+++

| Sección | Nombre | Descripción |
| - | ---- | ----------- |
| Información del grupo de compra | Nombre del grupo de compra | Nombre para mostrar del grupo de compra. |
|   | Nombre de la cuenta | Nombre de la cuenta. |
|   | Puntuación de participación | Puntuación de participación del grupo comprador, basada en las actividades de participación activas de los últimos 30 días. |
|   | Puntuación de integridad | Puntuación de integridad del grupo comprador. |
|   | Interés de la solución | Interés en la solución vinculado al grupo comprador |
|   | Estado | Estado del grupo comprador. |
| Características destacadas del grupo de compras | Miembros con mayor participación | Principales miembros comprometidos del grupo de compra mediante la puntuación de participación de miembro del grupo de compra y la función. |
|   | Tema de interés | Las palabras clave más frecuentes que se producen en la participación de contenido, en función de los correos electrónicos, las descargas, el chat, la revisión de PDF, el resumen de la actividad y las preguntas del seminario web. |
|   | Faltan roles | Funciones obligatorias en la plantilla, pero faltan en el grupo comprador. |
| Resumen del grupo de compra | Resumen de actividad (con tecnología de IA generativa) | Resumen generado por IA del grupo comprador basado en las actividades de los miembros. Se consideran las actividades de los últimos 30 días. |
|   | Momentos clave interesantes | Momentos interesantes recientes relacionados con los miembros del grupo de compra. |
| Miembros | Lista de cuatro miembros compradores | Detalles de los cuatro miembros principales del grupo de compra por puntuación de participación y función. |
| Cada miembro del grupo comprador | Nombre de miembro | Nombre del miembro del grupo comprador. |
|   | Título | Título del miembro del grupo comprador. |
|   | Función | La función de grupo de compra del miembro. |
|   | Puntuación de participación | Puntuación de participación de miembro del grupo comprador. La puntuación se basa en las actividades de participación activas en los últimos 30 días. |
|   | Último momento interesante | El último momento más interesante relacionado con el miembro. |
|   | Actividades más recientes | Las dos últimas actividades relacionadas con el miembro del grupo comprador. |
|   | Identificación de email | ID de correo electrónico del miembro del grupo comprador. |
|   | Número de teléfono | Número de teléfono del miembro del grupo comprador. |

## Agregar una acción de correo electrónico de alerta de ventas en un recorrido de cuenta

Puede configurar envíos de correo electrónico de alertas de ventas en un recorrido de cuenta cuando agregue un nodo _[!UICONTROL Realizar una acción]_ y haga lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Cuenta]**.

1. Para _[!UICONTROL Acción en cuentas]_, elige **[!UICONTROL Enviar alerta de ventas]**.

1. Para **[!UICONTROL Seleccionar interés de solución]**, elija el interés de solución que se usará para el contenido de correo electrónico generado.

1. Para **[!UICONTROL Enviar correo electrónico a]**, escriba cada dirección de correo electrónico o alias que desee incluir en la entrega.

   ![Crear nuevo cuadro de diálogo de correo electrónico](assets/sales-alert-email-journey-node.png){width="600" zoomable="yes"}

   Una vez publicado el recorrido de la cuenta, la alerta de ventas se envía según estos parámetros.
