---
title: Realizar un nodo de acción
description: Marcador de posición
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 2%

---

# Realizar un nodo de acción

En el recorrido de una persona, utilice una acción para las personas cuando desee aplicar un cambio a todas las personas de la ruta del nodo. Para un recorrido de cuentas, este tipo de nodo se puede utilizar dentro de la ruta dividida por personas o por cuentas.

## Acciones y restricciones

| Acción | Restricciones |
| ------ | ---------- |
| **[!UICONTROL Enviar correo electrónico]** | <li>Crear correo electrónico <li>Optimización del tiempo de envío (opcional) |
| **[!UICONTROL Cambiar valor de datos]** | <li>Seleccionar atributo de persona <li>Establecer nuevo valor |

## Añadir un nodo de acción {#add-an-action-node}

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Realizar una acción]**.

1. En las propiedades del nodo, a la derecha, seleccione una acción de la lista y establezca los valores para la acción.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL Enviar correo electrónico]

Utilice esta acción para enviar un correo electrónico. Después de crear el correo electrónico para el nodo, puede diseñar, personalizar y previsualizar mensajes de correo electrónico en el espacio de diseño de correo electrónico (consulte [Creación de correo electrónico](../content/email-authoring.md)).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

Puede usar [Optimización del tiempo de envío](../marketing/email-send-time-optimization.md) para personalizar el tiempo de envío del correo electrónico mediante la predicción de cuándo es más probable que se involucre cada perfil.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL Cambiar valor de datos]

Utilice esta acción para cambiar el valor de un atributo de perfil de persona en la base de datos. Seleccione el atributo y, a continuación, establezca el nuevo valor.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++
