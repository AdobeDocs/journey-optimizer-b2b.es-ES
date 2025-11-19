---
title: Perspectivas en CRM
description: Acceda a los grupos de compra de Journey Optimizer B2B edition directamente en Salesforce. Los miembros del equipo de ventas pueden ver los datos de participación e identificar las oportunidades de ventas con Perspectivas In-CRM.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Perspectivas en CRM

In-CRM Insights es una aplicación basada en web que se integra en Salesforce, lo que le permite acceder a sus grupos de compra de Journey Optimizer B2B edition directamente dentro de Salesforce. Permite identificar oportunidades para aumentar la participación y el potencial de ventas.

La aplicación In-CRM Insights está disponible en [Marketo Sales Insights package](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange).

## Permisos

Para tener acceso a la aplicación, los usuarios deben ser miembros de un rol con el permiso **Información sobre ventas:View Información sobre ventas**

Si desea restringir un grupo de usuarios a InCRM-Insights, utilice las siguientes directrices para crear una función personalizada específicamente para InCRM-Insights:

* Cree una función personalizada con el conjunto de permisos **Información de ventas:View Información de ventas** solamente.
* Cree un nuevo grupo de usuarios sin agregar perfiles de producto.
* Cree otro grupo de usuarios y añada un perfil de producto de AEP, o bien agregue un perfil de AEP existente al grupo de usuarios que acaba de crear.
* Asigne los nuevos grupos de usuarios a la nueva función y agregue nuevos usuarios a los nuevos grupos de usuarios.

## Uso de Insights en CRM

La aplicación In-CRM Insights está disponible en Salesforce a través del lanzador de aplicaciones.

1. Haga clic en el lanzador de aplicaciones en Salesforce.
1. Seleccione o busque `Journey Optimizer B2B Edition`.
1. En la pestaña que se muestra, inicie sesión con sus credenciales de Adobe.
1. Elija una zona protegida que aloje sus Recorridos de cuenta.

Los grupos de compra están cargados y disponibles. Los datos son de solo lectura mediante Insights en CRM.

>[!NOTE]
>
>Se requiere la pertenencia a la función de producto [Usuario de ventas B2B](../admin/user-management.md#b2b-built-in-roles) para acceder a las perspectivas en CRM.

Después de seleccionar un grupo de compra, puedes examinar los [detalles del grupo](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#), como en Journey Optimizer B2B edition.
