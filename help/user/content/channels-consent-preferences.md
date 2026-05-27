---
title: Consentimiento de mensajería de canal
description: Descubra cómo Journey Optimizer B2B edition lee las preferencias de consentimiento de perfil XDM de AEP y aplica la inclusión y la exclusión en el momento de la entrega de los mensajes para los canales de correo electrónico, SMS y WhatsApp.
feature: Setup, Channels
role: Admin, User
autotag-review: '2026-05-19T16:18:37.228Z'
TQID: 'https://experienceleague.adobe.com/-c0dJnpfiIcj0B5gViyEQ7E1Ws0BwP864OLF003rOjw'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: a22f05f6-0fcf-40c0-a70e-e13a3db185f7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 8226114f1a34adf85437579ef17a50b80ccfa596
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 1%

---

# Consentimiento de mensajería de canal

Adobe Journey Optimizer B2B edition lee las preferencias de consentimiento por persona almacenadas en perfiles XDM de Adobe Experience Platform y las aplica en el momento de la entrega de los mensajes, como parte de los [controles de gobernanza](../admin/governance.md) de la aplicación. Las personas que optaron por no participar en un canal quedan excluidas de la entrega antes de que se envíe el contenido desde el canal o el proveedor de mensajería descendente.

Las secciones siguientes describen cómo Journey Optimizer B2B edition evalúa el consentimiento en el momento de enviar el mensaje para cada canal admitido.

## Correo electrónico {#email}

Journey Optimizer B2B edition evalúa el siguiente atributo XDM para el consentimiento de correo electrónico al enviar mensajes en el [canal de correo electrónico](../admin/configure-channels-emails.md):

| Atributo XDM | `y` | `n` | Sin valor |
| --- | --- | --- | --- |
| `consents.marketing.email.val` | Incluido | Excluido | Incluido |

Tenga en cuenta las siguientes consideraciones para el consentimiento por correo electrónico:

* Las personas que se hayan excluido globalmente del correo electrónico pueden recibir correos electrónicos marcados como operativos.
* No se admiten las preferencias de nivel de suscripción.

Para revisar la actividad de cancelación de suscripción del correo electrónico enviado, consulte el [informe de rendimiento del correo electrónico](../dashboards/email-performance-dashboard.md).

## SMS {#sms}

Journey Optimizer B2B edition evalúa los siguientes atributos XDM para el consentimiento de SMS al enviar mensajes a través del [canal SMS](../admin/configure-channels-sms.md):

| Atributo XDM | `y` | `n` | Sin valor |
| --- | --- | --- | --- |
| `consents.marketing.sms.val` | Incluido | Excluido | Excluido |
| `consents.marketing.subscriptions.<senderID>` | Incluido | Excluido | Excluido |
| `consents.marketing.sms.subscriptions.<senderId>.subscribers.<phoneNumber>` | Incluido | Excluido | Excluido |

Tenga en cuenta las siguientes consideraciones para el consentimiento SMS:

* Cuando se excluye un registro de posible cliente (persona) de SMS, el registro se excluye por completo y no se pasa a proveedores de SMS descendentes.
* Cuando está disponible, se evalúa el consentimiento en el nivel de suscripción. La exclusión global se utiliza como alternativa cuando el consentimiento a nivel de suscripción no está disponible.
* Las personas excluidas de los SMS pueden seguir recibiendo mensajes marcados como operativos.
* Si varios registros de posibles clientes comparten el mismo número de teléfono, comparten el mismo estado de inclusión o exclusión.

## WhatsApp {#whatsapp}

Journey Optimizer B2B edition evalúa los siguientes atributos XDM para el consentimiento de WhatsApp al enviar mensajes a través de un [canal de WhatsApp](../admin/configure-channels-whatsapp.md) configurado:

| Atributo XDM | `y` | `n` | Sin valor |
| --- | --- | --- | --- |
| `consents.marketing.whatsApp.val` | Incluido | Excluido | Excluido |
| `consents.idSpecific.Phone.<number>.marketing.whatsApp.val` | Incluido | Excluido | Excluido |

Tenga en cuenta las siguientes consideraciones para el consentimiento de WhatsApp:

* Si el valor de atributo global de WhatsApp (`consents.marketing.whatsApp.val`) está presente, se utiliza para la evaluación del consentimiento.
* Si el valor de atributo global no está presente pero hay una entrada específica del remitente, la entrada específica del remitente se utiliza para evaluar el consentimiento.
* Si no hay ningún valor presente para ninguno de los atributos, la persona se trata como excluida.

## No compatible {#not-supported}

Actualmente, Journey Optimizer B2B edition no admite las siguientes funciones relacionadas con el consentimiento:

* Políticas de consentimiento de AEP
* Atributos preferidos de marketing (`consents.marketing.preferred`)
