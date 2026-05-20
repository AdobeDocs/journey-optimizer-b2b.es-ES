---
title: Funciones de gobernanza
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
source-git-commit: d7e971b6d533a173632224baa359f7559b865497
workflow-type: tm+mt
source-wordcount: 419
ht-degree: 0%

---

# Funciones de gobernanza

Journey Optimizer B2B edition es una aplicación integrada de Adobe Experience Platform. Utiliza varias herramientas y servicios que proporcionan control sobre los datos de experiencia recopilados en cumplimiento con las prácticas comerciales, las obligaciones legales y los procesos de desarrollo. Las secciones siguientes proporcionan un resumen de cada una de estas funciones de gobernanza.

## Privacidad - RGPD

Journey Optimizer B2B edition utiliza las funciones de control del RGPD de Marketo Engage existentes proporcionadas por Privacy Service y el Servicio de agente de privacidad de Marketo.

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
