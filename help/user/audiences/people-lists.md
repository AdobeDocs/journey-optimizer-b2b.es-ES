---
title: Listas de personas
description: Conozca las listas de personas y cómo explorarlas, verlas, editarlas, eliminarlas y utilizarlas en Journey Optimizer B2B Edition.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%
---

# Listas de personas

En [!DNL Journey Optimizer B2B Edition], una lista de personas es una colección con nombre de perfiles de personas que puede reutilizar en sus recorridos. En lugar de volver a crear el mismo conjunto de filtros en cada recorrido, defina el grupo de personas una vez y haga referencia a él donde lo necesite. Por ejemplo, utilice una lista de personas para excluir al personal interno o a los clientes existentes de un recorrido de nutrición, o para rastrear a las personas que completaron un paso en un recorrido de modo que otro recorrido pueda actuar en consecuencia.

Existen dos tipos de listas de personas:

* **[!UICONTROL Estático]**: la pertenencia solo cambia cuando se agregan o se quitan personas de forma explícita. Puede agregar personas aplicando un conjunto de filtros para rellenar la lista en función de los datos de la persona actual, o agregar y quitar personas mediante un recorrido de cuenta o persona. Ver [listas de personas estáticas](./people-lists-static.md).
* **[!UICONTROL Dinámico]**: usted define un conjunto de reglas (filtros) para depurar automáticamente la lista. La lista se actualiza dinámicamente a medida que las personas se califican o descalifican para la definición de reglas. Consulte [Listas dinámicas de personas](./people-lists-dynamic.md).

Puede [usar listas de personas en recorridos de cuenta y recorridos de personas](./people-lists-journeys.md) para dividir las rutas en función de la pertenencia a listas y para agregar o quitar personas de listas estáticas.

>[!NOTE]
>
>Las listas de personas incluyen perfiles de persona que ya están sincronizados y disponibles en [!DNL Journey Optimizer B2B Edition]. Los perfiles no se leen directamente desde las audiencias [!DNL Adobe Experience Platform] cuando se evalúa la lista.

## Acceso y exploración de listas de personas {#access-browse}

Acceda a las listas de personas desde la navegación izquierda para ver, crear y administrar la pertenencia a listas.

>[!AVAILABILITY]
>
>Los siguientes permisos de producto controlan el acceso a las listas de personas:
>
>* [!UICONTROL Administrar listas de personas B2B]: vea, cree, edite y elimine listas de personas.
>* [!UICONTROL Ver listas de personas B2B] - Ver listas de personas y sus miembros (solo lectura).
>
>Para obtener información sobre cómo asignar permisos, consulte [Acceso y permisos de usuarios](../admin/user-management.md#b2b-product-permissions).

* En el panel de navegación izquierdo, expanda **[!UICONTROL Cuentas]** y seleccione **[!UICONTROL Listas de personas]**.

* Seleccione **[!UICONTROL Listas dinámicas]** o **[!UICONTROL Listas estáticas]** para cambiar entre los dos tipos de lista.

* Escriba texto en el campo _Buscar_ de la parte superior de la lista para filtrar la lista mostrada por nombre.

  ![Acceda a listas de personas para administrar sus audiencias a nivel de persona](./assets/people-lists-browse-search.png){width="800" zoomable="yes"}

* Haga clic en el icono _Configuración de columna_ ( ![Icono de configuración de columna](../assets/do-not-localize/icon-column-settings-new.svg) ) en la esquina superior derecha para seleccionar o borrar las columnas mostradas.

* Para cambiar el ancho de una columna, arrastre el divisor entre los encabezados de columna.

Cada ficha incluye las columnas **[!UICONTROL Nombre]**, **[!UICONTROL Última actualización]**, **[!UICONTROL Actualizado por]**, **[!UICONTROL Creado el]** y **[!UICONTROL Creado por]**. Haga clic en el nombre de la lista de personas para ver sus detalles.

Desde esta página, también puede:

* Cree nuevas listas dinámicas y estáticas.
* Abrir una lista y [revisar los miembros actuales](#view-list-members).
* Haga clic en el icono _Más acciones_ ( **...** ) de una lista y elija [editarla](#edit-list-properties) o [eliminarla](#delete-people-list).

## Creación de una lista de personas {#create-people-list}

1. Haga clic en **[!UICONTROL Crear lista]** en la parte superior derecha de la página _[!UICONTROL Listas de personas]_.

   ![Crear cuadro de diálogo de lista de personas](./assets/people-list-create-dialog.png){width="450"}

1. Escriba **[!UICONTROL Name]** (obligatorio) y **[!UICONTROL Description]** (opcional) para la lista.

   El nombre puede incluir hasta 180 caracteres y debe ser único entre listas del mismo tipo. La descripción puede incluir hasta 2000 caracteres.

1. Elija la lista **[!UICONTROL Type]**:

   * [**[!UICONTROL Estático]**](./people-lists-static.md): los filtros de calificación determinan la pertenencia al aplicarlos a la lista. La suscripción solo se actualiza cuando se agregan personas manualmente o cuando un recorrido las agrega o las quita.
   * [**[!UICONTROL Dinámico]**](./people-lists-dynamic.md): los filtros de calificación determinan la pertenencia dinámicamente. La suscripción se actualiza automáticamente.

1. Haga clic en **[!UICONTROL Crear]**.

   La nueva lista de personas se abre en su página de detalles y el editor de filtros se abre para que pueda definir las personas de la lista. Para agregar personas a una lista estática, aplique uno o varios filtros. Para una lista dinámica, defina las reglas para la pertenencia a una lista.

## Ver miembros de la lista {#view-list-members}

En la página de detalles de una lista de personas, la lista **[!UICONTROL Miembros]** muestra las personas de la lista. El número total de personas en la lista se muestra en la parte superior de la tabla.

La tabla de miembros incluye las siguientes columnas:

* **[!UICONTROL Nombre]**
* **[!UICONTROL Dirección de correo electrónico]**
* **[!UICONTROL Título de trabajo]**
* **[!UICONTROL Empresa]**
* **[!UICONTROL Canceló la suscripción]**
* **[!UICONTROL Creado el]**
* **[!UICONTROL Última modificación]**

De manera predeterminada, el sistema ordena los miembros por **[!UICONTROL Última modificación]**, mostrando primero las personas modificadas más recientemente. También puede ordenar por **[!UICONTROL Nombre]**, **[!UICONTROL Dirección de correo electrónico]** o **[!UICONTROL Creado el]**.

* Para encontrar un miembro específico, usa el campo _Buscar_. Puede buscar por nombre, dirección de correo electrónico o compañía.
* Para elegir las columnas que se van a mostrar, haga clic en el icono _Configuración de columna_ y active o desactive las casillas de verificación. La columna _[!UICONTROL Nombre]_ siempre se muestra.
* Para ver la suscripción más reciente, usa el menú _[!UICONTROL Más]_ para elegir **[!UICONTROL Actualizar miembros]**.
* Para ver más información sobre una persona, haga clic en su nombre para abrir la página [detalles de la persona](../accounts/person-details.md), donde podrá ver su resumen y las actividades recientes.

## Editar propiedades de lista de personas {#edit-list-properties}

Puede cambiar el nombre y la descripción de una lista de personas estática o dinámica.

1. Abra el cuadro de diálogo _[!UICONTROL Editar lista]_ mediante uno de los métodos siguientes:

   * En la página _[!UICONTROL Listas de personas]_, haga clic en el icono _Más acciones_ ( **...** ) de la lista y elija **[!UICONTROL Editar]**.
   * En la página de detalles de la lista, haga clic en **[!UICONTROL Editar propiedades de lista]**.

1. Actualice **[!UICONTROL Name]** o **[!UICONTROL Description]**.

1. Haga clic en **[!UICONTROL Guardar]**.

## Eliminar una lista de personas {#delete-people-list}

>[!IMPORTANT]
>
>La eliminación de una lista de personas es permanente y no se puede deshacer. No se puede eliminar una lista de personas que esté siendo utilizada por un recorrido activo.

1. Elimine la lista mediante uno de los métodos siguientes:

   * En la página _[!UICONTROL Listas de personas]_, haga clic en el icono _Más acciones_ ( **...** ) junto al nombre de la lista y elija **[!UICONTROL Eliminar]**.
   * En la página de detalles de la lista, haga clic en **[!UICONTROL Eliminar lista]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.
