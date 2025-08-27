---
title: Configurar la ponderación de puntuación de participación
description: Aprenda a configurar la ponderación de la puntuación de participación personalizada para reflejar la lógica de puntuación que se ajusta a sus estrategias empresariales.
feature: Setup, Engagement, Buying Groups
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
role: Admin
source-git-commit: c17e66ae3bc6344a87cbb3e2d3a971babc9612c3
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Configurar la ponderación de puntuación de participación personalizada

Una puntuación de participación en el grupo de compra refleja el nivel de participación mediante la evaluación de diversas actividades registradas para los miembros del grupo de compra. Con la ponderación de puntuación personalizada, los equipos de operaciones de marketing tienen la flexibilidad de definir sus propios modelos para ponderar las actividades que son más significativas para la participación. Un modelo de puntuación personalizado produce un reflejo más preciso de su canalización al priorizar los comportamientos que indican con mayor precisión la intención de compra en su proceso de ventas.

Como administrador, puede definir varios modelos de puntuación de participación para su organización, pero solo uno puede estar activo a la vez. Se define un modelo de puntuación según las actividades que se van a incluir y el peso aplicado a cada actividad.

## Acceso a los modelos de ponderación de puntuación de participación

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en **[!UICONTROL Ponderación de puntuación de participación]** en el panel intermedio para mostrar la lista de modelos de puntuación.

   Desde esta página, puedes [crear (duplicar)](#create-an-engagement-score-model), [activar](#activate-a-score-model) y [editar](#change-the-engagement-weighting-settings) modelos de puntuación de participación.

   ![Acceder a las definiciones de eventos configuradas](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   La tabla está ordenada por la columna _[!UICONTROL Última actualización]_, con los modelos actualizados más recientemente en la parte superior de forma predeterminada, e incluye la capacidad de buscar por _[!UICONTROL Nombre]_. Puede personalizar la tabla mostrada si hace clic en el icono _Configuración de columna_ ( ![Configuración de columna](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha y activa o desactiva las casillas de verificación de la columna.

![Columnas que se mostrarán en la lista de ponderación de puntuación de participación](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Para acceder a los detalles de un modelo de puntuación de participación, haga clic en el nombre.

### Modelo de puntuación predeterminado

El sistema crea un modelo de puntuación de participación inicial denominado _Modelo de ponderación de actividad 1_, que es el modelo activo hasta que cree su propio modelo personalizado y lo active. Al activar el modelo personalizado, el modelo predeterminado cambia a un estado _Archivado_. Puede duplicarlo si decide volver al modelo de puntuación de participación predeterminado o si decide utilizarlo como punto de partida para otro modelo personalizado.

![Modelo de ponderación de puntuación de participación predeterminado](./assets/configuration-engagement-scoring-model-default.png){width="600" zoomable="yes"}

### Eliminar un modelo de borrador

Puede eliminar un borrador de modelo de puntuación de participación si decide que no desea activarlo en el futuro. Haga clic en el icono _Más menú_ (***...***) junto al nombre del modelo de puntuación del borrador en la lista y elija **[!UICONTROL Eliminar]**.

![Eliminar el modelo de puntuación de borrador](./assets/configuration-engagement-scoring-model-more-delete.png){width="350"}

En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.

## Crear un modelo de puntuación de participación personalizado

Para crear un modelo de puntuación de participación personalizado, duplique el modelo predeterminado u otro modelo personalizado que ya se haya creado. Puede duplicar el modelo _Activo_ actual, un modelo _Borrador_ o un modelo _Archivado_. A continuación, edite el modelo duplicado según sus necesidades.

1. Haga clic en el nombre del modelo para abrir la página de detalles del modelo y haga clic en **[!UICONTROL Duplicar]** en la parte superior derecha.

   ![Duplicar el modelo activo](./assets/configuration-engagement-scoring-model-duplicate.png){width="600" zoomable="yes"}

   También puede hacer clic en el icono _Más menú_ (***...***) junto al nombre del modelo de puntuación en la lista y elegir **[!UICONTROL Duplicado]**.

   ![Use el menú Más para duplicar el modelo activo](./assets/configuration-engagement-scoring-model-more-duplicate.png){width="325"}

1. En el cuadro de diálogo _Duplicar_, escriba un nombre único para el modelo duplicado y haga clic en **[!UICONTROL Duplicar]**.

   ![Confirmar para duplicar el modelo de puntuación](./assets/configuration-engagement-scoring-model-duplicate-dialog.png){width="500"}

   El modelo duplicado se muestra en la lista con un estado _Borrador_. Haga clic en el nombre para abrir los detalles del modelo de puntuación y realizar los cambios.

### Cambio de la configuración de ponderación de participación

La configuración de peso define las bandas que puede asignar a cada actividad del modelo. Puede cambiar las bandas para reflejar las estrategias de su organización para evaluar la participación. Por ejemplo, podría ajustar la banda de ponderación _Normal_ a un valor de 65 si desea asignar un valor más alto a las actividades normales. O bien, puede agregar una banda de ponderación diseñada para capturar actividades que se encuentren entre _Normal_ y _Importante_. En este caso, podría agregar una banda y etiquetarla como _Significant_ y asignar un valor de banda de peso de 75.

1. En la página de detalles del modelo de puntuación, haga clic en **[!UICONTROL Configuración del peso de la participación]** en la parte superior.

   ![Configuración de peso de participación de acceso](./assets/configuration-engagement-scoring-model-weight-settings-button.png){width="600" zoomable="yes"}

1. Para cada banda de peso, ajuste el nombre o los valores según sus necesidades:

   * Cambie el nombre en el campo _[!UICONTROL Banda de ponderación]_.
   * Escriba un nuevo valor o haga clic en **+** o en **-** para aumentar o disminuir el valor.

   ![Configuración de peso de la participación](./assets/configuration-engagement-scoring-model-weight-settings.png){width="500"}

1. Si es necesario, añada otra banda de ponderación:

   Haga clic en **[!UICONTROL + Agregar banda de ponderación]** al final de la lista. Esta acción inserta una banda de ponderación en blanco en la parte inferior de la lista.

   Introduzca el nombre y defina el valor de la banda. Asegúrese de utilizar un nombre y un valor únicos.

1. Si es necesario, quite una banda de ponderación y haga clic en el icono _Eliminar_ ( ![Eliminar icono](../assets/do-not-localize/icon-delete-outline.svg) ) de la fila de la banda de ponderación.

1. Una vez completados los cambios, haz clic en **[!UICONTROL Guardar]**.

### Cambio de la ponderación de actividad

Cada modelo de puntuación incluye la lista completa de actividades de puntuación de participación admitidas:

{{engagement-activities}}

Para cada actividad de la lista, establezca el valor que desea asignar a cada ocurrencia de actividad. Haga clic en la flecha hacia abajo del campo Ponderación y seleccione la banda de ponderación tal como se define en la configuración de ponderación de participación.

![Establecer ponderación de actividad](./assets/configuration-engagement-scoring-model-set-activity-weighting.png){width="500"}

Si no desea que el cálculo de puntuación de participación utilice una actividad, establezca la ponderación en un valor cero (0).

Los cambios se guardarán automáticamente.

## Activación de un modelo de puntuación

Cuando se activa un modelo de puntuación de borrador, este reemplaza al modelo activo actualmente. El modelo activo actualmente se archiva automáticamente.

1. Abra un modelo de puntuación de borrador para ver la página de detalles.

1. Haga clic en **[!UICONTROL Activar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Activar]**.

   ![Acceder a las definiciones de eventos configuradas](./assets/configuration-engagement-scoring-activate-dialog.png){width="400"}
