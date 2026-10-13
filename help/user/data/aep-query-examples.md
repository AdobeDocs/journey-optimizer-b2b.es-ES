---
title: Consultas de conjuntos de datos
description: Aprenda a utilizar ejemplos de consultas SQL en Query Service para analizar datos de cuenta, grupo de compra, persona y recorrido exportados por Adobe Journey Optimizer B2B Edition.
feature: Reporting, Data Management
role: Admin, Developer
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: 6db81a0b993f450a3ff448dcb4c417e3e81ec70a
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%
---

# Consultas de conjuntos de datos

Encuentre ejemplos de consultas SQL listos para usar para analizar los datos de cuenta, persona, grupo de compra y recorrido que [!DNL Adobe Journey Optimizer B2B Edition] exporta a [!DNL Adobe Experience Platform]. Para informar sobre cuentas, grupos de compras, participación por correo electrónico y actividad de recorridos, ejecute las consultas en [!DNL Query Service].

Para obtener descripciones de los conjuntos de datos y los campos utilizados en estas consultas, consulte [Conjuntos de datos exportados](./aep-exported-datasets.md).

## Prerrequisitos {#prerequisites}

Antes de ejecutar cualquier consulta en esta página, asegúrese de que dispone de lo siguiente:

* **Acceso a [!DNL Query Service]:** Debe tener acceso a [Servicio de consultas](https://experienceleague.adobe.com/es/docs/experience-platform/query/home){target="_blank"} en su zona protegida de [!DNL Experience Platform].
* **Conjuntos de datos disponibles:** Las consultas se dirigen a los conjuntos de datos [!DNL Journey Optimizer B2B Edition] exportados. En su zona protegida, vaya a **[!UICONTROL Conjuntos de datos]** y compruebe que los conjuntos de datos existen y contienen datos.
* **Valores de campo de esquema:** Asegúrese de que los campos de las consultas tengan valores en el esquema correspondiente. Los campos vacíos no devuelven resultados y no producen errores.

>[!NOTE]
>
>Los ejemplos utilizan nombres de tabla cortos, como `account_table` y `person_activity_table`. Reemplace cada nombre de tabla con el nombre del conjunto de datos correspondiente en la zona protegida. Si el nombre de un conjunto de datos contiene guiones, escríbalo entre comillas dobles. Reemplace valores de marcador de posición, como `Example Company` y `PASTE_COMPLETE_JOURNEY_ID_HERE`, por valores de su entorno.

## Ejecutar una consulta {#run}

Para ejecutar cualquier ejemplo en esta página:

1. En [!DNL Experience Platform], seleccione **[!UICONTROL Servicio de consultas]** > **[!UICONTROL Consultas]**.
1. Pegue el ejemplo en el editor de consultas y, a continuación, reemplace los nombres de tabla y los valores de marcador de posición.
1. Seleccione **[!UICONTROL Ejecutar]**.

Los ejemplos que filtran por fecha utilizan los últimos 30 días. Para cambiar el intervalo de tiempo, edite el valor `INTERVAL '30' DAY`.

## Elija una consulta

Utilice la siguiente tabla para elegir una consulta para la tarea de creación de informes.

| Quiero... | Ir a |
|---|---|
| Revisar nombres, industrias y ubicaciones de cuentas | [Revisar detalles de la cuenta](#account-details) |
| Comparar grupos de compra por participación | [Comparar la participación del grupo comprador](#buying-group-engagement) |
| Búsqueda de las personas asociadas a una cuenta | [Buscar personas en una cuenta](#account-people) |
| Rastrear cambios en el estado del grupo de compra | [Revisar los cambios de estado del grupo de compra](#buying-group-status-changes) |
| Buscar personas que hicieron clic en un correo electrónico | [Buscar personas que hicieron clic en un correo electrónico](#email-clicks) |
| Comparar actividad reciente por tipo | [Comparar actividad de persona reciente](#person-activity) |
| Comparar recorridos de cuenta por tamaño | [Comparar recuentos de cuentas por recorrido](#account-journey-counts) |
| Enumeración de las cuentas en un recorrido | [Enumerar cuentas en un recorrido](#journey-accounts) |
| Rastrear actividad de recorrido diario de cuenta | [Rastrear la actividad diaria de la cuenta](#account-daily-activity) |
| Investigación del historial de una cuenta en un recorrido | [Revisar una escala de tiempo de recorridos de cuenta](#account-timeline) |
| Comparar recorridos de personas por tamaño y estado | [Comparar recuentos de personas por recorrido](#person-journey-counts) |
| Enumeración de las personas de un recorrido | [Enumerar personas en un recorrido](#journey-people) |
| Ver dónde están las personas en un recorrido | [Comparar recuentos de personas por paso](#person-step-counts) |
| Rastrear actividad reciente del recorrido de personas | [Rastrear actividad de recorrido reciente](#person-journey-activity) |
| Investigar la historia de una persona en un recorrido | [Revisar la escala de tiempo del recorrido de una persona](#person-timeline) |

## Consultas de cuenta y grupo de compra

Utilice estas consultas para revisar las cuentas, los grupos de compra y las personas disponibles para los informes.

### Revisar detalles de la cuenta {#account-details}

Revise los nombres de las cuentas, los sectores, las ubicaciones y los tamaños de las empresas para comprender las cuentas disponibles para los informes.

```sql
SELECT
a._id AS accountID,
a.accountName,
a.industry,
a.country,
a.numberOfEmployees
FROM account_table a
WHERE a.isDeleted = FALSE
ORDER BY a.accountName
LIMIT 100;
```

### Comparar la participación del grupo comprador {#buying-group-engagement}

Compare grupos de compras por puntuación de participación registrada, junto con la integridad y el interés por la solución.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
bg.engagementScore,
bg.completenessScore,
bg.solutionInterest,
bg.buyingGroupStatus
FROM buying_group_table bg
WHERE bg.isDeleted = FALSE
ORDER BY bg.engagementScore DESC NULLS LAST, bg.buyingGroupName
LIMIT 100;
```

### Buscar personas en una cuenta {#account-people}

Encuentre a las personas y los cargos asociados con una cuenta para comprender a sus contactos. Reemplace `Example Company` con un nombre de cuenta de su zona protegida.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
p._id AS personID,
p.firstName,
p.lastName,
p.email,
p.jobTitle
FROM account_member_table m
JOIN account_table a ON m.accountID = a._id
JOIN person_table p ON m.personID = p._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND p.isDeleted = FALSE
AND a.accountName = 'Example Company'
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Revisar cambios de estado de grupo de compra {#buying-group-status-changes}

Revise los cambios de estado del grupo de compra en los últimos 30 días para comprender cómo cambian los grupos con el paso del tiempo.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
e.timestamp AS changedAt,
e.newStatus
FROM buying_group_event_table e
JOIN buying_group_table bg ON e.buyingGroupID = bg._id
WHERE bg.isDeleted = FALSE
AND e.eventType = 'buyingGroup.changeStatus'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Consultas de participación de persona

Utilice estas consultas para revisar la participación por correo electrónico y otra actividad de persona registrada.

### Buscar personas que hicieron clic en un correo electrónico {#email-clicks}

Para revisar la participación reciente del correo electrónico, identifique a las personas con clics en correos electrónicos registrados en los últimos 30 días.

```sql
SELECT DISTINCT
p._id AS personID,
p.firstName,
p.lastName,
p.email
FROM person_activity_table e
JOIN person_table p ON e.personID = p._id
WHERE e.isDeleted = FALSE
AND p.isDeleted = FALSE
AND e.eventType = 'directMarketing.emailClicked'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### Comparar actividad de persona reciente {#person-activity}

Compare los tipos de actividades registradas y el número de personas involucradas para comprender la participación reciente.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC
LIMIT 100;
```

## Consultas de recorrido de cuenta

Utilice estas consultas para analizar los recorridos de cuenta. Reemplace `PASTE_COMPLETE_JOURNEY_ID_HERE` con el valor `_id` del recorrido de la cuenta y `PASTE_COMPLETE_ACCOUNT_ID_HERE` con el valor `_id` de la cuenta.

### Comparar recuentos de cuentas por recorrido {#account-journey-counts}

Compare recorridos de cuenta por estado y recuento de suscripciones registradas para ver qué recorridos tienen las poblaciones de cuentas más grandes.

```sql
SELECT
j._id AS journeyID,
j.accountJourneyName,
j.accountJourneyStatus,
COUNT(DISTINCT m.accountID) AS accountsWithRecordedMembership
FROM account_journey_table j
LEFT JOIN account_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.accountID <> ''
WHERE j.isDeleted = FALSE
GROUP BY j._id, j.accountJourneyName, j.accountJourneyStatus
ORDER BY accountsWithRecordedMembership DESC, j.accountJourneyName
LIMIT 100;
```

### Enumeración de cuentas en un recorrido {#journey-accounts}

Revisar las cuentas asociadas a un recorrido en particular, incluidos sus sectores y países.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
a.industry,
a.country
FROM account_journey_member_table m
JOIN account_table a ON m.accountID = a._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY a.accountName, accountID
LIMIT 100;
```

### Rastrear actividad diaria de la cuenta {#account-daily-activity}

Rastree las adiciones, eliminaciones y cambios de paso de las cuentas diarias para comprender la actividad en un recorrido durante los últimos 30 días.

```sql
SELECT
CAST(e.timestamp AS DATE) AS activityDate,
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.accountID) AS distinctAccounts
FROM account_activity_table e
WHERE e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.accountID IS NOT NULL
AND e.accountID <> ''
AND e.eventType IN (
'account.addAccountToJourney',
'account.removeAccountFromJourney',
'account.changeAccountJourneyNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY CAST(e.timestamp AS DATE), e.eventType
ORDER BY activityDate DESC, e.eventType
LIMIT 100;
```

### Revisar una cronología de recorridos de cuenta {#account-timeline}

Investigue el historial de recorrido reciente de una cuenta revisando sus eventos registrados y los pasos de recorrido.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
n.nodeType,
e.previousJourneyNodeID,
e.buyingGroupID
FROM account_activity_table e
LEFT JOIN account_journey_node_table n
ON e.journeyNodeID = n._id
AND e.journeyID = n.accountJourneyID
AND n.isDeleted = FALSE
WHERE e.accountID = 'PASTE_COMPLETE_ACCOUNT_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## Consultas del recorrido de personas

Utilice estas consultas para analizar los recorridos de las personas. Reemplace `PASTE_COMPLETE_JOURNEY_ID_HERE` por el valor `_id` del recorrido de persona y `PASTE_COMPLETE_PERSON_ID_HERE` por el valor `_id` de la persona.

### Comparar recuentos de personas por recorrido {#person-journey-counts}

Compare los recorridos de las personas por recuento de miembros registrado, estado y fechas para comprender su tamaño y ciclo de vida.

```sql
SELECT
j._id AS journeyID,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate,
COUNT(DISTINCT m.personID) AS peopleWithRecordedMembership
FROM person_journey_table j
LEFT JOIN person_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.personID <> ''
WHERE j.isDeleted = FALSE
GROUP BY
j._id,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate
ORDER BY peopleWithRecordedMembership DESC, j.personJourneyName
LIMIT 100;
```

### Enumerar personas en un recorrido {#journey-people}

Revise quién está asociado a un recorrido, cuándo entró por última vez y con qué frecuencia.

```sql
SELECT DISTINCT
m.personID,
p.firstName,
p.lastName,
p.email,
m.membershipDate,
m.lastEntryDate,
m.entryCount,
m.reentryOpensAt,
m.journeyNodeID
FROM person_journey_member_table m
LEFT JOIN person_table p
ON m.personID = p._id
AND p.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY m.lastEntryDate DESC NULLS LAST, m.personID
LIMIT 100;
```

### Comparar recuentos de personas por paso {#person-step-counts}

Vea cómo se distribuyen las personas entre los pasos registrados en sus suscripciones a recorrido.

```sql
SELECT
m.journeyNodeID,
n.nodeType,
COUNT(DISTINCT m.personID) AS peopleWithRecordedStep
FROM person_journey_member_table m
LEFT JOIN person_journey_node_table n
ON m.journeyNodeID = n._id
AND m.journeyID = n.personJourneyID
AND n.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
GROUP BY m.journeyNodeID, n.nodeType
ORDER BY peopleWithRecordedStep DESC, m.journeyNodeID
LIMIT 100;
```

### Rastrear actividad de recorrido reciente {#person-journey-activity}

Compare inicios, finales y transiciones de recorridos registrados para comprender la actividad de la persona en un recorrido durante los últimos 30 días.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.eventType IN (
'person.journeyAdd',
'person.journeyRemove',
'person.journeyStart',
'person.journeyEnd',
'person.journeyNodeTransition',
'person.journeySplitNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC, e.eventType
LIMIT 100;
```

### Revisar la cronología del recorrido de una persona {#person-timeline}

Investigue el historial de recorridos reciente de una persona, incluidas las transiciones de pasos, las opciones divididas y las actualizaciones de perfil atribuidas a recorridos.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
e.previousJourneyNodeID,
e.newJourneyNodeID,
e.journeyChoiceNumber,
e.journeyEntryCount,
e.attributeName,
e.attributeOldValue,
e.attributeNewValue
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID = 'PASTE_COMPLETE_PERSON_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```
