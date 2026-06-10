---
title: Tokens personalizados para Personalization de correo electrónico
description: 'Cree y administre Mis tokens personalizados para la personalización dinámica de correos electrónicos: defina variables de texto y número para los recorridos de cuenta en Journey Optimizer B2B edition.'
feature: Personalization, Content, Email Authoring
role: User
exl-id: 05d4f446-6348-4555-9c46-316c2857f01d
autotag-review: '2026-05-27T16:17:44.938Z'
TQID: 'https://experienceleague.adobe.com/Jhx5DqeSOi5oTIyBNXw04RagSUFiNx-OPig-vTdFWfU'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: d90cafcd84266a177523fc6d716ebfa8bf999d89
workflow-type: tm+mt
source-wordcount: 605
ht-degree: 2%

---

# Tokens personalizados para la personalización de correo electrónico

La personalización de contenido utiliza tokens como marcadores de posición o variables que se rellenan cuando se genera el artefacto de contenido. Los tokens de personalización estándar están disponibles para correos electrónicos, páginas de aterrizaje, fragmentos y plantillas. También puede definir un conjunto de tokens personalizados con valores específicos del recorrido de la cuenta. Este conjunto de tokens personalizados se denomina _Mis tokens_ y cualquiera de ellos se usa para personalizar al [crear correos electrónicos de recorrido](./email-authoring.md#content-authoring---personalization).

Además de _Mis tokens_, que son específicos del recorrido de la cuenta, puede usar cualquiera de los tokens estándar (integrados) para la personalización de correo electrónico.

## Administrar mis tokens {#my-tokens}

Los _Mis tokens_ son variables personalizadas que se crean o modifican para un recorrido de cuenta en estado de Borrador. Actualmente, este conjunto de tokens personalizados admite definiciones de tokens de texto y números.

Cuando agrega un token personalizado a un correo electrónico, se muestra como `{{my.TokenName}}`. Por ejemplo, podría tener `{{my.EventDate}}` o `{{my.WebinarSpeaker}}` tokens creados para administrar el contenido de los correos electrónicos relacionados con los próximos seminarios web.

_Para tener acceso a los tokens personalizados de un recorrido de cuenta :_

1. Abra el recorrido de cuenta provisional.

1. Haz clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y elige **[!UICONTROL Mis tokens]**.

   ![Haga clic en Más en la parte superior derecha](../journeys/assets/account-journey-draft-more-menu.png){width="450"}

   La página _Mis tokens_ enumera todos los tokens personalizados definidos para el recorrido.

   ![Mis tokens](./assets/my-tokens-list-page.png){width="700" zoomable="yes"}

### Crear un token

1. En la página _[!UICONTROL Mis tokens]_, haga clic en **[!UICONTROL Crear]** y elija el tipo de token que desea definir:

   * **[!UICONTROL Texto]**: utilice este tipo para definir un token con un valor de cadena de texto básico.

   * **[!UICONTROL Número]**: utilice este tipo para definir un token con un valor numérico.

1. En el cuadro de diálogo, escriba **[!UICONTROL Nombre]** y **[!UICONTROL Valor]** para el token.

   ![Escriba un nombre y un valor para el token de texto](./assets/my-tokens-create-text-token-dialog.png){width="400"}

   No se pueden utilizar espacios ni caracteres especiales en el nombre del token. Puede usar _minúscula_, como `EventType`, para usar un nombre de varias palabras que se identifique fácilmente.

   Si está definiendo un token _Number_, el valor solo puede contener caracteres numéricos. Puede utilizar un valor decimal.

   ![Escriba un nombre y un valor para el token numérico](./assets/my-tokens-create-number-token-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Agregar]**.

### Edición de un token

Aunque el recorrido de la cuenta permanece en estado de borrador, puede editar cualquiera de los Mis tokens definidos.

1. En la página _[!UICONTROL Mis tokens]_, haga clic en el icono _Más acciones_ (**...**) junto al nombre del token y elija **[!UICONTROL Editar]**.

   ![Menú de acciones Token More](./assets/my-tokens-more-actions.png){width="430"}

1. En el cuadro de diálogo, cambie **[!UICONTROL Nombre]** y **[!UICONTROL Valor]** según sea necesario para el recorrido.

   ![Cambiar el nombre y el valor del token](./assets/my-tokens-edit-text-token-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Editar]**.

### Eliminación de un token

Puede eliminar un token personalizado de la lista _Mis tokens_, pero debe asegurarse de que no lo esté utilizando actualmente en el contenido del correo electrónico de recorrido.

1. En la página _[!UICONTROL Mis tokens]_, haga clic en el icono _Más acciones_ (**...**) junto al nombre del token y elija **[!UICONTROL Eliminar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Uso de tokens personalizados en el contenido

Cuando esté creando contenido de correo electrónico para el recorrido de su cuenta, puede usar cualquiera de los tokens de la lista _Mis tokens_ al usar las herramientas de personalización en el espacio de diseño visual.

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ ( ![Agregar icono de personalización](../../assets/do-not-localize/icon-personalization-field.svg) ) de la barra de herramientas.

   ![Haga clic en el icono Añadir personalización](./assets/email-personalize-text.png){width="600"}

   Esta acción abre el diálogo _Editar Personalization_. El cuadro de diálogo incluye una carpeta _[!UICONTROL Mis tokens]_ en la biblioteca _[!UICONTROL Personalization Tokens]_ si hay tokens personalizados definidos para el recorrido de la cuenta.

1. Para agregar uno de los tokens personalizados al espacio en blanco, expanda la carpeta **[!UICONTROL Mis tokens]** y, a continuación, haga clic en **+** o **...**.

   Puede agregar cualquier texto estático adicional que necesite.

   ![Crear texto personalizado con Mis tokens](./assets/personalization-edit-dialog-my-tokens.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.
