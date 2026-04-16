---
title: Configurar lista de comprobación
description: Configure Journey Optimizer B2B Edition. Configure esquemas XDM, canales de correo electrónico/SMS, acciones de recorrido de Marketo Engage y usuarios.
feature: Setup, Administration
role: Admin, Developer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
source-git-commit: 944d2616fa21e7f8d2f8c439eaa2f5e529dacb84
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 83%

---

# Configurar lista de comprobación

Adobe Journey Optimizer B2B Edition se basa en Adobe Experience Platform. Con esta implementación, Journey Optimizer B2B Edition y Marketo Engage no están en el mismo sistema y en el mismo almacén de datos. Journey Optimizer B2B Edition recibe datos de Adobe Experience Platform. Sin embargo, sigue dependiendo de los derechos de Marketo Engage y algunas funciones back-end, como la entrega por correo electrónico, para aprovisionar y configurar el sistema.

<!-- 
>>[!NOTE]
>
>Earlier documentation referred to this deployment as the *simplified architecture*. That model is now the Journey Optimizer B2B Edition Ultimate implementation. 
-->

Esta implementación es la base que desbloquea las capacidades en Journey Optimizer B2B Edition:

* **Unifique y escale fácilmente sus datos:** La plataforma admite modelos de datos complejos, incluidos objetos personalizados, grupos de compra y eventos de cuenta.

* **Conectar varias instancias de Adobe Marketo Engage:** Administrar y unificar datos de varios entornos de Marketo Engage en un solo lugar.

* **Mantenga sus datos seguros:** Funciones avanzadas de privacidad y seguridad que ayudan a proteger la información de sus clientes. (_Próximamente_)

* **Compilado para el futuro:** Esta configuración admite mejoras e innovaciones continuas.

Siga estas directrices para la configuración.

Utilice esta lista de comprobación para completar la configuración de Journey Optimizer B2B Edition.

## &#x200B;1. Generar espacios de nombres y esquemas B2B

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuración del entorno:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Descargue la utilidad de generación automática de esquemas y áreas de nombres de GitHub.</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Recopile las credenciales de la API de Experience Platform y los encabezados necesarios.</td>
<td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-guide?lang=es">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Aplique valores de entorno al entorno de Postman.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">Más información</a></td>
</tr>
<tr>
<td colspan="2"><strong>Ejecute los scripts:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Ejecute la utilidad de generación de <em>Espacios de nombres y esquemas</em> en Postman y confirme que se han creado los espacios de nombres y los esquemas.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">Más información</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. Configuración de campos y eventos XDM

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Clases XDM estándar</strong>: configure clases de perfil XDM individual y de cuenta empresarial XDM.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Seleccione los campos administrados que desee exponer para recorridos, grupos de compra y personalización de correo electrónico.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Editar campos actualizables para esquemas.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">Más información</a></td>
</tr>
<tr>
<td colspan="2"><strong>Esquemas relacionales</strong>: seleccione una clase XDM relacional (objeto personalizado varios a uno de la cuenta).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Asegúrese de que los esquemas tengan los valores de configuración necesarios.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">Más información</a></td>
</tr>
<tr>
<td colspan="2"><strong>Eventos</strong>: configure los tipos y campos de eventos de Experience Platform.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configure cada tipo de evento de Experience Platform con campos que se admitirán en las rutas de división/toma de decisiones de recorrido.</td>
<td><a href="./admin/configure-aep-events.md">Más información</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. Configuración del seguimiento y la entrega por correo electrónico

Para enviar correos electrónicos desde [!DNL Journey Optimizer B2B Edition], configure el seguimiento y la capacidad de entrega de los correos electrónicos en la instancia de producción [!DNL Marketo Engage] adjunta y en la aplicación [!DNL Journey Optimizer B2B Edition].

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuración inicial</strong> para la instancia de Marketo Engage adjunta</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configuración del nuevo CNAME para el seguimiento de vínculos en registros DNS</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar dominios de promoción de la marca para la instancia de Marketo Engage adjunta</td>
<td><a href="./start/branding-domains.md">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configuración de DKIM y SPF en la instancia de Marketo Engage adjunta</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar DMARC</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar registros MX para el dominio</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Adición de direcciones IP salientes a listas de permitidos</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">Más información</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configuración de correo electrónico</strong> para la instancia de Marketo Engage adjunta</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar <em>Desde el correo electrónico</em> y <em>Desde la etiqueta</em> (opcional)</td>
<td><a href="./start/email-setup.md#from-email-and-label">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar <em>Cancelar la suscripción a HTML</em> y <em>Cancelar la suscripción a Text</em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar <em>Ver como HTML de página web</em> y <em>Ver como texto de página web</em></td>
<td><a href="./start/email-setup.md#view-as-web-page">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar <em>límites personalizados de recuperación de objetos</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar <em>Opciones de encabezado personalizadas</em></td>
<td><a href="./start/email-setup.md#custom-header-options">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar el filtrado de <em>Actividad de bots</em></td>
<td><a href="./start/email-setup.md#filter-email-bots">Más información</a></td>
</tr>
<tr>
<td colspan="2"><strong>Configuración del canal de correo electrónico</strong> para Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configurar <em>límites de comunicación</em> en Journey Optimizer B2B edition</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">Más información</a></td>
</tr>
</tbody>
</table>

<!--
 TBD for later

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. Configuración de canales de contenido adicionales

Para permitir que los especialistas en marketing incluyan otros canales en sus recorridos, configure canales adicionales.

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">Configuración del canal <strong>SMS</strong> para Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configure todas las cuentas de SMS que desee admitir.</td>
<td><a href="./admin/configure-channels-sms.md">Más información</a></td>
</tr>
<tr>
<td colspan="2">Configuración del canal <strong>Páginas de aterrizaje</strong> (Beta) para Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Complete la configuración de la página de aterrizaje para ofrecer asistencia a los especialistas en marketing que crean y publican estas páginas</td>
<td><a href="./admin/landing-page-settings.md">Más información</a></td>
</tr>
<tr>
<td colspan="2">Configuración del canal <strong>Web</strong> (Beta) para Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configure el sitio web de su empresa para que admita Adobe Experience Platform Web SDK.</td>
<td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Añada propiedades web mediante una dirección URL donde se envíe el contenido.</td>
<td><a href="./admin/configure-channels-web.md">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Indique a los autores de experiencias web que instalen la extensión del explorador Ayuda de edición visual de Adobe Experience Cloud.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">Más información</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Conectar la instancia de Marketo Engage para admitir acciones de recorrido (opcional)

Si planea complementar las funcionalidades de Journey Optimizer B2B edition con campañas y programas en Marketo Engage, configure la compatibilidad con acciones de Marketo Engage. Estas acciones permiten a sus equipos de marketing coordinar sus esfuerzos de marketing _basados en cuentas_ en Journey Optimizer B2B edition y _basados en posibles clientes_ en Marketo Engage.

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Para que cada instancia de Marketo Engage</strong> admita acciones de recorrido</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Creación del servicio personalizado de Marketo Engage</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Añadir la integración en Journey Optimizer B2B edition</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">Más información</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. Habilitar acceso de usuario

Cuando se complete el aprovisionamiento, los entornos limitados están enlazados y las tareas de configuración iniciales están completadas, configure el acceso de Journey Optimizer B2B edition y Marketo Engage para su equipo y para los usuarios.

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Proporcionar acceso al producto y permisos</strong> para los usuarios</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Crear un perfil de producto de Marketo Engage en Adobe Admin Console (solo la nueva instancia de Marketo Engage)</td>
<td><a href="./admin/user-management.md#marketo-engage-profile">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Añadir un grupo de usuarios para el perfil</td>
<td><a href="./admin/user-management.md#add-user-group">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configuración de funciones de usuario B2B</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">Más información</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Agregar usuarios o grupos a las funciones</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">Más información</a></td>
</tr>
</tbody>
</table>
