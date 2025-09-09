---
title: Revisión del informe de spam
description: Genere informes de spam con la puntuación SpamAssassin para comprobar si los correos electrónicos almacenan déclencheur de spam y mejorar la capacidad de envío en Journey Optimizer B2B edition.
feature: Email Authoring
level: Beginner
role: User
exl-id: 0ab2a85c-fbab-4681-9964-74b7fd1d574f
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Revisión del informe de correo no deseado

Muchos proveedores de bandejas de entrada de correo electrónico y la mayoría de los sistemas corporativos emplean un proceso de filtrado de correo no deseado. El envío de correos electrónicos que almacenan en déclencheur estos filtros puede afectar gravemente a la capacidad de entrega. En Journey Optimizer B2B edition, puede comprobar la puntuación de spam del contenido del correo electrónico mediante la generación de un informe de spam. Este informe usa [[!DNL SpamAssassin]](https://spamassassin.apache.org/) para probar el correo electrónico y le ayuda a determinar si las herramientas de filtrado de correo no deseado pueden considerar un mensaje como no deseado. Puede utilizar la información del informe para realizar acciones que mejoren la puntuación del contenido del correo electrónico y la capacidad de envío.

Cuando revise la configuración de correo electrónico o edite el contenido, abra la página _[!UICONTROL Simular]_ y genere un _informe de correo no deseado_ para revisar la puntuación y los elementos marcados que pueden almacenar en déclencheur el filtrado de correo no deseado.

1. En la página _[!UICONTROL Simular]_, haga clic en **[!UICONTROL Informe de spam]** en la parte superior derecha.

   ![Botón de informe de spam](./assets/email-spam-report-button.png){width="700" zoomable="yes"}

   El proceso de creación de informes analiza el contenido del correo electrónico y genera una puntuación con una lista de las reglas de filtrado activadas que se utilizan para generar la puntuación. Los factores incluyen el diseño del cuerpo, la estructura, el tamaño de la imagen, las palabras del déclencheur de spam y otros elementos. Para obtener una lista de las pruebas de evaluación de reglas para los elementos de correo electrónico, consulte la [[!DNL SpamAssassin] lista de pruebas](https://spamassassin.apache.org/old/tests_3_0_x.html).

1. Compruebe las puntuaciones y descripciones de cada elemento.

   >[!NOTE]
   >
   >La puntuación de spam se calcula mediante SpamAssassin y Adobe no posee las reglas ni la lógica de puntuación. Para obtener más información sobre el proyecto de código abierto [!DNL SpamAssassin], consulte la [[!DNL SpamAssassin] documentación](https://cwiki.apache.org/confluence/display/SPAMASSASSIN/).

   Cuanto más baja sea la puntuación, menos probable es que el correo electrónico se marque como correo no deseado.

   ![Puntuación positiva de informe de spam](./assets/email-spam-report-positive.png){width="600" zoomable="yes"}

   Con una puntuación mayor que 5, el informe incluye una advertencia de que algunos mensajes pueden bloquearse o marcarse como correo no deseado cuando se reciben. Se recomienda asegurarse de que la puntuación sea inferior a 2.

   ![Puntuación negativa de informe de spam](./assets/email-spam-report-negative.png){width="600" zoomable="yes"}

1. Si el contenido del correo electrónico contiene elementos que se pueden mejorar, edite el contenido para aplicar las actualizaciones necesarias.

1. Cuando se hayan completado los cambios, vuelva a la página _[!UICONTROL Simular]_ y haga clic en **[!UICONTROL Informe de spam]** de nuevo para comprobar las mejoras de puntuación resultantes.
