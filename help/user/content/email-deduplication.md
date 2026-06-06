---
title: Anulación de duplicación de correo electrónico
description: Obtenga información sobre cómo utilizar la anulación de duplicación de correos electrónicos en recorridos de cuenta para evitar que el mismo correo electrónico se envíe varias veces a la misma dirección de correo electrónico.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: correo electrónico, deduplicación, recorrido, duplicado
exl-id: 93107acd-1cb2-4316-acfc-e32ab1e065ae
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: 2026-03-30T22:08:16.582Z
TQID: https://experienceleague.adobe.com/aWKXaC6x4Izeh81A6Fpy-Nrf18fHgnq6jUc-82ohErs
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 1%

---

# Deduplicación de correo electrónico

Para asegurarse de que el mismo correo electrónico no se envíe varias veces a la misma dirección de correo electrónico dentro de un recorrido, utilice la anulación de duplicación de correo electrónico en los recorridos de cuenta. Al habilitar esta función, se bloquean las direcciones de correo electrónico duplicadas hasta que el primer registro con esa dirección de correo electrónico complete el recorrido. Una vez que una cuenta termina un recorrido, una persona puede cumplir los requisitos para recibir correos electrónicos de nuevo como parte de una nueva cuenta que entra en el recorrido.

## Cuándo utilizar la deduplicación de correo electrónico

Hay algunos escenarios clave a considerar para habilitar la deduplicación de correo electrónico:

* **El correo electrónico no se usa como identidad en Real-Time CDP**. Puede que aparezca la misma dirección de correo electrónico en varios perfiles de persona. Si esos perfiles duplicados cumplen los requisitos para el mismo recorrido y desea evitar que se envíe el correo electrónico más de una vez, habilite esta función.

* **Persona única asociada con varias cuentas**: si el modelo de datos de [!DNL Real-Time CDP] asocia a una sola persona con varias cuentas, habilite esta característica para evitar que se envíe el mismo correo electrónico dos veces cuando varios perfiles con la misma dirección de correo electrónico cumplan los requisitos para el mismo recorrido.

>[!NOTE]
>
>La deduplicación de correos electrónicos se aplica en el nivel de recorrido. Si una persona con la misma dirección de correo electrónico cumple los requisitos para diferentes recorridos, aún puede recibir correos electrónicos de cada recorrido.

## Habilitar la deduplicación de correo electrónico para un recorrido

Para habilitar la anulación de duplicación de correo electrónico en un recorrido de cuenta:

1. Abra un recorrido de cuenta.

1. Haga clic en **[!UICONTROL Más]** (**...**) en la esquina superior derecha del espacio de trabajo de recorrido.

   ![Espacio de trabajo de Recorrido con menú Más expandido que muestra la opción Deduplicación de correo electrónico](./assets/email-deduplication-more-menu.png){width="450"}

1. Elija **[!UICONTROL Anulación de duplicación de correo electrónico]**.

1. En el cuadro de diálogo, seleccione la casilla de verificación **[!UICONTROL Deduplicación de correo electrónico]**.

   ![Cuadro de diálogo de anulación de duplicación de correo electrónico con la opción habilitada](./assets/email-deduplication-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Guardar]**.

Cuando la deduplicación de correo electrónico está habilitada, el recorrido comprueba cada dirección de correo electrónico antes de enviarlo. Si ya ha entrado en ese nodo de recorrido un registro con la misma dirección de correo electrónico, la nueva entrada se bloquea hasta que el primer registro complete la recorrido.
