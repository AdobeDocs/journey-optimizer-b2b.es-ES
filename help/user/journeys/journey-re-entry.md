---
title: reentrada de recorrido
description: Controle cuándo y con qué frecuencia las cuentas pueden volver a introducir el mismo recorrido de cuenta.
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
source-git-commit: 5adf65f3c48c17f73e4897fb9ce027631bf196a7
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 1%

---

# reentrada de recorrido

_Solo recorridos de cuenta_

Al habilitar la reentrada para un recorrido de cuenta, puede controlar cuándo y con qué frecuencia una cuenta puede volver a introducir el mismo recorrido. Utilice la configuración de reentrada para establecer criterios, límites y tiempos de espera para que las cuentas se vuelvan a calificar para el recorrido de forma controlada.

Una cuenta puede volver a clasificarse para un recorrido cuando los siguientes elementos son verdaderos:

* La cuenta está dentro del número de reentradas permitidas para el recorrido.
* La cuenta ha alcanzado el umbral de tiempo de espera (el tiempo mínimo de espera antes de volver a clasificarse).
* La cuenta no está actualmente en el recorrido.

## Habilitar la reentrada para un recorrido de cuenta

Puede habilitar la reentrada y cambiar la configuración de esta cuando el recorrido se encuentre en estado _Borrador_.

1. Abra el recorrido de cuenta provisional.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y elija **[!UICONTROL Reentrada]**.

   ![Haga clic en Más en la parte superior derecha](./assets/account-journey-draft-more-menu.png){width="450"}

1. En el cuadro de diálogo _[!UICONTROL reentrada de Recorrido]_, active la opción **[!UICONTROL Habilitar reentrada]**.

   Cuando la función está activada, se muestran las opciones de temporización, retraso y límites.

   ![Cuadro de diálogo de reentrada de Recorrido con característica habilitada](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. Para **[!UICONTROL tiempo de reentrada]**, elija cómo se calcula la espera:

   * **[!UICONTROL Esperar desde el final del recorrido]**: el período de espera comienza cuando la cuenta sale o completa el recorrido. Por ejemplo: &quot;30 días después de que la cuenta complete el recorrido, pueden volver a entrar&quot;.

   * **[!UICONTROL Esperar desde el inicio del recorrido]**: el período de espera se basa en el momento en que la cuenta entró en el recorrido por primera vez. Por ejemplo, &quot;30 días después de que la cuenta haya iniciado el recorrido, pueden volver a entrar&quot;.

1. Establezca **[!UICONTROL Retraso en la reentrada]**, que es la duración de la espera en horas o días.

   Esta configuración determina cuánto tiempo debe esperar una cuenta después de salir o iniciar el recorrido para que pueda volver a entrar.

1. Defina el **[!UICONTROL límite de entradas]** para definir el número máximo de veces que una cuenta puede ingresar al recorrido.

   Cuando una cuenta alcanza el límite, ya no cumple los requisitos para la entrada hasta que se restablece el límite o se vuelve a publicar el recorrido con un nuevo límite.

   Este límite se aplica por cuenta para ese recorrido.

1. Haga clic en **[!UICONTROL Guardar]**.

## Progresión y actividad de la cuenta

Para un recorrido de cuenta publicado, el mapa de recorrido muestra [progresión de cuenta](./journeys-overview.md#review-account-progression) para los nodos de recorrido. Cada nodo del mapa muestra el número de cuentas que se van a alcanzar y, para los recorridos activos, el número de cuentas que hay actualmente en ese nodo. Cada vez que una cuenta vuelve a introducir un recorrido, se cuenta como una entrada distinta.
<!-- You can see how many times accounts have entered the journey. ?? -->

Cuando explora en [detalles de la cuenta](../accounts/account-details.md), la actividad de la cuenta se muestra cada vez que la cuenta ingresó al recorrido. Incluye una actividad explícita y un recuento de periodicidad para que pueda ver claramente las reentradas.
