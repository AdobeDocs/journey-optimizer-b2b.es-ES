---
title: '[!DNL Adobe Target] audiencias externas'
description: Activar audiencias externas a  [!DNL Adobe Target] mediante recorridos de cuenta. Personalice las experiencias web B2B y mantenga la coherencia entre plataformas.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# [!DNL Adobe Target] audiencias externas

Puede activar y personalizar experiencias para audiencias externas en [!DNL Adobe Target] mediante recorridos de cuenta. Utilice esta integración para lograr una personalización avanzada y adaptada que aumente la participación y para mantener la coherencia entre plataformas en [!DNL Target] y [!DNL Journey Optimizer B2B Edition]. Esta coherencia garantiza que los equipos alineen y personalicen los canales web para los grupos de compra en todo el recorrido de comprador B2B.

Se trata de un flujo de trabajo de dos pasos para activar una audiencia externa a través de Adobe Target:

1. [Agregar a la audiencia de cliente externa](#add-to-customer-external-audience-from-a-journey) desde un recorrido.
2. [Activar la audiencia externa](#activate-the-external-audience-to-target-as-a-destination) a [!DNL Target] como destino en Experience Platform.

## Añadir a la audiencia externa del cliente desde un recorrido

En su recorrido, [agregue un _Realice una acción_ nodo](../journeys/action-nodes.md) para ejecutar la acción _[!UICONTROL Agregar a la audiencia de cliente externa]_. Las acciones suelen ser lo que desea que ocurra como resultado de algún tipo de déclencheur, como un evento o una acción anterior. El recorrido ejecuta la acción cuando una cuenta correspondiente con perfiles de persona llega al nodo.

>[!NOTE]
>
>Cuando una cuenta correspondiente con perfiles de persona alcanza el nodo _Agregar a la audiencia de cliente externa_ en un recorrido publicado, esos perfiles pueden tardar hasta 48 horas en rellenarse en la audiencia externa.

1. Con el nodo _Realizar una acción_ seleccionado en el lienzo del recorrido, elige la opción _[!UICONTROL Acción en]_ **[!UICONTROL Personas]**.

1. Para _[!UICONTROL Acción sobre personas]_, elija **[!UICONTROL Agregar a la audiencia externa del cliente]**.

   ![nodo de Recorrido - realizar una acción con personas - agregar a la audiencia externa del cliente](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. En las propiedades del nodo a la derecha, establezca la audiencia externa.

   * Si ya se han creado una o más audiencias externas, puede elegir **[!UICONTROL Seleccionar audiencias existentes]** y [seleccionar la audiencia que desee usar](#choose-an-external-audience).

   * Si desea [crear una audiencia](#create-an-external-audience) para el nodo, elija **[!UICONTROL Crear nuevo]**.

### Creación de una audiencia externa

1. Después de elegir la opción **[!UICONTROL Crear nuevo]** en las propiedades del nodo, haga clic en **[!UICONTROL Crear audiencia de cliente externa]**.

   ![Realizar una acción con personas - agregar a audiencia de cliente externa - crear nueva opción](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** (obligatorio) y **[!UICONTROL Descripción]** (opcional) para la nueva audiencia.

   ![Cuadro de diálogo Crear audiencia de cliente externo](./assets/create-external-customer-audience-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

   El sistema crea la nueva audiencia y muestra un mensaje de confirmación. A continuación, puede utilizarla como audiencia existente para la acción del nodo.

### Selección de una audiencia externa

1. Después de elegir la opción **[!UICONTROL Seleccionar existente]** en las propiedades del nodo, haga clic en **[!UICONTROL Seleccionar audiencia de cliente externa]**.

   ![Realizar una acción con personas - agregar a audiencia de cliente externa - seleccionar opción existente](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. En el cuadro de diálogo _[!UICONTROL Agregar audiencia]_, seleccione la audiencia que desee usar.

   Puede escribir texto en el campo _Buscar_ para filtrar los elementos mostrados y buscar una coincidencia del nombre de la audiencia.

   ![Realizar una acción con personas - agregar a audiencia de cliente externa - agregar cuadro de diálogo de audiencia](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Agregar audiencia]**.

## Activar la audiencia externa para Target como destino

Para activar la audiencia externa en Adobe Target, es necesario que haya configurado [!DNL Adobe Target] como destino en [!DNL Real-time Customer Data Platform (RTCDP)]. Para obtener más información sobre esta configuración, consulte la [documentación de RTCDP](https://experienceleague.adobe.com/es/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}.

>[!IMPORTANT]
>
>El uso de la activación mediante un recorrido requiere que la implementación de RTCDP utilice ID de correo electrónico.

El proceso de activación requiere que agregue [!DNL Adobe Target] como audiencia externa o destino externo. Para empezar, cree una audiencia [!DNL Target] en el generador de audiencias. También puede crear una audiencia de marcador de posición y agregar la función de audiencia externa.

>[!BEGINSHADEBOX]

![Icono de permisos de AEP](../../assets/do-not-localize/icon_permissions-outline.svg): estos pasos requieren los siguientes permisos para la función de usuario asignada:

* **[!UICONTROL Experience Platform]** - Para el recurso _[!UICONTROL Destinos]_: `Activate Destinations`, `Manage and Activate Dataset Destination` y `View Destination`
* **[!DNL Target]** - `Approver`

>[!ENDSHADEBOX]

1. En Experience Platform, vaya a **[!UICONTROL Conexiones]** > **[!UICONTROL Destinos]** en el panel de navegación izquierdo.

1. Seleccione la pestaña **[!UICONTROL Examinar]**. 

1. Busque la conexión de destino que desee usar para activar los segmentos, haga clic en el icono de _menú Más_ ( **...** ) junto al nombre y elija **[!UICONTROL Activar audiencias]**.

   Escriba texto en el campo _[!UICONTROL Buscar]_ para filtrar los destinos mostrados para una coincidencia por nombre.

   ![Experience Platform - destinos - examinar destinos de Target - menú más](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. En la lista _[!UICONTROL Audiencias disponibles]_, seleccione su audiencia externa y haga clic en **[!UICONTROL Siguiente]**.

   ![Experience Platform - destinos - examinar destinos de Target - menú más](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. Realice cualquier asignación de campo adicional al destino (opcional) y haga clic en **[!UICONTROL Siguiente]**.

1. Revise los nuevos parámetros de audiencia y haga clic en **[!UICONTROL Finalizar]**.

   ![Experience Platform - destinos - activar destino - revisar](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

Tras la activación, podrá ver la audiencia en [audiencias de Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"} y usarlas en actividades de Adobe Target.

