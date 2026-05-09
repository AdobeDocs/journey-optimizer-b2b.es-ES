---
title: Configuración de página de aterrizaje
description: Configure subdominios de página de aterrizaje, configuración de relleno previo de formularios y flujos de datos para habilitar la publicación de páginas web de Campaign en Journey Optimizer B2B edition.
feature: Setup, Landing Pages, Content
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
exl-id: 54b812cb-0129-4253-8e9e-538c25fc4709
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: fbb9aba8-f6d8-4266-abfe-9a84ebf4aee2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: '2026-03-27T22:50:39.828Z'
source-git-commit: e54cfce913e61fb1f96fc7bedeb51885085d095b
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 100%

---

# Configuración de página de aterrizaje

Los administradores deben asegurarse de que la configuración de la página de aterrizaje esté establecida para los especialistas en marketing que crean y publican estas páginas.

## Configuración

Para revisar la configuración de la página de aterrizaje, ve a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**. En _[!UICONTROL Páginas de destino]_ en el panel de navegación, seleccione **[!UICONTROL Configuración]**.

![Configuración de página de aterrizaje](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

### Cadena de cuenta {#account-string}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_account_string"
>title="Cadena de cuenta de las páginas de destino"
>abstract="La cadena de la cuenta identifica la instancia de Adobe Journey Optimizer B2B Edition que aloja las páginas de destino."

La cadena de la cuenta identifica la instancia de Adobe Journey Optimizer B2B Edition que aloja las páginas de destino. Asegúrese de que el equipo de sistemas agrega y configura la entrada DNS.

### Relleno previo de formulario {#form-prefill}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_form_prefill"
>title="Configuración del relleno previo del formulario de la página de destino"
>abstract="Puede habilitar la opción de rellenado previo del formulario para permitir que los formularios de las páginas de destino utilicen información rellenada previamente para usuarios conocidos."

Habilite la opción **[!UICONTROL Relleno previo de formulario]** para permitir que los formularios de sus páginas de aterrizaje utilicen información rellenada previamente para usuarios conocidos. Cuando esta opción está deshabilitada, los autores de páginas de aterrizaje no pueden incluir campos de formulario rellenados previamente.

### Secuencia de datos {#datastream}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_datastream"
>title="Requisito de la secuencia de datos"
>abstract="Se necesita una secuencia de datos para recopilar eventos de página de las páginas de aterrizaje de este dominio."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_missing_datastream"
>title="Falta el ID de secuencia de datos"
>abstract="En el subdominio falta un ID de secuencia de datos, que es necesario para el enrutamiento adecuado. Configúrelo en Configuración para continuar"

Establezca la opción **[!UICONTROL Flujo de datos]** para configurar un flujo de datos para la colección de eventos de páginas de aterrizaje.

## Subdominios {#add-subdomain}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_add_subdomain"
>title="Añadir subdominio de la página de destino"
>abstract="Puede añadir un máximo de 50 subdominios. Configure un nuevo subdominio para cada URL de marca única que desee alojar en Adobe Journey Optimizer B2B Edition."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_configure_subdomain"
>title="Configurar subdominio de la página de destino"
>abstract="Se requiere un subdominio configurado para publicar páginas de destino. Puede utilizar un subdominio que ya se haya delegado a Adobe o bien crear uno nuevo."

Un subdominio de página de aterrizaje debe ayudar a identificar el tipo de contenido, el nombre del producto o la campaña y reforzar la autenticidad de la página. Antes de configurar los subdominios, defina uno o varios CNAME para utilizarlos en las páginas de aterrizaje. Por ejemplo:

* **producto**.[DominioCompañía].com
* **ir**.[DominioCompañía].com
* **registro**.[DominioCompañía].com

En estos ejemplos, la primera parte (en negrita) es `LandingPageCNAME`.

Añada un nuevo subdominio para cada URL de marca única que desee alojar en Adobe Journey Optimizer B2B edition. Puede agregar un número máximo de 50 subdominios.

>[!IMPORTANT]
>
>No se permite delegar un subdominio no válido a Adobe. Asegúrese de introducir un subdominio válido de su organización, como _marketing.yourcompany.com_.

Para revisar los subdominios y agregar nuevos, ve a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**. En _[!UICONTROL Páginas de destino]_ en el panel de navegación, seleccione **[!UICONTROL Subdominios]**.

![Subdominios de página de aterrizaje](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

_Para agregar un subdominio de página de aterrizaje :_

1. Haga clic en **[!UICONTROL Agregar subdominio]** en la parte superior derecha.

1. En _[!UICONTROL Detalles del subdominio]_, escriba la información del subdominio:

   * **[!UICONTROL Subdominio]**: la dirección URL de subdominio que se va a usar, como `marketing.yourcompany.com`
   * **[!UICONTROL Página predeterminada]**: URL de la página de subdominio predeterminada, como `marketing.yourcompany.com/products`
   * **[!UICONTROL Página de reserva]**: URL de la página de reserva que se utilizará si una página de aterrizaje del subdominio no está activa, como `marketing.yourcompany.com/expired`

   ![Agregar subdominio de página de aterrizaje](./assets/config-landing-pages-add-subdomain.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.
