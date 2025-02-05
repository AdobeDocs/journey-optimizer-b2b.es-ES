---
title: Fragmentos
description: Se han reutilizado notas y elementos visuales para anotar una función o página que se aplica a una edición específica
source-git-commit: 8892aff0501a157006506663ef304be5ccc9695c
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Fragmentos

<!-- Content authoring steps for reuse -->

## Configuración de datos por intención {#intent-data-note}

>[!NOTE]
>Los datos de intención también se pueden incluir en la página cuando se configuran para la instancia de Journey Optimizer B2B edition. Para obtener más información acerca del modelo de detección de intención y cómo enviar palabras clave, vea [Datos por intención](../user/admin/intent-data.md).
>

## AEM nota de licencia de recursos de {#aem-assets-licensing-note}

>[!NOTE]
>
>Las licencias para AEM Assets as a Cloud Service y la licencia de Dynamic Media son requisitos previos para la integración. Debe asegurarse de que [Dynamic Media con API abierta](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"} esté habilitado.<br/>
>Según el contrato y la configuración, se puede acceder directamente al as a Cloud Service de Adobe Experience Manager Assets desde Adobe Journey Optimizer B2B edition al diseñar contenido visual.

## Creación de contenido: componentes, paso de estructuras {#structures-step}

1. Para iniciar el diseño de contenido, arrastre un elemento desde **[!UICONTROL Structures]** y suéltelo en el lienzo.

   Agregue tantos elementos de _[!UICONTROL Structures]_ como necesite y edite la configuración de cada uno en el panel de la derecha.

   >[!TIP]
   >
   >Seleccione el componente _[!UICONTROL n:n column]_ para definir el número de columnas que desee (entre tres y 10). También puede definir el ancho de cada columna moviendo las flechas debajo de la columna.

   ![Arrastre una estructura al lienzo y ajuste la configuración](../assets/content-design-shared/content-design-add-structure.png){width="800" zoomable="yes"}

   Cada tamaño de columna no puede ser inferior al 10 % de la anchura total del componente de estructura. Solo se pueden eliminar columnas vacías.

## Creación de contenido: componentes, paso de contenido {#contents-step}

1. Expanda la sección **[!UICONTROL Contenido]** y agregue tantos elementos como necesite a uno o más componentes de estructura.

   ![Arrastre un elemento de contenido al lienzo y ajuste la configuración](../assets/content-design-shared/content-design-add-content.png){width="800" zoomable="yes"}
   <!--
   reference to the contents elements--->

## Creación de contenido: componentes, paso de configuración {#settings-step}

1. Si es necesario, puede realizar personalizaciones adicionales para cada componente en las fichas _[!UICONTROL Configuración]_ o _[!UICONTROL Estilo]_.

   Por ejemplo, puede cambiar el estilo del texto, el relleno o el margen de cada componente.

## Creación de contenido: paso de activos {#assets-step}

1. Desde el selector _Asset_, puede seleccionar directamente los recursos almacenados en la biblioteca de recursos.

   Haga doble clic en la carpeta que contiene los recursos. Arrastre y suelte los elementos en un componente de estructura.

   Para obtener más información sobre el uso de recursos del tipo de origen, consulte [Agregar recursos al contenido](../user/content/assets-overview.md#use-assets-for-content-authoring).

   ![Arrastre un recurso de Marketo Engage al lienzo y ajuste la configuración](../assets/content-design-shared/content-design-add-asset.png){width="800" zoomable="yes"}

## Creación de contenido: paso de personalización {#personalization-step}

1. Inserte campos de personalización para personalizar el contenido a partir de atributos de perfiles, pertenencias a audiencias, atributos contextuales, etc.

## Creación de contenido: paso para habilitar el contenido de condición {#dynamic-content-step}

1. Haga clic en **[!UICONTROL Habilitar contenido de condición]** para agregar contenido dinámico y adaptar el contenido a los perfiles de destino según las reglas condicionales.

## Creación de contenido: paso de seguimiento de vínculos {#links-tracking-step}

1. Seleccione la ficha **[!UICONTROL Vínculos]** del panel izquierdo para mostrar todas las direcciones URL del contenido del que se realiza un seguimiento.

   Puede modificar _Tracking Type_ o _Label_ y agregar etiquetas si es necesario.
