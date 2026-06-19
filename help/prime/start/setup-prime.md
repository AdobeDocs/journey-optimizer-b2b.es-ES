---
title: Instalación
description: Complete las tareas de configuración iniciales de la instancia de Prime B2B de Journey Optimizer, incluida la configuración de acceso de los usuarios y la infraestructura de envío de correo electrónico.
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f467931a-9b22-4ca8-869f-adfbd64061ceid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 579f36911af99308294726e91e80c5d08015d5cf
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 55%

---

# Configuración

Complete estas tareas para habilitar la funcionalidad en la instancia de Recorrido B2B Prime aprovisionada.

## Habilitar acceso de usuario

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
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Crear un perfil de producto de Marketo Engage en Adobe Admin Console (solo la nueva instancia de Marketo Engage)</td>
<td><a href="./user-management.md#create-profile">Más información</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Añadir un grupo de usuarios para el perfil</td>
<td><a href="./user-management.md#add-user-group">Más información</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configuración de funciones de usuario B2B</td>
<td><a href="./user-management.md#edit-roles-for-product-permissions">Más información</a></td>
</tr>
<tr>
<td><img src=".../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Agregar usuarios o grupos a las funciones</td>
<td><a href="./user-management.md#add-users-to-a-role">Más información</a></td>
</tr>
</tbody>
</table>

## Entregabilidad del correo electrónico

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
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Delegación de un subdominio en Adobe</td>
<td><a href="./admin/configuration-email-deliverability.md#delegate-fully-delegated">Totalmente delegado</a> o <a href="./admin/configuration-email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Configuración de DMARC para el subdominio</td>
<td><a href="./admin/configuration-email-deliverability.md#configure-dmarc">Más información</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Revisar y asignar un grupo de IP</td>
<td><a href="./admin/configuration-email-deliverability.md#review-ip-pool">Más información</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Casilla de verificación"/></td>
<td>Crear una configuración de canal de correo electrónico</td>
<td><a href="./admin/configuration-email-deliverability.md#create-email-channel-configuration">Obtenga más información</a></td>
</tr>
</tbody>
</table>

