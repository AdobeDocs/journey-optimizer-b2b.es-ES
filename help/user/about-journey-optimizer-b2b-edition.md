---
title: Información general sobre Adobe Journey Optimizer B2B Edition
description: Descubra las funciones clave, los casos de uso y las arquitecturas de Adobe Journey Optimizer B2B Edition.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 164a038ecce64cbf113c50b9328f84a95aa7b201
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Información general sobre Adobe Journey Optimizer B2B Edition

Con Adobe Journey Optimizer B2B Edition, puede orquestar recorridos de cuenta y de grupo de compra mediante IA generativa integrada y automatización líder del sector para maximizar la demanda de ofertas específicas mediante grupos de compra cualificados para marketing.

## Recorridos de cuenta con grupos compradores

Al comparar Adobe Journey Optimizer B2B Edition con Marketo Engage y Adobe Journey Optimizer Standard, la distinción clave es que los recorridos de cuentas mueven cuentas a través del Recorrido, no personas. Una persona asociada a una cuenta tiene muy probablemente una progresión no lineal, basada en el progreso de la cuenta a través del recorrido, no en función de sus acciones individuales. Por ejemplo, cuando una cuenta se encuentra en la fase inicial del recorrido de compra, la información enviada puede referirse a las funciones o características generales de la solución. Más adelante en el proceso de compra, el contenido podría centrarse más en ofertas u otros artículos concretos orientados al cierre de una venta. Una vez adquirida la solución, la información podría cambiar de nuevo para ofrecer guías de procedimientos, prácticas recomendadas, información acerca de próximos eventos o contenido acerca de ventas adicionales. Incluso si un individuo no ha interactuado con el contenido de la fase inicial, aún desea progresar a la fase actual en función no de sus propias acciones, sino de las acciones de otras personas dentro de su cuenta o grupo de compra.

## Arquitectura de alto nivel

Adobe Journey Optimizer B2B Edition usa _Audiencias de cuenta_ y _Audiencias de personas_ de la cuenta de Adobe Experience Platform para activar un recorrido de cuentas, que se ejecuta dentro de Marketo Engage. Experience Platform siempre es la fuente fiable de estos datos, pero toda la ejecución y el procesamiento del recorrido de cuentas se producen dentro de la infraestructura de marketing B2B del Marketo Engage. La orquestación devuelve los datos al Experience Platform en tiempo casi real gracias al conector de origen existente de Marketo Engage - Adobe Real-Time CDP B2B Edition, que transmite los cambios de datos de Marketo Engage a Experience Platform.

![Arquitectura de datos de alto nivel](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

### Modelo de suscripción

Una suscripción a Journey Optimizer B2B Edition está definida por un par de zonas protegidas de Experience Platform (AEP) con una suscripción de Marketo Engage _munchkin_. No es posible asociar una sola suscripción de Marketo Engage con más de una zona protegida de AEP. Si no elige utilizar una suscripción de Marketo Engage existente con Journey Optimizer B2B Edition o no utiliza Marketo Engage en este momento, se le proporcionará una nueva suscripción de Marketo Engage vacía para utilizarla con Journey Optimizer B2B Edition.

El propósito de Experience Platform en esta configuración es proporcionar una vista unificada de los datos de las instancias de Marketo Engage (y de cualquier sistema CRM conectado) y, a continuación, poder actuar sobre los datos unificados mediante un recorrido de cuentas.

### Operaciones de recorrido de cuenta

Los recorridos de cuenta se crean en Journey Optimizer B2B Edition y se almacenan en la instancia de Marketo Engage asociada a la suscripción. Aunque se almacena en el almacén de datos de Marketo Engage, no es visible desde la interfaz de usuario de Marketo Engage y solo se puede utilizar desde Journey Optimizer B2B Edition.

Un recorrido de cuentas siempre comienza con la selección de un segmento de cuenta para utilizarlo como audiencia de cuenta para el recorrido. La selección de la audiencia utiliza el componente de selector de audiencia de Experience Platform estándar. Los especialistas en marketing pueden implementar el recorrido de cuentas dividiendo las rutas del recorrido según sus propios criterios, que pueden incluir criterios de cuenta, criterios de personas o criterios de grupos de compras. En cada rama, se pueden realizar acciones para implementar el recorrido, como enviar un correo electrónico o esperar a que se produzca un evento.

Una vez creado el recorrido de la cuenta, debe publicarse. En el momento de la publicación, el recorrido de la cuenta se valida y se convierte en una serie de campañas de Marketo Engage que implementan la experiencia de recorrido y se contacta con Data Integration Services para iniciar el flujo de datos que, a su vez, inicia las operaciones de recorrido de la cuenta. El primer paso es crear los segmentos para las Personas de la cuenta.

### Flujo de datos

Journey Optimizer B2B Edition utiliza la segmentación de cuentas de Real-Time CDP para definir y ejecutar segmentos de cuenta y segmentos de persona de cuenta relacionados requeridos por recorrido. A medida que se ejecuta un recorrido publicado, los datos sobre las personas y las cuentas pueden cambiar, y se recopilan datos sobre las personas que interactúan con el recorrido. Journey Optimizer B2B Edition se basa en el conector de origen del Marketo Engage para Real-Time CDP B2B Edition para devolver los cambios de datos al entorno limitado del Experience Platform, que es la fuente fiable.  Estos datos se envían a AEP de forma casi en tiempo real.

Solo los tipos de datos existentes compatibles con el conector de origen del Marketo Engage (cuentas, personas y oportunidades) regresan a Real-Time CDP. Esto significa que la compra de datos de grupo no fluye a AEP y, en su lugar, reside en la instancia de Marketo Engage utilizada por la suscripción a Journey Optimizer B2B Edition.
