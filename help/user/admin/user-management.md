---
title: Gestión de usuarios
description: Obtenga información sobre cómo asignar integrantes del equipo a perfiles de producto de Journey Optimizer B2B edition.
feature: Setup, Permissions
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: 8fd1bda4a0ccfa2abe84974f7e895825477a7299
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 2%

---

# Administración de usuarios

Una vez completado el aprovisionamiento y enlazados los entornos limitados, complete los siguientes pasos para proporcionar acceso a Adobe Journey Optimizer B2B edition a su equipo y a los usuarios.

1. [Crear un perfil de producto de Marketo Engage](#marketo-engage-profile) en Admin Console (solo una nueva instancia de Marketo Engage).
1. [Crear un grupo de usuarios](#create-user-group) en Admin Console.
<!-- 1. [Edit built-in roles](#edit-roles) or [create a custom role](#create-a-custom-role) with Journey Optimizer B2B Edition permissions. -->
1. [Agregar usuarios](#add-users) o [grupos](#add-user-groups-to-a-role) a los roles.

Como administrador, puede completar estas tareas en Adobe Admin Console, que es un lugar central para administrar las licencias y los usuarios de productos de Adobe. En Admin Console, puede crear y administrar usuarios en una sola ubicación en lugar de en las distintas soluciones individuales. Consulte la página [Información general de Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html) para obtener más información sobre sus funciones y capacidades.

## Acceso a Admin Console

Antes de poder usar Admin Console para administrar usuarios dentro de su equipo, debe asegurarse de que puede acceder a Admin Console y de que dispone de los permisos adecuados.

1. Como administrador del sistema, debe recibir varios correos electrónicos de Adobe como parte del proceso de incorporación.

   Busque el correo electrónico de bienvenida que proporciona la información acerca del nombre de la organización a la que se le ha concedido acceso.

1. Haga clic en el vínculo **[!UICONTROL Introducción]** del correo electrónico de bienvenida para ir a Admin Console.

   Si no encuentra el correo electrónico, abra un explorador directamente en Admin Console en [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Inicie sesión con su Adobe ID.

   Una vez que inicie sesión correctamente, verá la página _Información general_ de Adobe Admin Console.

1. Si tiene acceso a varias organizaciones, asegúrese de haber iniciado sesión en la organización correcta.

   Para cambiar su organización, haga clic en el nombre de la organización en la esquina superior derecha y seleccione la organización a la que necesita acceder.

1. Seleccione **[!UICONTROL Administradores]** de la tarjeta _[!UICONTROL Usuarios]_ para comprobar que es administrador del sistema.

   ![Información general de Admin Console: haga clic en Administradores](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Busque introduciendo su correo electrónico, nombre de usuario, nombre o apellidos de Adobe ID.

   * Si el acceso está configurado correctamente, la búsqueda devolverá el registro.

   * Si el valor de la columna **[!UICONTROL ROL DE ADMINISTRADOR]** muestra `System`, sabrá que usted (o el usuario mostrado) es administrador del sistema.

## Creación del perfil de producto de Marketo Engage {#marketo-engage-profile}

Al conceder a los usuarios acceso a una solución de Adobe, no necesariamente desea darles acceso completo. Los perfiles de producto permiten que cada solución tenga su propio conjunto de permisos de usuario. Utilice Admin Console para asignar perfiles de producto.

Para obtener más información sobre el uso de perfiles de producto para las autorizaciones de usuario, consulte [Administrar perfiles de producto para usuarios empresariales](https://helpx.adobe.com/es/enterprise/using/manage-product-profiles.html){target="_blank"} en la documentación de Admin Console.

>[!BEGINSHADEBOX]

Cuando agrega un usuario al perfil de producto de Marketo Engage, posteriormente se agrega al rol _Usuario estándar_ dentro del área de trabajo predeterminada de la suscripción de Marketo Engage. Esta función les otorga a todos los _usuarios estándar_ permisos para Marketo Engage en ese espacio de trabajo. Actualmente, todos los usuarios de Journey Optimizer B2B edition deben ser usuarios de Marketo Engage. Un administrador de Marketo Engage puede restringir el acceso actualizando los permisos de la función _Usuario estándar_ o moviendo al usuario a una función de usuario de Marketo Engage diferente con permisos más restrictivos.

Para obtener más información sobre la administración de estos permisos en Marketo Engage, consulte [Administración de roles y permisos de usuarios](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} en la documentación de Marketo Engage.

>[!ENDSHADEBOX]

![Requisitos de función de administrador](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrador del sistema o de producto de Marketo Engage puede realizar los siguientes pasos.

1. Inicie sesión en [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Seleccione la ficha **[!UICONTROL Productos]**.

1. Abra la instancia de Marketo Engage donde desee agregar el perfil y haga clic en **[!UICONTROL Nuevo perfil]**.

   ![Admin Console - Instancia de Marketo Engage - Nuevo perfil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Escriba un nombre de perfil de producto, como _Usuario estándar_.

1. Haz clic en **Siguiente** y luego en **Guardar**.

## Crear un grupo de usuarios {#create-user-group}

Un grupo de usuarios es una colección de usuarios a los que se concede un conjunto compartido de permisos. Puede agregar o quitar usuarios de su grupo de usuarios. Los permisos del grupo siguen siendo los mismos mientras cambian los usuarios dentro del grupo.

Para obtener más información sobre cómo se usan los grupos de usuarios para administrar permisos, consulte [Administrar grupos de usuarios](https://helpx.adobe.com/es/enterprise/using/user-groups.html){target="_blank"} en la documentación de Admin Console.

![Requisitos de función de administrador](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrador del sistema puede realizar los siguientes pasos.

1. Inicie sesión en [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Seleccione la ficha **[!UICONTROL Usuarios]**.

1. Elija **[!UICONTROL grupos de usuarios]** en el panel de navegación izquierdo.

1. Haga clic en **[!UICONTROL Nuevo grupo de usuarios]** en la parte superior derecha.

1. Escriba un nombre para el grupo de usuarios, como _Usuarios estándar_ y haga clic en **[!UICONTROL Guardar]**.

1. Haga clic en el grupo de usuarios que acaba de crear.

1. Seleccione la ficha **[!UICONTROL Perfiles de producto asignados]** y haga clic en **[!UICONTROL Asignar perfil]**.

1. Haga clic en **+** y agregue cada instancia de los siguientes productos:

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Recopilación de datos de Adobe Experience Platform]
   * [!UICONTROL Acceso completo a la recopilación de datos]

   ![Admin Console - grupo de usuarios - agregar productos](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.

## Adición de usuarios a un grupo

Para obtener información acerca de la administración de usuarios, consulte [Usuarios de Admin Console](https://helpx.adobe.com/es/enterprise/using/user-groups.html) en la documentación de Admin Console.

![Requisitos de función de administrador](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrador del sistema o de producto puede realizar los siguientes pasos. Un administrador de productos solo puede agregar usuarios que ya existen en su organización.

1. Vaya a [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. En _[!UICONTROL Vínculos rápidos]_, haga clic en **[!UICONTROL Agregar usuarios]**.

1. Añada cada usuario:

   * Introduzca la dirección de correo electrónico, el nombre y los apellidos del usuario.

     ![Experience Platform - agregar perfiles para el nuevo rol](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * Para **[!UICONTROL grupos de usuarios]**, haga clic en **+**.

   * Seleccione el grupo de usuarios que creó anteriormente.

   * Haga clic en **[!UICONTROL Aplicar]**.

1. Haga clic en **[!UICONTROL Guardar]**.

<!-- ## Edit roles for product permissions {#edit-roles}

Permissions are unitary rights that allow you to define the authorizations assigned to a product profile. Each permission is gathered under a capability, such as journeys or buying groups, which represents the different functionalities or objects in Journey Optimizer B2B Edition.

The _Permissions_ area of Adobe Experience Platform is where administrators can define user roles and access policies to manage access permissions for features and objects within a product application. In this app, you can create and manage roles, as well as assign the desired resource permissions for these roles. Permissions also allow you to manage the sandboxes and users associated with a specific role.

For more information about role permissions in Experience Platform, see [Manage permissions for a role](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} in the Experience Platform documentation.

### B2B product permissions

The following permissions govern access to Journey Optimizer B2B Edition capabilities:

| Category | Description | Permissions |
| -------- | ----------- | ---------- |
| B2B Account Lists | Configure, manage, view, and publish permissions for B2B account lists. These permissions include actions such as add, remove, import, and delete accounts from account lists. | <li>Manage B2B Account Lists |
| B2B Admin Configurations | Configure, manage, and view permissions for B2B administrative configurations. These permissions include digital asset management connections, asset repositories, and events. | <li>Manage B2B Admin Configurations |
| B2B Assets | Configure, manage, and view permissions for B2B assets. These permissions include emails, SMS, landing pages, fragments, templates, and images. | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments|
| B2B Buying Groups | Configure, manage, and view permissions for B2B buying groups. These permissions include solution interests, roles templates, and buying group status. | <li>Manage B2B Buying Groups |
| B2B Channel Configurations | Configure, manage, and view permissions for B2B channel configurations. These permissions include settings for communication limits, API credentials, and security settings. | <li>Manage B2B Channels Configurations |
| B2B Dashboards |Configure and view permissions for B2B dashboards. These permissions include account engagement, buying group stages, surging accounts, and contact coverage. | <li>Manage B2B Dashboards |
| B2B Journeys | Configure manage, view, and publish permissions for B2B journeys. These permissions include account and person actions, event listeners, and split paths | <li>Manage B2B Journeys |

### B2B built-in roles

When your organization has the Journey Optimizer B2B Edition product provisioned, Experience Platform includes a set of built-in (default) roles that you can use to manage access to the product capabilities:

| Role | Permissions |
| ---- | ----------- |
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Engagement Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View B2B Engagement Dashboard |

### Edit role permissions

For built-in or custom roles, you can decide at any time to add or delete permissions. If you modify a default or custom role, it impacts every user assigned to the role.

In the following example, you want to add permissions related to the B2B Journeys resource for users assigned to the B2B Channel Manager role. This change enables users for that role to manage account journeys also.

>[!NOTE]
>
>An Admin Console system administrator can perform these steps.

_To change the permissions for a role:_

1. Go to [experience.adobe.com](https://experience.adobe.com/).

1. In the _[!UICONTROL Quick access]_ panel, select **[!UICONTROL Permissions]**.

   >[!NOTE]
   >
   >If you don't see _[!UICONTROL Permissions]_, you may need to click **[!UICONTROL View all]** and select it from the available applications.

   ![Experience Platform - access Permissions](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Select **[!UICONTROL Roles]** in the left navigation.

1. Click the **_B2B Channel Manager_** role name.

1. In the details page, click **[!UICONTROL Edit]** at the top right.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   In the role editor, the _[!UICONTROL Resources]_ menu displays the list of resources that apply to the Experience Cloud - Platform powered applications products.

   You can enter _B2B_ in the search tool to filter the list for the B2B product permissions. 
   
1. Click the _Add_ icon (**+**) for the B2B Journeys resource.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-add.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL B2B Journeys]_ permissions card, select **[!UICONTROL Manage B2B Account Journeys]**.

1. Click **[!UICONTROL Save]**.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Close]** to return to the details page.

### Add users to a role

![Administrator role requirements](../../assets/do-not-localize/icon-admin-user.svg){width="30"} A system administrator or AEP product administrator can perform the following steps. 

1. Open the role details and select the **[!UICONTROL Users]** tab.

   This tab displays a list of all users assigned to the role.

1. Click **[!UICONTROL Add users]**.

   ![Experience Platform - add users to the role](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL Add users]_ dialog, locate and select the users that you want to add to the role.

   * You can use the Search tool to filter the list of users. 

   * Select the checkbox for each user.

   ![Experience Platform - Add users dialog](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]** when you have selected all the users that you want to add.

### Add user groups to a role

For information about user management, see [Admin Console users](https://helpx.adobe.com/enterprise/using/user-groups.html) in the Admin Console documentation.

![Administrator role requirements](../../assets/do-not-localize/icon-admin-user.svg){width="30"} A system administrator or AEP product administrator can perform the following steps. 

1. Open the role details and select the **[!UICONTROL User groups]** tab.

   This tab displays a list of all user groups assigned to the role. 

1. Click **[!UICONTROL Add Groups]**.

   ![Experience Platform - add users to the role](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL Add groups]_ dialog, locate and select the groups that you want to add to the role.

   * You can use the Search tool to filter the list of user groups. 

   * Select the checkbox for each user group.

   ![Experience Platform - Add groups dialog](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]** when you have selected all the users that you want to add. -->

## Crear una función personalizada

![Requisitos de función de administrador](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrador del sistema o de producto de AEP puede realizar los siguientes pasos.

1. Seleccione **[!UICONTROL Roles]** en el panel de navegación izquierdo y seleccione **[!UICONTROL Crear rol]**.

1. En el cuadro de diálogo _[!UICONTROL Crear nuevo rol]_, escriba un nombre para el rol, como _Especialistas en marketing B2B_, y una descripción (opcional).

1. Haga clic en **[!UICONTROL Confirmar]**.

1. Seleccione las zonas protegidas.

   ![Experience Platform - agregar zonas protegidas para el nuevo rol](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Añada los permisos de perfil:

   * En la lista _[!UICONTROL Recursos]_ de la izquierda, busque el elemento **[!UICONTROL Administración de perfiles]** y haga clic en el icono _Agregar_ (**+**) para agregar el atributo.

   * Para el atributo, agregue los siguientes permisos:
      * [!UICONTROL Ver segmentos]
      * [!UICONTROL Administrar segmentos]
      * [!UICONTROL Ver perfiles]
      * [!UICONTROL Administrar perfiles]
      * [!UICONTROL Ver perfil B2B]
      * [!UICONTROL Administrar perfil B2B]

   ![Experience Platform - agregar perfiles para el nuevo rol](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Añadir permisos de productos B2B:

   Consulte la lista de [permisos de producto B2B](#b2b-product-permissions) para determinar qué capacidades de producto desea para la función.

   En la lista _[!UICONTROL Recursos]_ de la izquierda, busque los elementos **[!UICONTROL B2B]** y haga clic en el icono _Agregar_ (**+**) para agregar cada atributo que desee habilitar para el rol.

   Puede introducir _B2B_ en la herramienta de búsqueda para filtrar la lista de permisos de productos B2B.

1. Haga clic en **[!UICONTROL Guardar]** en la parte superior derecha.

1. Vaya a los detalles de la función y seleccione la pestaña **[!UICONTROL Grupos de usuarios]**.

1. Haga clic en **[!UICONTROL Agregar grupos]**.

   ![Experience Platform - agregar perfiles para el nuevo rol](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Seleccione la casilla de verificación situada junto al grupo de usuarios que creó anteriormente en Admin Console.

1. Haga clic en **[!UICONTROL Guardar]**.
