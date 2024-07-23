---
title: Creación de correo electrónico
description: Obtenga información sobre cómo crear contenido de correo electrónico personalizado que se utiliza en Recorridos de cuenta.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: cae7aa7faa67bd1888b85051ff247848b6c3c072
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 1%

---

# Creación de correo electrónico

Utilice Adobe Journey Optimizer B2B Edition para enviar mensajes de correo electrónico a sus clientes. Puede crear, personalizar y previsualizar mensajes en el Diseñador de correo electrónico.

## Añadir una acción de correo electrónico en un recorrido de cuenta

Puede configurar los envíos de correo electrónico en un Recorrido de cuentas cuando agregue un nodo _[!UICONTROL Realizar una acción]_ y hacer lo siguiente:

1. Para la _[!UICONTROL acción en]_ destino, elige **[!UICONTROL Personas]**.
1. Para la _[!UICONTROL acción sobre personas]_, elige **[!UICONTROL Enviar correo electrónico]**.
1. Para el _[!UICONTROL origen del correo electrónico]_, elija **[!UICONTROL Crear nuevo correo electrónico]**.

   También puede seleccionar la opción `Select email from Adobe Marketo Engage` para utilizar uno de los correos electrónicos creados previamente en Marketo Engage y enviarlo como parte del Recorrido de cuentas.

   >[!NOTE]
   >
   >Si crea un correo electrónico por primera vez, asegúrese de que el canal de correo electrónico esté configurado desde Adobe Marketo Engage. Para obtener más información, consulte [Garantizar la entrega de correos electrónicos](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) en la documentación del Marketo Engage.

   ![Realizar una acción: enviar un correo electrónico](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. En la parte inferior del panel _[!UICONTROL Realizar una acción]_, haga clic en **[!UICONTROL Crear correo electrónico]**.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único para el correo electrónico y una **[!UICONTROL Línea de asunto]**.

   ![Crear nuevo cuadro de diálogo de correo electrónico](assets/create-new-email.png){width="400"}

1. Haga clic en **[!UICONTROL Crear]**.

   En la sección _[!UICONTROL Propiedades de correo electrónico]_ de la página de contenido de correo electrónico, los campos _[!UICONTROL De correo electrónico]_ y _[!UICONTROL Responder a dirección]_ ya están configurados. Puede escribir valores para los campos _[!UICONTROL Nombre del formulario]_ y _[!UICONTROL Descripción]_ (opcional).

## Creación de contenido de correo electrónico

Haga clic en **[!UICONTROL Agregar contenido de correo electrónico]** en la parte superior del panel de vista previa de _[!UICONTROL Correo electrónico]_.

![Haga clic en Agregar contenido de correo electrónico ](./assets/add-email-content.png){width="700" zoomable="yes"}

Esta acción inicia el Designer de correo electrónico, donde puede elegir cómo desea diseñar el correo electrónico entre las siguientes opciones:

* [Diseñe su correo electrónico desde cero](#design-your-email-from-scratch) mediante la interfaz de Designer de correo electrónico.

* [Importe contenido existente del HTML](#import-existing-html-content) desde un archivo o una carpeta .zip.

* [Seleccione una plantilla existente](#select-a-template) de una lista de plantillas de correo electrónico integradas o personalizadas.

Para configurar y personalizar la línea de asunto con el editor de expresiones, haga clic en el icono _Personalization_ y agregue cualquiera de los tokens de Marketo Engage.

Después de crear y personalizar el contenido del correo electrónico, puede exportarlo para su validación o uso posterior. Haga clic en **[!UICONTROL HTML de exportación]** para guardar el contenido como archivo .zip que incluye el HTML y los recursos.

>[!TIP]
>
>Utilice AI Assistant en Adobe Journey Optimizer B2B Edition, con tecnología de IA generativa, para elevar el contenido al siguiente nivel. El asistente de IA puede ayudarle a optimizar el impacto de sus envíos generando correos electrónicos completos, contenido de texto de destino y obteniendo recomendaciones del asistente de IA para imágenes que resuenen con su audiencia. [Más información](./ai-assistant-emails.md)

### Diseñe su correo electrónico desde cero

1. En la página de inicio de Designer, seleccione la opción **[!UICONTROL Diseñar desde cero]**.

1. Para iniciar el diseño de contenido, arrastre un elemento desde **[!UICONTROL Structures]** y suéltelo en el lienzo.

   Repita este paso para cada componente de estructura para construir el diseño del correo electrónico.

1. Agregue tantos elementos de _Structures_ como necesite y edite la configuración de cada uno en el panel de la derecha.

   Seleccione el componente de columna n:n para definir el número de columnas que desea (entre tres y 10). También puede definir el ancho de cada columna moviendo las flechas debajo de la columna.

   Cada tamaño de columna no puede ser inferior al 10 % de la anchura total del componente de estructura. Solo se pueden eliminar columnas vacías.

1. Expanda la sección **[!UICONTROL Contenido]** y agregue tantos elementos como necesite a uno o más componentes de estructura.

1. Si es necesario, puede realizar personalizaciones adicionales para cada componente en las fichas _[!UICONTROL Configuración]_ o _[!UICONTROL Estilo]_.

   Por ejemplo, puede cambiar el estilo del texto, el relleno o el margen de cada componente.

1. Desde el Selector de recursos, puede seleccionar directamente los recursos almacenados en la biblioteca de Assets.

   Haga doble clic en la carpeta que contiene los recursos. Arrastre y suelte los elementos en un componente de estructura.

1. Inserte campos de personalización para personalizar el contenido a partir de atributos de perfiles, suscripciones a audiencias, atributos contextuales, etc.

1. Haga clic en **[!UICONTROL Habilitar contenido de condición]** para agregar contenido dinámico y adaptar el contenido a los perfiles de destino según las reglas condicionales.

1. Seleccione la ficha **[!UICONTROL Vínculos]** del panel izquierdo para mostrar todas las direcciones URL del contenido de las que se realiza un seguimiento.

   Puede modificar el Tipo de seguimiento o la Etiqueta y añadir etiquetas si es necesario.

Si es necesario, puede personalizar aún más su correo electrónico haciendo clic en **[!UICONTROL Cambiar al editor de código]** desde el menú avanzado. El editor de código permite editar el código fuente del correo electrónico, como añadir etiquetas de seguimiento o de HTML personalizadas.

>[!CAUTION]
>
>No puede volver al diseñador visual para este correo electrónico después de cambiar al editor de código.

Cuando finalice el contenido, haga clic en **[!UICONTROL Simular contenido]** en la parte superior para comprobar la renderización. Puede elegir la vista de escritorio o la vista móvil.

Cuando esté listo, haga clic en Guardar.

### Importación de contenido de HTML existente

El contenido importado puede ser:

* Archivo de HTML con una hoja de estilos incorporada
* Carpeta .zip que incluye un archivo de HTML, la hoja de estilos (.css) y archivos de imagen

>[!NOTE]
>
>No hay restricciones en la estructura de archivos .zip. Sin embargo, las referencias deben ser relativas y ajustarse a la estructura de árbol de la carpeta .zip.

_Para importar un archivo que contenga contenido de HTML:_

1. En la página de inicio de Email Designer, seleccione **[!UICONTROL Importar HTML]**.

1. Arrastre y suelte el archivo HTML o .zip que contiene el contenido del HTML y haga clic en [!UICONTROL Importar].

   Cuando finalice la carga de contenido del HTML, el contenido estará en _modo de compatibilidad_. En este modo, solo puede personalizar el texto, agregar vínculos o incluir recursos en el contenido.

### Seleccionar una plantilla

Puede elegir entre:

* Plantillas de muestra. La interfaz de Journey Optimizer ofrece 20 plantillas de correo electrónico predeterminadas entre las que puede elegir.

* Plantillas guardadas.

* Una plantilla personalizada que creó desde cero con el menú _Plantillas_ o que guardó desde un correo electrónico en un recorrido con la opción _[!UICONTROL Guardar como plantilla de contenido]_.

_Para empezar a crear contenido con una de las plantillas de ejemplo o guardadas:_

1. Acceda a _Email Designer_ desde el área de trabajo de edición de contenido de correo electrónico.

   En la página _[!UICONTROL Crear su correo electrónico]_, la pestaña **[!UICONTROL Plantillas de ejemplo]** está seleccionada de forma predeterminada.

1. Para usar una plantilla personalizada, selecciona la pestaña **[!UICONTROL Plantillas guardadas]**.

   Se muestra la lista de todas las plantillas de contenido creadas en la zona protegida actual. Puede ordenarlos por nombre, última modificación o última creación.

1. Seleccione la plantilla que desee en la lista.

1. Después de seleccionar una categoría, puede desplazarse entre todas las plantillas de dicha categoría (de ejemplo o guardadas según su selección) utilizando las flechas derecha e izquierda.

1. Haga clic en **[!UICONTROL Usar esta plantilla]** en la parte superior derecha de la página.

1. Edite el contenido según sea necesario en _Email Designer_.

## Comprobación de alertas

Al diseñar el contenido del mensaje de correo electrónico, se muestran alertas en la interfaz (parte superior derecha de la página) cuando falta la configuración clave.

Si no ve este botón, no se detectan problemas.

Se pueden detectar dos tipos de alertas:

* **_Advertencias_** que hacen referencia a recomendaciones y prácticas recomendadas, como:

   * `The opt-out link is not present in the email body`: se recomienda agregar un vínculo para darse de baja al cuerpo del correo electrónico.

     >[!NOTE]
     >
     >Los mensajes de correo electrónico de estilo marketing deben incluir un vínculo de no participación, que no es necesario para los mensajes transaccionales.

   * `Text version of HTML is empty`: no olvide definir una versión de texto de su cuerpo del correo electrónico, que se utiliza cuando no se puede mostrar el contenido del HTML.

   * `Empty link is present in email body`: compruebe que todos los vínculos del correo electrónico sean correctos.

   * `Email size has exceeded the limit of 100KB`: para una entrega óptima, asegúrese de que el tamaño del correo electrónico no supere los 100 KB.

* **_Errores_** que impiden probar o activar el recorrido o la campaña siempre y cuando no se resuelvan, como:

   * `The subject line is missing`: la línea de asunto del correo electrónico es obligatoria.

   * `The email version of the message is empty`: este error se muestra cuando no se ha configurado el contenido del correo electrónico.

## Comprobación y prueba del correo electrónico

Cuando se define el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo, enviar pruebas y controlar su renderización en clientes populares de escritorio, móviles y basados en web. Si ha insertado contenido personalizado, puede obtener una vista previa de cómo se muestra este contenido en el mensaje mediante los datos del perfil de prueba.

Para obtener una vista previa del contenido del correo electrónico, haga clic en **[!UICONTROL Simular contenido]** y, a continuación, agregue un perfil de prueba para comprobar el mensaje mediante los datos del perfil de prueba.

![Simule el contenido del correo electrónico para comprobar su diseño](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
