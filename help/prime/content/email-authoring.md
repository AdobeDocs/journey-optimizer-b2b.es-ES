---
title: Creación del correo electrónico
description: Utilice las herramientas de diseño de correo electrónico de Journey Optimizer B2B Prime, incluidas las plantillas de correo electrónico, los fragmentos, la personalización, las temáticas, el modo oscuro y la validación.
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '2710'
ht-degree: 1%

---

# Creación del correo electrónico

En [!DNL Adobe Journey Optimizer B2B Edition] Prime, el espacio de diseño de correo electrónico proporciona un lienzo visual en el que los especialistas en marketing componen el correo electrónico. Las herramientas de diseño de correo electrónico de los paneles izquierdo y superior (estructuras, componentes de contenido, plantillas, fragmentos y mucho más) admiten la creación desde cero con la función de arrastrar y soltar. También puede elegir comenzar desde una plantilla, pegar HTML sin procesar o ensamblar mensajes a partir de fragmentos visuales reutilizables.

>[!IMPORTANT]
>
>Para obtener información sobre la configuración de administrador de subdominios, autenticación, grupos de IP y configuraciones de canal de correo electrónico, consulte [Capacidad de entrega de correo electrónico y configuración de canal](../admin/configuration-email-deliverability.md).

En [!DNL Journey Optimizer B2B Edition] Prime, cada correo electrónico está asociado con una acción _[!UICONTROL Enviar correo electrónico]_ dentro de un recorrido. El flujo de trabajo completo, desde el diseño del recorrido hasta la definición de correo electrónico, se produce en una experiencia continua. Cuando [agregue un nodo _Enviar correo electrónico_](../marketing/person-journey-nodes.md#add-an-action-node) a un recorrido de persona, haga clic en **[!UICONTROL Crear correo electrónico]** para iniciar el proceso de diseño del contenido del correo electrónico.



Esta acción inicia las herramientas de diseño de correo electrónico, donde puede elegir cómo desea diseñar el correo electrónico entre las siguientes opciones:

* [Diseñe su correo electrónico desde cero](#design-your-email-from-scratch) con la interfaz de diseño visual. Cree el componente Diseño de correo electrónico mediante arrastrar y soltar en un lienzo en blanco. Este método es mejor para crear nuevas plantillas o correos electrónicos únicos.

* [Codifique o pegue su HTML sin procesar](#html) en el editor de código o trabaje en paralelo con el lienzo visual.

  <!-- Full HTML import workflow with .html and .zip uploads is on the Beta roadmap. -->

* [Seleccione una plantilla existente](#select-a-template) de una lista de plantillas de correo electrónico integradas o personalizadas. Este método es mejor para casos de uso de correo electrónico repetibles.

<!-- * Upload a design prototype (JPG, PNG, PDF, or Figma export) and have AI Assitant convert it into a responsive HTML email. (Image to HTML (Img2HTML) -->

## Herramientas de diseño de correo electrónico

* **Barra de herramientas superior:** Guardar, Atrás, Cambiar al editor de código, controles de vista previa.
* **Carril izquierdo:** estructuras (diseños de columna), contenido (texto, botón, imagen, divisor, social, HTML), fragmentos, plantillas, árbol de navegación (jerarquía de estilo DOM del correo electrónico).
* **Lienzo central:** editor de WYSIWYG con vista previa para escritorio y móvil.
* **Carril derecho:** Configuración y estilos para el componente seleccionado actualmente, incluidas las propiedades de contenido, el fondo, el borde, el relleno y la personalización.

## Creación de un correo electrónico a partir de un recorrido {#email-from-journey}

1. Haga clic en el botón **[!UICONTROL Editar correo electrónico]** para continuar con el paso de configuración del correo electrónico.
1. En la pantalla siguiente, selecciona una configuración de canal creada previamente en la lista desplegable **[!UICONTROL Configuración de correo electrónico]**. Solo se muestran las configuraciones activas.
1. Introduzca una Label para la acción (visible en el lienzo del recorrido) y un Email name interno.
1. Introduzca la línea Subject.
1. Alternativamente, **[!UICONTROL Habilite el seguimiento de URL]** para este nodo de correo electrónico.
1. Haga clic en **[!UICONTROL Editar contenido]** para abrir el espacio de diseño de correo electrónico.

### La pantalla Editar contenido {#edit-content-screen}

Desde esta pantalla, puede confirmar los detalles del remitente (heredados de la configuración del canal), definir la línea de asunto y abrir el espacio de diseño de correo electrónico para crear el cuerpo. El preencabezado está configurado en el espacio de diseño del correo electrónico (consulte [Configuración del preencabezado](#preheader)).

* **Nombre del remitente, Correo electrónico del remitente, CCO:** Heredado de la configuración del canal. Sólo lectura en esta pantalla.
* **Se requiere la línea de asunto:**. Personalization es compatible.
* **Editar cuerpo del correo electrónico:** Abre el espacio de diseño del correo electrónico.

>[!NOTE]
>
>El tamaño del correo electrónico tiene un límite de 100 KB por práctica recomendada de ISP. Prime le advierte en el editor si supera este límite. Los errores (falta asunto, falta cuerpo, configuración de canal eliminada) impiden que el recorrido se active hasta que se resuelvan.

## Diseño desde cero {#design-from-scratch}

### Paso a paso: crear un correo electrónico desde cero {#build-from-scratch}

1. En el nodo de correo electrónico de recorrido, haga clic en **[!UICONTROL Editar contenido]** → **[!UICONTROL Editar cuerpo del correo electrónico]**.
1. En la pantalla Crear tu correo electrónico, haz clic en **[!UICONTROL Diseñar desde cero]**.
1. Haz clic en **[!UICONTROL Confirmar]** para abrir un lienzo en blanco.
1. Desde el carril izquierdo, arrastre una **[!UICONTROL Estructura]** (columna 1, columna 1:1, columna 2:2, columna n:n) al lienzo.
1. Arrastre los componentes **[!UICONTROL Contenido]** a las columnas de la estructura: Texto, Botón, Imagen, Divisor, Social, HTML.
1. Haga clic en cualquier componente del lienzo para seleccionarlo. El carril derecho muestra las pestañas Configuración y Estilos.
1. Use la ficha **[!UICONTROL Configuración]** para configurar opciones específicas del componente (contenido de texto, origen de imagen, dirección URL del botón).
1. Use la ficha **[!UICONTROL Estilos]** para configurar el relleno, el borde, el fondo, la fuente y el color.
1. Utilice el icono **[!UICONTROL Árbol de navegación]** en el carril izquierdo para saltar entre los componentes de un correo electrónico anidado en profundidad.
1. Cambie entre la vista previa para escritorio y la vista previa para móvil mediante los iconos de la barra de herramientas superior.
1. Haz clic en **[!UICONTROL Guardar]** (o usa la lista desplegable Guardar para ver opciones de guardado adicionales).
1. Haga clic en **[!UICONTROL Atrás]** para volver a las propiedades de correo electrónico.

### Componentes de contenido disponibles {#content-components}

| Componente | Descripción |
| --------- | ----------- |
| **Texto** | Texto enriquecido con formato (negrita, cursiva, tamaño de fuente, color, alineación, listas, vínculos). |
| **Botón** | CTA activo. Admite el color de fondo, el borde, el relleno, el comportamiento de desplazamiento y las direcciones URL personalizadas. |
| **Imagen** | Inserte desde Marketo Design Studio (selector de recursos). Admite texto alternativo, alineación, seguimiento de vínculos y clics. |
| **Divisor** | Regla horizontal con grosor y color configurables. |
| **Social** | Iconos de medios sociales prediseñados con configuración de vínculo. |
| **HTML** | Bloque de HTML sin procesar para contenido avanzado. Útil para incrustar marcado codificado a mano. |

### Estructuras y diseños de columna {#structures}

Las estructuras definen la cuadrícula de columnas del correo electrónico. Las estructuras disponibles incluyen: 1 columna, 1:1 (dos columnas iguales), 1:2 / 2:1 (dos columnas asimétricas), 1:1:1 (tres columnas iguales) y n:n (varias columnas personalizadas). Utilice estructuras para controlar cómo fluye el contenido en los dispositivos móviles: la mayoría de las estructuras se contraen a una sola columna en pantallas estrechas de forma predeterminada.

>[!TIP]
>
>Mantenga una estructura de correo electrónico sencilla. Los diseños de dos o tres columnas proporcionan una representación coherente en todos los clientes de correo electrónico (especialmente Outlook y Gmail). Las estructuras profundamente anidadas pueden resultar impredecibles.

### Configuración del preencabezado {#preheader}

El preencabezado es el fragmento de texto que se muestra después de la línea de asunto en las vistas previas de la bandeja de entrada. En Prime, el preencabezado se configura en el lienzo visual en el espacio de diseño del correo electrónico, no en la pantalla de propiedades de correo electrónico junto a la línea de asunto.

1. Abra el correo electrónico en el espacio de diseño del correo electrónico.
1. En el lienzo, busque el área de preencabezado en la parte superior del cuerpo del correo electrónico.
1. Haga clic en la región de texto de preencabezado e introduzca la copia de preencabezado.
1. Aplique los tokens de formato y personalización según sea necesario mediante los controles de texto enriquecido.
1. Haga clic en **[!UICONTROL Guardar]**.

>[!TIP]
>
>Mantenga el encabezado previo entre 40 y 100 caracteres. Debe complementar la línea de asunto (no repetirla) y dar al destinatario un motivo adicional para abrir el correo electrónico.

## Uso de plantillas {#templates}

Las plantillas son diseños de correo electrónico reutilizables. Aceleran la creación de correos electrónicos, refuerzan la coherencia de la marca y facilitan la colaboración en equipo.

### Tipos de plantilla

* **Plantillas de muestra (listas para usar).** Alrededor de 20 plantillas listas para usar que cubren casos de uso comunes (divulgación basada en cuentas, invitaciones a eventos, nutrición, anuncios de productos). Disponible inmediatamente para cada cliente.
* **Plantillas guardadas (personalizadas).** Plantillas creadas por su equipo: o bien creadas desde cero en **[!UICONTROL Administración de contenido]** → **[!UICONTROL Plantillas]**, o bien guardadas de un correo electrónico existente usando la opción &quot;Guardar como plantilla&quot;.

### Paso a paso: crear un correo electrónico a partir de una plantilla {#create-from-template}

1. En el nodo de correo electrónico de recorrido, haga clic en **[!UICONTROL Editar contenido]** → **[!UICONTROL Editar cuerpo del correo electrónico]**.
1. En la pantalla Crear su correo electrónico, la ficha **[!UICONTROL Plantillas de ejemplo]** está seleccionada de forma predeterminada.
1. Examine la galería. Utilice el cuadro de búsqueda para filtrar por nombre o categoría.
1. Cambie a la pestaña **[!UICONTROL Plantillas guardadas]** para ver las plantillas creadas por su equipo.
1. Haga clic en una miniatura de plantilla para previsualizarla.
1. Haga clic en **[!UICONTROL Usar esta plantilla]** para aplicarla. El contenido de la plantilla se abre en el lienzo en el espacio de diseño del correo electrónico.
1. Personalice el texto, las imágenes y los vínculos. La estructura heredada de la plantilla se puede modificar como un correo electrónico desde cero.
1. Haga clic en **[!UICONTROL Guardar]** → **[!UICONTROL Atrás]** para volver a las propiedades de correo electrónico.

### Paso a paso: creación de una plantilla reutilizable {#create-reusable-template}

1. Vaya a **[!UICONTROL Administración de contenido]** → **[!UICONTROL Plantillas]**.
1. Haga clic en **[!UICONTROL Crear plantilla]**.
1. Introduzca un nombre y una descripción. Seleccione **[!UICONTROL Correo electrónico]** como canal.
1. Haga clic en **[!UICONTROL Crear]**. El espacio de diseño de correo electrónico se abre para editarlo.
1. Genere la plantilla (desde cero, desde una plantilla existente o pegando HTML).
1. Habilite **[!UICONTROL Configuración de administración]** de forma opcional:
   * Permitir la edición de estructura y contenido: controla si los autores de correo electrónico pueden cambiar la estructura de la plantilla o solo su contenido.
   * Bloquear componentes específicos: haga que los componentes individuales sean de solo lectura cuando se utilicen en un correo electrónico.
1. Haga clic en **[!UICONTROL Guardar]**. La plantilla ahora está disponible para todos los usuarios en la galería Plantillas guardadas.

### Paso a paso: guardar un correo electrónico como plantilla {#save-as-template}

1. Abra un correo electrónico existente en el espacio de diseño de correo electrónico.
1. En el menú desplegable **[!UICONTROL Guardar]**, haga clic en **[!UICONTROL Guardar como plantilla]**.
1. Introduzca un nombre y una descripción.
1. Si lo desea, configure Governance.
1. Haga clic en **[!UICONTROL Guardar]**.

>[!NOTE]
>
>Las plantillas guardadas y su contenido de correo electrónico son independientes. La edición de una plantilla no actualiza de forma retroactiva los correos electrónicos creados a partir de ella. Para propagar los cambios en muchos correos electrónicos, utilice Fragmentos visuales en lugar de plantillas.

## Fragmentos visuales {#visual-fragments}

Un fragmento visual es un bloque de contenido reutilizable (un encabezado, pie de página, CTA, exención de responsabilidad legal, conjunto de vínculos sociales) que se puede insertar en muchos correos electrónicos. Al actualizar un fragmento, el cambio se propaga automáticamente a todos los correos electrónicos que lo utilicen. Los fragmentos son la forma recomendada de aplicar coherencia de marca y centralizar las actualizaciones de contenido.

### Paso a paso: crear un fragmento visual {#create-fragment}

1. Vaya a **[!UICONTROL Administración de contenido]** → **[!UICONTROL Fragmentos]**.
1. Haga clic en **[!UICONTROL Crear fragmento]**.
1. Seleccione **[!UICONTROL Fragmento visual]** como tipo. Introduzca un nombre y una descripción.
1. Haga clic en **[!UICONTROL Crear]**. El espacio de diseño de correo electrónico se abre para editarlo.
1. Arrastre estructuras y componentes de contenido al lienzo para crear el fragmento (por ejemplo, una estructura de 1 columna con una imagen de logotipo, un encabezado y una lista de vínculos de navegación).
1. (Opcional) Marque los campos como **[!UICONTROL Editables]** para que se puedan personalizar por uso:
   * Seleccione un componente y, a continuación, en el carril derecho, abra la sección **[!UICONTROL Campos editables]**.
   * Añada campos con valores predeterminados (por ejemplo, un campo de fuente de imagen con una URL de logotipo predeterminada, un campo de texto con un titular predeterminado).
   * Los autores de correo electrónico que utilizan el fragmento pueden anular estos campos sin romper la estructura del fragmento.
1. Haga clic en **[!UICONTROL Guardar]**.

### Paso a paso: insertar un fragmento en un correo electrónico {#insert-fragment}

1. Abra el correo electrónico en el espacio de diseño del correo electrónico.
1. En el carril izquierdo, haga clic en **[!UICONTROL Fragmentos]**.
1. Busque el fragmento deseado o haga una búsqueda.
1. Arrastre el fragmento al lienzo en la ubicación deseada.
1. Si el fragmento tiene campos editables, configure los valores en el carril derecho.
1. Haga clic en **[!UICONTROL Guardar]**.

>[!TIP]
>
>Utilice fragmentos para cualquier contenido que deba ser coherente en todos los correos electrónicos: encabezado de marca, pie de página legal, barra de vínculos sociales, bloque de cancelación de suscripción. Cuando el equipo jurídico actualiza la exención de responsabilidad, cambia un fragmento y se actualizan todos los correos electrónicos.

## Personalización {#personalization}

Prime utiliza la sintaxis Handlebars para la personalización. Los tokens se sustituyen en el momento del envío con valores de los datos de perfil de cada destinatario.

### Donde puede personalizar

* **Línea de asunto**: el punto de personalización más común.
* **Preheader**: se establece dentro del lienzo visual; admite tokens de atributos de perfil.
* **Texto del cuerpo del correo electrónico**: nombres y otros atributos de perfil insertados en línea.
* **URL de botón** — anexar parámetros por destinatario.

>[!NOTE]
>
>En esta versión solo están disponibles los atributos de perfil en el Editor de Personalization.

### Paso a paso: inserción de un token de personalización {#insert-token}

1. En el espacio de diseño de correo electrónico (o en la pantalla de propiedades de correo electrónico de la línea de asunto), haga clic en el campo donde desee insertar un token.
1. Haga clic en el icono de personalización (con frecuencia denominado **[!UICONTROL Abrir cuadro de diálogo de personalización]** o **[!UICONTROL Agregar expresión]**).
1. En el cuadro de diálogo de personalización, examine el árbol de esquema de la izquierda. Se muestran los atributos de perfil (nombre, apellidos, correo electrónico, cargo y otros campos de perfil).
1. Seleccione un atributo. Prime inserta la expresión Handlebars correspondiente; por ejemplo, `{{profile.firstName}}`.
1. Agregue un valor de reserva para controlar los datos que faltan: `{{profile.firstName | default: "there"}}`.
1. Haga clic en **[!UICONTROL Confirmar]** o **[!UICONTROL Insertar]**. La expresión aparece en línea en el campo.

### Patrones de personalización comunes {#personalization-patterns}

Utilice expresiones Handlebars como las siguientes (la personalización utiliza la misma sintaxis descrita en [Paso a paso: inserte un token de personalización](#insert-token)):

* **`{{profile.lastName}}`** — inserta el apellido del destinatario.
* **`{{profile.jobTitle}}`** — Hacer referencia al cargo del destinatario en la copia de cuerpo.
* **`{{profile.firstName}}, ready to take the next step?`** — Combina token y texto estático en línea.

Para un saludo de nombre con una alternativa cuando falte el valor, use el asistente `default` como se muestra en los pasos de personalización anteriores (por ejemplo, nombre con el valor predeterminado `"there"`).

## Adición de recursos desde Marketo Design Studio {#marketo-assets}

Prime hace que los recursos existentes de Marketo Design Studio estén disponibles en el espacio de diseño de correo electrónico. Puede examinar e insertar estas imágenes en los correos electrónicos directamente desde el selector de recursos.

>[!IMPORTANT]
>
>La disponibilidad de los recursos en Prime se basa en **una copia única** de los recursos de Marketo Design Studio. Volver a cargar o modificar recursos en Marketo después de la copia inicial **no** se reflejará en Prime. En esta versión tampoco se admiten las cargas de imágenes directamente a Prime. La administración nativa de recursos digitales en Prime, incluida la carga, la navegación, la búsqueda y la edición de imágenes, forma parte del ámbito de Beta.

### Tipos de archivos compatibles {#asset-file-types}

* **Totalmente compatible (visible en el selector, incrustable en línea):** JPG, PNG, GIF, WebP.
* **Accesible con advertencias:** SVG (con una advertencia de que algunos clientes de correo electrónico no procesan SVG).
* **No se admite en esta versión:** TIFF, PDF, DOCX, XLSX, PPTX, CSS, JS, HTML, TXT, archivos binarios, PSD, AI, INDD.

### Insertar una imagen de Marketo Design Studio {#insert-image}

1. En el espacio de diseño del correo electrónico, arrastre un componente de contenido **[!UICONTROL Image]** al lienzo (o haga clic en una imagen existente para reemplazarla).
1. En el carril derecho, haga clic en **[!UICONTROL Marketo Engage Assets]**.
1. Se abre el selector de recursos. Examine carpetas o busque por nombre de archivo.
1. Seleccione el recurso que desee.
1. Haga clic en **[!UICONTROL Seleccionar]**. La imagen se inserta en el correo electrónico desde la copia del recurso disponible en Prime.
1. En el carril derecho, configure lo siguiente:
   * Texto alternativo (recomendado para accesibilidad y para clientes que bloquean imágenes de forma predeterminada).
   * Alineación.
   * Destino del vínculo: haga que la imagen sea seleccionable.
1. Haga clic en **[!UICONTROL Guardar]**.

## Temas y modo oscuro {#themes-dark-mode}

### Temas {#themes}

Un tema es un ajuste preestablecido de estilo reutilizable que define colores, tipografía, espaciado, estilos de botón y divisores. Aplique un tema a un correo electrónico para aplicar instantáneamente el estilo de marca en todos los componentes.

Para aplicar o editar temáticas:

1. En el espacio de diseño del correo electrónico, haga clic en **[!UICONTROL Temas]** (en la barra de herramientas superior o en el carril derecho, según la vista).
1. Elija **[!UICONTROL Aplicar tema]** para seleccionar un tema existente o **[!UICONTROL Crear nuevo tema]** para definir una paleta de marca.
1. Personalice colores, fuentes y estilos de nivel de componente. Se admiten las variantes claro/oscuro.
1. Se aplican de forma global; las anulaciones locales por componente siguen siendo posibles.
1. Cambie la temática más tarde para cambiar la marca sin volver a crear.

### Modo oscuro {#dark-mode}

Se admite el procesamiento en modo oscuro mediante consultas de medios CSS `prefers-color-scheme`. Las herramientas de diseño de correo electrónico incluyen una previsualización en modo oscuro por cliente de correo electrónico para ayudar a los autores a validar que el texto sigue siendo legible, los logotipos no desaparecen y los colores de la marca se mantienen contra fondos oscuros.

Para obtener una vista previa del modo oscuro, haga clic en el botón de alternancia de modo oscuro en los controles de vista previa del lienzo.

>[!TIP]
>
>Problemas comunes del modo oscuro: los logotipos oscuros desaparecen en los fondos oscuros, el texto de bajo contraste y los colores invertidos en las imágenes transparentes. Previsualice siempre el correo electrónico en modo oscuro antes de guardar la versión final.

## Validación del contenido de correo electrónico {#validation}

Antes de activar el recorrido, el contenido del correo electrónico debe ser válido. Prime muestra alertas de nivel de contenido en el correo electrónico y en el lienzo del recorrido. Esta sección trata sobre las alertas que puede ver y cómo resolverlas.

### Alertas de contenido comunes y cómo resolverlas {#content-alerts}

| Alerta | Lo que significa | Cómo resolver |
| ----- | ------------- | -------------- |
| **Falta la línea de asunto** | El campo Subject line está vacío. | Abra el correo electrónico e introduzca una línea de asunto en la pantalla Editar contenido. Se permiten tokens de Personalization, pero el campo no puede estar vacío. |
| **El cuerpo del correo electrónico está vacío** | El lienzo del espacio de diseño del correo electrónico no tiene contenido. | Haga clic en **[!UICONTROL Editar cuerpo del correo electrónico]** para abrir el espacio de diseño del correo electrónico. Arrastre al menos un componente Estructura y un componente Contenido al lienzo y haga clic en Guardar. |
| **Configuración de canal no seleccionada** | No se ha elegido ninguna configuración de correo electrónico para el nodo de correo electrónico. | En la pantalla de propiedades de correo electrónico, selecciona una configuración de Active channel en la lista desplegable **[!UICONTROL Configuración de correo electrónico]**. |
| **Configuración de canal eliminada** | La configuración de canal seleccionada anteriormente se ha eliminado o ya no está activa. | Abra las propiedades de correo electrónico y seleccione otra configuración de Active channel. Si no hay ninguno disponible, un administrador debe crear o reactivar uno. |
| **El tamaño del correo electrónico supera los 100 KB** | El tamaño total del correo electrónico (HTML, CSS en línea, contenido codificado) es mayor que el límite de las prácticas recomendadas del ISP de 100 KB. | Reduzca el tamaño del correo electrónico: reemplace las imágenes en línea grandes con imágenes alojadas externamente de Marketo Design Studio, elimine los CSS en línea no utilizados y simplifique las estructuras anidadas. |
| **Token de personalización sin resolver** | Un token de Handlebars hace referencia a un atributo de perfil sin reserva y es posible que falte el atributo para algunos destinatarios. | Agregue una reserva utilizando el asistente de Handlebars `default` como se describe en [Personalization](#personalization). Como alternativa, restrinja la audiencia de recorrido a perfiles en los que el atributo esté garantizado. |
| **Imagen no cargada** | Un componente de imagen hace referencia a un recurso que ya no está disponible. | Haga clic en la imagen, abra el selector de recursos y vuelva a seleccionar el recurso en Marketo Design Studio. |

### Paso a paso: revisar y resolver alertas {#resolve-alerts}

1. Abra el recorrido que contiene el nodo de correo electrónico. Los nodos de correo electrónico con alertas sin resolver se marcan con un distintivo rojo en el lienzo.
1. Haga clic en el nodo de correo electrónico para abrir el carril de propiedades.
1. Revise la sección **[!UICONTROL Alertas]** en el carril de propiedades. Cada alerta se vincula al campo o pantalla donde se puede resolver el problema.
1. Resuelva cada alerta a su vez; por ejemplo, introduzca la línea de asunto que falta, seleccione una configuración de canal o abra el espacio de diseño de correo electrónico para corregir el contenido.
1. Después de resolver todas las alertas, haga clic en **[!UICONTROL Guardar]** en el nodo de correo electrónico.
1. Confirme el distintivo rojo cuando se borre el nodo del correo electrónico.

>[!NOTE]
>
>Las alertas deben borrarse antes de que pueda continuar el recorrido. Las advertencias no son de bloqueo, pero deben revisarse (por ejemplo, un correo electrónico que utilice un token sin reserva puede procesarse con valores vacíos para algunos destinatarios).
