---
title: Información general sobre Adobe Journey Optimizer B2B edition
description: Descubra las funciones clave, casos de uso y arquitecturas de la edición B2B de Adobe Journey Optimizer.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Información general sobre Adobe Journey Optimizer B2B edition

Con la edición B2B de Adobe Journey Optimizer puede organizar los recorridos de la cuenta y de los grupos de compras mediante la IA generativa integrada y la automatización líder del sector para maximizar la demanda de ofertas específicas mediante grupos de compras cualificados para marketing.

## Recorridos de la cuenta con grupos de compra

Al comparar Adobe Systems Journey Optimizer B2B Edition con Marketo Engage y Adobe Systems estándar de Journey Optimizer, la distinción clave es que cuenta viajes mueven cuentas a través del Journey, no personas. Una persona que está asociada con un cuenta típicamente tiene una progresión no lineal que se basa en el progreso del cuenta a través del viaje, no en función de sus acciones individuales. Por instancia, cuando un cuenta se encuentra en una fase temprana del proceso de compra, la información enviada puede ser sobre capacidades o características generales de la solución. Más adelante en el proceso de compra, el contenido podría centrarse más en ofertas particulares u otros artículos orientados a cerrar una venta. Después de comprar la solución, la información puede cambiar nuevamente para proporcionar guías prácticas, prácticas recomendadas o información sobre próximos eventos, o con contenido sobre ventas adicionales adicionales. Incluso si un individuo no ha interactuado con la fase inicial contenido, aún desea progresar a la fase actual basándose no en sus propias acciones, sino en las acciones de las otras personas dentro de su cuenta o comprando grupo.

## Arquitectura de alto nivel

Adobe Systems Journey Optimizer B2B Edition usa _Account Audiences_ y _People Audiences_ desde Adobe Experience Platform para impulsar un viaje cuenta, que se desarrolla dentro de Marketo Engage. Experience Platform siempre es la fuente fiable de estos datos, pero toda la ejecución y el procesamiento del recorrido de cuentas se producen dentro de la infraestructura de marketing B2B de Marketo Engage. La orquestación devuelve los datos a la Experience Platform casi en tiempo real mediante el conector de origen Marketo Engage existente Adobe Systems CDP B2B Edition en tiempo real, que transmite los cambios de datos de Marketo Engage a Experience Platform.

![Arquitectura de datos de alto nivel](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Compruebe sus derechos de licencia y la [descripción del producto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} correspondiente acerca de las protecciones de rendimiento y las limitaciones estáticas.

### Modelo de suscripción

Una suscripción a Journey Optimizer B2B Edition está definida por un par de entornos limitados de Experience Platform (AEP) con una suscripción a Marketo Engage _Munchkin_ . No es posible emparejar una suscripción de un solo Marketo Engage con más de un entorno limitado de AEP. Si no elige emparejar una suscripción de Marketo Engage existente con Journey Optimizer B2B Edition, se le proporcionará una nueva suscripción de Marketo Engage vacía para su uso con Journey Optimizer B2B Edition.

El propósito de Experience Platform en esta configuración es proporcionar un vista unificado de los datos de las instancias de Marketo Engage (y cualquier sistema CRM conectado) y, a continuación, poder actuar en los datos unificados mediante un recorrido de cuenta.

### Operaciones de recorrido de la cuenta

Los recorridos de la cuenta se crean en Journey Optimizer B2B Edition y se almacenan en el instancia Marketo Engage asociado con la suscripción. Aunque se almacena en el tienda de datos de Marketo Engage, no es visible desde el IU Marketo Engage y solo se puede utilizar desde Journey Optimizer B2B Edition.

Un viaje cuenta siempre comienza con la selección de un segmento de cuenta para usar como cuenta audiencia para el viaje. La selección del audiencia utiliza el componente estándar Experience Platform audiencia selector. Los especialistas en marketing pueden implementar el recorrido de cuentas dividiendo las rutas del recorrido según sus propios criterios, que pueden incluir criterios de cuenta, criterios de personas o criterios de grupos de compras. En cada rama, se pueden realizar acciones para implementar el recorrido, como enviar un correo electrónico o esperar a que se produzca un evento.

Una vez creado el recorrido de la cuenta, debe publicarse. En el momento de la publicación, el recorrido de la cuenta se valida y se convierte en una serie de campañas de Marketo Engage que implementan la experiencia de recorrido. Se contacta con Data Integration Services para iniciar el flujo de datos que, a su vez, inicia las operaciones de recorrido de cuentas. El primer paso es crear los segmentos para las Personas de la cuenta.

### Flujo de datos

Journey Optimizer B2B Edition usa el segmentación de cuenta CDP en tiempo real para definir y ejecutar segmentos cuenta y segmentos relacionados cuenta persona que requieren los viajes. A medida que se ejecuta un viaje publicado, los datos sobre las personas y las cuentas pueden cambiar, y se recopilan datos sobre las personas que interactúan con el viaje. Journey Optimizer B2B Edition se basa en el conector de origen Marketo Engage para Real-Time CDP B2B Edition para transmitir los cambios de datos al entorno Experience Platform de pruebas, que es la fuente de la verdad.  Estos datos se entregan a AEP casi en tiempo real.

Solo los tipos de datos existentes admitidos por el conector de origen de Marketo Engage (cuentas, personas y oportunidades) vuelven a CDP en tiempo real. Esto significa que la compra de datos de grupo no fluye a AEP sino que reside en la instancia de Marketo Engage utilizada por la suscripción a Journey Optimizer B2B Edition.
