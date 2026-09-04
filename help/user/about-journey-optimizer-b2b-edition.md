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
source-git-commit: 8d2fc3ebc7df1674ac9af441679228a9e19d8d5a
workflow-type: tm+mt
source-wordcount: 739
ht-degree: 15%

---

# Información general de Adobe Journey Optimizer B2B Edition

Con Adobe Journey Optimizer B2B edition, puede organizar los recorridos de personas y cuentas mediante IA generativa integrada y automatización líder del sector para maximizar la demanda de ofertas específicas mediante grupos de compra cualificados para marketing.

## Recorridos de cuenta con grupos de compras

Al comparar los recorridos de cuenta con las funciones de recorrido de Marketo Engage y Adobe Journey Optimizer Standard, la distinción clave es que los recorridos de cuenta mueven cuentas a través del recorrido, no personas. Una persona asociada a una cuenta suele tener una progresión no lineal que se basa en el progreso de la cuenta a través del recorrido, no en sus acciones individuales. Por ejemplo, cuando una cuenta se encuentra en la fase inicial del recorrido de compra, la información enviada suele referirse a las funciones o características generales de la solución. Más adelante en el proceso de compra, el contenido se orienta más a ofertas particulares u otros artículos orientados al cierre de una venta. Una vez adquirida la solución, la información vuelve a cambiar para ofrecer guías de procedimientos, prácticas recomendadas, información acerca de próximos eventos o contenido acerca de ventas adicionales. Incluso si un individuo no ha interactuado con el contenido de la fase inicial, puede llevarlo a la fase actual en función de las acciones de otros dentro de su cuenta o grupo de compra.

## Arquitectura de alto nivel

Adobe Journey Optimizer B2B edition se basa en Adobe Experience Platform, incluido Real-Time CDP B2B. Journey Optimizer B2B edition y Marketo Engage se ejecutan en sistemas independientes, cada uno con su propio almacén de datos. Experience Platform es el almacén de datos principal y la fuente autorizada para cuentas, personas y oportunidades. Journey Optimizer B2B edition es propietario de los recorridos de la cuenta, los grupos de compras y las funciones de grupo de compras.

Una instancia de Marketo Engage específica es compatible con cada suscripción de Journey Optimizer B2B edition. Esta instancia no almacena los recorridos de la cuenta, las audiencias ni los grupos compradores. En su lugar, proporciona derechos y servicios back-end, como envío de correo electrónico, configuración de remitente y dominios de marca.

Para admitir acciones de recorrido, también puede conectar una o más instancias de Marketo Engage existentes, incluida la instancia de producción. Las acciones de recorrido permiten a los especialistas en marketing coordinar recorridos basados en cuentas en Journey Optimizer B2B edition con campañas basadas en posibles clientes en Marketo Engage, como agregar personas a una lista o una campaña de solicitud. [Más información sobre cómo conectar instancias de Marketo Engage](./admin/marketo-actions-connect.md).

![Arquitectura de datos de alto nivel que muestra Journey Optimizer B2B edition conectado a Adobe Experience Platform como la fuente fiable para audiencias de cuenta y personas, una instancia de Marketo Engage dedicada que proporciona derechos y servicios back-end y una instancia de Marketo Engage de producción opcional utilizada para ejecutar acciones de recorrido.](./assets/high-level-data-architecture.png){zoomable="yes"}

>[!NOTE]
>
>Compruebe sus derechos de licencia y la [descripción del producto](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=es){target="_blank"} correspondiente para comprobar las protecciones de rendimiento y las limitaciones estáticas.

### Modelo de suscripción

Una zona protegida de Experience Platform combinada con una instancia de Marketo Engage específica define una suscripción de Journey Optimizer B2B edition. Esta instancia dedicada es independiente de la instancia de producción de Marketo Engage y existe para admitir autorizaciones y servicios back-end en lugar de almacenar datos de recorrido de cuentas. [Más información sobre la instalación](./setup-ultimate.md).

Experience Platform proporciona una vista unificada de los datos de las instancias de Marketo Engage conectadas y de los sistemas CRM. Utilice esos datos unificados para crear y ejecutar sus recorridos.

### operaciones de recorrido

Journey Optimizer B2B edition crea, almacena y ejecuta las recorridos de la cuenta. Los recorridos de cuenta no aparecen en Marketo Engage y solo se pueden utilizar en Journey Optimizer B2B edition.

Un recorrido siempre comienza con una audiencia que califica a los posibles clientes o cuentas y a su gente para el recorrido. Seleccione esta audiencia con el selector de audiencia estándar de Experience Platform. Los especialistas en marketing implementan el recorrido dividiendo las rutas mediante criterios de cuenta, criterios de personas o criterios de grupo de compra. En cada ruta, las acciones envían comunicaciones o esperan a que se produzca un evento.

Después de crear un recorrido de cuenta, publíquelo para activar el recorrido. Las cuentas que cumplen los requisitos introducen un recorrido publicado en un plazo de 24 horas.

### Flujo de datos

Journey Optimizer B2B edition funciona como un destino de B2B edition de Adobe Real-Time CDP. Utilice la segmentación de cuentas de Real-Time CDP para crear y evaluar las audiencias de cuenta y las audiencias de personas que califican a las cuentas y personas para un recorrido. Al publicar un recorrido, Journey Optimizer B2B edition activa las audiencias aptas de Experience Platform.

La compra de grupos, la compra de funciones de grupo y la compra de puntuaciones de grupo se crean y almacenan en Journey Optimizer B2B edition. [Más información sobre cómo comprar grupos](./buying-groups/buying-groups-overview.md).
