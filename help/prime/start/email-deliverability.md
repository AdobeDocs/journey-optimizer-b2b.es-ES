---
title: Configuración de envío de correo electrónico
description: Configure la delegación de subdominios, DMARC, SPF, DKIM y grupos de IP para Journey Optimizer B2B Prime.
badgeBeta: label="Beta" type="informative" tooltip="Esta función forma parte de una versión beta limitada."
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 6227b7f64baf307e3778e73bcceabb140ab65fb8
workflow-type: tm+mt
source-wordcount: 1920
ht-degree: 1%

---

# Entregabilidad del correo electrónico

La siguiente información está destinada a los administradores que configuran la infraestructura de envío para apoyar a los especialistas en marketing y a los creadores de contenido de correo electrónico. Describe las funciones de envío y cómo configurar subdominios, autenticación y grupos de IP. Consulte los siguientes temas para obtener información adicional sobre los canales de correo electrónico:

* Configurando canales de correo electrónico: [Configuración de canal de correo electrónico](../admin/email-channel-configuration.md)
* Creando correos electrónicos - [Agregar correos electrónicos a recorrido](../marketing/email-channel.md)
* Diseñando contenido de correo electrónico: [Creación de contenido de correo electrónico](../content/email-authoring.md).

La capacidad de entrega de correo electrónico en [!DNL Journey Optimizer B2B Prime] es el conjunto de configuraciones de infraestructura y autenticación que ayudan a los mensajes de correo electrónico a llegar a la bandeja de entrada del destinatario, no a la carpeta de correo no deseado y no bloqueados por los ISP (proveedores de servicios de Internet).

Utiliza los siguientes componentes básicos, configurados por un administrador, normalmente en el siguiente orden:

1. [Delegar uno o más subdominios](#subdomain-delegation) en Adobe.
1. [Configure registros de DMARC, SPF y DKIM](#dmarc-spf-dkim) en cada subdominio.
1. [Confirme el grupo de IP](#ip-pools) que se utilizó para enviar correo electrónico para su subdominio.
1. [Cree una o más configuraciones de canal de correo electrónico](../admin/email-channel-configuration.md#create-email-channel-configuration) que enlacen un subdominio, un grupo de IP y la identidad del remitente.

![Configuración de envío de correo electrónico para Journey Optimizer B2B Prime](./assets/email-deliverability-diagram.svg){width="450" zoomable="yes"}

>[!TIP]
>
>Trate la capacidad de entrega y la configuración de canal como una actividad de administrador única. Cuando se configura, los especialistas en marketing y los autores de correo electrónico no necesitan volver a visitarla.

## Limitaciones actuales {#limitations}

* **El método de delegación personalizada** para la delegación de subdominios aún no está disponible — use Totalmente delegado o CNAME. La delegación personalizada es el objetivo de la versión de GA.
* **Los grupos de IP dedicados** no están disponibles en Beta. El grupo de IP compartido es la única opción. Las direcciones IP dedicadas se envían en GA, incluida la planificación del calentamiento de la IP y la administración de registros PTR.

## Conceptos clave {#key-concepts}

Antes de configurar el correo electrónico, revise estos conceptos que se aplican a las funciones de envío del canal de correo electrónico:

| Concepto | Qué significa en [!DNL Journey Optimizer B2B Prime] |
| ------- | ---------------------- |
| **_Subdominio_** | Una parte delegada del dominio de envío (por ejemplo, `mail.contoso.com`) que se usa para enviar correo electrónico a través de Prime. Los subdominios aíslan su reputación de marketing B2B del correo corporativo o transaccional. |
| **_grupo de IP_** | Grupo de direcciones IP asociadas a uno o varios subdominios. Prime es compatible con un grupo de IP compartido que Adobe administra en esta versión; los grupos de IP dedicados están en la hoja de ruta de GA. |
| **_Configuración de canal_** | Un conjunto reutilizable de configuraciones de envío de correo electrónico (identidad del remitente, dirección de respuesta, subdominio, grupo de IP, tipo de correo electrónico y seguimiento) que se adjuntan a las acciones de correo electrónico en recorrido. Puede tener varias configuraciones de canal con nombre para diferentes marcas, unidades de negocio o tipos de envío. |

<!--

## Roles and permissions {#roles-permissions}

[!DNL Journey Optimizer B2B Prime] uses role-based access control (RBAC) for email features. Permissions are managed in the Adobe Admin Console (IMS) and synced at login. Product administrators assign granular permissions to product profiles, and then attach those product profiles to users.

Access to email functionality in [!DNL Journey Optimizer B2B Prime] is gated by two layers:

1. **Feature flag (LD).** A LaunchDarkly flag controls whether the entire feature is turned on for your organization. Email authoring and deliverability are gated by `dx_ajo_btob_channel_foundation`. Without this flag, the feature is hidden regardless of permissions.
2. **Functional permission.** A user-level permission that controls whether a specific user can read or write within a feature.

Most email features follow a `view-*` (read) and `manage-*` (write) pattern. A user needs the read permission to see a feature in the navigation, and the write permission to create, edit, or delete within it.

### Email authoring permissions {#email-authoring-permissions}

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View emails** | `view-b2b-emails` | View the email list, open emails, view content (read-only). |
| **Create / edit / delete emails** | `manage-b2b-emails` | All read access plus create, edit, duplicate, and delete emails. Required to author email content within a journey. |
| **View templates** | `view-b2b-templates` | Browse and preview templates in the Templates gallery (read-only). |
| **Create / edit / delete templates** | `manage-b2b-templates` | All read access plus create, edit, and delete saved templates. |
| **View fragments** | `view-b2b-fragments` | Browse and preview visual fragments (read-only). |
| **Create / edit fragments** | `manage-b2b-fragments` | All read access plus create and edit visual fragments. |
| **Publish fragments** | `publish-b2b-fragments` | Publish a fragment so it becomes available to email authors across the organization. |
| **Manage shared assets and library items** | `manage-b2b-library-items` | Manage the underlying shared library used by templates, fragments, and emails. Often granted alongside the template/fragment manage permissions. |
| **Manage usage labels** | `manage-b2b-delete-usage-labels` | Manage data usage labels (DULE) attached to library items for governance. |
| **Manage packages** | `manage-b2b-packages` | Bundle and move templates, fragments, and emails between sandboxes. |
| **View assets (Marketo Design Studio assets in Prime)** | `view-b2b-assets` | Browse the asset picker and preview images. Read-only. |
| **Manage assets** | `manage-b2b-assets` | All read access plus future asset-management actions (Beta scope). |
| **Export message data** | `manage-b2b-message-export` | Export email-level message data and reports. |

Within a person journey, the **Send email** action requires `manage-b2b-person-journeys` (to add the action and activate the journey). A user with only email permissions can author content but cannot add an email to a journey.

### Email deliverability permissions {#email-deliverability-permissions}

Deliverability features (subdomains, DMARC, IP pools, suppression lists, allowed lists, IP warmup plans, and seed lists) are administrator-level configuration. They are governed by two permissions covering the entire **[!UICONTROL Channels]** > **[!UICONTROL Email settings]** area:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **View email settings** | `view-b2b-email-settings` | View subdomains, PTR records, IP pools, suppression list, allowed list, IP warmup plans, and seed lists (read-only). |
| **Manage email settings** | `manage-b2b-email-settings` | All read access plus delegate subdomains, configure DMARC, manage suppression and allowed lists, manage IP warmup plans and seed lists. |

Some sub-features within Email settings are gated by additional LaunchDarkly flags — Suppression list (`enable-suppression`), Allowed list (`enable-allow-list`), Seed lists (`enable-seedlist-ui`). If a sub-feature is not visible in your organization, check with your Adobe representative on flag enablement.

### Channel configuration permissions {#channel-configuration-permissions}

Channel configurations sit under **[!UICONTROL Channels]** → **[!UICONTROL General settings]**. They tie deliverability primitives (subdomain, IP pool, sender identity) to a reusable object that journey authors reference. They are governed by a single permission:

| Capability | Permission | What it allows |
| ---------- | ---------- | -------------- |
| **Manage channel configurations** | `manage-b2b-channels-configurations` | View, create, edit, and delete email channel configurations. |

-->

## Delegación de subdominios {#subdomain-delegation}

La delegación de subdominios indica a Internet que Adobe está autorizado a enviar correos electrónicos en nombre de un subdominio específico (por ejemplo, `mail.contoso.com`) de su dominio. La delegación de un subdominio dedicado, en lugar del dominio raíz, protege el correo electrónico corporativo y ofrece las siguientes ventajas:

* **Aislamiento de la reputación.** Los envíos de marketing se mantienen separados del correo corporativo. Si la reputación de marketing disminuye, el correo transaccional y corporativo no se ven afectados.
* **Calentamiento más rápido de la IP.** Los subdominios dedicados ayudan a establecer una reputación positiva del remitente más rápidamente con los ISP.
* **Autenticación moderna.** SPF, DKIM y DMARC se pueden configurar sin problemas por subdominio sin afectar a otros flujos de correo.
* **Cumplimiento.** Ayuda a satisfacer los requisitos de remitente masivo de Gmail, Yahoo y otros ISP importantes.

>[!NOTE]
>
>Cada subdominio de Prime solo lo puede utilizar un producto de Adobe. No puede compartir el mismo subdominio de envío entre Prime y otro producto como Adobe Marketo Engage o Adobe Campaign; debe utilizar subdominios distintos.

### Métodos admitidos {#supported-methods}

Prime admite dos de los tres métodos de delegación de subdominios de esta versión de Beta. El tercer método (delegación personalizada) está en la hoja de ruta.

| Método | Cuándo usar | Qué implica |
| ------ | ----------- | ---------------- |
| **Totalmente Delegado** | Recomendado | Delegue la autoridad DNS completa para el subdominio a Adobe. Adobe crea y mantiene registros MX, SPF, DKIM, DMARC, A y CNAME. Menor sobrecarga operativa. Adobe administra los cambios de DNS por usted. |
| **CNAME** | Para directivas restringidas | Mantenga la autoridad de DNS de su lado y cree registros CNAME que apunten a registros administrados por Adobe. Utilícelo cuando la política DNS de su organización no permita la delegación completa. Usted es responsable de mantener los registros DNS. |
| **Delegación personalizada** | Hoja de ruta (GA) | Mantener la propiedad total de los certificados DNS y SSL. Proporciona el máximo control, incluida la capacidad de usar sus propios certificados. Este está dirigido a la versión de GA. |

### Delegación de un subdominio (método completamente delegado) {#delegate-fully-delegated}

>[!PREREQUISITES]
>
>* Decida una convención de nomenclatura de subdominios (por ejemplo, `mail.contoso.com` para marketing, `alerts.contoso.com` para transaccional).
>* Confirme con su equipo de TI/DNS que puede delegar el subdominio (registros NS) a Adobe.
>* Cree el nuevo subdominio en el proveedor DNS y espere de 24 a 48 horas para la propagación de DNS antes de delegar a Adobe.
>* Confirme que tiene la función Administrador en Prime.

1. En la navegación izquierda de [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Canales]**.
1. En el panel, expanda **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Subdominios]**.
1. Haga clic en **[!UICONTROL Configurar subdominio]**.
1. Escriba el nombre completo del subdominio (por ejemplo, `mail.contoso.com`).
1. Elija **[!UICONTROL Totalmente delegado]** como método de delegación.
1. Configure DMARC para el subdominio (consulte [DMARC, SPF y DKIM](#dmarc-spf-dkim)).

   Como mínimo, configure un registro de DMARC con una directiva de inicio de `none` para que pueda supervisar los informes sin que ello afecte a la entrega.

1. Revise la lista de registros DNS que debe administrar Adobe.

   Estos suelen incluir registros MX, SPF, DKIM, DMARC, A y CNAME (para el seguimiento y las direcciones URL de páginas espejo).

1. Descargue los registros DNS como archivo CSV con el botón **[!UICONTROL Descargar registros]**. Comparta este archivo con su equipo DNS.

1. Su equipo DNS agrega los registros NS en la solución de alojamiento de dominios que delegan el subdominio a Adobe.

1. Una vez que el equipo DNS confirme que los registros están en su lugar, vuelva a [!DNL Journey Optimizer B2B Prime] y marque la casilla que confirma que ha creado los registros necesarios en el sitio de alojamiento.

1. Haga clic en **[!UICONTROL Enviar]** para iniciar una serie de comprobaciones de validación (prevalidación, MX, SPF, DKIM, DMARC, registro FBL).

1. Espere a que el estado del subdominio cambie a **[!UICONTROL Correcto]**.

   Esto suele tardar unos minutos una vez que se completa la propagación del DNS.

>[!NOTE]
>
>Si la validación falla, el estado cambia a **[!UICONTROL Failed]** y [!DNL Journey Optimizer B2B Prime] muestra el motivo (por ejemplo, registro NS no encontrado, registro MX ausente o DMARC mal configurado). Corrija el problema de DNS subyacente y vuelva a intentar el envío.

### Delegación de un subdominio (método CNAME) {#delegate-cname}

Utilice este método únicamente si la directiva DNS de su organización prohíbe la delegación completa. Con CNAME, mantiene los registros DNS de su lado.

1. En la navegación izquierda de [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Canales]**.
1. En el panel, expanda **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Subdominios]**.
1. Haga clic en **[!UICONTROL Configurar subdominio]**.
1. Introduzca el nombre completo del subdominio.
1. Elija **[!UICONTROL CNAME]** como método de delegación.
1. Configure DMARC para el subdominio ([DMARC, SPF y DKIM](#dmarc-spf-dkim)).
1. Revise la lista de registros CNAME que se van a generar. Estos dirigen los componentes del subdominio a registros administrados por Adobe.
1. Descargue los registros como CSV y compártalos con su equipo DNS.
1. Su equipo DNS agrega cada registro CNAME a su solución de alojamiento DNS.
1. Cuando los registros estén colocados y propagados, vuelva a [!DNL Adobe Journey Optimizer B2B Prime] y confirme.
1. Haga clic en **[!UICONTROL Enviar]**.
1. Espere a que el estado alcance **[!UICONTROL Éxito]**.

>[!IMPORTANT]
>
>Con CNAME, Adobe no puede ayudarle a cambiar, mantener o solucionar problemas de DNS para el subdominio. Cualquier cambio futuro, como agregar un nuevo CNAME para una actualización de características, debe realizarlo su equipo DNS.

### Protecciones de subdominio {#subdomain-guardrails}

* **Límite predeterminado:** 10 subdominios por organización. Póngase en contacto con su representante de Adobe si necesita más (hasta 100 en función del contrato).
* **Propagación de DNS:** Espere entre 24 y 48 horas para que los cambios se propaguen globalmente. La validación puede fallar simplemente porque DNS aún no se ha propagado.
* **Reutilización de subdominios:** Un subdominio que ya está siendo utilizado por otro producto de Adobe (Marketo Engage, Adobe Campaign) no se puede reutilizar en Prime.

## DMARC, SPF y DKIM {#dmarc-spf-dkim}

DMARC, SPF y DKIM son estándares de autenticación de correo electrónico. Juntos, demuestran a los servidores de correo de recepción que su mensaje se envía genuinamente en nombre de su dominio y no se ha falsificado. Los ISP modernos (Gmail, Yahoo, Microsoft) requieren estos estándares para los remitentes masivos.

| Registro | Significa | Finalidad |
| ------ | ---------- | ------- |
| **SPF** | Marco de política de remitentes | Muestra las direcciones IP del servidor de correo permitidas para enviar correo desde el dominio. Los servidores de recepción rechazan el correo de las direcciones IP que no están en esta lista. Adobe crea y mantiene el registro SPF automáticamente al delegar un subdominio (completamente delegado). |
| **DKIM** | DomainKeys Identified Mail | Una firma criptográfica agregada a cada correo electrónico saliente. El servidor receptor comprueba la firma con una clave pública publicada en DNS. Adobe genera automáticamente claves DKIM y registros DNS durante la delegación de subdominios. |
| **DMARC** | Autenticación de mensajes, creación de informes y conformidad basados en dominio | Indica a los servidores receptores qué hacer si SPF o DKIM falla y le proporciona informes sobre los resultados de autenticación. DMARC tiene tres modos de directiva: Ninguno, Cuarentena y Rechazar. |

### Modos de directiva de DMARC {#dmarc-policy-modes}

| Política | Acción | Cuándo usar |
| ------ | ------ | ----------- |
| `none` | Monitorizar | El servidor receptor no hace nada si falla DMARC, pero aun así envía un informe. Utilícelo cuando delegue por primera vez un subdominio para confirmar que la autenticación funciona sin riesgo de pérdida de mensajes. |
| `quarantine` | Cuarentena | El servidor de recepción coloca los mensajes erróneos en la carpeta de correo no deseado. |
| `reject` | Rechazar | El servidor de recepción rechaza (rechaza) los mensajes que no superan la autenticación. Modo más estricto. Se recomienda una vez que esté seguro de la configuración de autenticación. |

### Configuración de DMARC {#configure-dmarc}

DMARC se configura en el momento de la delegación de subdominios, pero también puede agregar o actualizar DMARC para un subdominio ya delegado.

1. En la navegación izquierda de [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Canales]**.

1. En el panel, expanda **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Subdominios]**.

1. En la lista Subdominios, busque el subdominio y marque la columna Registro de DMARC.

   Si falta un registro, se muestra una alerta.

1. Abra el subdominio y desplácese hasta la sección de registros de DMARC.

   * Si ya existe un registro de DMARC en el dominio principal, [!DNL Journey Optimizer B2B Prime] recupera los valores automáticamente. Puede conservarlos o anularlos.
   * Si no existe ningún registro, elige **[!UICONTROL Administrar con Adobe]** y Adobe crea y aloja el registro de DMARC.

1. Establezca la directiva: `none`, `quarantine` o `reject`. Comience por `none` a menos que ya tenga una postura de DMARC madura en su dominio principal.

1. (Opcional) Configure etiquetas de DMARC adicionales (`sp` para la directiva de subdominio, `pct` para el porcentaje, `rua` y `ruf` para las direcciones de informe).

1. Si usa Totalmente delegado, haga clic en **[!UICONTROL Guardar]**.

   Adobe aplica el registro automáticamente. Si utiliza CNAME, copie el registro DNS, haga que su equipo DNS lo agregue y, a continuación, confirme en [!DNL Journey Optimizer B2B Prime].

1. Permita hasta 48 horas para la propagación de DNS y, a continuación, compruebe que el indicador de estado de DMARC de la página del subdominio esté en verde/en buen estado.

>[!TIP]
>
>Empiece por `policy=none` para supervisar los informes de autenticación, después avance a `quarantine` y, finalmente, a `reject` una vez que los informes muestren una alineación correcta de SPF y DKIM. Si se mueve directamente a `reject` sin supervisión, se puede rechazar el correo legítimo.

## Grupos de IP {#ip-pools}

Un grupo de IP es un grupo con nombre de direcciones IP que se utiliza para enviar el correo electrónico. Los grupos de IP son esenciales para la reputación del remitente: cada grupo tiene su propia reputación con los ISP, por lo que un problema con un grupo (por ejemplo, una ráfaga de marketing que déclencheur quejas de spam) no contamina a otro (por ejemplo, confirmaciones transaccionales).

### Tipos de grupo {#pool-types}

| Tipo de grupo | Disponibilidad | Descripción |
| --------- | ------------ | ----------- |
| **Grupo de IP compartidas** | Disponible en Beta | Grupo de direcciones IP administrado por Adobe y compartido entre muchos clientes. Adobe mantiene la reputación en todo el grupo. Es ideal para los clientes que no desean administrar el calentamiento de la IP y para los que tienen un volumen de correo electrónico entre bajo y medio. |
| **Grupo de IP dedicado** | Hoja de ruta (GA) | Una o más direcciones IP asignadas exclusivamente a su organización. Eres dueño de la reputación. Recomendado para remitentes de gran volumen. Incluye planificación del calentamiento de IP y administración de registros PTR. |

### Revisar y asignar un grupo de IP {#review-ip-pool}

En esta versión, los grupos de IP están aprovisionados previamente para su organización. Puede asignar un grupo de IP al crear una configuración de canal de correo electrónico.

1. En la navegación izquierda de [!DNL Adobe Journey Optimizer B2B Prime], expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Canales]**.
1. En el panel, expanda **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Grupos de IP]**.
1. Confirme que hay un grupo de IP con el estado **[!UICONTROL Activo]** disponible para su organización.
1. Pase el ratón sobre el grupo para ver las direcciones IP y sus registros PTR (DNS inverso).
1. Si su organización tiene varias unidades de negocio o marcas, planifique cómo utilizará los grupos de IP (por ejemplo, grupo de marketing o grupo de seminarios web) antes de crear configuraciones de canal.

>[!IMPORTANT]
>
>No mezcle tráfico transaccional y de marketing en el mismo grupo de IP, incluso cuando el grupo compartido esté disponible. La configuración Tipo de correo electrónico del canal (marketing frente a transaccional) rige el comportamiento de supresión, pero las configuraciones de canal deben seguir utilizando grupos distintos siempre que sea posible.

<!--

### Frequently asked questions {#faq}

| Question | Answer |
| -------- | ------ |
| **Can I reuse the subdomain I already use in Marketo Engage?** | No. A subdomain can only be associated with one Adobe product at a time. Create a new subdomain (for example, mail2.contoso.com) for Prime. |
| **Why does my channel configuration show Failed?** | The most common reasons are: MX record validation failed (your subdomain DNS isn't fully configured); DMARC misalignment; or an IP pool that is in Processing and has never been associated with the selected subdomain. Open the configuration to see the specific reason. |
| **What happens if a personalization token has no value at send time?** | If you defined a fallback with the Handlebars `default` helper, the fallback is used. If not, the token resolves to an empty string. Prime warns you when a token has no fallback and the underlying attribute is not guaranteed by the audience definition. |
| **Can I personalize using account-level attributes?** | Not in this release. Personalization in Prime today supports profile attributes only. |
| **What's the maximum email size?** | 100 KB is the recommended best-practice cap for inbox rendering. Prime warns you in the editor if you exceed it. |
| **Can I migrate existing Marketo email templates into Prime?** | A guided self-serve migration tool — including Velocity-to-Handlebars conversion — is delivered at GA. In this release, you can manually rebuild templates or paste raw HTML. |
| **Will my updates to Marketo assets show up in Prime?** | No. Asset availability in Prime is based on a one-time copy from Marketo Design Studio. Re-uploaded or modified Marketo assets are not reflected in Prime today. Native asset upload and management within Prime is on the Beta roadmap. |

## Glossary {#glossary}

| Term | Definition |
| ---- | ---------- |
| **DKIM** | DomainKeys Identified Mail — cryptographic email signature. |
| **DMARC** | Domain-based Message Authentication, Reporting & Conformance. |
| **FBL** | Feedback Loop — a service ISPs offer to receive spam-complaint reports back to senders. |
| **Handlebars** | JavaScript templating language used in Prime for personalization expressions. |
| **IP pool** | Group of IP addresses used to send email. |
| **MX record** | Mail Exchange DNS record — directs incoming mail to the correct mail servers. |
| **NS record** | Name Server DNS record — used to delegate a subdomain. |
| **PTR record** | Pointer record — reverse DNS that maps an IP address back to a hostname. |
| **RBAC** | Role-Based Access Control. |
| **SPF** | Sender Policy Framework — DNS record listing authorized sending IPs. |
| **Subdomain delegation** | Granting Adobe authority over a portion of your domain (a subdomain) for sending email. |

-->

