---
title: Escuchar un evento
description: Obtenga información acerca del tipo de nodo Escuchar un evento que puede utilizar para organizar las recorridos de su cuenta en Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: 632eee973730f527ea0314c6affe5a49a72e3945
workflow-type: tm+mt
source-wordcount: '1373'
ht-degree: 12%

---

# Escuchar un evento

Agregue el nodo _Escuchar un evento_ para mover la audiencia al siguiente paso en el recorrido de la cuenta cuando se produzca un evento.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea el vídeo de información general](#overview-video)

>[!NOTE]
>
>No puede agregar este tipo de nodo en la ruta dividida por personas.

## Eventos de cuenta

Escuche un evento basado en la cuenta cuando desee mover la cuenta hacia adelante en el recorrido según los eventos activados por la actividad de la cuenta.

### Eventos y restricciones

| Evento | Restricciones |
| ----- | ----------- |
| La cuenta tuvo un momento interesante | Escriba (correo electrónico, hito o web)<br/>restricciones adicionales (opcionales): <li>Descripción</li><li>Origen</li><li>Fecha de la actividad</li> <br/>Tiempo de espera (opcional) |
| Cambio en el valor de datos de cuenta | Atributo<br/>Restricciones adicionales (opcional): <li>Nuevo valor</li><li>Valor anterior</li><li>Fecha de la actividad</li> <br/>Tiempo de espera (opcional) |
| Cambio en la fase de grupo de compra | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nueva fase</li><li>Fase anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |
| Cambio en el estado del grupo de compra | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nuevo estado</li><li>Estado anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |
| Cambio en la puntuación de integridad | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nuevo puntaje</li><li>Puntuación anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |
| Cambio en la puntuación de participación | Interés en la solución<br/>Restricciones adicionales (opcional): <li>Nuevo puntaje</li><li>Puntuación anterior</li><li>Fecha de la actividad</li>Tiempo de espera de <br/> (opcional) |

### Agregar un evento de cuenta

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

1. En las propiedades del nodo de la derecha, elija **[!UICONTROL Cuentas]** para el tipo de evento.

   ![nodo de Recorrido: escucha eventos en la cuenta](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Seleccione un evento de la lista.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

## Eventos de personas

Escuche un evento basado en personas cuando desee mover la cuenta hacia adelante en el recorrido según los eventos activados por la actividad de personas.

### Eventos y restricciones

| Tipo de entrada | Evento | Restricciones |
| ---------- | ----- | ----------- |
| Edición B2B de Journey Optimizer | Asignado a grupo comprador | Interés en la solución<br/><br/>Restricciones adicionales (opcional): <li>Función</li><li>Fecha de la actividad</li><br/>Tiempo de espera (opcional) |
| | Hace clic en el vínculo del correo electrónico | Correo electrónico<br/><br/>Restricciones adicionales (opcional): <li>Vínculo</li><li>Identificación del vínculo</li><li>Es un dispositivo móvil</li><li>Device</li><li>Plataforma</li><li>Explorador</li><li>Es contenido predictivo</li><li>Es actividad del bot</li><li>Patrón de actividad de bot</li><li>Explorador</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Haga clic en el enlace en SMS | Correo electrónico<br/><br/>Restricciones adicionales (opcional): <li>Vínculo</li><li>Device</li><li>Plataforma</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Cambios en el valor de los datos | Atributo de persona<br/><br/>Restricciones adicionales (opcional): <li>Nuevo valor</li><li>Valor anterior</li><li>Razón</li><li>Origen</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Abre el email | Correo electrónico<br/><br/>Restricciones adicionales (opcional): <li>Vínculo</li><li>Identificación del vínculo</li><li>Es un dispositivo móvil</li><li>Device</li><li>Plataforma</li><li>Explorador</li><li>Es contenido predictivo</li><li>Es actividad del bot</li><li>Patrón de actividad de bot</li><li>Explorador</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Eliminado del grupo de compra | Interés de la solución<br/>Fecha de la actividad (opcional)<br/>Tiempo de espera (opcional) |
| | Se cambia el puntaje | Nombre de puntuación<br/><br/>Restricciones adicionales (opcional):<li>Cambiar</li><li>Nuevo puntaje</li><li>Urgencia</li><li>Prioridad</li><li>Puntaje relativo</li><li>Urgencia relativa</li><li>Fecha de la actividad</li><li>Mín. número de veces</li><br/>Tiempo de espera (opcional) |
| | Devoluciones de SMS | Mensaje SMS<br/><br/>Restricciones adicionales (opcional): <li>Fecha de la actividad</li><li>Número mínimo de veces</li><br/>Tiempo de espera (opcional) |
| Marketo Engage | Visita la página web | Página web <br/> Seleccione una o más páginas de Marketo Engage para que coincidan. <br/><br/>Restricciones adicionales (opcional): <li>Querystring</li><li>Dirección IP del cliente</li><li>Referente</li><li>Agente de usuario</li><li>Motor de búsqueda</li><li>Consulta de búsqueda</li><li>Token</li><li>Explorador</li><li>Plataforma</li><li>Device</li><li>Fecha de la actividad</li> |
| | Completa el formulario | Formulario <br/>: seleccione uno o varios formularios de Marketo Engage para que coincidan.  <br/><br/>Restricciones adicionales (opcional): <li>Fecha de la actividad</li><li>Querystring</li><li>Dirección IP del cliente</li><li>Referente</li><li>Agente de usuario</li><li>Plataforma</li><li>Device</li><br/>Tiempo de espera (opcional) |
| Adobe Experience Platform | Definición del evento | Tipo de evento <br/><br/>Restricciones adicionales (opcional): <li>Campos</li> <br/>Restricciones adicionales (no admitidas): <li>Fecha de la actividad</li><li>Mín. número de veces</li>Tiempo de espera de <br/> (opcional) |

### Añadir un evento de personas

1. Vaya al editor de recorrido.

1. Haga clic en el icono de signo más (**+** ) en una ruta y elija **[!UICONTROL Escuchar un evento]**.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para el tipo de evento.

   ![nodo de Recorrido: escucha eventos de personas](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Seleccione un evento de la lista.

1. Haga clic en **[!UICONTROL Editar evento]** y defina los detalles del evento.

### Escuchar el evento de Marketo Engage

Si tiene páginas web creadas en la instancia de Marketo Engage conectada, puede almacenar en déclencheur un evento basado en una visita o no visita a páginas web de Marketo Engage, así como formularios de Marketo Engage que se rellenaron o no.

1. Seleccione un nodo **[!UICONTROL Listen for an event]** en el editor de recorrido.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para el tipo de evento.

1. Haga clic en la flecha del selector **[!UICONTROL Seleccionar evento de personas]** y desplace el menú a la sección **[!UICONTROL Marketo Engage]**.

1. Seleccione un tipo de actividad de participación en el mercado:

   * **[!UICONTROL Visita La Página Web]**.
   * **[!UICONTROL Rellena El Formulario]**

   ![Escuchar un evento de experiencia](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar evento]** y defina una o más páginas web para que coincidan y cualquier restricción adicional para el evento.

   * (Obligatorio) En el cuadro de diálogo _[!UICONTROL Editar evento]_, defina la restricción **[!UICONTROL Página web]** o Rellena el formulario. Use **[!UICONTROL is]** (predeterminado) para hacer coincidir una o más páginas o formularios seleccionados. Use **[!UICONTROL no es]** para hacer coincidir en todas las visitas/formularios de página con la exclusión de una o más páginas/formularios seleccionados. O bien, use **[!UICONTROL es cualquier]** para que coincida con cualquier visita a una página web de Marketo Engage o formulario rellenado.

   * (Opcional) Haga clic en **[!UICONTROL Agregar restricción]** y elija el campo que desea utilizar para la restricción. Establezca el operador y el valor del campo.

     ![Escuchar un evento de experiencia](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     Puede repetir esta acción para incluir restricciones de campo adicionales según sea necesario.

   * Una vez definidas las restricciones, haga clic en **[!UICONTROL Listo]**.

1. Si es necesario, establezca la opción **[!UICONTROL Tiempo de espera]** para limitar el período de tiempo para escuchar el evento (consulte [Agregar un tiempo de espera a un nodo de evento](#add-a-timeout-to-an-event-node)).

1. En el editor de recorrido, añada el siguiente nodo que se ejecutará cuando se produzca el evento.

### Escuchar un evento de experiencia

Los administradores pueden configurar definiciones de eventos basadas en Adobe Experience Platform (AEP), que permiten a los especialistas en marketing crear recorridos de cuenta que reaccionen a [Eventos de experiencia de AEP](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent). El uso de eventos de experiencia de AEP en recorridos de cuenta es un proceso de dos pasos:

1. [Cree y publique una definición de evento de AEP](../admin/configure-aep-events.md).

2. En un recorrido de cuenta, agrega un nodo _Escuchar un evento_ y selecciona una definición de evento de Experience Platform para un evento basado en personas.

![Vídeo](../../assets/do-not-localize/icon-video.svg){width="30"} [Vea la descripción general del vídeo](../admin/configure-aep-events.md#overview-video)

_Para incluir un evento de experiencia en el recorrido:_

1. Seleccione un nodo **[!UICONTROL Listen for an event]** en el editor de recorrido.

1. En las propiedades del nodo a la derecha, elija **[!UICONTROL Personas]** para el tipo de evento.

1. Haga clic en la flecha del selector **[!UICONTROL Seleccionar evento de personas]** y desplace el menú a la sección **[!UICONTROL Adobe Experience Platform]**.

   ![Escuchar un evento de experiencia](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Seleccione el evento.

   El tipo de evento se muestra vacío en los detalles del nodo.

   ![Editar el evento](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

1. Haga clic en **[!UICONTROL Editar evento]** y defina los tipos de evento y las restricciones adicionales para el evento.

   * (Obligatorio) En el cuadro de diálogo _[!UICONTROL Editar evento]_, defina el tipo de evento. Puede usar el operador predeterminado **[!UICONTROL is]** para que coincida con uno o más tipos de evento seleccionados. O puede usar el operador **[!UICONTROL is not]** para que coincida en todos los tipos de eventos con la exclusión de uno o más tipos de eventos seleccionados.

   * (Opcional) Haga clic en **[!UICONTROL Agregar restricción]** y elija el campo que desea utilizar para la restricción. Establezca el operador y el valor del campo.

     ![Escuchar un evento de experiencia](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >No se admiten las restricciones de _fecha de la actividad_ y _número mínimo de veces_.

     Puede repetir esta acción para incluir restricciones de campo adicionales según sea necesario.

   * Una vez definidas las restricciones, haga clic en **[!UICONTROL Listo]**.

1. Si es necesario, establezca la opción **[!UICONTROL Tiempo de espera]** para limitar el período de tiempo para escuchar el evento (consulte [Agregar un tiempo de espera a un nodo de evento](#add-a-timeout-to-an-event-node)).

1. En el editor de recorrido, añada el siguiente nodo que se ejecutará cuando se produzca el evento.

1. Complete los nodos restantes del recorrido y [publíquelo](./journey-overview.md).

   Cuando el recorrido está activo (publicado) y llega al nodo _Escuchar un evento_, comienza a escuchar eventos de experiencia de AEP.

## Añadir un tiempo de espera a un nodo de evento

Si es necesario, defina la cantidad de tiempo que el recorrido espera el evento. El recorrido finaliza después de un tiempo de espera a menos que defina una ruta de tiempo de espera, donde puede agregar otros nodos.

1. Habilite la opción **[!UICONTROL Tiempo de espera]**.

1. Seleccione el periodo de tiempo durante el cual el recorrido espera a que se produzca un evento antes de que se agote el tiempo de espera.

   Puede optar por finalizar la ruta aquí o realizar una acción diferente estableciendo otra ruta.

1. Para crear una nueva ruta en el recorrido donde se puedan agregar acciones y eventos aplicables a las cuentas cuando no se produzca el evento, active la casilla de verificación **[!UICONTROL Establecer ruta de tiempo de espera]**.

   ![nodo de evento de Recorrido - establecer ruta de tiempo de espera](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Vídeo de información general

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on)
