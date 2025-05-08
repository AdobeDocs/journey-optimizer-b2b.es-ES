---
title: Públicos de la cuenta
description: Obtenga información acerca de las audiencias de cuenta y cómo habilitan los recorridos basados en cuentas.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 100%

---

# Públicos de la cuenta

Una audiencia es un conjunto de personas que comparten comportamientos o características similares. Journey Optimizer B2B Edition utiliza las funcionalidades de segmentación de cuentas que se encuentran en las ediciones B2B y B2P de Adobe Real-Time Customer Data Platform. Con la segmentación de cuentas, los usuarios pueden generar audiencias de cuenta aprovechando los datos de cualquiera de las entidades B2B del sistema. Estas audiencias de cuenta sirven como entradas para los recorridos de cuenta de Journey Optimizer B2B Edition, lo que facilita la activación y personalización sin problemas.

Obtenga más información acerca de las audiencias de cuenta y cómo definirlas en la [documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.

## Flujo de trabajo de público de la cuenta

Puede considerar Journey Optimizer B2B Edition como un destino de Experience Platform (AEP) que no aparece en el catálogo de destinos. Active las audiencias de cuenta en Journey Optimizer B2B Edition siguiendo estos pasos:

1. Cree esquemas para los datos en AEP.
1. Introduzca sus datos en AEP.
1. Cree un segmento de cuenta para evaluar los datos.
1. Active los datos evaluados en Journey Optimizer B2B Edition.

En Journey Optimizer B2B Edition, las audiencias de cuenta se utilizan como entrada para recorridos basados en cuentas, lo que permite dirigirse a las personas dentro de esas cuentas. Por ejemplo, puede utilizar las audiencias de cuenta para recuperar registros de todas las cuentas que no tengan información de contacto de cualquier persona con el título de Director de operaciones (COO) o Director de marketing (CMO).

Journey Optimizer B2B Edition le permite crear audiencias de cuenta de Adobe Experience Platform (AEP) directamente desde el panel de navegación izquierdo e incorporarlas a los recorridos de la cuenta.

![Acceder a las audiencias de la cuenta](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Crear un público de cuenta

Defina el público de cuenta creando una segmentación de cuentas. Tiene la opción de crear la segmentación de cuentas directamente en la aplicación de Journey Optimizer B2B Edition o puede usar la [IU del generador de segmentos](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/segment-builder){target="_blank"}. A continuación, se indican los pasos que puede seguir para crear una segmentación de cuentas en Journey Optimizer B2B Edition.

1. En el panel de navegación izquierdo, elija **[!UICONTROL Cuentas]** > **[!UICONTROL Audiencias]**.

1. Haga clic en **[!UICONTROL Crear audiencia]** en la parte superior derecha.

1. Genere la definición del segmento.

   Los atributos y audiencias de la cuenta se muestran en la barra de navegación izquierda. En la pestaña _[!UICONTROL Atributos]_, puede añadir atributos creados y personalizados por Platform. Arrastre cada atributo para crear la lógica del segmento.

   >[!TIP]
   >
   >Al crear una audiencia de cuenta, tenga en cuenta que los eventos se incluyen en _[!UICONTROL Personas]_, ya que estos atributos están asociados a personas.<br/>
   >
   >En la pestaña _[!UICONTROL Audiencias]_, puede añadir audiencias basadas en personas creadas anteriormente sobre las que basarse al crear su propia audiencia de cuenta.

   En el siguiente ejemplo se define la audiencia creada con `Country Code`, `Revenue Amount` y `Market segment`. La consulta en inglés sería: “Quiero todas las cuentas en los Estados Unidos que estén en el segmento Finanzas cuyos ingresos superen 1 millón de dólares”.

   ![ejemplo del generador de segmentos de audiencia de cuenta](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >El atributo `Account Name` de los registros de cuenta debe contener un valor que se va a incluir en los recorridos de cuenta. Si este atributo está vacío (nulo), se excluirá el registro de cuenta.<br/>
   >Para asegurarse de que solo se incluyen las cuentas con un nombre de cuenta que no esté vacío, añada el atributo **[!UICONTROL Account Name]** y seleccione _[!UICONTROL exists]_ como condición de coincidencia.<br/>
   >![El atributo Nombre de cuenta existe](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>Si está usando un atributo personalizado para el nombre de cuenta, use su nombre de atributo personalizado en lugar de _[!UICONTROL Nombre de cuenta]_.

1. Haga clic en **[!UICONTROL Guardar y cerrar]** en la parte superior derecha.

Para activar la audiencia de su cuenta para Journey Optimizer B2B Edition, debe [añadirla a un recorrido de cuenta](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) y [publicar el recorrido](../journeys/journey-overview.md).
