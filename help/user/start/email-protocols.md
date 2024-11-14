---
title: Protocolos de seguimiento y envío por correo electrónico
description: Obtenga información sobre cómo configurar los protocolos en Marketo Engage para que Journey Optimizer B2B edition los use en las funciones de seguimiento y canal de correo electrónico.
feature: Setup
role: Admin
source-git-commit: a8ca8b99ddf33b4a64b42b751f7be798274d0084
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# Protocolos de seguimiento y envío por correo electrónico

Adobe Journey Optimizer B2B edition aprovecha las funciones del canal de correo electrónico y el seguimiento de eventos en Marketo Engage. Para garantizar que la entrega de correo electrónico funciona según lo esperado en las organizaciones que utilizan una configuración restrictiva del servidor de seguridad o del servidor proxy, un administrador del sistema debe añadir determinados dominios e intervalos de direcciones IP a la lista de permitidos.

>[!NOTE]
>
>Si su organización ya está utilizando la instancia de Marketo Engage conectada de para ejecutar sus operaciones de marketing, estos protocolos y configuraciones ya deben estar implementados.

Asegúrese de que los siguientes dominios (incluido el asterisco) se agregan a la lista de permitidos para habilitar todos los recursos de Marketo Engage y sockets web:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Siga estos pasos para garantizar el seguimiento y la entrega por correo electrónico:

1. [Crear registros DNS para ](#create-dns-records-for-landing-pages-and-email)
1. [Configuración de SPF y DKIM](#set-up-spf-and-dkim)
1. [Configuración de DMARC](#set-up-dmarc)
1. [Configurar registros MX para su dominio](#set-up-mx-records-for-your-domain)
1. [Adición de direcciones IP salientes a listas de permitidos](#outbound-ip-addresses)

## Crear registros DNS para <!-- landing pages and -->correo electrónico

La conexión de un registro CNAME permite a los especialistas en marketing alojar versiones web de correos electrónicos, páginas de aterrizaje y blogs con una marca coherente que mejora el tráfico y las conversiones. Se recomienda añadir los CNAME al host de dominio raíz para que el Marketo Engage aloje los recursos web centrados en marketing. Como administrador, debe trabajar con su equipo de marketing para planificar e implementar un registro CNAME para los vínculos de seguimiento que se incluyen en los correos electrónicos enviados a través de Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Añadir el CNAME para los vínculos de seguimiento de correo electrónico

Agregue el CNAME del correo electrónico de modo que `[YourEmailCNAME]` apunte a `[MktoTrackingLink]`, que es el vínculo de seguimiento predeterminado que el Marketo Engage asignó, con el formato:

`[YourEmailCNAME].[YourDomain].com` EN CNAME `[MktoTrackingLink]`

Por ejemplo:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>El valor `[MktoTrackingLink]` debe ser el dominio de marca predeterminado.

### Aprovisionar el certificado SSL

Póngase en contacto con el [Soporte técnico de Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"} para iniciar el proceso de aprovisionamiento de un certificado SSL.

Este proceso puede tardar hasta tres días hábiles en completarse.

## Configuración de SPF y DKIM

Su equipo de marketing debe proporcionar la información de DKIM (Domain Keys Identified Mail) que se agregará a su registro de recursos DNS. Siga estos pasos para configurar DKIM y SPF (Marco de política del remitente) y, a continuación, notifique al equipo de marketing cuando se actualice.

1. Para configurar SPF, agregue la línea siguiente a las entradas DNS:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Si ya tiene un registro SPF existente en la entrada DNS, simplemente agréguele lo siguiente:

   ```
   include: mktomail.com
   ```

   Reemplace `CompanyDomain` por el dominio principal del sitio web (como `company.com/`) y `CorpIP` por la dirección IP del servidor de correo electrónico corporativo (como `255.255.255.255`). Si planea enviar correos electrónicos desde varios dominios a través de Marketo Engage, agregue esta línea para cada dominio (en una línea).

1. Para DKIM, cree registros de recursos DNS para cada dominio.

   Agregue los registros host y los valores TXT de cada dominio:

   `[DKIMDomain1]`: el registro de host es `[HostRecord1]` y el valor TXT es `[TXTValue1]`.

   `[DKIMDomain2]`: el registro de host es `[HostRecord2]` y el valor TXT es `[TXTValue2]`.

   Copie `HostRecord` y `TXTValue` para cada dominio DKIM después de seguir las [instrucciones](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentación del Marketo Engage. Puede comprobar los dominios en Journey Optimizer B2B edition (consulte [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Configuración de DMARC

DMARC (Autenticación de mensajes, creación de informes y conformidad basados en dominio) es un protocolo de autenticación que se utiliza para ayudar a las organizaciones a proteger su dominio contra el uso no autorizado. Amplía los protocolos de autenticación existentes, como SPF y DKIM, para informar a los servidores de destinatarios sobre las acciones que deben realizarse si se produce un error de autenticación en su dominio. DMARC es opcional, pero se recomienda porque le ayuda a proteger su marca y su reputación. Los principales proveedores, como Google y Yahoo, empezaron a exigir el uso de DMARC para remitentes masivos a partir de febrero de 2024.

Para que DMARC funcione, debe tener al menos uno de los siguientes registros TXT DNS:

* Un SPF válido
* Un registro DKIM válido para su dominio FROM: (recomendado para Marketo Engage y Journey Optimizer B2B edition)

También debe tener un registro TXT DNS específico de DMARC para el dominio `FROM:`. De forma opcional, puede definir una dirección de correo electrónico que especifique adónde deben ir los informes de DMARC dentro de su organización para la monitorización de informes.

### Ejemplo de flujo de trabajo de DMARC

>[!TIP]
>
>Se recomienda implementar DMARC como un _despliegue lento_. Escale la directiva de DMARC de `p=none` a `p=quarantine` y luego a `p=reject` a medida que vaya entendiendo el impacto potencial y establezca la directiva de DMARC para una alineación más flexible en SPF y DKIM.

Si recibe informes de DMARC, debe hacer lo siguiente:

1. Use `p=none` y analice los comentarios y los informes que reciba. Los informes indican al destinatario que no realice ninguna acción contra los mensajes que no superan la autenticación y que envíe informes de correo electrónico al remitente.

   * Si los mensajes legítimos fallan en la autenticación, revise y corrija los problemas con SPF/DKIM.

   * Determine si SPF o DKIM están alineados y pasa la autenticación para todos los correos electrónicos legítimos.

   * Revise los informes para asegurarse de que los resultados son los esperados en función de las políticas de SPF/DKIM.

1. Ajuste la directiva a `p=quarantine`, que indica al servidor de correo electrónico receptor que ponga en cuarentena los correos electrónicos que no se autentiquen correctamente (normalmente, colocando esos mensajes en la carpeta de correo no deseado).

   Revise los informes para asegurarse de que los resultados son los esperados.

1. Si está satisfecho con el comportamiento de los mensajes en el nivel `p=quarantine`, puede ajustar la directiva a (`p=reject`).

   La directiva de rechazo indica al destinatario que deniegue (devuelva) cualquier correo electrónico del dominio que falle en la autenticación. Con esta directiva habilitada, solo los correos electrónicos verificados como 100 % autenticados por el dominio pueden colocarse en la bandeja de entrada.

   >[!CAUTION]
   >
   >Utilice esta directiva con precaución y determine si es apropiada para su organización.

### Informes de DMARC

DMARC ofrece la capacidad de recibir informes sobre correos electrónicos que fallan en SPF/DKIM. Existen dos informes diferentes generados por los proveedores de servicios de Internet como parte del proceso de autenticación. Los remitentes pueden recibir estos informes a través de las etiquetas RUA/RUF de su política de DMARC.

* **Informes agregados (RUA)**: No contiene ninguna PII (información de identificación personal) que pueda ser confidencial según el RGPD (Reglamento general de protección de datos).

* **Informes forenses (RUF)** - Contienen direcciones de correo electrónico que son sensibles al RGPD. Antes de implementar este informe, compruebe la política de su organización para gestionar la información que debe cumplir con el RGPD.

El uso principal de estos informes es recibir una descripción general de los correos electrónicos que se intentan suplantar. Son informes muy técnicos y se digieren mejor mediante una herramienta de terceros.

### Ejemplo de registros de DMARC

* Registro mínimo vacío: `v=DMARC1; p=none`

* Registro que dirige a una dirección de correo electrónico para recibir informes: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Etiquetas DMARC

Los registros de DMARC tienen varios componentes llamados _DMARC tags_. Cada etiqueta tiene un valor que especifica un aspecto determinado de DMARC.

| Nombre de la etiqueta | Utilice  | Función | Ejemplo | Valor predeterminado |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Requerido | Especifica la versión. Solo hay una versión, por lo que tiene un valor fijo de `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Requerido | Especifica la directiva de DMARC, que indica al destinatario que informe, ponga en cuarentena o rechace los mensajes de correo electrónico que no superen las comprobaciones de autenticación. | `p=none`, `p=quarantine` o `p=reject` | - |
| `fo` | Opcional | Permite al propietario del dominio especificar las opciones de creación de informes. | `0`: Generar informe si SPF y DKIM fallan <br> `1` - Generar informe si SPF o DKIM falla <br> `d` - Generar informe si DKIM falla <br> `s` - Generar informe si falla SPF | `1` (recomendado para informes de DMARC) |
| `pct` | Opcional | Especifica el porcentaje de mensajes sujetos al filtrado. | `pct=20` | `100` |
| `rua` | Opcional (recomendado) | Designa dónde se envían los informes agregados. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Opcional (recomendado) | Designa dónde se entregan los informes forenses. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Opcional | Especifica la directiva de DMARC para los subdominios del dominio principal. | `sp=reject` | - |
| `adkim` | Opcional | Especifica una alineación estricta (`s`) o relajada (`r`). La alineación relajada significa que el dominio se utiliza en la firma DKIM y puede ser un subdominio de la dirección `From:`. La alineación estricta significa que el dominio se utiliza en la firma DKIM y debe coincidir exactamente con el dominio utilizado en la dirección `From:`. | `adkim=r` | `r` |
| `aspf` | Opcional | Puede ser estricto (`s`) o relajado (`r`). El modo relajado significa que el dominio Return-Path puede ser un subdominio de la dirección `From:`. El modo estricto significa que el dominio Return-Path debe coincidir exactamente con la dirección `From:`. | `aspf=r` | `r` |

Para obtener información detallada acerca de DMARC y todas sus opciones, consulte [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Implementación de DMARC para Marketo Engage

Existen dos tipos de alineación para DMARC:

* Alineación de **DKIM** (correo identificado por claves de dominio): el dominio especificado en el encabezado `From:` de un correo electrónico coincide con la firma DKIM. La firma DKIM contiene un valor `d=` en el que el dominio se ha especificado para coincidir con el dominio del encabezado `From:`.

  La alineación DKIM valida si el remitente está autorizado para enviar correos electrónicos desde el dominio y verifica que no se haya cambiado ningún contenido durante el tránsito de correos electrónicos. Para implementar DMARC alineado con DKIM:

   * Configure DKIM para el dominio MAIL FROM del mensaje. Use las [instrucciones](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentación del Marketo Engage.

   * Configure DMARC para el dominio DKIM MAIL FROM.

  >[!NOTE]
  >
  >Se recomienda la alineación DKIM para el Marketo Engage.

* Alineación de **SPF** (Marco de directivas de remitente): el dominio del encabezado `From:` debe coincidir con el dominio del encabezado Return-Path:. Si ambos dominios DNS son iguales, el SPF coincide (se alinea) y proporciona un resultado de aprobación. Para implementar DMARC alineado con SPF:

   * Configure el dominio Return-Path con marca.

      * Configure el registro SPF adecuado.
      * Cambie el registro MX para que vuelva al MX predeterminado del centro de datos desde el que se envía el correo

   * Configure DMARC para el dominio Return-Path de marca.

  >[!NOTE]
  >
  >No se admite ni se recomienda una alineación estricta del SPF para el Marketo Engage.

### IP dedicadas y grupo compartido

Si envía correo a través de un Marketo Engage a través de una IP específica y no ha implementado una ruta de retorno de marca (o no está seguro de haberlo hecho), abra un ticket con [Soporte de Adobe](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=home#support){target="_blank"}.

Las IP de confianza son un grupo compartido de IP que están reservadas para usuarios de menor volumen que envíen menos de 75 000 al mes y no cumplen los requisitos para una IP dedicada. Estos usuarios también deben cumplir con los requisitos de las prácticas recomendadas.

* Si está enviando correo a través del Marketo Engage mediante un grupo compartido de direcciones IP, puede comprobar si cumple los requisitos para las direcciones IP de confianza [solicitando el programa de intervalo de envío de IP de confianza](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. La ruta de retorno con marca se incluye al enviar desde direcciones IP de confianza de Marketo Engage. Si se aprueba para este programa, póngase en contacto con Soporte técnico de Adobe para configurar la ruta de retorno de marca.

* Si envía más de 100 000 mensajes al mes y desea enviar un correo electrónico a través de Marketo Engage mediante direcciones IP compartidas, póngase en contacto con el equipo de cuenta de Adobe (su administrador de cuentas) para adquirir una dirección IP dedicada.

## Configurar registros MX para su dominio

Un registro MX le permite recibir correo electrónico en el dominio desde el que envía el correo electrónico para procesar las respuestas y los respondedores automáticos. Si envía desde su dominio corporativo, probablemente ya esté configurado. Si no es así, normalmente puede configurarlo para asignarlo a su registro MX de dominio corporativo.

## Direcciones IP de salida

Una conexión saliente es la que realiza el Marketo Engage a un servidor de Internet en su nombre. Su organización de TI y algunos socios/proveedores pueden utilizar listas de permitidos para restringir el acceso a los servidores. Si es así, debe proporcionarles bloques de direcciones IP salientes de Marketo Engage para añadirlos a sus listas de permitidos.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Bloqueos de direcciones IP salientes

Las siguientes listas abarcan todos los servidores de Marketo Engage que realizan llamadas salientes. Consulte estas listas para configurar una lista de permitidos IP, un servidor, un cortafuegos, una lista de control de acceso, un grupo de seguridad o un servicio de terceros para recibir conexiones salientes de Marketo Engage.

| Bloque IP (Notación CIDR) | Dirección IP individual |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
