---
title: Nodos de Recorrido de cuenta
description: Obtenga información acerca de los tipos de nodos que puede utilizar para crear las recorridos de cuenta en Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: af72f5183cb1de56804340cbc9148de82faeca35
workflow-type: tm+mt
source-wordcount: '2443'
ht-degree: 9%

---

# Nodos del Recorrido de cuentas

Después de [crear un recorrido de cuenta](journey-overview.md#create-an-account-journey) y [agregar la audiencia](journey-overview.md#add-the-account-audience-for-your-journey), genere el recorrido mediante nodos. El mapa de recorrido proporciona un lienzo en el que puede crear sus casos de uso de marketing B2B de varios pasos.

Cree su recorrido de cuentas combinando los diferentes nodos de acción, evento y orquestación como un escenario de varios pasos y canales cruzados. Cada nodo de un recorrido representa un paso a lo largo de una ruta lógica. Utilice los siguientes tipos de nodos para construir un recorrido de cuentas:

* [Público de cuenta](#account-audience-node)
* [Realizar una acción](#take-an-action)
* [Escuchar un evento](#listen-for-an-event)
* [Dividir rutas](#split-paths)
* [Espera](#wait)
* [Combinar rutas](#merge-paths)

## Nodo Audiencia de cuenta

El nodo [Audiencia de cuenta](journey-overview.md#add-the-account-audience-for-your-journey) define la audiencia de cuenta de entrada (creada y administrada en Adobe Experience Platform) para el recorrido. Este nodo siempre es el primero y se crea automáticamente de forma predeterminada.

## Realizar una acción

Ejecute una acción como enviar un correo electrónico, cambiar una puntuación, asignar a un grupo comprador, etc.

**Acción en cuentas**: la acción se aplica a todas las personas que forman parte de cuentas en esta ruta.

**Acción en personas**: la acción se aplica a todas las personas de esta ruta. Se puede utilizar una acción en personas dentro de la ruta dividida por personas o por ruta dividida por cuentas.

### Acciones y restricciones {#action-nodes}

| Contexto del nodo | Acción | Restricciones |
| ------------ | ------ | ----------- |
| [People](#add-a-people-action) | Agregar a Lista | Seleccione el espacio de trabajo del Marketo Engage<br/>Nombre de lista |
| | Añadir a campaña de solicitud de Marketo Engage | Seleccione el espacio de trabajo del Marketo Engage<br/>Seleccionar campaña de solicitud |
| | Asignar a grupo de compra | Seleccionar interés de solución<br/>Seleccionar rol |
| | Cambiar la partición de personas en Marketo Engage | Nueva partición |
| | Cambiar calificación | Nombre de puntuación<br/>Cambiar |
| | Momento interesante de la persona | Escriba<br/>Descripción |
| | Eliminar del grupo de compra | Seleccionar interés de solución |
| | Quitar de Lista | Seleccione el espacio de trabajo del Marketo Engage<br/>Nombre de lista |
| | Enviar email | Crear nuevo correo electrónico<br/>Seleccionar correo electrónico del Marketo Engage |
| | Enviar SMS | Creación de SMS |
| [Cuentas](#add-an-account-action) | Valor de datos de cambio de cuenta | Seleccionar atributo<br/>Nuevo valor |
| | Momento interesante de la cuenta | Escriba (correo electrónico, hito o web)<br/>Descripción (opcional) |
| | Agregar cuenta a (otro) Recorrido | Seleccionar Recorrido de cuenta activa |
| | Quitar cuenta del Recorrido | Seleccionar Recorrido de cuenta activa |
| | Enviar alerta de ventas | Seleccionar interés de solución<br/>Enviar correo electrónico a |
| | Actualizar fase de grupo de compra | Seleccione el interés de la solución<br/>Seleccione la fase de compra del grupo |
| | Actualizar estado del grupo de compra | Seleccione el interés de la solución<br/>Estado (obligatorio, máximo 50 caracteres) |

### Agregar una acción de cuenta

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Realizar una acción]**.

   ![Agregar nodo de recorrido - realizar una acción](./assets/add-node-action.png){width="400"}

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

### Eventos y restricciones {#event-nodes}

| Contexto del nodo | Evento | Restricciones |
| ------------ | ----- | ----------- |
| [People](#add-a-people-event) | Asignado a grupo comprador | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Función</li><li>Fecha de la actividad</li><br/>Tiempo de espera (opcional) |
| | Hace clic en el vínculo del correo electrónico | Correo electrónico<br/>Restricciones adicionales (opcional): <li>Vínculo</li><li>Identificación del vínculo</li><li>Es un dispositivo móvil</li><li>Device</li><li>Plataforma</li><li>Explorador</li><li>Es contenido predictivo</li><li>Es actividad del bot</li><li>Patrón de actividad de bot</li><li>Explorador</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Haga clic en el enlace en SMS | Correo electrónico<br/>Restricciones adicionales (opcional): <li>Vínculo</li><li>Device</li><li>Plataforma</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Cambios en el valor de los datos | Atributo de persona<br/>Restricciones adicionales (opcional): <li>Nuevo valor</li><li>Valor anterior</li><li>Razón</li><li>Origen</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Abre el email | Correo electrónico<br/>Restricciones adicionales (opcional): <li>Vínculo</li><li>Identificación del vínculo</li><li>Es un dispositivo móvil</li><li>Device</li><li>Plataforma</li><li>Explorador</li><li>Es contenido predictivo</li><li>Es actividad del bot</li><li>Patrón de actividad de bot</li><li>Explorador</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Eliminado del grupo de compra | Interés de la solución<br/>Fecha de la actividad (opcional)<br/>Tiempo de espera (opcional) |
| | Se cambia el puntaje | Nombre de puntuación<br/>Restricciones adicionales (opcional):<li>Cambiar</li><li>Nuevo puntaje</li><li>Urgencia</li><li>Prioridad</li><li>Puntaje relativo</li><li>Urgencia relativa</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Devoluciones de SMS | Mensaje SMS<br/>Restricciones adicionales (opcional): <li>Fecha de la actividad</li><li>Número mínimo de veces</li><br/>Tiempo de espera (opcional) |
| [Cuentas](#add-an-account-event) | La cuenta tuvo un momento interesante | Escriba (correo electrónico, hito o web)<br/>restricciones adicionales (opcionales): <li>Descripción</li><li>Origen</li><li>Fecha de la actividad</li> <br/>Tiempo de espera (opcional) |
| | Cambio en el valor de datos de cuenta | Atributo<br/>Restricciones adicionales (opcional): <li>Nuevo valor</li><li>Valor anterior</li><li>Fecha de la actividad</li> <br/>Tiempo de espera (opcional) |
| | Cambio en la fase de grupo de compra | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nueva fase</li><li>Fase anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |
| | Cambio en el estado del grupo de compra | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nuevo estado</li><li>Estado anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |
| | Cambio en la puntuación de integridad | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nuevo puntaje</li><li>Puntuación anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |
| | Cambio en la puntuación de participación | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nuevo puntaje</li><li>Puntuación anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |

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

Si es necesario, defina la cantidad de tiempo que el recorrido espera el evento. El recorrido finaliza después de un tiempo de espera.

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

**Dividir rutas por cuentas**: las rutas divididas por cuentas pueden incluir acciones y eventos de personas y cuentas. Estas rutas se pueden dividir más.

_¿Cómo funciona un nodo de ruta dividida por cuentas?_

* Cuando agrega un nodo de ruta dividida y elige _Account_, cada ruta que se agrega incluye un nodo final con la capacidad de agregar nodos a cada borde.
* Es posible dividir la ruta por cuentas repetidamente, como en una manera anidada. Una ruta dividida incluye una opción para no añadir la ruta predeterminada.
* Si una cuenta o persona no cumple los requisitos para una de las rutas divididas, no avanza en el recorrido.
* Estas rutas se pueden combinar mediante un nodo de combinación.

![nodo de Recorrido - dividir rutas por cuenta](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Dividir rutas por personas**: las rutas se dividen por personas y solo pueden incluir acciones de personas. Estas rutas no se pueden volver a dividir y se vuelven a unir automáticamente.

_¿Cómo funciona un nodo de ruta dividida por personas?_

* La ruta dividida por nodos de personas son nodos agrupados. Las rutas se combinan automáticamente para que todas las personas de la audiencia puedan pasar al siguiente paso sin perder el contexto de la cuenta.
* No se puede anidar la ruta dividida para las personas; no se puede agregar una ruta dividida para las personas que se encuentran en este nodo agrupado.
* La ruta dividida incluye una opción para omitir una ruta predeterminada. Las cuentas o personas sin coincidencia en una ruta definida no avanzan en el Recorrido.
* La ruta dividida por personas admite el uso de _relaciones cuenta-persona_, lo que permite filtrar a las personas según su rol (como contratista o empleado a tiempo completo), tal como se define en las plantillas de roles.

![nodo de Recorrido: rutas divididas por personas](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Condiciones de ruta {#path-conditions}

| Contexto del nodo | Condiciones de ruta | Descripción |
| ------------ | --------------- | ----------- |
| [Cuentas](#add-a-split-path-by-account-node) | Atributos de la cuenta | Atributos del perfil de cuenta, incluidos: <li>Ingresos anuales</li><li>Ciudad</li><li>País</li><li>Cantidad de empleados</li><li>Industria</li><li>Nombre</li><li>Código SIC</li><li>Estado</li> |
| | [!UICONTROL Filtros especiales] > [!UICONTROL Tiene grupo de compra] | La cuenta tiene o no miembros de grupos de compra evaluados según uno o más de los siguientes criterios: <li>Interés de solución</li><li>Estado del grupo de compra</li><li>Puntuación de integridad</li><li>Puntaje de participación</li> |
| [Personas](#add-a-split-path-by-people-node) > [!UICONTROL Solo atributos de personas] | [!UICONTROL Atributos de persona] | Atributos del perfil de la persona, incluidos: <li>Ciudad</li><li>País</li><li>Fecha de nacimiento</li><li>Dirección de correo electrónico</li><li>Email no válido</li><li>Email suspendido</li><li>Nombre</li><li>Región del estado inferida</li><li>Cargo</li><li>Apellido</li><li>Número de teléfono móvil</li><li>Número de teléfono</li><li>Código postal</li><li>Estado</li><li>Suscripción cancelada</li><li>Razón de la cancelación de la suscripción</li> |
| | [!UICONTROL Historial de actividades] > [!UICONTROL Correo electrónico] | Actividades de correo electrónico asociadas con el recorrido: <li>[!UICONTROL Se hizo clic en el vínculo del correo electrónico]</li><li>Abrió el email</li><li>Se entregó el email</li><li>Se envió email</li> Estas condiciones se evalúan utilizando un mensaje de correo electrónico seleccionado de anteriormente en el recorrido. |
| | [!UICONTROL Historial de actividades] > [!UICONTROL Se ha cambiado el valor de los datos] | Se ha producido un cambio de valor en un atributo de persona seleccionado. Estos tipos de cambio incluyen: <li>Nuevo valor</li><li>Valor anterior</li><li>Razón</li><li>Origen</li><li>Fecha de la actividad</li><li>Mín. número de veces</li> |
| | [!UICONTROL Historial de actividades] > [!UICONTROL Ha tenido un momento interesante] | Actividad de momento interesante que se define en la instancia de Marketo Engage asociada. Las restricciones incluyen: <li>Hito</li><li>Correo electrónico</li><li>Web</li> |
| | [!UICONTROL Filtros especiales] > [!UICONTROL Miembro del grupo comprador] | La persona es o no un miembro del grupo comprador evaluado según uno o más de los siguientes criterios: <li>Interés de solución</li><li>Estado del grupo de compra</li><li>Puntuación de integridad</li><li>Puntaje de participación</li><li>Función</li> |
| [Personas](#add-a-split-path-by-people-node) > [!UICONTROL Solo atributos de cuenta-persona] | Rol en atributos de cuenta | La persona tiene o no una función asignada en la cuenta. Restricciones opcionales: <li>Introduzca un nombre de rol</li> |

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

     ![Nodo de ruta de división: condiciones de cuentas, lógica de filtro](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Haga clic en **[!UICONTROL Finalizado]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]** y repita los pasos anteriores para agregar las condiciones aplicables a esta ruta.

   También puede etiquetar cada ruta en función de estas condiciones o utilizar las etiquetas predeterminadas.

1. Si es necesario, reordene las rutas según la prioridad que desee para la división.

   El filtrado de rutas se evalúa en orden descendente. Cada cuenta procede por la primera ruta que coincida.

   Haga clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista de rutas.

   ![Nodo de ruta dividida - reordenar rutas](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"}

1. Habilite la opción **[!UICONTROL Otras cuentas]** para agregar una ruta predeterminada para las cuentas que no coinciden con las rutas definidas. Si no, el recorrido termina para estas personas.

### Agregar un nodo de ruta dividida por personas

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Dividir rutas]**.

   ![Agregar nodo de recorrido - rutas divididas](./assets/add-node-split.png){width="300"}

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para la división.

1. Establezca los **[!UICONTROL Atributos utilizados para las condiciones]**.

   * Elija **[!UICONTROL Solo atributos de personas]** para usar condiciones relacionadas con el perfil de la persona y los eventos.
   * Elija **[!UICONTROL Solo atributos de cuenta-persona]** para usar condiciones relacionadas con la pertenencia a funciones de la persona en una cuenta.

1. Para definir una condición aplicable a _[!UICONTROL Ruta 1]_, haga clic en **[!UICONTROL Aplicar condición]**.

1. En el editor de condiciones, añada uno o más filtros para definir la ruta dividida.

   * Arrastre y suelte cualquiera de los atributos de personas desde la navegación izquierda y complete la definición de la coincidencia.

     >[!NOTE]
     >
     >Si tiene campos de persona personalizados definidos en el esquema de audiencia de cuenta en Experience Platform, estos campos también están disponibles para usarlos como atributos de persona en condiciones.

   * Ajuste las condiciones aplicando la **[!UICONTROL lógica de filtro]** en la parte superior. Puede elegir hacer coincidir todas las condiciones de atributo o cualquier condición.

     ![Nodo de ruta de división: lógica de filtro de persona de condiciones](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Haga clic en **[!UICONTROL Finalizado]**.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]** y repita los pasos anteriores para agregar las condiciones aplicables a esta ruta.

   También puede etiquetar cada ruta en función de estas condiciones o utilizar las etiquetas predeterminadas.

1. Si es necesario, reordene las rutas según la prioridad que desee para la división.

   El filtrado de rutas se evalúa en orden descendente. Cada persona continúa por el primer camino que coincida.

   Haga clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista de rutas.

   ![Nodo de ruta dividida - reordenar rutas](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"}

1. Habilite la opción **[!UICONTROL Otras personas]** para agregar una ruta predeterminada para las personas que no coinciden con las rutas definidas. Si no, el recorrido termina para estas personas.

Cuando haya definido condiciones para cada ruta para dividir la audiencia en personas, puede agregar las acciones que desee realizar con las personas.

>[!NOTE]
>
>Cuando se divide la audiencia por personas, solo se pueden agregar acciones de personas hasta que las rutas se cierren o combinen.

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

1. En las propiedades del nodo de rutas de combinación, seleccione las rutas que desee combinar.

   ![nodo de Recorrido - rutas de combinación](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   En este punto, las rutas se combinan para que las cuentas de las rutas seleccionadas se combinen en una sola ruta que pueda continuar avanzando a través del recorrido.

1. Si es necesario, puede anular la combinación de rutas volviendo a las propiedades del nodo de rutas de combinación y desactivando la casilla de verificación de las rutas que desee eliminar.
