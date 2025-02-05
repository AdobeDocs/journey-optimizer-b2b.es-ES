---
title: Dividir y combinar rutas
description: Obtenga información acerca de los tipos de nodos de rutas de acceso divididas y rutas de acceso de combinación que puede utilizar para organizar los recorridos de la cuenta en Journey Optimizer B2B edition.
feature: Account Journeys
source-git-commit: af6e89b25ca20e14ec9a4c2ed4c8d632ad7c12dc
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 4%

---

# Dividir y combinar rutas

Utilice los nodos de ruta divididos y combinados en el recorrido de la cuenta para organizar los recorridos de la cuenta. Puede segmentar la audiencia según las condiciones que defina y combinar los segmentos para continuar.

## Dividir rutas

Agregue un nodo _Split paths_ para definir una o más rutas segmentadas según atributos de cuenta o personas.

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

* _Dividir ruta por personas_ nodos son nodos agrupados. Las rutas se combinan automáticamente para que todas las personas de la audiencia puedan pasar al siguiente paso sin perder el contexto de la cuenta.
* _No se pueden anidar los nodos de la ruta dividida por personas_; no se puede agregar la ruta dividida para personas en una ruta que se encuentre en este nodo agrupado.
* Los nodos de ruta dividida incluyen una opción para omitir una ruta predeterminada de modo que las cuentas o personas sin una ruta coincidente no avancen en el recorrido.
* _Los nodos de_ de la ruta dividida por personas admiten el uso de _relaciones entre la cuenta y la persona_, lo que permite filtrar a las personas según su rol (como contratista o empleado a tiempo completo), tal como se define en las plantillas de roles.

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
| | [!UICONTROL Filtros especiales] > [!UICONTROL Miembro de la lista] | La persona es o no es miembro de una o más listas de Marketo Engage. |
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

>[!NOTE]
>
>Cuando divide las rutas por personas, se inserta automáticamente un nodo _Cerrar rutas divididas_ para finalizar la división. Una ruta dividida por personas solo permite _realizar una acción_ en los nodos de personas.

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

>[!BEGINSHADEBOX &quot;inscripción a la lista de Marketo Engage&quot;]

En Marketo Engage, _Campañas inteligentes_ comprueba la pertenencia de los programas para asegurarte de que los posibles clientes no reciban correos electrónicos duplicados y no sean miembros de varios flujos de correos electrónicos al mismo tiempo. En Journey Optimizer B2B, puede comprobar la pertenencia a la lista de Marketo Engage como condición para que las personas dividan la ruta y así eliminar la duplicación en las actividades de recorrido.

Para ello, expanda **[!UICONTROL Filtros especiales]** y arrastre la condición **[!UICONTROL Miembro de la lista]** al espacio de filtro y complete la definición de filtro para evaluar la pertenencia a una o más listas de Marketo Engage.

![Condición de división de ruta por personas para pertenencia a lista de Marketo Engage](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

Cuando haya definido condiciones para cada ruta para dividir la audiencia en personas, puede agregar las acciones que desee realizar con las personas.

>[!NOTE]
>
>Cuando se divide la audiencia por personas, solo se pueden agregar acciones de personas hasta que las rutas se cierren o combinen.

## Combinar rutas

Agregue un nodo _Combinar rutas_ para combinar diferentes rutas divididas por cuenta en el recorrido.

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
