---
title: Nodos de audiencia de cuenta
description: Configure nodos de audiencia de cuenta con audiencias de cuenta o listas de cuentas para definir puntos de entrada de recorrido para la orquestación de destino en Journey Optimizer B2B edition.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 2a676f3cbeb43616a75fa3fa6eb9106230b9fb40
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Nodos del recorrido de audiencia de cuenta

El nodo de audiencia de cuenta especifica qué cuentas entran en el recorrido. Cuando [crea un recorrido de cuenta](./create-publish-journey.md#create-a-journey), el recorrido siempre comienza con un nodo de audiencia de cuenta que define su entrada.

Utilice una de las siguientes opciones de entrada para este nodo de recorrido:

* **[Audiencia de la cuenta](../audiences/account-audience-overview.md)**: la audiencia de la cuenta representa la audiencia básica que se sincroniza desde el servicio de segmentación de Experience Platform.
* **[Lista de cuentas](../accounts/account-lists.md)**: la lista de cuentas es una colección de cuentas con nombre que utiliza para la orquestación de recorrido de destino. Una lista de cuentas se dirige a las cuentas con nombre utilizando criterios definidos, como el sector, la ubicación o el tamaño de la empresa.

## Establezca la audiencia para el nodo de audiencia de la cuenta

1. Haga clic en el nodo **[!UICONTROL Audiencia de la cuenta]**. Esta acción muestra las propiedades del nodo a la derecha.

   ![Nodo de recorrido de audiencia de cuenta](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Elija el tipo de entrada para las cuentas que introducen el recorrido:

   * **[!UICONTROL Audiencia de la cuenta]**

     Elija la opción de audiencia de la cuenta. A continuación, haga clic en **[!UICONTROL Agregar audiencia de cuenta]**.

     En el cuadro de diálogo _[!UICONTROL Agregar audiencia]_, seleccione un segmento de audiencia creado anteriormente. A continuación, haga clic en **[!UICONTROL Agregar audiencia]**.

     ![Seleccione un segmento de audiencia para el nodo](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Lista de cuentas]**

     Elija la opción de lista de cuentas. Haga clic en **[!UICONTROL Agregar lista de cuentas]**.

     En el cuadro de diálogo _[!UICONTROL Seleccionar lista de cuentas activas]_, seleccione una lista de cuentas publicadas. A continuación, haga clic en **[!UICONTROL Guardar]**.

     ![Seleccione una lista de cuentas activas para el nodo](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Para obtener más información acerca de cómo crear y publicar listas de cuentas, vea [Listas de cuentas](../accounts/account-lists.md).

## Crear un segmento de audiencia

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Cuentas]** > **[!UICONTROL Audiencias]**.

1. Haga clic en **[!UICONTROL Crear audiencia]** en la esquina superior derecha.

   ![Crear un segmento de audiencia](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Siga los pasos de la [guía del servicio de segmentación](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.
