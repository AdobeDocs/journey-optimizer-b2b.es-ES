---
title: Funciones de gobernanza
description: Obtenga información acerca de las funciones de gobernanza que están disponibles actualmente en Journey Optimizer B2B Edition.
source-git-commit: 1353defe804947617a4d7489592d380bf372c7df
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# Funciones de gobernanza

Como aplicación integrada de Adobe Experience Platform, Journey Optimizer B2B Edition emplea varios servicios y herramientas que le permiten controlar de forma segura los datos de experiencia recopilados para cumplir con las prácticas comerciales, las obligaciones legales y los procesos de desarrollo. Las secciones siguientes proporcionan un resumen de cada una de estas funciones de gobernanza.

## Privacidad - RGPD

Journey Optimizer B2B Edition utiliza las funciones de control del RGPD de Marketo Engage existentes proporcionadas por Privacy Service y el Servicio de Marketo Privacy Broker.

## Control de acceso basado en roles (RBAC)

Con Journey Optimizer B2B Edition y el acceso a Adobe Admin Console, los administradores pueden otorgar permisos de usuario a un tipo de entidad (ver segmentos, administrar segmentos, administrar recorridos, etc.). Esta capacidad forma parte del marco de permisos unificado (UPF) que permite a todos los clientes de Adobe Experience Platform definir y administrar funciones y permisos para su organización.

## Cifrado de datos

**_Cifrado para datos en reposo_**: todos los datos de cuentas y perfiles de persona transferidos de Adobe Experience Platform a Journey Optimizer B2B Edition están cifrados para mantener la conformidad existente de Experience Platform. Todas las entidades que se originan en Journey Optimizer B2B Edition, como recorridos y grupos de compra, también están cifradas.

**_Cifrado para datos en tránsito_** (a través de una red pública): todas las API y entidades de Journey Optimizer B2B Edition se cifran en tránsito mediante TLS 1.2.

## Inclusión/exclusión de consentimiento

La inclusión/exclusión de consentimiento es una forma de gobernanza en la que un perfil puede excluirse de un canal de comunicación, como correo electrónico o SMS, y un perfil debe excluirse de dicho canal de comunicación.

Con Journey Optimizer B2B Edition, puede crear y administrar casos de uso de suscripción/cancelación de suscripción para sus casos de uso de envío de correo electrónico y SMS. Estas preferencias de consentimiento se almacenan dentro del grupo de campos de consentimiento de perfil de XDM y se sincronizan con y desde Journey Optimizer B2B Edition como parte del marco de trabajo de sincronización de datos. Estas preferencias se utilizan en el momento de la entrega para excluir los perfiles de exclusión de las entregas.

## Aún no está disponible

Las siguientes funciones de gobernanza aún no están disponibles, pero se incluyen en la hoja de ruta del producto:

* Aplicación de etiquetas de uso de datos (DULE) / políticas de uso
* Higiene de datos
* Restablecer zona protegida
* Políticas de consentimiento
* Control de acceso de nivel de campo (FLAC)
* Control de acceso de nivel de objeto (OLAC)
* Cifrado CMK para datos en reposo
* Servicio de auditorías de Platform
