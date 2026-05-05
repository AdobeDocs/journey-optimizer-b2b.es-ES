---
title: Configuración del seguimiento y el envío de correo electrónico
description: 'Configuración de los protocolos de envío de correo electrónico: configure las listas de permitidos DNS, SPF, DKIM, DMARC e IP para un seguimiento y una entregabilidad óptimos en Journey Optimizer B2B Edition.'
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
subfeature_v2:
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cad51180-f8ce-4cb7-aefc-437847b5d6d6
autotag-review: '2026-03-30T23:06:01.153Z'
source-git-commit: ee080e04cdc38327ef2367c0f55eee2ae606de51
workflow-type: tm+mt
source-wordcount: 2374
ht-degree: 89%

---

# Configuración del seguimiento y el envío de correo electrónico

Adobe Journey Optimizer B2B edition aprovecha las funciones del canal de correo electrónico y el seguimiento de eventos en la instancia de Marketo Engage adjunta. Para garantizar que la entrega de correo electrónico funciona según lo esperado en las organizaciones que utilizan una configuración restrictiva del servidor de seguridad o del servidor proxy, un administrador del sistema debe añadir determinados dominios e intervalos de direcciones IP a la lista de permitidos.

>[!NOTE]
>
>Si su organización ya está utilizando la instancia de Marketo Engage conectada para ejecutar las operaciones de marketing, estos protocolos y configuraciones ya deben estar implementados.

Asegúrese de que los siguientes dominios (incluido el asterisco) se agregan a la lista de permitidos para habilitar todos los recursos de Marketo Engage y sockets web:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Complete los siguientes pasos para garantizar el seguimiento y la entrega por correo electrónico:

1. [Creación de registros DNS para páginas de aterrizaje y correo electrónico](#create-dns-records-for-landing-pages-and-email)
1. [Configurar SPF y DKIM](#set-up-spf-and-dkim)
1. [Configurar DMARC](#set-up-dmarc)
1. [Configurar registros MX para el dominio](#set-up-mx-records-for-your-domain)
1. [Adición de direcciones IP salientes a listas de permitidos](#outbound-ip-addresses)

>[!NOTE]
>
>Los servicios de envío de correo electrónico y consultoría son ofertas pagadas independientes de Adobe. Si necesita o desea recibir asistencia del equipo de entrega de la instancia de Journey Optimizer B2B edition, debe adquirir uno de los paquetes de servicios de entrega de correo electrónico (Essentials, Enhanced o Plus) para esa instancia. Esto es independiente de cualquier paquete de capacidad de entrega en una instancia de Marketo Engage preexistente. Los servicios de capacidad de entrega se adjuntan por instancia, no por organización. La compatibilidad con la entrega en ambas instancias requiere dos paquetes de servicios de entrega independientes. Cada vez que se aprovisiona una nueva IP para Journey Optimizer B2B edition, se requiere un nuevo paquete de servicios de capacidad de entrega para el calentamiento de la IP y la compatibilidad de la capacidad de entrega continua.

## Creación de registros DNS para páginas de aterrizaje y correo electrónico

La conexión de un registro CNAME permite a los especialistas en marketing alojar versiones web de los correos electrónicos, páginas de destino y blogs con una personalización de marca coherente que mejora el tráfico y las conversiones. Se recomienda muy especialmente añadir los CNAME a su host de dominio raíz para que Marketo Engage aloje sus recursos web centrados en marketing. Como administrador, debe trabajar con su equipo de marketing para planificar e implementar un registro CNAME para los vínculos de seguimiento que se incluyen en los correos electrónicos enviados a través de Marketo Engage.

Como administrador, debe trabajar con su equipo de marketing para planificar e implementar dos registros CNAME. El primero es para las direcciones URL de las páginas de aterrizaje, de modo que las páginas de aterrizaje aparezcan en direcciones URL que reflejen el dominio y no Adobe Marketo Engage (el host real). El segundo es para los vínculos de seguimiento incluidos en los correos electrónicos enviados a través de Marketo Engage.

### Añadir el CNAME para páginas de aterrizaje

Agregue el CNAME de la página de aterrizaje a su registro DNS para que `[YourLandingPageCNAME]` apunte a la cadena de cuenta única asignada a sus páginas de aterrizaje. Inicie sesión en el sitio del registrador de dominios e introduzca el CNAME de la página de aterrizaje y la cadena de cuenta. Esta entrada suele incluir tres campos:

* Alias: escriba `[YourLandingPageCNAME]`
* Tipo: CNAME
* Apuntar a: Escriba `[MunchkinID].mktoweb.com`

### Añadir el CNAME de los vínculos de seguimiento del correo electrónico

Añada el CNAME del correo electrónico para que `[YourEmailCNAME]` apunte a `[MktoTrackingLink]`, que es vínculo de seguimiento predeterminado que Marketo Engage asigna, en el formato:

`[YourEmailCNAME].[YourDomain].com` IN CNAME `[MktoTrackingLink]`

Por ejemplo:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>El valor `[MktoTrackingLink]` debe ser el [dominio de personalización de marca](../admin/configure-channels-emails.md#branding-domains) predeterminado.

### Aprovisionar el certificado SSL

Póngase en contacto con [el servicio de asistencia de Adobe](https://experienceleague.adobe.com/home?lang=es&support-tab=home#support){target="_blank"} para iniciar el proceso de aprovisionamiento de un certificado SSL.

Este proceso puede tardar hasta tres días hábiles en completarse.

## Configurar SPF y DKIM

El equipo de marketing debe proporcionar la información de DKIM (Domain Keys Identifed Mail) que se añadirá al registro de recursos DNS. Siga estos pasos para configurar DKIM y SPF (marco de directivas de remitente) y, a continuación, notifíqueselo a su equipo de marketing cuando esté actualizado.

Puede utilizar la misma configuración de DKIM para la instancia de producción de Marketo Engage y la instancia de Journey Optimizer B2B edition adjunta. En la instancia adjunta, cree exactamente el mismo dominio que en la instancia de Marketo Engage. No es necesario que coincidan los valores del selector y el cifrado. Una vez agregado el dominio a la instancia de Journey Optimizer B2B edition, abra un ticket de asistencia de Adobe para solicitar que la configuración de DKIM se comparta desde la instancia de Marketo Engage a la nueva. Proporcione el prefijo Marketo Engage (Munchkin ID) y el nuevo prefijo Journey Optimizer B2B edition (Munchkin ID).

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

DMARC (Domain-based Message Authentication, Reporting, and Conformance) es un protocolo de autenticación que se utiliza para ayudar a las organizaciones a proteger su dominio frente al uso no autorizado. Amplía los protocolos de autenticación existentes, como SPF y DKIM, para informar a los servidores de destinatario sobre las acciones que deben realizarse si se produce un error de autenticación en su dominio. DMARC es opcional, pero se recomienda encarecidamente porque ayuda a proteger su marca y su reputación. Los principales proveedores, como Google y Yahoo, comenzaron a exigir el uso de DMARC para remitentes masivos a partir de febrero de 2024.

Para que DMARC funcione, debe tener al menos uno de los siguientes registros TXT de DNS:

* Un SPF válido
* Un registro de DKIM válido para su dominio FROM: (recomendado para [!DNL Marketo Engage] y [!UICONTROL Journey Optimizer B2B edition])

Además, configure un registro TXT DNS específico de DMARC para su dominio `FROM:`. Opcionalmente, puede definir una dirección correo electrónico que especifique adónde deben ir los informes DMARC dentro de su organización para la monitorización de informes.

### Ejemplo de flujo de trabajo DMARC

>[!TIP]
>
>Se recomienda implementar DMARC como un _despliegue gradual_. Escale su directiva de DMARC de `p=none`, a `p=quarantine`, y luego a `p=reject`, a medida que vaya comprendiendo el impacto potencial, y establezca su directiva DMARC en una alineación relajada en SPF y DKIM.

Si recibe informes DMARC, debe hacer lo siguiente:

1. Utilice `p=none` y analice los comentarios e informes que reciba. Los informes indican al receptor que no realice ninguna acción con los mensajes que no superan la autenticación y que envíe informes de correo electrónico al remitente.

   * Si los mensajes legítimos fallan en la autenticación, revise y corrija los problemas con SPF/DKIM.

   * Determine si SPF o DKIM están alineados y pasando la autenticación para todos los correos electrónicos legítimos.

   * Revise los informes para asegurarse de que los resultados son los esperados en función de sus directivas de SPF/DKIM.

1. Ajuste la directiva en `p=quarantine`, que indica al servidor de correo electrónico receptor que ponga en cuarentena los correos electrónicos en los que se producen errores de autenticación (normalmente colocando esos mensajes en la carpeta de spam).

   Revise los informes para asegurarse de que los resultados son los esperados.

1. Si está satisfecho con el comportamiento de los mensajes en el nivel `p=quarantine`, puede ajustar la directiva a (`p=reject`).

   La directiva de rechazo indica al receptor que deniegue (rechace) cualquier correo electrónico del dominio que no supere la autenticación. Con esta directiva habilitada, solo el correo electrónico verificado como 100 % autenticado por su dominio tiene la oportunidad de colocarse en la bandeja de entrada.

   >[!CAUTION]
   >
   >Utilice este directiva con precaución y determine si es adecuada para su organización.

### Sistema de informes DMARC

DMARC ofrece la posibilidad de recibir informes sobre correos electrónicos en los que se producen errores en SPF/DKIM. Los servicios ISP generan dos informes diferentes como parte del proceso de autenticación. Los remitentes pueden recibir estos informes a través de las etiquetas RUA/RUF de su directiva DMARC.

* **Informes agregados (RUA):** no contienen ninguna PII (información de identificación personal) que pueda ser sensible al RGPD (Reglamento general de protección de datos).

* **Informes forenses (FRU):** contienen direcciones correo electrónico que son sensibles al RGPD. Antes de implementar este informe, verifique la directiva de su organización para gestionar la información que debe cumplir con el RGPD.

El principal uso de estos informes es recibir información general de los correos electrónicos cuya identidad se ha intentando suplantar. Son informes muy técnicos y se analizan mejor con una herramienta de terceros.

### Ejemplos de registros DMARC

* Registro mínimo: `v=DMARC1; p=none`

* Registro que dirige a una dirección correo electrónico para recibir informes: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### Etiquetas DMARC

Los registros de DMARC tienen varios componentes llamados _Etiquetas DMARC_. Cada etiqueta tiene un valor que especifica un aspecto determinado de DMARC.

| Nombre de la etiqueta | Utilice | Función | Ejemplo | Valor predeterminado |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obligatorio | Especifica la versión. Solo hay una versión, por lo que tiene un valor fijo de `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obligatorio | Especifica la directiva de DMARC, que indica al receptor que informe, ponga en cuarentena o rechace los mensajes de correo electrónico que no superen las comprobaciones de autenticación. | `p=none`, `p=quarantine` o `p=reject` | - |
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

  La alineación de DKIM valida si el remitente está autorizado para enviar correo desde el dominio y comprueba que no se ha cambiado ningún contenido durante el envío de correo electrónico. Para implementar DMARC alineado con DKIM:

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

Si envía un correo electrónico mediante Marketo Engage a través de una IP dedicada y no ha implementado return-path (o no está seguro de si lo ha hecho), abra una entrada con el [servicio de asistencia de Adobe](https://experienceleague.adobe.com/home?lang=es&support-tab=home#support){target="_blank"}.

>[!BEGINSHADEBOX]

**Migración de direcciones IP dedicadas a Journey Optimizer B2B edition**

Si tiene direcciones IP dedicadas, debe tener la nueva instancia de Journey Optimizer B2B edition creada en la misma región que la instancia de Marketo Engage existente. Si la nueva instancia se encuentra en una región diferente, no es posible compartir la IP existente. Si la región coincide, abre un ticket con [Soporte técnico de Adobe](https://experienceleague.adobe.com/home?lang=es&support-tab=home#support){target="_blank"} para solicitar que tus grupos de enlace e IP existentes se compartan con la nueva instancia. Proporcione el prefijo Marketo Engage (Munchkin ID) y el nuevo prefijo Journey Optimizer B2B edition (Munchkin ID).

Con esta solicitud, Adobe replica las mismas direcciones IP, grupos de enlace y dominios de ruta de retorno configurados como instancia de Marketo Engage. Cuando las IP se comparten entre las instancias de Marketo Engage y Journey Optimizer B2B edition, las utilizan simultáneamente.

>[!ENDSHADEBOX]

Las IP de confianza son un grupo compartido de IP reservadas a usuarios con un volumen de envíos inferior a 75 000 por mes y que no pueden optar a una IP dedicada. Estos usuarios también deben cumplir los requisitos de prácticas recomendadas.

* Si envía correo a través de Marketo Engage utilizando un grupo compartido de IP, puede comprobar si reúne los requisitos para las IP de confianza [solicitando el programa de rango de envíos de IP de confianza](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html?lang=es){target="_blank"}. La ruta return-path de marca se incluye al enviar las IP de confianza de Marketo Engage. Si ha recibido la aprobación para este programa, póngase en contacto con el servicio de asistencia de Adobe para configurar la ruta return-path de marca.

* Si envía más de 100 000 mensajes al mes y desea enviar correo electrónico través de Marketo Engage utilizando IP compartidas, póngase en contacto con el equipo de cuentas de Adobe (su administrador de cuentas) para comprar una IP dedicada.

Los clientes del grupo de IP compartidas no necesitan ninguna configuración adicional. Sigue utilizando los mismos grupos de IP y el mismo dominio de ruta de retorno predeterminado que antes.

## Configurar registros MX para el dominio

Un registro MX le permite recibir correo en el dominio desde el que envía correo para procesar respuestas y respondedores automáticos. Si envía desde su dominio corporativo, probablemente ya esté configurado. Si no es así, puede configurarlo para que se asigne al registro MX de su dominio corporativo.

## Direcciones IP permitidas

Marketo Engage establece una conexión saliente con un servidor de Internet en su nombre. Su organización de TI y algunos socios/proveedores pueden utilizar listas de permitidos para restringir el acceso a los servidores. Si es así, debe proporcionarles bloques de direcciones IP salientes de Marketo Engage para añadirlos a sus listas de permitidos.

<!--
Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allow list on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allow list. For more information, see [_Create a webhook_](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [_Call Webhook_](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [_Add an Existing Salesforce Field to the Marketo Sync_](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [_Understanding the Microsoft Dynamics Sync_](https://experienceleague.adobe.com/es/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. 
-->

## Bloques de direcciones IP de salida

Las siguientes listas abarcan todos los servidores de Marketo Engage que realizan llamadas de salida. Consulte estas listas para configurar una lista de permitidos IP, servidor, cortafuegos, lista de control de acceso, grupo de seguridad o servicio de terceros para recibir conexiones de salida desde Marketo Engage.

| Bloque de IP (notación CIDR) | Dirección IP individual |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
