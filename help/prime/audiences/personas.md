---
title: Personas derivadas
description: Utilice personalidades derivadas en Journey Optimizer B2B Prime para segmentar listas de personas y rutas de recorrido. Conozca las asignaciones de personas predeterminadas y el filtro Persona derivada.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-23T22:01:21.605Z'
TQID: 'https://experienceleague.adobe.com/OZ4GDkaqg9a5Aikic-m-f0MtHSpc3BO0h41fTAL1Rww'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: af10a912422f1736fdc86e0609aee76f5d4daa46
workflow-type: tm+mt
source-wordcount: 650
ht-degree: 2%

---

# Personas derivadas

La clasificación personal transforma los datos sin procesar de los clientes en una comprensión semántica del comprador que la IA puede utilizar para generar contexto y dirigir decisiones personalizadas en todos los canales y recorridos. Este perfil unificado proporciona lo siguiente:

* _ramificación de Recorridos_: las rutas divididas dirigen a los posibles clientes por persona, profundidad de participación y rol
* _Arbitraje de Recorrido_: determina a qué elemento nutritivo pertenece un posible cliente en este momento, evitando conflictos de mensajes entre programas simultáneos
* _Personalización de contenido_: contenido que es narrativas específicas de roles (&quot;para un ejecutivo&quot; vs. &quot;para un profesional&quot;)
* _Contexto del calificador de ventas_ - Los BDR obtienen un informe de una pantalla que muestra &quot;quién es esta persona, qué les importa, dónde se encuentran en el recorrido del comprador&quot;

## Personalidades predeterminadas {#default-ersonas}

Para la versión de Beta de Journey Optimizer B2B Prime, las siguientes personas predeterminadas se definen según el atributo del puesto:

| Persona | Títulos de trabajo |
| ------- | ---------- |
| [!UICONTROL CXO / EVP] | CEO, CIO, CTO, CMO, CFO, Vicepresidente Ejecutivo de Estrategia |
| [!UICONTROL SVP / VP] | vicepresidente senior de marketing, vicepresidente de ventas, vicepresidente de operaciones, vicepresidente de producto, vicepresidente de TI |
| [!UICONTROL Responsable principal / Responsable] | Director de Marketing, Director de TI, Director de Operaciones, Director de Ventas, Director de Recursos Humanos |
| [!UICONTROL Colaborador individual] | Ejecutivo de cuentas, Ingeniero de software, Especialista en marketing, Representante de éxito del cliente |
| [!UICONTROL Analista] | Analista de negocios, Analista de datos, Analista de investigación de mercado, Analista financiero, Analista de operaciones |
| [!UICONTROL Desarrollador] | Desarrollador front-end, desarrollador back-end, desarrollador de pila completa, desarrollador de aplicaciones móviles, ingeniero de DevOps |
| [!UICONTROL Personal del Cuadro Orgánico] | Especialista en Recursos Humanos, Asesor Jurídico, Oficial de Cumplimiento, Gerente de Proyectos, Especialista en Adquisiciones |
| [!UICONTROL Consultor] | Consultor de administración, consultor de TI, consultor de procesos empresariales, consultor de marketing |
| [!UICONTROL Otras] | Especialista en el sector, Asesor independiente, Consultor independiente, Experto en la materia |

>[!NOTE]
>
>En la versión de General Availability, podrá editar cualquiera de estas personalidades predeterminadas según las necesidades de su organización. También admite la asignación y las definiciones de personas personalizadas.

## Filtrar por persona derivada {#derived-persona-filter}

Journey Optimizer B2B Prime deriva un registro de persona para cada persona mediante la evaluación de los atributos del registro frente a las personas definidas. Puede utilizar el resultado deducido (_Persona derivada_) como filtro al definir la audiencia para una lista de personas o para segmentar en un recorrido de personas.

El filtro _[!UICONTROL Persona derivada]_ aparece en el panel de filtro bajo la categoría **[!UICONTROL Atributos de persona]**.

### Listas de personas {#people-lists}

Cuando agrega o quita miembros de una [lista de personas estáticas](./people-lists.md#static-list), o cuando define las reglas de pertenencia para una [lista de personas dinámicas](./people-lists.md#dynamic-lists), puede filtrar por Persona derivada para dirigirse a todas las personas cuyos atributos coincidan con una persona configurada específica.

![Filtro de persona derivado para una lista de personas](./assets/derived-persona-filter-people-list.png){width="750" zoomable="yes"}

**Lista estática — Agregar miembros**

1. Abra la lista estática y haga clic en **[!UICONTROL Agregar personas]** en la parte superior derecha.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de personas]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para aplicar el filtro y calificar a las personas coincidentes en la lista.

**Lista dinámica — Establecer reglas de pertenencia**

1. Abra la lista dinámica y seleccione la ficha **[!UICONTROL Reglas]**.

1. Haga clic en **[!UICONTROL Editar reglas]**.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de personas]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para guardar la regla.

   La pertenencia se actualiza automáticamente a medida que se evalúan los registros de persona según la regla.

### Recorridos de persona {#person-journeys}

Al configurar la segmentación para un recorrido de persona en un nodo [_Split paths_](../marketing/split-merge-paths-nodes.md), puede usar un perfil derivado como un filtro de perfil de persona para controlar qué personas ingresan a la ruta de recorrido.

![Filtro de persona derivada para una condición de ruta dividida](./assets/derived-persona-filter-split-path.png){width="750" zoomable="yes"}

1. Haga clic en el nodo **[!UICONTROL Dividir rutas]** en el lienzo de recorrido.

1. En el panel de propiedades del nodo de la derecha, haga clic en **[!UICONTROL Aplicar condición]** o **[!UICONTROL Editar condición]** para una ruta.

1. En el cuadro de diálogo de filtro, expanda **[!UICONTROL Atributos de personas]** y arrastre **[!UICONTROL Persona derivada]** al lienzo.

1. En la condición de filtro, elija **[!UICONTROL is]** y seleccione una o más personalidades de la lista.

1. Haga clic en **[!UICONTROL Listo]** para guardar el filtro de la ruta.
