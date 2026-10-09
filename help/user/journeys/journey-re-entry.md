---
title: reentrada de recorrido
description: Controle cuándo y con qué frecuencia las cuentas o personas pueden volver a introducir el mismo recorrido de cuenta o persona.
feature: Account Journeys
role: User
level: Intermediate
exl-id: e5153125-6d5b-4835-bd19-c9b7ce67e46a
autotag-review: '2026-08-14T19:11:15.391Z'
TQID: 'https://experienceleague.adobe.com/BabVdaLaAwER8tEQLOAjChwyy4WI2Cle19-Uu-varIc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: 07717d3ba2d67a61e3dcfa4693e2ee2e151e78da
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 1%
---
# reentrada de recorrido

Al habilitar la reentrada para un recorrido, puede controlar cuándo y con qué frecuencia una cuenta o una persona puede volver a introducir el mismo recorrido. Utilice la configuración de reentrada para establecer criterios, límites y tiempos de espera para que las cuentas o personas se vuelvan a calificar para el recorrido de forma controlada.

Una cuenta o persona puede volver a calificar para un recorrido cuando los siguientes elementos son verdaderos:

* La cuenta o la persona se encuentra dentro del número de reentradas permitidas para el recorrido.
* La cuenta o la persona ha alcanzado el umbral de tiempo de espera (el tiempo mínimo de espera antes de volver a calificar).
* La cuenta o la persona no se encuentran actualmente en el recorrido.

## Habilitar la reentrada para un recorrido

Puede habilitar la reentrada y cambiar la configuración de esta cuando el recorrido se encuentre en estado _Borrador_.

>[!BEGINTABS]

>[!TAB recorrido de la cuenta]

1. Abra el recorrido de cuenta provisional.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y elija **[!UICONTROL Reentrada]**.

   ![Haga clic en Más en la parte superior derecha del recorrido de una cuenta](./assets/account-journey-draft-more-menu.png){width="450"}

1. En el cuadro de diálogo _[!UICONTROL reentrada de Recorrido]_, active la opción **[!UICONTROL Habilitar reentrada]**.

   Cuando la función está activada, se muestran las opciones de temporización, retraso y límites.

   ![Cuadro de diálogo de reentrada de Recorrido para un recorrido de cuenta con característica habilitada](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. Para **[!UICONTROL tiempo de reentrada]**, elija cómo se calcula la espera:

   * **[!UICONTROL Esperar desde el final del recorrido]**: el período de espera comienza cuando la cuenta sale o completa el recorrido. Por ejemplo: &quot;30 días después de que la cuenta complete el recorrido, puede volver a entrar&quot;.

   * **[!UICONTROL Esperar desde el inicio del recorrido]**: el período de espera se basa en el momento en que la cuenta entró en el recorrido por primera vez. Por ejemplo: &quot;30 días a partir de la fecha en que la cuenta inició la recorrido, puede volver a introducirla&quot;.

1. Establezca **[!UICONTROL Retraso en la reentrada]**, que es la duración de la espera en horas o días.

   Esta configuración determina cuánto tiempo debe esperar una cuenta después de salir o iniciar el recorrido para poder volver a entrar.

1. Para definir el número máximo de veces que una cuenta puede ingresar al recorrido, establezca **[!UICONTROL Límite de entrada]**.

   Cuando una cuenta alcanza el límite, ya no cumple los requisitos para la entrada hasta que se restablece el límite o se vuelve a publicar el recorrido con un nuevo límite.

   Este límite se aplica por cuenta para ese recorrido.

1. Haga clic en **[!UICONTROL Guardar]**.

>[!TAB recorrido de personas]

1. Abra el recorrido de persona de borrador.

1. Haga clic en el menú **[!UICONTROL Más...]** en la parte superior derecha y elija **[!UICONTROL Configuración de reentrada]**.

   ![Haga clic en Más en la parte superior derecha del recorrido de una persona](./assets/person-journey-draft-more-menu.png){width="450"}

1. En el cuadro de diálogo _[!UICONTROL reentrada de Recorrido]_, active la opción **[!UICONTROL Habilitar reentrada]**.

   Cuando la función está activada, se muestran las opciones de temporización, retraso y límites.

   ![Cuadro de diálogo de reentrada de Recorrido para el recorrido de una persona con la característica habilitada](./assets/person-journey-re-entry-dialog.png){width="450"}

1. Para **[!UICONTROL tiempo de reentrada]**, elija cómo se calcula la espera:

   * **[!UICONTROL Esperar desde el final del recorrido]**: el período de espera comienza cuando la persona sale o completa el recorrido. Por ejemplo: &quot;30 días después de que la persona complete el recorrido, puede volver a entrar&quot;.

   * **[!UICONTROL Esperar desde el inicio del recorrido]**: el período de espera se basa en el momento en que la persona entró al recorrido por primera vez. Por ejemplo: &quot;30 días después de que la persona haya iniciado el recorrido, puede volver a entrar&quot;.

1. Establezca **[!UICONTROL Retraso en la reentrada]**, que es la duración de la espera en horas o días.

   Esta configuración determina cuánto tiempo debe esperar una persona después de salir o iniciar el recorrido para poder volver a entrar.

1. Para definir el número máximo de veces que una persona puede entrar al recorrido, establezca el **[!UICONTROL límite de entradas]**.

   Cuando una persona alcanza el límite, ya no cumple los requisitos para la entrada hasta que se restablece el límite o se vuelve a publicar el recorrido con un nuevo límite.

   Este límite se aplica por persona para ese recorrido.

1. Haga clic en **[!UICONTROL Guardar]**.

>[!ENDTABS]

## Progresión y actividad

Para un recorrido de persona o cuenta publicada, el lienzo de recorrido muestra [progresión](./journeys-overview.md#review-account-progression) para los nodos de recorrido. Cada nodo muestra el número de cuentas o personas que llegan a ese nodo y, para los recorridos activos, el número que se encuentra actualmente en ese nodo. Cada vez que una cuenta o persona vuelve a introducir un recorrido, se cuenta como una entrada distinta.

<!-- 
You can see how many times accounts have entered the journey. ?? 

When you drill in to [account details](../accounts/account-details.md), the account activity shows each time the account entered the journey. It includes explicit activity and a recurrence count so that you can see re-entries clearly.
-->
