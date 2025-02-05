---
title: 'Creación de contenido: personalización'
description: Sección reutilizada sobre el uso de la personalización para la creación de contenido
source-git-commit: 3791beb98068a56882bb0a96fbc6b192e85130bb
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# Creación de contenido: personalización

Journey Optimizer B2B edition utiliza una sintaxis simple en línea que le permite crear expresiones con contenido personalizado entre llaves dobles `{}`. Puede agregar varias expresiones en el mismo contenido o campo sin restricciones.

Ejemplos:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Al procesar el contenido, Journey Optimizer B2B edition reemplaza la expresión con los datos contenidos en la base de datos del Experience Platform. Así, el primer ejemplo se convierte en _Hello John Doe_.

En el siguiente ejemplo se describen los pasos para personalizar el contenido mediante atributos de cliente potencial/cuenta y tokens del sistema.

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ de la barra de herramientas.

   ![Haga clic en el icono Personalizar](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Esta acción abre el diálogo _Editar Personalization_.

1. Haga clic en **+** o **...** para agregar un token al espacio en blanco.

   ![Construir texto personalizado con tokens](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.
