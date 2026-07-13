---
title: Creación de fragmentos
description: 'Cree fragmentos de contenido reutilizables con las herramientas de diseño visual: añada estructura, recursos, personalización, contenido condicional y seguimiento de URL vinculado para correos electrónicos y plantillas en Journey Optimizer B2B Prime.'
badgeBeta: label="Beta" type="informative" tooltip="Esta función forma parte de una versión beta limitada."
autotag-review: '2026-07-13T16:38:09.506Z'
TQID: 'https://experienceleague.adobe.com/Zn5L6Bc3x8SuGyjOPDdTWI-oxrrhk06a2f8ZvX2SN4s'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: e1663313-7961-4100-bea9-fa9f4edf8493id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 5206ed7bc0ce24e65700da28b023d76c68cb6419
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 4%

---

# Creación de fragmentos

Después de [crear un fragmento](./fragments.md#create-fragments), use el espacio de diseño visual para crear la estructura y los componentes de contenido del fragmento.

## Añadir estructura y contenido {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## Añadir recursos {#add-assets}

En el espacio de diseño visual, seleccione el icono _Assets_ ( ![Assets icon](../../assets/do-not-localize/icon-assets-me.svg) ) en la barra de navegación izquierda para examinar y seleccionar recursos de imagen de la biblioteca de recursos [!DNL Journey Optimizer B2B Prime].

Para ver los pasos para seleccionar, reemplazar o cargar recursos de imagen, consulte [Usar recursos para la creación de contenido](./digital-asset-management.md#assets-authoring).

## Desplazamiento por las capas, la configuración y los estilos {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## Personalización del contenido {#personalize-content}

[!DNL Journey Optimizer B2B Prime] utiliza la sintaxis de Handlebars para la personalización. Los tokens se sustituyen en el momento del envío con valores de los datos de perfil de cada destinatario.

_Para agregar personalización :_

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ ( ![Icono de personalización](../../user/assets/do-not-localize/icon-personalize.svg) ) de la barra de herramientas.
1. En el cuadro de diálogo de personalización, examine el árbol de esquema de la izquierda y seleccione un atributo de perfil. El editor inserta la expresión Handlebars correspondiente; por ejemplo, `{{profile.firstName}}`.
1. Agregue un valor de reserva para controlar los datos que faltan, si es necesario; por ejemplo, `{{profile.firstName | default: "there"}}`.
1. Haga clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]**. La expresión aparece en línea en el campo.

Para obtener más información sobre las herramientas y la sintaxis del editor de expresiones, consulte [Editor de Personalization](./personalization-expressions.md).

## Editar seguimiento de URL vinculadas {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
