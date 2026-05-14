---
title: Probar procesamiento de correo electrónico
description: Pruebe el procesamiento de correo electrónico en clientes de escritorio, móviles y web con la integración de Litmus para garantizar la compatibilidad con la bandeja de entrada en Journey Optimizer B2B edition.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: c8f3fb27-3167-48ac-a66a-fa4bc3f58ddaid: f01b5556-e951-40ba-8625-2e3001864f2bid: e666e996-b2cf-4c45-8fc2-1c625212abab
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cad51180-f8ce-4cb7-aefc-437847b5d6d6
autotag-review: 2026-03-30T22:28:13.343Z
TQID: https://experienceleague.adobe.com/G9c2TdbEje4HgE82tKURAn-UYz5wB-9iLsT9805m1JI
source-git-commit: 9baf03a1ddc1733385b0398ffadde8f548c431cc
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 2%

---

# Prueba de representación de correo electrónico con Litmus

Para probar tus correos electrónicos, puedes aprovechar una cuenta de [Litmus](https://www.litmus.com/email-testing){target="_blank"} Enterprise de Journey Optimizer B2B edition. Con esta integración, puede previsualizar el procesamiento de correo electrónico en clientes de correo electrónico populares. Esta herramienta le ayuda a garantizar que el contenido del correo electrónico tenga un aspecto impecable y funcione según lo diseñado en cada bandeja de entrada.

>[!AVAILABILITY]
>
>Esta integración solo está disponible para usuarios de B2B edition de Journey Optimizer con cuentas de Litmus Enterprise. Para obtener más información, consulte la [página de la solución en el sitio web de Litmus](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}.

1. Una vez completado el diseño del correo electrónico y listo para probarlo, haga clic en **[!UICONTROL Simular contenido]** en el espacio de diseño del correo electrónico.

1. Haga clic en **[!UICONTROL Procesar correo electrónico]** en la parte superior derecha.

   ![Botón Procesar correo electrónico](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Si todavía no se ha conectado a su cuenta de Litmus desde Journey Optimizer B2B edition, la página mostrada proporciona una opción para iniciar una cuenta de prueba o conectarse a su cuenta existente.

1. Haga clic en **[!UICONTROL Conectar su cuenta de Litmus]** en la parte superior derecha o use el vínculo dentro de la página.

   ![Conecte su cuenta de Litmus](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Escriba las credenciales de su cuenta de Litmus y haga clic en **[!UICONTROL Iniciar sesión]**.

1. Haga clic en **[!UICONTROL Conectar]** para confirmar la conexión entre Litmus y Journey Optimizer B2B edition y enviar el contenido del correo electrónico para su procesamiento.

   >[!IMPORTANT]
   >
   >Al conectar su cuenta de Litmus con Journey Optimizer B2B edition, acepta que los mensajes de prueba se envíen a Litmus. A continuación, este contenido se administra dentro de Litmus y no en Adobe. Como consecuencia, la política de correo electrónico de retención de datos de Litmus se aplica a estos correos electrónicos, incluidos los datos de personalización que pueden incluirse en los mensajes de prueba.

1. Haga clic en **[!UICONTROL Ejecutar prueba]** en la parte superior derecha para generar vistas previas de correo electrónico.

   ![Ejecutar una prueba de procesamiento Litmus](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. Compruebe el contenido de su correo electrónico en clientes populares de escritorio, móviles y web.

   Haga clic en la miniatura mostrada para ver los detalles de cualquiera de las pruebas de cliente procesadas.

   ![Vistas previas de correo electrónico Litmus](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. Cuando termine de revisar, haga clic en la flecha hacia atrás ( ![Icono de mostrar u ocultar filtros](../../assets/do-not-localize/icon_back-arrow.svg) ) en la parte superior izquierda para regresar a la página Simular contenido.

   Puede seleccionar otro perfil y realizar otra prueba de procesamiento o volver al espacio de diseño de correo electrónico para realizar los ajustes necesarios según la revisión.
