---
title: Nodos de espera
description: Utilice los nodos de espera para pausar la progresión del recorrido y controlar el tiempo de salida por duración, fecha o configuración avanzada de día y hora.
feature: Account Journeys, Person Journeys
role: User
exl-id: fecab788-4e8e-490a-bcca-bc3ab43411d9
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2
autotag-review: 2026-03-30T23:11:12.994Z
TQID: https://experienceleague.adobe.com/a-dPU6YNtDv86OD-i35749QY4HCDFtVIVn9F6jm0zEA
source-git-commit: 7cd6c4ecfbbd3a86b4f30d1b4fe6f06655a9c4f5
workflow-type: tm+mt
source-wordcount: 687
ht-degree: 0%

---

# Nodos de espera

Use un nodo _Wait_ cuando desee pausar la progresión del recorrido durante un tiempo determinado antes de pasar al siguiente paso.

Existen dos formas de definir el tiempo de espera:

* Una fecha específica en la que desea avanzar al siguiente nodo del recorrido
* Una duración relativa (cantidad de minutos, horas, días, semanas o meses)

## Añadir el nodo de espera

1. Vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **[!UICONTROL Esperar]**.

   ![Agregar nodo de recorrido: espera](./assets/add-node-wait.png){width="440"}

1. Para establecer el tiempo de espera antes de que el recorrido continúe con el siguiente nodo en la ruta de acceso, use las propiedades del nodo a la derecha para establecer **[!UICONTROL Type]**.

   * **[!UICONTROL Duración]**: defina un número específico de días, horas o minutos entre la entrada y la salida del nodo de espera.
   * **[!UICONTROL Fecha]** - Especifique una fecha y hora para la salida.

   ![nodo de Recorrido: espera](./assets/node-wait.png){width="500"}

## Configuración de espera avanzada

Habilite la opción **[!UICONTROL Debe finalizar el]** para configurar un _paso de espera avanzado_ y garantizar que los mensajes lleguen a las personas y a los miembros de la cuenta en el momento óptimo. Esta configuración le proporciona un control preciso sobre cuándo una persona o cuenta sale de un paso de espera y pasa al siguiente nodo de la recorrido. En lugar de un número fijo de horas o días desde la entrada hasta la salida, puede programar acciones para que se produzcan en momentos específicos y en días específicos de la semana.

Con un _paso de espera avanzado_, usted define **_cuándo_** sale la persona o cuenta, no simplemente cuánto tiempo esperan.

![nodo de Recorrido - paso de espera avanzado](./assets/node-wait-advanced.png){width="500"}

### Tipos de espera

| Tipo de espera | Descripción | Configuración |
| --------- | ----------- | ------------- |
| **Hora específica del día** | Retener hasta una hora específica (como 9:00 a.m.) | Establezca la hora (hora y minuto). Sale en la siguiente incidencia de esa hora (para la zona horaria seleccionada). |
| **Día específico de la semana** | Retener hasta un día en particular (por ejemplo, el martes) | Seleccione un día de la semana. Si no se especifica ninguna hora, sale a medianoche (para la zona horaria seleccionada) del siguiente día coincidente. |
| **Intervalo o combinación de días** | Mantener hasta cualquier día dentro de un intervalo (como lunes a viernes) o en cualquiera de los días especificados | Seleccione los días de destino. Si no se especifica ninguna hora, sale a medianoche (para la zona horaria seleccionada) del siguiente día coincidente. |
| **Combinación de tiempo + día** | Combine ambos para una programación precisa (como martes a las 10:00 a.m.) | Seleccione los días objetivo y establezca la hora objetivo. Sale en la incidencia de día/hora siguiente (para la zona horaria seleccionada). |

### Casos comunes

Los siguientes escenarios ilustran cómo se pueden aplicar ejemplos típicos a la configuración del nodo de espera:

+++Llegada por correo electrónico durante el horario laboral

**Escenario:** Vende a clientes B2B que leen correos electrónicos durante su jornada laboral. Desea que todos los correos electrónicos lleguen durante el horario laboral.

**Solución:** configure su paso de espera para liberar posibles clientes a las 9:00 de la mañana en días laborables (de lunes a viernes). Independientemente de cuándo un posible cliente entre en el nodo de espera, recibirá el correo electrónico durante el horario laboral.

+++

+++Tiempos de envío coherentes para audiencias dinámicas

**Escenario:** Su audiencia cambia a diario conforme califican nuevas cuentas o posibles clientes. Desea que todos los posibles clientes reciban el primer correo electrónico al mismo tiempo, independientemente de cuándo cumplan los requisitos.

**Solución:** configure el paso de espera para que finalice a una hora específica (por ejemplo, a las 10:00 de la mañana). Todos los posibles clientes, independientemente de si se clasificaron a medianoche o al mediodía, abandonan el paso de espera juntos a las 10:00 a. m.

+++

+++Tareas de seguimiento compatibles con SLA

**Escenario:** su equipo de ventas tiene un SLA de dos días hábiles para hacer un seguimiento de los posibles clientes de las cuentas calificadas para mercadeo. Se excluyen los fines de semana.

**Solución:** configure el paso de espera para liberar posibles clientes solo en días laborables. Una ventaja clasificada el viernes se dirige para el seguimiento el lunes o el martes, no durante el fin de semana.

+++

### Ejemplos de entrada y salida

| Configuración de espera | Ingresantes de cuenta/posible cliente | Salidas de cuenta/posible cliente |
| ------------------ | ------------------- | ------------------ |
| 9:00 a. m., cualquier día | Lunes 11:00 AM | Martes a las 9:00 |
| 9:00 a. m., cualquier día | Lunes, 7:00 | Lunes, 9:00 |
| Martes, no hay tiempo establecido | Viernes 3:00 PM | Martes 12:00 a.m. |
| 10:00 a.m., de lunes a viernes | Sábado 2:00 PM | Lunes 10:00 a. m. |
| 10:00 a.m., de lunes a viernes | Miércoles, 8:00 | Miércoles, 10:00 |
