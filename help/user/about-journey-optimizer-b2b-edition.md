---
title: Información general de Adobe Journey Optimizer B2B Edition
description: 'Obtenga información sobre Adobe Journey Optimizer B2B Edition: organice recorridos de cuenta con grupos de compras, información de IA e integración de Experience Platform para el marketing B2B.'
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
autotag-review: 2026-04-29T23:21:13.339Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
TQID: https://experienceleague.adobe.com/L58cK4MP-S-8U9fFiXU2qZn4HCieNzjoOaSRCLkyanI
source-git-commit: ca0c6b10cf6a979249901d514116f373014544ad
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 66%

---

# Información general de Adobe Journey Optimizer B2B Edition

Con la edición B2B de Adobe Journey Optimizer puede organizar los recorridos de la cuenta y de los grupos de compras mediante la IA generativa integrada y la automatización líder del sector para maximizar la demanda de ofertas específicas mediante grupos de compras cualificados para marketing.

## Recorridos de cuenta con grupos de compras

Al comparar los recorridos de cuenta con las funciones de recorrido de Marketo Engage y Adobe Journey Optimizer Standard, la distinción clave es que los recorridos de cuenta mueven cuentas a través del recorrido, no personas. Una persona asociada a una cuenta suele tener una progresión no lineal que se basa en el progreso de la cuenta a través del recorrido, no en sus acciones individuales. Por ejemplo, cuando una cuenta se encuentra en la fase inicial del recorrido de compra, la información enviada suele referirse a las funciones o características generales de la solución. Más adelante en el proceso de compra, el contenido se orienta más a ofertas particulares u otros artículos orientados al cierre de una venta. Una vez adquirida la solución, la información vuelve a cambiar para ofrecer guías de procedimientos, prácticas recomendadas, información acerca de próximos eventos o contenido acerca de ventas adicionales. Incluso si un individuo no ha interactuado con el contenido de la fase inicial, puede llevarlo a la fase actual en función de las acciones de otros dentro de su cuenta o grupo de compra.

## Arquitectura de alto nivel

Adobe Journey Optimizer B2B Edition usa _Públicos de cuenta_ y _Públicos de personas_ de Adobe Experience Platform para activar un recorrido de cuentas, que se ejecuta dentro de Marketo Engage. Experience Platform siempre es la fuente principal de estos datos, pero todo el proceso de recorrido de la cuenta se lleva a cabo dentro de la infraestructura de marketing B2B de Marketo Engage. La orquestación devuelve los datos a Experience Platform en tiempo casi real mediante el conector de origen Marketo Engage Adobe Real-Time CDP B2B Edition existente, que transmite los cambios de datos de Marketo Engage a Experience Platform.

![Arquitectura de datos de alto nivel](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Compruebe sus derechos de licencia y la [descripción del producto](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=es){target="_blank"} correspondiente sobre las protecciones del rendimiento y las limitaciones estáticas.

### Modelo de suscripción

Un par de zonas protegidas de Experience Platform (AEP) con una suscripción de Marketo Engage _Munchkin_ define una suscripción de Journey Optimizer B2B edition. No es posible asociar una sola suscripción de Marketo Engage con más de una zona protegida de AEP. Si no opta por emparejar una suscripción existente de Marketo Engage con Journey Optimizer B2B Edition, se le proporcionará una nueva suscripción de Marketo Engage vacía para su uso con Journey Optimizer B2B Edition.

Experience Platform proporciona una vista unificada de los datos de las instancias de Marketo Engage y de los sistemas CRM conectados para actuar sobre esos datos mediante un recorrido de cuentas.

### Operaciones de recorrido de cuenta

Los recorridos de cuenta se crean en Journey Optimizer B2B Edition y se almacenan en la instancia de Marketo Engage asociada a la suscripción. Aunque se almacenan en el almacén de datos de Marketo Engage, no son visibles desde la interfaz de usuario de Marketo Engage y solo se pueden utilizar en Journey Optimizer B2B edition.

Un recorrido de cuentas siempre comienza con la selección de un segmento de cuenta para utilizarlo como público de cuenta para el recorrido. La selección del público utiliza el componente de selector de público estándar de Experience Platform. Los expertos en marketing pueden implementar el recorrido de cuentas dividiendo las rutas del recorrido según sus propios criterios, que pueden incluir criterios de cuenta, criterios de personas o criterios de grupos de compras. En cada rama, se pueden realizar acciones para implementar el recorrido, como enviar un correo electrónico o esperar a que se produzca un evento.

Una vez creado el recorrido de la cuenta, debe publicarse. En el momento de la publicación, el recorrido de la cuenta se valida y se convierte en una serie de campañas de Marketo Engage que implementan la experiencia de recorrido. Se contacta con Data Integration Services para iniciar el flujo de datos que, a su vez, inicia las operaciones de recorrido de cuentas. El primer paso es crear los segmentos para las Personas de la cuenta.

### Flujo de datos

Journey Optimizer B2B Edition utiliza la segmentación de cuentas de Real-Time CDP para definir y ejecutar segmentos de cuenta y segmentos de persona de cuenta relacionados requeridos por recorridos. A medida que se ejecuta un recorrido publicado, los datos sobre las personas y las cuentas pueden cambiar, y se recopilan datos sobre las personas que interactúan con el recorrido. Journey Optimizer B2B edition se basa en el conector de origen de Marketo Engage para Real-Time CDP B2B edition para devolver los cambios de datos de flujo a la zona protegida de Experience Platform, que es la fuente de datos principal.  Estos datos se envían a AEP en tiempo casi real.

Solo los tipos de datos existentes compatibles con el conector de origen de Marketo Engage (cuentas, personas y oportunidades) regresan a Real-Time CDP. Esto significa que los datos del grupo de compras no fluye a AEP y, en su lugar, reside en la instancia de Marketo Engage utilizada por la suscripción de Journey Optimizer B2B Edition.
