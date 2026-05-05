---
title: Nodos externos
description: Aprenda a utilizar los nodos Acción externa y Ruta de división externa en recorridos de cuenta para conectarse con servicios externos y enrutar cuentas y personas en función de la respuesta del servicio.
feature: Account Journeys, Integrations
role: User
exl-id: fc0d6baa-d2e9-4a28-9d78-c74b99282ec1
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2: id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 0216cf3b1cbc1124b50ad99e649778aef71f5aca
workflow-type: tm+mt
source-wordcount: 870
ht-degree: 0%

---

# Nodos externos

Utilice nodos externos para conectar la recorrido de la cuenta con un servicio externo. Cuando la audiencia de una cuenta llega a uno de estos nodos, Journey Optimizer B2B edition envía asincrónicamente datos de atributos de audiencia al servicio externo. El servicio procesa los datos y responde con una llamada de retorno, devolviendo la información de la audiencia y los metadatos que el recorrido utiliza para continuar.

>[!NOTE]
>
>Los nodos de acción externa solo están disponibles en recorridos de cuenta. No son compatibles con los recorridos de persona.
>
>Un administrador debe [configurar y activar la acción externa](../admin/configure-external-actions.md) antes de que los especialistas en marketing agreguen e implementen estos nodos en un recorrido.

Existen dos tipos de nodos de acción externa:

* **[Acción externa](#external-action)**: llama a un servicio externo y continúa en una sola ruta de salida. Utilice este nodo cuando desee almacenar en déclencheur un proceso externo sin lógica de ramificación, como actualizar un registro en un sistema externo o enviar una señal a un servicio descendente.
* **[Rutas divididas externas](#external-split-paths)**: llama a un servicio externo y evalúa la respuesta para enrutar cuentas a lo largo de una de varias rutas definidas. Utilice este nodo cuando el servicio externo devuelva un valor, como una puntuación, nivel o clasificación, que determina el siguiente paso del recorrido.

## Nodo de acción externa {#external-action}

El nodo _Acción externa_ llama a un servicio externo y continúa en una sola ruta de salida, independientemente del contenido de la respuesta. Utilícelo para integraciones en las que no sea necesaria la bifurcación después de la llamada externa.

1. Vaya al mapa de recorrido de la cuenta.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Acción externa]**.

   ![Agregar un nodo de acción externa](./assets/node-external-action.png){width="400"}

1. En las propiedades del nodo de la derecha, establezca la **[!UICONTROL Acción en]** contexto para la acción externa:

   * Elija **[!UICONTROL Cuentas]** cuando desee aplicar la acción externa a todas las personas que formen parte de cuentas en la ruta del nodo.
   * Elija **[!UICONTROL Personas]** cuando desee aplicar un cambio a todas las personas en la ruta del nodo.

1. Seleccione el **[!UICONTROL nombre de servicio]** externo.

   ![Nodo de acción externa: seleccione el servicio externo](./assets/node-external-action-service-name.png){width="600" zoomable="yes"}

   La lista incluye todas las acciones externas configuradas que están activas y designadas para el tipo _Acción externa_ y el contexto.

1. Si el servicio tiene atributos globales, introduzca los valores necesarios en los campos que se muestran debajo del nombre del servicio.

1. Continúe creando la recorrido desde las rutas de salida del nodo.

   La ruta de acceso _[!UICONTROL Tiempo de espera o error]_ se crea automáticamente. Si el período de tiempo de espera (como se configura en el servicio) transcurre antes de recibir una respuesta, la cuenta o la persona progresa por esta ruta. Es lo mismo si se recibe una respuesta de error. Puede añadir nodos de recorrido a esta ruta para gestionar estos escenarios o el recorrido termina para el miembro de la audiencia.

## Nodo de rutas divididas externas {#external-split-paths}

El nodo Rutas de acceso divididas externas llama a un servicio externo y utiliza la respuesta para determinar qué cuentas de ruta de acceso son las siguientes. Cada ruta está definida por una condición basada en una variable (descriptor de acceso) devuelta por el servicio externo. El recorrido evalúa la respuesta con respecto a las condiciones de ruta definidas y enruta cada cuenta a lo largo de la primera ruta coincidente. Las condiciones de ruta se evalúan en orden descendente. Cada cuenta continúa con la primera ruta cuya condición coincida con el valor devuelto por el servicio externo.

1. Vaya al mapa de recorrido de la cuenta.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Rutas de división externas]**.

   ![Agregar un nodo de ruta dividida externa](./assets/node-external-split-path.png){width="400"}

1. En las propiedades del nodo a la derecha, elija un tipo **[!UICONTROL Dividir rutas por]**:

   * **[!UICONTROL Cuentas]**: para las rutas divididas por cuentas, puede agregar nodos de cuenta y de personas dentro de las rutas definidas.
   * **[!UICONTROL Personas]**: para las rutas divididas por personas, solamente puede agregar nodos de acción de personas dentro de las rutas definidas. Una división basada en personas se cierra automáticamente con un nodo _[!UICONTROL Combinar rutas]_ para que todas las personas puedan pasar al siguiente paso sin perder el contexto de su cuenta.

1. Seleccione el **[!UICONTROL nombre del servicio]**.

1. Si la configuración del servicio tiene _atributos globales_, escriba los valores requeridos en los campos que aparecen debajo del nombre del servicio.

1. Para _[!UICONTROL Ruta 1]_, defina la condición de bifurcación:

   * Para **[!UICONTROL Label]**, reemplace el valor predeterminado con una etiqueta más descriptiva.
   * Para **[!UICONTROL Seleccionar variable]**, elija un descriptor de acceso. Los descriptores de acceso son valores que devuelve el servicio externo y se definen cuando se configura la acción.
   * Para **[!UICONTROL Seleccionar operador]**, elija el operador.
   * Para **[!UICONTROL Introducir valores]**, escriba el valor con el que se debe hacer coincidir.

   ![Nodo de ruta dividida externa: establezca la condición de ruta mediante una variable de servicio](./assets/node-external-split-path-properties.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Las variables de condición disponibles y el contexto de recorrido admitido (_Cuenta_, _Personas_ o _Personas en la Cuenta_) están determinados por la configuración de acción externa. Póngase en contacto con el administrador si el servicio o las variables esperados no están disponibles.

1. Para agregar más rutas, haga clic en **[!UICONTROL Agregar ruta]** y defina una condición para cada una de las rutas que necesite.

1. Continúe creando la recorrido desde cada ruta de salida del nodo.

   La ruta de acceso _[!UICONTROL Tiempo de espera o error]_ se crea automáticamente. Si el período de tiempo de espera (como se configura en el servicio) transcurre antes de recibir una respuesta, la cuenta o la persona progresa por esta ruta. Es lo mismo si se recibe una respuesta de error. Puede añadir nodos de recorrido a esta ruta para gestionar estos escenarios o el recorrido termina para el miembro de la audiencia.

1. Para _Dividir por cuentas_, puede agregar un [nodo de rutas de combinación](./split-merge-paths-nodes.md#merge-paths) para combinar dos o más rutas según sea necesario.
