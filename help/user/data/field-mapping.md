---
title: Campos XDM
description: Revise los campos de atributos predeterminados que se sincronizan entre Adobe Experience Platform y Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: b38878ca063967e6c1ae56617674af52c10913df
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 16%

---

# Campos XDM

Los datos de audiencia de cuenta se almacenan como atributos en las clases Cuenta empresarial de XDM y Persona empresarial de XDM. Los datos se sincronizan periódicamente entre Adobe Experience Platform y Journey Optimizer B2B Edition. En las secciones siguientes se enumeran los conjuntos predeterminados de atributos.

## Atributos de persona empresarial de XDM

| [Propiedad](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Nombre para mostrar | Nombre para mostrar de Journey Optimizer B2B | Tipo de datos | Descripción |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | Nombre de la empresa | Nombre de la empresa | Cadena | Nombre de la compañía con la que está asociado un profesional. |
| `b2b.companyWebsite` | Sitio web de empresa | Sitio web | Cadena | Sitio web de la compañía con la que está asociado un profesional. |
| `b2b.isMarketingSuspended` | Indicador suspendido de marketing | Marketing suspendido | Booleano | El valor indica si el marketing está suspendido para la persona. |
| `b2b.marketingSuspendedCause` | Causa de suspensión de marketing | Causa de suspensión de marketing | Cadena | Si el marketing está suspendido para la persona, esta propiedad proporciona el motivo por el que. |
| `b2b.personStatus` | Estado de la persona | Estado del lead | Cadena | Campo que registra el estado actual de marketing/ventas de la persona. |
| `consents.marketing.email.reason` | Razón de exclusión | Razón de la cancelación de la suscripción | Cadena | Razón asociada con la exclusión de correo electrónico. |
| `consents.marketing.email.val` | Suscripción cancelada | Suscripción cancelada | Cadena | Si la cancelación de la suscripción es verdadera (por ejemplo, valor = 1), establezca `consents.marketing.email.val` como (n). Si la cancelación de la suscripción es falsa (por ejemplo, valor = 0), establezca `consents.marketing.email.val` como nulo. |
| `extendedWorkDetails.jobTitle` | Cargo | Cargo | Cadena | Cargo de la persona. |
| `faxPhone.number` | Número | Número de fax | Cadena | Número de teléfono fax. |
| `mobilePhone.number` | Número | Número de teléfono móvil | Cadena | El número de teléfono móvil asociado con la persona. |
| `person.birthDate` | Fecha de nacimiento (AAAA-MM-DD) | Fecha de nacimiento | Cadena | La fecha completa en la que nació una persona. DD/MM/YYYY |
| `person.name.courtesyTitle` | Título de cortesía | Saludo | Cadena | Normalmente, una abreviatura del título, el honor o el saludo de una persona. courtesyTitle se utiliza delante del nombre completo o los apellidos en los textos de apertura. Por ejemplo, Sr., Sra. o Dr. |
| `person.name.firstName` | Nombre | Nombre | Cadena | El primer segmento del nombre en el orden escrito que se acepta más comúnmente en el idioma del nombre. En muchas culturas, es el nombre personal o de pila preferido. Las propiedades firstName y lastName se han introducido para mantener la compatibilidad con los sistemas existentes que modelan los nombres de una manera simplificada, no semántica y no internacionalizable. Siempre es preferible usar `xdm:fullName`. |
| `person.name.lastName` | Apellido | Apellido | Cadena | El último segmento del nombre en el orden escrito que se acepta más comúnmente en el idioma del nombre. En muchas culturas, es el nombre de familia heredado, apellido, patronímico o matronímico. Las propiedades firstName y lastName se han introducido para mantener la compatibilidad con los sistemas existentes que modelan los nombres de una manera simplificada, no semántica y no internacionalizable. Siempre es preferible usar `xdm:fullName`. |
| `person.name.middleName` | Segundo nombre | Segundo nombre | Cadena | Segundos nombres, nombres alternativos o adicionales que se ponen entre el nombre y los apellidos. |
| `workAddress.city ` | Ciudad | Ciudad | Cadena | El nombre de la ciudad. |
| `workAddress.country` | País | País | Cadena | El nombre del territorio administrado por el gobierno. Aparte de `xdm:countryCode`, es un campo de forma libre que puede tener el nombre del país en cualquier idioma. |
| `workAddress.postalCode` | Código postal | Código postal | Cadena | El código postal de la ubicación. Los códigos postales no están disponibles en todos los países. En algunos países, solo contiene parte del código postal. |
| `workAddress.state` | Estado | Estado | Cadena | El nombre del estado de la dirección. Es un campo de forma libre. |
| `workAddress.street1` | Calle 1 | Dirección | Cadena | Información principal de la dirección postal, número de piso, número de calle y nombre de la calle. |
| `workEmail.address` | Dirección | Correo electrónico | Cadena | La dirección técnica, por ejemplo, `<name@domain.com>`, tal como se define comúnmente en RFC2822 y estándares subsiguientes. |
| `workEmail.status` | Estado | Email suspendido | Cadena | Una indicación de la capacidad de uso de la dirección de correo electrónico. |
| `workPhone.number` | Número | Número de teléfono | Cadena | Número de teléfono de trabajo. |

## Atributos de cuenta empresarial de XDM

| [Propiedad](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Nombre para mostrar | Nombre para mostrar de Journey Optimizer B2B | Tipo de datos | Descripción |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Ciudad | Ciudad | Cadena | El nombre de la ciudad usado en la dirección de facturación. |
| `accountBillingAddress.country` | País | País | Cadena | El nombre del territorio administrado por el gobierno que se usa en la dirección de facturación. Aparte de `xdm:countryCode`, es un campo de forma libre que puede tener el nombre del país en cualquier idioma. |
| `accountBillingAddress.postalCode` | Código postal | Código postal de la dirección | Cadena | El código postal de la ubicación de la dirección de facturación. Los códigos postales no están disponibles en todos los países. En algunos países, solo contiene parte del código postal. |
| `accountBillingAddress.region` | Región | Región de dirección | Cadena | La parte de región, condado o distrito de la dirección de facturación. |
| `accountBillingAddress.state` | Estado | Estado | Cadena | El nombre del estado de la dirección de facturación. Es un campo de forma libre. |
| `accountBillingAddress.street1` | Calle 1 | Calle 1 | Cadena | Información principal de la dirección de facturación, que generalmente incluye el número del apartamento, el número de la calle y el nombre de la calle. |
| `accountName` | Nombre | Nombre | Cadena | Nombre de la empresa. Se permiten hasta 255 caracteres en este campo. |
| `accountOrganization.annualRevenue.amount` | Ingresos anuales | Ingresos anuales | Número | Cantidad estimada de los ingresos anuales de la organización. |
| `accountOrganization.industry` | Industria | Industria | Cadena | La industria atribuida a la organización. Es un campo de forma libre, y es recomendable usar un valor estructurado para consultas o usar la propiedad `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL de logotipo | URL de logotipo | Cadena | Ruta que combinar con la URL de una instancia de Salesforce (por ejemplo, `https://yourInstance.salesforce.com/`) para generar una URL para solicitar la imagen de perfil de red social asociada con la cuenta. La URL generada devuelve un redireccionamiento HTTP (código 302) a la imagen de perfil de la red social de la cuenta. |
| `accountOrganization.numberOfEmployees` | Número de empleados | Cantidad de empleados | Entero | El número de empleados de la organización. |
| `accountOrganization.SICCode` | Código SIC | Código SIC | Cadena | El código de Clasificación Industrial Estándar (SIC), que es un código de cuatro dígitos que categoriza las industrias a las que pertenecen las compañías en función de sus actividades comerciales. |
| `accountOrganization.website` | URL del sitio web | Nombre de dominio | Cadena | Dirección URL del sitio web de la organización. |
| `accountPhone.number` | N/A | Número de teléfono de cuenta | Cadena | El número de teléfono asociado con la cuenta. |
| `accountSourceType` | N/A | Tipo de origen | Cadena | Tipo de Source de la cuenta. |
