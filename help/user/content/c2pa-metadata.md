---
title: Metadatos de C2PA
description: Descubra cómo Adobe Journey Optimizer B2B edition aplica automáticamente los metadatos de C2PA a las imágenes generadas o editadas con herramientas de IA generativa y qué significa esto para su contenido.
feature: Assets, Content
hide: true
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c1e8e03ccd6f2d132ca1bc1a27c0d9ea18dcdcac
workflow-type: tm+mt
source-wordcount: 913
ht-degree: 0%

---

# Metadatos de C2PA

Las organizaciones de marketing están más preocupadas que nunca por la transparencia del contenido, la divulgación de la IA y la prevención de la manipulación de activos. Content Authenticity Initiative (CAI) en Adobe crea herramientas compatibles con el estándar técnico de [Coalición para la procedencia y autenticidad del contenido](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). Los _metadatos de C2PA_ son información cifrada y a prueba de manipulaciones que ayuda a los espectadores a comprender el linaje del contenido y a garantizar la integridad de los recursos de la marca. Esta información incluye:

* Emisor o signatario: información sobre la entidad o compañía que emitió la firma digital para certificar o firmar el activo.
* Fecha de emisión: la fecha en la que se aplicaron los metadatos de C2PA al recurso.
* Crédito y uso: información sobre el productor del activo, incluido el nombre, los identificadores de las redes sociales u otra información relacionada con la identidad.
* Proceso: Registra las ediciones o modificaciones realizadas en el recurso.
* Detalles del dispositivo: información sobre la aplicación o el dispositivo utilizado para crear o editar el recurso.
* Herramienta de IA utilizada: si se ha utilizado IA generativa para editar o crear el recurso, se puede incluir el nombre del modelo utilizado.
* Otra información pertinente: también se pueden incluir datos adicionales para ayudar a ofrecer más contexto sobre el historial de un recurso.

Para obtener información completa sobre el historial de recursos, puede usar la [herramienta de inspección](https://contentauthenticity.adobe.com/inspect) de Adobe Content Authenticity.

Los metadatos de C2PA persisten con el archivo de imagen. Cuando se carga o exporta una imagen generada o editada con IA generativa desde [!DNL Adobe Journey Optimizer B2B Edition], se conservan sus metadatos de C2PA.

>[!NOTE]
>
>Es posible que algunos métodos para importar imágenes en el contenido, como extraer una imagen de un PDF o de un origen incrustado (base64), no conserven los metadatos originales de C2PA. En estos casos, los metadatos de C2PA no se pueden leer desde el origen y no se crea ninguno para el resultado.

>[!BEGINSHADEBOX]

## Persistencia de metadatos de C2PA a través de canales {#channels}

Cuando se incluyen imágenes en los mensajes de correo electrónico o WhatsApp, los metadatos de C2PA de las imágenes entregadas también se mantienen:

* **Correo electrónico**: cuando uses una acción de recorrido _Enviar correo electrónico_, agrega la imagen al contenido del correo electrónico desde la biblioteca de _Assets_. Cuando se envía el correo electrónico, el destinatario puede descargar la imagen del mensaje y los metadatos de C2PA están intactos.
* **WhatsApp**: agrega la imagen a la plantilla de mensaje de WhatsApp en tu cuenta comercial de Meta. Puede agregarlo directamente desde su propio sistema o descargar un archivo de imagen desde la biblioteca _Assets_. Usa la plantilla para una acción de recorrido _Enviar aplicación WhatsApp_. Cuando se envía el mensaje de WhatsApp, el destinatario puede descargar la imagen del mensaje y los metadatos de C2PA están intactos.

>[!ENDSHADEBOX]

## Acciones que afectan a los metadatos de C2PA {#cc-workflows}

>[!INFO]
>
>Están surgiendo nuevas leyes en torno a la transparencia generativa de la IA, y Adobe está trabajando para cumplir con los requisitos aplicables en todas las jurisdicciones. Los metadatos de C2PA son la herramienta de procedencia que utiliza Adobe para cumplir con los requisitos de estas leyes.

Cuando genera o edita una imagen con herramientas de IA generativa en [!DNL Journey Optimizer B2B Edition], los metadatos de C2PA se adjuntan automáticamente a esa imagen y no se requiere ninguna acción por su parte.

### Generar una imagen {#generate}

**_Ejemplo:_** Generar una imagen de titular para un mensaje de correo electrónico a partir de un mensaje de texto que describa el elemento visual deseado. Los metadatos de C2PA se adjuntan a la imagen generada.

Cuando se crea una nueva imagen a partir de un mensaje de texto, una imagen de referencia o se genera una imagen similar, siempre se adjuntan metadatos de C2PA.

### Recortar una imagen {#crop}

**_Ejemplos:_**

* Recorte una imagen de titular generada para adaptarla a una página web. Los metadatos de C2PA se conservan a través del recorte.
* Utilice una foto de archivo cargada como fondo de correo electrónico y córtela para que se ajuste a la pantalla. Si la foto de archivo no contiene información de IA generativa, no se crean metadatos de C2PA.

Al realizar un ajuste en un archivo de imagen, como recortarlo a dimensiones solicitadas, conserva sus metadatos de C2PA solo si la imagen de origen ya lo tenía. Al recortar se vuelven a crear los píxeles de la imagen, lo que normalmente elimina esos metadatos de C2PA, por lo que el asistente de IA los lee de la imagen de origen antes de recortarlos y, a continuación, los vuelve a crear y a adjuntar al resultado recortado. El recorte en sí no agrega una nueva acción de IA generativa; conserva la existente.

### Añadir una superposición de texto

**_Ejemplo:_** Produzca un titular promocional como una superposición de texto en una imagen de fondo generada para una página de aterrizaje. Se conservan los metadatos de C2PA de la imagen de fondo.

Cuando procesa texto generado sobre una imagen de fondo, los metadatos de C2PA se adjuntan en la imagen resultante solo si la imagen de fondo ya tenía metadatos de C2PA. Al procesar la superposición, se genera una nueva imagen, por lo que la herramienta de edición de imágenes lee los metadatos de C2PA del fondo y los vuelve a adjuntar al resultado. El paso de superposición no agrega una nueva acción de IA generativa.

### Superposición de una imagen

**_Ejemplos:_**

* Cree un encabezado de correo electrónico combinando una imagen de producto generada con un fondo generado. El resultado lleva metadatos C2PA que reflejan ambas fuentes de IA generativa.
* Combina dos fotos de marca cargadas en una imagen de collage. Dado que ninguna de las imágenes de origen lleva a una acción de IA generativa, no se crean metadatos de C2PA.

Cuando se componen dos o más imágenes juntas y cualquiera de las imágenes de origen tiene metadatos C2PA, la imagen combinada la conserva y la combina en un solo elemento de metadatos C2PA. La composición produce una nueva imagen a partir de las fuentes, que normalmente elimina los metadatos de C2PA. Sin embargo, las herramientas de edición de imágenes leen los metadatos de origen antes de la composición y, a continuación, crean un único elemento de metadatos combinado de C2PA que enumera todas las fuentes que han contribuido con una acción de IA generativa.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see C2PA metadata directly within the _Assets_ library. When you open the asset details, any image with C2PA metadata (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the C2PA metadata remains intact with the asset.

_To access C2PA metadata:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->
