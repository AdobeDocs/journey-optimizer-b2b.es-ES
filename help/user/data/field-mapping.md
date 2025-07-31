---
title: Campos XDM
description: Revise los campos de atributos predeterminados que se sincronizan entre Adobe Experience Platform y Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: b62891e3d87ac4ff5345dac564d63c0b8aaa9669
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 13%

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
>El atributo de dirección de correo electrónico es obligatorio y debe rellenarse para que funcione correctamente. De manera predeterminada, el sistema utiliza `workEmail.Address`. Si tiene intención de utilizar un atributo diferente, póngase en contacto con el Soporte técnico de Adobe antes de publicar los recorridos para garantizar la configuración adecuada.<br/>
>
>Asegúrese de que el atributo de correo electrónico no sea nulo, ya que esto puede afectar a la sincronización de datos y a los procesos descendentes.
><ul><li>Si el atributo de correo electrónico es nulo en Real-time CDP B2B y la persona existe en Journey Optimizer B2B edition, el atributo en se sobrescribe en Journey Optimizer B2B edition con un valor nulo durante la sincronización. Posteriormente, persiste en Marketo Engage como nulo.<li>Si el atributo de correo electrónico es nulo en Real-time CDP B2B y la persona no existe en Journey Optimizer B2B edition, el registro de persona no se sincroniza.<ul/>

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

<!-- ## XDM Business Opportunity attributes

Additionally, opportunity data is stored as attributes in the XDM Business Opportunity class, which can be associated with the XDM Business Account class through a many-to-one relationship, as described in the [Exerience Platform documentation](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`expectedCloseDate` | Expected Close Date  | Expected opportunity close date   | String | Expected date of closure for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | Total opportunity expected revenue   | String | Calculated revenue based on the Amount and Probability.   |
|`fiscalQuarter` | Fiscal Quarter   | Opportunity fiscal quarter  | String | The targeted fiscal quarter for the opportunity.   |
|`fiscalYear` | Fiscal Year   | Opportunity fiscal year   | String | The targeted fiscal year for the opportunity.   |
|`forecastCategory`|Forecast Category | Opportunity Forecast category | String | Forecast Category determined by the opportunity Stage value. |
|`forecastCategoryName`|Forecast Category Name | Opportunity forecast category name | String | Forecast category name that is displayed in reports for a particular forecast category. |
|`isClosed` | Closed Flag  | Opportunity closed   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | Opportunity won   | String | Flag that indicates if the opportunity is won.  |
|`lastActivityDate` | Last Activity Date  | Last activity date   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | Lead source   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | Opportunity next step   | String | Description of the next task for closing the opportunity.   |
|`opportunityAmount.amount` | Opportunity Amount  | Total Opportunity Amount | String | Estimated total sale amount for the opportunity.   |
|`opportunityDescription` | Opportunity Description   | Opportunity description  |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityName` | Opportunity Name   | Opportunity name |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityQuantity` | Opportunity Quantity  | Opportunity quantity   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`opportunityStage` | Opportunity Stage   | Opportunity stage   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`opportunityType` | Opportunity Type   | Opportunity type   | String | Type assigned to the opportunity, such as _Existing Business_ or _New Business_  |
|`probabilityPercentage` | Probability Percentage  | Opportunity probability percentage  | String | Likelihood of closing the opportunity, stated as a percentage.  |
 -->