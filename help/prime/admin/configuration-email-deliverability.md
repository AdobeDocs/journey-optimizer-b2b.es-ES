---
title: Entrega de correo electrónico y configuración de canal
description: Configure las configuraciones delegación de subdominios, DMARC, SPF, DKIM, grupos de IP y canal de correo electrónico para Journey Optimizer B2B Prime.
autotag-review: '2026-06-12T22:43:42.799Z'
TQID: 'https://experienceleague.adobe.com/RKZSQkjSRvHixOm2faRT5D-yB00IykXfPO06vvIUQ6k'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f01b5556-e951-40ba-8625-2e3001864f2bid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 0a877cc1fc0dfd9c3d8271c8f7be6a5e34a69a9a
workflow-type: tm+mt
source-wordcount: 3095
ht-degree: 1%

---

# Entrega de correo electrónico y configuración de canal

La siguiente información está destinada a los administradores que configuran la infraestructura de envío para admitir especialistas en marketing y autores de correo electrónico. Describe las funciones, las funciones y los permisos de la capacidad de entrega, y cómo configurar subdominios, autenticación, grupos de IP y configuraciones de canal.

Para obtener información detallada sobre la creación de correos electrónicos y contenido de correo electrónico en el espacio de diseño de correo electrónico, consulte [Creación de correos electrónicos](../content/email-authoring.md).

## Conceptos clave {#key-concepts}

Antes de configurar el correo electrónico, revise estos conceptos que se aplican a las funciones de envío del canal de correo electrónico:

| Concepto | Qué significa en [!DNL Journey Optimizer B2B Edition] Prime |
| ------- | ---------------------- |
| **_Configuración de canal_** | Un conjunto reutilizable de configuraciones de envío de correo electrónico, incluida la identidad del remitente, la dirección de respuesta, el subdominio, el grupo de IP, el tipo de correo electrónico (de marketing o transaccional) y el seguimiento, que se adjunta a las acciones de correo electrónico en recorrido. Puede tener varias configuraciones de canal con nombre para diferentes marcas, unidades de negocio o tipos de envío. |
| **_Subdominio_** | Una parte delegada del dominio de envío (por ejemplo, `mail.contoso.com`) que se usa para enviar correo electrónico a través de Prime. Los subdominios aíslan su reputación de marketing B2B del correo corporativo o transaccional. |
| **_grupo de IP_** | Grupo de direcciones IP asociadas a uno o varios subdominios. Prime es compatible con un grupo de IP compartido que Adobe administra en esta versión; los grupos de IP dedicados están en la hoja de ruta de GA. |

## Funciones y permisos {#roles-permissions}

[!DNL Journey Optimizer B2B Edition] Prime usa el control de acceso basado en roles (RBAC) para las funciones de correo electrónico. Los permisos se administran en Adobe Admin Console (IMS) y se sincronizan al iniciar sesión. Los administradores de productos asignan permisos granulares a los perfiles de producto y, a continuación, adjuntan esos perfiles de producto a los usuarios.

El acceso a la funcionalidad de correo electrónico en [!DNL Journey Optimizer B2B Edition] Prime se rige por dos niveles:

1. **Indicador de característica (LD).** Un indicador LaunchDarkly controla si toda la función está activada para su organización. La creación y la entrega de correo electrónico están controladas por `dx_ajo_btob_channel_foundation`. Sin este indicador, la función se oculta independientemente de los permisos.
2. **Permiso funcional.** Permiso de nivel de usuario que controla si un usuario específico puede leer o escribir dentro de una función.

La mayoría de las funciones de correo electrónico siguen un patrón `view-*` (lectura) y `manage-*` (escritura). Un usuario necesita el permiso de lectura para ver una función en la navegación y el permiso de escritura para crear, editar o eliminar dentro de ella.

### Permisos de creación de correo electrónico {#email-authoring-permissions}

| Capacidad | Permiso | Lo que permite |
| ---------- | ---------- | -------------- |
| **Ver correos electrónicos** | `view-b2b-emails` | Ver la lista de correos electrónicos, abrir correos electrónicos y ver contenido (solo lectura). |
| **Crear/editar/eliminar correos electrónicos** | `manage-b2b-emails` | Todos los accesos de lectura además de crear, editar, duplicar y eliminar correos electrónicos. Necesario para crear contenido de correo electrónico en un recorrido. |
| **Ver plantillas** | `view-b2b-templates` | Examine y previsualice las plantillas en la galería Plantillas (solo lectura). |
| **Crear/editar/eliminar plantillas** | `manage-b2b-templates` | Todos los accesos de lectura, además de crear, editar y eliminar plantillas guardadas. |
| **Ver fragmentos** | `view-b2b-fragments` | Examine y previsualice fragmentos visuales (solo lectura). |
| **Crear/editar fragmentos** | `manage-b2b-fragments` | Todo el acceso de lectura, además de crear y editar fragmentos visuales. |
| **Publicar fragmentos** | `publish-b2b-fragments` | Publique un fragmento para que esté disponible para los autores de correo electrónico de toda la organización. |
| **Administrar recursos compartidos y elementos de biblioteca** | `manage-b2b-library-items` | Administre la biblioteca compartida subyacente que utilizan las plantillas, los fragmentos y los correos electrónicos. A menudo se concede junto con los permisos de administración de plantillas/fragmentos. |
| **Administrar etiquetas de uso** | `manage-b2b-delete-usage-labels` | Administre las etiquetas de uso de datos (DULE) adjuntas a los elementos de la biblioteca para el control. |
| **Administrar paquetes** | `manage-b2b-packages` | Agrupe y mueva plantillas, fragmentos y correos electrónicos entre zonas protegidas. |
| **Ver recursos (recursos de Marketo Design Studio en Prime)** | `view-b2b-assets` | Examine el selector de recursos y previsualice las imágenes. Sólo lectura. |
| **Administración de recursos** | `manage-b2b-assets` | Todo el acceso de lectura más las futuras acciones de administración de recursos (ámbito de Beta). |
| **Exportar datos de mensajes** | `manage-b2b-message-export` | Exportar datos e informes de mensajes de correo electrónico. |

Dentro del recorrido de una persona, la acción **Enviar correo electrónico** requiere `manage-b2b-person-journeys` (para agregar la acción y activar el recorrido). Un usuario con solo permisos de correo electrónico puede crear contenido, pero no puede agregar un correo electrónico a un recorrido.

### Permisos de envío de correo electrónico {#email-deliverability-permissions}

Las funciones de entrega (subdominios, DMARC, grupos de IP, listas de supresión, listas de permitidos, planes de calentamiento de IP y listas de semilla) son configuraciones de administrador. Se rigen por dos permisos que abarcan todo el área de **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]**:

| Capacidad | Permiso | Lo que permite |
| ---------- | ---------- | -------------- |
| **Ver configuración de correo electrónico** | `view-b2b-email-settings` | Ver subdominios, registros PTR, grupos de IP, lista de supresión, lista de permitidos, planes de calentamiento de IP y listas semilla (solo lectura). |
| **Administrar configuración de correo electrónico** | `manage-b2b-email-settings` | Todos los subdominios de acceso de lectura y delegados, configuración de DMARC, administración de listas de permitidos y supresión, administración de planes de calentamiento de IP y listas de inicio. |

Algunas subcaracterísticas de la configuración de correo electrónico están cerradas por marcas LaunchDarkly adicionales: lista de supresión (`enable-suppression`), Lista de permitidos (`enable-allow-list`), listas semilla (`enable-seedlist-ui`). Si una subfunción no es visible en su organización, póngase en contacto con su representante de Adobe para conocer la habilitación de marcas.

### Permisos de configuración de canal {#channel-configuration-permissions}

Las configuraciones de canal se encuentran en **[!UICONTROL Canales]** → **[!UICONTROL Configuración general]**. Unen las primitivas de capacidad de entrega (subdominio, grupo de IP, identidad del remitente) a un objeto reutilizable al que hacen referencia los autores de recorrido. Se rigen por un único permiso:

| Capacidad | Permiso | Lo que permite |
| ---------- | ---------- | -------------- |
| **Administrar configuraciones de canal** | `manage-b2b-channels-configurations` | Vea, cree, edite y elimine configuraciones de canal de correo electrónico. |

## Resumen de envío de correo electrónico {#deliverability-overview}

La capacidad de entrega de correo electrónico en [!DNL Journey Optimizer B2B Edition] Prime es el conjunto de configuraciones de infraestructura y autenticación que ayudan a los mensajes de correo electrónico a llegar a la bandeja de entrada del destinatario, no a la carpeta de correo no deseado, y no bloqueados por los ISP (proveedores de servicios de Internet).

Utiliza los siguientes componentes básicos, configurados por un administrador, normalmente en el siguiente orden:

1. Delegue uno o varios subdominios en Adobe.
1. Configure los registros de DMARC, SPF y DKIM en cada subdominio.
1. Confirme el grupo de IP que enviará el correo electrónico para el subdominio.
1. Cree una o más configuraciones de canal de correo electrónico que enlacen un subdominio, un grupo de IP y la identidad del remitente.
1. Utilice esas configuraciones de canal en las acciones de correo electrónico de recorrido.

>[!TIP]
>
>Considere la configuración de la capacidad de envío como una actividad de administrador única por unidad empresarial o marca. Cuando se configura, los especialistas en marketing y los autores de correo electrónico no necesitan volver a visitarla.

## Delegación de subdominios {#subdomain-delegation}

La delegación de subdominios indica a Internet que Adobe está autorizado a enviar correos electrónicos en nombre de un subdominio específico (por ejemplo, `mail.contoso.com`) de su dominio. La delegación de un subdominio dedicado, en lugar del dominio raíz, protege el correo electrónico corporativo y genera un

* **Aislamiento de la reputación.** Los envíos de marketing se mantienen separados del correo corporativo. Si la reputación de marketing disminuye, el correo transaccional y corporativo no se ven afectados.
* **Calentamiento más rápido de la IP.** Los subdominios dedicados ayudan a establecer una reputación positiva del remitente más rápidamente con los ISP.
* **Autenticación moderna.** SPF, DKIM y DMARC se pueden configurar sin problemas por subdominio sin afectar a otros flujos de correo.
* **Cumplimiento.** Ayuda a satisfacer los requisitos de remitente masivo de Gmail, Yahoo y otros ISP importantes.

>[!NOTE]
>
>Cada subdominio de Prime solo lo puede utilizar un producto de Adobe. No puede compartir el mismo subdominio de envío entre Prime y otro producto como Adobe Marketo Engage o Adobe Campaign; debe utilizar subdominios distintos.

### Métodos admitidos

Prime admite dos de los tres métodos de delegación de subdominios de Alpha. El tercer método (delegación personalizada) está en la hoja de ruta.

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

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime, vaya a **[!UICONTROL Administración]** → **[!UICONTROL Canales]** → **[!UICONTROL Configuración de correo electrónico]** → **[!UICONTROL Subdominios]**.
1. Haga clic en **[!UICONTROL Configurar subdominio]**.
1. Escriba el nombre completo del subdominio (por ejemplo, `mail.contoso.com`).
1. Elija **[!UICONTROL Totalmente delegado]** como método de delegación.
1. Configure DMARC para el subdominio (consulte [DMARC, SPF y DKIM](#dmarc-spf-dkim)).

   Como mínimo, configure un registro de DMARC con una directiva de inicio de `none` para que pueda supervisar los informes sin que ello afecte a la entrega.

1. Revise la lista de registros DNS que debe administrar Adobe.

   Estos suelen incluir registros MX, SPF, DKIM, DMARC, A y CNAME (para el seguimiento y las direcciones URL de páginas espejo).

1. Descargue los registros DNS como archivo CSV con el botón **[!UICONTROL Descargar registros]**. Comparta este archivo con su equipo DNS.

1. Su equipo DNS agrega los registros NS en la solución de alojamiento de dominios que delegan el subdominio a Adobe.

1. Una vez que el equipo DNS confirme que los registros están en su lugar, vuelva a [!DNL Journey Optimizer B2B Edition] Prime y marque la casilla que confirma que ha creado los registros necesarios en el sitio de alojamiento.

1. Haga clic en **[!UICONTROL Enviar]** para iniciar una serie de comprobaciones de validación (prevalidación, MX, SPF, DKIM, DMARC, registro FBL).

1. Espere a que el estado del subdominio cambie a **[!UICONTROL Correcto]**.

   Esto suele tardar unos minutos una vez que se completa la propagación del DNS.

>[!NOTE]
>
>Si la validación falla, el estado cambia a **[!UICONTROL Failed]** y [!DNL Journey Optimizer B2B Edition] Prime muestra el motivo (por ejemplo, registro NS no encontrado, registro MX ausente o DMARC mal configurado). Corrija el problema de DNS subyacente y vuelva a intentar el envío.

### Delegación de un subdominio (método CNAME) {#delegate-cname}

Utilice este método únicamente si la directiva DNS de su organización prohíbe la delegación completa. Con CNAME, mantiene los registros DNS de su lado.

1. En [!DNL Adobe Journey Optimizer B2B Edition] Prime, vaya a **[!UICONTROL Administración]** → **[!UICONTROL Canales]** → **[!UICONTROL Configuración de correo electrónico]** → **[!UICONTROL Subdominios]**.
1. Haga clic en **[!UICONTROL Configurar subdominio]**.
1. Introduzca el nombre completo del subdominio.
1. Elija **[!UICONTROL CNAME]** como método de delegación.
1. Configure DMARC para el subdominio ([DMARC, SPF y DKIM](#dmarc-spf-dkim)).
1. Revise la lista de registros CNAME que genera Prime. Estos registros dirigen los componentes del subdominio a registros administrados por Adobe.
1. Descargue los registros como CSV y compártalos con su equipo DNS.
1. Su equipo DNS agrega cada registro CNAME a su solución de alojamiento DNS.
1. Una vez que los registros estén colocados y propagados, vuelva a Prime y confirme. Haga clic en **[!UICONTROL Enviar]**.
1. Espere a que el estado alcance **[!UICONTROL Éxito]**.

>[!IMPORTANT]
>
>Con CNAME, Adobe no puede ayudarle a cambiar, mantener o solucionar problemas de DNS para el subdominio. Cualquier cambio futuro (por ejemplo, agregar un nuevo CNAME para una actualización de características) debe realizarlo su equipo DNS.

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

### Modos de directiva de DMARC

| Política | Acción | Cuándo usar |
| ------ | ------ | ----------- |
| `none` | Monitorizar | El servidor receptor no hace nada si falla DMARC, pero aun así envía un informe. Utilícelo cuando delegue por primera vez un subdominio para confirmar que la autenticación funciona sin riesgo de pérdida de mensajes. |
| `quarantine` | Cuarentena | El servidor de recepción coloca los mensajes erróneos en la carpeta de correo no deseado. |
| `reject` | Rechazar | El servidor de recepción rechaza (rechaza) los mensajes que no superan la autenticación. Modo más estricto. Se recomienda una vez que esté seguro de la configuración de autenticación. |

### Configuración de DMARC {#configure-dmarc}

DMARC se configura en el momento de la delegación de subdominios, pero también puede agregar o actualizar DMARC para un subdominio ya delegado.

1. Vaya a **[!UICONTROL Administración]** → **[!UICONTROL Canales]** → **[!UICONTROL Configuración de correo electrónico]** → **[!UICONTROL Subdominios]**.

1. En la lista Subdominios, busque el subdominio y marque la columna Registro de DMARC.

   Si falta un registro, se muestra una alerta.

1. Abra el subdominio y desplácese hasta la sección de registros de DMARC.

   * Si ya existe un registro de DMARC en el dominio principal, [!DNL Journey Optimizer B2B Edition] Prime recupera los valores automáticamente. Puede conservarlos o anularlos.
   * Si no existe ningún registro, elige **[!UICONTROL Administrar con Adobe]** y Adobe crea y aloja el registro de DMARC.

1. Establezca la directiva: `none`, `quarantine` o `reject`. Comience por `none` a menos que ya tenga una postura de DMARC madura en su dominio principal.

1. (Opcional) Configure etiquetas de DMARC adicionales (`sp` para la directiva de subdominio, `pct` para el porcentaje, `rua` y `ruf` para las direcciones de informe).

1. Si usa Totalmente delegado, haga clic en **[!UICONTROL Guardar]**.

   Adobe aplica el registro automáticamente. Si utiliza CNAME, copie el registro DNS y pida a su equipo DNS que lo agregue y, a continuación, confírmelo en [!DNL Journey Optimizer B2B Edition] Prime.

1. Permita hasta 48 horas para la propagación de DNS y, a continuación, compruebe que el indicador de estado de DMARC de la página del subdominio esté en verde/en buen estado.

>[!TIP]
>
>Empiece por `policy=none` para supervisar los informes de autenticación, después avance a `quarantine` y, finalmente, a `reject` una vez que los informes muestren una alineación correcta de SPF y DKIM. Si se mueve directamente a `reject` sin supervisión, se puede rechazar el correo legítimo.

## Grupos de IP {#ip-pools}

Un grupo de IP es un grupo con nombre de direcciones IP que se utiliza para enviar el correo electrónico. Los grupos de IP son esenciales para la reputación del remitente: cada grupo tiene su propia reputación con los ISP, por lo que un problema con un grupo (por ejemplo, una ráfaga de marketing que déclencheur quejas de spam) no contamina a otro (por ejemplo, confirmaciones transaccionales).

### Tipos de grupo

| Tipo de grupo | Disponibilidad | Descripción |
| --------- | ------------ | ----------- |
| **Grupo de IP compartidas** | Disponible en Alpha | Grupo de direcciones IP administrado por Adobe y compartido entre muchos clientes. Adobe mantiene la reputación en todo el grupo. Es ideal para los clientes que no desean administrar el calentamiento de la IP y para los que tienen un volumen de correo electrónico entre bajo y medio. |
| **Grupo de IP dedicado** | Hoja de ruta (GA) | Una o más direcciones IP asignadas exclusivamente a su organización. Eres dueño de la reputación. Recomendado para remitentes de gran volumen. Incluye planificación del calentamiento de IP y administración de registros PTR. |

### Revisar y asignar un grupo de IP {#review-ip-pool}

En esta versión, los grupos de IP están aprovisionados previamente para su organización. Puede asignar un grupo de IP al crear una configuración de canal de correo electrónico.

1. Vaya a **[!UICONTROL Administración]** → **[!UICONTROL Canales]** → **[!UICONTROL Configuración de correo electrónico]** → **[!UICONTROL Grupos de IP]**.
1. Confirme que hay un grupo de IP con el estado **[!UICONTROL Activo]** disponible para su organización.
1. Pase el ratón sobre el grupo para ver las direcciones IP y sus registros PTR (DNS inverso).
1. Si su organización tiene varias unidades de negocio o marcas, planifique cómo utilizará los grupos de IP (por ejemplo, grupo de marketing o grupo de seminarios web) antes de crear configuraciones de canal.

>[!IMPORTANT]
>
>No mezcle tráfico transaccional y de marketing en el mismo grupo de IP, incluso cuando el grupo compartido esté disponible. La configuración Tipo de correo electrónico del canal (marketing frente a transaccional) rige el comportamiento de supresión, pero las configuraciones de canal deben seguir utilizando grupos distintos siempre que sea posible.

## Configuraciones de canal de correo electrónico {#email-channel-configurations}

Una configuración de canal es el objeto central que vincula la identidad del remitente, el subdominio, el grupo de IP y la configuración de seguimiento. Las acciones de correo electrónico en los recorridos hacen referencia a una configuración de canal para saber cómo enviar el mensaje:

* **Canal:** Correo electrónico.
* **Tipo de correo electrónico:** Marketing o transaccional. Esta configuración determina si se aplican las reglas de supresión (Marketing las aplica; Transactional omite la supresión de quejas de spam de forma predeterminada para los mensajes transaccionales legítimos).
* **Parámetros De Encabezado:** Del Nombre, Del Correo Electrónico, Del Nombre De Respuesta, Del Correo Electrónico De Respuesta, Del Correo Electrónico De Error.
* **Subdominio:** El subdominio delegado utilizado para el envío. El correo electrónico de origen debe utilizar este subdominio.
* **Grupo de IP:** Grupo de IP usado para entregar el mensaje.
* **Seguimiento de URL:** Habilite o deshabilite el rastreo de clics y aperturas; configure el dominio de seguimiento.
* **Etiquetas:** Etiquetas para organización y búsqueda.

### Crear una configuración de canal de correo electrónico {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* Al menos un subdominio debe ser delegado y activo.
>* Debe asignarse al menos un grupo de IP a la organización.
>* Necesita la función Administrador.

1. Vaya a **[!UICONTROL Canales]** → **[!UICONTROL Configuración general]** → **[!UICONTROL Configuraciones de canal]**.
1. Haga clic en **[!UICONTROL Crear configuración de canal]**.
1. Introduzca un Nombre (por ejemplo, &quot;Contoso B2B Marketing — Norteamérica&quot;) y una Descripción opcional.
1. Seleccione el canal **[!UICONTROL Correo electrónico]**.
1. Si lo desea, seleccione etiquetas para categorizar la configuración.
1. En la sección **[!UICONTROL Tipo de correo electrónico]**, elija Marketing o Transaccional.
1. En la sección **[!UICONTROL Subdominio]**, seleccione un subdominio delegado anteriormente.
1. En la sección **[!UICONTROL grupo de IP]**, seleccione un grupo de IP activo. Puede pasar el ratón sobre las direcciones IP para ver los registros PTR.
1. Configurar los **[!UICONTROL parámetros de encabezado]**:
   * Nombre de origen (por ejemplo, &quot;Contoso Marketing&quot;).
   * Desde correo electrónico: debe utilizar el subdominio seleccionado (por ejemplo, `marketing@mail.contoso.com`).
   * Nombre de respuesta y Correo electrónico de respuesta: si está en blanco, el valor predeterminado es De.
   * Correo electrónico de error: dirección que recibe notificaciones de no entrega.
1. Habilite **[!UICONTROL Seguimiento de URL]** y seleccione el dominio de seguimiento.
1. Haga clic en **[!UICONTROL Enviar]**.
1. Prime ejecuta la validación: estado del subdominio, registro MX, alineación SPF/DKIM/DMARC, preparación del grupo de IP, registro FBL. La configuración se desplaza por Borrador → Procesamiento → Activo.

>[!NOTE]
>
>Si la validación falla, la configuración pasa al estado **[!UICONTROL Failed]**. Abra la configuración para ver el motivo del error: las causas comunes son un error de validación de registro MX, IP en el grupo que no coinciden con la configuración o desalineación de DMARC. Resolver y volver a enviar.

### Editar o eliminar una configuración de canal {#edit-channel-configuration}

Puede editar las configuraciones de canal después de la creación, pero con una restricción importante:

* **El canal no se puede cambiar.** Una configuración de está enlazada a su canal.

Cuando edita una configuración que está en uso:

* **Para recorridos publicados:** el cambio se aplica en la siguiente periodicidad o en la siguiente ejecución. Las ejecuciones en vuelo continúan con la configuración anterior.
* **Para mensajes transaccionales o en tiempo real:** cambios se propagan en unos cinco minutos.

Para eliminar una configuración, primero elimine o actualice todas las acciones de correo electrónico que hagan referencia a ella. [!DNL Journey Optimizer B2B Edition] Prime no elimina ninguna configuración que utilice actualmente un recorrido activo.

### Configuraciones de varios canales {#multiple-channel-configurations}

La mayoría de las organizaciones B2B utilizan varias configuraciones de canal para separar marcas, regiones o tipos de envío. Patrones comunes:

* Una configuración de marketing independiente por unidad de negocio (por ejemplo, *Marketing BU-A*, *Marketing BU-B*).
* Una configuración transaccional dedicada con Tipo de correo electrónico = Transaccional para las notificaciones de productos o contratos.
* Configuraciones específicas de la región que utilizan subdominios específicos de la región (por ejemplo, `mail.eu.contoso.com`, `mail.us.contoso.com`) para alinearse con los ISP regionales y el cumplimiento.

>[!TIP]
>
>Asigne un nombre a las configuraciones con una convención clara y estructurada, por ejemplo: *[Marca] - [Región] - [Tipo]*. Esto resulta esencial una vez que tenga una docena o más de configuraciones.

### Limitaciones conocidas {#known-limitations}

* **El método de delegación personalizada** para la delegación de subdominios aún no está disponible — use Totalmente delegado o CNAME. La delegación personalizada es el destino de GA.
* **Los grupos de IP dedicados** no están disponibles en Alpha. El grupo de IP compartido es la única opción. Las direcciones IP dedicadas se envían en GA, incluida la planificación del calentamiento de la IP y la administración de registros PTR.
* La importación de **HTML a través de la carga .html o .zip** está limitada en Alpha. La importación completa de HTML, que incluye el editor de código y la vista dual de lienzo visual, la validación y la conversión automática de CSS en línea, se envía en Beta.
* **La carga de imágenes nativas y DAM en Prime** (cargar, organizar, editar) está en la hoja de ruta de Beta. Utilice los recursos de Marketo Design Studio en esta versión. Las recargas en Marketo no se reflejan en Prime.
* **Los perfiles de prueba, Simular contenido y Enviar prueba** no están disponibles en esta versión. Los informes de spam basados en Litmus rendering y SpamAssassin se encuentran en la hoja de ruta de Beta.
* La personalización de nivel de cuenta y los datos de objeto personalizado **1 no están disponibles en esta versión.** Utilice atributos de perfil.
* La **migración automatizada de Velocity-to-Handlebars** de las plantillas de Marketo existentes se enviará en GA.
* Los **comentarios y la colaboración en los correos electrónicos** (comentarios en línea, @mentions, flujo de trabajo de solicitud y revisión) se envían en la versión de seguimiento rápido.
* Las integraciones de **AEM Assets, fragmentos de contenido de AEM y Adobe Express** se encuentran en la hoja de ruta de seguimiento rápido.

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
