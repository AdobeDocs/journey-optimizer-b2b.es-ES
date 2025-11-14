---
title: 'Creación de contenido: personalización'
description: Sección reutilizada sobre el uso de la personalización para la creación de contenido
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Creación de contenido: personalización

Journey Optimizer B2B edition utiliza una sintaxis simple en línea que le permite crear expresiones con contenido personalizado entre llaves `{{}}`. Puede agregar varias expresiones en el mismo contenido o campo sin restricciones.

Por ejemplo, podría agregar una expresión personalizada como `Hello {{lead.firstName}} {{lead.lastName}}`. Al procesar el contenido, Journey Optimizer B2B edition reemplaza la expresión con los datos contenidos en la base de datos de Experience Platform. Así, el primer ejemplo se convierte en _Hello John Doe_.

Consulte [Personalización de contenido](../user/content/personalization.md) para obtener información más completa sobre el uso de herramientas de personalización en Journey Optimizer B2B edition.

>[!NOTE]
>
>Journey Optimizer B2B edition sigue la sintaxis de _camel case_ para los tokens de personalización de los mensajes de correo electrónico que coincidan con las demás aplicaciones de Adobe Experience Platform para ofrecer una experiencia coherente. Este formato de token es totalmente compatible con el [idioma de plantilla Handlebars](https://handlebarsjs.com/guide/#what-is-handlebars){target="_blank"}. Todos los tokens que se hayan agregado antes de este cambio se actualizan automáticamente.

En el siguiente ejemplo se describen los pasos para personalizar el contenido mediante tokens de persona y de sistema. Refleja los cambios disponibles para los entornos B2B edition de Journey Optimizer que se aprovisionan en la [arquitectura simplificada](../user/simplified-architecture.md).

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ ( ![Agregar icono de personalización](../assets/do-not-localize/icon-personalization-field.svg) ) de la barra de herramientas.

   ![Haga clic en el icono Personalizar](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Esta acción abre el diálogo _Editar Personalization_.

1. Agregue un token haciendo clic en el símbolo más ( **+** ) que hay junto a él.

   Si desea agregar el token con una reserva (texto predeterminado que aparece cuando ese campo no está disponible para un posible cliente), haga clic en el icono _Más_ ( **...** ) y elija **[!UICONTROL Insertar con texto de reserva]**.

   ![Construir texto personalizado con tokens](../assets/content-design-shared/visual-designer-personalize-dialog-handlebar.png){width="700" zoomable="yes"}

1. Agregue cualquier token adicional u otro texto estático que desee incluir.

1. Haga clic en **[!UICONTROL Guardar]**.

   Los scripts de personalización se muestran en el espacio de diseño visual. Puede seleccionarlo para realizar cambios cuando sea necesario.

   ![Seleccionar script de personalización](../assets/content-design-shared/visual-designer-select-personalization-script.png){width="600"}
