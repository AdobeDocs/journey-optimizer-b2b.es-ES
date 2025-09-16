---
title: Información general de Adobe Journey Optimizer B2B Edition
description: 'Obtenga información sobre Adobe Journey Optimizer B2B Edition: organice recorridos de cuenta con grupos de compras, información de IA e integración de Experience Platform para el marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d3247a48ff1fbda54c559fa03580865da7252935
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 100%

---

# Información general de Adobe Journey Optimizer B2B Edition

Con la edición B2B de Adobe Journey Optimizer puede organizar los recorridos de la cuenta y de los grupos de compras mediante la IA generativa integrada y la automatización líder del sector para maximizar la demanda de ofertas específicas mediante grupos de compras cualificados para marketing.

## Recorridos de cuenta con grupos de compras

Al comparar Adobe Journey Optimizer B2B Edition con Marketo Engage y Adobe Journey Optimizer estándar, la distinción clave es que los recorridos de cuentas mueven cuentas a través de Journey, no personas. Una persona asociada a una cuenta suele tener una progresión no lineal que se basa en el progreso de la cuenta a través del recorrido, no en sus acciones individuales. Por ejemplo, cuando una cuenta se encuentra en la fase inicial del recorrido de compra, la información enviada puede referirse a las funciones o características generales de la solución. Más adelante en el proceso de compra, el contenido podría centrarse más en ofertas u otros artículos concretos orientados al cierre de una venta. Una vez adquirida la solución, la información podría cambiar de nuevo para ofrecer guías de procedimientos, prácticas recomendadas, información acerca de próximos eventos o contenido acerca de ventas adicionales. Incluso si un individuo no ha interactuado con el contenido de la fase inicial, aún desea progresar a la fase actual en función no de sus propias acciones, sino de las acciones de otras personas dentro de su cuenta o grupo de compras.

## Arquitectura de alto nivel

Adobe Journey Optimizer B2B Edition usa _Públicos de cuentas_ y _Públicos de personas_ de Adobe Experience Platform para activar un recorrido de cuentas, que se ejecuta dentro de Marketo Engage. Experience Platform siempre es la fuente fiable de estos datos, pero toda la ejecución y el procesamiento del recorrido de cuentas se producen dentro de la infraestructura de marketing B2B de Marketo Engage. La orquestación devuelve los datos a Experience Platform en tiempo casi real mediante el conector de origen Marketo Engage Adobe Real-Time CDP B2B Edition existente, que transmite los cambios de datos de Marketo Engage a Experience Platform.

![Arquitectura de datos de alto nivel](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Compruebe sus derechos de licencia y la [descripción del producto](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=es){target="_blank"} correspondiente sobre las protecciones del rendimiento y las limitaciones estáticas.

### Modelo de suscripción

Una suscripción a Journey Optimizer B2B Edition se define mediante un par de zonas protegidas de Experience Platform (AEP) con una suscripción a Marketo Engage _Munchkin_. No es posible asociar una sola suscripción de Marketo Engage con más de una zona protegida de AEP. Si no opta por emparejar una suscripción existente de Marketo Engage con Journey Optimizer B2B Edition, se le proporcionará una nueva suscripción de Marketo Engage vacía para su uso con Journey Optimizer B2B Edition.

El propósito de Experience Platform en esta configuración es proporcionar una vista unificada de los datos de las instancias de Marketo Engage (y de cualquier sistema CRM conectado) y, a continuación, poder actuar sobre los datos unificados mediante un recorrido de cuenta.

### Operaciones de recorrido de cuenta

Los recorridos de cuenta se crean en Journey Optimizer B2B Edition y se almacenan en la instancia de Marketo Engage asociada a la suscripción. Aunque se almacena en el almacén de datos de Marketo Engage, no es visible desde la interfaz de usuario de Marketo Engage y solo se puede utilizar desde Journey Optimizer B2B Edition.

Un recorrido de cuentas siempre comienza con la selección de un segmento de cuenta para utilizarlo como público de cuenta para el recorrido. La selección del público utiliza el componente de selector de público estándar de Experience Platform. Los expertos en marketing pueden implementar el recorrido de cuentas dividiendo las rutas del recorrido según sus propios criterios, que pueden incluir criterios de cuenta, criterios de personas o criterios de grupos de compras. En cada rama, se pueden realizar acciones para implementar el recorrido, como enviar un correo electrónico o esperar a que se produzca un evento.

Una vez creado el recorrido de la cuenta, debe publicarse. En el momento de la publicación, el recorrido de la cuenta se valida y se convierte en una serie de campañas de Marketo Engage que implementan la experiencia de recorrido. Se contacta con Data Integration Services para iniciar el flujo de datos que, a su vez, inicia las operaciones de recorrido de cuentas. El primer paso es crear los segmentos para las Personas de la cuenta.

### Flujo de datos

Journey Optimizer B2B Edition utiliza la segmentación de cuentas de Real-Time CDP para definir y ejecutar segmentos de cuenta y segmentos de persona de cuenta relacionados requeridos por recorridos. A medida que se ejecuta un recorrido publicado, los datos sobre las personas y las cuentas pueden cambiar, y se recopilan datos sobre las personas que interactúan con el recorrido. Journey Optimizer B2B Edition se basa en el conector de origen de Marketo Engage para Real-Time CDP B2B Edition para devolver los cambios de datos de flujo a la zona protegida de Experience Platform, que es la fuente fiable.  Estos datos se envían a AEP casi en tiempo real.

Solo los tipos de datos existentes compatibles con el conector de origen de Marketo Engage (cuentas, personas y oportunidades) regresan a Real-Time CDP. Esto significa que la compra de datos de grupo no fluye a AEP y, en su lugar, reside en la instancia de Marketo Engage utilizada por la suscripción de Journey Optimizer B2B Edition.
