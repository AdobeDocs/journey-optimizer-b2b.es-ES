---
title: Configurar lista de comprobación
description: Complete las tareas de configuración iniciales de la instancia de Prime B2B de Journey Optimizer, incluida la configuración de acceso de los usuarios y la infraestructura de envío de correo electrónico.
badgeBeta: label="Beta" type="informative" tooltip="Esta función forma parte de una versión beta limitada."
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f467931a-9b22-4ca8-869f-adfbd64061ceid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 0f264f00c8018324abf1d409ddc381c6dcc9c08a
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 10%

---

# Configurar lista de comprobación

Complete estas tareas para habilitar la funcionalidad en la instancia [!DNL Journey Optimizer B2B Prime] aprovisionada.

## Habilitar acceso de usuario {#enable-user-access}

Cuando el aprovisionamiento se haya completado y las zonas protegidas estén enlazadas, configure el acceso de [!DNL Journey Optimizer B2B Edition] para su equipo y para los usuarios.

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
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Crear un perfil de producto de Journey Optimizer B2B edition en Admin Console (solo una vez/configuración inicial)</td>
<td><a href="./user-management.md#create-profile">Crear perfil</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Añadir un grupo de usuarios en Admin Console</td>
<td><a href="./user-management.md#add-user-group">Agregar grupo de usuarios</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Asigne el perfil de producto al grupo de usuarios en Admin Console</td>
<td><a href="./user-management.md#assign-profile">Asignar perfil de producto</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Añadir usuarios al grupo de usuarios en Admin Console</td>
<td><a href="./user-management.md#add-users">Añadir usuarios</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Editar funciones integradas o crear una función personalizada con permisos de producto</td>
<td><a href="./user-management.md#edit-role-permissions">Editar roles</a> <br/> <a href="./user-management.md#create-a-custom-role">Crear un rol personalizado</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Adición de usuarios o grupos a las funciones de Adobe Experience Platform</td>
<td><a href="./user-management.md#add-users-to-a-role">Agregar usuarios</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">Agregar grupos</a></td>
</tr>
</tbody>
</table>

## Entregabilidad del correo electrónico {#email-deliverability}

Para que los especialistas en marketing puedan enviar correos electrónicos desde las recorridos, configure la infraestructura de envío de su organización, incluida la delegación de subdominios, la autenticación de correo electrónico y la configuración de canal.

<table>
<thead>
<tr>
<th colspan="2">Tarea</th>
<th>Detalles e instrucciones</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configuración de la entrega de correo electrónico y canales</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Delegación de un subdominio en Adobe (completamente delegado o CNAME)</td>
<td><a href="./email-deliverability.md#delegate-fully-delegated">Delegado completamente</a> <br/> <a href="./email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Configuración de DMARC para el subdominio</td>
<td><a href="./email-deliverability.md#configure-dmarc">Configuración de DMARC</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Revisar y asignar un grupo de IP</td>
<td><a href="./email-deliverability.md#review-ip-pool">Revisar grupo de IP</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación para tarea"/></td>
<td>Crear una configuración de canal de correo electrónico</td>
<td><a href="../admin/email-channel-configuration.md#create-email-channel-configuration">Configuración de canal de correo electrónico</a></td>
</tr>
</tbody>
