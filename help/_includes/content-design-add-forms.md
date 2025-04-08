---
title: 'Creación de contenido: añadir formularios'
description: Sección reutilizada sobre cómo agregar formularios en páginas de aterrizaje y plantillas
source-git-commit: 97d8e5b366e8786e517c18828236f95304f3f3be
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Creación de contenido: añadir formularios

Un formulario es un componente reutilizable al que se puede hacer referencia en varias páginas de aterrizaje y plantillas de páginas de aterrizaje en Adobe Journey Optimizer B2B edition. Es un bloque de campos y un botón de envío que se pueden crear previamente e insertar rápidamente para que el diseño de la página sea más rápido y coherente.

En el siguiente ejemplo se describen los pasos para agregar un formulario al diseñar la página.

1. En la sección **[!UICONTROL Contenido]**, arrastre el elemento **[!UICONTROL Formulario]** y suéltelo en un componente estructural en el espacio de diseño de la página.

   ![Arrastre un componente Formulario al espacio de diseño visual](../assets/content-design-shared/content-design-add-form.png){width="600"}

   >[!TIP]
   >
   >Para agregar el formulario de modo que ocupe todo el diseño horizontal dentro del correo electrónico, agregue una estructura de columna 1:1 y, a continuación, arrastre y suelte el formulario en él.

1. Haga clic en el icono _Formulario_ en la barra de herramientas de componentes o use las propiedades de **[!UICONTROL Incrustar formulario]** a la derecha para seleccionar el formulario publicado.

   ![Seleccionar el formulario publicado](../assets/content-design-shared/content-design-add-form-properties.png){width="600"}

1. Si desea anular el **[!UICONTROL tipo de seguimiento]** predeterminado del formulario, cambie la configuración según los requisitos de la página o plantilla.

   Esto también se conoce como _página de agradecimiento_ por el formulario y esta configuración determina qué sucede cuando un visitante envía el formulario:

   * **[!UICONTROL Permanecer en la página]**: elija esta opción para mantener al visitante en la misma página cuando se envíe el formulario.

   * **[!UICONTROL Página de aterrizaje]**: elija esta opción para seleccionar cualquier página de aterrizaje de Journey Optimizer B2B edition o Marketo Engage como seguimiento.

   * **[!UICONTROL Dirección URL externa]**: elija esta opción para especificar cualquier dirección URL como página de seguimiento. Una vez que el visitante envía el formulario, el explorador carga la dirección URL designada.

     >[!TIP]
     >
     >Si desea que el usuario utilice el formulario para descargar un archivo, puede especificar una URL para el archivo alojado. Con esta configuración, el botón de envío funciona como un botón de descarga.

   ![Cambiar la configuración de seguimiento](../assets/content-design-shared/content-design-add-form-follow-up.png){width="280"}

1. Si desea limitar la visualización del formulario por tipo de dispositivo, cambie la configuración de **[!UICONTROL Opciones de visualización]**:

   * **[!UICONTROL Mostrar solo en dispositivos de escritorio]**
   * **[!UICONTROL Mostrar solo en dispositivos móviles]**
   * **[!UICONTROL Mostrar en todos los dispositivos]** (predeterminado)

1. Si es necesario, seleccione la ficha **[!UICONTROL Estilos]** en el panel derecho para establecer los márgenes del formulario dentro de la página.
