---
title: Calificador de ventas
description: Aprenda a utilizar la aplicación Calificador de ventas para acelerar y mantener sus recorridos.
feature: Account Journeys, AI Assistant
role: User
source-git-commit: 8fb86fe3434a5acdec6fd638fad571a0bc901884
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 1%

---


# Calificador de ventas

>[!NOTE]
>Esta función se encuentra actualmente en disponibilidad limitada y no está disponible para todos los usuarios.
>

El cualificador de ventas es una aplicación complementaria de Adobe Journey Optimizer B2B edition basada en IA que contiene Account Qualification Agent y que está diseñada para optimizar los flujos de trabajo de los representantes de desarrollo empresarial (BDR). El calificador de ventas automatiza los flujos de trabajo de cualificación de clientes potenciales, alcance y participación del comprador en todos los canales, reduciendo la carga manual de BDR y acelerando la velocidad de la canalización para las empresas B2B empresariales.
Utilice los complementos de explorador y correo electrónico para acceder a inteligencia empresarial directamente desde CRM o Outlook.

El calificador de ventas se incluye con AJO B2B, pero es una aplicación independiente dentro de AEP Experience Cloud.

![Página de inicio del calificador de ventas](assets/home-screen.png)

## Account Qualification Agent

Account Qualification Agent (AQA) es el núcleo del Calificador de ventas. El AQA utiliza IA para leer sus cuentas y determinar cuáles están listas para el siguiente paso.  Ayuda con la investigación, redacción de correos electrónicos y actualizaciones de CRM.

![Account Qualification Agent](assets/acc-qualification-agent.png)

* **Investigación prospectiva**

  Realice investigaciones de clientes potenciales utilizando la recuperación automática y la visualización de información clave del cliente potencial (como el puesto, los compromisos recientes, la pertenencia al grupo de compra) para proporcionar una imagen completa en segundos.

* **Investigación de la cuenta**

  Investigue la cuenta utilizando la recuperación automática y la visualización de información detallada sobre la organización de un cliente potencial. Esta información incluye elementos vitales de la empresa, noticias recientes, prioridades estratégicas y miembros de alto compromiso.

* **Correos electrónicos de borrador**

  Genere borradores de correos electrónicos sintetizando la investigación a partir de perspectivas y perspectivas de cuenta para producir contenido de correo electrónico único relevante y personalizado en función del objetivo de BDR.

* **Correos electrónicos del plan de participación**

  Cree borradores de correo electrónico de plan de participación personalizados para cada paso de una cadencia de alcance definida por BDR, lo que garantiza que toda la secuencia esté personalizada

### Uso básico

Los agentes de inteligencia artificial aplicada a Adobe usan _consultas en lenguaje natural_, lo que significa que usan el mismo idioma en el mensaje de texto que cuando se habla con una persona. Cuanto más detallado sea, mejores serán los resultados.

Con el lenguaje natural, puede pedir al agente que:

* Mostrar mis posibles clientes asignados sin participación todavía
* Muéstrame todos mis leads que no formen parte de ningún compromiso autónomo
* Dame un resumen detallado de `<company>`, incluido su grupo de compra, las señales de intención recientes y nuestro compromiso anterior.

Puedes entender inmediatamente qué cuentas y clientes potenciales son los más activos y mostrar la intención más alta, para que puedas enfocar tu energía donde tenga el mayor impacto.

Itere sobre el recorrido refinando los indicadores para obtener los resultados que necesita. Por ejemplo:

* Redacte un borrador de un correo electrónico de seguimiento a partir de un contexto como llamadas de ganancias o informes. Hasta 120 palabras. Línea de asunto: cautivador, que incorpora un tema clave. Introducción: enlace con una cita directa de fuentes de contexto. Cuerpo: conéctese a puntos problemáticos y propuestas de valor. CTA: Proponga una breve llamada para explorar más a fondo.

* El objetivo de este correo electrónico es iniciar una conversación y generar credibilidad. Redacte un correo electrónico con menos de 120 palabras que tenga un tono consultivo y empático. Asegúrese de evitar un enfoque demasiado familiar o de ventas y no utilice las frases &quot;espero que esté bien&quot;, &quot;solo registrarse&quot; o &quot;por favor&quot;.

## Perspectivas

Esta ventana enumera todos los posibles clientes a los que tiene acceso. Es muy rápido comprobar cosas como el estado del posible cliente y la última actividad.

![Ver todos los posibles clientes en la tabla de posibles clientes](assets/prospects.png)

Haga clic en el icono Filtro ![Icono de filtro](../assets/icon-filter.png) para filtrar por estado de posible cliente.

## Planes de participación

Esta ventana proporciona detalles sobre cualquier plan de participación definido.

![Planes de participación](assets/engagement-plans.png)

Para crear un nuevo plan de participación, haga clic en **[!UICONTROL Crear plan de participación]**.

1. En la fase Detalles, proporcione un nombre y una descripción opcional. Haga clic en **[!UICONTROL Guardar y continuar]**.
1. En la fase Seleccionar posibles clientes, seleccione los posibles clientes que deben pertenecer a este plan.
1. En la fase Definir cadencia, defina los parámetros del plan.
1. En la fase de vista previa, asegúrese de que todo funciona según lo esperado.

## Bandeja de salida de correo

El panel Bandeja de salida de correo electrónico enumera todos los correos electrónicos automatizados que ha enviado.

## Reservas de reunión

Este panel muestra todas las reuniones configuradas mediante automatización.

## Bandeja de entrada de chat

Este panel muestra todos los hilos de chats.

![Bandeja de entrada de chat](assets/chat-inbox.png)

No solo puede interactuar con los clientes, sino que también puede ver un resumen del contacto y un resumen del hilo, de modo que pueda saber rápidamente dónde se encuentra en el hilo.

## Integraciones

Con las integraciones, el cualificador de ventas puede aprovechar los CRM y otras fuentes de datos para enriquecer los perfiles de los clientes y aprovechar las actividades de ventas:

* Integre con la bandeja de entrada de su correo electrónico para realizar un seguimiento de los correos electrónicos entrantes relevantes y ayudar a generar respuestas.
* Leer y actualizar datos de CRM, como Salesforce o Microsoft® Dynamics, ZoomInfo o Buildwidth.

![Integración de Outlook del Calificador de ventas](assets/outlook.png)

### Configuración de una nueva integración

Para iniciar una nueva integración, haga clic en **[!UICONTROL Crear integración]** en la parte superior derecha.

![Detalles de integración](assets/integration-details.png)

Aquí definimos la URL de la integración y establecemos la carga útil que se va a enviar.

1. Proporcione un nombre único y una descripción (opcional) para la integración.
1. Establezca el campo URL en el punto final de autenticación de integración de su sitio de integración.
1. En Parámetros de ruta, establezca el método HTTP.
1. En Parámetros de encabezado, configure los encabezados HTTP que necesite enviar. Por lo general, un objeto JSON que se envía y requiere un encabezado de tipo de contenido.
1. En Parámetros de consulta, establezca los parámetros necesarios.
1. En Autenticación, configure la información de inicio de sesión para el sitio de integración.

   * Ninguna
   * OAuth 2.0
   * Clave de API
   * Autenticación básica

1. Establezca los valores de regulación y caché en la sección Configuración de carga útil.
1. En Configuración de carga útil, haga clic en el icono de lápiz. En el cuadro de diálogo Pegar carga útil, pegue o introduzca su objeto de carga útil JSON.
   * Solicitar carga útil: un objeto JSON que contiene datos para enviar el sitio de integración.
   * Carga útil de respuesta: la estructura de datos que espera obtener a cambio.
1. Haga clic en [!UICONTROL Probar conexión] para asegurarse de que la configuración es correcta.

Cuando la configuración de conexión sea válida, haga clic en **[!UICONTROL Guardar como borrador]**.

Cuando vuelva a la tabla de integraciones principal, seleccione la integración y haga clic en **[!UICONTROL Activar]** para activar la integración, o en **[!UICONTROL Guardar como borrador]**.



#### Administrar acceso

Puede administrar el acceso a los usuarios y qué tipo de datos se comparten con distintos grupos de usuarios.

Haga clic en **[!UICONTROL Administrar acceso]** para abrir el cuadro de diálogo Administrar acceso.

Este cuadro de diálogo enumera todas las etiquetas que ha establecido su organización. Seleccione las etiquetas que desee aplicar a esta integración.

Si necesita una etiqueta nueva, haga clic en **[!UICONTROL Crear etiqueta]** y rellene:

* Nombre
* Nombre descriptivo
* Descripción

## Configuración de representante

Aquí es donde introduce información sobre usted: detalles personales, configuración de correo electrónico y calendario y disponibilidad del chat.

### Detalles

La pestaña Detalles es donde se introduce información sobre el usuario:

![Configuración de detalles del calificador de ventas](assets/details.png)

### Configuración de correo electrónico

En la pestaña Configuración de correo electrónico, configure las conexiones de correo electrónico.

![Configuración de correo electrónico](assets/email-settings.png)

#### Conexiones de correo electrónico

Haga clic en **[!UICONTROL Conectar]** y siga el procedimiento de inicio de sesión de Microsoft.

#### Firma de correo electrónico

Configure la firma de correo electrónico que se utiliza en los correos electrónicos autogenerados.

### Configuración del calendario

En la pestaña Configuración del calendario, establezca la zona horaria y la disponibilidad.

![Configuración del calendario](assets/calendar-settings.png)

#### Conexión de calendario

Haga clic en **[!UICONTROL Conectar]** y siga el procedimiento de inicio de sesión de Microsoft para integrar su calendario.

#### Correo electrónico de confirmación de la reunión

Cuando un cliente confirma una reunión con usted, recibe el correo electrónico de confirmación como respuesta.
Utilice esta configuración para definir el asunto y el cuerpo del correo electrónico.

#### Preferencias

Establezca la duración predeterminada de la reunión y el tiempo que desea entre reuniones consecutivas.

### Configuración de chat

En esta pestaña, establezca la disponibilidad del chat de Zona horaria en vivo.

![Configuración de chat](assets/chat-settings.png)

## Gestión representativa

En este panel, se muestra una tabla de todos los representantes definidos y su estado de calendario.

## Rendimiento de las reuniones

Este panel presenta análisis en torno a las reuniones completadas.

## Configuración del complemento de Chrome

El complemento AI Assistant Chrome está disponible en [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

Cuando el complemento está instalado en Chrome, el logotipo de Adobe aparece en el centro a la derecha cuando se encuentra en un sitio integrado:

* Aplicaciones web de Adobe
* Salesforce
* Outlook
* Microsoft Dynamics y aplicaciones web
* Aplicaciones de Google

## Editar barra de navegación izquierda

En la parte inferior izquierda de la aplicación, haga clic en **[!UICONTROL Editar]** para controlar cuáles de los iconos son visibles en la navegación. También puede arrastrarlos y soltarlos para reordenarlos como desee.

## Vídeo de demostración

El siguiente vídeo proporciona una breve demostración del Cualificador de ventas y Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476564?captions=spa)
