---
title: Campos XDM
description: Revise los campos de atributos predeterminados que se sincronizan entre Adobe Experience Platform y Journey Optimizer B2B edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 16%

---

# Campos de XDM

Los datos de audiencia de cuenta se almacenan como atributos en las clases Cuenta empresarial de XDM y Persona empresarial de XDM. Los datos se sincronizan periódicamente entre Adobe Experience Platform y Journey Optimizer B2B edition. En las secciones siguientes se enumeran los conjuntos predeterminados de atributos.

>[!TIP]
>
>Puede modelar clases de persona de negocios XDM y de cuenta de negocios XDM en una relación de varios a varios mediante la clase de relación de persona de cuenta de negocios XDM como se describe en la [documentación de Experience Platform XDM](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

## Atributos de relación de persona de la cuenta XDM

| [Propiedad](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nombre para mostrar | Nombre para mostrar de Journey Optimizer B2B | Tipo de datos | Descripción |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Funciones de persona | Función | Matriz de cadenas | Una matriz de funciones asociadas con la persona de la cuenta, como `owner, accountant, designer`. |

## Atributos de persona empresarial de XDM

>[!IMPORTANT]
>
>Se requiere el atributo `workEmail.Address`. Si está vacía para un miembro de la audiencia de una cuenta, esa persona no se ingiere y se omite en los recorridos de la cuenta y en los grupos de compra que hacen referencia a la audiencia.

| [Propiedad](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Nombre para mostrar | Nombre para mostrar de Journey Optimizer B2B | Tipo de datos | Descripción |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
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
| `workEmail.address` | Dirección | Correo electrónico | Cadena | **Campo obligatorio** <br/>La dirección técnica, por ejemplo, `<name@domain.com>`, tal como se define comúnmente en RFC2822 y estándares subsiguientes. |
| `workEmail.status` | Estado | Email suspendido | Cadena | Una indicación de la capacidad de uso de la dirección de correo electrónico. |
| `workPhone.number` | Número | Número de teléfono | Cadena | Número de teléfono de trabajo. |

## Atributos de cuenta empresarial de XDM

>[!IMPORTANT]
>
>Se requiere el atributo `accountName`. Si está vacía para una cuenta en una audiencia de cuenta, esa cuenta no se ingiere y se omite en los recorridos de cuentas y grupos de compra que hacen referencia a la audiencia.

| [Propiedad](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | Nombre para mostrar | Nombre para mostrar de Journey Optimizer B2B | Tipo de datos | Descripción |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Ciudad | Ciudad | Cadena | El nombre de la ciudad usado en la dirección de facturación. |
| `accountBillingAddress.country` | País | País | Cadena | El nombre del territorio administrado por el gobierno que se usa en la dirección de facturación. Aparte de `xdm:countryCode`, es un campo de forma libre que puede tener el nombre del país en cualquier idioma. |
| `accountBillingAddress.postalCode` | Código postal | Código postal de la dirección | Cadena | El código postal de la ubicación de la dirección de facturación. Los códigos postales no están disponibles en todos los países. En algunos países, solo contiene parte del código postal. |
| `accountBillingAddress.region` | Región | Región de dirección | Cadena | La parte de región, condado o distrito de la dirección de facturación. |
| `accountBillingAddress.state` | Estado | Estado | Cadena | El nombre del estado de la dirección de facturación. Es un campo de forma libre. |
| `accountBillingAddress.street1` | Calle 1 | Calle 1 | Cadena | Información principal de la dirección de facturación, que generalmente incluye el número del apartamento, el número de la calle y el nombre de la calle. |
| `accountName` | Nombre | Nombre | Cadena | **Campo obligatorio** <br/>Nombre de la compañía. Se permiten hasta 255 caracteres en este campo. |
| `accountOrganization.annualRevenue.amount` | Ingresos anuales | Ingresos anuales | Número | Cantidad estimada de los ingresos anuales de la organización. |
| `accountOrganization.industry` | Industria | Industria | Cadena | La industria atribuida a la organización. Es un campo de forma libre, y es recomendable usar un valor estructurado para consultas o usar la propiedad `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL de logotipo | URL de logotipo | Cadena | Ruta que combinar con la URL de una instancia de Salesforce (por ejemplo, `https://yourInstance.salesforce.com/`) para generar una URL para solicitar la imagen de perfil de red social asociada con la cuenta. La URL generada devuelve un redireccionamiento HTTP (código 302) a la imagen de perfil de la red social de la cuenta. |
| `accountOrganization.numberOfEmployees` | Número de empleados | Cantidad de empleados | Entero | El número de empleados de la organización. |
| `accountOrganization.SICCode` | Código SIC | Código SIC | Cadena | El código de Clasificación Industrial Estándar (SIC) es un código de cuatro dígitos que categoriza los sectores a los que pertenecen las empresas en función de sus actividades comerciales. |
| `accountOrganization.website` | URL del sitio web | Nombre de dominio | Cadena | Dirección URL del sitio web de la organización. |
| `accountPhone.number` | N/A | Número de teléfono de cuenta | Cadena | El número de teléfono asociado con la cuenta. |
| `accountSourceType` | N/A | Tipo de origen | Cadena | Tipo de Source de la cuenta. |

## Atributos de oportunidad empresarial de XDM

Además, los datos de oportunidad se almacenan como atributos en la clase de oportunidad empresarial de XDM, que se puede asociar a la clase de cuenta empresarial de XDM mediante una relación de varios a uno, como se describe en la [documentación de Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

| [Propiedad](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} | Nombre para mostrar | Nombre para mostrar de Journey Optimizer B2B | Tipo de datos | Descripción |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Fecha de cierre esperada | Fecha de cierre de oportunidad prevista | Cadena | Fecha prevista de cierre de la oportunidad. |
| `expectedRevenue.amount` | Ingreso esperado | Ingreso esperado total de la oportunidad | Cadena | Ingresos calculados basados en el importe y la probabilidad. |
| `fiscalQuarter` | Trimestre fiscal | Trimestre fiscal de oportunidad | Cadena | El trimestre fiscal objetivo de la oportunidad. |
| `fiscalYear` | Año fiscal | Año fiscal de oportunidad | Cadena | El año fiscal objetivo de la oportunidad. |
| `forecastCategory` | Categoría de pronóstico | Categoría de pronóstico de oportunidad | Cadena | Categoría de pronóstico determinada por el valor de la fase de oportunidad. |
| `forecastCategoryName` | Nombre de la categoría de pronóstico | Nombre de categoría de previsión de oportunidad | Cadena | Nombre de la categoría de pronóstico que se muestra en los informes de una categoría de pronóstico determinada. |
| `isClosed` | Indicador cerrado | Oportunidad cerrada | Cadena | Indicador que indica si la oportunidad está cerrada. |
| `isWon` | Indicador obtenido | Oportunidad ganada | Cadena | Indicador que indica si se ha ganado la oportunidad. |
| `lastActivityDate` | Fecha de la última actividad | Fecha de la última actividad | Cadena | Fecha de la última actividad de la oportunidad. |
| `leadSource` | Origen del lead | Origen del cliente potencial | Cadena | Source de la oportunidad, como un anunciante, un socio o la web. |
| `nextStep` | Siguiente paso | Paso siguiente de la oportunidad | Cadena | Descripción de la siguiente tarea para cerrar la oportunidad. |
| `opportunityAmount.amount` | Monto de la oportunidad | Monto total de la oportunidad | Cadena | Importe total de venta estimado de la oportunidad. |
| `opportunityDescription` | Descripción de la oportunidad | Descripción de oportunidad | Cadena | Información adicional para describir la oportunidad, como posibles productos para vender o compras anteriores al cliente. |
| `opportunityName` | Nombre de la oportunidad | Nombre de oportunidad | Cadena | Asunto o nombre descriptivo, como el pedido esperado o el nombre de la empresa, de la oportunidad. |
| `opportunityQuantity` | Cantidad de la oportunidad | Cantidad de oportunidad | Cadena | Total de todos los valores de campo de cantidad de todos los productos en la lista de productos relacionados para la oportunidad. |
| `opportunityStage` | Etapa de la oportunidad | Fase de oportunidad | Cadena | Fase de ventas de la oportunidad para ayudar al equipo de ventas en sus esfuerzos por ganarla. |
| `opportunityType` | Tipo de oportunidad | Tipo de oportunidad | Cadena | Tipo asignado a la oportunidad, como _Empresa existente_ o _Nueva empresa_ |
| `probabilityPercentage` | Porcentaje de probabilidad | Porcentaje de probabilidad de oportunidad | Cadena | Probabilidad de cerrar la oportunidad, expresada como porcentaje. |
