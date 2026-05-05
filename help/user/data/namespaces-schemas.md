---
title: Espacios de nombres y esquemas B2B
description: Configure los espacios de nombres y esquemas de Experience Platform B2B para Journey Optimizer B2B edition mediante la utilidad de generación automática de Postman.
feature: Setup, Data Management
role: Admin
exl-id: 40d01027-7cf2-4189-8a49-7a0783c00721
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bdid: f7ea94b0-a6b4-43ef-bd93-f2c98c8f2072
feature_v2: id: f2da1b69-6919-4386-a5d2-9c7b5c9033dbid: c8f3fb27-3167-48ac-a66a-fa4bc3f58ddaid: d6e625c1-468f-4d73-9f32-fd1edb87f96b
subfeature_v2: id: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: d378ca77-2da1-4f39-ad92-1917fe974a38
topic_v2: id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 0216cf3b1cbc1124b50ad99e649778aef71f5aca
workflow-type: tm+mt
source-wordcount: 1004
ht-degree: 96%

---

# Espacios de nombres y esquemas B2B

La configuración de Journey Optimizer B2B edition incluye la configuración de los espacios de nombres y esquemas de Experience Platform que se utilizan con fuentes B2B. La utilidad de automatización de Postman es necesaria para generar espacios de nombres y esquemas B2B.

>[!AVAILABILITY]
>
>- Debe tener acceso a [Adobe Real-Time Customer Data Platform B2B edition](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdpb2b-intro/b2b-overview){target="_blank"} para que sus esquemas B2B califiquen en [Perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/profile/home){target="_blank"}.
>
>- Las entidades de Experience Platform B2B deben utilizar las relaciones estándar descritas en la [guía de esquemas y áreas de nombres B2B](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/schemas/b2b){target="_blank"}.

Revise la siguiente información sobre la configuración subyacente de los espacios de nombres y esquemas que se utilizarán con orígenes B2B. También proporciona detalles para configurar la utilidad de automatización de Postman, que es necesaria para generar espacios de nombres y esquemas B2B.

## Configurar la utilidad de generación automática

Consulte los siguientes recursos para conocer los requisitos previos y obtener información detallada sobre cómo configurar su entorno [!DNL Postman] para que sea compatible con el espacio de nombres B2B y la utilidad de generación automática de esquemas.

- Descargue la colección de utilidades de generación automática de esquemas y áreas de nombres del [repositorio de GitHub](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility){target="_blank"}.
- Para obtener información sobre el uso de las API de Experience Platform, incluidos detalles sobre la recopilación de valores para los encabezados necesarios y la lectura de llamadas de API de ejemplo, consulte [_Introducción a las API de Adobe Experience Platform_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-guide?lang=es){target="_blank"}.
- Para obtener información sobre cómo generar las credenciales para las API de Experience Platform, consulte [_Autenticar y acceder a las API de Experience Platform_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication){target="_blank"}.
- Para obtener información sobre la configuración de [!DNL Postman] para las API de Experience Platform, consulte [_[!DNL Postman] en Adobe Experience Platform _](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman){target="_blank"}.

### Valores de entorno

Con una consola de desarrollador de Experience Platform y [!DNL Postman] configuradas, puede aplicar los valores de entorno apropiados a su entorno [!DNL Postman]. La siguiente tabla proporciona valores de ejemplo e información adicional sobre cómo rellenar el entorno [!DNL Postman]:

| Variable | Descripción | Ejemplo |
| --- | --- | --- |
| `CLIENT_SECRET` | Un identificador único usado para generar su `{ACCESS_TOKEN}`. | `{CLIENT_SECRET}` |
| `API_KEY` | Identificador único utilizado para autenticar llamadas a las API de Experience Platform. | `c8d9a2f5c1e03789bd22e8efdd1bdc1b` |
| `ACCESS_TOKEN` | El token de autorización necesario para completar las llamadas a las API de Experience Platform. | `Bearer {ACCESS_TOKEN}` |
| `META_SCOPE` | Con respecto a [!DNL Journey Optimizer B2B] y [!DNL Marketo Engage], este valor es fijo y siempre se establece en: `ent_dataservices_sdk`. | `ent_dataservices_sdk` |
| `CONTAINER_ID` | El contenedor `global` contiene todas las clases, los grupos de campos de esquema, los tipos de datos y los esquemas proporcionados por los socios estándar de Adobe y Experience Platform. Con respecto a [!DNL Marketo], este valor es fijo y siempre se establece en `global`. | `global` |
| `TECHNICAL_ACCOUNT_ID` | Credencial utilizada para integrarse en Adobe I/O. | `D42AEVJZTTJC6LZADUBVPA15@techacct.adobe.com` |
| `IMS` | El sistema de Identity Management (IMS) proporciona el marco para la autenticación en los servicios de Adobe. Con respecto a [!DNL Journey Optimizer B2B] y [!DNL Marketo Engage], este valor es fijo y siempre se establece en: `ims-na1.adobelogin.com`. | `ims-na1.adobelogin.com` |
| `IMS_ORG` | Una entidad corporativa que puede poseer o licenciar productos y servicios y permitir el acceso a sus miembros. | `ABCEH0D9KX6A7WA7ATQE0TE@adobeOrg` |
| `SANDBOX_NAME` | Nombre de la partición de zona protegida virtual que está utilizando. | `prod` |
| `TENANT_ID` | ID que se utiliza para garantizar que los recursos que crea tengan un espacio de nombres correcto y estén contenidos en su organización. | `b2bcdpproductiontest` |
| `PLATFORM_URL` | El extremo URL al que realiza llamadas de API. Este valor es fijo y siempre se establece en: `http://platform.adobe.io/`. | `http://platform.adobe.io/` |

{style="table-layout:auto"}

### Ejecutar los scripts

Una vez que los valores de entorno estén establecidos, utilice la interfaz [!DNL Postman] para ejecutar el script para crear los espacios de nombres y esquemas. Seleccione la carpeta raíz de la utilidad autogenerador y, a continuación, seleccione **[!DNL Run]** en el encabezado superior.

![Carpeta raíz del generador de espacios de nombres y esquemas en la interfaz de usuario de Postman](./assets/namespaces-schemas-postman-root-folder.png){width="500" zoomable="yes"}

Aparecerá la interfaz [!DNL Runner]. Aquí, asegúrese de que todas las casillas de verificación estén seleccionadas y luego seleccione **[!DNL Run Namespaces and Schemas Autogeneration Utility]**.

![IU de Postman con varias solicitudes en la colección de espacios de nombres y esquemas seleccionada.](./assets/namespaces-schemas-postman-run-generator.png){width="800" zoomable="yes"}

Una solicitud correcta crea los espacios de nombres y esquemas B2B necesarios.

## Áreas de nombres B2B

Las áreas de nombres de identidad son un componente de Experience Platform [[!DNL Identity Service]](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"} que sirve para distinguir el contexto de una identidad. Una identidad completa incluye un valor de identidad y un área de nombres. Vea [información general sobre áreas de nombres](https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces){target="_blank"} para obtener más información.

Las áreas de nombres B2B se utilizan en la identidad principal de la entidad.

| Nombre para mostrar | Símbolo de identidad | Tipo de identidad |
| --- | --- | --- |
| Persona B2B | `b2b_person` | `CROSS_DEVICE` |
| Cuenta B2B | `b2b_account` | `B2B_ACCOUNT` |
| Oportunidad B2B | `b2b_opportunity` | `B2B_OPPORTUNITY` |
| Relación de persona de oportunidad B2B | `b2b_opportunity_person_relation` | `B2B_OPPORTUNITY_PERSON` |
| Campaña B2B | `b2b_campaign` | `B2B_CAMPAIGN` |
| Miembro de la campaña B2B | `b2b_campaign_member` | `B2B_CAMPAIGN_MEMBER` |
| Lista de marketing B2B | `b2b_marketing_list` | `B2B_MARKETING_LIST` |
| Miembro de lista de marketing B2B | `b2b_marketing_list_member` | `B2B_MARKETING_LIST_MEMBER` |
| Relación de persona de la cuenta B2B | `b2b_account_person_relation` | `B2B_ACCOUNT_PERSON` |

{style="table-layout:auto"}

## Esquemas B2B

Experience Platform utiliza esquemas para describir la estructura de los datos de una manera uniforme y reutilizable. Al definir los datos de forma coherente en todos los sistemas, resulta más fácil conservar el significado y, por lo tanto, obtener valor de los datos.

Para que Experience Platform pueda introducir datos, debe haber un esquema que describa la estructura de los datos y proporcione restricciones al tipo de datos que se pueden contener en cada campo. Los esquemas constan de una clase base y cero o más grupos de campos de esquema.

Para obtener más información sobre el modelo de composición de esquema, incluidos los principios de diseño y las prácticas recomendadas, vea [_Conceptos básicos de la composición de esquema_](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}.

+++ Cuenta B2B

<table>
    <tr>
        <td style="width: 30%;">Clase base</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account" target="_blank">Cuenta empresarial de XDM</a></td>
    </tr>
    <tr>
        <td>Grupos de campos</td>
        <td>Detalles de la cuenta empresarial de XDM</td>
    </tr>
    <tr>
        <td>[!DNL Profile] en el esquema</td>
        <td>Habilitado</td>
    </tr>
    <tr>
        <td>Identidad principal</td>
        <td><code>accountKey.sourceKey</code> en la clase base</td>
    </tr>
    <tr>
        <td>Espacio de nombres de identidad principal</td>
        <td>Cuenta B2B</td>
    </tr>
    <tr>
        <td>Identidad secundaria</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> en la clase base</td>
    </tr>
    <tr>
        <td>Área de nombres de identidad secundaria</td>
        <td>Cuenta B2B</td>
    </tr>
    <tr>
        <td>Relación</td>
        <td><ul><li><code>accountParentKey.sourceKey</code> en el grupo de campos Detalles de cuenta empresarial de XDM</li><li>Propiedad de destino: <code>/accountKey/sourceKey</code></li><li>Tipo: uno a uno</li><li>Esquema de referencia: cuenta B2B</li><li>Área de nombres: Cuenta B2B</li></ul> </td>
    </tr>
</table>

+++

+++ Persona B2B

<table>
    <tr>
        <td style="width: 30%;">Clase base</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile">Perfil individual de XDM</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Grupos de campos</td>
        <td><ul><li>Detalles de la persona empresaria de XDM</li><li>Componentes de la persona empresaria de XDM</li><li>IdentityMap</li><li>Detalles de consentimiento y preferencia</li></ul> </td>
    </tr>
    <tr>
        <td>[!DNL Profile] en el esquema</td>
        <td>Habilitado</td>
    </tr>
    <tr>
        <td>Identidad principal</td>
        <td><code>b2b.personKey.sourceKey</code> en el grupo de campos Detalles de persona de negocio de XDM</td>
    </tr>
    <tr>
        <td>Espacio de nombres de identidad principal</td>
        <td>Persona B2B</td>
    </tr>
    <tr>
        <td>Identidad secundaria</td>
        <td><ol><li><code>extSourceSystemAudit.externalKey.sourceKey</code> del grupo de campos Detalles de persona de negocio de XDM</li><li><code>workEmail.address</code> del grupo de campos Detalles de persona de negocio de XDM</li></ol></td>
    </tr>
    <tr>
        <td>Área de nombres de identidad secundaria</td>
        <td><ol><li>Persona B2B</li><li>Correo electrónico</li></ol></td>
    </tr>
    <tr>
        <td>Relación</td>
        <td><ul><li><code>personComponents.sourceAccountKey.sourceKey</code> del grupo de campos Componentes de persona de negocio XDM</li><li>Tipo: varios a uno</li><li>Esquema de referencia: Cuenta B2B</li><li>Área de nombres: Cuenta B2B</li><li>Propiedad de destino: accountKey.sourceKey</li><li>Nombre de relación del esquema actual: Cuenta</li><li>Nombre de relación del esquema de referencia: Personas</li></ul> </td>
    </tr>
</table>

+++

<!--

+++B2B Opportunity

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity">XDM Business Opportunity</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Opportunity Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in the base class</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td><ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: Opportunities</li></ul></td>
    </tr>
</table>

+++

+++B2B Opportunity Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation">XDM Business Opportunity Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td> **First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Opportunities</li></ul>**Second relationship**<ul><li><code>opportunityKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Opportunity </li><li>Namespace: B2B Opportunity </li><li>Destination property: <code>opportunityKey.sourceKey</code></li><li>Relationship name from current schema: Opportunity</li><li>Relationship name from reference schema: People</li></ul> </td>
    </tr>
</table>


+++

+++B2B Campaign

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign">XDM Business Campaign</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

+++

+++B2B Campaign Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign-members">XDM Business Campaign Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Member Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Campaigns</li></ul>**Second relationship**<ul><li><code>campaignKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Campaign</li><li>Namespace: B2B Campaign</li><li>Destination property: <code>campaignKey.sourceKey</code></li><li>Relationship name from current schema: Campaign</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++B2B Marketing List

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list">XDM Business Marketing List</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

>[!NOTE]
>
>Static List in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Marketing List Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members">XDM Business Marketing List Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Marketing Lists</li></ul>**Second relationship**<ul><li><code>marketingListKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Marketing List</li><li>Namespace: B2B Marketing List</li><li>Destination property: <code>marketingListKey.sourceKey</code></li><li>Relationship name from current schema: Marketing List</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

>[!NOTE]
>
>Static List member in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Account Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account-person-relation">XDM Business Account Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>Identity Map</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>accountPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Account Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: People</li><li>Relationship name from reference schema: Account</li></ul>**Second relationship**<ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++
-->
