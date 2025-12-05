---
title: Activar Marketo Engage para admitir acciones de Recorrido
description: Active las conexiones de Marketo Engage para admitir acciones de recorrido y que los especialistas en marketing puedan coordinar campañas entre Marketo Engage y Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---


# Activar instancias de Marketo Engage para admitir acciones

Las acciones de Marketo Engage son acciones _basadas en personas_ que le permiten coordinar su orquestación de marketing _basada en cuentas_ entre Journey Optimizer B2B edition y sus esfuerzos de marketing _basados en clientes potenciales_ en Marketo Engage. Utilice estas acciones para organizar la pertenencia a listas estáticas y colocar a las personas en campañas.

Para usar acciones de recorrido de Marketo Engage, un administrador crea primero un [servicio personalizado](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} en Marketo Engage, que proporciona las credenciales necesarias para la autenticación. A continuación, un administrador de productos de Journey Optimizer B2B edition usa las credenciales para crear una conexión con Marketo Engage. Los usuarios de Journey Optimizer B2B edition pueden hacer referencia a la conexión para configurar acciones de Marketo Engage en <!-- person and -->recorridos de cuenta, como agregar o quitar personas de listas de Marketo Engage o agregarlas a campañas de solicitud.

## Configuración de una conexión de Marketo Engage {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Conexiones Marketo Engage externas"
>abstract="Los administradores de productos pueden configurar conexiones a instancias de Marketo Engage externas, lo que las hace disponibles para acciones de recorrido."

Complete las siguientes tareas para configurar una instancia de Marketo Engage externa y utilizarla con las acciones del recorrido.

### Creación del servicio personalizado de Marketo Engage

1. Inicie sesión en Marketo Engage como administrador y [cree un servicio personalizado](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Copie los siguientes valores para usarlos para la conexión de Journey Optimizer B2B edition:

   * Identificación de Munchkin
   * Identificación del cliente
   * Secreto de cliente

La visibilidad del espacio de trabajo de Marketo Engage para los recursos, como listas y campañas, se rige por los [permisos de función asignados en el servicio personalizado](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}. Los especialistas en marketing pueden utilizar la misma conexión varias veces dentro de un recorrido y utilizar diferentes conexiones de Marketo Engage dentro del mismo recorrido.

### Añadir la integración

![Agregar detalles de integración](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. En Journey Optimizer B2B edition, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.
1. Seleccione la ficha **[!UICONTROL Integraciones]**.
1. Haga clic en **[!UICONTROL Crear una conexión]**.
1. Escriba **[!UICONTROL Nombre]** (obligatorio) y **[!UICONTROL Descripción]** (opcional).
1. Seleccione la directiva de actualización que se utiliza para aplicar una acción a un registro de persona coincidente.

   Cuando se ejecuta una acción para la instancia de Marketo Engage conectada, la _directiva de actualización_ seleccionada determina los registros de persona en Marketo Engage para seleccionar si existen varios identificadores en el perfil de persona unificado.

   * **[!UICONTROL Actualizar todos los registros coincidentes]**
   * **[!UICONTROL Actualizar solo el registro coincidente más antiguo]**
   * **[!UICONTROL Actualizar solo el registro coincidente más reciente]**

   >[!NOTE]
   >
   >Las personas pasan por el recorrido independientemente de la coincidencia, excepto cuando se produce un error.

1. Introduzca el Munchkin ID, el ID de cliente y el secreto de cliente para el servicio creado en la instancia externa de Marketo Engage.
1. Haga clic en **[!UICONTROL Conectarse a Marketo]**.
1. Haga clic en **[!UICONTROL Crear]**.

## Usar la conexión en una acción de recorrido

Cuando un especialista en marketing utiliza una acción de Marketo Engage en un recorrido, puede configurar el nodo con el nombre de la conexión.

Con la integración completada, las acciones de Marketo Engage están disponibles en **Acciones en:** en las propiedades del nodo.

![lista de acciones de Marketo](assets/marketo-actions-list.png){width="800" zoomable="yes"}