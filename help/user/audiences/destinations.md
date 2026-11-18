---
title: Destinos
description: Obtenga información acerca de los destinos de Experience Platform admitidos y cómo conectar un destino para activar listas de personas estáticas en Journey Optimizer B2B Edition.
feature: Audiences, Integrations
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 4%
---

# Destinos

Los destinos son integraciones prediseñadas que le permiten enviar [listas estáticas de personas](./people-lists-static.md) miembros y audiencias de recorrido de cuentas a las plataformas sociales. Al activar una lista estática en un destino, la suscripción se mantiene sincronizada. A medida que se añaden personas a la lista o se eliminan de ella, se añaden o eliminan también de la audiencia de destino y, por extensión, de cualquier campaña a la que se alimente la audiencia.

Existen tres formas de activar personas en un destino conectado:

* **De una lista estática**: active una lista estática existente directamente desde la ficha **_[!UICONTROL Listas de personas]_**. Ver [_Activar en un destino_](./people-lists-static.md#static-list-activate).
* **Desde un recorrido de cuentas**: agregue un nodo de acción **_[!UICONTROL Activar en destino]_** a una ruta de acceso de recorrido para que las cuentas que cumplan los requisitos se activen en el destino cuando lleguen a ese nodo. Ver [_Activar o desactivar de un destino_](../journeys/action-nodes.md#activate-deactivate-destination).
* **De un grupo de compras**: para llenar roles vacíos en tus grupos de compras, puedes activar una audiencia coincidente de LinkedIn para segmentar clientes potenciales que coincidan con los parámetros de tu grupo de compras. Ver [_LinkedIn Cuenta con audience_s](../data/linkedin-account-matched-audiences.md#activate-buying-group) coincidentes.

>[!BEGINSHADEBOX]

## Permisos necesarios {#required-permissions}

La funcionalidad de destino completa requiere los siguientes [!DNL Adobe Experience Platform] permisos.

| Categoría | Permiso |
|--- |--- |--- |
| Zonas protegidas | Acceso a zona protegida |
| Paneles de control | Ver paneles estándar |
| Paneles de control | Administrar paneles estándar |
| Destinos | Ver destinos |
| Destinos | Administrar destinos |
| Destinos | Activar destinos |
| Destinos | Activar segmento sin asignación |
| Destinos | Administrar y activar el destino del conjunto de datos |
| Destinos | Creación de destino |
| Gobernanza de datos | Ver directivas de uso de datos |
| Gobernanza de datos | Administrar políticas de uso de datos |
| Ingesta de datos | Ver orígenes |
| Ingesta de datos | Administrar fuentes |
| Administración de perfiles | Ver configuración del perfil |
| Administración de perfiles | Administrar configuración de perfil |

>[!ENDSHADEBOX]

## Destinos admitidos {#supported-destinations}

Para poder activar una lista estática, debe existir un destino en el catálogo de destinos. En el panel de navegación izquierdo, expanda **[!UICONTROL Conexiones]** y seleccione **[!UICONTROL Destinos]**. [!DNL Journey Optimizer B2B Edition] admite actualmente el destino **[!UICONTROL Audiencia coincidente de LinkedIn]** (Social). Ver [_audiencias coincidentes con la cuenta de LinkedIn_](../data/linkedin-account-matched-audiences.md) para

<!-- 
the following destinations:

* **[!UICONTROL Google Customer Match]** (Advertising)
* **[!UICONTROL Facebook Custom Audience]** (Social)
* **[!UICONTROL LinkedIn Matched Audience]** (Social)

![Access the available connector types](./assets/destinations-catalog.png){width="800" zoomable="yes"}

-->

>[!NOTE]
>
>El catálogo mostrado no es el catálogo de destinos completo de [!DNL Adobe Experience Platform]. Si accede a destinos directamente desde [!DNL Experience Platform], verá un catálogo más grande, pero solo estos destinos están disponibles actualmente para su activación en [!DNL Journey Optimizer B2B Edition]. Hay destinos adicionales planificados para futuras versiones.

## Configurar un destino {#set-up-destination}

Cada tarjeta de destino admitida muestra **[!UICONTROL Configurar nuevo destino]**. La configuración de un destino es un requisito previo para la activación.

1. En la tarjeta del conector, haga clic en **[!UICONTROL Configurar nuevo destino]**.

   ![Configurar un nuevo destino](./assets/destinations-configure-new.png){width="500"}

1. Seleccione **[!UICONTROL Cuenta existente]** o **[!UICONTROL Cuenta nueva]** e introduzca los detalles de la cuenta, como el nombre y la descripción de la cuenta.

1. Haga clic en **[!UICONTROL Conectar con destino]**.

   Un flujo de OAuth le permite iniciar sesión en la cuenta correspondiente: LinkedIn, Google o Facebook.

   >[!IMPORTANT]
   >
   >En este punto, no ingrese los _[!UICONTROL detalles de destino]_. Solo se necesita la conexión.

1. Complete cualquier asignación de campo requerida entre los atributos de las personas y los campos requeridos por el destino.

1. Revise la configuración del control de datos y la acción de marketing y, a continuación, haga clic en **[!UICONTROL Guardar]**.

Para ver los pasos completos de la configuración, consulte [Crear una nueva conexión de destino](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} en la documentación de [!DNL Experience Platform].

Cuando está configurado, el destino está disponible para la activación en todas partes donde se puede seleccionar un destino en [!DNL Journey Optimizer B2B Edition].

## Activación y sincronización {#activation-sync}

La activación se basa en la pertenencia a listas estáticas, con una sincronización bidireccional entre la lista y la audiencia de destino:

* Añadir una persona a la lista estática la activa en el destino en un plazo de 24 horas, añadiéndola a la audiencia de destino y, posteriormente, a cualquier campaña que alimente la audiencia.
* Al eliminar a una persona de la lista estática, se desactiva del destino. Se eliminan de la audiencia de destino y de cualquier campaña conectada.
* La misma lista se puede activar en varios destinos a la vez. La pertenencia se sincroniza con todos ellos.

>[!TIP]
>
>Para ejecutar una campaña de LinkedIn en un segmento, active la lista estática de esas personas en el destino de audiencia coincidente de LinkedIn. Todas las personas de la lista se añaden a la audiencia coincidente de LinkedIn, donde una campaña puede dirigirlos y la audiencia se mantiene actualizada automáticamente a medida que cambia la lista.
