---
title: Protocolos para el seguimiento y el envío de correos electrónicos
description: Obtenga información sobre cómo configurar protocolos en Marketo Engage para que los utilice Journey Optimizer B2B Edition para el seguimiento y las funciones de canal de correo electrónico.
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 100%

---

# Protocolos para el seguimiento y el envío de correos electrónicos

Adobe Journey Optimizer B2B Edition aprovecha las funciones del canal de correo electrónico y el seguimiento de los eventos de Marketo Engage. Para asegurarse de que el envío de correo electrónico funciona de acuerdo con lo previsto para las organizaciones que utilizan cortafuegos restrictivos o una configuración de servidor proxy, un administrador del sistema debe añadir determinados dominios e intervalos de direcciones IP a la lista de permitidos.

>[!NOTE]
>
>Si su organización ya está utilizando el instancia de Marketo Engage conectada para ejecutar sus operaciones de marketing, estos protocolos y configuraciones ya deberían estar implementados.

Asegúrese de que los siguientes dominios (incluido el asterisco) se añaden a la lista de permitidos para habilitar todos los recursos de Marketo Engage y sockets web:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Siga estos pasos para garantizar el seguimiento y el envío de correos electrónicos:

1. [Crear registros DNS para ](#create-dns-records-for-landing-pages-and-email)
1. [Configurar SPF y DKIM](#set-up-spf-and-dkim)
1. [Configurar DMARC](#set-up-dmarc)
1. [Configurar registros MX para el dominio](#set-up-mx-records-for-your-domain)
1. [Añadir direcciones IP de salida a las listas de permitidos](#outbound-ip-addresses)

## Crear registros DNS para <!-- landing pages and -->correos electrónicos

La conexión de un registro CNAME permite a los especialistas en marketing alojar versiones web de los correos electrónicos, páginas de aterrizaje y blogs con una personalización de marca coherente que mejora el tráfico y las conversiones. Se recomienda muy especialmente añadir los CNAME a su host de dominio raíz para que Marketo Engage aloje sus recursos web centrados en marketing. Como administrador, debe trabajar con su equipo de marketing para planificar e implementar un registro CNAME para los vínculos de seguimiento que se incluyen en los correos electrónicos enviados a través de Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Añadir el CNAME de los vínculos de seguimiento del correo electrónico

Añada el CNAME del correo electrónico para que `[YourEmailCNAME]` apunte a `[MktoTrackingLink]`, que es vínculo de seguimiento predeterminado que Marketo Engage asigna, en el formato:

`[YourEmailCNAME].[YourDomain].com` IN CNAME `[MktoTrackingLink]`

Por ejemplo:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>El valor `[MktoTrackingLink]` debe ser el dominio de personalización de marca predeterminado.

### Aprovisionar el certificado SSL

Póngase en contacto con [el servicio de asistencia de Adobe](https://experienceleague.adobe.com/home?lang=es&amp;support-tab=home#support){target="_blank"} para iniciar el proceso de aprovisionamiento de un certificado SSL.

Este proceso puede tardar hasta tres días hábiles en completarse.

## Configurar SPF y DKIM

El equipo de marketing debe proporcionar la información de DKIM (Domain Keys Identifed Mail) que se añadirá al registro de recursos DNS. Siga estos pasos para configurar DKIM y SPF (marco de directivas de remitente) y, a continuación, notifíqueselo a su equipo de marketing cuando esté actualizado.

1. Para configurar SPF, añada la línea siguiente a las entradas de DNS:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Si ya tiene un registro SPF existente en la entrada de DNS, simplemente añada lo siguiente:

   ```
   include: mktomail.com
   ```

   Sustituya `CompanyDomain` por el dominio principal de su sitio web (como `company.com/`) y `CorpIP` por la dirección IP de su servidor de correo electrónico corporativo (como `255.255.255.255`). Si tiene pensado enviar el correo electrónico desde varios dominios a través de Marketo Engage, añada esta línea para cada dominio (en una línea).

1. Para DKIM, cree registros de recursos DNS para cada dominio.

   Añada los registros de host y los valores TXT de cada dominio:

   `[DKIMDomain1]`: El registro de host es `[HostRecord1]` y el valor TXT es `[TXTValue1]`.

   `[DKIMDomain2]`: El registro de host es `[HostRecord2]` y el valor TXT es `[TXTValue2]`.

   Copie `HostRecord` y `TXTValue` para cada dominio DKIM después de seguir las [instrucciones](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentación de Marketo Engage. Puede verificar los dominios en Journey Optimizer B2B Edition (consulte [SPF/DKIM).](../admin/configure-channels-emails.md#spfdkim)

## Configurar DMARC

DMARC (Domain-based Message Authentication, Reporting, and Conformance) es un protocolo de autenticación que se utiliza para ayudar a las organizaciones a proteger su dominio frente al uso no autorizado. Amplía los protocolos de autenticación existentes, como SPF y DKIM, para informar a los servidores de destinatario sobre las acciones que deben realizarse si se produce un error de autenticación en su dominio. DMARC es opcional, pero se recomienda muy especialmente porque ayuda a proteger su marca y su reputación. Los principales proveedores, como Google y Yahoo, comenzaron a exigir el uso de DMARC para remitentes masivos a partir de febrero de 2024.

Para que DMARC funcione, debe tener al menos uno de los siguientes registros TXT de DNS:

* Un SPF válido
* Un registro DKIM válido para su dominio FROM: (recomendado para Marketo Engage y Journey Optimizer B2B Edition)

También debe tener un registro TXT de DNS específico de DMARC para su dominio `FROM:`. Opcionalmente, puede definir una dirección correo electrónico que especifique adónde deben ir los informes DMARC dentro de su organización para la monitorización de informes.

### Ejemplo de flujo de trabajo DMARC

>[!TIP]
>
>Es una buena práctica implementar DMARC como un _despliegue lento_. Escale su directiva de DMARC de `p=none`, a `p=quarantine`, y luego a `p=reject`, a medida que vaya comprendiendo el impacto potencial, y establezca su directiva DMARC en una alineación relajada en SPF y DKIM.

Si recibe informes DMARC, debe hacer lo siguiente:

1. Utilice `p=none` y analice los comentarios e informes que reciba. Los informes indican al receptor que no realice ninguna acción con los mensajes que no superan la autenticación y que envíe informes de correo electrónico al remitente.

   * Si los mensajes legítimos fallan en la autenticación, revise y corrija los problemas con SPF/DKIM.

   * Determine si SPF o DKIM están alineados y pasando la autenticación para todos los correos electrónicos legítimos.

   * Revise los informes para asegurarse de que los resultados son los esperados en función de sus directivas de SPF/DKIM.

1. Ajuste la directiva en `p=quarantine`, que indica al servidor de correo electrónico receptor que ponga en cuarentena los correos electrónicos en los que se producen errores de autenticación (normalmente colocando esos mensajes en la carpeta de spam).

   Revise los informes para asegurarse de que los resultados son los esperados.

1. Si está satisfecho con el comportamiento de los mensajes en el nivel `p=quarantine`, puede ajustar la directiva en (`p=reject`).

   La directiva de rechazo indica al receptor que deniegue (rechace) cualquier correo electrónico del dominio que no supere la autenticación. Con esta directiva habilitada, solo el correo electrónico verificado como 100 % autenticado por su dominio tiene la oportunidad de colocarse en la bandeja de entrada.

   >[!CAUTION]
   >
   >Utilice este directiva con precaución y determine si es adecuada para su organización.

### Sistema de informes DMARC

DMARC ofrece la posibilidad de recibir informes sobre correos electrónicos en los que se producen errores en SPF/DKIM. Existen dos informes distintos que generan los proveedores de servicios de Internet como parte del proceso de autenticación. Los remitentes pueden recibir estos informes a través de las etiquetas RUA/RUF de su directiva DMARC.

* **Informes agregados (RUA):** no contienen ninguna PII (información de identificación personal) que pueda ser sensible al RGPD (Reglamento general de protección de datos).

* **Informes forenses (FRU):** contienen direcciones correo electrónico que son sensibles al RGPD. Antes de implementar este informe, verifique la directiva de su organización para gestionar la información que debe cumplir con el RGPD.

El principal uso de estos informes es recibir información general de los correos electrónicos cuya identidad se ha intentando suplantar. Son informes muy técnicos y es mejor procesarlos a través de un herramienta de terceros.

### Ejemplos de registros DMARC

* Registro mínimo: `v=DMARC1; p=none`

* Registro que dirige a una dirección correo electrónico para recibir informes: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Etiquetas DMARC

Los registros de DMARC tienen varios componentes llamados _Etiquetas DMARC_. Cada etiqueta tiene un valor que especifica un aspecto determinado de DMARC.

| Nombre de la etiqueta | Utilice  | Función | Ejemplo | Valor predeterminado |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obligatorio | Especifica la versión. Solo hay una versión, por lo que tiene un valor fijo de `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obligatorio | Especifica la directiva de DMARC, que indica al receptor que informe, ponga en cuarentena o rechace los mensajes de correo electrónico que no superen las comprobaciones de autenticación. |  `p=none`, `p=quarantine` o `p=reject` | - |
| `fo` | Opcional | Permite al propietario del dominio especificar las opciones del sistema de informes. | `0`: generar informe si SPF y DKIM fallan <br> `1`. generar informe si SPF o DKIM falla <br> `d`: generar informe si DKIM falla <br> `s`: generar informe si falla SPF | `1` (recomendado para informes de DMARC) |
| `pct` | Opcional | Especifica el porcentaje de mensajes sujetos al filtrado. | `pct=20` | `100` |
| `rua` | Opcional (recomendado) | Designa adónde se envían los informes agregados. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Opcional (recomendado) | Designa adónde se envían los informes forenses. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Opcional | Especifica la directiva de DMARC para los subdominios del dominio principal. | `sp=reject` | - |
| `adkim` | Opcional | Especifica una alineación estricta (`s`) o relajada (`r`). La alineación relajada significa que el dominio se utiliza en la firma de DKIM y puede ser un subdominio de la dirección `From:`. La alineación estricta significa que el dominio se utiliza en la firma de DKIM y debe coincidir exactamente con el dominio utilizado en la dirección `From:`. | `adkim=r` | `r` |
| `aspf` | Opcional | Puede ser estricto (`s`) o relajado (`r`). El modo relajado significa que el dominio Return-Path puede ser un subdominio de la dirección `From:`. El modo estricto significa que el dominio Return-Path debe coincidir exactamente con la dirección `From:`. | `aspf=r` | `r` |

Para obtener información detallada sobre DMARC y todas sus opciones, consulte [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### Implementación de DMARC para Marketo Engage

Existen dos tipos de alineación para DMARC:

* Alineación **DKIM** (Domain Keys Identified Mail): el dominio especificado en el encabezado `From:` de un correo electrónico coincide con DKIM-Signature. La firma de DKIM contiene un valor `d=` en el que el dominio se ha especificado para coincidir con el dominio del encabezado `From:`.

  La alineación DKIM valida si el remitente está autorizado a enviar correo desde el dominio y comprueba que no se ha cambiado ningún contenido durante el envío de correo. Para implementar DMARC alineado con DKIM:

   * Configure DKIM para el dominio MAIL FROM del mensaje. Siga las [instrucciones](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} de la documentación de Marketo Engage.

   * Configure DMARC para el dominio DKIM MAIL FROM.

  >[!NOTE]
  >
  >Se recomienda la alineación de DKIM para Marketo Engage.

* Alineación **SPF** (marco de directivas de remitente): el dominio del encabezado `From:` debe coincidir con el dominio del encabezado Return-Path:. Si ambos dominios DNS son iguales, el SPF coincide (se alinea) y proporciona un resultado de aprobación. Para implementar DMARC alineado con SPF:

   * Configure el dominio de marca Return-Path.

      * Configure el registor SPF apropiado.
      * Cambie el registro MX para que apunte de nuevo al MX predeterminado del centro de datos desde el que se envía el correo.

   * Configure DMARC para el dominio de marca Return-Path.

  >[!NOTE]
  >
  >La alineación SPF estricta no es compatible ni recomendable para Marketo Engage.

### Direcciones IP dedicadas y grupos compartidos

Si envía un correo electrónico mediante Marketo Engage a través de una IP dedicada y no ha implementado return-path (o no está seguro de si lo ha hecho), abra una entrada con el [servicio de asistencia de Adobe](https://experienceleague.adobe.com/home?lang=es&amp;support-tab=home#support){target="_blank"}.

Las IP de confianza son un grupo compartido de IP reservadas a usuarios con un volumen de envíos inferior a 75 000 por mes y que no pueden optar a una IP dedicada. Estos usuarios también deben cumplir los requisitos de prácticas recomendadas.

* Si envía correo a través de Marketo Engage utilizando un grupo compartido de IP, puede comprobar si reúne los requisitos para las IP de confianza [solicitando el programa de rango de envíos de IP de confianza](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html?lang=es){target="_blank"}. La ruta return-path de marca se incluye al enviar las IP de confianza de Marketo Engage. Si ha recibido la aprobación para este programa, póngase en contacto con el servicio de asistencia de Adobe para configurar la ruta return-path de marca.

* Si envía más de 100 000 mensajes al mes y desea enviar correo electrónico través de Marketo Engage utilizando IP compartidas, póngase en contacto con el equipo de cuentas de Adobe (su administrador de cuentas) para adquirir una IP dedicada. 

## Configurar registros MX para el dominio

Un registro MX le permite recibir correo en el dominio desde el que envía correo para procesar respuestas y respondedores automáticos. Si envía desde su dominio corporativo, probablemente ya esté configurado. Si no es así, puede configurarlo para que se asigne al registro MX de su dominio corporativo. 

## Direcciones IP permitidas

Una conexión de salida es aquella creada por Marketo Engage en un servidor de Internet en su nombre. Su organización de TI y algunos socios/proveedores pueden utilizar listas de permitidos para restringir el acceso a los servidores. Si es así, debe proporcionarles bloques de direcciones IP de salida de Marketo Engage para añadirlos a sus listas de permitidos.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Bloques de direcciones IP de salida

Las siguientes listas abarcan todos los servidores de Marketo Engage que realizan llamadas de salida. Consulte estas listas para configurar una lista de permitidos IP, servidor, cortafuegos, lista de control de acceso, grupo de seguridad o servicio de terceros para recibir conexiones de salida desde Marketo Engage.

| Bloque de IP (notación CIDR) | Dirección IP individual |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
