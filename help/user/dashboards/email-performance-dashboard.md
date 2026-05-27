---
title: Informe de rendimiento de los correos electrónicos
description: Utilice el informe Rendimiento del correo electrónico de Journey Optimizer B2B edition para monitorizar las métricas de envío, envío, participación y exclusión de correo electrónico en todos los recorridos de una sola vista unificada.
feature: Dashboards, Reporting
role: User
autotag-review: '2026-05-21T15:04:51.176Z'
TQID: 'https://experienceleague.adobe.com/hA63o9-2-atw0kRNFeEu6H449WmZ59CjL3uiVS7nEcA'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2:
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 8226114f1a34adf85437579ef17a50b80ccfa596
workflow-type: tm+mt
source-wordcount: 833
ht-degree: 5%

---

# Informe de rendimiento del correo electrónico

El informe **Rendimiento del correo electrónico** proporciona a los especialistas en marketing una vista unificada de la actividad del correo electrónico en todos los recorridos de Adobe Journey Optimizer B2B edition. Agrupa las métricas de envío, envío, participación y exclusión. Al mostrar los recuentos sin procesar y las tasas calculadas, puede monitorizar el estado de la campaña, comparar el rendimiento del correo electrónico e identificar los problemas de envío o participación de un vistazo. Para obtener métricas de nivel de recorrido en canales de correo electrónico y SMS, consulte el [tablero de Recorridos de cuenta](./journeys-dashboard.md).

## Acceso al informe

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Tablero]**.
1. Seleccione la pestaña **[!UICONTROL Rendimiento del correo electrónico]** en la parte superior del panel de informes.

![Informe de rendimiento del correo electrónico](./assets/email-performance-dashboard.png){width="800" zoomable="yes"}

## Filtrado de datos

Haga clic en el icono _Filtro_ ( ![Icono de filtro](../assets/do-not-localize/icon-filter.svg) ) en la parte superior izquierda para filtrar la visualización de datos usando los dos tipos de filtro admitidos. Estos filtros se aplican a todos los paneles simultáneamente:

* **[!UICONTROL Recorrido]**: filtra el informe para mostrar datos de uno o más recorridos seleccionados. Utilice este filtro para aislar el rendimiento de los recorridos importantes para su campaña o programa.

* **Intervalo de fechas** - Restringe todas las métricas a correos electrónicos enviados dentro del intervalo de tiempo especificado. Admite intervalos preestablecidos y un selector de fechas personalizado. El selector de intervalo de fechas se encuentra en la esquina superior derecha del panel.

![Filtros de Recorrido e intervalo de fechas en el cuadro de diálogo Filtros](./assets/email-performance-filters.png){width="500"}

Cuando cambie los filtros en el cuadro de diálogo de filtros, haga clic en **[!UICONTROL Aplicar]**.

## Gráficos de métricas de recuento y tasa

La sección superior del informe de rendimiento de correo electrónico contiene dos gráficos de barras paralelos que proporcionan un resumen visual del estado general del programa de correo electrónico en el intervalo de fechas y el recorrido seleccionados.

**Contar métricas**: muestra el volumen absoluto de actividad de correo electrónico. Cada barra representa el recuento total de un evento de correo electrónico clave en todos los correos electrónicos del ámbito filtrado: Enviados, Entregas, Aperturas, Clics, Devoluciones y Cancelaciones de suscripción.

**Métricas de tasa**: muestra las tasas de porcentaje calculadas, lo que le permite evaluar la calidad de la participación y la capacidad de entrega independientemente del volumen: tasa de entrega, tasa de apertura, tasa de clics, tasa de devoluciones, tasa de clics hasta apertura y tasa de cancelación de suscripción.

Pase el ratón sobre el gráfico para ver datos numéricos.

![Pase el ratón sobre el gráfico de barras - recuento mostrado](./assets/email-performance-counts-hover.png){width="500"}

| Métrica | Tipo | Descripción |
|--------|------|-------------|
| Enviado | Conteo | Número total de mensajes de correo electrónico enviados para su envío. |
| Enviados | Conteo | Correos electrónicos aceptados correctamente por el servidor de correo del destinatario. |
| Abierto | Conteo | Número de correos electrónicos enviados que se abrieron al menos una vez. |
| Hizo clic en | Conteo | Número de correos electrónicos que han recibido al menos un clic en vínculo. |
| Rechazados | Conteo | Correos electrónicos que no se han podido enviar (rechazos graves o leves). |
| Cancelaciones de suscripción | Conteo | Destinatarios que se excluyeron mediante un vínculo de cancelación de suscripción en el correo electrónico. |
| Tasa de entrega | Tasa | Entregado ÷ enviado. Indica el porcentaje de correos electrónicos que llegaron a las bandejas de entrada. |
| Tasa de apertura | Tasa | Abierto ÷ Entregado. Mide la participación del destinatario con las líneas de asunto. |
| Tasa de pulsaciones | Tasa | Se Hizo Clic ÷ Entregar. Mide la participación de clics generales por correo electrónico enviado. |
| Tasa de rechazo | Tasa | ÷ rechazados enviados. Resalta la capacidad de entrega y enumera los problemas de estado. |
| Tasa de pulsaciones para abrir (CTOR) | Tasa | Haga Clic ÷ Abrir. Mide el contenido y la eficacia de CTA entre los lectores comprometidos. |
| Tasa de cancelación de la suscripción | Tasa | Cancela La Suscripción ÷ Entregado. Indica relevancia y ajuste de la audiencia. |

## Tabla de rendimiento de correo electrónico

En la parte inferior de la página, se muestra una tabla detallada con las métricas por correo electrónico de cada recurso de correo electrónico en el ámbito filtrado. De forma predeterminada, la tabla muestra 10 filas por página.

La columna **Cancelar la suscripción %** es una métrica priorizada para supervisar la actividad de exclusión directamente en la vista de tabla.

| Columna | Descripción |
|--------|-------------|
| Nombre de email | El nombre de [recurso de correo electrónico](../content/add-email.md) configurado en la recorrido. |
| Enviado | Total de envíos para este correo electrónico dentro del intervalo de fechas seleccionado. |
| Enviados | Número de correos electrónicos enviados correctamente a los servidores de correo de destinatario. |
| % de envío | Entregado ÷ Enviado, expresado como porcentaje. |
| Aperturas | Número total de eventos abiertos registrados para este correo electrónico. |
| Abrir % | Abre ÷ Entregado, expresado como un porcentaje. |
| Clics | Total de eventos de clic en vínculo para este correo electrónico. |
| Haga clic en % | Los clics ÷ entregados, expresados como porcentaje. |
| % DE CTOR | Tasa de clics para abrir: clics ÷ aperturas, expresados como porcentaje. |
| Devoluciones | Número de correos electrónicos no entregables (rechazos graves y leves). |
| % de rebote | Devoluciones ÷ enviadas, expresadas como porcentaje. |
| Porcentaje de cancelación de suscripciones | Cancela La Suscripción ÷ Entregado. Métrica priorizada para monitorizar el estado de exclusión. |
| Primera actividad | Marca de tiempo del primer evento registrado (enviar, abrir o hacer clic) para este correo electrónico en el período seleccionado. |
| Última actividad | Marca de tiempo del evento registrado más reciente para este correo electrónico en el período seleccionado. |

## Exportar datos del informe

El informe de rendimiento del correo electrónico admite la exportación de datos para un análisis más detallado en herramientas externas o para compartir resultados con las partes interesadas. Puede exportar los datos de la tabla en formato CSV, que es compatible con cualquier herramienta de análisis de datos o BI.

>[!CAUTION]
>
>Las exportaciones reflejan los filtros activos actualmente. Asegúrese de que el intervalo de fechas y los filtros de recorrido estén correctamente configurados antes de exportar para evitar datos incompletos en el archivo de salida.

**_Para exportar datos de informe:_**

1. Establezca su intervalo de fechas en la parte superior derecha y aplique el filtrado **[!UICONTROL Recorrido]** según sea necesario.
1. Haga clic en el icono de menú **...** en la esquina superior derecha del panel Rendimiento del correo electrónico y elija **[!UICONTROL Ver más]**.
1. Haga clic en **[!UICONTROL Descargar CSV]** en el menú.

   ![Ver datos detallados y descargar CSV](./assets/email-performance-data-export.png){width="700" zoomable="yes"}

   El archivo se descarga automáticamente en la ubicación de descarga predeterminada del explorador.

1. Haga clic en **[!UICONTROL Cerrar]** para volver al informe de rendimiento del correo electrónico.
