---
title: Rutas de división de variante
description: Aprenda a utilizar nodos de ruta dividida de variante para distribuir cuentas o personas en varias rutas de recorrido mediante la asignación basada en porcentajes en Journey Optimizer B2B edition.
feature: Account Journeys, Person Journeys
solution: Journey Optimizer B2B Edition
role: User
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-08-17T19:14:54.674Z'
TQID: 'https://experienceleague.adobe.com/42lSbF7J-yEzFYbFFhs2sSQ4j4NfRtENlIz-R-HcPx8'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2: id: c31bc6c7-76bc-467b-80c0-7315a4e3f6beid: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: d378ca77-2da1-4f39-ad92-1917fe974a38
source-git-commit: b9abc88d05d5863ad57a19118fb905c394dbc76e
workflow-type: tm+mt
source-wordcount: 2018
ht-degree: 1%

---

# Rutas divididas de variantes

Use un nodo _Rutas divididas variables_ para distribuir cuentas o personas en dos o más rutas de recorrido según las asignaciones porcentuales que defina. Este nodo es útil cuando desea probar diferentes tácticas de mensajería, tiempo o participación en segmentos de su audiencia sin aplicar reglas condicionales.

>[!AVAILABILITY]
>
>El nodo _Variante dividida de rutas_ para recorridos de cuenta y persona está disponible para clientes seleccionados como una característica de disponibilidad limitada. Para obtener acceso, póngase en contacto con su representante de Adobe.

## Comparación por tipo de recorrido {#journey-type-comparison}

El nodo de rutas divididas de variante utiliza diferentes algoritmos de asignación según el tipo de recorrido. Comprender esta diferencia es importante para elegir el caso de uso correcto para cada tipo de recorrido.

| | Recorridos de la cuenta | Recorridos de persona |
| - | ---------------- | --------------- |
| **Algoritmo** | Asignación aleatoria basada en cuotas | Asignación de hash determinística |
| **Determinismo** | No determinista: la misma cuenta puede asignarse a una ruta diferente al volver a entrar, según el estado de la cuota actual. | Determinístico: siempre se asigna la misma persona a la misma ruta para un determinado recorrido publicado, independientemente de cuántas veces entre o vuelva a entrar. |
| **Pruebas A/B** | No adecuado: la asignación de rutas no es estable en las reentradas. | Adecuado: la asignación de rutas coherente por persona admite experimentos controlados y atribución. |
| **Comportamiento de reentrada** | La cuenta puede seguir una ruta diferente cada vez que entra en el recorrido. | La persona siempre sigue la misma ruta que se le asignó en la primera entrada. |
| **Precisión de distribución** | En una cuenta por ruta debido a la aplicación de cuotas. | Converge a un valor ±2% de los porcentajes configurados en 1000 o más entradas de recorrido. |

## Comparación con rutas divididas {#compare-split-paths}

Tanto _[Split paths](./split-merge-paths-nodes.md)_ como _Variant split paths_ dividen un recorrido en varias ramas (rutas), pero usan diferentes mecanismos:

| Aspecto | Dividir rutas | Rutas divididas de variantes |
| -------- | ----------- | ------------------- |
| **Lógica de asignación** | _Basado en reglas condicionales_: cada entidad se evalúa según las condiciones definidas y continúa en la primera ruta que coincida. | _Asignación basada en porcentajes_: las entidades se distribuyen entre rutas según porcentajes configurados sin condiciones de filtrado. |
| **Determinismo** | _Determinístico_: la misma entidad siempre sigue la misma ruta siempre que coincida con las mismas condiciones. | _Depende del tipo de recorrido_. Los recorridos de persona son determinísticos (la misma persona siempre sigue la misma ruta para un recorrido publicado). Los recorridos de cuenta no son determinísticos (basados en cuotas). |
| **Ruta de acceso de otras cuentas/personas** | _Compatible_: las entidades que no coinciden con ninguna ruta definida se pueden enrutar a una ruta predeterminada. | _No aplicable_: todas las entidades que llegan al nodo se asignan a una ruta. |
| **Ejemplo de uso** | Segmentar por cuenta conocida o atributos de persona; evaluación ordenada por prioridad. | Distribuya entidades para probar mensajes, temporización o tácticas. Recorridos de persona: adecuado para experimentos A/B. Recorridos de cuenta: idóneo para la distribución aleatoria sin coherencia por cuenta. |

## Recorridos de la cuenta {#account-journeys}

Para los recorridos de cuenta, el algoritmo de distribución usa [asignaciones aleatorias basadas en cuotas](#account-journeys--quota-based-random-assignment). Este algoritmo es **_no determinista_**: la misma cuenta podría asignarse a una ruta de acceso diferente cada vez que entre o vuelva a entrar en el recorrido. La asignación de rutas depende del estado de la cuota actual en el momento de la evaluación, no de una propiedad de cuenta fija.

### Dividir por cuenta {#split-by-account}

Cuando una cuenta alcanza un nodo de rutas divididas de variante, el motor en tiempo de ejecución evalúa cuántas cuentas ya se han asignado a cada ruta durante la instancia de recorrido actual y enruta la cuenta a la ruta más alejada de su cuota configurada.

* Cada cuenta se asigna exactamente a una ruta.
* La asignación se basa en cuotas. El algoritmo ajusta las asignaciones de forma dinámica para aproximarse a los porcentajes configurados en toda la población general.
* Dado que el algoritmo realiza un seguimiento de los recuentos de cuotas, la distribución real sólo se desplaza en una cuenta como máximo por ruta debido al redondeo cuando los totales no se dividen uniformemente.

### Dividido por personas {#split-by-people}

En un recorrido de cuentas, también puede usar un nodo de rutas divididas de variante para distribuir aleatoriamente a las _personas dentro de las cuentas_ entre las rutas basadas en porcentajes. Este tipo de división es útil cuando desea probar contenido o experiencias diferentes en el nivel de persona. Las cuentas siguen moviéndose por el recorrido. El nodo variante de rutas divididas por personas funciona con las siguientes protecciones:

* El nodo funciona como un _nodo agrupado_, que es una combinación de combinación dividida. Las rutas divididas se cierran automáticamente en un nodo de combinación correspondiente para que todas las personas puedan avanzar sin perder el contexto de su cuenta.
* Cada persona de la cuenta se asigna exactamente a una ruta en función de los porcentajes configurados.
* El mismo algoritmo basado en cuotas utilizado para las cuentas se aplica a las personas. La asignación de ruta no es determinista y la misma persona puede seguir una ruta diferente al volver a entrar.
* Solo se admiten _[!UICONTROL nodos de acción]_ para personas dentro de las rutas. Las rutas no se pueden dividir más.

>[!BEGINSHADEBOX &quot;Comportamiento de distribución entre personas&quot;]

Las personas de una cuenta se procesan como un lote. El número asignado a cada ruta se calcula como `floor(percentage / 100 × people_in_account)` y la **última ruta configurada recibe a todas las personas restantes**. Esto significa que:

* Cuando una cuenta tiene un número impar de personas, la última ruta recibe una persona más que las rutas anteriores.
* En el caso de las cuentas con una sola persona, esta siempre se asigna a la primera ruta independientemente de los porcentajes configurados.
* En el caso de las cuentas con muy pocas personas (menos de 10), la distribución por cuenta puede diferir considerablemente de los porcentajes configurados. La distribución converge hacia las proporciones configuradas cuando se mide en muchas cuentas.

>[!NOTE]
>
>Este redondeo se aplica por lote de cuentas, no a todas las cuentas del recorrido. La última ruta recibe sistemáticamente un poco más de personas que las configuradas cuando los tamaños de cuenta son impares. Este es el comportamiento esperado.

>[!ENDSHADEBOX]

## Recorridos de persona {#person-journeys}

Cuando una persona llega a un nodo de rutas divididas de variante, el motor de ejecución las asigna a una ruta en función de un hash de su ID y el ID de recorrido.

* Cada persona se asigna exactamente a una ruta.
* La asignación es determinista: la misma persona siempre recibe la misma asignación de ruta para un recorrido publicado determinado, independientemente de cuántas veces entre o vuelva a entrar.
* El hash solo se calcula a partir del ID de persona y el ID de recorrido. No depende de la posición del nodo, la hora de entrada ni ningún estado de cuota. Esto significa que al volver a entrar en el recorrido se produce la misma asignación de ruta cada vez.

>[!NOTE]
>
>**La división de variante del recorrido de persona es adecuada para pruebas A/B y experimentos.**
>
>Dado que la asignación es determinista y coherente en todas las reentradas, las rutas divididas de variante en los recorridos de persona admiten experimentos controlados en los que la misma persona debe recibir de forma consistente la misma experiencia. Utilice la vista [Detalles de recorrido](./journey-details.md) para supervisar la distribución en las rutas una vez que el recorrido esté activo.

## Algoritmo de distribución

El algoritmo de distribución aplicado depende del tipo de recorrido.

### Recorridos de cuenta: asignación aleatoria basada en cuotas

El nodo de rutas divididas de variante en los recorridos de cuenta usa un algoritmo de asignación aleatoria **basada en cuotas**. Cuando una cuenta llega al nodo, el motor en tiempo de ejecución evalúa cuántas cuentas ya se han asignado a cada ruta durante la instancia de recorrido actual y enruta la cuenta a la ruta más alejada de su cuota configurada.

**Propiedad de clave del algoritmo basado en cuotas:**

* La distribución realiza un seguimiento atento de los porcentajes configurados en todos los volúmenes de la cuenta. Dado que el algoritmo mantiene de forma activa los recuentos de cuotas, la distribución real sólo se desplaza en una cuenta como máximo por ruta debido al redondeo cuando los totales no se dividen uniformemente.

### Recorridos de persona: asignación de hash determinística

El nodo de rutas divididas de variante en los recorridos de personas usa un algoritmo de asignación hash **determinístico**. Cuando una persona llega al nodo, el motor en tiempo de ejecución calcula un valor hash a partir del ID de persona y el ID de recorrido y, a continuación, asigna el resultado a una ruta de acceso basada en los intervalos de porcentaje configurados. El algoritmo se aplica utilizando el siguiente flujo de trabajo:

1. El motor en tiempo de ejecución calcula un hash de MurmurHash3 de 32 bits a partir de una clave compuesta que combina el ID de persona y el ID de recorrido.
1. El valor hash se asigna a una posición en un rango de 10 000 bloques del mismo tamaño.
1. Los contenedores se dividen según los porcentajes de ruta configurados. Por ejemplo, con rutas al 30 %, 30 % y 40 %, los primeros 3000 contenedores corresponden a la Ruta 1, los siguientes 3000 a la Ruta 2 y los restantes 4000 a la Ruta 3.
1. La persona se asigna a la ruta cuyo intervalo de períodos contiene su posición hash.

Existen dos propiedades clave del algoritmo hash determinístico:

* **_Coherencia_**: siempre se asigna la misma persona al mismo espacio para un ID de recorrido determinado. Al volver a entrar en el recorrido, se asigna la misma ruta de acceso cada vez.
* **_Distribución estadística_**: la distribución converge a un ±2% de los porcentajes configurados cuando al menos 1.000 personas únicas han entrado en el recorrido. Con audiencias más pequeñas, los recuentos por ruta pueden diferir más notablemente de las proporciones configuradas.

## Limitaciones {#limitations}

Revise estas limitaciones antes de utilizar rutas divididas de variante en los recorridos.

### Limitaciones de recorrido de cuenta {#account-journey-limitations}

>[!IMPORTANT]
>
>**La asignación de ruta no es determinista.**
>
>El algoritmo basado en cuotas no garantiza que la misma cuenta siempre siga la misma ruta. Si una cuenta sale y vuelve a entrar en el recorrido, se le puede asignar una ruta diferente según el estado de la cuota en el momento de la reentrada. No utilice rutas divididas de variante de recorrido de cuentas para casos de uso que requieran una asignación de ruta por cuenta coherente en todas las instancias de recorrido.

| Limitación | Descripción |
| ---------- | ----------- |
| **No apto para experimentos controlados** | Dado que la asignación de rutas no es determinista, las rutas de acceso divididas de variante en los recorridos de cuenta no son **adecuadas** para experimentos A/B o escenarios de atribución que requieran que una cuenta determinada reciba el mismo tratamiento de manera consistente. |
| **Desviación menor de redondeo** | Cuando el recuento total de cuentas no es uniformemente divisible entre los porcentajes configurados, la distribución puede estar desactivada como máximo en una cuenta por ruta. Se espera este comportamiento de redondeo y no es un error. |
| **La asignación de ruta no es idempotente** | Volver a introducir el recorrido puede producir una asignación de ruta diferente para la misma cuenta. |
| **Sin filtrado condicional** | A diferencia de _Split paths_, las rutas divididas de variante no aplican condiciones. Cada cuenta que llega al nodo se asigna a una ruta. |

### Limitaciones del recorrido de personas {#person-journey-limitations}

| Limitación | Descripción |
| ---------- | ----------- |
| **Variación estadística a pequeña escala** | La distribución converge a los porcentajes configurados en aproximadamente el ±2 % cuando al menos 1000 personas únicas han entrado en el recorrido. Con menos entradas, los recuentos por ruta pueden diferir más notablemente de las proporciones configuradas. Este es el comportamiento esperado de la distribución hash y no es un error. |
| **Sin filtrado condicional** | A diferencia de _Split paths_, las rutas divididas de variante no aplican condiciones. Cada persona que llega al nodo se asigna a una ruta. |

## Agregar un nodo de rutas divididas de variante {#add-variant-split-paths-node}

Los pasos para agregar y configurar un nodo de ruta de división de variante son los mismos para los recorridos de cuenta y persona.

1. Vaya al mapa del recorrido.

1. Haga clic en el icono _Agregar_ ( **+** ) de una ruta y elija **[!UICONTROL Rutas divididas de variante]**.

   ![Agregar nodo de recorrido - rutas divididas de variante](./assets/node-variant-split-paths-add.png){width="300" zoomable="no"}

   En el mapa de recorrido, el nodo tiene dos rutas predeterminadas.

1. (_Solo recorridos de cuenta_) En las propiedades del nodo a la derecha, elija **[!UICONTROL Cuentas]** o **[!UICONTROL Personas]** para la división.

   Si usa el tipo _[!UICONTROL Personas]_, se inserta automáticamente un nodo _Cerrar rutas divididas de variante_ para cerrar la división agrupada.

   ![lienzo de Recorrido: variante dividida por personas con nodo de cierre insertado automáticamente](./assets/node-variant-split-paths-people-canvas.png){width="700" zoomable="yes"}

1. Revise o actualice la **[!UICONTROL Etiqueta]** para cada ruta.

   Las etiquetas de ruta aparecen como etiquetas de borde en el lienzo del recorrido y ayudan a distinguir las rutas en el análisis de recorrido.

   ![Nodo de rutas divididas de variante - configuración del nombre de ruta](./assets/node-variant-split-paths-names.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Percentage]** para cada ruta.

   Los valores deben ser enteros entre 1 y 99.

   ![Nodo de rutas divididas de variante - configuración de porcentaje de ruta](./assets/node-variant-split-paths-config.png){width="500" zoomable="yes"}

   El indicador de total actual muestra la suma de todos los porcentajes de ruta. El total debe ser igual exactamente al 100 % para poder publicar el recorrido. Se muestra un estado de error cuando el total no es igual a 100%.

   ![Nodo de rutas divididas de variante: error de validación cuando el total no es igual a 100%](./assets/node-variant-split-paths-validation-error.png){width="500" zoomable="yes"}

   Para distribuir los porcentajes uniformemente en todas las rutas, haga clic en **[!UICONTROL Distribuir uniformemente]**. El sistema calcula las acciones iguales y ajusta el redondeo para garantizar que el total sea igual al 100 %.

1. Para definir rutas adicionales, haga clic en **[!UICONTROL Agregar ruta]** para cada una.

   El nodo admite hasta 20 rutas. A medida que agregue más rutas, ajuste _[!UICONTROL Percentage]_ para que el total sea igual al 100%.

   Para quitar una ruta, haga clic en el icono _Eliminar_ ( ![Eliminar icono](../assets/do-not-localize/icon-delete-outline.svg) ) de la tarjeta de ruta. Una ruta solo se puede eliminar si quedan al menos dos rutas.

   Las siguientes reglas se aplican a la configuración de ruta dividida de variante. Publicación del recorrido de bloque de infracciones.

   | Regla | Requisito |
   | ---- | ----------- |
   | Rutas mínimas | 2 |
   | Rutas máximas | 20 |
   | Porcentaje por ruta | Entero de 1 a 99 |
   | Porcentaje total | Debe ser igual exactamente al 100 % |
