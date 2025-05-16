---
title: Datos por intención
description: Aprenda a ensamblar y enviar palabras clave para generar datos de intención para Journey Optimizer B2B edition.
feature: Setup, Intent, Account Insights
roles: Admin
exl-id: c7f9f6fe-2275-42a4-af80-b5c3d1a82837
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Datos de intención

En Journey Optimizer B2B edition, el modelo de detección de intención predice una solución o producto de interés con una confianza lo suficientemente alta según la actividad de un posible cliente. También aprovecha las actividades de otros miembros de la cuenta, junto con el contenido etiquetado. La intención de una persona puede interpretarse como la probabilidad de tener interés en un producto.

* Niveles de intención: disponible en el nivel de cliente potencial, cuenta y grupo de compra conocido.
* Tipos de señal de intención: palabras clave, producto y solución

![Visualización de datos por intención](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

Para activar esta función, puede enviar una lista de palabras clave en una hoja de cálculo al administrador de cuentas de Adobe. Estas palabras clave se utilizan para el etiquetado de contenido.

Se puede asociar un conjunto de palabras clave (hasta 20) a un producto. Un conjunto de productos (hasta 20) se puede asociar con una categoría. Puede tener un máximo de 20 categorías. Todo este modelo se logra a través de una hoja de cálculo simple que se ingiere. La hoja de cálculo puede contener una sola pestaña que se correlaciona con el nombre del producto y una columna que se correlaciona con una lista de palabras clave.

![Palabras clave de datos por intención: ficha de producto única](./assets/intent-data-keywords-single-product-tab.png){width="500" zoomable="yes"}

Puede agregar varias pestañas, cada una con un nombre de producto y toda la hoja de cálculo se puede correlacionar con una categoría.

![Palabras clave de datos por intención: varias fichas de producto](./assets/intent-data-keywords-multiple-product-tabs.png){width="500" zoomable="yes"}
