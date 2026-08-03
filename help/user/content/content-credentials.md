---
title: Content Credentials
description: Descubra cómo Adobe Journey Optimizer B2B edition aplica automáticamente Content Credentials a las imágenes generadas o editadas con herramientas de IA generativa y qué significa esto para su contenido.
feature: Assets, Content
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: ad794b50f6c6f3b59e853e99f7983136ee098e18
workflow-type: tm+mt
source-wordcount: 913
ht-degree: 0%

---

# Content Credentials

Las organizaciones de marketing están más preocupadas que nunca por la transparencia del contenido, la divulgación de la IA y la prevención de la manipulación de activos. Content Authenticity Initiative (CAI) en Adobe crea herramientas compatibles con el estándar técnico de [Coalición para la procedencia y autenticidad del contenido](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). _Content Credentials_, metadatos cifrados y a prueba de manipulaciones, puede ayudar a los espectadores a comprender el linaje del contenido y garantizar la integridad de los recursos de la marca. Esta información incluye:

* Emisor o signatario: información sobre la entidad o compañía que emitió la firma digital para certificar o firmar el activo.
* Fecha de emisión: la fecha en la que se aplicó Content Credential al recurso.
* Crédito y uso: información sobre el productor del activo, incluido el nombre, los identificadores de las redes sociales u otra información relacionada con la identidad.
* Proceso: Registra las ediciones o modificaciones realizadas en el recurso.
* Detalles del dispositivo: información sobre la aplicación o el dispositivo utilizado para crear o editar el recurso.
* Herramienta de IA utilizada: si se ha utilizado IA generativa para editar o crear el recurso, se puede incluir el nombre del modelo utilizado.
* Otra información pertinente: también se pueden incluir datos adicionales para ayudar a ofrecer más contexto sobre el historial de un recurso.

Para obtener información completa sobre el historial de recursos, puede usar la [herramienta de inspección](https://contentauthenticity.adobe.com/inspect) de Adobe Content Authenticity.

Content Credentials persiste con el archivo de imagen. Cuando se carga o exporta una imagen generada o editada con IA generativa desde [!DNL Adobe Journey Optimizer B2B Edition], se conservan sus Content Credentials.

>[!NOTE]
>
>Es posible que algunos métodos para importar imágenes en el contenido, como extraer una imagen de un PDF o de un origen incrustado (base64), no conserven el Content Credentials original. En estos casos, Content Credentials no se puede leer desde el origen y no se crea ninguno para el resultado.

>[!BEGINSHADEBOX]

## Persistencia de Content Credentials mediante canales {#channels}

Cuando se incluyen imágenes en los mensajes de correo electrónico o WhatsApp, las Content Credentials de las imágenes enviadas también se mantienen:

* **Correo electrónico**: cuando uses una acción de recorrido _Enviar correo electrónico_, agrega la imagen al contenido del correo electrónico desde la biblioteca de _Assets_. Cuando se envía el correo electrónico, el destinatario puede descargar la imagen del mensaje y el Content Credentials está intacto.
* **WhatsApp**: agrega la imagen a la plantilla de mensaje de WhatsApp de tu cuenta comercial de Meta. Puede agregarlo directamente desde su propio sistema o descargar un archivo de imagen desde la biblioteca _Assets_. Usa la plantilla para una acción de recorrido _Enviar aplicación WhatsApp_. Cuando se envía el mensaje de WhatsApp, el destinatario puede descargar la imagen del mensaje y el Content Credentials está intacto.

>[!ENDSHADEBOX]

## Acciones que afectan a Content Credentials {#cc-workflows}

>[!INFO]
>
>Están surgiendo nuevas leyes en torno a la transparencia generativa de la IA, y Adobe está trabajando para cumplir con los requisitos aplicables en todas las jurisdicciones. Content Credentials es la herramienta de procedencia que utiliza Adobe para cumplir los requisitos de estas leyes.

Cuando genera o edita una imagen con herramientas de IA generativa en [!DNL Journey Optimizer B2B Edition], Content Credentials se adjunta automáticamente a esa imagen y no se requiere ninguna acción por su parte.

### Generar una imagen {#generate}

**_Ejemplo:_** Generar una imagen de titular para un mensaje de correo electrónico a partir de un mensaje de texto que describa el elemento visual deseado. Los Content Credentials se adjuntan a la imagen generada.

Cuando se crea una imagen nueva a partir de un mensaje de texto, una imagen de referencia o se genera una imagen similar, siempre se adjuntan Content Credentials.

### Recortar una imagen {#crop}

**_Ejemplos:_**

* Recorte una imagen de titular generada para adaptarla a una página web. Los Content Credentials se conservan a través del recorte.
* Utilice una foto de archivo cargada como fondo de correo electrónico y córtela para que se ajuste a la pantalla. Si la foto de archivo no contiene información de IA generativa, no se crean Content Credentials.

Al realizar un ajuste en un archivo de imagen, como recortarlo a dimensiones solicitadas, conserva su Content Credentials solo si la imagen de origen ya los tenía. Al recortar se vuelven a crear los píxeles de la imagen, lo que normalmente elimina esa Content Credential, por lo que el Asistente de IA la lee de la imagen de origen antes de recortarla y, a continuación, la vuelve a crear y a adjuntar al resultado recortado. El recorte en sí no agrega una nueva acción de IA generativa; conserva la existente.

### Añadir una superposición de texto

**_Ejemplo:_** Produzca un titular promocional como una superposición de texto en una imagen de fondo generada para una página de aterrizaje. Se conservan los Content Credentials de la imagen de fondo.

Cuando se procesa texto generado sobre una imagen de fondo, Content Credentials se adjunta en la imagen resultante solo si la imagen de fondo ya tenía Content Credentials. Al procesar la superposición, se genera una nueva imagen, por lo que la herramienta de edición de imágenes lee el Content Credentials del fondo y lo vuelve a adjuntar al resultado. El paso de superposición no agrega una nueva acción de IA generativa.

### Superposición de una imagen

**_Ejemplos:_**

* Cree un encabezado de correo electrónico combinando una imagen de producto generada con un fondo generado. El resultado lleva Content Credentials que refleja ambas fuentes de IA generativas.
* Combina dos fotos de marca cargadas en una imagen de collage. Dado que ninguna de las imágenes de origen lleva consigo una acción de IA generativa, no se crean Content Credentials.

Cuando se componen dos o más imágenes juntas y cualquiera de las imágenes de origen tiene Content Credentials, la imagen combinada las conserva, combinadas en un único elemento de metadatos de Content Credentials. La composición produce una nueva imagen a partir de las fuentes, que normalmente elimina esas Content Credentials. Pero las herramientas de edición de imágenes leen cada una antes de componer, luego construyen un solo elemento combinado de Content Credentials que enumera todas las fuentes que contribuyeron con una acción de IA generativa.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see Content Credentials directly within the _Assets_ library. When you open the asset details, any image with Content Credentials (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the Content Credentials remain intact with the asset.

_To access Content Credentials:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->