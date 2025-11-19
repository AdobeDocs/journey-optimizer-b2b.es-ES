---
title: Administración de campos XDM
description: Utilice la administración de campos XDM para controlar los datos disponibles para Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 2%

---


# Administración de campos XDM

Los campos XDM (Experience Data Model) son elementos de esquema que proporcionan datos a la aplicación [!DNL Journey Optimizer B2B Edition]. Los campos XDM se utilizan como filtros y restricciones en recorridos, grupos de compra y funciones, como la personalización de correo electrónico y el contenido condicional.

Los esquemas definen campos basados en clases XDM estándar. Las clases XDM estándar incluyen Perfil individual, Cuenta empresarial y Evento de experiencia. Los esquemas relacionales también definen campos que permiten modelar datos estructurados de manera similar a las bases de datos relacionales tradicionales.

Los esquemas de Adobe Experience Platform (AEP) suelen contener muchos campos en jerarquías complejas. Recorrer los árboles de esquema XDM lleva tiempo. La administración de campos XDM optimiza la selección de campos al mostrar solo los campos relevantes para cada recorrido. Los administradores controlan qué campos aparecen para los creadores de recorridos. Los administradores también establecen los campos como de solo lectura o editables. Estas acciones mejoran la eficacia durante el diseño del recorrido.

Los administradores que comprenden XDM y colaboran con los ingenieros de datos o las partes interesadas en el modelado de datos de la plataforma de datos del cliente B2B (CDP) siguen los procedimientos de esta guía.

>[!NOTE]
>[Los esquemas relacionales](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) están disponibles para [!DNL Journey Optimizer B2B Edition] como una versión limitada. Los esquemas relacionales y de Data Mirror están disponibles para los titulares de licencias de las campañas orquestadas de Journey Optimizer. Los esquemas relacionales también están disponibles como una versión limitada para los usuarios de Customer Journey Analytics, según la licencia y la habilitación de funciones. Póngase en contacto con su representante de Adobe para obtener acceso.

## Acceso a clases XDM

Para abrir el área de administración de campos XDM, vaya a **Configuraciones** > CONFIGURACIÓN > **Clases XDM**.

* Solo puede agregar nuevos campos después de que un esquema se esté utilizando activamente en un recorrido.
* Eliminar, cambiar el nombre o los tipos de campo pueden causar problemas de funcionalidad de recorrido. Tenga cuidado al manipular esquemas.
* No cambie el nombre ni elimine esquemas, ni modifique claves en esquemas relacionales.

>[!IMPORTANT]
>Puede actualizar la selección de campos en cualquier momento seleccionando nuevos campos o anulando la selección de los campos que ya no necesite. Una vez publicado un recorrido con este esquema, se bloquea la estructura del esquema. No se admite la eliminación o el cambio de nombre del esquema, la adición de nuevos campos o el cambio de tipos de campos, y puede provocar errores de recorrido.

## Clases estándar

En la pestaña Clases estándar, puede editar _Campos administrados_ y _Campos actualizables_.

* Los campos administrados aparecen en los recorridos, los grupos de compra y las funciones de personalización.
* Los campos actualizables sirven como restricciones para los nodos de recorrido _Actualizar perfil de cuenta_ y _Actualizar perfil de persona_.

![Pestaña de clases estándar que muestra campos administrados y actualizables para la configuración de clases XDM](assets/xdm-standard.png){width="600" zoomable="yes"}

Siga estos pasos para seleccionar campos del esquema de unión para clases XDM estándar:

1. Vaya a **Administración** > **Configuraciones** > **Clases XDM**.
1. Abra la ficha **Estándar**. Elija una de las siguientes clases:

   * Perfil individual de XDM
   * Cuenta empresarial de XDM

La tabla muestra información que incluye:

* Número de campos administrados
* Número de campos actualizables
* Hora de la última actualización

Haga clic en el nombre de clase para abrir el cuadro de diálogo de selección _Campos administrados_.

![Cuadro de diálogo de selección de campos administrados para clases XDM estándar que muestran opciones de campos configurables](assets/xdm-standard-managed-fields.png){width="600" zoomable="yes"}

1. Haga clic en el menú **...** para cambiar entre _[!UICONTROL Campos administrados]_ y _[!UICONTROL Campos actualizables]_. El cuadro de diálogo enumera todos los campos configurables.
1. Seleccione hasta 100 campos para cada clase XDM.
1. Haga clic en **[!UICONTROL Guardar]** para confirmar las selecciones.

Use el filtro [!UICONTROL Mostrar solo los campos seleccionados] para mostrar solo los campos activos.

Para _campos actualizables_, tiene acceso a un cuadro de diálogo independiente que le permite elegir campos de otros orígenes de datos:

1. En el menú desplegable Conjuntos de datos, seleccione el origen de datos que desea configurar.
1. Edite los campos del conjunto de datos seleccionado.
1. Haga clic en **[!UICONTROL Guardar]** para aplicar los cambios.

![Cuadro de diálogo para seleccionar campos actualizables de conjuntos de datos en la configuración de esquema XDM](assets/xdm-select-updateable.png){width="600" zoomable="yes"}

El campo debe ser _Administrado_ antes de que pueda _actualizarse_. Los _campos actualizables_ que seleccione deben existir en el esquema proporcionado por el usuario.

## Esquemas relacionales

Los esquemas relacionales permiten crear clases de datos personalizadas. Con acceso a varios conjuntos de datos, puede crear clases adaptadas específicamente a sus necesidades de datos.
Utilice esquemas relacionales para entidades comerciales, como compras, licencias y registros de eventos, en las decisiones de recorrido y la personalización de correo electrónico. Puede seleccionar hasta 50 esquemas y hasta 100 campos por esquema.

![La pestaña Esquemas relacionales del Editor de esquemas muestra campos de entidad empresarial para Adobe Journey Optimizer](assets/xdm-relational.png)

>[!NOTE]
>Actualmente, esta función admite casos de uso de objetos personalizados relacionados con la cuenta, y tiene previsto admitir más casos de uso de objetos predeterminados en el futuro.

Cree esquemas relacionales con el Editor de esquemas en **Administración de datos** > **Esquemas**.

Estos valores de configuración deben incluirse al crear un esquema para utilizarlo con [!DNL Journey Optimizer B2B Edition]:

* Comportamiento: Registro
* Segmentación: habilitada
* Tipo de relación: varios a uno
* Esquema de referencia: cuenta B2B
* Campos obligatorios: Clave principal, clave externa y descriptor de versión
* Conjunto de datos asociado: definido y asignado al esquema

### Crear un esquema relacional

Siga estos pasos para seleccionar campos para usarlos en [!DNL Journey Optimizer B2B Edition]:

1. Vaya a **Administración** > **Configuraciones** > **Clases XDM**.
1. Abra la pestaña **Relacional** para ver los esquemas.
1. Haga clic en **[!UICONTROL Seleccionar esquema XDM relacional]**.

   * En la versión beta, solo se admiten _objetos personalizados varios a uno_ de cuenta.

1. Seleccione un esquema relacional y haga clic en **[!UICONTROL Siguiente]**.

   * En la versión beta, no se puede quitar un esquema de la lista una vez que se ha seleccionado.

1. Introduzca un área de nombres o utilice la predeterminada. Haga clic en **[!UICONTROL Siguiente]**.

   * Solo puede establecer el área de nombres una vez y no puede revertir esta acción.

1. Revise los campos de esquema relacional. Haga clic en el icono ![Información](../assets/do-not-localize/icon-info-light.svg) [!UICONTROL Información] para ver los metadatos del campo.
1. Seleccione los campos que desea habilitar para recorridos y personalización. La plataforma selecciona automáticamente los siguientes campos obligatorios:

   * Clave extranjera
   * Clave principal
   * Descriptor de versión

1. Use el control deslizante [!UICONTROL Mostrar solo los campos seleccionados] para obtener una vista previa de las selecciones.
1. Filtre los campos por nombre mediante la barra de búsqueda.
1. Haga clic en **[!UICONTROL Guardar]**.

## Eventos

Utilice eventos de experiencia y sus campos asociados en las decisiones de recorrido. Puede seleccionar hasta 50 eventos y hasta 100 campos por evento.

![La pestaña Eventos muestra la selección de eventos de experiencia y los campos de esquema para los recorridos y la personalización](assets/xdm-events.png){width="700" zoomable="yes"}

Haga clic en un nombre de evento para ver los detalles y editar los campos configurados.

Siga estos pasos para seleccionar eventos de experiencia y campos de esquema:

1. Vaya a **Administración** > **Configuraciones** > **Clases XDM**.
1. Abra la ficha **Eventos**.
1. Para seleccionar campos para un evento, haga clic en **[!UICONTROL Seleccionar evento de experiencia]**.
1. En la página Detalles, haga clic en **[!UICONTROL Seleccionar tipo de evento]**.
1. En la lista Evento, elija su evento.
1. Haga clic en **[!UICONTROL Seleccionar]** para cerrar el cuadro de diálogo.

   * En la versión beta, no se pueden eliminar los eventos seleccionados.

1. Haga clic en **[!UICONTROL Seleccionar campos]**.
1. Use el control deslizante [!UICONTROL Mostrar solo los campos seleccionados] para ver las selecciones actuales.
1. Seleccione los campos que se usarán en [!DNL Journey Optimizer B2B Edition]. Haga clic en **[!UICONTROL Seleccionar]** para cerrar el cuadro de diálogo.
1. Haga clic en [!UICONTROL Guardar].
