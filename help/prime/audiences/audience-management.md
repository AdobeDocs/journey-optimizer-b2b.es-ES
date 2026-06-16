---
title: Gestión de público
description: Página de marcador de posición para audiencias.
autotag-review: '2026-06-12T22:47:10.727Z'
TQID: 'https://experienceleague.adobe.com/KWT9-Lr6358MQ0sLQyKAlb4SLERnBl-QQL7Cj1iXCZM'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: beb5f4be-cec3-471a-9db6-831a77dd3ac9id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c844cb4fb520f802c18a9988461c39106000b778
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 3%

---

# Gestión de público

En el centro de administración de mercadotecnia, haga clic en **[!UICONTROL Listas de personas]** en el panel de navegación derecho.

![Acceder a listas de personas para administrar tus audiencias](./assets/people-lists.png){width="800" zoomable="yes"}

Hay dos fichas para la página donde puede ver y administrar **[!UICONTROL listas dinámicas]** y **[!UICONTROL listas estáticas]**. Haga clic en la pestaña para cambiar la vista de lista entre cada tipo.

Desde esta página puede:

* Creación de nuevas listas dinámicas y estáticas
* Buscar listas existentes
* Consulte la información del recurso
* Acceso a listas para revisar su pertenencia

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across AJO B2B. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## Creación de una lista de personas


Para crear una lista dinámica o estática:

1. Haga clic en **[!UICONTROL Crear lista]** en la parte superior derecha de la página _[!UICONTROL Listas de personas]_.
1. Seleccione un programa como **[!UICONTROL Principal]** de la lista.
1. Escriba la lista a **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]** (opcional).
1. Elija y luego enumere **[!UICONTROL Type]**:

   * **[!UICONTROL Estático]**: la pertenencia se determina mediante filtros calificadores evaluados al crear la lista. La inscripción a la lista no se actualiza a menos que califique o descalifique manualmente registros.
***[!UICONTROL Dinámico]**: la pertenencia se determina dinámicamente mediante filtros que cumplen los requisitos. La inscripción a la lista se actualiza automáticamente.

1. Haga clic en **[!UICONTROL Crear]**.

>[!NOTE]
>
>Eliminar y duplicar no son compatibles actualmente con las listas de personas en esta versión de Beta.

## Listas estáticas

La pertenencia a una lista estática se define mediante filtros simples que hacen referencia a los atributos y las actividades de las personas. La pertenencia no cambia a menos que califique o descalifique manualmente a los miembros.

>[!NOTE]
>
>Las definiciones de filtros de lista estática se aplican una sola vez cuando se agregan o se quitan miembros de la lista. El filtro definido no está disponible posteriormente. Si desea mantener una definición de audiencia coherente mediante filtros, utilice una lista dinámica en su lugar.

### Añadir miembros

1. Abra la lista estática y haga clic en **[!UICONTROL Agregar personas]** en la parte superior derecha.

1. En el cuadro de diálogo, defina las reglas para calificar los posibles clientes arrastrando y soltando filtros desde la izquierda.

   Puede filtrar personas mediante cualquier combinación de:

   * Historial de actividad
   * Atributos de la compañía
   * Atributos de la persona
   * Filtros especiales, como pertenencia a Recorridos

1. Para guardar los cambios, haga clic en **[!UICONTROL Listo]**.

1. Seleccione la ficha **[!UICONTROL Miembros]**.

   Después de un breve tiempo, los miembros calificados aparecen en la lista.

### Quitar miembros

1. Abra la lista estática y haga clic en **[!UICONTROL Quitar personas]** en la parte superior derecha.

1. En el cuadro de diálogo, agregue los filtros para que coincidan con los miembros que desea descalificar.

1. Para guardar los cambios, haga clic en **[!UICONTROL Listo]**.

1. Seleccione la ficha **[!UICONTROL Miembros]**.

   Después de un breve tiempo, los miembros descalificados abandonan la lista.

## Listas dinámicas

La pertenencia a listas dinámicas se define mediante filtros simples que hacen referencia a atributos y actividades de personas. La pertenencia se mantiene automáticamente calificando y descalificando posibles clientes según la lógica del filtro.

### Definir la lógica de pertenencia

1. Abra la lista estática y seleccione la pestaña Reglas.

1. Haga clic en Editar reglas.

1. En el cuadro de diálogo, defina las reglas para calificar los posibles clientes arrastrando y soltando filtros desde la izquierda.

   Puede calificar a los posibles clientes para la lista mediante cualquier combinación de:

   * Historial de actividad
   * Atributos de la compañía
   * Atributos de la persona
   * Filtros especiales, como pertenencia a Recorridos

1. Para guardar los cambios, haga clic en **[!UICONTROL Listo]**.

1. Seleccione la ficha **[!UICONTROL Miembros]**.

   Después de un breve tiempo, los miembros calificados aparecen en la lista.

Para abrir la página de detalles del perfil del posible cliente, en la que puede ver el resumen y las actividades recientes, haga clic en el nombre de una persona en la lista.