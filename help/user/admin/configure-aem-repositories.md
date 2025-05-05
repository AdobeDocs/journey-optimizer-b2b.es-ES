---
title: Configuración de repositorios de recursos de Experience Manager
description: Obtenga información sobre cómo configurar una conexión a repositorios de Experience Manager Assets para utilizarla en la creación de contenido de Journey Optimizer B2B edition.
feature: Assets, Integrations
exl-id: 4cdfc8bc-823f-4320-a2c3-08226f26eec2
source-git-commit: 728d5316cfdeee92bd4f67277d299bbec2773a4f
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Configuración de repositorios de recursos de Experience Manager

Adobe Journey Optimizer B2B edition se integra con Adobe Experience Manager Assets as a Cloud Service, lo que permite algo más que usar recursos como correos electrónicos en un recorrido de cuenta. Garantiza la transparencia al intercambiar información con Experience Manager Assets. Configure la conexión al Adobe de Experience Assets para habilitar esta capacidad.

Adobe Experience Manager Cloud Manager está organizado en programas y cada programa tiene varios entornos y repositorios ([Más información](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/programs/program-types)). Al configurar Adobe Experience Manager Assets en Adobe Journey Optimizer B2B edition, se configuran las conexiones a cada repositorio que desea utilizar para acceder a los recursos digitales.

{{aem-assets-licensing-note}}

## Requisitos previos

* AEM Genere las credenciales de servicio para el entorno deseado en el Developer Console sin encabezado de la ([Más información](https://experienceleague.adobe.com/es/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials#generate-service-credentials)).
* Adquiera los certificados necesarios para la conexión. Como práctica recomendada, asegúrese de que restan al menos seis meses para la caducidad de los certificados. Los certificados caducan cada 365 días.
* Adobe Journey Optimizer B2B edition admite el acceso a una fuente de administración de recursos digitales a la vez. Asegúrese de que los recursos necesarios estén disponibles en Adobe Experience Manager antes de cambiar.

>[!IMPORTANT]
>
>Las credenciales del servicio son de buena fe y contienen una clave privada. Estas credenciales deben almacenarse, administrarse y accederse según la directiva de TI y seguridad de su organización.

## Añadir una conexión al repositorio

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Assets]** en el panel intermedio.

   ![Acceder al espacio de configuración de Assets](./assets/configuration-assets-aem.png){width="700" zoomable="yes"}

<!--   The default digital asset management option is configured as `Adobe Marketo Engage`.
-->
AEM Desde aquí, puede configurar las conexiones a cada repositorio de entorno de uno a uno.

1. En el cuadro _[!UICONTROL Adobe Experience Manager Assets]_, haga clic en la flecha situada junto a **[!UICONTROL Configurar un repositorio]** y elija el repositorio.

   ![Elegir un repositorio de AEM Assets](./assets/configure-assets-aem-choose-respository.png){width="500"}

1. Haga clic en **[!UICONTROL Agregar un certificado]** y use las herramientas de cuadro de diálogo para cargar el archivo.

   Puede cargar un archivo .json arrastrándolo al cuadro de diálogo o haciendo clic en el vínculo para localizar y seleccionar un archivo de su sistema (asegúrese de que el archivo sea de un tipo JSON válido).

   ![Cargar el archivo JSON del certificado](./assets/configuration-assets-aem-upload-cert.png){width="500"}

   Después de la carga, el certificado se muestra en la parte inferior.

   >[!NOTE]
   >
   >Si se utiliza un archivo no válido, el cuadro de diálogo muestra un error en la parte inferior.

   Haga clic en **[!UICONTROL Agregar]** para completar el certificado.

1. Haga clic en la flecha hacia atrás (←) para volver a la página de configuración principal.

   El repositorio configurado se muestra en la tabla debajo del panel de selección. Puede agregar otro repositorio repitiendo los pasos 3-4.

   AEM ![Revisar los repositorios de recursos configurados de la](./assets/configuration-assets-aem-repositories.png){width="600" zoomable="yes"}

Cuando termine de configurar los repositorios, los integrantes del equipo pueden seleccionar Adobe Experience Manager Assets al crear el contenido.

>[!NOTE]
>
>Adobe Journey Optimizer B2B edition admite el acceso a una fuente de administración de recursos digitales a la vez durante la creación de contenido. 

## Reemplazar un certificado

Los certificados caducan cada 365 días desde la fecha de creación. Sustitúyalo antes de que caduque para garantizar que su equipo pueda seguir accediendo a los recursos.

>[!NOTE]
>
>Adobe Journey Optimizer B2B edition se comunica con los recursos del Experience Manager para obtener información de uso. La conexión debe permanecer activa para que la sincronización de datos de uso sea fiable y para evitar discrepancias en los datos. A los usuarios administradores se les notifica sobre los certificados que caducan mediante las notificaciones en la aplicación. También pueden anotar las fechas de caducidad en la subsección de Assets, Administración de recursos digitales, en el área de Administración.

1. En la página de administración de recursos digitales, busque la lista de los repositorios configurados.

1. Haga clic en el repositorio deseado para reemplazar el certificado.

1. Haga clic en el icono de puntos suspensivos (**...**) del archivo de certificado para mostrar las opciones de acciones que contiene.

   AEM ![Acceda al menú de opciones del certificado del repositorio de recursos de la biblioteca de recursos](./assets/configuration-assets-aem-repo-menu.png){width="600" zoomable="yes"}

1. Elija **[!UICONTROL Reemplazar]** para abrir el cuadro de diálogo de carga de archivos.

1. Cargue un archivo arrastrándolo al cuadro de diálogo o utilizando el vínculo. Asegúrese de que el archivo sea del tipo json.

   AEM ![Cargar el archivo JSON del certificado del repositorio de recursos de reemplazo](./assets/configuration-assets-aem-upload-replacement-cert.png){width="500"}

1. Haga clic en **[!UICONTROL Reemplazar]** para confirmar la carga.

## Ver un certificado

Puede ver el archivo JSON de certificado asociado a la conexión al repositorio.

1. En la página de administración de recursos digitales, busque la lista de los repositorios configurados.

1. Haga clic en el repositorio conectado.

1. Haga clic en el icono de puntos suspensivos (**...**) del archivo de certificado para mostrar las opciones de acciones que contiene.

1. Elija **[!UICONTROL Ver]**.

   AEM ![Ver el archivo JSON de certificado de un repositorio de recursos conectado a un repositorio de recursos de la](./assets/configuration-assets-aem-view-cert.png){width="600"}

1. Haga clic en **[!UICONTROL Cerrar]** para volver a la página Configurar repositorio.

## Eliminación de una conexión al repositorio

Al eliminar un repositorio, se elimina el acceso de los usuarios al entorno de Experience Manager Assets en Journey Optimizer B2B edition.

1. En la página _[!UICONTROL Administración de recursos digitales]_, busque la lista de repositorios de recursos configurados.

1. Haga clic en el nombre del repositorio deseado para editar la conexión.

1. Haga clic en el icono de puntos suspensivos (**...**) del archivo de certificado para mostrar las opciones de acciones que contiene.

1. Elija **[!UICONTROL Eliminar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.
<!--

## Switch back to Adobe Marketo Engage Assets

Select Adobe Marketo Engage digital asset management in the Assets section.

After the confirmation, the Adobe Marketo Engage assets library is available for users.
-->
