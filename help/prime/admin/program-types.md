---
title: Tipos de programas
description: Cree y administre tipos de programas que definan atributos y flujos de estado de miembros para programas en Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-23T19:10:36.949Z'
TQID: 'https://experienceleague.adobe.com/gDNLfcAICFtF7M-cB1zJjLih5kL6nUlpYA5zb1aQJv0'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: aed878b8-11d0-487c-828b-d23b2051ec37id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
subfeature_v2: id: f6df9def-cdf7-4728-9ec8-3f65716828c7id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ad5a67d291ffef797bb93f8b06f1bd8657efb67f
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 2%

---

# Tipos de programas

Los tipos de programas definen aspectos importantes de [programas](../marketing/programs.md) y sus miembros, y distinguen los distintos tipos de programas de marketing entre sí. Cada tipo de programa define las siguientes propiedades, que se heredan para los programas que utilizan el tipo de programa:

* **Atributos**: los atributos describen aspectos importantes del tipo de programa, como fechas de eventos y atributos de ubicación.

* **Flujo de estado del programa** - Cada estado se asigna a un paso en el tipo de programa (como 1, 2 o 3). Los miembros de un programa solo pueden pasar de un estado con el mismo número de paso (por ejemplo, de _No mostrado_ a _Asistido_) o a un estado con un número de paso superior (por ejemplo, de _Invitado_ a _Registrado_).

  Los estados de los programas son mutuamente excluyentes y lineales, por lo que una persona solo puede tener un valor de estado por programa. Al diseñar estados, piense en los estados entre los que desee permitir el movimiento. Por ejemplo, si alguien no asistió a un seminario web pero tiene la opción de asistir a petición más tarde, le interesa que tenga el mismo número de estado o que establezca un número de estado más alto a petición para que un miembro del programa pueda avanzar a él.

>[!NOTE]
>
>Si al menos un programa utiliza un tipo de programa, no se puede editar.

_Para definir un tipo de programa personalizado :_

1. En la navegación izquierda de [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Tipos de programa]**.

   ![Acceder a la lista de tipos de programas](./assets/program-types-list.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Crear tipo]** en la parte superior derecha.

1. Escriba un **[!UICONTROL Nombre]** único (obligatorio) y una **[!UICONTROL Descripción]** (opcional).

   ![Crear tipo de programa](./assets/program-type-create.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Incluir una descripción es una práctica recomendada y hace que la biblioteca de tipos de programa sea más manejable.

1. Haga clic en **[!UICONTROL Crear tipo]**.

1. Agregue los **[!UICONTROL Atributos]** para el tipo de programa.

   Para cada atributo que desee agregar:

   * Haga clic en **[!UICONTROL Agregar atributo]**.
   * Elija **[!UICONTROL nombre de API]** e introduzca **[!UICONTROL nombre para mostrar]**.
   * Haga clic en **[!UICONTROL Guardar]**.

   ![Atributos de tipo de programa](./assets/program-type-attributes.png){width="600" zoomable="yes"}

1. Defina los pasos para **[!UICONTROL estados de programas]**.

   Defina cada paso que desee incluir en el flujo:

   * Haga clic en **[!UICONTROL Agregar paso]**.
   * Introduzca un nombre de estado.
   * (Opcional) Haga clic en **[!UICONTROL Agregar estado]** e introduzca un nombre de estado adicional para incluir en el paso.

   Active la casilla de verificación **[!UICONTROL Marcar como correcto]** para cualquier paso que desee rastrear como una ejecución correcta del programa.

   ![Estados de tipo de programa](./assets/program-type-statuses.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Listo]** para guardar los cambios y volver a la lista de tipos de programas.