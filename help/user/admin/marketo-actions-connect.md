---
title: Activar Marketo Engage para admitir acciones de Recorrido
description: Active las conexiones de Marketo Engage para admitir acciones de recorrido y que los especialistas en marketing puedan coordinar campañas entre Marketo Engage y Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---


# Activar instancias de Marketo Engage para admitir acciones

Las acciones de Marketo Engage son acciones _basadas en personas_ que le permiten coordinar su orquestación de marketing _basada en cuentas_ entre Journey Optimizer B2B edition y sus esfuerzos de marketing _basados en clientes potenciales_ en Marketo Engage. Utilice estas acciones para organizar la pertenencia a listas estáticas y colocar a las personas en campañas.

Para usar acciones de Marketo Engage, un administrador primero crea un [servicio personalizado](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#) en Marketo Engage, que proporciona las credenciales necesarias para la autenticación.
A continuación, un administrador de productos para Journey Optimizer B2B edition crea una conexión con Marketo Engage introduciendo las credenciales.
Los usuarios de Journey Optimizer B2B edition pueden hacer referencia a la conexión para configurar acciones de Marketo Engage en <!-- Person and -->recorridos de cuenta, como agregar o quitar personas de listas de Marketo Engage o agregarlas a campañas de solicitud.

La visibilidad del espacio de trabajo de Marketo Engage para los recursos, como listas y campañas, se rige por los permisos de función asignados en el servicio personalizado.

La misma conexión se puede utilizar varias veces dentro de un recorrido, y diferentes conexiones de Marketo Engage pueden coexistir en un solo recorrido.

Cuando se ejecuta una acción, utiliza la directiva de selección para determinar qué registros de persona en Marketo Engage se seleccionarán si existen varios identificadores en el perfil de persona unificado. Las opciones incluyen elegir los registros de Marketo Engage más antiguos, más recientes o todos los que coincidan. Las personas pasan por el recorrido independientemente de la coincidencia, excepto cuando se produce un error.

## Configuración de una conexión de Marketo Engage

Configuración de una instancia remota de Marketo Engage para su uso con acciones del recorrido de Marketo Engage.

### Creación del servicio personalizado de Marketo Engage

1. Inicie sesión en Marketo Engage como administrador y cree un servicio personalizado.
1. Registre los siguientes valores para utilizarlos para la conexión:

   * Identificación de Munchkin
   * Identificación del cliente
   * Secreto de cliente

### Añadir la integración

![Agregar detalles de integración](assets/integration-connection-details.png)

1. En Journey Optimizer B2B edition, vaya a **Administración** > **Configuraciones**.
1. Seleccione la ficha **Integraciones**.
1. Haga clic en **[!UICONTROL Crear una conexión]**.
1. Introduzca un nombre (obligatorio) y una descripción (opcional).
1. Seleccione una **política de selección** para los registros de persona coincidentes.
1. Introduzca su Munchkin ID, ID de cliente y Secreto de cliente.
1. Haga clic en **[!UICONTROL Conectarse a Marketo]**.
1. Haga clic en **[!UICONTROL Crear]**.

Cuando un especialista en marketing utiliza una acción de Marketo Engage en un recorrido, puede configurar el nodo con el nombre de la conexión.

Con la integración completada, las acciones de Marketo Engage están disponibles en **Acciones en:** en las propiedades del nodo.

![lista de acciones de Marketo](assets/marketo-actions-list.png)