---
title: Administrar seguimiento de aperturas de correo electrónico
description: Deshabilite el seguimiento de aperturas de correo electrónico de un correo electrónico individual o capture la preferencia de seguimiento de una persona y utilice una ruta dividida para enviar variantes de correo electrónico de seguimiento y sin seguimiento.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
autotag-review: '2026-07-08T00:02:50.497Z'
TQID: 'https://experienceleague.adobe.com/LIutoajlpVQTeJP2y4i0Wv7H-WqGj-c-LVsOGfin384'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: e666e996-b2cf-4c45-8fc2-1c625212ababid: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 61481d57fb8eca805d9a9bc545124aed568b5416
workflow-type: tm+mt
source-wordcount: 860
ht-degree: 0%

---

# Administrar seguimiento de aperturas de correo electrónico

Puede deshabilitar el seguimiento de aperturas para un correo electrónico individual o capturar las preferencias de seguimiento de cada persona en Adobe Experience Platform y utilizar una ruta dividida para dirigir a las personas a las variantes de correo electrónico de seguimiento y sin seguimiento.

>[!BEGINSHADEBOX &quot;Guía CNIL sobre píxeles de seguimiento de correo electrónico&quot;]

El 14 de abril de 2026, la *Comisión Nacional de Informática y Libertades* (CNIL) publicó una [recomendación sobre el uso de píxeles de seguimiento en correos electrónicos](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). La guía aclara cuándo se requiere el consentimiento y resalta la importancia de las prácticas de consentimiento adecuadas para el seguimiento de píxeles del correo electrónico. Esta política podría afectar a las prácticas de envío de cualquier entidad que envíe correos electrónicos a suscriptores con sede en Francia.

Un píxel de seguimiento de correo electrónico es una imagen transparente 1x1 incrustada en el HTML de un correo electrónico. Cuando el cliente de correo electrónico del destinatario carga esa imagen, el píxel hace ping a un servidor que registra datos como una marca de tiempo, un tipo de dispositivo, un cliente de correo electrónico y, a veces, una dirección IP para obtener una ubicación aproximada. A continuación, ese registro se vincula al registro de un destinatario, lo que permite a los especialistas en marketing saber si se abre un correo electrónico.

Las funcionalidades del producto [!UICONTROL Journey Optimizer B2B edition] que se describen aquí son componentes básicos que, configurados y operados correctamente, pueden admitir una implementación compatible. Cada cliente es responsable de determinar y cumplir con sus obligaciones según la ley aplicable.

>[!ENDSHADEBOX]

## Deshabilitar el seguimiento de un solo correo electrónico {#disable-tracking-single-email}

Utilice esta opción cuando desee que un correo electrónico específico nunca informe de una actividad abierta, independientemente de quién la reciba.

1. En las propiedades del nodo de recorrido, a la derecha, abra el correo electrónico.

1. En las propiedades del correo electrónico, seleccione la casilla de verificación **[!UICONTROL Deshabilitar seguimiento de aperturas]**.

   ![Deshabilitar el seguimiento de aperturas de correo electrónico](./assets/email-tracking-disable-all.png){width="500" zoomable="yes"}

   Consulte [Definir la configuración de correo electrónico](./add-email.md#define-the-email-settings) para obtener una lista completa de las propiedades de correo electrónico.

## Segmentar personas por preferencia de seguimiento {#segment-people-tracking-preference}

Si desea permitir que cada persona elija si desea que se rastreen las aperturas de su correo electrónico, capture esa preferencia como un atributo de persona en Adobe Experience Platform (AEP). Puede usar este campo en un [formulario de página de aterrizaje](./forms.md) para que sus contactos tengan la oportunidad de excluirse del seguimiento de aperturas de correo electrónico. A continuación, puede utilizar un nodo _Split paths_ en sus recorridos para enrutar las personas que realizan seguimiento y no seguimiento a diferentes variantes de correo electrónico. Esto le permite aceptar una exclusión individual sin deshabilitar el seguimiento abierto para todos.

El flujo de trabajo consta de tres partes:

1. [Agregue un campo personalizado para la preferencia de seguimiento](#add-custom-field-tracking-preference) en AEP y envíe una comunicación de no participación con un vínculo de formulario.
1. [Agregar una ruta dividida para la exclusión de seguimiento](#add-split-path-tracking) en el recorrido.
1. [Configure variantes de correo electrónico de seguimiento y sin seguimiento](#configure-tracking-and-non-tracking-email-variants) para cada ruta.

### Agregar un campo personalizado para las preferencias de seguimiento {#add-custom-field-tracking-preference}

>[!NOTE]
>
>Añadir y asignar campos XDM personalizados es una tarea de administración de Adobe Experience Platform. Póngase en contacto con el administrador de AEP o con el equipo de ingeniería de datos para completar este paso.

1. En AEP, abra el esquema utilizado para su perfil de persona B2B (por ejemplo, _Persona B2B_).

1. En el id. de inquilino, busque o cree un grupo de campos para los campos de administración de consentimiento de su organización (por ejemplo, `consents`).

1. Agregue un campo al grupo de campos, como un campo booleano denominado `emailTracking`, para representar si la persona ha aceptado abrir el seguimiento.

1. Escriba el nombre del campo y el nombre para mostrar, establezca el tipo, asígnelo al grupo de campos y haga clic en **[!UICONTROL Aplicar]**.

1. Haga clic en **[!UICONTROL Guardar]** para guardar los cambios de esquema.

   ![Agregar el campo emailTracking al grupo de campos de consentimiento de esquema de AEP](./assets/email-tracking-xdm-field-aep-schema.png){width="800" zoomable="yes"}

1. Haga que el campo esté disponible en [!DNL Journey Optimizer B2B Edition] seleccionándolo como _campo administrado_ para la clase [!UICONTROL XDM Individual Profile] en [XDM field management](../admin/xdm-field-management.md#managed-fields).

   ![Seleccione emailTracking como campo administrado en la administración de campos XDM](./assets/email-tracking-xdm-field-select.png){width="450"}

   Esto hace que el campo esté disponible como condición en los nodos de ruta dividida.

### Adición de una ruta dividida para el seguimiento de la exclusión {#add-split-path-tracking}

Agregue [_Rutas divididas por personas_ nodo](../journeys/split-merge-paths-nodes.md#split-paths-by-people) al recorrido y defina una ruta para cada valor de preferencia de seguimiento.

1. Agregue un nodo **[!UICONTROL Split paths]** y elija **[!UICONTROL Personas]** para la división.

1. Para la primera ruta, aplique una condición utilizando su campo de preferencia de seguimiento personalizado (por ejemplo, `emailTracking` es `true`) para identificar a las personas que permiten el seguimiento de aperturas.

   ![Condición de ruta dividida: agregue el campo de seguimiento de correo electrónico como verdadero](./assets/email-tracking-condition-true.png){width="700" zoomable="yes"}

1. Agregue una segunda ruta y aplique la condición inversa (`emailTracking` es `false`) para identificar a las personas que excluyeron el seguimiento.

   Para ver los pasos generales para agregar rutas, aplicar condiciones y reordenar rutas, consulte [Agregar una ruta dividida por el nodo de personas](../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node).

   ![Dividir ruta por personas: seguimiento de correo electrónico activado y desactivado](./assets/email-tracking-split-paths.png){width="500" zoomable="yes"}

### Configurar variantes de correo electrónico de seguimiento y sin seguimiento {#configure-tracking-and-non-tracking-email-variants}

Agregue un nodo de acción [_[!UICONTROL Enviar correo electrónico ]_](./add-email.md) a cada ruta para que cada persona reciba la variante de correo electrónico que coincida con su preferencia de seguimiento.

1. En la ruta habilitada para el seguimiento, agrega una acción **[!UICONTROL Enviar correo electrónico]** y selecciona o crea el correo electrónico de la forma habitual, dejando **[!UICONTROL Deshabilitar el seguimiento de aperturas]** borrado en las propiedades del correo electrónico.

1. En la ruta de exclusión, agregue una acción **[!UICONTROL Enviar correo electrónico]** con el mismo correo electrónico o un correo electrónico duplicado y, a continuación, seleccione la casilla de verificación **[!UICONTROL Deshabilitar el seguimiento de aperturas]** en las propiedades de correo electrónico a la derecha.

   ![Correo electrónico para el seguimiento de la ruta de acceso - deshabilitar el seguimiento de aperturas](./assets/email-tracking-disable.png){width="600" zoomable="yes"}

1. [Publicación del recorrido](../journeys/create-publish-journey.md#publish-a-journey).

   Las personas se dirigen automáticamente a la variante de correo electrónico que coincida con el valor de su campo de preferencia de seguimiento y cualquier actualización que realicen en su preferencia se reflejará la próxima vez que entren en el recorrido.
