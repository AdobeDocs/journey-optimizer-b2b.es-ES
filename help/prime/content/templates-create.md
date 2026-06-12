---
title: Crear plantillas de correo electrónico
description: 'Aprenda a crear plantillas de correo electrónico en Journey Optimizer B2B Prime: diseñe desde cero, guarde un correo electrónico de un recorrido como plantilla o convierta una imagen de diseño en una plantilla de correo electrónico.'
badgeBeta: label="Beta" type="informative" tooltip="Esta función forma parte de una versión beta limitada."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---


# Crear plantillas de correo electrónico

Puede crear una plantilla de correo electrónico en [!DNL Journey Optimizer B2B Edition Prime] de tres maneras:

* **Diseñar desde cero**: cree una nueva plantilla en la biblioteca de plantillas con el espacio de diseño visual de correo electrónico.
* **Guardar desde un correo electrónico de recorrido**: guarde un correo electrónico que haya creado en un recorrido como una plantilla reutilizable.
* **Convertir una imagen**: cargue una imagen de diseño y use IA generativa para convertirla en una plantilla de correo electrónico editable.

>[!NOTE]
>
>En esta versión de Beta, solo se admiten plantillas de correo electrónico.

## Diseño de una plantilla desde cero {#design-from-scratch}

1. Vaya a **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas]**.
1. Haga clic en **[!UICONTROL Crear plantilla]**.
1. Escriba un **[!UICONTROL nombre de plantilla]** y una **[!UICONTROL descripción]** opcional.
1. Si lo desea, puede añadir etiquetas para categorizar la plantilla.
1. Haga clic en **[!UICONTROL Crear]** para abrir el espacio de diseño de correo electrónico.
1. Diseño del diseño del correo electrónico con estructuras y componentes de contenido. Para obtener una referencia completa sobre las herramientas disponibles, consulte [Creación de correo electrónico](email-authoring.md).
1. Si lo desea, puede configurar [bloqueo de contenido](template-content-locking.md) para restringir qué partes de la plantilla pueden editar los autores al usarla en un recorrido.
1. Haga clic en **[!UICONTROL Guardar]**.

## Guardar un correo electrónico de recorrido como plantilla {#save-as-template}

Cuando diseñe un correo electrónico en un recorrido que desee reutilizar, guárdelo directamente en la biblioteca de plantillas desde el espacio de diseño de correo electrónico.

1. En el espacio de diseño del correo electrónico, abra la lista desplegable **[!UICONTROL Guardar]** en la parte superior del editor.
1. Seleccione **[!UICONTROL Guardar como plantilla de contenido]**.
1. Escriba un **[!UICONTROL nombre de plantilla]** y una **[!UICONTROL descripción]** opcional.
1. Opcionalmente, agregue etiquetas y configure [bloqueo de contenido](template-content-locking.md).
1. Haga clic en **[!UICONTROL Guardar]**.

El correo electrónico de recorrido original no se ve afectado. La plantilla guardada está disponible en la biblioteca de plantillas para todos los usuarios de la zona protegida.

## Convertir una imagen en una plantilla {#image-to-template}

[!DNL Journey Optimizer B2B Edition Prime] puede convertir una imagen estática, como una maqueta de Figma o Photoshop, en una plantilla de correo electrónico editable mediante IA generativa. Esto elimina la necesidad de volver a generar manualmente los diseños a partir de archivos de diseño.

### Requisitos

Antes de empezar:

* Su organización debe haber firmado el anexo de IA generativa con Adobe.
* Debe tener el permiso **[!UICONTROL Generar contenido]** además de **[!UICONTROL Administrar plantillas de contenido]**.
* El archivo de imagen debe cumplir estas especificaciones:
   * Formato: JPEG (.jpg, .jpeg) o PNG (.png)
   * Tamaño máximo de archivo: 10 MB
   * Anchura recomendada: 600-800 píxeles
   * Imagen clara y de alta calidad con texto legible y distintos elementos visuales

>[!IMPORTANT]
>
>La imagen no debe contener información de identificación personal (PII) ni datos confidenciales.

### Convertir una imagen

1. Vaya a **[!UICONTROL Administración de contenido]** > **[!UICONTROL Plantillas]**.
1. Haga clic en **[!UICONTROL Convertir imagen en plantilla]** en el encabezado.
1. Escriba un **[!UICONTROL nombre de plantilla]** y una **[!UICONTROL descripción]** opcional.
1. Si lo desea, seleccione **[!UICONTROL Tema de marca]** para aplicar los colores, las fuentes y el espaciado de su marca a la salida generada.
1. Cargue la imagen mediante arrastrar y soltar o el explorador de archivos.
1. Confirme que la imagen no contiene datos personales.
1. Revise y acepte las Directrices del usuario de IA generativa de Adobe (solo la primera vez).
1. Haga clic en **[!UICONTROL Convertir]**.

   La conversión suele completarse en cinco minutos. Las imágenes complejas o grandes pueden tardar hasta diez minutos. Puede salir, el proceso continúa en segundo plano.

1. Cuando finalice la conversión, haga clic en el nombre de la plantilla para previsualizar y editar el contenido generado.

>[!NOTE]
>
>El resultado no se muestra automáticamente. Actualice la página o vuelva a la biblioteca de plantillas para ver la plantilla completada.

### Editar tras la conversión

La plantilla convertida se abre en el espacio de diseño de correo electrónico como un correo electrónico totalmente editable. Utilice las herramientas de diseño estándar para lo siguiente:

* Edite texto y agregue [tokens de personalización](email-authoring.md#personalization).
* Actualizar o reemplazar imágenes y agregar vínculos.
* Ajustar colores, fuentes y espaciado.
* Agregar, quitar o reorganizar componentes de contenido.
* Configurar [bloqueo de contenido](template-content-locking.md).

>[!IMPORTANT]
>
>La IA generativa produce una HTML estática basada en la imagen visual. Revise todo el texto para comprobar su precisión y agregue personalización, contenido dinámico y seguimiento manualmente después de la conversión.

La plantilla convertida se guarda automáticamente en la biblioteca de plantillas cuando se completa la conversión.

### Sugerencias para obtener mejores resultados

Siga estas directrices para obtener los mejores resultados de la conversión de imagen a plantilla:

**Antes de la conversión:**

* Utilice la versión de mayor resolución del archivo de diseño.
* Diseñe con anchuras de correo electrónico estándar (600-800 píxeles) e incluya el diseño completo (de encabezado a pie de página) en una sola imagen.
* Asegúrese de que haya suficiente contraste entre el texto y los fondos y utilice tamaños de fuente legibles.

**Diseño para una conversión precisa:**

* Utilice diseños sencillos y bien estructurados con una clara separación entre las secciones.
* Siga los patrones de correo electrónico estándar (encabezado, cuerpo, llamadas a la acción, pie de página) en lugar de diseños complejos de varias capas.
* Mantenga los elementos visuales distintos para que la IA pueda identificar correctamente los límites estructurales.

**Después de la conversión:**

* Pruebe el procesamiento en clientes de correo electrónico y dispositivos antes de utilizar la plantilla en un recorrido.
* Compruebe la alineación con los colores de marca, las fuentes y las directrices de estilo.
* Revise y mejore la accesibilidad, incluido el texto alternativo de la imagen.
