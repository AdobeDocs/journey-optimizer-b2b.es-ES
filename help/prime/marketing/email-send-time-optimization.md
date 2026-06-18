---
title: Optimización del tiempo de envío del correo electrónico
description: La optimización del tiempo de envío (STO) en Adobe Journey Optimizer B2B Prime personaliza el envío de correo electrónico para los recorridos de las personas. Aprenda a habilitar STO y a mejorar la participación.
autotag-review: '2026-06-17T20:52:02.535Z'
TQID: 'https://experienceleague.adobe.com/wlxhS7E8DnbThm5ge-wzTkMcn-eBzFUXfw3ZGrfcRHA'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
source-git-commit: 951d9ceaa95656952e36b6d8f238348b08c796ca
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Optimización del tiempo de envío del correo electrónico

Utilice la función de optimización del tiempo de envío (STO) para personalizar el tiempo de envío del correo electrónico para [recorridos de personas](./person-journeys.md) mediante la predicción de cuándo es más probable que se involucre cada perfil. En lugar de un tiempo de envío fijo, STO utiliza señales de participación de correo electrónico históricas para programar la entrega en el momento óptimo para cada destinatario, lo que mejora la participación general.

STO analiza la participación histórica de cada perfil mediante un modelo de lenguaje de gran tamaño. Predice y clasifica los tiempos de envío potenciales y luego programa el envío en la hora de mayor clasificación dentro de la ventana de optimización.

<!-- Performance insights, such as usage, engagement lift, and STO vs. non-STO comparisons, are available through natural language queries in the AI Assistant. -->

>[!BEGINSHADEBOX]

Hay muchas **_mejoras futuras_** planificadas para STO:

* Configuración global de STO en el área _[!UICONTROL Admin]_
* Habilitación de STO de nivel de recorrido
* Divisiones de prueba/control configurables

>[!ENDSHADEBOX]

## Configuración {#configuration}

Puede configurar la optimización del tiempo de envío cuando [agregue un nodo _[!UICONTROL Realizar una acción]_](./action-nodes.md) al recorrido de una persona y elija la acción **[!UICONTROL Enviar correo electrónico]**.

1. Seleccione el nodo de acción de recorrido _Enviar correo electrónico_.

1. En las propiedades del nodo, a la derecha, habilite la opción **[!UICONTROL Optimización del tiempo de envío]**.

   ![Enviar nodo de recorrido de correo electrónico - Opciones de optimización del tiempo de envío](./assets/email-node-send-time-optimization.png){width="450" zoomable="no"}

1. Para especificar la ventana y la distribución de prueba, defina las opciones de STO:

   * **[!UICONTROL Enviar en el plazo del siguiente]**: este valor determina la ventana de optimización (en días), que es el intervalo de tiempo en el que se pueden enviar los correos electrónicos. Por ejemplo, para un seminario web que se produzca en cinco días, puede establecer una ventana de cuatro o cinco días. STO selecciona el tiempo de envío mejor predicho para cada perfil dentro de esta ventana.

   * **STO / Fixed distribution** - STO crea automáticamente una _división de prueba y control_ para dividir los perfiles elegibles entre los tiempos de envío optimizados y fijos. La división permite la comparación directa del rendimiento. (Las futuras mejoras están planificadas para permitir porcentajes de división personalizados).

   >[!NOTE]
   >
   >Los perfiles con un historial de participación sólido se dividen uniformemente en grupos de control y prueba para medir el impacto del STO. Para garantizar resultados estadísticamente fiables, la división de STO frente a no STO se restringe entre el 30 % y el 70 %. Esto ayuda a evitar que cohortes más pequeñas distorsionen los resultados y garantiza comparaciones significativas.

1. Justo después del nodo _[!UICONTROL Enviar correo electrónico]_, [agregue un nodo _Wait_](./wait-nodes.md).

   Un nodo de espera debe seguir inmediatamente a una acción de correo electrónico habilitada para STO. Añadir este nodo garantiza que los perfiles permanezcan en la recorrido hasta que se borre la ventana de optimización completa y se completen todos los envíos de STO. Si omite este nodo, el sistema marca la configuración como no válida.

1. Después de completar el resto del recorrido de la persona, continúe con [publicar](./person-journeys.md#publish).

## Informes


