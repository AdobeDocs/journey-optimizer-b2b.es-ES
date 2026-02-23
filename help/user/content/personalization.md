---
title: Personalización de contenido
description: Personalice los correos electrónicos B2B con tokens de cuenta, persona y sistema en Journey Optimizer B2B edition. Aprenda a utilizar el editor de personalización y la sintaxis.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: expresión, editor, inicio, personalización
exl-id: 60bf2e06-8d6e-4cc4-8aff-5c5ca11f05ab
source-git-commit: 10e02b821609c48b82ea0248501daa60de6daa12
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Personalización de contenido {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="Personalizar experiencias de contenido"
>abstract="Use **Adobe Journey Optimizer B2B edition** para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Puede ser su nombre, sector, título y mucho más."

Las funcionalidades de personalización de [!DNL Adobe Journey Optimizer B2B Edition] le permiten adaptar sus mensajes de correo electrónico a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Puede ser su nombre, sector, título y mucho más.

Con el _editor de personalización_, puede seleccionar, organizar, personalizar y validar todos los datos para crear una personalización personalizada para su contenido. Utilice varias herramientas, como funciones de ayuda, para adaptar los mensajes. El editor usa una sintaxis de personalización en línea basada en _Handlebars_, donde las expresiones se construyen con contenido entre llaves dobles `{{}}`.

Al procesar el mensaje, Journey Optimizer B2B edition reemplaza la expresión por los datos contenidos en el conjunto de datos de Adobe Experience Platform y los valores del sistema local. Por ejemplo, `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se convierte dinámicamente en `Hello John Doe`.

Con esta sintaxis, puede personalizar los mensajes en varios campos, incluidas las líneas de asunto de los correos electrónicos, los cuerpos de los mensajes y la información del remitente.

## tokens de Personalization

En [!DNL Journey Optimizer B2B Edition], puede generar su contenido de correo electrónico dinámico mediante tokens de personalización:

* **Tokens de cuenta**: estos tokens se basan en atributos de cuenta como _nombre de cuenta_, _sector_ y _número de empleados_. Utilice estos tokens para rellenar los datos de atributos administrados por el esquema **_XDM Business Account Details_**, que se define en Adobe Experience Platform.

* **tokens de persona**: estos tokens se basan en los atributos de la persona de negocios, como _nombre_, _cargo_ y _nombre de la compañía_. Utilice estos tokens para rellenar datos de atributo administrados por el esquema **_XDM Business Person Details_**, que se define en Adobe Experience Platform.

* **tokens del sistema**: estos tokens se basan en los valores de los campos del sistema, como _fecha_, _hora_ y _vínculo para cancelar la suscripción_.

* **Mis tokens** (cuando se definen para el recorrido): los [tokens personalizados definidos para el recorrido](./personalization-my-tokens.md) donde reside el correo electrónico.

>[!NOTE]
>
>Obtenga más información acerca de los esquemas XDM en la [documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/home){target="_blank"}.

## editor de Personalization

El editor de personalización está disponible en todos los contextos en los que necesita definir la personalización en el contenido del correo electrónico. En el editor, puede seleccionar, organizar, personalizar y validar todos los datos para crear una personalización personalizada para el contenido.

Agregue personalización en cualquier campo o componente de contenido haciendo clic en el icono _Agregar personalización_ ( ![Agregar icono de personalización](../../assets/do-not-localize/icon-personalization-field.svg) ).

![Editor de Personalization](./assets/personalization-editor.png){width="800" zoomable="yes"}

>[!NOTE]
>
>La siguiente información sobre el editor de personalización refleja los cambios disponibles para [!DNL Journey Optimizer B2B Edition] entornos aprovisionados en la [arquitectura simplificada](../simplified-architecture.md).

### Tokens y funciones de ayuda

Para usar un token de personalización o una función de ayuda, localícelo en el panel de navegación izquierdo y haga clic en **+** para agregarlo a la expresión.

Haga clic en el icono de _menú Más_ ( **...** ) (junto al icono de _Agregar_ ( **+** )) para ver más detalles de cada atributo y agregar los atributos utilizados con más frecuencia a _favoritos_. Se puede acceder a los atributos agregados a favoritos desde el menú **[!UICONTROL Favoritos]** en la navegación izquierda del editor.

![Editor de Personalization - menú Token More](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
También puede definir una cadena de texto de reserva predeterminada que se muestra si un atributo de perfil de tipo cadena está vacío. Haga clic en el icono _Menú más_ ( **...** ) del atributo y seleccione **[!UICONTROL Insertar con texto de reserva]**. Escriba el texto que se debe mostrar cuando el valor del atributo esté vacío para un perfil y, a continuación, haga clic en **[!UICONTROL Agregar]**.

Se recomienda validar la expresión antes de insertarla en el contenido. Haga clic en **[!UICONTROL Validar]** en la parte inferior del editor para comprobar la sintaxis y asegurarse de que no haya errores.

![Código validado por el editor de Personalization](./assets/personalization-editor-validated.png){width="500"}

Cuando la expresión esté completa y libre de errores, haga clic en **[!UICONTROL Guardar]**.

### Conjuntos de datos personalizados

[!BADGE Beta]{type=Informative tooltip="Función Beta"}

Puede utilizar esquemas relacionales para la personalización del correo electrónico. Los objetos personalizados se definen en _esquemas relacionales_, y un administrador de productos puede [configurar campos de esquema relacionales](../admin/xdm-field-management.md#relational-schemas) en [!DNL Journey Optimizer B2B Edition]. Se puede acceder a estos campos en el editor de personalización. Solo están disponibles los objetos personalizados que tienen una relación &quot;uno a varios&quot; (1:M) con Personas o Cuenta.

>[!IMPORTANT]
>
>Antes de usar objetos personalizados para la personalización mediante scripts, asegúrese de revisar y comprender el [lenguaje de plantilla Handlebars](https://handlebarsjs.com/guide/), la [sintaxis de personalización](./personalization-syntax.md) y las [funciones de ayuda integradas](./personalization-helper-functions.md).

Cuando define la personalización mediante objetos personalizados, puede acceder a todas las variables en objetos accesibles mediante scripts en los **[!UICONTROL tokens de Personalization]** (persona/posible cliente, cuenta, sistema y Mis tokens) y en los **[!UICONTROL objetos personalizados]** (esquemas relacionales). Con los objetos personalizados seleccionados, puede ver los campos haciendo clic en la carpeta de objetos personalizados. Haga clic en **+** para cada campo que desee agregar a la expresión.

![Editor de Personalization - Clases basadas en modelos - agregar campos de objeto personalizados](./assets/personalization-editor-custom-object-fields.png){width="700" zoomable="yes"}
