---
title: Comprar plantillas de rol de grupo
description: Obtenga información acerca de la definición de una plantilla de rol para utilizarla como componente de grupo comprador.
feature: Buying Groups
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Comprar plantillas de rol de grupo

En un mercado B2B, las decisiones de compra suelen ser tomadas por varios individuos. Esas personas participan en el proceso de adopción de decisiones de acuerdo con su función dentro de la organización. Cree plantillas de función Grupo de compra que contengan estas definiciones de función según cada tipo de oferta de producto o caso de uso de cuenta.

## Acceso y exploración de plantillas de función

1. En la página de inicio de Adobe Experience Platform, haga clic en Adobe Journey Optimizer B2B Edition.

1. En el panel de navegación izquierdo, haz clic en **[!UICONTROL Comprar grupos]**.

1. En la página _[!UICONTROL Comprar grupos]_, seleccione la pestaña **[!UICONTROL Plantillas de roles]**.

   ![Ficha Plantillas de roles](assets/roles-templates-tab.png){width="700" zoomable="yes"}

   La pestaña proporciona una lista de inventario de todas las plantillas de funciones existentes con las siguientes columnas:

   * [!UICONTROL Nombre]
   * [!UICONTROL Estado]
   * [!UICONTROL Fecha de creación]
   * [!UICONTROL Creado por]
   * [!UICONTROL Última actualización]
   * [!UICONTROL Última actualización por]
   * [!UICONTROL Publicado el]
   * [!UICONTROL Publicado por]

   La lista está ordenada de forma predeterminada por la columna _[!UICONTROL Última actualización]_.

   El número de plantillas de roles _publicados_ activos se muestra en la parte superior derecha de la página. Todas las plantillas de roles tienen un estado de `Draft` o `Live`.

1. Para filtrar la lista por nombre, utilice el campo de búsqueda situado en la parte superior de la lista.

   Introduzca los primeros caracteres del nombre para reducir la lista mostrada a los elementos coincidentes.

   ![Plantillas de roles filtrando por cadena de búsqueda](assets/roles-templates-search.png){width="700" zoomable="yes"}

## Crear una plantilla de funciones

1. En la ficha _[!UICONTROL Plantillas de roles]_, haga clic en **[!UICONTROL Crear plantilla]** en la esquina superior derecha.

1. En el cuadro de diálogo, escriba un **[!UICONTROL Nombre]** único (obligatorio) y **[!UICONTROL Descripción]** (opcional) para la plantilla.

   ![Cuadro de diálogo Crear plantilla de roles](assets/roles-template-create-dialog.png){width="400"}

1. Agregue una regla para cada rol que desee definir para la plantilla.

   * Elija **[!UICONTROL Comprar rol de grupo]** de la lista.

     En la versión actual hay seis funciones: `Decision Maker`, `Influencer`, `Practitioner`, `Executive Steering Committee`, `Champion` y `Other`.

     ![Lista de funciones de grupo de compra](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * Defina **[!UICONTROL Ponderación]** para el rol, el cual se usa para calcular la puntuación de participación.

     El valor de cada opción se traduce en un porcentaje para el cálculo de puntuación: [!UICONTROL Trivial] = 20, [!UICONTROL Menor] = 40, [!UICONTROL Normal] = 60, [!UICONTROL Importante] = 80 y [!UICONTROL Vital] = 100.

     Por ejemplo, una plantilla de función con funciones que utilizan Vital, Importante y Normal se convierte a continuación como 100/240, 80/240, 60/240.

   * **[!UICONTROL Agregar condiciones para la asignación automática]**: seleccione esta casilla de verificación para agregar condiciones para la asignación automática de miembros al grupo de compra que cumplan la condición. Si la casilla de verificación no está seleccionada, la adición de condiciones NO es obligatoria.

   * **[!UICONTROL Necesario para la puntuación de integridad]**. Seleccione esta casilla de verificación para el rol si desea que sea un requisito para calcular una puntuación de integridad.

   * Haga clic en **[!UICONTROL Agregar condición]**.

      * En el cuadro de diálogo de condición, expanda la lista de **[!UICONTROL atributos de persona]** y busque un atributo que desee usar para que coincida con el rol. Arrástrela a la derecha y suéltela en el espacio de filtro.

        ![Atributo de arrastre de condición para agregar plantilla de roles](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

      * Utilice el atributo para crear un filtro coincidente con uno o más valores.

        En el ejemplo siguiente, se utiliza el atributo Job title para identificar una coincidencia para Decision Maker. Cualquier valor del título que comience por `Director` o `Sr Director` se evalúa como verdadero para la condición.

        ![Ejemplo de condición de plantilla de roles usando el cargo](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

      * Si es necesario, agregue otro atributo y condición que restrinja aún más los criterios para una coincidencia en la función.

      * Haga clic en **[!UICONTROL Finalizado]**.

   Para cada rol adicional que desee incluir en la plantilla, haga clic en **[!UICONTROL Agregar otro rol]** y defina una o más condiciones que coincidan con el rol.

   ![Plantilla de roles con varios roles definidos](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

1. Si la plantilla está lista para usarse, haga clic en **[!UICONTROL Publish]** en la parte superior derecha.

   La publicación de la plantilla la establece en el estado _Activo_ y la hace disponible para asociarla con un interés de solución. Debe haber al menos una función definida para publicar la plantilla de funciones.

   Los cambios se guardarán automáticamente en el estado _Borrador_. Si no está listo para publicar la plantilla de roles, haga clic en la flecha izquierda (atrás) situada en la parte superior de la página y vuelva a la lista Plantillas de roles.

## Editar una plantilla de funciones de borrador

Cuando una plantilla de roles se encuentra en estado _Borrador_, puede seguir editando los roles definidos. Los cambios que realice se guardarán automáticamente.

Cambie cualquiera de las configuraciones en el encabezado de la tarjeta de función, incluido el requisito de rol de grupo de compra, ponderación, asignación automática y puntuación de integridad.

![Cambiar propiedades de rol de grupo de compra](./assets/roles-template-role-properties.png){width="600"}

### Modificación de los filtros de un rol

Para cambiar la lógica de filtrado de cualquiera de los roles, haga clic en el icono _Editar_ (lápiz) en la parte superior derecha de la tarjeta de roles. Esta acción abre el área de trabajo _[!UICONTROL Conditions]_, donde puede modificar un filtro existente, agregar otro filtro, quitar un filtro o cambiar la lógica del filtro.

### Eliminar una tarjeta de función

Si desea quitar una función de la plantilla, haga clic en el icono _Eliminar_ (papelera) de la tarjeta de funciones.

### Establecer la prioridad de los roles

Puede reordenar las funciones dentro de la plantilla, lo que determina la prioridad para asignar posibles clientes a una función. Hay un controlador **[!UICONTROL Priority]** a la derecha de cada tarjeta de rol. Haga clic en la flecha _Arriba_ o _Abajo_ a la derecha para subir o bajar la tarjeta de rol en la prioridad.

![Cambiar prioridad de rol](./assets/roles-template-role-priority.png){width="700"}

## Eliminar una plantilla de funciones

Puede eliminar una plantilla de funciones si se encuentra en el estado _Borrador_.

1. Seleccione la plantilla de funciones de la lista para abrirla.

1. Haga clic en **[!UICONTROL Eliminar]** en la parte superior derecha.

   ![Cambiar prioridad de rol](./assets/roles-template-delete.png){width="700"}

1. En el cuadro de diálogo, haga clic en **[!UICONTROL Eliminar]** para confirmar.
