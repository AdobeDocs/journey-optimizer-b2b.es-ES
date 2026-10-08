---
applyTo: "**/*.md"
source-git-commit: 0f90b37c1ed8e4da0840f64179a0e99e0fe786d7
workflow-type: tm+mt
source-wordcount: '5174'
ht-degree: 1%
---

# Documentación de Adobe Experience League: instrucciones de código de Claude

Está ayudando a un redactor técnico en el repositorio de documentación pública de Adobe Experience League (`journey-optimizer-b2b.en`). Cada parte del contenido que elabore, edite o revise DEBE seguir todas las reglas que se indican a continuación. Si tiene dudas acerca de la terminología, consulte las wikis a las que se hace referencia mediante la herramienta MCP de confluencia (`mcp__adobe-wiki-confluence`).

&#x200B;---

## &#x200B;1. Voz, tono y estilo

### Escritura centrada en el usuario

Centrar al usuario, no la función. Escriba lo que el usuario puede **hacer**, no lo que hace la característica.

- Use una segunda persona (&quot;usted&quot;) y un estado de ánimo imperativo para obtener instrucciones.
- Utilice &quot;usted&quot; cuando hable con la audiencia sobre sí mismos, no &quot;usuarios&quot;. &quot;Usuarios&quot; es aceptable cuando se hace referencia a una función (por ejemplo, un administrador que administra usuarios).
- EVITE &quot;La función X le permite...&quot; o &quot;La función X le permite...&quot;. Ponga al usuario como sujeto o use un estado de ánimo imperativo.
  - Malo: &quot;La API de servidor se puede utilizar en servidores de&quot;.
  - Bueno: &quot;Usar la API de servidor en servidores&quot;.
  - Malo: &quot;Los campos calculados permiten crear valores...&quot;
  - Bueno: &quot;Utilice campos calculados para crear valores...&quot;
- Ten en cuenta que &quot;puedes&quot;. Es apropiado, pero puede ser usado en exceso, creando oraciones repetitivas o verbales.
- Utilice &quot;seleccionar&quot; para elegir opciones de una lista o resaltar texto. Utilice &quot;click&quot; solo para acciones explícitas del ratón. Evite asignar nombres al tipo de control (botón, vínculo) a menos que sea necesario para la desambiguación.
- Utilice &quot;Abrir&quot; / &quot;Cerrar&quot; para aplicaciones y ventanas o paneles principales.
- Utilice &quot;Salir&quot; para abandonar un sitio o experiencia (por ejemplo, &quot;Salir de Report Builder&quot;).
- Utilice &quot;ir a&quot; o &quot;navegar a&quot; para la navegación.
- Use &quot;Reproducir vídeo&quot;, no &quot;Ver vídeo&quot;. No todo el mundo está mirando.
- Utilice &quot;Ver&quot;, &quot;Mostrar&quot; o &quot;Ir a todos&quot;, no &quot;Ver todos&quot;. No todo el mundo está viendo.
- Utilice &quot;iniciar sesión&quot; / &quot;cerrar sesión&quot;, no &quot;iniciar sesión&quot; / &quot;cerrar sesión&quot;.
- Evite &quot;con el fin de&quot;. En su lugar, utilice &quot;to&quot;.
- Evite utilizar. Utilice &quot;use&quot; en su lugar.
- Evite adjetivos vagos como &quot;rápido&quot; o &quot;fácil&quot;. Sea preciso: &quot;Este proceso suele tardar 5 minutos&quot;.
- Evite los adverbios débiles: muy, extremadamente, increíblemente.

### Estructura de frase y párrafo

- Objetivo ≤20 palabras por frase (la guía de creación indica ≤35 máximo). Un pensamiento por frase.
- Párrafos: máximo 125 palabras, idealmente ≤100. Máximo de 4 a 5 frases. No hay paredes de texto.
- Usa la voz activa. Evite las construcciones y nominalizaciones pasivas (por ejemplo, utilice &quot;crear&quot; en lugar de &quot;creación&quot;).
- Utilice una estructura simple de sujeto-verbo-objeto.
- Evite los temas falsos (&quot;Es...&quot;, &quot;Hay...&quot;).
- Utilice la misma palabra de forma coherente. No girar sinónimos.
- Sin humor, jerga, jerga o ejemplos específicos de la cultura (debe localizarse bien).
- Utilice la coma de Oxford en listas de tres o más elementos.
- Escriba números enteros entre cero y nueve; utilice números para 10 y más.
- Sin punto y coma. Utilice un punto y una nueva oración en su lugar.

### Explorabilidad

- Los lectores deben entender el alcance del artículo solamente desde el título, encabezados y subtítulos.
- Máximo de 2 a 5 subsecciones por sección.
- Dirija 7 pasos por tarea; 10 es el máximo práctico. Dividir procedimientos más largos en subtareas.
- Máximo de 8 elementos por lista con viñetas.
- Utilice tablas cuando faciliten el análisis de las listas de términos y definiciones.
- El contenido debe puntuarse por debajo del grado 10 en una prueba de legibilidad (después de eliminar los sustantivos y títulos adecuados).

### Escritura para la detección de IA

Los asistentes de IA y las herramientas de búsqueda muestran cada vez más el contenido de Experience League en respuestas generadas.

- Coloque términos clave (nombres de productos, nombres de funciones, tareas) en el texto del cuerpo y el texto del vínculo, no solo en imágenes o tablas complejas. Los sistemas de IA dependen del texto legible.
- Escriba títulos y primeros párrafos claros e independientes. Las herramientas de IA a menudo las extraen aisladamente; deben tener sentido sin contexto.
- Utilice frases cortas y directas. La prosa concisa es más fácil de analizar y citar con precisión para la IA.
- Utilice formatos estructurados (pasos numerados, viñetas cortas, encabezados de definición) para procedimientos y comparaciones. La estructura ayuda a la IA a identificar la respuesta correcta.
- Incluya sinónimos o términos alternativos en el primer uso (por ejemplo, &quot;ECID (Experience Cloud ID)&quot;) para mejorar la recuperación de frases de consulta variadas.
- Asegúrese de que los campos de metadatos (título, descripción, etiquetas de función) sean completos y precisos.

&#x200B;---

## &#x200B;2. Sintaxis de Adobe Markdown (Experience League)

### Frontmatter (requerido en cada archivo)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

Campos opcionales adicionales utilizados en este repositorio: `solution`, `type`, `role`, `exl-id`. Coincide con el patrón de los archivos existentes.

**IMPORTANTE:** NO agregue `exl-id` al crear una nueva página. Se genera automáticamente en el momento de la publicación. Solo se deben conservar `exl-id` campos que ya existen en páginas existentes.

**Reglas de metadatos de título:**

- Caso de título (solo se coloca en Experience League que utiliza el caso de título).
- Máximo de 60 caracteres (inglés). El sistema anexa `| Adobe Experience Platform` automáticamente. Conviértalo en longitud.
- NO añada la barra vertical ni el nombre del producto. Se añade automáticamente.
- Considérelo la versión SEO del nombre de su página (lo que buscan los usuarios).
- Título del concepto: frase nominal (por ejemplo, &quot;Informe de vistas de la página&quot;).
- Título de la tarea: frase verbal (por ejemplo, &quot;Crear un segmento para vistas de página&quot;).
- Marketing no aprueba las siglas para la mayoría de los usos, pero un uso limitado es aceptable para SEO, entradas de TDC, metadatos de descripción y encabezados donde la longitud es un problema.

**Reglas de metadatos de descripción:**

- Caso de sentencia. De 150 a 160 caracteres idealmente; 160 máximo.
- Una o dos frases concisas. La primera frase resume, la segunda es un call to action.
- Comience las descripciones de conceptos con &quot;Más información sobre...&quot; o &quot;Comprender...&quot;.
- Comience las descripciones de las tareas con &quot;Aprenda a...&quot; o un verbo imperativo.
- NO comience por el nombre del producto. Comience con un verbo para SEO.
- NO copie el primer párrafo literalmente (propósito diferente).
- Si un campo de metadatos comienza con una etiqueta `[!DNL]` o &grave;&grave;, escriba todo el valor del campo entre comillas o se producirá un error de validación.

### Encabezados

- `#` = H1 (título de artículo, uno por página). `##` = Secciones principales H2. `###` = H3, etc.
- NO omita los niveles de encabezado (por ejemplo, no salte de H2 a H4).
- Objetivo ≤5 palabras. Máximo de 69 caracteres (inglés).
- Línea en blanco antes y después de cada encabezado.
- Cada título debe ir seguido de al menos una frase de texto independiente. NUNCA apile dos encabezados ni coloque una nota, lista o tabla directamente debajo de un encabezado sin tener primero un párrafo.
- Identificadores de anclaje personalizados: `## Section title {#section-id}` (en minúsculas, con guiones, sin puntos).
- Evite los nombres de anclaje que entren en conflicto con JavaScript/CSS: búsqueda, resultados, contenido, encabezado, pie de página, navegación, barra lateral, paginación, etc.
- NO coloque insignias ni elementos de Markdown dentro del texto del encabezado.
- NO utilice encabezados abstractos de una sola palabra como &quot;Información general&quot; o &quot;Introducción&quot; por sí solos. Describa siempre de qué trata la descripción general o la introducción.
- NO numere los H1. Para tutoriales, utilice &quot;Paso 1: ...&quot; en subtítulos en lugar de anclajes numerados.
- Mayúsculas y minúsculas en las frases de todos los encabezados (excepto los sustantivos propios y los elementos de la interfaz de usuario).
- Encabezados del concepto: sustantivos y frases sustantivadas (por ejemplo, &quot;Información general de segmentación&quot;).
- Encabezados de tareas: verbos obligatorios (por ejemplo, &quot;Crear un flujo de trabajo de objetivos&quot;). Evite los gerundios (-ing forms).
- Evite unificar verbos con -ment o -ion (utilice &quot;Crear una hoja de ruta&quot; en lugar de &quot;Creación de hoja de ruta&quot;).
- Mantenga la estructura de encabezados paralela dentro de las secciones.
- No hay ID de anclaje de encabezado duplicados en un documento.
- Si un encabezado incluye números, especifique un identificador de encabezado explícito que no comience con un número (por ejemplo, `## Release notes for 2016 {#release-notes-2016}`).

### Vínculos

- Referencias cruzadas internas: rutas relativas a la raíz que comienzan por `/help/`: `[link text](/help/path/to/file.md)`
- Vínculos profundos a anclajes: `[text](/help/path/to/file.md#anchor-id)`
- Vínculos externos (fuera de este repositorio): `https://` direcciones URL absolutas. Se abren en una pestaña nueva automáticamente.
- Abrir en ficha nueva explícitamente: anexar `{target="_blank"}` (se usa para vínculos entre guías).
- Vínculos de referencia (con el estilo `[1]: url`): solo funcionan con direcciones URL absolutas.
- NO agregue el mismo archivo varias veces en un índice.
- Evite las direcciones URL sin procesar en el texto principal. Utilice siempre un texto de vínculo descriptivo.
- Nunca utilice &quot;haga clic aquí&quot; o &quot;vínculo&quot; como texto del vínculo. Los lectores de pantalla muestran vínculos fuera de contexto y no pueden distinguir varias instancias de &quot;clic aquí&quot;.
- El texto del vínculo debe aclarar el destino por sí solo.
- Para obtener listas de referencias cruzadas &quot;Más información&quot;, utilice un subencabezado `More help on this topic` con una lista con viñetas.

### Imágenes

- Sintaxis: `![alt text](path/to/image.png)`
- Cambiar tamaño: `{width="300"}` o `{width="50%"}`
- Alinear: `{align="center"}` o `{align="right"}`
- Ampliable: `{zoomable="yes"}`
- Visualización modal: `{modal="regular"}`. NO combinar con un vínculo.
- Anchura recomendada: de 640 a 2000 px. Tamaño máximo de archivo: 5 MB recomendado; límite estricto de 100 MB. Máximo de 100 imágenes por artículo.
- Las imágenes van en una subcarpeta `assets/` relativa al archivo Markdown.
- Las imágenes que NO se deben localizar se ubican en una subcarpeta `do-not-localize/`.
- Captura siempre capturas de pantalla con el tema **Claro** en la interfaz de usuario del producto de Experience Cloud, no con el tema Oscuro.
- NO mostrar datos de clientes en las capturas de pantalla.
- NO documente interfaces de terceros en capturas de pantalla. En su lugar, vincule a la documentación propia del tercero.
- NO utilice capturas de pantalla solo para rastrear el progreso a través de las pantallas o mostrar elementos obvios de la interfaz de usuario.
- NO incluya ilustraciones de iconos fácilmente identificables más de una vez por artículo.
- NO utilice imágenes de código. En su lugar, utilice bloques de código.
- NO utilice el color solo para transmitir información (no accesible para los usuarios daltónicos).
- NO utilice gráficos animados que parpadeen más de tres veces por segundo (riesgo de convulsiones).
- Asegúrese de que las imágenes tengan un buen contraste y sean nítidas.
- Directrices de tamaño de píxel de captura de pantalla: 2000 px máximo para grandes, 672 px para medianos, 300 px para pequeños, 30-35 px para iconos.
- Para llamadas: utilice #EB1000 HEX rojos, grosor de línea de 3 píxeles, radio de esquina de 8 píxeles.

### Texto alternativo

Google indexa el texto alternativo y los lectores de pantalla lo leen. Siempre escríbelo con cuidado.

- Describa lo que muestra la imagen, no solo el nombre de pantalla.
- Utilice frases completas con la gramática y la puntuación adecuadas.
- Incluya el texto relevante de la imagen.
- Utilice palabras completas, no abreviaciones. Los lectores de pantalla escriben abreviaturas.
- NO empiece con &quot;Esta imagen muestra...&quot;. Solo tiene que describir el contenido directamente.
- El texto alternativo no suele ser necesario para imágenes puramente decorativas, pero se proporciona cuando hay dudas.

| Texto alternativo correcto | Evitar |
|---|---|
| Captura de pantalla del Generador de audiencias que muestra los filtros demográficos geográficos y de edad seleccionados. | Generador de público |
| Seleccione una extensión del catálogo de extensiones. | Biblioteca de extensiones |

### Vídeos

- Sintaxis: `>[!VIDEO](https://video.tv.adobe.com/v/xxxxx/?quality=12&learn=on)`
- Agregue `?quality=12&learn=on` al final de todas las direcciones URL de vídeo para una mejor reproducción.
- Los vídeos NO deben reproducirse automáticamente. No agregue `?autoplay=true` a la documentación.
- Proporcione siempre una alternativa textual, una transcripción o un vínculo a instrucciones escritas: &quot;Para obtener instrucciones escritas, consulte [vínculo]&quot;.
- Use subtítulos significativos.
- Habilite las transcripciones con `{transcript=true}` en vídeos individuales o agregue `auto-video-transcripts: true` a `TOC.md` para toda la guía.

### Notas y advertencias

```markdown
>[!NOTE]
>
>Note content here.

>[!TIP]
>
>Tip content here.

>[!IMPORTANT]
>
>Important content here.

>[!WARNING]
>
>Warning content here.

>[!CAUTION]
>
>Caution content here.
```

Tipos adicionales: `[!ADMIN]`, `[!AVAILABILITY]`, `[!PREREQUISITES]`, `[!INFO]`, `[!ERROR]`, `[!SUCCESS]`.

Reglas de sintaxis CRÍTICAS:
- DEBE haber una línea `>` en blanco entre la línea de etiqueta y el contenido.
- Cada línea de continuación debe comenzar con `>`.
- Se admite la sintaxis de comilla de bloque (`>` sin etiqueta), pero se representa como una comilla de bloque sin formato. NO lo utilice si espera llamadas con estilo.
- NO agregue comentarios dentro de componentes de bloque, como listas de viñetas, especialmente listas de viñetas anidadas. El comentario puede cambiar el modo en que se procesa la lista.

### Pestañas

```markdown
>[!BEGINTABS]

>[!TAB Tab label]

Tab content here.

>[!TAB Another tab]

More content.

>[!ENDTABS]
```

- NO anide conjuntos de pestañas.
- NO anide conjuntos de pestañas dentro de listas.
- Los títulos de las pestañas no pueden tener formato de negrita o cursiva.
- La búsqueda en la página (Ctrl+F) no encuentra contenido en pestañas ocultas.

### Secciones contraíbles

```markdown
+++Click to expand
Content here.

* Bullet one
* Bullet two

+++
```

- Agregue líneas en blanco encima y debajo de listas y bloques de código dentro de contraíbles.
- NO anide secciones contraíbles dentro de secciones contraíbles.
- Se permiten encabezados dentro de los contraíbles, pero no se recomiendan.
- Nota: Buscar en la página (Ctrl+F) detecta el texto contraído en Chrome, pero no en Safari.

### Cuadros de sombra

```markdown
>[!BEGINSHADEBOX "Optional Title"]

Content with gray background.

>[!ENDSHADEBOX]
```

### Bloques de código

- En línea: una sola comilla invertida `` `code` ``. Se utiliza para nombres de cookies, nombres de archivo, valores, parámetros, comandos y direcciones URL de ejemplo que no deben validarse.
- Bloques delimitados: triples comillas invertidas con identificador de idioma (habilita el resaltado de sintaxis y un botón Copiar).
- Atributos opcionales: `{line-numbers="true"}`, `{start-line="7"}`, `{highlight="11-13, 16"}`
- Los bloques de código NO están localizados. No es necesario agregar DNL o UICONTROL dentro de ellos.
- Utilice comillas invertidas (no comillas) para el código, los nombres de archivo, los parámetros y el texto escrito.
- NO utilice imágenes de código. Utilice siempre bloques de código.

### Insignias

- En línea: `[!BADGE Beta]{type=Informative}`
- Metadatos (por encima de H1): `badgePremium: label="Premium" type="Positive"`
- Tipos: `Informative` (azul), `Positive` (verde), `Negative` (rojo), `Neutral` (gris oscuro), `Caution` (amarillo)
- Máximo de 2 insignias en metadatos por artículo.
- NO coloque insignias en encabezados.
- NO utilice distintivos para información que se vuelva obsoleta rápidamente (por ejemplo, &quot;Nueva&quot;).
- Las etiquetas de distintivo están localizadas. Manténgalos concisos.
- Para el distintivo beta, use solamente frontmatter `badgeBeta`. NO coloque un distintivo en línea en el H1.
- Si desea que se abra una dirección URL de distintivo en una ficha nueva, agregue `newtab=true` a la sintaxis del distintivo.

### Listas

- Use `*` o `-` de forma coherente en un solo artículo. Compruebe la convención del archivo existente. La combinación de marcadores provoca un error de validación.
- Para listas numeradas, use `1.` para cada elemento. GitHub/EDS los numera automáticamente correctamente.
- Listas de viñetas: cuando el orden no es importante. Listas numeradas: para pasos y procedimientos ordenados.
- Para un procedimiento de un solo paso, use una viñeta (`*`) en lugar de `1.`.
- Mantenga las entradas de la lista breves. Generalmente una oración o menos.
- Utilice puntos para frases completas; omita puntos para las entradas de una sola palabra o de frases incompletas (aplique la regla de forma coherente dentro de una lista).
- NO termine elementos de la lista con punto y coma, comas o conjunciones como &quot;y&quot; u &quot;o&quot; cuando los elementos deban leerse como una serie simple.
- Todas las entradas de la lista deben ser paralelas gramaticalmente.
- Sangría del contenido anidado: 3 espacios para listas numeradas, 2 para listas con viñetas.
- Rodee las listas con líneas en blanco.
- NO utilice listas de tareas (casillas de verificación `- [ ]` al estilo de GitHub). No son compatibles con Experience League.

### Tablas

- Utilice tablas de markdown estándar.
- Para diseños complejos (celdas combinadas, bordes separados), se permite HTML `<table>`.
- Rodear tablas con líneas en blanco.
- Utilice `{style="table-layout:auto"}` para tablas de ancho automático cuando sea necesario.
- Evite las capturas de pantalla en celdas de tabla. Se aceptan iconos o miniaturas pequeños en las celdas.

### Previsualizar resaltado de funciones

Utilice un intervalo para el contenido de vista previa en línea y un div para el contenido de vista previa de varios párrafos:

```markdown
<span class="preview">This feature is in limited availability.</span>
```

```markdown
<div class="preview">

Multiple paragraphs of preview content here.

</div>
```

### Fragmentos e incluye

```markdown
{{$include /path/to/snippet.md}}
```

Se utiliza para bloques de contenido reutilizable compartidos en varios artículos.

### Caracteres especiales

- Omitir caracteres especiales del texto independiente con barra invertida: `\#`, `\*`, `\[`, `\]`.
- Usar entidades de HTML para los corchetes angulares: `&lt;`, `&gt;`, `&amp;`.
- Usar entidades de HTML para símbolos especiales: `&reg;`, `&mdash;`, `&ndash;`.

### Comentarios

Use comentarios de HTML para el texto del borrador o notas para otros redactores:

```markdown
<!-- This is a comment. Not rendered in the published doc. -->
```

Los comentarios SON visibles para los usuarios que editan en GitHub.com. NO incluya información confidencial en los comentarios.

NO agregue comentarios dentro de componentes de bloque, como listas de viñetas (especialmente las anidadas). Los comentarios pueden interrumpir la representación de listas. En los archivos TOC.md, no comente las líneas en medio de la lista de TDC: mueva los comentarios al final del archivo.

### Acciones de teclado

Ponga en negrita cada tecla individual de un método abreviado de teclado: **cmd** + **shift** + **p**.

### Nombres de archivos y carpetas

- Nombres de archivo de Markdown: minúsculas con guiones. Sin mayúsculas, guiones bajos, puntos ni espacios.
- Usar slugs descriptivos: `create-calculated-metric.md`, `calculated-metric-overview.md`. Evite nombres de archivo vacíos como `overview.md` o `introduction.md` a menos que el IA requiera un nombre fijo.
- Evite nombres de archivo que entren en conflicto con JavaScript/CSS: `metadata.md`, `search.md`.
- Nombres de archivo del recurso: se prefieren las minúsculas; se permiten mayúsculas y guiones bajos, pero no se recomiendan.

&#x200B;---

## &#x200B;3. Etiquetas de localización (CRÍTICO)

Aplique siempre etiquetas de localización. La traducción automática se ejecuta automáticamente en cada confirmación a main.

### `[!DNL Product Name]`: no localizar

Se utiliza para nombres de productos de marca que deben permanecer en inglés.

**Aplicar a:**
- Nombres de productos de Adobe: `[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`, `[!DNL Experience Platform]`
- Nombres de productos de terceros: `[!DNL Mozilla Firefox]`, `[!DNL Workfront]`
- Nombres funcionales que podrían confundir la traducción: `[!DNL Pass]`, `[!DNL Campaign]`
- Operadores booleanos usados como términos lógicos: `[!DNL AND]`, `[!DNL OR]`

**NO aplicar a:**
- Direcciones URL, nombres de archivo o nombres de directorio
- Bloques de código (no localizados de forma predeterminada)
- Acrónimos (permanecer en inglés automáticamente)
- Los términos ya se encuentran en la base de datos Do Not Translate

**En el texto del vínculo:** Quite los corchetes de etiqueta para evitar problemas de representación. Usar `[Adobe](https://www.adobe.com)` no `[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]`: controles de IU

Se utiliza para elementos de interfaz: opciones, campos, pestañas, páginas, menús, botones y nombres de funciones tal y como aparecen en la interfaz de usuario. Esta es la etiqueta más crítica para la calidad de la traducción. Trátelo como obligatorio en los procedimientos.

**Aplicar a:**
- Cada elemento de IU en el que se puede hacer clic en los pasos del procedimiento (obligatorio)
- Nombres de funciones y elementos de navegación como se muestran en el producto
- Nombres de páginas, opciones, campos y pestañas tal como se etiquetan en la interfaz de

**Formato:**
- Negrita en pasos y navegación: `Select **[!UICONTROL Destinations]** from the left navigation.`
- Cursiva aceptable en el texto conceptual (no paso) para una mayor claridad.
- En tablas de HTML: use `<span class="uicontrol">term</span>` en lugar de &grave;&grave;.
- En el texto del vínculo: elimine los corchetes de etiqueta.

**Mayúsculas:** Coincide exactamente con la interfaz.

**NO aplicar a:**
- Términos genéricos utilizados conceptualmente: &quot;segment&quot;, &quot;metric&quot;, &quot;campaign&quot; (solo etiqueta cuando se hace referencia explícita al elemento de la interfaz de usuario)
- Oraciones largas (a menos que el nombre del elemento de la interfaz de usuario sea una frase larga)
- Bloques de código o siglas
- Descripciones de iconos. Utilice el nombre del puntero del ratón/información del objeto si está disponible; no etiquete descripciones genéricas como &quot;icono de lápiz&quot;

### `[!DONOTLOCALIZE]`: excluir secciones completas

Ajuste el contenido que debe permanecer en inglés en todas las configuraciones regionales:

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

No se necesita dentro de bloques de código. Estos no están localizados de forma predeterminada.

### Dónde se pueden y no se pueden usar las etiquetas

**Se puede usar en:** párrafos, listas, encabezados, tablas, distintivos, texto alternativo y metadatos.

**No se puede usar en:** bloques de código, acrónimos.

**Regla de metadatos:** Si un campo de metadatos (título o descripción) comienza con una etiqueta `[!DNL]` o &grave;&grave;, escriba todo el valor del campo entre comillas o se producirá un error de validación.

&#x200B;---

## &#x200B;4. Estructura de la información y tipos de contenido

### Tres tipos de contenido: mantenerlos separados

- **Concepto**: Qué y por qué. Presentaciones, descripciones generales, antecedentes. Utilice encabezados de sustantivo/frase de sustantivo.
- **Tarea**: Cómo. Procedimientos paso a paso. Use encabezados de verbo imperativos. Siempre precedido por un concepto.
- **Referencia**: Campos, parámetros, opciones, códigos de error. Utilice tablas. Recoger con otro material de referencia.

### Estructura del artículo

- Abierto con contexto conceptual que orienta al lector.
- A continuación, desplácese a las tareas y haga referencia al material.
- Responda a una pregunta específica por página. No demasiado amplio, no demasiado estrecho.
- Página de concepto con páginas de tareas secundarias (varias páginas) O subencabezados de concepto H1 + tarea H2 (una sola página).
- Introduzca sinónimos o nombres anteriores una vez (por ejemplo, &quot;ECID (Experience Cloud ID)&quot;) para conectar términos de búsqueda.

### Pasos

- Cada paso es un solo comando: una frase completa con un punto (o dos puntos si se introduce una sublista).
- Los pasos siempre comienzan con un verbo o el objetivo antes de la acción: &quot;Para ejecutar el informe, seleccione Ejecutar&quot;.
- Combine pequeñas acciones que se producen en el mismo lugar de la interfaz de usuario en un solo paso cuando la frase permanece clara.
- Dirija 7 pasos por tarea; 10 es el máximo práctico. Dividir tareas más largas en subtareas.
- Utilice una sola viñeta (no `1.`) para un procedimiento que solo tenga un paso.
- NO utilice encabezados como pasos en la documentación del producto. Para tutoriales largos de varias páginas, utilice subencabezados de estilo &quot;Paso 1: ...&quot; cuando sea necesario.
- Coloque la información del paso (texto explicativo) con sangría en una nueva línea después del paso.
- Coloque las capturas de pantalla con sangría después del paso o la acción que hace que aparezca la pantalla.
- Repita los nombres de las páginas, pestañas o paneles por pasos para que los lectores sepan dónde están.

### Archivos TOC (TOC.md)

- Mayúsculas y minúsculas en las frases de todas las entradas (excepto sustantivos propios y elementos de la interfaz de usuario).
- Entradas de concepto: sustantivos y frases sustantivadas.
- Entradas de tarea: verbos imperativos (no gerundios).
- Mantenga las entradas paralelas.
- Cada encabezado de sección del índice debe tener un identificador de anclaje válido: `+ Processing rules {#processing-rules}`
- Un encabezado de sección (principal) del índice no puede ser un vínculo. Debe tener un ID de anclaje.
- NO agregue el mismo archivo varias veces en un índice.
- NO comente líneas en medio de una lista de índice. Mover comentarios al final del archivo.

### Ocultar archivos de navegación

Use el método **V2** para todo el trabajo nuevo. El método V1 está obsoleto.

**V2 (actual): `{hide-from-toc}` en TOC.md**

Coloque `{hide-from-toc}` directamente en `TOC.md` antes del artículo o sección que desee ocultar. NO lo agregue al contenido principal del artículo.

```
+ {hide-from-toc} [Article title](filename.md)
+ {hide-from-toc} Section name {#section-id}
  + [Nested article](nested.md)
```

- Los artículos ocultos siguen siendo accesibles a través de una dirección URL directa.
- Una sección cuyas entradas estén todas ocultas desaparecerá de la navegación izquierda.

**V1 (obsoleto): `hidefromtoc: yes` en frontmatter**

```yaml
hidefromtoc: yes
```

NO utilice esta opción en páginas nuevas. El artículo debe seguir apareciendo en `TOC.md` para poder publicarse, pero no aparecerá en la navegación izquierda.

**Ocultándose de los motores de búsqueda: `hide: yes` en frontmatter**

```yaml
hide: yes
```

Esto excluye la página de la búsqueda externa e interna. La configuración `hide: yes` establece `index: no` automáticamente. Utilice esto además de `{hide-from-toc}` cuando desee ocultar una página tanto para la navegación como para la búsqueda.

&#x200B;---

## &#x200B;5. Terminología y marca

Origen autorizado: [wiki de terminología de cara al usuario de AEP](https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology). Consulte siempre a través de la herramienta MCP de confluencia (`mcp__adobe-wiki-confluence`) para obtener la versión más reciente.

### Nombres de productos

Utilice siempre estos formularios exactos. Incluya &quot;Adobe&quot; en la primera referencia de una guía; puede soltarlo en menciones posteriores donde la directiva lo permita.

NO anteponga a los nombres de los productos &quot;el&quot; a menos que el nombre oficial lo incluya.
- Correcto: &quot;Introducción al asistente de IA&quot;.
- Incorrecto: &quot;Introducción al asistente de IA&quot;.

| Correcto | NUNCA use |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (referencia secundaria) | Plataforma (sola, a menos que el contexto sea inequívoco) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secundario) | Real-time CDP (minúscula &quot;t&quot;) |
| Adobe Real-Time Customer Data Platform | — |
| Perfil del cliente en tiempo real | Perfil del cliente en tiempo real, perfil unificado |
| Adobe Journey Optimizer | AJO |
| Adobe Journey Optimizer B2B Edition | AJO B2B |
| Adobe Journey Optimizer B2B Prime | AJO B2B Prime |
| Adobe Marketo Optimizer | AMO |
| Adobe Marketo Engage | Marketo (se puede usar como adjetivo) |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secundario) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Conexiones de Adobe Real-Time CDP | Conexiones de RTCDP, Conexiones de AEP, Conexiones (solas) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Etiquetas (nombre del producto) | Launch (obsoleto) |
| Gestión de decisiones | Offer Decisioning (solo entre paréntesis: &quot;anteriormente Offer Decisioning&quot;) |
| secuencia de datos (una palabra, minúscula) | flujo de datos, configuración de edge |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (en desuso) |
| GenAI de Adobe | — |
| Adobe GenStudio for Performance Marketing | — |

**&quot;Tiempo real&quot;** siempre usa R mayúscula y T mayúscula cuando forma parte del nombre de un producto (Real-Time CDP, Perfil del cliente en tiempo real, Real-Time Customer Data Platform).

**Ediciones**: &quot;ediciones&quot; se escribe en minúsculas genéricamente; &quot;Edición&quot; se escribe en mayúsculas como parte del nombre de una edición de producto (por ejemplo, &quot;Adobe Real-Time CDP B2C Edition&quot;).

**Abreviaciones en comunicaciones externas**: NO abrevie los nombres de productos en la documentación del usuario. No hay AEP, CJA, AJO ni RTCDP en los documentos. Excepciones limitadas: los acrónimos pueden aparecer entre paréntesis en el primer uso cuando ayudan a la optimización de los motores de búsqueda (SEO) o en las entradas del índice, los metadatos de descripción y los encabezados cuando la longitud es un problema.

### Terminología de funciones y conceptos

| Correcto | NO use |
|---|---|
| reenvío de eventos | reenvío del lado del servidor, Launch Server Side |
| lista de permitidos | lista blanca |
| LISTA DE BLOQUEADOS / LISTA DE BLOQUEADOS | poner en lista negra |
| primary/replica OR primary/secondary (servidores) | maestro/esclavo |
| principal (rama de GitHub) | principal |
| hacker ético | hacker de sombrero blanco |
| remarketing | retargeting |
| grupo de campos | mixin (en desuso), Extensiones, Mixins |
| caducidad automática de datos | TTL, tiempo de vida y caducidad |
| zona protegida de no producción | ensayo (como nombre de entorno) |
| definición del segmento | segmento (solo, cuando se refiere a la definición) |
| ID (escribir siempre en mayúsculas) | Identificación |
| ingesta/ingesta/ingesta | incorporación (para agregar datos a Platform) |
| conjunto de datos/conjuntos de datos | Archivo de datos, archivos de conjuntos de datos |
| control de acceso | permisos (para la función Platform) |
| widget | tarjeta de métrica (obsoleta) |
| variable de marcador de posición | variable ficticia |
| no disponible / bloqueado / desactivado / desactivado | atenuado |
| control coherencia | control de sanidad |
| incorporado | nativo (como sinónimo de integrado) |
| de alta prioridad | debe clavar |
| legacy | cláusula de abuelo |
| principal/principal/origen | principal (como descriptor) |

**Uso de mayúsculas específico de Analytics:**
- Los nombres de los paneles están en minúsculas: en blanco, atribución, experimentación, forma libre (excepción: &quot;lienzo de Recorrido&quot;)
- Los nombres de las visualizaciones están en minúsculas: barra, anillo, histograma, línea, mapa del árbol, texto

### Términos solo internos: NUNCA se utiliza en documentos públicos

Estos términos aparecen en Jira, wikis y discusiones internas, pero nunca deben aparecer en la documentación:

| Término interno | Utilice en su lugar |
|---|---|
| AEP | Adobe Experience Platform |
| PALMERA | administración de zonas protegidas/control de acceso |
| BIOMA | entorno |
| Hidratar/hidratar | crear/rellenar |
| Perfil unificado | Perfil del cliente en tiempo real |
| Ensayo (entorno) | zona protegida de no producción |
| DTM | Etiquetas |
| Inquilino | Organización/organización de IMS |
| BRUTO | crear, leer, actualizar y eliminar (deletrear) |
| Sifón, BSO, Ethos | nombres de código internos, nunca externos |
| Lúpulo | término interno del RGPD/control de acceso |
| Ritmo | término de publicidad no orientada al usuario |
| En preparación | término de infraestructura interna de Adobe |

&#x200B;---

## &#x200B;6. Idioma inclusivo y accesibilidad

### Principios de lenguaje inclusivo

- Use términos neutrales en cuanto al género: &quot;representante de ventas&quot;, no &quot;vendedor&quot;, &quot;moderador&quot;, no &quot;presidente&quot;.
- Prefiera una segunda persona (&quot;usted&quot;) para evitar los pronombres de género.
- Use &quot;ellos&quot; singulares para una persona cuyo sexo es desconocido. NO use él/ella o (s)él.
- Incluya nombres de culturas no blancas en ejemplos (por ejemplo, Ayesha, Ibrahim, Vignesh, Quynh). NO use solo nombres culturalmente blancos (John, Bill, Karen, Amy).
- NO combinar el sexo (hombre/mujer) con el sexo (hombre/mujer).
- Ponga mayúsculas en las nacionalidades, los pueblos, las razas (que no sean &quot;blancos&quot;, según el AP Stylebook) y las tribus.
- Utilice un lenguaje que dé prioridad a las personas: &quot;personas que utilizan tecnología de asistencia&quot;, no &quot;personas con discapacidad&quot;.
- Evite eufemismos como &quot;con capacidades diferentes&quot;. Evite los descriptores utilizados como sustantivos: &quot;ciego&quot;, &quot;sordo&quot;.
- Evite términos que reflejen la identidad (apropiación cultural): animal espiritual, sherpa, pow wow, gurú, ninja, tribu.

### Terminología no inclusiva para evitar

| Utilice | No |
|---|---|
| lista de permitidos/lista de bloqueados de la/lista de bloqueados | lista blanca/lista negra |
| primary/replica OR primary/secondary | maestro/esclavo |
| principal (rama git) | principal |
| de alta prioridad | debe clavar |
| variable de marcador de posición | variable ficticia |
| no disponible / bloqueado / desactivado / desactivado | atenuado |
| control coherencia | control de sanidad |
| incorporado | nativo (como sinónimo) |
| autoridad/experto | gurú/ninja |
| miembros de su grupo | miembros de su tribu |
| reunión | pow wow / dar la vuelta a los vagones |
| modelo a seguir / espíritu emparentado | animal espirituoso |
| guía | sherpa |
| legacy | cláusula de abuelo |
| empresa fútil | marcha de la muerte |
| ridículo/incompetente/impredecible | tonto/cojo/loco |
| hacker ético / no ético | sombrero blanco / hacker sombrero negro |
| Reproducir vídeo | Ver vídeo |
| Ver / Mostrar / Ir a todos | Ver todo |

### Accesibilidad: descripción de la IU

NO describa los elementos de la interfaz de usuario por color o posición de pantalla. El color no funciona para usuarios daltónicos o lectores de pantalla. La posición de la pantalla no es fiable con tecnologías de asistencia.

**Usar idioma cronológico, no idioma espacial:**

| Utilice | No |
|---|---|
| Primero, Siguiente, Finalmente | Arriba, Abajo |
| En la barra de menús | A la izquierda |
| Antes/Después | En la parte superior/inferior de la pantalla |

**Describa qué hacen los controles, no su aspecto:**

| Utilice | No |
|---|---|
| Seleccionar búsqueda | Haga clic en el icono de lupa |
| Editar | El icono de lápiz |
| Activado/desactivado | Conmutar/conmutar/activar |
| Menú | Cajón lateral |
| Ingresar email | Escriba su dirección de correo electrónico |
| Guarde. | El botón &quot;Guardar&quot; |
| Cancelar | Cerrar |

NO utilice el color solo para transmitir información. Siempre combine el color con el texto o la forma.

### Accesibilidad: texto alternativo

- Describa lo que muestra la imagen, no solo su nombre de pantalla.
- Utilice frases completas con la gramática y la puntuación adecuadas.
- Incluya el texto relevante de la imagen.
- Utilice palabras completas, no abreviaciones. Los lectores de pantalla escriben abreviaturas en voz alta.
- Las imágenes que transmiten información independientemente del texto adyacente DEBEN tener texto alternativo.
- Las imágenes puramente decorativas pueden omitir el texto alternativo, pero es recomendable incluirlo.
- Pruebe imágenes con un simulador de daltonismo cuando el color se utiliza para transmitir significado.
- NO utilice gráficos animados que parpadeen más de tres veces por segundo (riesgo de convulsiones).

### Accesibilidad: vínculos

- Nunca utilice &quot;haga clic aquí&quot; o &quot;vínculo&quot; como texto del vínculo.
- Borre el destino solo del texto del vínculo.
  - Bueno: Consulte los requisitos previos de RTCDP en la Guía del usuario de RTCDP.
  - Malo: &quot;Haga clic aquí para conocer los requisitos previos&quot;.

### Accesibilidad: vídeos

- Los vídeos NO deben reproducirse automáticamente.
- Proporcione siempre una alternativa textual, una transcripción o un vínculo a instrucciones escritas.
- Incluya subtítulos significativos en todos los vídeos.
- Cuando sea posible, vincule a instrucciones escritas: &quot;Para instrucciones escritas, consulte [vínculo]&quot;.

&#x200B;---

## &#x200B;7. Ortografía y puntuación

### Inglés americano

| Utilice | No |
|---|---|
| color | color |
| reconocer | reconocer |
| licencia | licencia |
| while | while |
| vencimiento | vencimiento |
| medidor | medidor |
| entre | entre |

### Reglas de puntuación

- Las comillas de cierre no incluyen comas ni puntos.
- Reserve comillas para citar personas. No cite cadenas de interfaz de usuario (utilice UICONTROL y negrita en los pasos).
- Utilice cursiva para los términos usados como términos (no comillas): *perfil*, no &quot;perfil&quot;.
- Utilice comillas invertidas para el código, los parámetros, los nombres de archivo y el texto escrito: `datasetId`.
- Negrita: solo para elementos de la interfaz de usuario en procedimientos (con UICONTROL) y términos clave en la primera introducción. Las líneas de posible cliente en negrita son aceptables en los diseños de preguntas más frecuentes que no utilizan preguntas de nivel de encabezado.
- Cursiva: para énfasis, palabras extranjeras, términos que se están definiendo o nombres conceptuales en texto sin pasos.
- Negrita + cursiva combinados: `***text***`.
- NO utilice reglas horizontales (`---` o `***`). No son compatibles con Experience League.
- NO utilice guiones largos (—), guiones largos (-) ni guiones en prosa. En su lugar, reformule la frase. Los guiones solo se permiten en adjetivos compuestos que aparecen en la interfaz de usuario, los nombres de archivo y el código.
- Dos puntos: se utiliza para presentar una lista. Ponga en mayúscula la primera palabra después de dos puntos cuando siga una frase completa (o la palabra es un sustantivo propio).
- Sin punto y coma. Utilice un punto y una nueva oración en su lugar.

&#x200B;---

## &#x200B;8. SEO y buscabilidad

- Incluya términos de búsqueda (palabras clave) en los primeros párrafos.
- Utilice términos que los lectores busquen realmente. Incluya sinónimos y nombres de términos anteriores cuando sea útil.
- Palabras clave en los encabezados: incluyen nombres de funciones, elementos de interfaz y la tarea que se está realizando.
- Google indiza el texto alternativo de las imágenes. Haga que sea descriptivo y significativo.
- Evite colocar términos esenciales únicamente en tablas o imágenes complejas (no indexadas de forma fiable por IA o búsqueda).
- Metadatos de descripción: utilice un lenguaje natural con palabras clave. NO incluya palabras clave aleatorias. Google puede degradar el contenido para el relleno de palabras clave.
- Mantenga los campos de metadatos (título, descripción, etiquetas de características) completos y precisos: las superficies de detección utilizan metadatos para filtrar y clasificar los resultados antes de leer el contenido de la página.

&#x200B;---

## &#x200B;9. Convenciones de archivos y repositorios

- Se requiere Frontmatter en cada archivo de `.md`.
- Las imágenes van en una subcarpeta `assets/` relativa al archivo Markdown.
- Las imágenes que no se deben localizar se ubican en una subcarpeta `do-not-localize/`.
- Los archivos de índice (`TOC.md`) definen la estructura de navegación izquierda. Actualícelas cuando añada o elimine páginas.
- Use vínculos relativos a la raíz (`/help/...`) para referencias cruzadas entre documentos en este repositorio.
- Para vínculos a documentos fuera de este repositorio, use `https://experienceleague.adobe.com/es...` URL absolutas.
- Nomenclatura de rama: sin prefijo de nombre de usuario. Utilice el número de ticket de Jira y un slug con título (por ejemplo, `PLAT-12345-Update-Guardrail-Limits`). Asigne un nombre a la sucursal y al título de PR con el mismo formato.
- Los componentes discretos (encabezados, bloques de código delimitado, listas) deben estar rodeados de líneas en blanco.
- Solamente un H1 (`#`) por documento. La primera línea después de frontmatter debe ser la H1.

&#x200B;---

## &#x200B;10. Revisar lista de comprobación

Al revisar o editar la documentación, compruebe todos los elementos siguientes.

**Voz y estilo**

- [ ] Voz centrada en el usuario. No &quot;te permite&quot;, &quot;te permite&quot;
- [ ] &quot;usted&quot; utilizó en lugar de &quot;usuarios&quot; al dirigirse directamente a la audiencia
- [ ] Segunda persona y estado de ánimo imperativo en los procedimientos
- [ ] voz activa en todo
- [ ] frases ≤ 20 palabras como destino
- [ ] Sin adjetivos vagos (&quot;rápido&quot;, &quot;fácil&quot;). Sustitúyalo por descripciones precisas.
- [ ] Los términos clave aparecen en el texto del cuerpo (no solo en imágenes o tablas) para la detección de IA

**Estructura y encabezados**
- [ ] encabezados: mayúsculas y minúsculas de la oración, ≤5 palabras / 69 caracteres, seguido de texto independiente, sin encabezados apilados
- [ ] No se han omitido niveles de encabezado
- [ ] Los encabezados de concepto son frases sustantivadas; los encabezados de tarea son verbos imperativos
- [ ]: 7 pasos de Target por tarea; máximo de 10. Los procedimientos de un solo paso utilizan una viñeta, no `1.`
- [ ] máximo de 8 elementos por lista con viñetas

**Terminología**
- [ ] nombres y formularios de productos correctos (Sección 5)
- [ ] Sin términos obsoletos: mixin, TTL, Offer Decisioning, Launch, Unified Profile, Tiempo real (t minúscula), Sensei
- [ ] Sin términos internos: AEP, PALM, BIOME, hidrato, ensayo, DTM, inquilino, canalización
- [ ] Sin términos no inclusivos: lista blanca, lista negra, maestro/esclavo, prueba de cordura, tonto, atenuado, nativo, gurú, ninja, animal espiritual, sherpa, marcha de la muerte, pow wow, tribu
- [ ] Sin &quot;el&quot; antes de los nombres de producto (por ejemplo, no &quot;el Adobe Experience Platform&quot;)

**Etiquetas de localización**
- [ ] &grave;&grave; en todos los nombres de elementos de la interfaz de usuario; negrita en pasos
- [ ] `[!DNL]` en todos los nombres de productos y de terceros
- [ Operadores booleanos ] etiquetados: `[!DNL AND]`, `[!DNL OR]`
- [ ] Sin etiquetas dentro de bloques de código
- [ ] Los campos de metadatos que comienzan con una etiqueta están entre comillas

**Sintaxis de Markdown**
- [ ] sintaxis de advertencia correcta (en blanco `>` línea entre etiqueta y contenido)
- [ ] listas utilizan marcadores coherentes; las listas numeradas utilizan `1.` para cada elemento
- [ ] No hay listas de tareas (`- [ ]`)
- [ ] Sin reglas horizontales (`---` entre contenido)
- [ ] líneas en blanco alrededor de encabezados, bloques de código, listas y tablas
- [ ] No hay imágenes de código. Utilice bloques de código.
- [ ] capturas de pantalla utilizan el tema claro; sin datos de clientes; sin IU de terceros

**Accesibilidad**
- [ ] Texto alternativo: oraciones completas, palabras completas, describe contenido (no solo el nombre de pantalla)
- [ ] Sin idioma direccional/espacial: sin &quot;arriba&quot;, &quot;abajo&quot;, &quot;a la izquierda&quot;, &quot;en la parte superior derecha&quot;
- [ ] El texto del vínculo describe el destino. Sin &quot;clic aquí&quot;
- [ ] vídeos no configurados para la reproducción automática; se han proporcionado transcripciones o alternativas escritas
- [ ] No se utiliza ningún color solo para transmitir información

**Archivos y vínculos**

- [ ] Asunto principal requerido: título (caso de título, ≤60 caracteres), descripción (de 150 a 160 caracteres)
- [ ] No hay direcciones URL vacías en el texto del cuerpo. Utilice siempre un texto de vínculo descriptivo.
- [ ] vínculos internos relativos a la raíz; vínculos absolutos para referencias entre repositorios
- [ ] Los nombres de archivo están en minúsculas con guiones; slugs descriptivos (no incluye `overview.md`)
- [ ] imágenes en `assets/`; imágenes no localizadas en `do-not-localize/`

&#x200B;---

## &#x200B;11. Referencias externas

Utilice la herramienta MCP correcta según el tipo de recurso:

- **Problemas y tickets de Jira** (`jira.corp.adobe.com`): use la herramienta MCP de Corp Jira (`mcp__corp-jira`)
- **Páginas Wiki / Confluence** (`wiki.corp.adobe.com`): use la herramienta MCP de Confluence (`mcp__adobe-wiki-confluence`)
- **Experience League público/páginas web**: use WebFetch

**Páginas wiki internas (usar la herramienta MCP de confluencia):**
- **wiki de terminología**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1230620427/Adobe+Experience+Platform+User-Facing+Terminology
- **Guía de estilo de plataforma**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/1938986972/Platform+style+guide
- **Guía de accesibilidad e inclusión**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2234798784/Writing+for+accessibility+and+inclusivity
- **Guía de ayuda contextual**: https://wiki.corp.adobe.com/spaces/DMSArchitecture/pages/2575057078/How+to+add+contextual+help+popovers+to+the+Experience+Platform+documentation+and+UI

**Público (usar WebFetch):**
- **Descripción general de la localización**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localization-overview
- **Referencia de etiquetas de localización**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/authoring/localization/localize
- **Sintaxis de Experience League Markdown**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/markdown-syntax
- **Hoja de trucos de Markdown**: https://experienceleague.adobe.com/en/docs/authoring-guide/using/markdown/cheatsheet
- **Referencia de estilo de notas de la versión**: https://experienceleague.adobe.com/es/docs/experience-platform/release-notes/latest

**Clon local:**
- **Repositorio de guías de creación:** Use un cierre de compra disponible de la guía de creación de Adobe Experience League o de su documentación pública.
