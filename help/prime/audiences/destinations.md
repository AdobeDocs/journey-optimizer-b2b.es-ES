---
title: Destinos
description: Obtenga información acerca de los permisos necesarios, los destinos admitidos y cómo conectar un destino en Journey Optimizer B2B Prime para activar listas de personas estáticas en plataformas publicitarias y sociales.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-17T18:30:02.442Z'
TQID: 'https://experienceleague.adobe.com/xO1p-VvIfv1KB77g0l2-fFRHQ0w2hy97vnG1QHpMw8c'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 7a954ba7ade748d5d51cae82a0cddb64449fa2a2
workflow-type: tm+mt
source-wordcount: 655
ht-degree: 8%

---

# Destinos

Los destinos son integraciones prediseñadas que le permiten enviar [listas de personas estáticas](./people-lists.md#static-lists) desde [!DNL Journey Optimizer B2B Prime] a publicidad externa o plataformas sociales, como una audiencia de campaña de LinkedIn, una audiencia de Customer Match de Google o una audiencia personalizada de Facebook. La activación de una lista estática en un destino mantiene la pertenencia sincronizada: a medida que se añaden personas a la lista o se eliminan de ella, estas se añaden o eliminan en consecuencia de la audiencia de destino y, por extensión, de cualquier campaña a la que la audiencia alimente.

Existen dos formas de activar personas en un destino conectado:

* **De una lista estática**: active una lista estática existente directamente desde la ficha **_[!UICONTROL Listas de personas]_**. Ver [Activar en un destino](./people-lists.md#static-list-activate).
* **De un recorrido de persona**: agregue una acción **_[!UICONTROL Activar en destino]_** a una ruta de acceso de recorrido para que cualquier persona que llegue a ese nodo se agregue a una lista y se envíe al destino. Consulte [_Agregar un nodo de acción_](../marketing/action-nodes.md#add-an-action-node).

>[!BEGINSHADEBOX]

## Permisos necesarios {#required-permissions}

La funcionalidad de destino completa requiere que se habiliten los siguientes [!DNL Adobe Experience Platform] permisos.

| Categoría | Permiso | Obligatorio |
|--- |--- |--- |
| Zonas protegidas | Acceso a zona protegida _(habilitado de forma predeterminada)_ | Sí |
| Paneles de control | Ver paneles estándar | Sí |
| Paneles de control | Administrar paneles estándar | Sí |
| Destinos | Ver destinos | Sí |
| Destinos | Administrar destinos | Sí |
| Destinos | Activar destinos | Sí |
| Destinos | Activar segmento sin asignación | Sí |
| Destinos | Administrar y activar el destino del conjunto de datos | Sí |
| Destinos | Creación de destino | Sí |
| Gobernanza de datos | Ver directivas de uso de datos | Sí |
| Gobernanza de datos | Administrar políticas de uso de datos | Sí |
| Ingesta de datos | Ver orígenes | Sí |
| Ingesta de datos | Administrar fuentes | Sí |
| Administración de perfiles | Ver configuración del perfil | Sí |
| Administración de perfiles | Administrar configuración de perfil | Sí |

>[!ENDSHADEBOX]

## Destinos admitidos {#supported-destinations}

Para poder activar una lista estática, debe existir un destino en el catálogo de destinos. En el panel de navegación izquierdo, expanda **[!UICONTROL Conexiones]** y seleccione **[!UICONTROL Destinos]**. [!DNL Journey Optimizer B2B Prime] admite actualmente los siguientes destinos:

* **[!UICONTROL Coincidencia de clientes de Google]** (Advertising)
* **[!UICONTROL Audiencia personalizada de Facebook]** (Social)
* **[!UICONTROL Audiencia coincidente de LinkedIn]** (Social)

![Acceder a los tipos de conectores disponibles](./assets/destinations-catalog.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Este catálogo no es el catálogo de destinos completo de [!DNL Adobe Experience Platform]. Si accede a destinos directamente desde [!DNL Experience Platform], verá un catálogo más grande, pero solo estos destinos están disponibles actualmente para su activación en [!DNL Journey Optimizer B2B Prime]. Hay destinos adicionales planificados para futuras versiones.

## Configuración de un destino {#set-up-destination}

Cada tarjeta de destino admitida muestra **[!UICONTROL Configurar nuevo destino]**. La configuración de un destino es un requisito previo para la activación.

1. En la tarjeta del conector, haga clic en **[!UICONTROL Configurar nuevo destino]**.

1. Seleccione **[!UICONTROL Cuenta existente]** o **[!UICONTROL Cuenta nueva]** e introduzca los detalles de la cuenta, como el nombre y la descripción de la cuenta.

   ![Conectar una nueva cuenta de destino](./assets/destinations-configure-new.png){width="500"}

1. Haga clic en **[!UICONTROL Conectar con destino]**.

   Un flujo de OAuth le permite iniciar sesión en la cuenta correspondiente: LinkedIn, Google o Facebook.

   >[!IMPORTANT]
   >
   >En este momento, **no** escribe los _[!UICONTROL detalles del destino]_. Solo se necesita la conexión.

1. Complete cualquier asignación de campo requerida entre los atributos de las personas y los campos requeridos por el destino.

1. Revise la configuración del control de datos y la acción de marketing y, a continuación, haga clic en **[!UICONTROL Guardar]**.

Para ver los pasos completos de la configuración, consulte [Crear una nueva conexión de destino](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} en la documentación de [!DNL Experience Platform].

Cuando está configurado, el destino está disponible para la activación en todas partes donde se puede seleccionar un destino en [!DNL Journey Optimizer B2B Prime].

## Activación y sincronización {#activation-sync}

La activación se basa en la pertenencia a listas estáticas, con una sincronización bidireccional entre la lista y la audiencia de destino:

* Añadir una persona a la lista estática la activa en el destino en un plazo de 24 horas, añadiéndola a la audiencia de destino y, posteriormente, a cualquier campaña que alimente la audiencia.
* Al eliminar a una persona de la lista estática, se desactiva del destino (se elimina de la audiencia de destino y de cualquier campaña conectada).
* La misma lista se puede activar en varios destinos a la vez; la pertenencia se sincroniza con todos ellos.

>[!TIP]
>
>Para ejecutar una campaña de LinkedIn en un segmento, active la lista estática de esas personas en el destino de audiencia coincidente de LinkedIn. Todas las personas de la lista se añaden a la audiencia coincidente de LinkedIn, donde una campaña puede dirigirlos y la audiencia se mantiene actualizada automáticamente a medida que cambia la lista.
