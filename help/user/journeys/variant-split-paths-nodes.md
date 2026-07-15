---
title: Rutas de división de variante
description: Aprenda a utilizar nodos de rutas divididas de variantes para distribuir aleatoriamente cuentas en varias rutas de recorridos mediante la asignación basada en porcentajes en Journey Optimizer B2B edition.
feature: Account Journeys
solution: Journey Optimizer B2B Edition
role: User
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-07-06T23:50:12.985Z'
TQID: 'https://experienceleague.adobe.com/42lSbF7J-yEzFYbFFhs2sSQ4j4NfRtENlIz-R-HcPx8'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2: id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 11e6c1954e3a99f3da6fc0967038d1c316991d07
workflow-type: tm+mt
source-wordcount: 1439
ht-degree: 2%

---

# Rutas divididas de variantes

Use un nodo _Rutas divididas variables_ para distribuir cuentas aleatoriamente en dos o más rutas de recorrido según las asignaciones porcentuales que defina. Este nodo es útil para pruebas exploratorias de diferentes tácticas de mensajería, temporización o participación en segmentos de la audiencia de la cuenta, sin aplicar reglas condicionales. No es adecuado para experimentos A/B controlados que requieran una asignación de ruta por cuenta coherente.

>[!AVAILABILITY]
>
>El nodo de rutas divididas de variante está disponible actualmente para clientes seleccionados como una versión beta limitada, solo para **_recorridos de cuenta_**. Se ha planificado la compatibilidad con los recorridos de persona para una versión futura. Para obtener acceso, póngase en contacto con su representante de Adobe.

## Comparación con rutas divididas {#compare-split-paths}

Tanto _[Dividir rutas](./split-merge-paths-nodes.md)_ como _Variante de rutas divididas_ dividen las cuentas en varias ramas de recorrido, pero usan mecanismos diferentes:

| Aspecto | Dividir rutas | Rutas divididas de variantes |
| -------- | ----------- | ------------------- |
| **Lógica de asignación** | _Basado en reglas condicionales_: cada cuenta se evalúa según las condiciones definidas y continúa en la primera ruta que coincida. | _Asignación aleatoria basada en porcentajes_: las cuentas se distribuyen entre rutas de acceso según porcentajes configurados sin condiciones de filtrado. |
| **Determinismo** | _Determinístico_ - La misma cuenta siempre sigue la misma ruta siempre que coincida con las mismas condiciones. | No determinista: la misma cuenta puede seguir diferentes rutas al volver a entrar. |
| **Ejemplo de uso** | Segmentar por cuenta conocida o atributos de grupo de compra; evaluación ordenada por prioridad. | Distribuya aleatoriamente cuentas para probar mensajería, temporización o tácticas en la audiencia de la cuenta. |
| **Ruta de acceso de otras cuentas** | _Compatible_: las cuentas que no coinciden con ninguna ruta definida se pueden enrutar a una ruta predeterminada. | _No aplicable_: cada cuenta se asigna a una de las rutas de acceso definidas. |

## Dividir por cuenta {#split-by-account}

Cuando una cuenta alcanza un nodo de rutas divididas de variante, el nodo la asigna exactamente a una ruta en función de los porcentajes configurados. La asignación utiliza un algoritmo basado en cuotas que registra cuántas cuentas se han asignado a cada ruta y se ajusta con el tiempo para mantener las proporciones configuradas.

* Cada cuenta se asigna exactamente a una ruta.
* La asignación es aleatoria y se basa en cuotas. El algoritmo ajusta las asignaciones de forma dinámica para aproximarse a los porcentajes configurados en toda la población general.
* El nodo admite de 2 a 20 rutas. Cada ruta tiene un nombre configurable y un porcentaje entero entre 1 y 99. La suma de todos los porcentajes de ruta debe ser igual exactamente al 100%.

>[!IMPORTANT]
>
>**Algoritmo basado en cuotas: no determinista**
>
>El algoritmo de distribución utiliza una asignación aleatoria basada en cuotas. Este algoritmo es **_no determinista_**: la misma cuenta podría asignarse a una ruta de acceso diferente cada vez que entre o vuelva a entrar en el recorrido. La asignación de rutas depende del estado de la cuota actual en el momento de la evaluación, no de una propiedad de cuenta fija. Consulte [Limitaciones](#limitations) para obtener detalles sobre los casos de uso a los que afecta esto.

### Algoritmo de distribución {#distribution-algorithm}

El nodo de rutas divididas de variante usa un algoritmo de asignación aleatoria **_basada en cuotas_**. Cuando una cuenta llega al nodo, el sistema evalúa las asignaciones de cuenta existentes para cada ruta y enruta la cuenta a la ruta más alejada de su cuota configurada. Existen dos propiedades clave para el algoritmo:

* La distribución realiza un seguimiento atento de los porcentajes configurados en todos los volúmenes de la cuenta. Dado que el algoritmo mantiene de forma activa los recuentos de cuotas, la distribución real sólo varía en una cuenta como máximo por ruta debido al redondeo cuando los totales no se dividen uniformemente.
* El algoritmo utiliza un bloqueo pesimista durante la evaluación de cuotas para serializar las asignaciones, lo que garantiza un seguimiento preciso del recuento en ejecución simultánea.

### Limitaciones {#limitations}

Revise estas limitaciones antes de utilizar rutas divididas de variante en los recorridos.

>[!CAUTION]
>
>**La asignación de ruta no es determinista.**
>
>El algoritmo basado en cuotas no garantiza que la misma cuenta siempre siga la misma ruta. Si una cuenta sale y vuelve a entrar en el recorrido, se le puede asignar una ruta diferente según el estado de la cuota en el momento de la reentrada. No utilice rutas divididas de variante para casos de uso que requieran una asignación de ruta por cuenta coherente en todas las instancias de recorrido.

| Limitación | Descripción |
| ---------- | ----------- |
| **No apto para experimentos controlados** | Como la asignación de rutas no es determinista, las rutas divididas de variante **no son adecuadas** para experimentos A/B o escenarios de atribución que requieran que una cuenta determinada reciba el mismo tratamiento de manera consistente. Los casos de uso que dependen de la coherencia por cuenta (como medir las tasas de respuesta o atribuir resultados a una experiencia específica) pueden producir resultados no fiables. |
| **Desviación menor de redondeo** | Cuando el recuento total de cuentas no es uniformemente divisible entre los porcentajes configurados, la distribución puede estar desactivada como máximo en una cuenta por ruta. Se espera este comportamiento de redondeo y no es un error. |
| **La asignación de ruta no es idempotente** | Volver a introducir el recorrido puede producir una asignación de ruta diferente para la misma cuenta. Si el diseño del recorrido supone que una cuenta siempre sigue la misma ruta después del nodo dividido, esta suposición no se sostiene. |
| **Solo recorridos de cuenta** | Las rutas divididas de variante solo se admiten en recorridos de cuenta. Actualmente no se admiten recorridos de persona. |
| **Sin filtrado condicional** | A diferencia de _Split paths_, las rutas divididas de variante no aplican condiciones. Cada cuenta que llega al nodo se asigna a una ruta. |

## Dividido por personas {#split-by-people}

En un recorrido de cuentas, también puede usar un nodo de rutas divididas de variante para distribuir aleatoriamente a las _personas dentro de las cuentas_ entre las rutas basadas en porcentajes. Este tipo de división es útil cuando desea probar contenido o experiencias diferentes en el nivel de persona a medida que las cuentas siguen moviéndose por el recorrido. El nodo variante de rutas divididas por personas funciona con las siguientes protecciones:

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

## Agregar un nodo de rutas divididas de variante {#add-variant-split-paths-node}

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Rutas divididas de variante]**.

   ![Agregar nodo de recorrido - rutas divididas de variante](./assets/node-variant-split-paths-add.png){width="300" zoomable="no"}

   El nodo agregado tiene dos rutas para iniciarse.

1. En las propiedades del nodo de la derecha, elija **[!UICONTROL Cuentas]** o **[!UICONTROL Personas]** para la división.

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

### Reglas de validación {#validation-rules}

Las siguientes reglas se aplican a la configuración de ruta dividida de variante. Publicación del recorrido de bloque de infracciones.

| Regla | Requisito |
| ---- | ----------- |
| Rutas mínimas | 2 |
| Rutas máximas | 20 |
| Porcentaje por ruta | Entero de 1 a 99 |
| Porcentaje total | Debe ser igual exactamente al 100 % |
