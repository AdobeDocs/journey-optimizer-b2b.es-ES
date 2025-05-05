---
title: Nodos de audiencia de cuenta
description: Obtenga información acerca del tipo de nodo de audiencia de cuenta que puede utilizar para definir la entrada de los recorridos de la cuenta en Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 5ed7e58b7a069c8b436d0d2f7b338072259768be
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# Nodos del recorrido de audiencia de cuenta

El nodo Audiencia de cuenta define las cuentas de entrada para el recorrido. Cuando [crea un recorrido de cuenta](./journey-overview.md#create-an-account-journey), siempre comienza con un nodo _Audiencia de cuenta_ que define la entrada para el recorrido.

Existen dos tipos de entrada que puede utilizar para este nodo:

* **[Audiencia de cuenta](../audiences/account-audience-overview.md)**: Esta es la audiencia básica que se sincroniza desde el servicio de segmentación de Experience Platform.
* **[Lista de cuentas](../accounts/account-lists.md)**: se trata de una colección de cuentas con nombre que puede utilizar para la orquestación de recorrido de destino. Una lista de cuentas se dirige a las cuentas con nombre según los criterios definidos, como el sector, la ubicación o el tamaño de la compañía.

_Para establecer la audiencia del nodo:_

1. Haga clic en el nodo **[!UICONTROL Audiencia de la cuenta]** para mostrar las propiedades del nodo a la derecha.

   ![Nodo de audiencia de cuenta](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Elija el tipo de entrada para que las cuentas introduzcan el recorrido:

   * **[!UICONTROL Audiencia de la cuenta]**

     Elija este tipo y luego haga clic en **[!UICONTROL Agregar audiencia de cuenta]**.

     En el cuadro de diálogo _[!UICONTROL Agregar audiencia]_, seleccione un segmento de audiencia creado anteriormente y haga clic en **[!UICONTROL Agregar audiencia]**.

     ![Seleccione un segmento de audiencia para el nodo](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Lista de cuentas]**

     Elija este tipo y haga clic en **[!UICONTROL Agregar lista de cuentas]**.

     En el cuadro de diálogo _[!UICONTROL Seleccionar lista de cuentas activas]_, seleccione una lista de cuentas publicada anteriormente y haga clic en **[!UICONTROL Guardar]**.

     ![Seleccione una lista de cuentas activas para el nodo](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Vaya a [Listas de cuentas](../accounts/account-lists.md) para obtener información detallada sobre cómo crear y publicar listas de cuentas.

_Para crear un segmento de audiencia:_

1. En el panel de navegación izquierdo, elija **[!UICONTROL Cuentas]** > **[!UICONTROL Audiencias]**.

1. Haga clic en **[!UICONTROL Crear audiencia]** en la parte superior derecha.

   ![Crear un segmento de audiencia](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Siga los pasos descritos en la [guía del servicio de segmentación](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.
