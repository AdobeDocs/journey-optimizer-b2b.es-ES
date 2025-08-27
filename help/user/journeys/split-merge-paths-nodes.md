---
title: Dividir y combinar rutas
description: Obtenga información acerca de los tipos de nodos de rutas de acceso divididas y rutas de acceso de combinación que puede utilizar para organizar los recorridos de la cuenta en Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
source-git-commit: eb80b57b0481837a50c7c0985ac4dc5d71f3577e
workflow-type: tm+mt
source-wordcount: '2107'
ht-degree: 4%

---

# Dividir y combinar rutas

Utilice los nodos de ruta divididos y combinados en el recorrido de cuentas para segmentar personas o cuentas según las condiciones que defina. Puede definir rutas para la audiencia de recorrido o la lista de cuentas según las condiciones, definir cada ruta con nodos de acción y evento para cada segmento y, a continuación, combinar las rutas y continuar con el recorrido.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

Un nodo _Split paths_ define una o más rutas segmentadas en función de la cuenta de **_o bien_** o de los filtros de personas. Una división basada en un filtro de personas se cierra automáticamente con un nodo de rutas de combinación para que todas las personas puedan pasar al siguiente paso sin perder el contexto de su cuenta.

>[!NOTE]
>
>Se admite un máximo de 25 rutas.

## Dividir rutas por cuentas

Dividir por rutas de cuentas puede incluir acciones y eventos de cuenta y personas. Estas rutas se pueden dividir más.

_&#x200B;**Funcionamiento de un nodo de ruta dividida por cuentas**&#x200B;_

* Cada ruta que agregue incluirá un nodo final con la capacidad de agregar nodos a cada borde.
* Dividir por nodos de cuenta se puede anidar (puede dividir la ruta por cuentas repetidamente).
* La evaluación de cada ruta es de arriba abajo. Si una cuenta coincide para la primera y la segunda ruta, solo continúa en la primera ruta.
* Se pueden combinar dos o más rutas mediante un nodo de combinación.
* El nodo admite la definición de una ruta de acceso de _[!UICONTROL Otras cuentas]_, donde puede agregar acciones o eventos para cuentas que no coincidan con uno de los segmentos o rutas definidos.

![nodo de Recorrido - dividir rutas por cuenta](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

### Condiciones de ruta de cuenta

| Condiciones de ruta | Descripción |
| --------------- | ----------- |
| Atributos de la cuenta | Atributos del perfil de cuenta, incluidos: <li>Ingresos anuales <li>Ciudad <li>País <li>Cantidad de empleados <li>Industria <li>Nombre <li>Código SIC <li>Estado |
| [!UICONTROL Filtros especiales] > [!UICONTROL Tiene grupo de compra] | La cuenta tiene o no miembros de grupos compradores. También se puede evaluar con uno o más de los siguientes criterios: <li>Interés de solución <li>Estado del grupo de compra <li>Puntuación de integridad <li>Puntaje de participación |

### Adición de una ruta dividida por nodo de cuenta

1. Vaya al mapa del recorrido.

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

1. Habilite la opción **[!UICONTROL Otras cuentas]** para definir la ruta predeterminada de las cuentas que no coinciden con los segmentos o rutas definidos.

   Cuando esta opción no está habilitada, el recorrido finaliza para las cuentas que no coinciden con un segmento o ruta definida dentro de la división.

## Dividir rutas por personas

Dividir por rutas de personas solo puede incluir acciones de personas. Estas rutas no se pueden volver a dividir y se vuelven a unir automáticamente.

_&#x200B;**Funcionamiento de un nodo de ruta dividida por personas**&#x200B;_

* Dividido por nodos de personas funciona dentro de una combinación de _nodo agrupado_ de combinación dividida. Las rutas divididas se combinan automáticamente para que todas las personas puedan pasar al siguiente paso sin perder el contexto de su cuenta.
* No se pueden anidar nodos divididos por personas (no se puede agregar una ruta dividida para personas en una ruta que se encuentre en este nodo agrupado).
* La evaluación de cada ruta es de arriba abajo. Si una persona coincide para la primera y la segunda ruta, solo continúa por la primera ruta.
* El nodo admite el uso de _relaciones cuenta-persona_, lo que le permite filtrar a las personas según su función (como contratista o empleado a tiempo completo) según se defina en la relación.
* El nodo admite la definición de una ruta de acceso de _[!UICONTROL Otras personas]_, donde puede agregar acciones o eventos para las personas que no coincidan con uno de los segmentos o rutas definidos.

![nodo de Recorrido: rutas divididas por personas](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Condiciones de ruta de personas

| Condiciones de ruta | Descripción |
| --------------- | ----------- |
| [!UICONTROL Historial de actividades] > [!UICONTROL Correo electrónico] | Actividades de correo electrónico basadas en condiciones que se evalúan utilizando uno o más mensajes de correo electrónico seleccionados de anteriormente en el recorrido: <li>[!UICONTROL Se hizo clic en el vínculo del correo electrónico] <li>Abrió el email <li>Se entregó el email <li>Se envió el correo electrónico <br>**[!UICONTROL Cambiar al filtro de inactividad &#x200B;]**. Use esta opción para filtrar según la falta de actividad (una persona no tuvo la actividad de correo electrónico). |
| [!UICONTROL Historial de actividades] > [!UICONTROL Mensaje SMS] | Actividades de SMS basadas en condiciones que se evalúan utilizando uno o más mensajes SMS seleccionados de anteriormente en el recorrido: <li>[!UICONTROL Se hizo clic en un vínculo en SMS] <li>[!UICONTROL SMS rechazado] <br>**[!UICONTROL Cambiar al filtro de inactividad &#x200B;]**: use esta opción para filtrar según la falta de actividad (una persona no tuvo la actividad de SMS). |
| [!UICONTROL Historial de actividades] > [!UICONTROL Se ha cambiado el valor de los datos] | Se ha producido un cambio de valor en un atributo de persona seleccionado. Estos tipos de cambio incluyen: <li>Nuevo valor<li>Valor anterior<li>Razón<li>Origen<li>Fecha de la actividad<li>Mín. número de veces <br>**[!UICONTROL Cambiar al filtro de inactividad &#x200B;]**: utilice esta opción para filtrar según la falta de actividad (una persona no tuvo un cambio de valor de datos). |
| [!UICONTROL Historial de actividades] > [!UICONTROL Ha tenido un momento interesante] | Actividad de momento interesante que se define en la instancia de Marketo Engage asociada. Las restricciones incluyen: <li>Hito<li>Correo electrónico<li>Web <br>**[!UICONTROL Cambiar al filtro de inactividad &#x200B;]**: utilice esta opción para filtrar según la falta de actividad (una persona no ha tenido un momento interesante). |
| [!UICONTROL Historial de actividades] > [!UICONTROL Página web visitada] | Actividad de página web que se utiliza para una o varias páginas web administradas por la instancia de Marketo Engage asociada. Las restricciones incluyen: <li>Página web (obligatorio)<li>Fecha de la actividad<li>Dirección IP del cliente <li>Querystring <li>Referente <li>Agente de usuario <li>Motor de búsqueda <li>Consulta de búsqueda <li>URL personalizada <li>Token <li>Explorador <li>Plataforma <li>Device <li>Mín. número de veces <br>**[!UICONTROL Cambiar al filtro de inactividad &#x200B;]**: utilice esta opción para filtrar según la falta de actividad (una persona no visitó la página web). |
| [!UICONTROL Atributos de persona] | Atributos del perfil de la persona, incluidos: <li>Ciudad <li>País <li>Fecha de nacimiento <li>Dirección de correo electrónico <li>Email no válido <li>Email suspendido <li>Nombre <li>Región del estado inferida<li>Cargo <li>Apellido <li>Número de teléfono móvil <li>Puntuación de participación de persona <li>Número de teléfono <li>Código postal <li>Estado <li>Suscripción cancelada <li>Razón de la cancelación de la suscripción |
| [!UICONTROL Filtros especiales] > [!UICONTROL Miembro del grupo comprador] | La persona es o no un miembro del grupo comprador evaluado según uno o más de los siguientes criterios: <li>Interés de solución</li><li>Estado del grupo de compra</li><li>Puntuación de integridad</li><li>Puntaje de participación</li><li>Función</li> |
| [!UICONTROL Filtros especiales] > [!UICONTROL Miembro de la lista] | La persona es o no es miembro de una o más listas de Marketo Engage. |
| [!UICONTROL Filtros especiales] > [!UICONTROL Miembro del programa] | La persona es o no es miembro de uno o más programas de Marketo Engage. |

### Condiciones de ruta de persona-cuenta

| Condiciones de ruta | Descripción |
| --------------- | ----------- |
| [!UICONTROL Rol en la cuenta] | La persona tiene o no una función asignada en la cuenta. Restricciones opcionales: <li>Nombre de la función |

### Agregar un nodo de ruta dividida por personas

>[!NOTE]
>
>Cuando divide las rutas por personas, se inserta automáticamente un nodo _Cerrar rutas divididas_ para finalizar la división. Una ruta dividida por personas solo permite _realizar una acción_ en los nodos de personas.

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Dividir rutas]**.

   ![Agregar nodo de recorrido - rutas divididas](./assets/add-node-split.png){width="300"}

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para la división.

1. Establezca los **[!UICONTROL Atributos utilizados para las condiciones]**.

   * Elija **[!UICONTROL Solo atributos de personas]** para usar condiciones relacionadas con el perfil de la persona.
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

1. Habilite la opción **[!UICONTROL Otras personas]** para agregar una ruta predeterminada para las personas que no coinciden con las rutas definidas.

   Cuando esta opción no está habilitada, las personas que no coinciden con un segmento o ruta definida pasan la división y continúan con el siguiente paso del recorrido.

   Cuando haya definido condiciones para cada ruta para dividir la audiencia en personas, puede agregar las acciones que desee realizar con las personas.

### Filtrado de actividades

Para una ruta dividida por personas, puede definir una ruta según la actividad de la persona relacionada con lo siguiente:

* Mensajes de correo electrónico de versiones anteriores del recorrido
* Mensajes SMS de anteriores versiones del recorrido
* Cambio en el valor de los datos en el perfil de la persona
* Un momento interesante (rastreado en Marketo Engage) asociado con un correo electrónico, una página web o un hito
* Visita a una página web rastreada en Marketo Engage

>[!BEGINSHADEBOX &quot;Filtro de inactividad&quot;]

Para cada uno de los filtros _[!UICONTROL Historial de actividades]_, puede habilitar la opción **[!UICONTROL Cambiar al filtro de inactividad]**. Esta opción cambia el filtro a una evaluación para una ausencia de ese tipo de actividad. Por ejemplo, si desea crear una ruta de acceso para las personas que _&#x200B;**no**&#x200B;_ abrieron un mensaje de correo electrónico con anterioridad en el recorrido, agregue el filtro _[!UICONTROL Correo electrónico]_ > _[!UICONTROL Correo electrónico abierto]_. Active la opción de inactividad y especifique el correo electrónico. Se recomienda usar la restricción _[!UICONTROL Fecha de actividad]_ para definir un período de tiempo para la inactividad.

![Condición de división de ruta por personas para comprar la membresía del grupo](./assets/node-split-people-condition-inactivity.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

### Filtrado de pertenencia

Dentro de la sección _[!UICONTROL Filtros especiales]_, hay varios filtros que puedes usar para evaluar la pertenencia de una persona a un grupo de compras o a una lista de Marketo Engage. Por ejemplo, si desea crear una ruta para las personas que son miembros de un grupo comprador y se les asigna una función en particular, agregue el filtro _[!UICONTROL Filtros especiales]_ > _[!UICONTROL Miembro del grupo comprador]_. Para el filtro, establezca la pertenencia como _true_, seleccione un _[!UICONTROL interés de solución]_ que esté asociado con uno o más grupos compradores y establezca la _[!UICONTROL función]_ con la que desee hacer coincidir.

![Condición de división de ruta por personas para comprar la membresía del grupo](./assets/node-split-people-condition-buying-group-membership.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX &quot;inscripción a la lista Marketo Engage&quot;]

En Marketo Engage, _Campañas inteligentes_ comprueba la pertenencia de los programas para asegurarte de que los posibles clientes no reciban correos electrónicos duplicados y no sean miembros de varios flujos de correos electrónicos al mismo tiempo. En Journey Optimizer B2B, puede comprobar la pertenencia a listas de Marketo Engage como condición para que las personas puedan dividir la ruta y ayudar a eliminar la duplicación en las actividades de recorrido.

Para usar la pertenencia a una lista en una condición dividida, expanda **[!UICONTROL Filtros especiales]** y arrastre la condición **[!UICONTROL Miembro de la lista]** al espacio de filtro. Complete la definición del filtro para evaluar la pertenencia a una o varias listas de Marketo Engage.

![Condición de división de ruta por personas para la pertenencia a la lista de Marketo Engage](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

## Combinar rutas

Agregue un nodo _Combinar rutas_ para combinar diferentes rutas divididas por cuenta en el recorrido.

1. Vaya al mapa del recorrido.

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

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3443259/?learn=on&captions=spa)
