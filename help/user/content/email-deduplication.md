---
title: Anulación de duplicación de correo electrónico
description: Obtenga información sobre cómo utilizar la anulación de duplicación de correos electrónicos en recorridos de cuenta para evitar que el mismo correo electrónico se envíe varias veces a la misma dirección de correo electrónico.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: correo electrónico, deduplicación, recorrido, duplicado
source-git-commit: 89dcfae6293fc2bd1eefb58943bee354c57bc73a
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 1%

---

# Deduplicación de correo electrónico

Utilice la anulación de deduplicación de correos electrónicos en las recorridos de cuenta para asegurarse de que el mismo correo electrónico no se envíe varias veces a la misma dirección de correo electrónico dentro de un recorrido. Al habilitar esta función, se bloquean las direcciones de correo electrónico duplicadas hasta que el primer registro con esa dirección de correo electrónico complete el recorrido. Una vez que una cuenta termina un recorrido, una persona puede cumplir los requisitos para recibir correos electrónicos de nuevo como parte de una nueva cuenta que entra en el recorrido.

## Cuándo utilizar la deduplicación de correo electrónico

Hay un par de escenarios clave en los que debe considerar la posibilidad de habilitar la deduplicación de correo electrónico:

* **El correo electrónico no se usa como identidad en Real-Time CDP**. Puede que aparezca la misma dirección de correo electrónico en varios perfiles de persona. Si esos perfiles duplicados cumplen los requisitos para el mismo recorrido y desea evitar que se envíe el correo electrónico más de una vez, habilite esta función.

* **Persona única asociada con varias cuentas**: si el modelo de datos de Real-Time CDP permite que una sola persona se asocie con varias cuentas y desea evitar enviar el mismo correo electrónico dos veces a esa persona cuando varias cuentas (incluidos perfiles con la misma dirección de correo electrónico) cumplen los requisitos para el mismo recorrido, habilite esta característica.

>[!NOTE]
>
>La deduplicación de correos electrónicos se aplica en el nivel de recorrido. Si una persona con la misma dirección de correo electrónico cumple los requisitos para diferentes recorridos, aún puede recibir correos electrónicos de cada recorrido.

## Habilitar la deduplicación de correo electrónico para un recorrido

Para habilitar la anulación de duplicación de correo electrónico en un recorrido de cuenta:

1. Abra un recorrido de cuenta.

1. Haga clic en **[!UICONTROL Más]** (**...**) en la esquina superior derecha del área de trabajo de recorrido.

   ![Espacio de trabajo de Recorrido con menú Más expandido que muestra la opción Deduplicación de correo electrónico](./assets/email-deduplication-more-menu.png){width="450"}

1. Elija **[!UICONTROL Anulación de duplicación de correo electrónico]**.

1. En el cuadro de diálogo, seleccione la casilla de verificación **[!UICONTROL Deduplicación de correo electrónico]**.

   ![Cuadro de diálogo de anulación de duplicación de correo electrónico con la opción habilitada](./assets/email-deduplication-dialog.png){width="400"}

1. Haga clic en **[!UICONTROL Guardar]**.

Cuando la deduplicación de correo electrónico está habilitada, el recorrido comprueba cada dirección de correo electrónico antes de enviarlo. Si ya ha introducido un registro con la misma dirección de correo electrónico en ese nodo de recorrido, la nueva entrada se bloquea hasta que el primer registro complete la recorrido.
