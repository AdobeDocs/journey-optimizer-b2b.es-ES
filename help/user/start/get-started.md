---
title: Guía de incorporación para administradores y expertos en marketing
description: Como nuevo administrador o usuario de la B2B Edition de Journey Optimizer, obtenga información sobre las áreas clave del proceso de incorporación.
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 1e430af82b972dc73178161e64da10d1cdaaefaf
workflow-type: ht
source-wordcount: '713'
ht-degree: 100%

---

# Guía de incorporación

Las funciones y herramientas que desea abordar en Adobe Journey Optimizer B2B Edition dependen de la función que desempeñe en su equipo. En función de su organización, puede definir varios tipos de usuarios y concederles acceso a determinadas funcionalidades dependiendo de sus permisos.

>[!TIP]
>
>Compruebe sus derechos de licencia y la [descripción del producto](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html?lang=es){target="_blank"} correspondiente sobre las protecciones del rendimiento y las limitaciones estáticas.

>[!BEGINTABS]

>[!TAB Administrador]

Para que su equipo pueda empezar a utilizar las funciones de Adobe Journey Optimizer B2B Edition, es necesario realizar varios pasos para preparar su entorno. Siga estos pasos para que el ingeniero de datos y el experto en marketing puedan empezar a trabajar con Adobe Journey Optimizer B2B Edition.

Como administrador del sistema, necesita comprender los perfiles de producto y asignar permisos para la zona protegida, la administración y la configuración de canal. También debe configurar las zonas protegidas y administrarlas para los perfiles de producto disponibles. A continuación, puede asignar integrantes del equipo a los perfiles de producto. Los administradores de productos que tengan acceso a Adobe Admin Console pueden administrar estas funciones. [Obtenga más información acerca de Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html).

Obtenga información acerca de la administración de acceso en las siguientes páginas:

1. **Crear zonas protegidas** para dividir las instancias en entornos virtuales independientes y aislados. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **Trabaje con su ingeniero de datos** para planificar e implementar la activación de su público y perfil B2B. Revise los modelos publicados y siga las instrucciones según sus necesidades. [Más información](https://experienceleague.adobe.com/es/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **Planifique e implemente la integración de Marketo Engage** para incorporar un esquema personalizado, la ingesta de perfiles y cuentas, y la organización de recorridos personalizados para grupos de compras. [Más información]( https://experienceleague.adobe.com/es/docs/blueprints-learn/architecture/b2b-activation/b2b-journeys-with-marketo){target="_blank"}

1. **Configure el perfil del producto**. Los perfiles del producto son un conjunto de derechos unitarios de Adobe Experience Platform que permiten a los usuarios acceder a determinadas funcionalidades u objetos de la interfaz. [Más información](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Configure los permisos de usuario** para los perfiles del producto, incluidas las zonas protegidas, y otorgue acceso a los integrantes del equipo asignándolos a diferentes perfiles del producto. Este paso se lleva a cabo en Admin Console. [Más información](../admin/user-management.md#create-a-user-group)

1. **Configure el envío de correo electrónico** en Marketo Engage, lo que permite que su equipo envíe contenido de correo electrónico desde los recorridos de la cuenta. [Más información](https://experienceleague.adobe.com/es/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability){target="_blank"}

1. **Configure los servicios de SMS**. Configure uno de los proveedores de SMS de terceros compatibles que ofrecen servicios de mensajería de texto de forma independiente y configure las credenciales de la cuenta en Adobe Journey Optimizer B2B Edition. [Más información](../admin/configure-channels-sms.md)

1. **Configure y habilite el uso de recursos de Adobe Experience Manager** para equipos que usan Assets as a Cloud Service para la administración centralizada de recursos digitales. [Más información](../admin/configure-aem-repositories.md)

1. **Configure las definiciones de eventos de experiencia de Adobe Experience Platform (AEP)** para los equipos responsables de la creación de recorridos de cuenta que permanecen a la escucha de eventos de experiencia de AEP. [Más información](../admin/configure-aep-events.md)

>[!TAB Experto en marketing]

Como especialista en marketing o _profesional de recorridos de cuentas_, es responsable de diseñar recorridos y crear contenido. Puede empezar a trabajar con Adobe Journey Optimizer B2B Edition después de que el administrador del sistema y el ingeniero de datos preparen su entorno y le concedan acceso.

Consulte las siguientes secciones para configurar su primer recorrido, añadir recursos y enviar contenido:

1. **Añadir públicos en la cuenta**. Journey Optimizer B2B Edition le permite crear públicos en la cuenta mediante definiciones de segmentos directamente desde la aplicación y aprovecharlos en sus recorridos de la cuenta. [Más información](../audiences/account-audience-overview.md)

1. **Cree grupos de compras**. Defina los componentes clave para alcanzar sus metas y objetivos empresariales, y cree grupos de compras que identifiquen a los miembros para sus listas de cuentas objetivo. [Más información](../buying-groups/buying-groups-overview.md)

1. **Creación y administración de recursos**. Adobe Experience Manager Assets Essentials proporciona un único repositorio centralizado de recursos que puede utilizar para cumplimentar los mensajes. [Más información](../content/assets-overview.md)

1. **Añada plantillas de correo electrónico personalizadas y dinámicas**. Aproveche las funcionalidades de personalización y contenido dinámico de Journey Optimizer B2B Edition para adaptar el mensaje a su público. [Más información](../content/email-templates.md)

1. **Diseñe recorridos de clientes para ofrecer experiencias personalizadas y contextuales**. Journey Optimizer B2B Edition le permite crear casos de uso de orquestación en tiempo real con datos contextuales almacenados en eventos o fuentes de datos. Diseñe escenarios avanzados que constan de varios pasos con las siguientes funcionalidades:

   * Envíe en tiempo real entregas unitarias que se activan cuando se recibe un evento, o por lotes con los públicos de Adobe Experience Platform.

   * Utilice datos contextuales de eventos, información de Adobe Experience Platform o datos de servicios API de terceros.

   * Utilice las acciones de canal integradas (correo electrónico y SMS) para enviar mensajes diseñados en Journey Optimizer B2B Edition.

   * En el mapa del recorrido, cree casos de uso de varios pasos, añada condiciones y envíe mensajes personalizados.

[Más información](../journeys/journey-overview.md)

>[!ENDTABS]
