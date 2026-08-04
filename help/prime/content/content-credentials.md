---
title: Content Credentials
description: Descubra cómo Adobe Journey Optimizer B2B Prime aplica automáticamente Content Credentials a las imágenes generadas con IA generativa y qué significa esto para su contenido.
feature: Assets, Content
role: User
badgeBeta: label="Beta" type="informative" tooltip="Esta función forma parte de una versión beta limitada."
autotag-review: '2026-07-31T22:31:06.899Z'
TQID: 'https://experienceleague.adobe.com/fBPnAmupve3xMSw5fZPQBDTUfr-rwiH2-R3wbKvox-E'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: edb796d131c2b058215b73519b845125432d84f8
workflow-type: tm+mt
source-wordcount: 562
ht-degree: 0%

---

# Content Credentials

Las organizaciones de marketing están más preocupadas que nunca por la transparencia del contenido, la divulgación de la IA y la prevención de la manipulación de activos. Content Authenticity Initiative (CAI) en Adobe crea herramientas compatibles con el estándar técnico de [Coalición para la procedencia y autenticidad del contenido](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model) (C2PA). _Content Credentials_ es el conjunto de metadatos cifrados y a prueba de manipulaciones que pueden ayudar a los espectadores a comprender el linaje del contenido y garantizar la integridad de los recursos de la marca. Esta información incluye:

* Emisor o signatario: información sobre la entidad o compañía que emitió la firma digital para certificar o firmar el activo.
* Fecha de emisión: la fecha en la que se aplicó Content Credential al recurso.
* Crédito y uso: información sobre el productor del recurso, incluido el nombre, los identificadores de las redes sociales u otra información relacionada con la identidad.
* Proceso: Registra las ediciones o modificaciones realizadas en el recurso.
* Detalles del dispositivo: información sobre la aplicación o el dispositivo utilizado para crear o editar el recurso.
* Herramienta de IA utilizada: si se ha utilizado IA generativa para crear el recurso, se puede incluir el nombre del modelo utilizado.
* Otra información pertinente: también se incluyen datos adicionales para ayudar a ofrecer más contexto sobre el historial de un recurso.

Para obtener información completa sobre el historial de recursos, puede usar la [herramienta de inspección](https://contentauthenticity.adobe.com/inspect) de Adobe Content Authenticity.

Content Credentials persiste con el archivo de imagen. Cuando se carga o exporta una imagen generada o editada con IA generativa desde [!DNL Adobe Journey Optimizer B2B Prime], se conservan sus Content Credentials.

>[!NOTE]
>
>Es posible que algunos métodos para importar imágenes en el contenido, como extraer una imagen de un PDF o de un origen incrustado (base64), no conserven el Content Credentials original. En estos casos, Content Credentials no se puede leer desde el origen y no se crea ninguno para el resultado.

>[!BEGINSHADEBOX]

## Persistencia de Content Credentials mediante canales {#channels}

Cuando se incluyen imágenes en los mensajes de correo electrónico o WhatsApp, también se mantiene el Content Credentials de las imágenes entregadas:

* **Correo electrónico**: cuando uses una acción de recorrido _Enviar correo electrónico_, agrega la imagen al contenido del correo electrónico desde la biblioteca de _Assets_. Cuando se envía el correo electrónico, el destinatario puede descargar la imagen del mensaje y el Content Credentials está intacto.
* **WhatsApp**: agrega la imagen a la plantilla de mensaje de WhatsApp en tu cuenta comercial de Meta. Puede agregarlo directamente desde el sistema o descargar un archivo de imagen desde la biblioteca _Assets_. Usa la plantilla para una acción de recorrido _Enviar aplicación WhatsApp_. Cuando se envía el mensaje de WhatsApp, el destinatario puede descargar la imagen del mensaje y el Content Credentials está intacto.

>[!ENDSHADEBOX]

## Generación de imágenes {#generate}

>[!INFO]
>
>Están surgiendo nuevas leyes en torno a la transparencia generativa de la IA, y Adobe está trabajando para cumplir con los requisitos aplicables en todas las jurisdicciones. Content Credentials es la herramienta de procedencia que utiliza Adobe para cumplir los requisitos de estas leyes.

Cuando usa IA generativa para crear una imagen para el contenido del correo electrónico en [!DNL Journey Optimizer B2B Prime], Content Credentials se adjunta automáticamente a la imagen generada y no se requiere ninguna acción por su parte. Las herramientas de IA generativa producen un elemento de Content Credentials combinado para variantes de imágenes con credenciales existentes, incluida la fuente original.

>[!NOTE]
>
>[!DNL Journey Optimizer B2B Prime] no admite actualmente las acciones manuales de edición de imágenes. Los flujos de trabajo de Content Credentials para estas acciones no son aplicables en este momento.
