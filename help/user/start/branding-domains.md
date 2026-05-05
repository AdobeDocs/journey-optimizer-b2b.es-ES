---
title: Configurar dominios de marca
description: Configure los dominios de promoción de la marca para que cada una de las marcas tenga sus propios vínculos de seguimiento de marca.
feature: Setup, Channels
role: Admin
exl-id: ccbcbbee-a5be-46fe-bae0-ab026e5cdb72
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2:
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: '2026-04-29T23:21:59.633Z'
source-git-commit: 0216cf3b1cbc1124b50ad99e649778aef71f5aca
workflow-type: tm+mt
source-wordcount: 1014
ht-degree: 89%

---

# Configurar dominios de personalización de marca

Un dominio de promoción de la marca en Marketo Engage es un subdominio personalizado (como `links.yourcompany.com`) que se utiliza para reescribir vínculos y realizar un seguimiento de los clics en los correos electrónicos, así como para asegurarse de que reflejan su marca en lugar de un dominio genérico. Cada dominio de marca actúa como un dominio de seguimiento de clics para mejorar la capacidad de entrega y la confianza al hacer coincidir los vínculos de su correo electrónico y página de aterrizaje con su dominio.

* Reemplaza los vínculos genéricos con su propia marca en los hipervínculos de correo electrónico.
* Cuando un posible cliente de la cuenta hace clic en un vínculo, redirige a través de este dominio personalizado para permitir el seguimiento del rendimiento mientras parece legítimo a los filtros de correo electrónico.
* Si tiene varias marcas, puede configurar dominios de promoción de otras marcas para que admitan distintas unidades de negocio o marcas.

>[!BEGINSHADEBOX]

**CNAME únicos para vínculos de seguimiento**

Los vínculos de seguimiento de correo electrónico deben ser nuevos y únicos para la instancia de Marketo Engage adjunta. Si tiene CNAME existentes para el seguimiento de vínculos que apuntan a una instancia de Marketo Engage preexistente (producción), no se pueden reutilizar sin realizar modificaciones.

Puede compartir la marca del dominio de ruta de retorno entre la instancia de producción de Marketo Engage y la instancia adjunta, pero se trata de un cambio en el servidor. Abra un ticket de asistencia y proporcione su prefijo Marketo Engage (Munchkin ID) y su nuevo prefijo Journey Optimizer B2B edition (Munchkin ID) para solicitar la promoción de marca de dominio de ruta de retorno compartida.

>[!ENDSHADEBOX]

>[!PREREQUISITES]
>
>Antes de editar o agregar un dominio en la interfaz de usuario, debe tener un CNAME [asignado a un dominio de Marketo Engage proporcionado por Adobe](https://experienceleague.adobe.com/es/docs/marketo/using/getting-started/initial-setup/setup-steps#customize-your-landing-page-urls-with-a-cname){target="_blank"}.
>
>Al añadir un dominio, el sistema comprueba los SSL preexistentes, que pueden haberse creado manualmente anteriormente. Si se produce esta validación, cree el dominio sin seleccionar la creación de SSL y, a continuación, conéctelo como un procedimiento independiente.

## Acceso a dominios de marca en Marketo Engage

1. Vaya al área de **[!UICONTROL Admin]** de su instancia de Marketo Engage y seleccione **[!UICONTROL Correo electrónico]**.

1. Desplácese hacia abajo hasta el panel **[!UICONTROL Dominios de marca]**.

   ![Panel Dominios de marca en el Administrador en Correo electrónico, que muestra el dominio predeterminado](./assets/me-admin-email-branding-domains.png){width="700" zoomable="yes"}

   La lista muestra el dominio predeterminado para la instancia de Marketo Engage.

## Editar el dominio de marca predeterminado

El primer paso para trabajar con los dominios de promoción de la marca es editar el dominio de promoción de la marca predeterminado definido en la instancia de Marketo Engage.

>[!NOTE]
>
>No puede definir un dominio de personalización de marca adicional hasta que haya editado el dominio predeterminado genérico.

1. En el panel _[!UICONTROL Dominios de marca]_, seleccione el dominio genérico y haga clic en **[!UICONTROL Editar]** en la parte superior.

   ![Panel Dominios de marca con el dominio genérico seleccionado](./assets/me-admin-email-branding-domains-edit-default.png){width="500"}

1. En el cuadro de diálogo _[!UICONTROL Editar dominio de marca]_, escriba el nombre de su dominio predeterminado en el campo **[!UICONTROL Dominio]**.

   ![Cuadro de diálogo Editar dominio de marca](./assets/me-admin-email-branding-domains-edit-default-name.png){width="400"}

1. Si tiene varios espacios de trabajo definidos para la instancia de Marketo Engage, haga clic en **[!UICONTROL Siguiente]**.

   Seleccione cada uno de los espacios de trabajo en los que desea aplicar el dominio principal actualizado.

   ![Cuadro de diálogo Editar dominio de promoción de marca con selección de área de trabajo para dominio principal](./assets/me-admin-email-branding-domains-edit-default-workspaces.png){width="400"}

1. Haga clic en **[!UICONTROL Guardar]**.

## Definir un dominio adicional

Después de editar el dominio predeterminado, puede agregar otro dominio de promoción de la marca para admitir varias marcas dentro del entorno de Journey Optimizer B2B edition, donde cada una tiene sus propios vínculos de seguimiento de marca. Al agregar un dominio, tiene las siguientes opciones:

>* _Convertir en dominio principal_: Convierta este dominio en el dominio principal del área de trabajo. Al seleccionar esta opción, todos los correos electrónicos no enviados existentes se establecen en el dominio principal predeterminado y todos los correos electrónicos recién creados se establecen de forma predeterminada en este dominio principal. Los especialistas en marketing pueden elegir un dominio de marca alternativo donde sea necesario.
>
>* _Generar certificado SSL_: Cree una capa de sockets seguros (SSL) con la creación del dominio. El primer dominio de seguimiento inicia una configuración única de la infraestructura que puede tardar unas horas. El sistema envía una notificación al finalizar.

_Para agregar el dominio :_

1. En el panel _[!UICONTROL Dominios de marca]_, haga clic en **[!UICONTROL Agregar]** en la parte superior.

   ![Panel Dominios de marca con el botón Agregar en la parte superior](assets/me-admin-email-branding-domains-add.png){width="500"}

1. En el cuadro de diálogo _[!UICONTROL Nuevo dominio de marca]_, escriba el nombre del dominio de marca en el campo **[!UICONTROL Dominio]**.

1. (Opcional) Seleccione la casilla de verificación **[!UICONTROL Generar certificado SSL]** para generar automáticamente un SSL para el dominio.

   ![Cuadro de diálogo Nuevo dominio de promoción de marca](assets/me-admin-email-branding-domains-add-name.png){width="400"}

   Si es necesario y está disponible, también puede activar la casilla de verificación _Crear dominio principal_.

   >[!NOTE]
   >
   >**_SSL personalizados_**: Si necesita un SSL personalizado, puede enviar un [ticket de asistencia](https://experienceleague.adobe.com/es/support){target="_blank"}. No utilice la casilla de verificación para la creación SSL.

1. Si tiene varios espacios de trabajo definidos para la instancia de Marketo Engage, haga clic en **[!UICONTROL Siguiente]**.

   Si es necesario, seleccione cada uno de los espacios de trabajo donde desee aplicar el nuevo dominio como dominio principal.

   ![Cuadro de diálogo Nuevo dominio de promoción de marca con selección de área de trabajo para aplicar el dominio principal](assets/me-admin-email-branding-domains-add-workspaces.png){width="400"}

1. Haga clic en **[!UICONTROL Guardar]**.

## Editar SSL para dominios de promoción de la marca existentes

Siga estos pasos para habilitar SSL para los dominios existentes.

1. En el área _[!UICONTROL Administrador]_, seleccione **[!UICONTROL Correo electrónico]**.

1. En el panel _[!UICONTROL Dominios de marca]_, seleccione la fila de dominio y haga clic en **[!UICONTROL Agregar SSL]**.

   ![Panel Dominios de marca con Agregar SSL en la parte superior](./assets/me-admin-email-branding-domain-add-ssl.png){width="500"}

1. En el cuadro de diálogo, haga clic en **[!UICONTROL Confirmar]**.

   ![Cuadro de diálogo de confirmación Generar certificado SSL](./assets/me-admin-email-branding-domain-generate-ssl-cert-confirm.png){width="400"}

## Mensajes de error

| Error | Detalles |
| ----- | ------- |
| `Domain already exists.` | Ya existe un dominio con el mismo nombre. |
| `Domain is not mapped to the default domain.` | El dominio personalizado no está asignado correctamente al dominio predeterminado. Compruebe la configuración de asignación de dominios y asegúrese de que la configuración de DNS apunta al dominio predeterminado correcto. |
| `SSL certificates could not be issued due to unsupported CAA records. Request your IT to update your CAA records.` | Los registros de CAA no están actualizados. Para los que utilizan certificados SSL administrados por Adobe, los registros CAA deben actualizarse a los certificados recomendados por el proveedor. |
| `SSL certificate has already been issued.` | Ya existe un certificado SSL para este dominio personalizado. No es necesario realizar ninguna otra acción a menos que el certificado haya caducado o sea necesario volver a emitirlo. |
| `The default domain was not found. Please contact Support for assistance.` | Se ha producido un problema al intentar localizar el dominio predeterminado. Póngase en contacto con el servicio de asistencia de Adobe para investigar déclencheur. |
| `Unexpected error encountered while creating a domain. Please contact Support for assistance.` | Error inesperado. Recopile registros y detalles de errores y, a continuación, remita el problema al servicio de asistencia de Adobe. |

## Eliminar un dominio de personalización de marca

>[!NOTE]
>
>Si desea eliminar el dominio de personalización de marca principal (en uno o más espacios de trabajo), primero debe seleccionar un dominio de personalización de marca diferente para que sea el principal de cada espacio de trabajo.
>
>Al eliminar un dominio **_no_** se elimina el certificado SSL. Esta protección evita los errores de usuario que hacen que un sitio web no tenga certificados SSL. Si desea eliminar los certificados SSL, póngase en contacto con el servicio de asistencia de Adobe.

En el panel _[!UICONTROL Dominios de marca]_, seleccione el dominio y haga clic en **[!UICONTROL Eliminar]** en la parte superior.
