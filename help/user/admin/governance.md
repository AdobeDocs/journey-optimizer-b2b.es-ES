---
title: Funciones de gobernanza y privacidad
description: Obtenga información acerca de las funciones de gobernanza que están disponibles actualmente en Journey Optimizer B2B edition.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 697
ht-degree: 0%

---

# Funciones de gobernanza y privacidad

[!DNL Journey Optimizer B2B Edition] es una aplicación integrada de Adobe Experience Platform. Utiliza varias herramientas y servicios que proporcionan control sobre los datos de experiencia recopilados en cumplimiento con las prácticas comerciales, las obligaciones legales y los procesos de desarrollo. Las secciones siguientes proporcionan un resumen de cada una de estas funciones de gobernanza.

## Privacidad

Existen varias regulaciones que se aplican a [!DNL Journey Optimizer B2B Edition] clientes que tienen datos de sujetos de datos que residen en las regiones o países respectivos antes mencionados (UE, California, Tailandia, Brasil, Nueva Zelanda). Esta información en esta página no es asesoramiento legal y no garantiza el cumplimiento de la ley aplicable.

### GDPR (Reglamento general de protección de datos)

El Reglamento General de Protección de Datos (RGPD) es la ley de privacidad de la Unión Europea (UE) que armoniza y moderniza los [requisitos de protección de datos](https://commission.europa.eu/law/law-topic/data-protection/data-protection-explained_en){target="_blank"} de los países de la UE.

[!DNL Journey Optimizer B2B Edition] utiliza las funciones de control del RGPD de Marketo Engage existentes proporcionadas por Privacy Service y el Servicio de Marketo Privacy Broker.

### CNIL

El 14 de abril de 2026, la Commission nationale de l&#39;informatique et des libertés (CNIL) [publicó una recomendación](https://cnil.fr/sites/default/files/2026-05/recommandation_tracking_pixels_emails.pdf) sobre el uso de píxeles de seguimiento en correos electrónicos. La guía aclara cuándo se requiere el consentimiento y resalta la importancia de las prácticas de consentimiento adecuadas para el seguimiento de píxeles del correo electrónico. Esta política afecta a cualquier entidad que envíe correos electrónicos a suscriptores con sede en Francia.

CNIL proporcionó a las empresas un periodo de tres meses a partir de la fecha de la recomendación para informar a sus destinatarios de correo electrónico de la presencia de los píxeles de seguimiento, su propósito y el derecho de los destinatarios a la exclusión. Durante este periodo de transición, se espera que los usuarios de Marketo Engage notifiquen a sus destinatarios el seguimiento de píxeles y proporcionen una exclusión si es necesario. Se espera que CNIL inicie sus actividades de aplicación después del 14 de julio de 2026.

A medida que la CNIL y otros reguladores aclaren las directrices sobre el seguimiento de píxeles y problemas relacionados, Adobe seguirá supervisando las actualizaciones e informándole de los cambios en las capacidades técnicas.

[!DNL Journey Optimizer B2B Edition] ofrece controles que le ayudan a administrar el seguimiento abierto en el nivel de correo electrónico. Los usuarios son responsables de determinar sus propias obligaciones de cumplimiento según las directrices aplicables de la CNIL y otras leyes. Para obtener información sobre el uso de estas funcionalidades para administrar el seguimiento de aperturas de correo electrónico, consulte [_Administrar el seguimiento de correo electrónico_](../content/email-tracking-manage.md).

## Control de acceso basado en roles (RBAC)

Con Journey Optimizer B2B edition y el acceso a Adobe Admin Console, los administradores pueden otorgar permisos de usuario a un tipo de entidad (ver segmentos, administrar segmentos, administrar recorridos, etc.). Esta capacidad forma parte del marco de permisos unificado (UPF) que permite a todos los clientes de Adobe Experience Platform definir y administrar funciones y permisos para su organización.

## Cifrado de datos

**_Cifrado para datos en reposo_**: todos los datos de cuenta y perfil de persona transferidos desde Adobe Experience Platform a Journey Optimizer B2B edition se cifran para mantener la conformidad existente desde Experience Platform. Todas las entidades que se originan en Journey Optimizer B2B edition, como recorridos y grupos de compra, también están cifradas.

**_Cifrado para datos en tránsito_** (a través de una red pública): todas las entidades y API de Journey Optimizer B2B edition se cifran en tránsito mediante TLS 1.2.

## Inclusión/exclusión de consentimiento

Journey Optimizer B2B edition lee las preferencias de consentimiento por persona almacenadas en perfiles XDM de Adobe Experience Platform y las aplica en el momento de la entrega de los mensajes para canales de correo electrónico, SMS y WhatsApp. Una persona que se excluyó de un canal queda excluida de la entrega antes de que se envíe el contenido desde el canal o el proveedor de mensajería descendente.

El consentimiento se evalúa en el momento de la entrega mediante los campos XDM del grupo de campos de consentimiento del perfil. El comportamiento de consentimiento predeterminado difiere según el canal: el correo electrónico se establece de forma predeterminada como &quot;Opted in&quot; cuando no se establece ninguna preferencia, mientras que SMS y WhatsApp se establecen de forma predeterminada como &quot;opted out&quot;.

Para obtener más información sobre los atributos XDM evaluados para cada canal y sus comportamientos predeterminados, consulte [Preferencias de consentimiento](../content/channels-consent-preferences.md).

## Restablecer zona protegida

El restablecimiento de la zona protegida **no es compatible** actualmente con Adobe Journey Optimizer B2B edition. Restablecer o eliminar una zona protegida asignada a Journey Optimizer B2B edition puede causar una pérdida de datos permanente y requerir el aprovisionamiento de una nueva instancia.

## Aún no está disponible

Las siguientes funciones de gobernanza aún no están disponibles:

* Aplicación de etiquetas de uso de datos (DULE) / políticas de uso
* Higiene de datos
* Políticas de consentimiento
* Control de acceso de nivel de campo (FLAC)
* Control de acceso de nivel de objeto (OLAC)
* Cifrado CMK para datos en reposo
* Servicio de auditorías de Platform
