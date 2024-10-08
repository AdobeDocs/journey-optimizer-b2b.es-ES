---
title: Nodos de Recorrido de cuenta
description: Obtenga información acerca de los tipos de nodos que puede utilizar para crear las recorridos de cuenta.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1748'
ht-degree: 2%

---

# Nodos del Recorrido de cuentas

Después de [crear un recorrido de cuenta](journey-overview.md#create-an-account-journey) y [agregar la audiencia](journey-overview.md#add-the-account-audience-for-your-journey), genere el recorrido mediante nodos. El mapa de recorrido proporciona un lienzo en el que puede crear sus casos de uso de marketing B2B de varios pasos.

Cree su recorrido de cuentas combinando los diferentes nodos de acción, evento y orquestación como un escenario de varios pasos y canales cruzados. Cada nodo de un recorrido representa un paso a lo largo de una ruta lógica.

## Nodo Audiencia de cuenta

El nodo [Audiencia de cuenta](journey-overview.md#add-the-account-audience-for-your-journey) define la audiencia de cuenta de entrada (creada y administrada en Adobe Experience Platform) para el recorrido. Este nodo siempre es el primero y se crea automáticamente de forma predeterminada.

## Realizar una acción

Ejecute una acción como enviar un correo electrónico, cambiar la puntuación, etc.

**Acción en cuentas**: la acción se aplica a todas las personas que forman parte de cuentas en esta ruta.

**Acción en personas**: la acción se aplica a todas las personas de esta ruta. Se puede utilizar una acción en personas dentro de la ruta dividida por personas o por ruta dividida por cuentas.

| Contexto del nodo | Función | Restricciones |
| ------------ | -------- | ----------- |
| [People](#add-a-people-action) | Asignar a grupo de compra | Seleccionar interés de solución<br/>Seleccionar rol |
| | Eliminar del grupo de compra | Seleccionar interés de solución |
| | Enviar SMS | Creación de SMS |
| | Añadir a campaña de solicitud de Marketo Engage | Seleccione el espacio de trabajo del Marketo Engage<br/>Seleccionar campaña de solicitud |
| | Cambiar la partición de personas en Marketo Engage | Nueva partición |
| | Momento interesante de la persona | Escriba<br/>Descripción |
| | Cambiar calificación | Nombre de puntuación<br/>Cambiar |
| | Enviar email | Crear nuevo correo electrónico<br/>Seleccionar correo electrónico del Marketo Engage |
| [Cuentas](#add-an-account-action) | Enviar alerta de ventas | Seleccionar interés de solución<br/>Enviar correo electrónico a |
| | Agregar cuenta a (otro) Recorrido | Seleccionar Recorrido de cuenta activa |
| | Actualizar estado del grupo de compra | Interés de la solución<br/>Estado (obligatorio, máximo 50 caracteres) |
| | Quitar cuenta del Recorrido (actual) | Seleccionar Recorrido de cuenta activa |
| | Momento interesante de la cuenta | Escriba (correo electrónico, hito o web)<br/>Descripción (opcional) |
| | Valor de datos de cambio de cuenta | Seleccionar atributo<br/>Nuevo valor |

### Agregar una acción de cuenta

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Realizar una acción]**.

   ![Agregar nodo de recorrido - rutas divididas](./assets/add-node-action.png){width="400"}

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Cuentas]** para la acción.

1. Seleccione una acción de la lista y defina los valores que desee para la acción.

   ![nodo de Recorrido: realice una acción en una cuenta](./assets/node-take-action-account.png){width="700" zoomable="yes"}

### Añadir una acción de personas

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Realizar una acción]**.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para la acción.

1. Seleccione una acción de la lista y defina los valores que desee para la acción.

![nodo de Recorrido: realice una acción con personas](./assets/node-take-action-people.png){width="700" zoomable="yes"}

## Escuchar un evento

La audiencia avanza al siguiente paso del recorrido cuando se produce un evento.

* También puede definir la cantidad de tiempo que el recorrido espera este evento. El recorrido finaliza después de un tiempo de espera.
* Además, puede elegir añadir otros nodos en la ruta de tiempo de espera.

**Escuchar eventos en cuentas**: Si al menos una persona de una cuenta déclencheur un evento, la cuenta avanza al siguiente paso del recorrido.

**Escuchar eventos de personas**: los eventos de personas solo se pueden aplicar en una ruta de acceso de cuenta; no está disponible para un nodo dividido por personas.

| Contexto del nodo | Función | Restricciones |
| ------------ | -------- | ----------- |
| [People](#add-a-people-event) | Cambios en el valor de los datos | Atributo<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | Hace clic en el vínculo del correo electrónico | Correo electrónico<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | Asignado a grupo comprador | Interés en la solución<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | Abre el email | Correo electrónico<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | Se cambia el puntaje | Nombre de puntuación<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | Eliminado del grupo de compra | Interés de la solución<br/>Fecha de la actividad (opcional)<br/>Tiempo de espera (opcional) |
| [Cuentas](#add-an-account-event) | Cambio en el estado del grupo de compra | Interés en la solución<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | Cambio en la puntuación de integridad | Interés en la solución<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | La cuenta tuvo un momento interesante | Type<br/>Restricciones adicionales (opcional)<br/>Timeout (opcional) |
| | Cambio en la puntuación de participación | Interés en la solución<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |
| | Cambio en el valor de datos de cuenta | Atributo<br/>Restricciones adicionales (opcional)<br/>Tiempo de espera (opcional) |

### Agregar un evento de cuenta

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

1. En las propiedades del nodo de la derecha, elija **[!UICONTROL Cuentas]** para el tipo de evento.

   ![nodo de Recorrido: escucha eventos en la cuenta](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Seleccione un evento de la lista.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

### Añadir un evento de personas

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para el tipo de evento.

   ![nodo de Recorrido: escucha eventos de personas](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Seleccione un evento de la lista.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

### Añadir un tiempo de espera a un nodo de evento

Si es necesario, defina la cantidad de tiempo que el recorrido espera el evento. El recorrido finaliza después del tiempo de espera.

1. Habilite la opción timeout.

1. Seleccione el periodo de tiempo durante el cual el recorrido espera a que se produzca un evento antes de que se agote el tiempo de espera.

   Puede optar por finalizar la ruta aquí o realizar una acción diferente estableciendo otra ruta.

1. Para crear una nueva ruta en el recorrido donde se puedan agregar acciones y eventos aplicables a las cuentas cuando no se produzca el evento, active la casilla de verificación **[!UICONTROL Establecer ruta de tiempo de espera]**.

   ![nodo de evento de Recorrido - establecer ruta de tiempo de espera](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Dividir rutas

Divida la audiencia en función de las condiciones del filtro.

>[!NOTE]
>
>Se admite un máximo de 25 rutas.

**Dividir rutas por cuentas**: las rutas divididas por cuentas pueden incluir acciones y eventos de personas y cuentas, y estas rutas se pueden dividir más.

_¿Cómo funciona un nodo de ruta dividida por cuentas?_

* Cuando agrega un nodo de ruta dividida y elige _Account_, cada ruta que se agrega incluye un nodo final con la capacidad de agregar nodos a cada borde.
* Es posible dividir la ruta por cuentas repetidamente, como en una manera anidada. Una ruta dividida incluye una opción para no añadir la ruta predeterminada.
* Las cuentas o personas que no cumplen los requisitos para una de las rutas divididas no avanzan en el recorrido.
* Estas rutas se pueden combinar mediante un nodo de combinación.

![nodo de Recorrido - dividir rutas por cuenta](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Dividir rutas por personas**: las rutas divididas por personas solo pueden incluir acciones de personas, y estas rutas no se pueden dividir de nuevo. Las rutas se unen automáticamente.

_¿Cómo funciona un nodo de ruta dividida por personas?_

* La ruta dividida por nodos de personas son nodos agrupados. Se combinan automáticamente para que todas las personas de la audiencia puedan pasar al siguiente paso sin perder el contexto de las cuentas a las que pertenecen.
* No se puede anidar la ruta dividida para las personas; no se puede agregar una ruta dividida para las personas que se encuentran en este nodo agrupado.
* La ruta dividida incluye una opción para no agregar una ruta predeterminada. Las cuentas o personas que no cumplen los requisitos no avanzan en el Recorrido.

![nodo de Recorrido: rutas divididas por personas](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

| Contexto del nodo | Condiciones de ruta | Descripción |
| ------------ | -------- | ----------- |
| [People](#add-a-split-path-by-people-node) | Atributos de la persona | |
| | Valor de datos cambiado (como el filtro en el historial de actividades) | |
| | Abrió el email | |
| | Hizo clic en el vínculo del email | |
| | Hizo clic en un vínculo de una página web | |
| | Ha tenido un momento interesante | |
| | Miembro del grupo comprador | |
| [Cuentas](#add-a-split-path-by-account-node) | Cambio en el valor de los datos de cuenta (por ejemplo, al filtrar el historial de actividades) | |

### Adición de una ruta dividida por nodo de cuenta

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Dividir rutas]**.

   ![Agregar nodo de recorrido - rutas divididas](./assets/add-node-split.png){width="300"}

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Cuentas]** para la división.

1. Para definir una condición aplicable a _[!UICONTROL Ruta 1]_, haga clic en **[!UICONTROL Aplicar condición]**.

   ![Nodo de ruta dividida - agregar condición](./assets/node-split-properties-apply-condition.png){width="500"}

1. En el editor de condiciones, añada uno o más filtros para definir la ruta dividida.

   * Arrastre y suelte los atributos de filtro desde la navegación izquierda y complete la definición de la coincidencia.

   * Ajuste las condiciones aplicando la **[!UICONTROL lógica de filtro]** en la parte superior. Puede elegir hacer coincidir todas las condiciones de atributo o cualquier condición.

     ![Nodo de ruta de división: lógica de filtro de condiciones](./assets/node-split-conditions.png){width="700" zoomable="yes"}

   * Haga clic en **[!UICONTROL Finalizado]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]** y repita los pasos anteriores para agregar las condiciones aplicables a esta ruta.

   También puede etiquetar cada ruta en función de estas condiciones o utilizar las etiquetas predeterminadas.

1. (Opcional) Agregue una ruta predeterminada para las cuentas que no cumplan los requisitos para las demás rutas. Si no es así, el recorrido finaliza para estas cuentas.

   ![Dividir propiedades de nodo de ruta - otras cuentas](./assets/node-split-properties-other-accounts.png){width="700" zoomable="yes"}

### Agregar un nodo de ruta dividida por personas

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Dividir rutas]**.

   ![Agregar nodo de recorrido - rutas divididas](./assets/add-node-split.png){width="300"}

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para la división.

1. Para definir una condición aplicable a _[!UICONTROL Ruta 1]_, haga clic en **[!UICONTROL Aplicar condición]**.

1. En el editor de condiciones, añada uno o más filtros para definir la ruta dividida.

   * Arrastre y suelte los atributos de filtro desde la navegación izquierda y complete la definición de la coincidencia.

   * Ajuste las condiciones aplicando la **[!UICONTROL lógica de filtro]** en la parte superior. Puede elegir hacer coincidir todas las condiciones de atributo o cualquier condición.

   * Haga clic en **[!UICONTROL Finalizado]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]** y repita los pasos anteriores para agregar las condiciones aplicables a esta ruta.

   También puede etiquetar cada ruta en función de estas condiciones o utilizar las etiquetas predeterminadas.

1. Por último, puede agregar una ruta predeterminada para las personas no cualificadas para las rutas anteriores. Si no, el recorrido termina para estas personas

Cuando haya definido condiciones para cada ruta en la que vaya a dividir la audiencia en personas, puede agregar las acciones que desee llevar a cabo con las personas.

>[!NOTE]
>
>Cuando se divide la audiencia por personas, solo se pueden agregar acciones de personas.

## Espera

Espere un tiempo determinado antes de pasar al siguiente paso.

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Esperar]**.

1. En las propiedades del nodo de la derecha, establezca **[!UICONTROL Duration]** de tiempo de espera antes de que el recorrido continúe con el siguiente nodo de la ruta.

![nodo de Recorrido: espera](./assets/node-wait.png){width="700" zoomable="yes"}

## Combinar rutas

Las diferentes rutas del recorrido se pueden combinar y descombinar con este nodo.

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Dividir rutas]**.

1. Haga clic en el nodo dividido para abrir sus propiedades a la derecha.

1. Haga clic en [!UICONTROL Agregar ruta] para crear tres rutas.

1. Agregue una combinación de acciones y eventos a cada ruta.

1. Haga clic en el icono de signo más ( **+** ) de cualquiera de estas rutas y elija **[!UICONTROL Combinar]** de las opciones que se muestran.

   ![nodo de Recorrido - rutas de combinación](./assets/node-plus-icon-merge-paths.png){width="400"}

1. En las propiedades del nodo de combinación, seleccione las rutas que desee combinar.

   ![nodo de Recorrido - rutas de combinación](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Ahora debería ver que las rutas se combinan para que las cuentas de las rutas seleccionadas se combinen en una sola ruta y puedan continuar avanzando a través del recorrido.

1. Si es necesario, puede anular la combinación de rutas volviendo a las propiedades del nodo de combinación y desactivando la casilla de verificación de las rutas que desee eliminar.
