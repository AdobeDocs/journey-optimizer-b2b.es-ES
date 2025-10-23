---
title: Asignación de personas
description: Aprenda a configurar perfiles para el marketing basado en cuentas asignando atributos de persona para crear plantillas de función optimizadas para los grupos compradores.
feature: Setup, Buying Groups
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
role: Admin
source-git-commit: 521bfb3870e98dab85fbcabe711ed662e9b748d4
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 1%

---

# Asignación de personas

Las personas son un aspecto clave de un enfoque de marketing basado en cuentas (ABM), ya que ayudan a los especialistas en marketing a ajustar sus estrategias a las necesidades, preferencias y puntos problemáticos específicos de las personas dentro de las cuentas de destino. Los especialistas en marketing pueden crear perfiles detallados para cada persona, incluidos sus antecedentes, responsabilidades, puntos problemáticos y canales de comunicación preferidos. Con estas definiciones, los administradores pueden configurar las personas según sus atributos en Journey Optimizer B2B edition, de modo que las plantillas de funciones puedan utilizar condiciones de función optimizadas y coherentes que capturan a estas personas.

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
Limitaciones de uso y definición personal:

* Puede tener hasta 20 personalidades definidas en la lista _[!UICONTROL Asignación personal]_.
* Cada persona puede incluir hasta cinco atributos en su definición.
* En todas las personalidades definidas, puede utilizar hasta diez atributos de persona diferentes.

>[!BEGINSHADEBOX]

**Caso de uso: variaciones del puesto**

Muchos equipos de marketing y ventas utilizan los puestos como una forma de identificar diferentes personas dentro de una cuenta. Sin embargo, los títulos de los contactos pueden ser incoherentes y utilizar numerosas variaciones para funciones similares. Al crear plantillas de roles de grupo de compra, puede ser necesario definir todos los puestos relacionados posibles para un rol determinado. Puede simplificar estas definiciones y colocar a las personas con títulos de trabajo similares en una sola persona deducida, lo que puede aprovechar en diferentes plantillas de funciones para comprar grupos.

Por ejemplo, podría configurar un personaje llamado _Administración de productos_ y definirlo usando el atributo de puesto de trabajo para los valores de _Administrador de productos_, _Sr. Gerente de productos_, _Gerente de productos sénior_, _PM_, _Sr. PM_, _PM principal_ y _Gerente de producto principal_. A continuación, utilice este personaje en una plantilla de roles donde la condición coincida con _Persona es Product Management_. Al utilizar el perfil configurado, la creación de cada plantilla de funciones es más sencilla y no requiere una condición complicada que pueda coincidir con todos los puestos posibles.

>[!ENDSHADEBOX]

## Acceso a los perfiles configurados

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuraciones]**.

1. Haga clic en **[!UICONTROL Asignación de personalidades]** en el panel intermedio para mostrar la lista de personalidades.

   ![Acceder a los perfiles configurados](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   Desde esta página, puedes [crear](#create-an-engagement-score-model), [editar](#change-the-engagement-weighting-settings) o [eliminar](#delete-a-persona) personalidades.

   La lista de asignación personal. está organizado como una tabla y muestra los personajes actualizados más recientemente en la parte superior (ordenados por _[!UICONTROL Última actualización]_). Puede personalizar la tabla mostrada si hace clic en el icono _Configuración de columna_ ( ![Configuración de columna](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha y activa o desactiva las casillas de verificación de la columna.

![Columnas para mostrar en la lista de asignación de personas](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Para acceder a los detalles de una persona, haga clic en el nombre.

### Personalidades predeterminadas

La lista _Asignación de personas_ incluye cinco personalidades predeterminadas que se definen según el atributo de título del trabajo. Puede editar cualquiera de estos perfiles predeterminados según las necesidades de su organización:

| Persona | Títulos de trabajo |
| ------- | ---------- |
| CXO / EVP - CXO / Vicepresidente ejecutivo | CEO, CIO, CTO, CMO, CFO, Vicepresidente Ejecutivo de Estrategia |
| SVP / VP - Vicepresidente senior / Vicepresidente | vicepresidente senior de marketing, vicepresidente de ventas, vicepresidente de operaciones, vicepresidente de producto, vicepresidente de TI |
| Director Senior / Director - Director Senior / Director | Director de Ingeniería, Director de Producto, Director de Finanzas, Director de Éxito del Cliente |
| Responsable / Responsable - Responsable / Responsable | Director de Marketing, Director de TI, Director de Operaciones, Director de Ventas, Director de Recursos Humanos |
| Colaborador individual: colaborador individual | Ejecutivo de cuentas, Ingeniero de software, Especialista en marketing, Representante de éxito del cliente |
| Analista - Analista | Analista de negocios, Analista de datos, Analista de investigación de mercado, Analista financiero, Analista de operaciones |
| Desarrollador - Desarrollador | Desarrollador front-end, desarrollador back-end, desarrollador de pila completa, desarrollador de aplicaciones móviles, ingeniero de DevOps |
| Personal profesional - Personal profesional | Especialista en Recursos Humanos, Asesor Jurídico, Oficial de Cumplimiento, Gerente de Proyectos, Especialista en Adquisiciones |
| Consultor - Consultor | Consultor de administración, consultor de TI, consultor de procesos empresariales, consultor de marketing |
| Otros - Otros | Especialista en el sector, Asesor independiente, Consultor independiente, Experto en la materia |

### Filtrado de listas

Para localizar el perfil que desea, utilice las herramientas de búsqueda y filtrado:

* Introduzca una cadena de texto en la barra de búsqueda para que coincida con los perfiles por nombre,

  ![Filtrar las definiciones de eventos mostradas](./assets/configuration-events-defs-list-filtered.png){width="700" zoomable="yes"}

* Haga clic en el icono _Filtro_ ( ![Icono de filtro](../assets/do-not-localize/icon-filter.svg) ) en la parte superior izquierda para filtrar la lista mostrada por atributo.

## Crear una persona

1. En el panel de navegación izquierdo, elija **[!UICONTROL Administración]** > **[!UICONTROL Configuración]**.

1. Haga clic en **[!UICONTROL Asignación personal]** en el panel intermedio.

1. Haga clic en **[!UICONTROL Crear persona]**.

1. Escriba un **[!UICONTROL Nombre]** y una **[!UICONTROL Descripción]** únicos (opcionales) para la persona.

1. Seleccione los atributos que se utilizarán para hacer coincidir la persona.

   * Haga clic en **[!UICONTROL Seleccionar atributos de persona]**.

   * En el cuadro de diálogo _[!UICONTROL Seleccionar atributos de persona]_, active la casilla de verificación de cada atributo que desee asignar (un máximo de cinco).

     Puede personalizar la tabla mostrada haciendo clic en el icono _Configuración de columna_ ( ![Configuración de columna](../assets/do-not-localize/icon-column-settings.svg) ) en la esquina superior derecha.

     Para filtrar la lista de atributos por nombre, introduzca una cadena de texto en la barra de búsqueda. También puede hacer clic en el icono _Filtro_ ( ![Icono de filtro](../assets/do-not-localize/icon-filter.svg) ) en la parte superior izquierda para filtrar la lista mostrada por tipo, _Estándar_ o _Personalizado_.

   * Haga clic en **[!UICONTROL Guardar]**.

     Los atributos seleccionados se rellenan en la sección _[!UICONTROL Atributos personales]_.

1. Para cada atributo, introduzca los valores separados por comas que desee que coincidan con el atributo.

   En lugar de un valor, también puede agregar un mensaje que se puede utilizar para identificar una coincidencia. Por ejemplo, puede introducir

1. Haga clic en **[!UICONTROL Crear]**.

## Editar una persona

1. Para acceder a los detalles de la persona, haga clic en el nombre.

## Eliminar una persona

Al eliminar una persona, esta se eliminará de la lista _Asignación de personas_ y ya no estará disponible para su uso en plantillas de funciones.

1. En la página _[!UICONTROL Asignación personal]_, busque el perfil que desee eliminar.

1. Junto al nombre, haga clic en los puntos suspensivos (**...**) de y elija **[!UICONTROL Eliminar]**.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL Eliminar]**.
