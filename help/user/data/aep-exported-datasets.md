---
title: Conjuntos de datos de Experience Platform exportados
description: Referencia para los nombres de los conjuntos de datos de Adobe Experience Platform y las rutas de campo clave exportadas por Adobe Journey Optimizer B2B Edition.
feature: Setup, Data Management
role: Admin
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
autotag-review: '2026-09-29T00:00:00.000Z'
source-git-commit: 801025ee02617d56fc8ab933b59385bca38f5097
workflow-type: tm+mt
source-wordcount: '4845'
ht-degree: 7%
---

# Se exportaron [!DNL Experience Platform] conjuntos de datos

[!DNL Adobe Journey Optimizer B2B Edition] hace que la información de cuenta, persona, grupo de compra y recorrido esté disponible en [!DNL Adobe Experience Platform]. Un conjunto de datos es una colección de registros relacionados. Por ejemplo, un conjunto de datos de persona describe a las personas, un conjunto de datos de pertenencia conecta a las personas con cuentas o recorridos y un conjunto de datos de evento registra acciones como abrir un correo electrónico.

Utilice esta guía para comprender qué contiene cada conjunto de datos, qué significan sus campos y cómo se conectan los registros relacionados. Los nombres de conjuntos de datos siguen este patrón:

**`AJOB2B-<datasetVersion>-<entity>`**

Aquí, `<entity>` describe la información, como `person`, `account_relational` o `person_event`. `<datasetVersion>` identifica la versión de las definiciones de campo del conjunto de datos. Los encabezados de sección muestran los nombres documentados; es posible que el entorno [!DNL Experience Platform] también contenga versiones anteriores.

Para el espacio de nombres y la configuración de esquema que admite estas exportaciones, vea [Esquemas y áreas de nombres B2B](./namespaces-schemas.md).

>[!NOTE]
>
>Adobe conserva las versiones de conjuntos de datos más antiguas para evitar interrumpir el uso existente. Como resultado, es posible que encuentre varias versiones del mismo conjunto de datos en su zona protegida. Si ya no utiliza un conjunto de datos antiguo, puede solicitar a Adobe que lo elimine. Antes de solicitar la eliminación, confirme que el conjunto de datos ya no está en uso.

## Leer esta guía

- **Nombre de campo:** el nombre exacto que ve en [!DNL Experience Platform]. Los puntos separan los niveles dentro de un campo, como `consents.marketing.email.val`.
- **Id. de registro:** identifica el registro de ese conjunto de datos.
- **Relación:** nombra el conjunto de datos y el campo con los que coincide el identificador. Por ejemplo, `Matches AJOB2B-1_5_4-buying_group (_id)` significa que el campo hace referencia al `_id` de un grupo comprador. Coincida con el identificador completo; no lo acorte ni intente reconstruirlo.
- **Formato estándar de Adobe:** usa definiciones de campo compartido de Adobe.
- **Formato de registro relacionado:** organiza la información como registros que se pueden conectar mediante identificadores coincidentes.

Por ejemplo, `buying_group_member.buyingGroupID` coincide con `buying_group._id`, y su `personID` coincide con `person_relational._id` o el `personKey.sourceKey` del conjunto de datos de persona. Estos vínculos le ayudan a comprender quién pertenece a un grupo comprador. [!DNL Experience Platform] no crea automáticamente informes o audiencias solamente a partir de los vínculos.

Algunos identificadores hacen referencia a información que no tiene conjuntos de datos independientes en esta guía, como un programa de marketing. La columna Relación indica esto en lugar de nombrar un conjunto de datos que no existe aquí.

`isDeleted` es `true` cuando el registro se marca como eliminado y `false` cuando no lo es. No lo trate como un miembro activo general o indicador de consentimiento. `lastUpdatedDate` describe la última actualización de datos del registro; para los eventos, use `timestamp` para saber cuándo se produjo la actividad. Un campo en blanco significa que la información no está disponible o no se aplica a ese registro.

Los conjuntos de datos de registros relacionados utilizan la versión `1_5_4`. Cuando un campo no se rellena actualmente o necesita una administración especial, la sección correspondiente explica la limitación visible para el cliente.

Una audiencia es un grupo de personas que cumplen los criterios seleccionados. La disponibilidad para la creación de audiencias depende de la configuración de [!DNL Experience Platform] para combinar información en perfiles de persona. La presencia de un conjunto de datos en [!DNL Experience Platform] no significa, por sí sola, que esté disponible para la segmentación.

## Elección de un conjunto de datos

| Lo que desea comprender | Conjuntos de datos que buscar |
|---|---|
| Personas y sus preferencias de correo electrónico | `person` |
| Detalles de la cuenta y datos de contacto de la persona | `account_relational`, `person_relational` |
| Qué personas están asociadas a una cuenta | `account_member`, `account_person` |
| Cambios de estado, miembros y grupos compradores | `buying_group`, `buying_group_member`, `buying_group_event` |
| Recorridos de cuenta y cuentas participantes | `account_journey`, `account_journey_member`, `account_event` |
| Recorridos de personas y personas participantes | `person_journey`, `person_journey_member` |
| Pasos dentro de un recorrido | `account_journey_node`, `person_journey_node`, `journey_node` |
| Correo electrónico, web y otras actividades de personas admitidas | `person_event`, `person_event_relational` |

Las secciones siguientes proporcionan los nombres completos del conjunto de datos y los detalles del campo. Un recorrido describe la experiencia general; una pertenencia conecta a una persona o cuenta con ese recorrido; un evento describe algo que ha sucedido.

+++Diagrama de relación de entidad

![Diagrama de relación de entidad para conjuntos de datos exportados a [!DNL Adobe Experience Platform]](./assets/ajo-b2b-data-model.svg)

+++

## `AJOB2B-1_5_1-person`

Cada registro describe a una persona, sus identificadores y sus preferencias de marketing por correo electrónico. Utilícela para la creación de informes de nivel de persona y, cuando el perfil esté configurado, para ayudar a crear audiencias.

**Formato:** Formato Adobe estándar

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `personID` | Identificación de registro | Identificador de la persona. Utilice el valor completo para hacer coincidir registros relacionados. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `identityMap` |  | Otros identificadores que ayudan a [!DNL Experience Platform] a reconocer a la misma persona en los datos conectados. |
| `consents.marketing.email.val` |  | Preferencia de marketing por correo electrónico: `n` indica una exclusión; `y` indica que no se ha registrado ninguna exclusión en este campo. Este campo por sí solo no establece permisos para enviar correos electrónicos de marketing. |
| `consents.marketing.email.time` |  | Fecha y hora en que se actualizó la preferencia de correo electrónico por última vez. |
| `consents.marketing.email.reason` |  | Razón de la exclusión, cuando se proporciona (solo se establece al cancelar la suscripción). |
| `isDeleted` |  | Si este registro de persona está marcado como eliminado. |

>[!NOTE]
>
>Su organización puede tener campos de persona adicionales más allá de los enumerados aquí.

Cuando su organización utiliza sus propios conjuntos de datos de cuenta o persona configurados, esos registros también pueden incluir `isDeleted`. Consulte [Conjuntos de datos de propiedad del cliente](#customer-owned-datasets).

## `AJOB2B-1_5_4-account_member`

Cada registro vincula una cuenta a una persona. Utilice este conjunto de datos para informar de qué personas están asociadas a cada cuenta; describe la relación en lugar de cualquiera de los perfiles.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de relación. |
| `accountID` | Coincide con `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de cuenta. |
| `personID` | Coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de persona. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-buying_group`

Cada registro describe un grupo de compra asociado a una cuenta, incluido su nombre, estado, interés de la solución y puntuaciones de participación e integridad. La fase de grupo de compra no está rellenada actualmente.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Id. de registro de grupo de compra (usar el valor completo). |
| `buyingGroupName` |  | Nombre del grupo comprador. |
| `engagementScore` |  | Puntuación de participación. |
| `completenessScore` |  | Puntuación de integridad. |
| `accountID` | Coincide con `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de cuenta relacionado. |
| `solutionInterest` |  | Etiqueta de interés de solución. |
| `buyingGroupStatus` |  | Estado. |
| `buyingGroupStage` |  | Nombre de la fase del grupo de compra. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

>[!NOTE]
>
>**Nota de disponibilidad:** `buyingGroupStage` está actualmente en blanco. No lo utilice para filtrar o agrupar grupos de compra por fase.

## `AJOB2B-1_5_4-buying_group_member`

Cada registro vincula a una persona con un grupo comprador y registra la función de esa persona. Utilícelo para informar sobre la composición del grupo de compra y la cobertura de funciones.

`isDeleted` no siempre indica si una persona ha sido eliminada de un grupo comprador. No utilice este campo solo para determinar la pertenencia actual. El nombre de la función puede estar en blanco cuando no hay información sobre la función disponible.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de pertenencia. |
| `buyingGroupID` | Coincide con `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador del grupo de compra. |
| `personID` | Coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de persona. |
| `buyingGroupMemberRole` |  | Nombre de la función, cuando esté disponible. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-account_journey`

Cada registro describe un recorrido de cuenta, con su nombre, estado y fechas de inicio y finalización. Utilícela para informar sobre el ciclo de vida y el estado de los recorridos de las cuentas.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | id de registro de recorrido (usar el valor completo). |
| `accountJourneyName` |  | nombre del recorrido. |
| `accountJourneyStatus` |  | Estado (por ejemplo, borrador, activo o terminado). |
| `startDate` |  | Marca de tiempo de inicio. |
| `endDate` |  | Marca de hora final. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-account_journey_member`

Cada registro conecta una cuenta con un recorrido de cuentas. Utilícela para identificar e informar sobre qué cuentas participan en cada recorrido.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de pertenencia. |
| `accountID` | Coincide con `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de cuenta. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador del recorrido de la cuenta. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-person_journey`

Cada registro describe el recorrido de una persona, con su nombre, estado y fechas de inicio y finalización. Utilícelo para informar sobre el ciclo de vida y el estado de los recorridos de los recorridos centrados en la persona.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | id de registro de recorrido (usar el valor completo). |
| `personJourneyName` |  | nombre del recorrido. |
| `personJourneyStatus` |  | Estado (por ejemplo, borrador, activo o terminado). |
| `startDate` |  | Marca de tiempo de inicio. |
| `endDate` |  | Marca de hora final. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-person_journey_member`

En cada registro se describe la pertenencia de una persona a un recorrido, incluido el nodo de recorrido actual, las fechas de pertenencia y de entrada y el recuento de entradas. Utilícelo para informar sobre el progreso de inscripción, reentrada y recorrido.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de pertenencia. |
| `marketingProgramID` |  | Identificador del programa de marketing al que pertenece el recorrido. |
| `personID` | Coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de persona. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador del nodo de recorrido en el que se encuentra actualmente la persona. |
| `membershipDate` |  | Cuando la persona se convirtió en miembro del programa de marketing. |
| `lastEntryDate` |  | La última vez que la persona entró en el recorrido. |
| `reentryOpensAt` |  | Cuando la persona puede volver a entrar en el recorrido. |
| `entryCount` |  | Recuento de veces que la persona ha entrado en el recorrido. |
| `createdDate` |  | Cuando se creó el registro. |
| `updatedDate` |  | La última vez que se cambió el registro. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-account_journey_node`

Cada registro describe un paso de un recorrido, incluido el tipo de paso y el recorrido al que pertenece. Un nodo de recorrido es un paso como inicio, espera o decisión. Los mismos pasos pueden aparecer en `person_journey_node`; haga coincidir `accountJourneyID` con un recorrido de cuenta antes de tratar un paso como específico de la cuenta.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de nodo (utilice el valor completo). |
| `accountJourneyID` | Coincide con `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador del recorrido principal. |
| `uuid` |  | Identificador adicional para el paso de recorrido. |
| `journeyNodeTypeID` |  | Número que identifica el tipo de paso de recorrido. |
| `nodeType` |  | Etiqueta que identifica el tipo de paso de recorrido. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `createdDate` |  | Cuando se creó el registro. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-person_journey_node`

Cada registro describe un paso de un recorrido, incluido el tipo de paso y el recorrido al que pertenece. Los mismos pasos pueden aparecer en `account_journey_node`; asigne `personJourneyID` a un recorrido de persona antes de tratar un paso como específico de la persona.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de nodo (utilice el valor completo). |
| `personJourneyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador del recorrido principal. |
| `uuid` |  | Identificador adicional para el paso de recorrido. |
| `journeyNodeTypeID` |  | Número que identifica el tipo de paso de recorrido. |
| `nodeType` |  | Etiqueta que identifica el tipo de paso de recorrido. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `createdDate` |  | Cuando se creó el registro. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-account_event`

Cada registro captura un evento de recorrido de cuenta: una cuenta que se agrega o elimina de un recorrido o que se mueve entre nodos de recorrido. Use `eventType` y `timestamp` para crear una escala de tiempo de actividad de la cuenta; `buyingGroupID` está disponible cuando el evento se atribuye a un grupo de compra.

**Formato:** Formato de registro relacionado

`eventType` proporciona información sobre lo que ha sucedido. En las tablas siguientes se describen los campos de cada tipo de actividad.

`lastUpdatedDate` no se ha completado para estos eventos. Use `timestamp` para la fecha de la actividad.

### Cuenta agregada a un recorrido (`account.addAccountToJourney`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `account.addAccountToJourney`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `accountID` | Coincide con `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de cuenta. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificador del nodo de recorrido. |
| `buyingGroupID` | Coincide con `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador del grupo de compra, cuando el recorrido añadido es un grupo de compra atribuido. |
| `lastUpdatedDate` |  | Registrar tiempo de actualización. Actualmente en blanco; utilice la marca de tiempo para la fecha de la actividad. |

### Cuenta eliminada de un recorrido (`account.removeAccountFromJourney`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `account.removeAccountFromJourney`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `accountID` | Coincide con `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de cuenta. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificador del nodo de recorrido. |
| `buyingGroupID` | Coincide con `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador del grupo de compra, cuando la eliminación de recorridos está atribuida a un grupo de compra. |
| `lastUpdatedDate` |  | Registrar tiempo de actualización. Actualmente en blanco; utilice la marca de tiempo para la fecha de la actividad. |

### La cuenta se movió entre los pasos del recorrido (`account.changeAccountJourneyNode`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `account.changeAccountJourneyNode`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `accountID` | Coincide con `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de cuenta. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-account_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-account_journey_node` (`_id`) | Identificador del nodo de recorrido. |
| `previousJourneyNodeID` | Hace referencia a `AJOB2B-1_5_4-account_journey_node` (`_id`); los valores pueden no coincidir | Identificador del paso de recorrido anterior. Es posible que este valor no coincida con el registro de paso correspondiente; no confíe solo en él para conectar registros. |
| `buyingGroupID` | Coincide con `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador del grupo de compra, cuando el cambio de nodo se atribuye al grupo de compra. |
| `lastUpdatedDate` |  | Registrar tiempo de actualización. Actualmente en blanco; utilice la marca de tiempo para la fecha de la actividad. |

## `AJOB2B-1_5_4-buying_group_event`

Cada registro registra un cambio en el estado de un grupo comprador, incluido el nuevo estado y cuándo ha cambiado. El campo de nueva etapa no está rellenado actualmente.

**Formato:** Formato de registro relacionado

### Se cambió el estado del grupo de compra (`buyingGroup.changeStatus`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `buyingGroup.changeStatus`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `buyingGroupID` | Coincide con `AJOB2B-1_5_4-buying_group` (`_id`) | Identificador del grupo de compra. |
| `newStatus` |  | Nuevo valor de estado. |
| `newStage` |  | Nueva fase de compra-grupo. Actualmente en blanco. |
| `lastUpdatedDate` |  | Registrar tiempo de actualización. |

>[!NOTE]
>
>**Nota de disponibilidad:** use `newStatus` para informar de los cambios de estado. No use `newStage` para informar de cambios de etapa, ya que actualmente está en blanco.

## `AJOB2B-1_5-person_event`

Cada registro describe un evento web, de correo electrónico u otra actividad compatible a nivel de persona. Use `eventType` y `timestamp` para analizar el comportamiento a lo largo del tiempo, con detalles específicos de evento rellenados únicamente para el tipo de evento coincidente.

**Formato:** Formato Adobe estándar

`eventType` le informa sobre lo sucedido. En las tablas siguientes se describen los campos de cada tipo de actividad. Los detalles que no se aplican a un evento están en blanco.

### Correo electrónico enviado (`directMarketing.emailSent`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `directMarketing.emailSent`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `directMarketing.emailSent.mailingKey.sourceID` |  | ID del recurso de correo. |
| `directMarketing.emailSent.mailingKey.sourceType` |  | Nombre del producto conectado. |
| `directMarketing.emailSent.mailingKey.sourceInstanceID` |  | ID de instancia. |
| `directMarketing.emailSent.mailingKey.sourceKey` |  | Identificador completo del contenido del correo electrónico. |
| `directMarketing.emailSent.mailingName` |  | Nombre de correo. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |

### Correo electrónico enviado (`directMarketing.emailDelivered`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `directMarketing.emailDelivered`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID del recurso de correo. |
| `directMarketing.mailingKey.sourceType` |  | Nombre del producto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID de instancia. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo del contenido del correo electrónico. |
| `directMarketing.mailingName` |  | Nombre de correo. |
| `directMarketing.email` |  | Correo electrónico. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |

### Cancelar suscripción de correo electrónico (`directMarketing.emailUnsubscribed`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `directMarketing.emailUnsubscribed`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID del recurso de correo. |
| `directMarketing.mailingKey.sourceType` |  | Nombre del producto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID de instancia. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo del contenido del correo electrónico. |
| `directMarketing.mailingName` |  | Nombre de correo. |
| `directMarketing.email` |  | Correo electrónico. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |

### Correo electrónico abierto (`directMarketing.emailOpened`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `directMarketing.emailOpened`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID del recurso de correo. |
| `directMarketing.mailingKey.sourceType` |  | Nombre del producto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID de instancia. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo del contenido del correo electrónico. |
| `directMarketing.mailingName` |  | Nombre de correo. |
| `directMarketing.email` |  | Correo electrónico. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |
| `device.isMobileDevice` |  | Si se ha registrado un dispositivo móvil para la actividad. |
| `device.model` |  | Información del dispositivo o del cliente de correo electrónico. |
| `environment.browserDetails.userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `environment.operatingSystem` |  | Sistema operativo. |

### Vínculo de correo electrónico donde se hizo clic (`directMarketing.emailClicked`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `directMarketing.emailClicked`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID del recurso de correo. |
| `directMarketing.mailingKey.sourceType` |  | Nombre del producto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID de instancia. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo del contenido del correo electrónico. |
| `directMarketing.mailingName` |  | Nombre de correo. |
| `directMarketing.email` |  | Correo electrónico. |
| `directMarketing.linkURL` |  | URL de vínculo seleccionada. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |
| `device.isMobileDevice` |  | Si se ha registrado un dispositivo móvil para la actividad. |
| `device.model` |  | Información del dispositivo o del cliente de correo electrónico. |
| `environment.browserDetails.userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `environment.operatingSystem` |  | Sistema operativo. |

### Correo electrónico rechazado (`directMarketing.emailBounced`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `directMarketing.emailBounced`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID del recurso de correo. |
| `directMarketing.mailingKey.sourceType` |  | Nombre del producto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID de instancia. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo del contenido del correo electrónico. |
| `directMarketing.mailingName` |  | Nombre de correo. |
| `directMarketing.email` |  | Correo electrónico. |
| `directMarketing.emailBouncedCode` |  | Categoría/código de rechazo. |
| `directMarketing.emailBouncedDetails` |  | Texto detallado. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |

### Rechazo suave de correo electrónico (`directMarketing.emailBouncedSoft`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `directMarketing.emailBouncedSoft`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `directMarketing.mailingKey.sourceID` |  | ID del recurso de correo. |
| `directMarketing.mailingKey.sourceType` |  | Nombre del producto conectado. |
| `directMarketing.mailingKey.sourceInstanceID` |  | ID de instancia. |
| `directMarketing.mailingKey.sourceKey` |  | Identificador completo del contenido del correo electrónico. |
| `directMarketing.mailingName` |  | Nombre de correo. |
| `directMarketing.email` |  | Correo electrónico. |
| `directMarketing.emailBouncedCode` |  | Categoría/código de rechazo. |
| `directMarketing.emailBouncedDetails` |  | Texto detallado. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |

### Página web vista (`web.webpagedetails.pageViews`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `web.webpagedetails.pageViews`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `web.webPageDetails.webPageKey.sourceID` |  | ID del recurso de página. |
| `web.webPageDetails.webPageKey.sourceType` |  | Nombre del producto conectado. |
| `web.webPageDetails.webPageKey.sourceInstanceID` |  | ID de instancia. |
| `web.webPageDetails.webPageKey.sourceKey` |  | Identificador de página completo. |
| `web.webPageDetails.name` |  | Nombre de página. |
| `web.webPageDetails.URL` |  | URL de página. |
| `web.webPageDetails.queryParameters` |  | Información adicional incluida en una dirección web. |
| `web.webPageDetails.webPageID` |  | ID de página. |
| `environment.browserDetails.userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `web.webReferrer.URL` |  | URL de referente. |

### Vínculo web en el que se hizo clic (`web.webinteraction.linkClicks`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `web.webinteraction.linkClicks`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `web.webInteraction.webInteractionKey.sourceID` |  | ID del recurso de interacción. |
| `web.webInteraction.webInteractionKey.sourceType` |  | Nombre del producto conectado. |
| `web.webInteraction.webInteractionKey.sourceInstanceID` |  | ID de instancia. |
| `web.webInteraction.webInteractionKey.sourceKey` |  | Identificador de interacción completo. |
| `web.webInteraction.linkID` |  | ID del vínculo. |
| `web.webInteraction.linkURL` |  | URL de destino. |
| `web.webPageDetails.queryParameters` |  | Información adicional incluida en una dirección web. |
| `web.webPageDetails.webPageID` |  | ID de página. |
| `environment.browserDetails.userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `web.webReferrer.URL` |  | URL de referente. |

### Formulario enviado (`web.formFilledOut`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `web.formFilledOut`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `web.fillOutForm.webFormKey.sourceID` |  | ID del recurso de formulario. |
| `web.fillOutForm.webFormKey.sourceType` |  | Nombre del producto conectado. |
| `web.fillOutForm.webFormKey.sourceInstanceID` |  | ID de instancia. |
| `web.fillOutForm.webFormKey.sourceKey` |  | Identificador del formulario completo. |
| `web.fillOutForm.webFormID` |  | ID del formulario. |
| `web.fillOutForm.webFormName` |  | Nombre del formulario. |
| `web.webPageDetails.queryParameters` |  | Información adicional incluida en una dirección web. |
| `web.webPageDetails.webPageID` |  | ID de página. |
| `environment.browserDetails.userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `web.webReferrer.URL` |  | URL de referente. |

### Momento interesante registrado (`leadOperation.interestingMoment`)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de actividad. |
| `eventType` |  | `leadOperation.interestingMoment`. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `personID` | Coincide con `AJOB2B-1_5_1-person` (`personID`) | Identificador de persona. |
| `personKey.sourceID` |  | Identificador de persona en el sistema conectado. |
| `personKey.sourceType` |  | Nombre del producto conectado. |
| `personKey.sourceInstanceID` |  | Identificador del entorno [!DNL Experience Platform] o cuenta conectada. |
| `personKey.sourceKey` |  | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `leadOperation.interestingMoment.date` |  | Fecha y hora del momento. |
| `leadOperation.interestingMoment.description` |  | Descripción |
| `leadOperation.interestingMoment.source` |  | Nombre del producto o campaña relacionado. |
| `leadOperation.interestingMoment.type` |  | Escriba la etiqueta. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | id de recorrido (si se atribuye). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | id del nodo de recorrido (si se atribuye). |

## `AJOB2B-1_5_4-journey_node`

Cada registro describe un paso de recorrido, el recorrido al que pertenece y el tipo de paso. Los mismos pasos pueden aparecer en los conjuntos de datos de pasos de recorrido de cuentas y personas. Hacer coincidir `journeyID` con el recorrido apropiado; no cuente un paso más de una vez porque aparece en varios conjuntos de datos.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de nodo (utilice el valor completo). |
| `journeyID` | Coincide con `AJOB2B-1_5_4-account_journey` o `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador del recorrido principal. |
| `nodeType` |  | Tipo de paso de recorrido, como inicio, fin, espera o decisión. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-account_relational`

Cada registro describe una cuenta, incluidos los detalles de su organización, ubicación, tamaño, ingresos y campos personalizados. Utilice esta información para añadir contexto de cuenta a informes de recorridos y de grupos de compras.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID del registro de cuenta (utilice el valor completo). |
| `accountName` |  | Nombre de la cuenta. |
| `industry` |  | Clasificación del sector. |
| `country` |  | País. |
| `sicCode` |  | Código de clasificación industrial estándar. |
| `domainName` |  | Dominio web principal. |
| `primaryEmailDomain` |  | Dominio de correo electrónico principal. |
| `street` |  | Dirección de la calle. |
| `city` |  | Ciudad. |
| `state` |  | Estado o región. |
| `postalCode` |  | Código postal. |
| `region` |  | Región geográfica. |
| `phoneNumber` |  | Número de teléfono. |
| `logoUrl` |  | URL del logotipo de la cuenta. |
| `annualRevenue` |  | Ingresos anuales. |
| `numberOfEmployees` |  | Número de empleados. |
| `createdDate` |  | Cuando se creó el registro. |
| `sourceType` |  | Nombre del sistema conectado que identifica la cuenta. |
| `sourceInstanceID` |  | Identificador de su organización o cuenta en ese sistema conectado. |
| `sourceID` |  | Identificador de cuenta en ese sistema conectado. |
| `customAttributes` |  | Los nombres y valores de los campos personalizados se almacenan juntos como texto. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-person_relational`

Cada registro describe a una persona, incluida su información de contacto, detalles de trabajo, identificadores y campos personalizados. Utilícelo para agregar información de la persona a los informes de pertenencia, recorrido y actividad.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador completo de la persona utilizado para hacer coincidir registros relacionados. |
| `email` |  | Correo electrónico. |
| `firstName` |  | Nombre. |
| `middleName` |  | Segundo nombre. |
| `lastName` |  | Apellido... |
| `jobTitle` |  | Título del trabajo. |
| `personType` |  | Tipo de persona: contacto, cliente potencial o cliente potencial pendiente. |
| `isLead` |  | Si la persona es un posible cliente. |
| `isAnonymous` |  | Si la persona es anónima. |
| `salutation` |  | Saludo o honorífico. |
| `phone` |  | Número de teléfono principal. |
| `mobile` |  | Número de teléfono móvil. |
| `sourceType` |  | Nombre del sistema conectado que identifica a la persona, como [!DNL Marketo Engage]. |
| `sourceInstanceID` |  | Identificador de su organización o cuenta en ese sistema conectado. |
| `sourceID` |  | Identificador de persona en ese sistema conectado. |
| `identityNamespace` |  | Etiqueta que identifica el tipo de identificador de persona adicional. |
| `identityValue` |  | Valor de la identidad secundaria. |
| `customAttributes` |  | Los nombres y valores de los campos personalizados se almacenan juntos como texto. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-account_person`

Cada registro vincula un perfil de cuenta a un perfil de persona. Utilícela para informar sobre relaciones entre los conjuntos de datos de cuenta y perfil de persona.

**Formato:** Formato de registro relacionado

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | ID de registro de relación cuenta-persona (utilice el valor completo). |
| `accountID` | Coincide con `AJOB2B-1_5_4-account_relational` (`_id`) | Identificador de cuenta completo (referencias `account_relational._id`). |
| `personID` | Coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de persona completo (referencias `person_relational._id`). |
| `createdDate` |  | Cuando se creó la relación cuenta-persona. |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

## `AJOB2B-1_5_4-person_event_relational`

Cada registro describe una actividad de persona admitida, como ver una página web, interactuar con un correo electrónico o desplazarse por un recorrido. Use `eventType` y `activityTypeID` para comprender lo que ha sucedido. Solo se rellenan los detalles relevantes para ese tipo de actividad.

**Formato:** Formato de registro relacionado

La siguiente lista de campos abarca todos los tipos de actividades compatibles. Un registro individual contiene únicamente los detalles aplicables a su actividad.

>[!NOTE]
>
>**Disponibilidad:** algunas actividades pueden tener `_id` en blanco. No suponga que cada actividad tiene un identificador de registro utilizable. El conjunto de datos no garantiza un historial de actividad completo.

Se han proporcionado detalles de recorrido (`journeyID`, `journeyNodeID`, `journeyStepID` y campos similares) para las actividades de recorrido (`person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`) y para las actividades de `person.attributeChanged` asociadas con un paso de recorrido de &quot;Actualizar perfil de persona&quot;.

Los campos de cambio de atributo (`attributeName`, `attributeID`, `attributeNewValue`, `attributeOldValue`, `attributeChangeReason`) solo se rellenan para `person.attributeChanged`.

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id` | Identificación de registro | Identificador de la actividad, cuando está disponible. |
| `timestamp` |  | Cuando se produjo la actividad. |
| `eventType` |  | Etiqueta de actividad. Valores: `web.webpagedetails.pageViews`, `web.formFilledOut`, `web.webinteraction.linkClicks`, `directMarketing.emailSent`, `directMarketing.emailDelivered`, `directMarketing.emailBounced`, `directMarketing.emailBouncedSoft`, `directMarketing.emailUnsubscribed`, `directMarketing.emailOpened`, `directMarketing.emailClicked`, `leadOperation.interestingMoment`, `person.attributeChanged`, `person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`. |
| `activityTypeID` |  | Código de actividad. Utilícelo con `eventType` para distinguir las actividades que comparten la misma etiqueta de evento. |
| `personID` | Coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Identificador de persona completo utilizado para hacer coincidir la actividad con el registro de una persona. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de recorrido completo. En blanco para actividades no asociadas a un recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador completo del paso del recorrido. En blanco para actividades no asociadas a un recorrido. |
| `previousJourneyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo de recorrido anterior (completado para `person.journeyNodeTransition` y `person.journeySplitNode`). |
| `newJourneyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Id. del nodo de recorrido de destino (`person.journeyNodeTransition` y `person.journeySplitNode`). Normalmente es igual a `journeyNodeID`. |
| `journeyStepID` |  | Identificador del paso de recorrido asociado con la actividad. |
| `journeyChoiceNumber` |  | Número de selección dividida para `person.journeySplitNode`. Se registra como un número entero. |
| `journeyEntryCount` |  | Número de veces que esta persona ha entrado en el recorrido (rellenado en los eventos de adición/inicio del recorrido). Se registra como un número entero. |
| `journeyProgramID` | No hay ningún conjunto de datos de programa de marketing independiente en esta guía | Identificador del programa de marketing asociado a la actividad de recorrido. |
| `activitySource` |  | Nombre del producto o acción asociado con la actividad. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña cuando la actividad se atribuye a una campaña. |
| `attributeName` |  | Nombre del campo que cambió (`person.attributeChanged` solamente). |
| `attributeID` |  | Identificador del campo que cambió (`person.attributeChanged` solamente). |
| `attributeNewValue` |  | Nuevo valor de campo, registrado como texto (`person.attributeChanged` solamente). |
| `attributeOldValue` |  | Valor de campo anterior, registrado como texto (`person.attributeChanged` solamente). |
| `attributeChangeReason` |  | Etiqueta de motivo del cambio (`person.attributeChanged` solamente). |
| `assetID` |  | Identificador del contenido, la página o el formulario del correo electrónico relacionado. |
| `assetName` |  | Nombre del contenido relacionado. |
| `recipientEmail` |  | Dirección de correo electrónico del destinatario, cuando esté disponible. Rellenado solamente para los códigos de actividad **27** (mensajes devueltos no entregados) y **48** (mensajes devueltos no entregados de correo electrónico de ventas); en blanco para otras actividades de correo electrónico. Para esas actividades, busque el registro de persona con `personID`. `assetName` identifica el contenido del correo electrónico, no la dirección del destinatario. |
| `bouncedCode` |  | Código de categoría de rechazo (solo emailBounce / emailBounceSoft). |
| `bouncedDetails` |  | Motivo de rechazo detallado (solo emailBounce / emailBounceSoft). |
| `isMobileDevice` |  | Si se ha registrado un dispositivo móvil para una apertura de correo electrónico o un clic. |
| `deviceModel` |  | Modelo de dispositivo (emailOpened/emailClicked solamente). |
| `operatingSystem` |  | Sistema operativo (emailOpened / emailClicked solamente). |
| `userAgent` |  | Información del explorador o del cliente de correo electrónico, para aperturas de correo electrónico, clics en correos electrónicos y actividades web. |
| `clickedLinkUrl` |  | URL de vínculo de correo electrónico donde se hizo clic (solo emailClicked). |
| `webPageUrl` |  | Dirección URL de la página web (`web.webpagedetails.pageViews` solamente). |
| `queryParameters` |  | Información adicional en una dirección web, para vistas de página, envíos de formularios o clics en vínculos web. |
| `webPageID` |  | [!DNL Marketo Engage]: id de página web (pageViews, formFilledOut, linkClicks). |
| `referrerUrl` |  | URL del referente (pageViews, formFilledOut, linkClicks). |
| `formID` |  | [!DNL Marketo Engage] id. de formulario (`web.formFilledOut` solamente). |
| `linkID` |  | [!DNL Marketo Engage] id. de vínculo (`web.webinteraction.linkClicks` solamente). |
| `interestingMomentDate` |  | Fecha del momento (`leadOperation.interestingMoment` solamente). |
| `interestingMomentDescription` |  | Descripción de texto libre (solo interesanteMoment). |
| `interestingMomentSource` |  | Producto o campaña relacionados (solo interesanteMoment). |
| `interestingMomentType` |  | Categoría/tipo (solo interestMoment). |
| `isDeleted` |  | Indica si este registro está marcado como eliminado. |
| `lastUpdatedDate` |  | Hora de la última modificación. |

### Referencia de campo por tipo de actividad

Las siguientes tablas muestran los detalles que se aplican a cada actividad. Otros detalles están en blanco. Algunas actividades comparten la misma etiqueta `eventType`: los códigos 8 y 48 usan `directMarketing.emailBounced`. Use `activityTypeID` para distinguirlos.

#### Página web vista (`web.webpagedetails.pageViews`) (tipo de actividad 1)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de página. |
| `assetName` |  | Nombre de página. |
| `webPageUrl` |  | URL de página. |
| `queryParameters` |  | Información adicional incluida en una dirección web. |
| `webPageID` |  | [!DNL Marketo Engage] id. de página web. |
| `referrerUrl` |  | URL de referente. |
| `userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Formulario enviado (`web.formFilledOut`) (tipo de actividad 2)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID del formulario. |
| `assetName` |  | Nombre del formulario. |
| `formID` |  | [!DNL Marketo Engage] id. de formulario. |
| `queryParameters` |  | Información adicional incluida en una dirección web. |
| `webPageID` |  | [!DNL Marketo Engage] id. de página web. |
| `referrerUrl` |  | URL de referente. |
| `userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Vínculo web en el que se hizo clic (`web.webinteraction.linkClicks`) (tipo de actividad 3)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | Interacción / ID del vínculo. |
| `assetName` |  | URL de destino. |
| `linkID` |  | [!DNL Marketo Engage] id. de vínculo. |
| `queryParameters` |  | Información adicional incluida en una dirección web. |
| `webPageID` |  | [!DNL Marketo Engage] id. de página web. |
| `referrerUrl` |  | URL de referente. |
| `userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Correo electrónico enviado (`directMarketing.emailSent`) (tipos de actividad 6, 39)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Correo electrónico enviado (`directMarketing.emailDelivered`) (tipos de actividad 7, 45)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Cancelar suscripción por correo electrónico (`directMarketing.emailUnsubscribed`) (tipo de actividad 9)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Correo electrónico abierto (`directMarketing.emailOpened`) (tipos de actividad 10, 40)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `isMobileDevice` |  | Si se ha registrado un dispositivo móvil para la actividad. |
| `deviceModel` |  | Modelo de dispositivo. |
| `operatingSystem` |  | Sistema operativo. |
| `userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Vínculo de correo electrónico en el que se hizo clic (`directMarketing.emailClicked`) (tipos de actividad 11, 41)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `clickedLinkUrl` |  | URL de vínculo seleccionada. |
| `isMobileDevice` |  | Si se ha registrado un dispositivo móvil para la actividad. |
| `deviceModel` |  | Modelo de dispositivo. |
| `operatingSystem` |  | Sistema operativo. |
| `userAgent` |  | Información del explorador o del cliente de correo electrónico. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Correo electrónico rechazado (`directMarketing.emailBounced`): rechazo grave (Tipo de actividad 8)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `bouncedCode` |  | Código de categoría de rechazo. |
| `bouncedDetails` |  | Motivo de rechazo detallado. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

Esta actividad comparte la etiqueta `directMarketing.emailBounced` con el código de actividad 48, pero `recipientEmail` está en blanco para el código 8. Use `activityTypeID` para distinguir los dos.

#### Correo electrónico rechazado (`directMarketing.emailBounced`): devolución del mensaje de correo electrónico de ventas (tipo de actividad 48)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `recipientEmail` |  | Dirección de correo electrónico del destinatario |
| `bouncedCode` |  | Código de categoría de rechazo. |
| `bouncedDetails` |  | Motivo de rechazo detallado. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Rechazo suave de correo electrónico (`directMarketing.emailBouncedSoft`) (tipo de actividad 27)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `assetID` |  | ID de correo. |
| `assetName` |  | Nombre de correo. |
| `recipientEmail` |  | Dirección de correo electrónico del destinatario |
| `bouncedCode` |  | Código de categoría de rechazo. |
| `bouncedDetails` |  | Motivo de rechazo detallado. |
| `campaignID` |  | [!DNL Marketo Engage] id. de campaña, cuando se atribuye a la campaña. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Momento interesante registrado (`leadOperation.interestingMoment`) (tipo de actividad 46)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `interestingMomentDate` |  | Fecha y hora del momento. |
| `interestingMomentDescription` |  | Descripción de texto libre. |
| `interestingMomentSource` |  | Nombre del producto o campaña relacionado. |
| `interestingMomentType` |  | Escriba la etiqueta. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

`assetID` y `assetName` no se han rellenado para este tipo de actividad.

#### Campo de persona cambiado (`person.attributeChanged`) (tipo de actividad 13)

Solo se incluye cuando el cambio está asociado a un recorrido, como un paso &quot;Actualizar perfil de persona&quot;. Los cambios fuera de un recorrido no se incluyen.

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `attributeName` |  | Nombre del campo que ha cambiado. |
| `attributeID` |  | Identificador del campo que ha cambiado. |
| `attributeNewValue` |  | Nuevo valor de campo, registrado como texto. |
| `attributeOldValue` |  | Valor del campo anterior, registrado como texto. |
| `attributeChangeReason` |  | Etiqueta de motivo del cambio. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador del nodo de recorrido. |
| `journeyStepID` |  | Identificador del paso de recorrido. |
| `journeyProgramID` | No hay ningún conjunto de datos de programa de marketing independiente en esta guía | id del programa de recorrido. |
| `activitySource` |  | Producto o acción asociados con la actividad. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Persona agregada o que inició un recorrido (`person.journeyAdd`, `person.journeyStart`) (tipos de actividad 182, 184)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador del nodo de recorrido. |
| `journeyStepID` |  | Identificador del paso de recorrido. |
| `journeyEntryCount` |  | Número de veces que esta persona ha entrado en el recorrido. |
| `journeyProgramID` | No hay ningún conjunto de datos de programa de marketing independiente en esta guía | id del programa de recorrido. |
| `activitySource` |  | Producto o acción asociados con la actividad. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Persona eliminada de un recorrido o que finalizó (`person.journeyRemove`, `person.journeyEnd`) (tipos de actividad 183, 185)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador del nodo de recorrido. |
| `journeyStepID` |  | Identificador del paso de recorrido. |
| `journeyProgramID` | No hay ningún conjunto de datos de programa de marketing independiente en esta guía | id del programa de recorrido. |
| `activitySource` |  | Producto o acción asociados con la actividad. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### La persona siguió una rama de recorrido (`person.journeySplitNode`) (tipo de actividad 186)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador del nodo de recorrido (el nodo dividido). |
| `previousJourneyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo en el que se encontraba la persona antes de la división. |
| `newJourneyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo al que se movió la persona (normalmente es igual a `journeyNodeID`). |
| `journeyStepID` |  | Identificador del paso de recorrido. |
| `journeyChoiceNumber` |  | Qué rama de la división se tomó. |
| `journeyProgramID` | No hay ningún conjunto de datos de programa de marketing independiente en esta guía | id del programa de recorrido. |
| `activitySource` |  | Producto o acción asociados con la actividad. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

#### Persona que se movió entre los pasos del recorrido (`person.journeyNodeTransition`) (tipo de actividad 600)

| Nombre del campo | Relación | Lo que te dice |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | Id. de registro: `_id`; `personID` coincide con `AJOB2B-1_5_4-person_relational` (`_id`) | Campos comunes. |
| `journeyID` | Coincide con `AJOB2B-1_5_4-person_journey` (`_id`) | Identificador de recorrido. |
| `journeyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Identificador del nodo de recorrido actual. |
| `previousJourneyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo desde el que la persona realizó la transición. |
| `newJourneyNodeID` | Coincide con `AJOB2B-1_5_4-person_journey_node` (`_id`) | Nodo al que la persona realizó la transición (normalmente es igual a `journeyNodeID`). |
| `journeyStepID` |  | Identificador del paso de recorrido. |
| `journeyProgramID` | No hay ningún conjunto de datos de programa de marketing independiente en esta guía | id del programa de recorrido. |
| `activitySource` |  | Producto o acción asociados con la actividad. |
| `isDeleted`, `lastUpdatedDate` |  | Campos comunes. |

## Conjuntos de datos propiedad del cliente {#customer-owned-datasets}

Su organización puede utilizar sus propios conjuntos de datos de [!DNL Experience Platform] para cuentas o personas. Cuando se configura, [!DNL Adobe Journey Optimizer B2B Edition] puede agregar información a esos conjuntos de datos en lugar de crear otra cuenta o conjunto de datos personal.

Sus nombres y campos disponibles dependen de la configuración de su organización. Utilice la cuenta configurada o el identificador de persona para reconocer los registros coincidentes. Tener registros en estos conjuntos de datos no los hace disponibles automáticamente para las audiencias; la disponibilidad depende de la configuración de [!DNL Experience Platform].
