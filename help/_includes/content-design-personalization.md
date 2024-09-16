---
title: 'Creación de contenido: personalización'
description: Sección reutilizada sobre el uso de la personalización para la creación de contenido
source-git-commit: 0a9c05ac2ddd95e1fa5321f44f5cbe8cfa595007
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# Creación de contenido: personalización

Journey Optimizer B2B Edition utiliza una sintaxis simple en línea que le permite crear expresiones con contenido personalizado entre llaves dobles `{}`. Puede agregar varias expresiones en el mismo contenido o campo sin restricciones.

Ejemplos:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Al procesar el mensaje (correo electrónico y SMS), Journey Optimizer B2B Edition reemplaza la expresión por los datos contenidos en la base de datos de Experience Platform. Así, el primer ejemplo se convierte en _Hello John Doe_.

En el siguiente ejemplo se describen los pasos para personalizar el contenido mediante atributos de cliente potencial/cuenta y tokens del sistema.

1. Seleccione el componente de texto y haga clic en el icono _Agregar personalización_ de la barra de herramientas.

   ![Haga clic en el icono Personalizar](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Esta acción abre el diálogo _Editar Personalization_.

1. Haga clic en **+** o **...** para agregar un token al espacio en blanco.

   ![Construir texto personalizado con tokens](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Guardar]**.
