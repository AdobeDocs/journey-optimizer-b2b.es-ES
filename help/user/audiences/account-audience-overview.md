---
title: Audiencias de cuenta
description: Obtenga información acerca de las audiencias de cuenta y cómo habilitan los recorridos basados en cuentas.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: b6b26d9cb79926577ed7fc4ed50c094986796505
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Públicos de la cuenta

Una audiencia es un conjunto de personas que comparten comportamientos o características similares. Journey Optimizer B2B edition utiliza las funcionalidades de segmentación de cuentas que se encuentran en las ediciones B2B y B2P de Adobe Real-Time Customer Data Platform. Con la segmentación de cuentas, los usuarios pueden generar audiencias de cuenta aprovechando los datos de cualquiera de las entidades B2B del sistema. Estas audiencias de cuenta sirven como entradas para los recorridos de cuenta de Journey Optimizer B2B edition, lo que facilita la activación y personalización sin problemas.

Obtenga más información acerca de las audiencias de cuenta y cómo definirlas en la [documentación del servicio de segmentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/types/account-audiences).

## Flujo de trabajo de audiencia de cuenta

Puede considerar Journey Optimizer B2B edition como un destino de Experience Platform (AEP) que no aparece en el catálogo de destinos. Active las audiencias de cuenta en Journey Optimizer B2B edition siguiendo estos pasos:

1. Cree esquemas para los datos en AEP.
1. Introduzca sus datos en AEP.
1. Cree un segmento de cuenta para evaluar los datos.
1. Active los datos evaluados en Journey Optimizer B2B edition.

En Journey Optimizer B2B edition, las audiencias de cuenta se utilizan como entrada para recorridos basados en cuentas, lo que permite dirigirse a las personas dentro de esas cuentas. Por ejemplo, puede utilizar las audiencias de cuenta para recuperar registros de todas las cuentas que no tengan información de contacto de cualquier persona con el título de Director de operaciones (COO) o Director de marketing (CMO).

Journey Optimizer B2B edition le permite crear audiencias de cuenta de Adobe Experience Platform (AEP) directamente desde el panel de navegación izquierdo e incorporarlas a los recorridos de la cuenta.

![Acceder a audiencias de cuenta](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Crear una audiencia de cuenta

Defina la audiencia de la cuenta creando una segmentación de cuentas. Tiene la opción de crear la segmentación de cuentas directamente en la aplicación de Journey Optimizer B2B edition o puede usar la [interfaz de usuario del generador de segmentos](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder). A continuación se indican los pasos que puede seguir para crear una segmentación de cuentas en Journey Optimizer B2B edition.

1. En el panel de navegación izquierdo, elija **[!UICONTROL Cuentas]** > **[!UICONTROL Audiencias]**.

1. Haga clic en **[!UICONTROL Crear audiencia]** en la parte superior derecha.

1. Genere la definición del segmento.

   Los atributos y audiencias de la cuenta se muestran en la barra de navegación izquierda. En la ficha _[!UICONTROL Atributos]_, puede agregar atributos creados y personalizados por Platform. Arrastre cada atributo para crear la lógica del segmento.

   >[!TIP]
   >
   >Al crear una audiencia de cuenta, tenga en cuenta que los eventos se enumeran en _[!UICONTROL Personas]_, ya que estos atributos están asociados a personas.<br/>
   >
   >En la ficha _[!UICONTROL Audiencias]_, puede agregar audiencias basadas en personas creadas anteriormente a partir de al crear su propia audiencia de cuenta.

   En el siguiente ejemplo se define la audiencia creada con `Country Code`, `Revenue Amount` y `Market segment`. La consulta en inglés sería: &quot;Quiero todas las cuentas en Estados Unidos que estén en el segmento Finanzas cuyos ingresos superen 1 millón de dólares&quot;.

   ![ejemplo del generador de segmentos de audiencia de cuenta](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >El atributo `Account Name` de los registros de cuenta debe contener un valor que se va a incluir en los recorridos de cuenta. Si este atributo está vacío (nulo), se excluirá el registro de cuenta.<br/>
   >Para asegurarse de que solo se incluyen las cuentas con un nombre de cuenta que no esté vacío, agregue el atributo **[!UICONTROL Account Name]** y seleccione _[!UICONTROL exists]_ como condición de coincidencia.<br/>
   >![El atributo Nombre de cuenta existe](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>Si está usando un atributo personalizado para el nombre de cuenta, use su nombre de atributo personalizado en lugar de _[!UICONTROL Nombre de cuenta]_.

1. Haga clic en **[!UICONTROL Guardar y cerrar]** en la parte superior derecha.

Para activar la audiencia de tu cuenta para Journey Optimizer B2B edition, debes [agregarla a un recorrido de cuentas](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) y [publicar el recorrido](../journeys/journey-overview.md).
