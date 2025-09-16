---
title: Exportación de cuentas
description: Exporte listas de cuentas filtradas a CSV para plataformas de terceros con grupos de compra y filtros de puntuación de participación en Journey Optimizer B2B Edition.
feature: Audiences
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
source-git-commit: ae1885dbe724dcc751a72325d90641decd355a4c
workflow-type: ht
source-wordcount: '259'
ht-degree: 100%

---

# Exportación de cuentas

Use la función _Exportar cuentas_ para exportar todas las cuentas o un conjunto de cuentas según el filtro que defina. El proceso de exportación genera un archivo CSV y envía la dirección URL del archivo almacenado dentro de una notificación de impulsos. Puede utilizar esta función para mover cuentas a plataformas de terceros cuando sea necesario.

1. En Journey Optimizer B2B Edition, vaya a **[!UICONTROL Cuentas]** > **[!UICONTROL Grupos de compra]** en el panel de navegación izquierdo.

1. Seleccione la pestaña **[!UICONTROL Examinar]**. 

1. Haga clic en **[!UICONTROL Exportar cuentas]** en la parte superior derecha.

   ![Editar detalles de la cuenta](./assets/export-accounts.png){width="800" zoomable="yes"}

1. En el cuadro de diálogo, defina los parámetros de los públicos de cuenta que se exportarán.

   ![Especifique el filtrado de público de la cuenta](./assets/export-accounts-dialog.png){width="400"}

   Para la **[!UICONTROL puntuación de participación]**, el operador `Between` es inclusivo, al igual que los intervalos de porcentaje. Por ejemplo, 5.1 y 5 son ambos _entre_ 5 y 6.

   Los parámetros de filtrado vacíos se tratan como `Is Any`.

1. Haga clic en **[!UICONTROL Exportar cuentas]** para generar el archivo CSV con los filtros especificados.

1. Cuando reciba la notificación de que la exportación ha finalizado, haga clic en el vínculo de notificación para acceder al archivo CSV.

   ![Haga clic en la notificación para descargar el archivo CSV de lista de cuentas exportadas](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Si tiene una suscripción de notificación por correo electrónico configurada en las preferencias de cuenta de usuario de Adobe, puede ser una notificación por correo electrónico.

   La página de la aplicación redirige a la pestaña de exploración _Grupo de compras_ y el cuadro de diálogo de guardar archivo del sistema le pedirá que guarde el archivo en su sistema. Si necesita compartir los datos, puede utilizar el sistema compartir archivos de su equipo.
