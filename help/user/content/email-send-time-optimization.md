---
title: Optimización del tiempo de envío del correo electrónico
description: La optimización del tiempo de envío (STO) en Adobe Journey Optimizer personaliza la entrega de correo electrónico para los recorridos de las personas. Aprenda a habilitar STO y a mejorar la participación.
feature: Person Journeys, Channels
role: User
source-git-commit: 55cfcd3b4ee777ee8945ea9a1cd1429625ee61c3
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Optimización del tiempo de envío del correo electrónico

Utilice la función de optimización del tiempo de envío (STO) para personalizar el tiempo de envío del correo electrónico para [recorridos de personas](../journeys/journeys-overview.md) mediante la predicción de cuándo es más probable que se involucre cada perfil. En lugar de un tiempo de envío fijo, STO utiliza señales de participación de correo electrónico históricas para programar la entrega en el momento óptimo para cada destinatario, lo que mejora la participación general.

STO analiza la participación histórica de cada perfil mediante un modelo de lenguaje de gran tamaño. Predice y clasifica los tiempos de envío potenciales y luego programa el envío en la hora de mayor clasificación dentro de la ventana de optimización.

## Disponibilidad y ámbito actuales

Actualmente, la optimización del tiempo de envío es compatible con:

* **Tipo de Recorrido**: Recorridos de persona
* **Canal**: Correo electrónico
* **Configuración**: _Enviar correo electrónico_ nodo de acción
* **Informes**: asistente de IA a través de la habilidad de observación de Recorrido

  Las perspectivas de rendimiento, como el uso, el alza de la participación y las comparaciones de STO frente a no STO, están disponibles mediante consultas en lenguaje natural en el asistente de IA.

>[!BEGINSHADEBOX]

Hay muchas **_mejoras futuras_** planificadas para STO:

* Compatibilidad con _Recorridos de cuenta_
* Configuración global de STO en el área _[!UICONTROL Admin]_
* Habilitación de STO de nivel de recorrido
* Divisiones de prueba/control configurables
* Un tablero de informes de STO dedicado

>[!ENDSHADEBOX]

## Configuración

Puede configurar la optimización del tiempo de envío al [agregar un nodo _[!UICONTROL Realizar una acción]_](../journeys/action-nodes.md) al recorrido de una persona.

1. Para _[!UICONTROL Seleccionar acción]_, elige **[!UICONTROL Enviar correo electrónico]**.

1. Utilice la opción **[!UICONTROL Optimización del tiempo de envío]** para habilitar la característica.

1. Defina las opciones de STO para especificar la distribución de ventana y prueba:

   * **[!UICONTROL Enviar en el plazo del siguiente]**: este valor determina la ventana de optimización (en días), que es el intervalo de tiempo en el que se pueden enviar los correos electrónicos. Por ejemplo, para un seminario web que se produzca en cinco días, puede establecer una ventana de cuatro o cinco días. STO selecciona el tiempo de envío mejor predicho para cada perfil dentro de esta ventana.

   * **STO / Fixed distribution** - STO crea automáticamente una _división de prueba y control_ para dividir los perfiles elegibles entre los tiempos de envío optimizados y fijos. La división permite la comparación directa del rendimiento. (Las futuras mejoras están planificadas para permitir porcentajes de división personalizados).

   >[!NOTE]
   >
   >Los perfiles con un historial de participación sólido se dividen uniformemente en grupos de control y prueba para medir el impacto del STO. Para garantizar resultados estadísticamente fiables, la división de STO frente a no STO se restringe entre el 30 % y el 70 %. Esto ayuda a evitar que cohortes más pequeñas distorsionen los resultados y garantiza comparaciones significativas.

   ![Enviar nodo de recorrido de correo electrónico - Opciones de optimización del tiempo de envío](./assets/email-node-send-time-optimization.png){width="700" zoomable="no"}

1. Justo después del nodo _[!UICONTROL Enviar correo electrónico]_, [agregue un nodo _Wait_](../journeys/wait-nodes.md).

   Un nodo de espera debe seguir inmediatamente a una acción de correo electrónico habilitada para STO. Añadir este nodo garantiza que los perfiles permanezcan en la recorrido hasta que se borre la ventana de optimización completa y se completen todos los envíos de STO. Si omite este nodo, el sistema marca la configuración como no válida.

1. Después de completar el resto del recorrido de la persona, continúe con [publicar](../journeys/create-publish-journey.md#publish-a-journey).

## Perspectivas de STO

Las perspectivas de STO se entregan a través del _Asistente de IA_ con la [_aptitud de observación_](../agents/journey-agent.md#journey-observability-skill) de Journey Agent. Puede consultar el uso, las métricas de participación, los resultados de pruebas/control, el rendimiento del nodo y el impacto general en los recorridos.
