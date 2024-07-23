---
title: Asignación de campo XDM
description: Revise la asignación de campos entre el esquema XDM de AEP, Marketo Engage y Journey Optimizer B2B Edition.
source-git-commit: af287825508b2372f51aa8ea629cc6eda0a50b35
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 20%

---

# Asignación de campo XDM

El servicio de transferencia de datos (DTS) de es responsable de sincronizar datos de Adobe Experience Platform a Journey Optimizer B2B Edition. DTS se basa en asignaciones entre campos de esquema XDM de Experience Platform y sus equivalentes en Marketo Engage.

## Asignaciones de campo predeterminadas de persona de negocios XDM

| Persona empresaria de XDM | Nombre para mostrar de persona Marketo Engage | Nombre para mostrar de persona de AJO B2B | Tipo de XDM | Tipo de Marketo | Descripción de XDM |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Dirección | ? | cadena | texto | Información principal de la dirección postal, número de piso, número de calle y nombre de la calle. |
| `workAddress.city ` | Ciudad | Ciudad | cadena | cadena | El nombre de la ciudad. |
| `b2b.companyName` | Nombre de la empresa | ? | cadena | cadena | Nombre de la compañía con la que está asociado un profesional. |
| `workAddress.country` | País | País | cadena | cadena | El nombre del territorio administrado por el gobierno. Aparte de `xdm:countryCode`, este es un campo de forma libre que puede tener el nombre del país en cualquier idioma. |
| `person.birthDate` | Fecha de nacimiento | Fecha de nacimiento | cadena | fecha | La fecha completa en la que nació una persona.  DD/MM/YYYY |
| `workEmail.address` | Correo electrónico | Correo electrónico | cadena | correo electrónico | La dirección técnica, por ejemplo, &#39;<name@domain.com>&#39; como se define comúnmente en RFC2822 y estándares subsiguientes. |
| `workEmail.status` | Email suspendido | Email suspendido | cadena | booleano | Una indicación de la capacidad de uso de la dirección de correo electrónico. |
| `faxPhone.number` | Número de fax | ? | cadena | teléfono | Número de teléfono fax. |
| `person.name.firstName` | Nombre | Nombre | cadena | cadena | El primer segmento del nombre en el orden de escritura más comúnmente aceptado en el idioma del nombre. En muchas culturas, este es el nombre de pila preferido. Las propiedades firstName y lastName se han introducido para mantener la compatibilidad con los sistemas existentes que modelan los nombres de una manera simplificada, no semántica y no internacionalizable. Siempre es preferible utilizar xdm:fullName. |
| `extendedWorkDetails.jobTitle` | Cargo | Cargo | cadena | cadena | Cargo de la persona. |
| `person.name.lastName` | Apellido | Apellido | cadena | cadena | El último segmento del nombre en el orden de escritura más comúnmente aceptado en el idioma del nombre. En muchas culturas este es el nombre de familia heredado, apellido, patronímico o matronímico. Las propiedades firstName y lastName se han introducido para mantener la compatibilidad con los sistemas existentes que modelan los nombres de una manera simplificada, no semántica y no internacionalizable. Siempre es preferible utilizar xdm:fullName. |
| `b2b.personStatus` | Estado del lead | ? | cadena | cadena | Campo que registra el estado actual de marketing/ventas de la persona. |
| `b2b.isMarketingSuspended` | Marketing suspendido | ? | booleano | booleano | Indica si el marketing está suspendido para la persona. |
| `b2b.marketingSuspendedCause` | Causa de suspensión de marketing | ? | cadena | cadena | Si el marketing está suspendido para la persona, esta propiedad proporciona el motivo por el que. |
| `person.name.middleName` | Segundo nombre | ? | cadena | teléfono | Segundos nombres, nombres alternativos o adicionales que se ponen entre el nombre y los apellidos. |
| `mobilePhone.number` | Número de teléfono móvil | Número de teléfono móvil | cadena | teléfono | Número de teléfono móvil. |
| `workPhone.number` | Número de teléfono | Número de teléfono | cadena | teléfono | Número de teléfono de trabajo. |
| `workAddress.postalCode` | Código postal | Código postal | cadena | cadena | El código postal de la ubicación. Los códigos postales no están disponibles en todos los países. En algunos países, solo contiene parte del código postal. |
| `person.name.courtesyTitle` | Saludo | ? | cadena | cadena | Normalmente, una abreviatura de un título, honorífico o saludo de persona. courtesyTitle se utiliza delante del nombre completo o los apellidos en los textos de apertura. Por ejemplo, Sr., Sra. o Dr. |
| `workAddress.state` | Estado | Estado | cadena | cadena | El nombre del estado. Este es un campo de forma libre. |
| `consents.marketing.email.val` | Suscripción cancelada | Suscripción cancelada | cadena | booleano | Si la cancelación de la suscripción es verdadera (por ejemplo, valor = 1), establezca `consents.marketing.email.val` como (n). Si la cancelación de la suscripción es falsa (por ejemplo, valor = 0), establezca conents.marketing.email.val como nula. |
| `consents.marketing.email.reason` | Razón de la cancelación de la suscripción | Razón de la cancelación de la suscripción | cadena | cadena |  |
| `b2b.companyWebsite` | Sitio web | ? | cadena | url | Sitio web de la compañía con la que está asociado un profesional. |

