---
title: Destinos
description: Obtenga información sobre cómo conectar destinos y activar listas de personas estáticas en Journey Optimizer B2B Prime para exportar datos de audiencia a plataformas de publicidad, correo electrónico y otras plataformas de marketing.
autotag-review: '2026-06-17T18:30:02.442Z'
TQID: 'https://experienceleague.adobe.com/xO1p-VvIfv1KB77g0l2-fFRHQ0w2hy97vnG1QHpMw8c'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: af10a912422f1736fdc86e0609aee76f5d4daa46
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 2%

---

# Destinos

Los destinos son integraciones prediseñadas que le permiten exportar datos de listas de personas de [!DNL Adobe Journey Optimizer B2B Prime] a plataformas de marketing externas, como redes de publicidad, proveedores de servicios de correo electrónico y sistemas CRM. En [!DNL Journey Optimizer B2B Prime], activa [listas de personas estáticas](./people-lists.md#static-list) (compuestas de registros de personas de Marketo Engage) en destinos para que esas audiencias estén disponibles para la segmentación y la participación en canales descendentes.

<!-- 
Does not align w/AEP info for Beta

Activating a static list to a destination follows a three-step process:

1. **Connect** — Authenticate and configure a connection to a destination platform.
1. **Map** — Select the static list and map its people attributes to the fields required by the destination.
1. **Schedule** — Define when and how often the list data is exported to the destination.

Destination activations reflect the membership state of the static list at the time of each synch.

## Destination types {#destination-types}

[!DNL Journey Optimizer B2B Prime] supports the following destination types for activating static people lists:

| Type | Description |
|--- |--- |
| Streaming | Real-time API-based connections that push audience membership updates to the destination as they occur. |
| File-based (batch) | Scheduled exports that deliver audience data as structured files to cloud storage or SFTP locations, which the destination platform then ingests. |

-->

## Conectar un destino {#connect-destination}

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Conexiones]** y seleccione **[!UICONTROL Destinos]**.

1. En la ficha _[!UICONTROL Catálogo]_, busque el conector de tipo de destino externo.

   >[!TIP]
   >
   >Puede encontrar rápidamente el conector si escribe el nombre, como `LinkedIn`, en el cuadro de búsqueda.

   ![Acceder a los tipos de conectores disponibles](./assets/destinations-catalog.png){width="800" zoomable="yes"}

1. En la tarjeta del conector, haga clic en **[!UICONTROL Configurar nuevo destino]**.

1. Seleccione **[!UICONTROL Nueva cuenta]** e introduzca las credenciales de su cuenta.

   ![Conectar una nueva cuenta de destino](./assets/destinations-configure-new.png){width="500"}

1. Haga clic en **[!UICONTROL Conectar con destino]**.

   >[!IMPORTANT]
   >
   >En este momento, **no** escribe los _[!UICONTROL detalles del destino]_. Solo se necesita la conexión.

1. Revise la configuración del control de datos y la acción de marketing y, a continuación, haga clic en **[!UICONTROL Guardar]**.

El destino conectado aparece en la lista de la ficha _[!UICONTROL Examinar]_ y está disponible para la activación de listas estáticas.

## Activar una lista estática en un destino {#activate}

>[!NOTE]
>
>Solo se pueden activar [listas de personas estáticas](./people-lists.md#static-list) en los destinos de [!DNL Journey Optimizer B2B Prime]. [Las listas dinámicas](./people-lists.md#dynamic-lists) no cumplen los requisitos para la activación de destino.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración de mercadotecnia]**.

1. A la derecha de la lista de recursos de **[!UICONTROL Marketing]**, seleccione **[!UICONTROL Listas de personas]**.

   ![Acceder a listas de personas para administrar tus audiencias](./assets/people-lists.png){width="800" zoomable="yes"}

1. Seleccione la ficha **[!UICONTROL Listas estáticas]**.

1. Busque la lista estática que desea activar en un destino.

1. Haga clic en el icono _Activar_ ( ![Activar icono](../../assets/do-not-localize/icon-falco-activate-dest.svg) ) junto al nombre de la lista estática.

1. Seleccione la casilla de verificación de la conexión de destino configurada.

   ![Destinos configurados disponibles para la activación](./assets/static-list-activate-destination-select.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.

<!--

This method not working for Beta

1. On the _[!UICONTROL Browse]_ tab, locate the destination you want to use for the activation and click the name to open it.

1. Select the **[!UICONTROL Activation data]** tab.

1. Click **[!UICONTROL Activate people lists]**.

1. Select the static people list you want to export and click **[!UICONTROL Next]**.

1. Map the people list attributes to the required fields of the destination schema and click **[!UICONTROL Next]**.

1. Set the export schedule:

   * **[!UICONTROL Frequency]** — Choose how often the list is exported (for example, daily or weekly).
   * **[!UICONTROL Start date]** — Set when the first export should run.

1. Review the activation summary and click **[!UICONTROL Finish]**.

The activation is created and the static list data is exported to the destination according to the defined schedule.

-->
