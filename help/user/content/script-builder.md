---
title: Generador de scripts
description: Utilice Script Builder, un asistente con tecnología de IA en el espacio de diseño de correo electrónico, para generar scripts de personalización de Handlebars y convertir scripts de Marketo Engage Velocity en Journey Optimizer B2B edition.
feature: AI Assistant, Generative AI, Personalization, Email Authoring
role: User, Developer
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-07-27T16:18:02.498Z'
TQID: 'https://experienceleague.adobe.com/JWnXAAbCuZVLv4ZhWubpNsZ61xbYU7xtdOXkG9uoWis'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0004f8fba0c3d4ae89063418e4d3ef8fea22b0c3
workflow-type: tm+mt
source-wordcount: 1074
ht-degree: 2%

---

# Generador de scripts

_Script Builder_ es un asistente con tecnología de IA disponible en el espacio de diseño de correo electrónico de [!DNL Adobe Journey Optimizer B2B Edition]. Ayuda a los especialistas en marketing y a los desarrolladores de correo electrónico a crear scripts de personalización más rápido y a migrar de [!DNL Marketo Engage] convirtiendo la lógica de personalización existente en [!DNL Journey Optimizer B2B Edition] sin reescribir el código manualmente.

>[!AVAILABILITY]
>
>En este momento, el Generador de scripts está disponible para clientes seleccionados como una versión beta limitada para correos electrónicos en **_solo recorridos de cuenta_**. Se ha planificado la compatibilidad con los recorridos de persona para una versión futura. Para obtener acceso, póngase en contacto con su representante de Adobe.

Para crear una personalización de correo electrónico condicional, como cambiar bloques de idioma por configuración regional, intercambiar contenido por región o persona o insertar valores de perfil dinámico o de objeto personalizado, es necesario crear expresiones _Handlebars_. Si migra desde [!DNL Marketo Engage], tiene el desafío agregado de reescribir scripts de _Velocity_ línea a línea. El Generador de scripts aborda ambos obstáculos desde una sola interfaz conversacional:

* Genere un nuevo script de personalización de Handlebars a partir de una descripción en lenguaje sencillo.
* Pegue un script de Velocity [!DNL Marketo Engage] y conviértalo en un script de Handlebars equivalente con asignación de token automática.
* Obtenga una vista previa, edite, valide y guarde el resultado directamente en el correo electrónico, sin copiar y pegar entre herramientas.

## Directrices y limitaciones

>[!IMPORTANT]
>
>El acceso del usuario al Generador de scripts se controla mediante los mismos permisos utilizados para otras capacidades de IA generativa en [!DNL Journey Optimizer B2B Edition]. Para obtener información sobre cómo conceder permisos de características, consulte [Habilitar el acceso al Asistente de IA](../ai-assistant/enable-ai-assistant-access.md).

Antes de usar el Generador de scripts, revisa las [directrices y limitaciones](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations) que se aplican a las características de IA generativa de [!DNL Journey Optimizer B2B Edition]. También se requiere la aceptación de [acuerdo del usuario](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"} para poder usar las capacidades de IA.

Familiarícese con el [lenguaje de plantilla Handlebars](https://handlebarsjs.com/guide/){target="_blank"}, la [sintaxis de personalización](./personalization-syntax.md) y las [funciones de ayuda](./personalization-helper-functions.md) admitidas en [!DNL Journey Optimizer B2B Edition]. El Generador de scripts genera Handlebars válidos para usted, pero comprender la sintaxis le ayuda a revisar y editar el resultado con confianza.

## Abrir el Generador de scripts {#open-script-builder}

El generador de scripts está disponible en el [editor de personalización](./personalization.md) mientras [crea contenido de correo electrónico](./email-authoring.md) para un recorrido de cuenta.

1. En el espacio de diseño del correo electrónico, seleccione el componente en el que desea añadir o reemplazar un script de personalización.

1. Para abrir el editor de personalización, haga clic en el icono _Agregar personalización_ ( ![Agregar icono de personalización](../../assets/do-not-localize/icon-personalization-field.svg) ).

1. En el editor, seleccione **[!UICONTROL Generador de scripts]**.

   ![Editor de Personalization: seleccione Generador de scripts](./assets/personalization-script-builder-select.png){width="700" zoomable="yes"}

   >[!BEGINSHADEBOX]

   La primera vez que acceda al Generador de scripts, revise las [_[!UICONTROL Condiciones de uso de la inteligencia artificial aplicada generativa ]_](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"} y confirme el acuerdo.

   ![Cuadro de diálogo del acuerdo de condiciones de uso de inteligencia artificial generativa en el Generador de scripts](./assets/personalization-script-builder-gen-ai-terms.png){width="400"}

   >[!ENDSHADEBOX]

   El panel Generador de scripts se abre con una interfaz de chat conversacional.

   ![Editor de Personalization: panel Generador de scripts](./assets/personalization-script-builder-welcome.png){width="700" zoomable="yes"}

1. Inicie el chat según lo que desee hacer:

   * [Generación de un nuevo script](#generate-personalization-script)
   * [Conversión de un script de Velocity existente](#convert-marketo-velocity-script)

## Generación de un script de personalización {#generate-personalization-script}

Utilice el Generador de scripts para crear un nuevo script de personalización de Handlebars a partir de una descripción en lenguaje sencillo, sin tener que escribir la expresión usted mismo.

El Generador de scripts incluye una biblioteca de asignaciones que resuelve los campos de cliente potencial y cuenta [!DNL Marketo Engage] en sus atributos de perfil XDM [!DNL Journey Optimizer B2B Edition] equivalentes, según la asignación de campo XDM [definida para su organización](../admin/xdm-field-management.md).

1. En la interfaz de chat del Generador de scripts, describa la lógica de personalización que desee.

   Por ejemplo, describa el atributo, el objeto personalizado o la condición que determina qué variante de contenido se va a mostrar.

1. Revise el script Handlebars generado en el panel de vista previa.

1. Edite el script directamente en el panel de vista previa si desea restringir la lógica o la redacción.

1. Haga clic en **[!UICONTROL Validar]** para comprobar el script con el esquema [!DNL Journey Optimizer B2B Edition].

   La validación detecta errores de sintaxis y referencias de tokens sin resolver antes de guardar el script, de modo que la personalización interrumpida nunca se publique en un correo electrónico activo.

1. Haga clic en **[!UICONTROL Guardar]** para insertar el script directamente en la ubicación seleccionada en el correo electrónico.

## Conversión de un script de Marketo Engage Velocity {#convert-marketo-velocity-script}

Use el Generador de scripts para migrar un script de Velocity [!DNL Marketo Engage] existente a un script de Handlebars equivalente para [!DNL Journey Optimizer B2B Edition].

1. En el chat del Generador de scripts, ingrese `Convert this` y pegue el script de Velocity que desea convertir.

   El Generador de scripts analiza las construcciones de Velocity, hace coincidir las referencias de token con los atributos de perfil XDM y genera el script Handlebars equivalente.

1. Revise el [informe de conversión](#review-conversion-report) y [resuelva cualquier token que necesite asignación manual](#resolve-tokens-without-mapping).

1. [Obtenga una vista previa y valide](#preview-validate-script) el script generado y, a continuación, guárdelo directamente en el correo electrónico.

### Construcciones de Velocity admitidas {#supported-velocity-constructs}

El Generador de scripts convierte las siguientes construcciones de flujo de control de Velocity de [!DNL Marketo Engage] en sus expresiones Handlebars o Conditional Content equivalentes:

| Construcción Velocity | Handlebars o equivalente de contenido condicional |
| ------------------- | --------------------------------------------- |
| `#if` / `#elseif` / `#else` | Handlebars `{{#if}}`, `{{else if}}` y `{{else}}` bloquean los ayudantes o una regla [!DNL Journey Optimizer B2B Edition] [conditional content](./conditional-content.md) |
| `#set` | Asignación de variables Handlebars dentro del script generado |

Traduce lógica condicional basada en segmentos a [contenido condicional](./conditional-content.md) reglas que replican el comportamiento de ramificación, incluidos correos electrónicos con muchos bloques de variante de idioma.

Si una construcción de Velocity no tiene Handlebars directos ni contenido condicional equivalente, Script Builder la marca en el [informe de conversión](#review-conversion-report) en lugar de generar una expresión incompleta o incorrecta.

### Revisión del informe de conversión {#review-conversion-report}

Después de cada conversión, el Generador de scripts muestra un informe estructurado que enumera:

* Tokens asignados correctamente.
* Tokens que requieren resolución manual.
* Construcciones de Velocity sin equivalente de Handlebars directo.

Utilice el informe para confirmar que la conversión se ha completado antes de resolver los tokens restantes y guardar la secuencia de comandos.

### Resolver tokens sin una asignación {#resolve-tokens-without-mapping}

Para los tokens que no están en la biblioteca de asignaciones, como los atributos de posible cliente personalizados o los objetos [!DNL Marketo Engage] personalizados, el Generador de scripts intenta resolver una asignación en el siguiente orden:

1. Sugiere una asignación probable basada en los campos XDM disponibles y, para los objetos personalizados, en las [clases basadas en modelos](./personalization.md#custom-datasets) configuradas para su organización, cuando exista una coincidencia segura.

1. Si no puede sugerir una coincidencia segura, le pide la asignación correcta en el chat.

Cuando confirma una asignación para un token que no estaba en la biblioteca, el Generador de scripts le pregunta si desea recordar la decisión. Si está de acuerdo, la asignación se recuerda para la instancia de origen [!DNL Marketo Engage], identificada por su ID de Munchkin, de modo que el mismo token se resuelva automáticamente la próxima vez que convierta un script a partir de esa instancia.

### Previsualización y validación del script {#preview-validate-script}

Antes de confirmar una conversión, el Generador de scripts muestra una previsualización en paralelo del script original de Velocity y la salida de Handlebars generada, con compatibilidad de edición en línea. Utilice la vista previa para comparar las dos versiones y realizar los ajustes directamente en el script generado.

Haga clic en **[!UICONTROL Validar]** para comparar los Handlebars generados con el esquema [!DNL Journey Optimizer B2B Edition]. La validación se ejecuta de nuevo al guardar, de modo que la personalización interrumpida nunca se publique en un correo electrónico activo.

Cuando esté satisfecho con el resultado, haga clic en **[!UICONTROL Guardar]** para insertar el script directamente en la ubicación elegida del correo electrónico.

<!--
### Save reusable conversion profiles {#save-reusable-conversion-profiles}

Save your field mappings and segment mappings as a reusable conversion profile so that your token schema does not need to be re-entered for each script or migration batch. Select a saved profile at the start of a conversion to apply its mappings automatically.

### Audit logs {#conversion-audit-logs}

Script Builder records an audit log for every conversion event, including which scripts were processed, which tokens were remapped, which tokens required manual intervention, and who approved the final output. Use the audit log to review migration activity across your organization.

-->
