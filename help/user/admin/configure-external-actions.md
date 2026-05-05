---
title: Configuración de acciones externas
description: Descubra cómo los desarrolladores, administradores y especialistas en marketing trabajan juntos para implementar, configurar y utilizar acciones externas que conectan Journey Optimizer B2B edition con servicios externos en recorridos de cuenta.
feature: Setup, Integrations
role: Admin, Developer
exl-id: 226fbf23-7df2-4fd7-b5a4-2057a417a261
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 0216cf3b1cbc1124b50ad99e649778aef71f5aca
workflow-type: tm+mt
source-wordcount: 907
ht-degree: 1%

---

# Configuración de acciones externas

Las acciones externas permiten que los recorridos de cuenta de Journey Optimizer B2B edition se conecten con sistemas externos directamente desde el lienzo de recorrido. Cuando una audiencia de cuenta llega a un nodo de acción externa, el sistema realiza una llamada saliente asincrónica a un servicio externo configurado y pasa los datos de atributos de audiencia para cuentas, personas o ambos. El servicio externo procesa los datos y responde con una llamada de retorno, devolviendo datos de audiencia y metadatos que se pueden utilizar como guía para la ejecución del recorrido.

Esta función admite dos tipos de nodos de recorrido:

* **Acción externa**: llama a un servicio externo y continúa en una sola ruta de salida. Ideal para _activar y olvidar_ integraciones, como actualizar un registro CRM o activar una notificación descendente.
* **Rutas divididas externas**: llama a un servicio externo y evalúa la respuesta para enrutar cuentas a lo largo de una de varias rutas definidas.

>[!NOTE]
>
>Los servicios de acción externa solo se admiten para recorridos de cuenta. Estos tipos de nodo no están disponibles para los recorridos de persona.

## Resumen de implementación

La configuración de acciones externas requiere una coordinación entre tres funciones en secuencia:

| | Función | Tarea |
| ---- | ---- | ---- |
| 1 | Desarrollador | [Implementar y publicar el servicio externo](#implement-service) |
| 2 | Administrador | [Configurar la acción en Journey Optimizer B2B edition](#configure-action) |
| 3 | Experto en marketing | [Agregar un nodo externo a un recorrido de cuentas](#add-journey-node) |

## Implementación del servicio externo {#implement-service}

El desarrollador debe crear y publicar un servicio web público que cumpla con la [Interfaz de proveedor de servicios de acciones externas de Adobe Journey Optimizer B2B edition](https://developer.adobe.com/journey-optimizer-b2b-apis/).

>[!NOTE]
>
>La función de devolución de llamada requiere un token de portador. Recupere esto configurando [credenciales de servidor a servidor OAuth en Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation) para su organización IMS.

Una vez que el servicio esté activo, proporcione la URL de la especificación OpenAPI y las credenciales de autenticación al administrador del producto responsable de configurar la acción.

## Configurar la acción {#configure-action}

Se debe configurar y activar una acción antes de que los especialistas en marketing puedan utilizarla en un recorrido. Las acciones se crean en estado _Borrador_ y los cambios se guardan automáticamente. Permanece como borrador hasta que lo activa.

>[!PREREQUISITES]
>
>Obtenga la URL de la especificación OpenAPI y las credenciales de autenticación del desarrollador antes de añadir la configuración.
>
>Para definir y activar una acción externa, debe tener el _[!UICONTROL permiso de administración de configuraciones de B2B]_ [producto](./user-management.md#b2b-product-permissions).

1. Vaya a **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en **[!UICONTROL Acciones externas]** en el panel intermedio.

   ![Acceder al espacio de configuración de acciones externas](./assets/configuration-external-actions-list.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Crear acción]** en la parte superior derecha.

1. Escriba la dirección URL de la especificación OpenAPI para el servicio externo y haga clic en **[!UICONTROL Crear]**.

   ![Escriba la dirección URL del servicio](./assets/configuration-external-actions-create-url.png){width="500"}

   >[!NOTE]
   >
   >El servicio externo debe estar activo y accesible para que este paso se realice correctamente.

1. Cuando la dirección URL se resuelva correctamente, revise **[!UICONTROL Detalles del servicio]**.

   Los detalles del servicio se leen directamente desde la especificación OpenAPI cuando se crea la acción. Estas propiedades no se pueden cambiar en la configuración después de la creación.

   | Propiedad | Descripción | Propiedad de especificación OpenAPI |
   | -------- | ----------- | --------------------- |
   | [!UICONTROL Nombre] | Nombre de la acción | `info.title` |
   | [!UICONTROL Descripción] | Descripción de la acción | `info.description` |
   | [!UICONTROL Dirección URL] | URL de la especificación OpenAPI que define el servicio externo | `servers.url` |

1. Escriba las credenciales de **[!UICONTROL Authentication]** para el servicio externo (`components.securitySchemes`).

   >[!NOTE]
   >
   >Los campos de credenciales mostrados dependen del mecanismo de autenticación definido en el servicio externo. Los tipos compatibles son Clave de API, OAuth2 y Autenticación básica HTTP.

   ![Agregar las credenciales de autenticación](./assets/configuration-external-actions-auth-credentials.png){width="600" zoomable="yes"}

   Puede cambiar las credenciales según sea necesario cuando la acción configurada esté en estado _Borrador_ o _Activo_.

1. Haga clic en **[!UICONTROL Next]**.

1. Establezca las propiedades **[!UICONTROL Configurations]** para definir cómo la acción intercambia datos con el servicio externo.

   >[!NOTE]
   >
   >Las propiedades marcadas como _Estáticas_ no se pueden actualizar en el momento de la configuración y se basan en la definición del servicio.

   * **[!UICONTROL Tipo de acción]** (_Estática_): el tipo de nodo de recorrido admitido:

      * [!UICONTROL Acción externa] (`enableSplitPath` = false)
      * [!UICONTROL Ruta dividida de acción externa] (`enableSplitPath` = true)

     No se puede cambiar el tipo de acción después de crear la configuración de acción.

   * **[!UICONTROL Descriptores de acceso]** (_Estáticos_) - (Solo ruta de acceso dividida de acción externa) Las variables devueltas por el servicio externo para que estén disponibles como condiciones de ruta de acceso en un nodo de ruta de acceso dividida externa. (`invocationPayloadDef.accessorsMetadata`)

   * **[!UICONTROL Contexto de Recorrido]** (_Estático_): el ámbito de los datos de audiencia enviados en la solicitud (`supportedEntityType`):

      * [!UICONTROL Cuenta] - Envía solamente cuentas

      * [!UICONTROL Personas]: envía solamente personas

      * [!UICONTROL Personas en la cuenta]: envía cuentas y personas relacionadas con la cuenta

   * **[!UICONTROL Campos de salida]**: asigne cada campo de la tabla a un [campo XDM](../admin/xdm-field-management.md). Estos campos se envían en el cuerpo de la solicitud al servicio externo. Propiedades de definición de servicio: `invocationPayloadDef.accountFields`, `invocationPayloadDef.fields`.

   ![Asignar campos de salida de acción externa](./assets/configuration-external-actions-fields.png){width="600" zoomable="yes"}

   * **[!UICONTROL Campos entrantes]**: asigne cada campo de la tabla a un [campo XDM actualizable](../admin/xdm-field-management.md#updatable-fields). Estos campos se rellenan desde la respuesta del servicio externo. Propiedades de definición de servicio: `callbackPayloadDef.accountFields`, `callbackPayloadDef.fields`. Actualizable después de la creación.

   * **[!UICONTROL Parámetros de encabezado]**: escriba un valor para cada fila para pasarla como un encabezado HTTP en la solicitud. Propiedad de definición de servicio: `invocationPayloadDef.headers`.

   * **[!UICONTROL Tiempo de espera]**: escriba el número de minutos que esperar para que el servicio externo invoque la devolución de llamada antes de que la solicitud se considere errónea. Propiedad de definición de servicio: `timeout`.

   * **[!UICONTROL Atributos globales]**: escriba un valor para cada fila para incluirlo como campo estático en el cuerpo de la solicitud. Propiedad de definición de servicio: `invocationPayloadDef.globalAttributes`.

   ![Parámetros, tiempo de espera y atributos globales del encabezado de acción externa](./assets/configuration-external-actions-header-timeout-global.png){width="600" zoomable="yes"}

1. Haga clic en la _flecha hacia atrás_ para regresar a la lista y mantener la acción en estado _Borrador_.

   O haga clic en **[!UICONTROL Activar]** para cambiar la configuración de la acción al estado _Activo_. La acción externa configurada debe estar activa para que esté disponible para su uso en recorridos de cuenta.

## Añadir un nodo externo a un recorrido {#add-journey-node}

Una vez activada una acción, los especialistas en marketing pueden agregar un nodo _[!UICONTROL External action]_ o _[!UICONTROL External split path]_ a cualquier recorrido de cuenta. Para obtener información sobre cómo agregar y utilizar estos nodos en el lienzo de recorrido de la cuenta, consulte [Nodos externos](../journeys/external-nodes.md).
