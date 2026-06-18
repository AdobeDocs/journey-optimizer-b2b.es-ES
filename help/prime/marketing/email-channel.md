---
title: Canal de correo electrónico
description: 'Añadir nodos de acción de correo electrónico a los recorridos de la cuenta: cree nuevos correos electrónicos o utilice correos electrónicos de Marketo Engage existentes para comunicaciones de destino en Journey Optimizer B2B edition.'
feature: Email Authoring, Account Journeys
role: User
autotag-review: '2026-06-18T20:30:25.418Z'
TQID: 'https://experienceleague.adobe.com/K3OZnLvtSdwSq6AT4JlRQ62t32d6smIJ4K9EEnK-QUc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 2%

---

# Canal de correo electrónico

[!DNL Adobe Journey Optimizer B2B Prime] ofrece a los especialistas en marketing B2B una experiencia moderna de creación y envío de correo electrónico de nivel empresarial. Esta versión introduce herramientas de diseño de correo electrónico rediseñadas y un conjunto completo de controles de envío de correo electrónico.

>[!NOTE]
>
>Si envía un correo electrónico por primera vez, asegúrese de que el [canal de correo electrónico y la capacidad de entrega](../admin/configuration-email-deliverability.md) estén configurados.

## Resumen del canal de correo electrónico {#overview}

* **Configuraciones del canal de correo electrónico**: administre la identidad del remitente, el comportamiento de respuesta, el marketing frente a los tipos de mensajes transaccionales y el seguimiento.
* **Controles de envío de correo electrónico**: configure su canal de envío de correo electrónico, incluida la delegación de subdominios (métodos completamente delegados y CNAME), DMARC, la configuración automática de SPF/DKIM y la compatibilidad con grupos de IP compartidas.
* **Acción Enviar correo electrónico** - Desde un recorrido, agregue un nodo de acción _Enviar correo electrónico_, incluida la personalización mediante atributos de perfil (sintaxis de Handlebars).
* **Herramientas visuales de diseño de correo electrónico de arrastrar y soltar**: diseñe su contenido de correo electrónico con estructuras, componentes de contenido, temas, compatibilidad con modo oscuro y fragmentos visuales reutilizables.
* **Recursos de Marketo Design Studio**: elija imágenes y recursos de una copia única de la biblioteca de recursos de Marketo Engage directamente en el lienzo del correo electrónico.
* **Plantillas y fragmentos reutilizables**: guarde encabezados, pies de página, CTA y diseños de correo electrónico completos comunes y reutilícelos en todos los recorridos.
* **Control de acceso basado en roles (RBAC)**: aplique permisos granulares para crear, editar, aprobar y enviar correo electrónico.

## Conceptos clave {#key-concepts}

Antes de crear correos electrónicos para recorridos de personas y contenido de correo electrónico, revise estos conceptos:

| Concepto | En [!DNL Journey Optimizer B2B Prime] Prime |
| ------- | ---------------------- |
| **_Espacio de diseño de correo electrónico_** | El lienzo visual y las herramientas de diseño utilizadas para componer el contenido del correo electrónico. Incluye componentes de diseño de arrastrar y soltar, plantillas, fragmentos, temáticas y un editor de personalización. |
| **_Plantilla_** | Diseño de correo electrónico reutilizable disponible para crear un nuevo correo electrónico. Puede ser una plantilla de ejemplo integrada proporcionada por Adobe o una plantilla personalizada creada por su equipo. |
| **_Fragmento visual_** | Bloque de contenido reutilizable (como encabezado, pie de página, CTA, exención de responsabilidad legal) que se puede insertar en varios correos electrónicos. La actualización de un fragmento propaga el cambio a cada correo electrónico que lo utiliza. |
| **_Tema_** | Un ajuste preestablecido de estilo reutilizable (colores, tipografía, espaciado, estilos de botón) aplicado en un correo electrónico. |
| **_Token de Personalization_** | Una expresión Handlebars, por ejemplo, `{{profile.firstName}}`, se resuelve en el momento del envío con los datos de perfil de cada destinatario. |
| **_Enviar acción por correo electrónico_** | Nodo de acción de recorrido que utiliza una configuración de canal y contenido de correo electrónico para enviar un correo electrónico. |

## Adición de un correo electrónico desde un recorrido

Para enviar correo electrónico desde un recorrido, agrega un nodo _Realizar una acción_ y configúrelo para enviar correo electrónico.

1. En el lienzo del recorrido, haga clic en el icono **+** y seleccione **[!UICONTROL Realizar una acción]**.

1. En las propiedades del nodo a la derecha, establezca la acción en **[!UICONTROL Enviar correo electrónico]**.

   ![Realizar una acción - Enviar correo electrónico](./assets/person-action-node-send-email.png){width="450"}

1. Elija la fuente de correo electrónico:

   * **Crear/editar correo electrónico**: elija esta opción para definir el contenido del correo electrónico, incluida la línea de asunto, la información del remitente y el cuerpo del correo electrónico en el espacio de diseño del correo electrónico.

   * **[!UICONTROL Usar un correo electrónico personalizado con IA]**: elija esta opción para restringir un correo electrónico generado por IA en el espacio de diseño del correo electrónico. Estos correos electrónicos están optimizados para que los clientes de la bandeja de entrada asistida por IA fundamenten sus resúmenes y respuestas en sus ofertas y llamadas a la acción.

1. Haga clic en **[!UICONTROL Crear correo electrónico]**.

1. En el cuadro de diálogo _[!UICONTROL Crear correo electrónico]_, escriba un **[!UICONTROL Nombre]** único (obligatorio) y una **[!UICONTROL Descripción]** (opcional).

1. Haga clic en **[!UICONTROL Crear]**.

## Definir las propiedades y acciones del correo electrónico

1. Con el nodo _[!UICONTROL Enviar correo electrónico]_ seleccionado en el lienzo del recorrido, haga clic en **[!UICONTROL Editar correo electrónico]** en las propiedades del nodo a la derecha.

<!-- Staging environment broken -->

para el correo electrónico y **[!UICONTROL Línea de asunto]**.

Se abrirá la ficha **[!UICONTROL Acciones]**, donde podrá seleccionar o crear la configuración de correo electrónico que quiera usar.

1. (Opcional) Seleccione un conjunto de reglas en Reglas de negocio para aplicar reglas de límite a la acción de correo electrónico.

Puede usar la [opción de optimización del tiempo de envío](./email-send-time-optimization.md) para predecir el mejor momento para enviar el mensaje y maximizar la participación en función de la apertura histórica y las tasas de clics. Descubrir cómo

Seleccione el botón Editar contenido y cree el contenido que desee mediante el Designer de correo electrónico.

Volver al lienzo de recorrido. Si es necesario, complete el flujo de recorrido arrastrando y soltando acciones o eventos adicionales.

Para obtener más información sobre cómo crear, configurar y publicar un recorrido, consulte esta página.


### Definir configuración de correo electrónico {#email-settings}

Configure las opciones en la ficha **[!UICONTROL Detalles]** del panel de resumen del nodo.

| Configuración | Descripción |
| ------- | ----------- |
| **[!UICONTROL De nombre]** | Nombre del remitente mostrado en el encabezado del correo electrónico. Admite tokens de personalización. |
| **[!UICONTROL Del correo electrónico]** | Dirección de correo electrónico del remitente Valores predeterminados de configuración de canal. Admite personalización. |
| **[!UICONTROL Dirección de respuesta]** | Dirección que recibe las respuestas de los destinatarios. Admite personalización. |
| **[!UICONTROL Línea de asunto]** | Línea de asunto de correo electrónico. Editable a partir del valor introducido durante la creación. |
| **[!UICONTROL Dominio de marca]** | Dominio utilizado para el envío específico de la marca. |
| **[!UICONTROL IP dedicada]** | Dirección IP específica para el seguimiento de la capacidad de entrega. |
| **[!UICONTROL Correo electrónico operativo]** | Cuando está habilitado, evita la exclusión y la supresión de la suscripción. Utilícelo únicamente para mensajes operativos legítimos. |
| **[!UICONTROL Incluir vista como página web]** | Genera un vínculo a una página web para el contenido del correo electrónico. |
| **[!UICONTROL Deshabilitar seguimiento de aperturas]** | Evita el seguimiento de la actividad de apertura de correo electrónico. |
| **[!UICONTROL Encabezado previo]** | Texto de resumen corto que se muestra después de la línea de asunto en las vistas previas de la bandeja de entrada. |
| **[!UICONTROL Direcciones CC]** | Añada hasta 25 campos de correo electrónico de posible cliente o compañía para recibir una copia. |

### Comprobación de alertas {#alerts}

[!DNL Journey Optimizer B2B Prime] muestra los problemas en la esquina superior derecha del editor de correo electrónico. Resuelva todos los errores antes de activar el recorrido: las advertencias solo son recomendaciones.

**Errores** (evitar la activación del recorrido):

* El nombre de remitente está vacío
* Falta la línea de asunto
* El contenido del correo electrónico está vacío

**Advertencias** (recomendaciones):

* El vínculo de no participación no está presente en el cuerpo del correo electrónico
* La versión de texto de HTML está vacía
* Vínculos vacíos detectados
* El correo electrónico supera los 100 K
