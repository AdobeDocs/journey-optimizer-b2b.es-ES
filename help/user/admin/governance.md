---
title: Funciones de gobernanza
description: Obtenga información acerca de las funciones de gobernanza que están disponibles actualmente en Journey Optimizer B2B edition.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Funciones de gobernanza

Journey Optimizer B2B edition es una aplicación integrada de Adobe Experience Platform. Utiliza varias herramientas y servicios que proporcionan control sobre los datos de experiencia recopilados en cumplimiento con las prácticas comerciales, las obligaciones legales y los procesos de desarrollo. Las secciones siguientes proporcionan un resumen de cada una de estas funciones de gobernanza.

## Privacidad - RGPD

Journey Optimizer B2B edition utiliza las funciones de control del RGPD de Marketo Engage existentes que proporcionan Privacy Service y el servicio de agente de privacidad de Marketo.

## Control de acceso basado en roles (RBAC)

Con Journey Optimizer B2B edition y el acceso a Adobe Admin Console, los administradores pueden otorgar permisos de usuario a un tipo de entidad (ver segmentos, administrar segmentos, administrar recorridos, etc.). Esta capacidad forma parte del marco de permisos unificado (UPF) que permite a todos los clientes de Adobe Experience Platform definir y administrar funciones y permisos para su organización.

## Cifrado de datos

**_Cifrado para datos en reposo_**: todos los datos de cuentas y perfiles de persona transferidos desde Adobe Experience Platform a Journey Optimizer B2B edition están cifrados para mantener la conformidad existente desde Experience Platform. Todas las entidades que se originan en Journey Optimizer B2B edition, como recorridos y grupos de compra, también están cifradas.

**_Cifrado para datos en tránsito_** (a través de una red pública): todas las entidades y API de Journey Optimizer B2B edition se cifran en tránsito mediante TLS 1.2.

## Inclusión/exclusión de consentimiento

La inclusión/exclusión de consentimiento es una forma de gobernanza en la que un perfil puede excluirse de un canal de comunicación, como correo electrónico o SMS, y un perfil se excluye del canal de comunicación.

Con Journey Optimizer B2B edition, puede crear y administrar casos de uso de suscripción/cancelación de suscripción para sus casos de uso de envío de correo electrónico y SMS. Estas preferencias de consentimiento se almacenan dentro del grupo de campos de consentimiento de perfil de XDM y se sincronizan con y desde Journey Optimizer B2B edition como parte del marco de trabajo de sincronización de datos. Estas preferencias se utilizan en el momento de la entrega para excluir los perfiles de exclusión de las entregas.

## Restablecer zona protegida

El restablecimiento de la zona protegida **no es compatible** actualmente con Adobe Journey Optimizer B2B edition. Restablecer o eliminar una zona protegida asignada a Journey Optimizer B2B edition puede provocar la pérdida permanente de datos en Journey Optimizer B2B edition y requerir la provisión de una nueva instancia de Journey Optimizer B2B edition.

## Aún no está disponible

Las siguientes funciones de gobernanza aún no están disponibles:

* Aplicación de etiquetas de uso de datos (DULE) / políticas de uso
* Higiene de datos
* Políticas de consentimiento
* Control de acceso de nivel de campo (FLAC)
* Control de acceso de nivel de objeto (OLAC)
* Cifrado CMK para datos en reposo
* Servicio de auditorías de Platform
