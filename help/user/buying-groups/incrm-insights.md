---
title: Perspectivas en CRM
description: Acceda a los grupos de compra de Journey Optimizer B2B edition directamente en los CRM. Los miembros del equipo de ventas pueden ver los datos de participación e identificar las oportunidades de ventas con Perspectivas In-CRM.
feature: Sales Insights, Buying Groups
role: User
exl-id: c55a1fce-2ddc-481b-9f60-5e67a4bf9633
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
autotag-review: 2026-03-30T21:40:22.011Z
TQID: https://experienceleague.adobe.com/HfypAUMJxZyWaQlkknyxUn63x5uVqcfJU-pzXcDWYBs
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 483
ht-degree: 2%

---

# Perspectivas en CRM

[!DNL In-CRM Insights] es una aplicación basada en web que se integra en Salesforce y Microsoft Dynamics 365, lo que le permite acceder a [!DNL Journey Optimizer B2B Edition] grupos de compra directamente dentro de su CRM. Agrupa fuentes de datos de ventas, lo que facilita la identificación de oportunidades para aumentar la participación y el potencial de ventas.

## Instalación

El proceso de instalación incluye lo siguiente:

* Configuración de permisos y grupos de usuarios
* Instalación del paquete de software
* Inicio de sesión a través de CRM

### Definición de permisos

Los usuarios que instalen el software deben tener permisos para instalar paquetes de Salesforce.

Para tener acceso a la aplicación, los usuarios deben ser miembros de un rol con el permiso **Información sobre ventas:View Información sobre ventas**.

Si desea restringir los usuarios solo a [!DNL In-CRM Insights]:

1. Cree una [función personalizada](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role) y asígnele el permiso **Perspectivas de ventas: Ver perspectivas de ventas**.
1. Crear un nuevo [grupo de usuarios](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group).
1. Añada un perfil de producto de Experience Platform al grupo.

### Instalación del paquete

Para instalar el paquete de In-CRM Insights, siga los pasos para Salesforce o Microsoft Dynamics.

#### Salesforce

1. Descargue el [paquete del instalador de Insights en CRM](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce).
1. Después de iniciar sesión, se le redirigirá a la página de instalación del paquete.
1. Seleccione la opción **[!UICONTROL Instalar para todos los usuarios]** y haga clic en **[!UICONTROL Instalar]**.

   ![Instalar el paquete de perspectivas en CRM](assets/incrm-install-sf.png){width=500}

1. Apruebe el acceso de terceros en el cuadro de diálogo y, a continuación, haga clic en **[!UICONTROL Continuar]**.
1. Cuando finalice la instalación, haga clic en **[!UICONTROL Listo]**.

   Ahora aparece en la lista de la página **Paquetes instalados** y **Journey Optimizer B2B edition** aparece en el lanzador de aplicaciones.

   ![Información en CRM configurada en Salesforce](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. Descargue el [paquete del instalador de Insights en CRM](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics).
1. Vaya al [portal de aplicaciones de energía](https://make.powerapps.com/){target=_blank}.
1. Después de iniciar sesión, seleccione el entorno del paquete y vaya a **[!UICONTROL Soluciones]** en el menú de la izquierda.
1. Haga clic en **[!UICONTROL Importar solución]**.
1. Busque y cargue el paquete del instalador y haga clic en **[!UICONTROL Siguiente]**.
1. Compruebe los detalles del paquete y haga clic en **[!UICONTROL Siguiente]**.
1. En _Variables de entorno_, compruebe que el valor esté establecido en `prod` (no cambie el valor) y haga clic en **[!UICONTROL Importar]**.
1. Una vez finalizada la instalación, **[!UICONTROL Journey Optimizer B2B edition]** > **[!UICONTROL Grupos de compra]** se muestra en la barra de navegación izquierda.

   ![Información en CRM disponible en Microsoft Dynamics](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## Ver los grupos de compra

Siga las indicaciones para iniciar sesión en su cuenta de Adobe. Los grupos de compra están cargados y disponibles para su visualización.

Después de seleccionar un grupo de compra, puedes examinar los [detalles del grupo](https://experienceleague.adobe.com/es/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#). Es igual que los datos y las perspectivas mostrados en Journey Optimizer B2B edition, pero los datos son de solo lectura hasta [!DNL In-CRM Insights].
