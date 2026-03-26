---
title: Configuración del correo electrónico
description: Configure las opciones de Marketo Engage para la entrega de correo electrónico B2B de Journey Optimizer, incluidos los valores predeterminados, la cancelación de la suscripción, la vista web, los límites de objetos de Velocity, el seguimiento de encabezados y el filtrado de bots.
feature: Setup, Channels
role: Admin
exl-id: 5b28d8f2-a3a4-420a-ab03-d1115cf3ab61
source-git-commit: 0a9cff812d0631a34a09cca059ffb8496248c2b4
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 83%

---

# Configuración de correo electrónico

Para admitir la infraestructura de envío de correo electrónico proporcionada por la instancia de Marketo Engage adjunta, establezca las siguientes opciones de correo electrónico. Un administrador de productos de Marketo Engage puede establecer esta configuración navegando al área de **[!UICONTROL Admin]** en la instancia de Marketo Engage y seleccionando **[!UICONTROL Correo electrónico]**.

## Configuración de correo electrónico

Para configurar los valores predeterminados de correo electrónico de la instancia de Marketo Engage adjunta, cambie los valores configurados para reflejar el uso por parte de su organización de marketing.

### Desde correo electrónico y etiqueta

Cambie los valores del correo electrónico De y la etiqueta para que los nuevos correos electrónicos se rellenen automáticamente con estos valores predeterminados.

>[!NOTE]
>
>El cambio solo se aplica a los correos electrónicos que crea y no a otros usuarios de Marketo Engage o Journey Optimizer B2B edition.

1. Vaya al área de **[!UICONTROL Admin]** en la instancia de Marketo Engage adjunta y seleccione **[!UICONTROL Correo electrónico]**.

1. En el panel _[!UICONTROL Configuración]_, escriba los valores predeterminados que desee para **[!UICONTROL De correo electrónico]** y **[!UICONTROL De etiqueta]**.

   ![Configuración de correo electrónico - Valores predeterminados de las etiquetas Desde correo electrónico y Desde](./assets/me-admin-email-settings-from.png){width="500"}

1. Haga clic en **[!UICONTROL Guardar cambios]**.

### Mensajes de cancelación de suscripción

Para los correos electrónicos de marketing no operativos, el texto de cancelación de suscripción y los vínculos se anexan en la parte inferior. Como administrador de productos, debe configurar el HTML predeterminado y el texto que se rellena cuando un experto en marketing no marca el correo electrónico como operativo.

1. Vaya al área de **[!UICONTROL Admin]** en la instancia de Marketo Engage adjunta y seleccione **[!UICONTROL Correo electrónico]**.

1. En el panel _[!UICONTROL Configuración]_, escriba los valores predeterminados que desee para **[!UICONTROL Cancelar la suscripción a HTML]** y **[!UICONTROL Cancelar la suscripción a Text]**.

   >[!TIP]
   >
   >Los especialistas en marketing pueden cambiar la posición de HTML para cancelar la suscripción en su correo electrónico mediante tokens del sistema.

   ![Configuración de correo electrónico: valores predeterminados Cancelar la suscripción a HTML y Cancelar la suscripción de texto](./assets/me-admin-email-settings-unsubscribe.png){width="500"}

   >[!CAUTION]
   >
   >Las siguientes variables son críticas. **No los elimine**.
   >
   >* `%mkt_opt_out_prefix%`
   >* `mkt_unsubscribe=1&mkt_tok=##MKT_TOK##`

1. Haga clic en **[!UICONTROL Guardar cambios]**.

Si alguna vez necesita volver al contenido predeterminado del sistema, copie y pegue lo siguiente:

+++ Texto de cancelación de suscripción predeterminado del sistema

```
<p><font face="Verdana" size="1">If you no longer wish to receive these emails, click on the following link: <a href="%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##">Unsubscribe</a><br/></font></p>` [!UICONTROL Unsubscribe Text]:
%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##
```

+++

### Ver como página web

El contenido del correo electrónico tiene capacidades de visualización limitadas (CSS limitado y sin JavaScript ni formularios). Los especialistas en marketing pueden usar la opción _Ver como página web_ para aplicar una cookie para el destinatario de correo electrónico mediante Marketo Munchkin. Como administrador de productos, debe configurar el HTML predeterminado y el texto que se rellena cuando un experto en marketing elige esta opción.

1. Vaya al área de **[!UICONTROL Admin]** en la instancia de Marketo Engage adjunta y seleccione **[!UICONTROL Correo electrónico]**.

1. En el panel _[!UICONTROL Configuración]_, cambie el contenido en los campos **[!UICONTROL Ver como HTML de página web]** y **[!UICONTROL Ver como texto de página web]** para reflejar el tono y los mensajes.

   ![Configuración de correo electrónico - Ver como HTML de página web y Ver como texto de página web valores predeterminados](./assets/me-admin-email-settings-view-as-web-page.png){width="500"}

   >[!CAUTION]
   >
   >Las siguientes variables son críticas. **No los elimine**.
   >
   >`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
   >
   >La segunda parte `##MKT_TOK##` es la cookie de Munchkin de esa persona. Garantiza que las cookies se apliquen correctamente cuando el destinatario del correo electrónico haga clic en el vínculo.
   >
   >Asegúrese de evitar:
   >
   >* Añadir direcciones URL adicionales a cualquiera de los cuadros de HTML
   >* Incluir HTML en la versión de texto

1. Haga clic en **[!UICONTROL Guardar cambios]**.

Si alguna vez necesita volver al contenido predeterminado del sistema, copie y pegue lo siguiente:

+++ HTML de página web predeterminada del sistema

```
<div style="text-align: center"><font face="Verdana" size="1">To view this email as a web page, <a href="%mkt_webview_url%?mkt_tok=##MKT_TOK##">click here</a></font></div>
```

+++

+++ Texto de página web predeterminada del sistema

```
To view this email as a web page, go to the following address:
`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
```

+++

## Límites de recuperación de objetos personalizados

Si usa [!DNL Velocity Script] para mostrar datos de objeto personalizados en mensajes de correo electrónico, ajuste el límite de recuperación de objeto personalizado principal. De forma predeterminada, el límite permite el acceso a 10 objetos personalizados principales desde Secuencia de comandos de Velocity. Puede aumentar este límite si es necesario.

[[!DNL Apache Velocity]](https://velocity.apache.org/) es un lenguaje creado en [!DNL Java] que está diseñado para crear plantillas y scripts de contenido de HTML. La infraestructura de correo electrónico de Marketo Engage admite su uso en el contexto de los correos electrónicos a través de tokens de scripts, que proporcionan acceso a los datos almacenados en objetos personalizados.

Puede hacer referencia a objetos personalizados primarios y secundarios que estén conectados directamente al posible cliente o contacto, pero no a objetos personalizados de tercer nivel. Para cada objeto personalizado, los 10 registros actualizados más recientemente por persona/contacto están disponibles en tiempo de ejecución y se ordenan desde los más recientes (en `0`) a los más antiguos (en `9`).

_Para cambiar el límite :_

1. Vaya al área de **[!UICONTROL Admin]** en la instancia de Marketo Engage adjunta y seleccione **[!UICONTROL Correo electrónico]**.

1. Desplácese al panel _[!UICONTROL Límites personalizados de recuperación de objetos]_ e introduzca un nuevo valor en **[!UICONTROL Límite de recuperación principal]**
field.

   ![Administrador de correo electrónico de Marketo Engage - Límites de recuperación de objetos personalizados - valores predeterminados](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   Se admiten valores entre 10 y 100. El _[!UICONTROL límite de recuperación secundaria]_ se establece automáticamente al dividir 1000 por el límite principal. Por ejemplo, si establece el límite principal en 50, el límite secundario se calcula como 20 (1000 ÷ 50 = 20).

1. Haga clic en **[!UICONTROL Guardar cambios]**.

## Opciones de encabezado personalizadas

Cambie _[!UICONTROL Opciones de encabezado personalizado]_ para el correo electrónico con el fin de configurar los encabezados de los vínculos de seguimiento de correo electrónico. Habilite estas opciones para implementar vínculos de seguimiento seguros mediante HTTPS con transporte estricto.

1. Vaya al área de **[!UICONTROL Admin]** en la instancia de Marketo Engage adjunta y seleccione **[!UICONTROL Correo electrónico]**.

1. Desplácese al panel _[!UICONTROL Opciones de encabezado personalizado]_ y cambie la configuración según las directivas de vínculos de seguimiento:

   ![Administrador de correo electrónico de Marketo Engage - Configuración predeterminada de opciones de encabezado personalizadas](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   * **[!UICONTROL Seguridad de transporte estricta]**: establezca esta opción en Habilitada para garantizar que los vínculos de seguimiento siempre se proporcionen a través de HTTPS (solo debe establecerse para suscripciones con vínculos de seguimiento protegidos por SSL).
   * **[!UICONTROL Max-age]**: este campo admite la directiva obligatoria para especificar el tiempo, en segundos, que el explorador debe recordar para acceder únicamente al dominio a través de HTTPS.
   * **[!UICONTROL IncludeSubDomains]**: utilice esta opción para incluir la directiva que aplica la directiva HSTS a todos los subdominios del host.

   >[!IMPORTANT]
   >
   >Revise esta configuración con su equipo de TI para asegurarse de que está alineada con la política de su organización. Una configuración incorrecta puede impedir que algunos visitantes accedan a sus vínculos de correo electrónico.

1. Haga clic en **[!UICONTROL Guardar cambios]**.

## Filtrar actividad de bots de correo electrónico {#filter-email-bots}

La actividad de bots de correo electrónico, también conocida como interacción no humana (NHI), puede inflar los datos de _aperturas_ y _clics_ del correo electrónico, distorsionando las métricas de participación y activando la progresión de recorridos basada en eventos. Utilice el filtrado de bots de correo electrónico para mantener la integridad de las métricas y perspectivas de participación de clics. Existen dos métodos para identificar la sospecha de actividad de bots:

* _&#x200B;**[!UICONTROL Coincidencia con la lista de bots de la IAB]**&#x200B;_: las actividades que coinciden con cualquier elemento de la [lista de bots de la empresa de Advertising interactiva](https://www.iab.com/guidelines/iab-abc-international-spiders-bots-list/){target="_blank"} (agente de usuario/dirección IP) están marcadas como bots.
* _&#x200B;**[!UICONTROL Coincidencia con el patrón de proximidad]**&#x200B;_: dos o más actividades que se producen al mismo tiempo (en menos de un segundo) se identifican como bots. Los atributos considerados durante la comparación son:
   * ID de posible cliente (debe ser el mismo)
   * Recurso de correo electrónico (debe ser el mismo)
   * Clic en vínculo o correo electrónico abierto

Para la actividad de clic en vínculo de correo electrónico y de apertura de correo electrónico, los atributos se rellenan con los siguientes valores:

* Actividades identificadas como bots: _Actividad de bots_ = `true` y _Patrón de actividad de bots_ = patrón/método identificado
* Actividades que se han identificado como no bots - _Actividad de bots_ = `false` y _Patrón de actividad de bots_ = `n/a`

### Definición de los filtros

1. Vaya al área de **[!UICONTROL Admin]** en la instancia de Marketo Engage adjunta y seleccione **[!UICONTROL Correo electrónico]**.

1. Seleccione la ficha **[!UICONTROL Actividad de bots]**.

   ![Administrador de correo electrónico de Marketo Engage - ficha Actividad de bots](./assets/me-admin-email-bot-activity.png){width="700" zoomable="yes"}

   El panel Identificación de actividad de bots muestra dos controles deslizantes que puede utilizar para identificar la actividad de bots.

1. Cambie el control deslizante para habilitar uno o ambos.

   Para cada método que habilite, elija _[!UICONTROL Registrar actividad de bots]_ o _[!UICONTROL Filtrar actividad de bots]_.

   >[!IMPORTANT]
   >
   >Si eliges [!UICONTROL Filtrar actividad de bots], es posible que veas una caída en las aperturas y los clics de correos electrónicos porque se eliminan las actividades falsas.

   ![Administrador de correo electrónico de Marketo Engage - Opciones de identificación de actividad de bots](./assets/me-admin-email-bot-activity-set-filters.png){width="500"}

   Para _[!UICONTROL Coincidir con el patrón de proximidad]_, también puede establecer el número de segundos para **[!UICONTROL Duración entre actividades]** (el valor predeterminado es `0`, el máximo es `3`).

   >[!NOTE]
   >
   >Con _Duración entre actividades_ establecida en `0` segundos, Marketo Engage identifica las actividades de correo electrónico que se producen en ese segundo exacto. Si se producen varias actividades de correo electrónico en el número designado de segundos, se identifica como actividad de bots.

   Para desactivar cualquiera de los métodos de filtrado, coloque el control deslizante a la izquierda. Si lo hace, los datos no se restablecen.

### LISTA DE BLOQUEADOS IP

Adobe ha identificado una lista de direcciones IP responsables de generar millones de participaciones falsas, ya que las participaciones recibidas de cualquiera de las siguientes direcciones IP se filtran automáticamente y no se agregan a la instancia de Marketo Engage. Este filtrado puede reducir las aperturas de correo electrónico, los clics y otras actividades relacionadas. Esta lista puede actualizarse periódicamente.

+++ Direcciones IP bloqueadas

* 40.94.34.52
* 40.94.34.86
* 52.34.76.65
* 54.70.53.60
* 54.71.187.124
* 60.28.2.248
* 64.235.150.252
* 64.235.153.10
* 64.235.153.2
* 64.235.154.105
* 64.235.154.109
* 64.235.154.140
* 64.74.215.1
* 64.74.215.100
* 64.74.215.138
* 64.74.215.139
* 64.74.215.142
* 64.74.215.146
* 64.74.215.150
* 64.74.215.154
* 64.74.215.158
* 64.74.215.162
* 64.74.215.164
* 64.74.215.166
* 64.74.215.170
* 64.74.215.174
* 64.74.215.176
* 64.74.215.178
* 64.74.215.51
* 64.74.215.56
* 64.74.215.58
* 64.74.215.59
* 64.74.215.86
* 64.74.215.98
* 65.154.226.101
* 66.249.91.149
* 70.42.131.106
* 74.125.217.116
* 74.217.90.250
* 104.129.41.4
* 104.47.55.126
* 104.47.58.126
* 104.47.70.126
* 104.47.73.126
* 104.47.73.254
* 104.47.74.126
* 128.220.160.1
* 155.70.39.101
* 162.129.251.14
* 162.129.251.42
* 208.52.157.204

>[!NOTE]
>
>Cada dirección IP se analiza y examina cuidadosamente antes de incluirse en esta lista, lo que garantiza que solo se bloqueen las direcciones IP más críticas y dañinas.

+++
