---
title: Aptitudes de audiencia para cuentas B2B y personas
description: Obtenga información acerca de las habilidades de audiencia para cuentas B2B y personas. Explore la intención del producto, identifique personas, evalúe la cobertura de funciones y cree plantillas de grupo de compra.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
    internal-label: Taxonomy
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 1%
---
# Aptitudes de audiencia para personas y cuentas B2B

Use aptitudes de audiencia para B2B en la interfaz [!DNL CX Coworker]. Explore la intención del producto en cuentas y personas. Identifique las personas relevantes, evalúe la cobertura del grupo de compra y cree plantillas de rol de grupo de compra.

* Evalúe el interés de la cuenta en productos específicos y compare las tendencias por intención.
* Identificar personas y perfiles asociados con el interés del producto.
* Revise las funciones de grupo de compra e identifique las brechas de cobertura.
* Generar y perfeccionar plantillas de rol de grupo de compra.

>[!PREREQUISITES]
>
>Antes de usar habilidades de audiencia para cuentas y personas B2B, configure las siguientes definiciones y asignaciones de datos:
>
>* [Asignación y taxonomía de datos por intención](../admin/intent-data.md)
>* [Asignación de campo XDM](#xdm-data-prerequisites)

Haga clic en el icono _Preguntar[!DNL Coworker]_ ( ![Preguntar [!DNL Coworker]](../assets/do-not-localize/icon-ask-coworker.svg) ) en la parte superior de la aplicación para abrir la aplicación [!DNL Coworker]. Introduzca el indicador de lenguaje natural en la interfaz de chat.

![Mensaje de audiencia en [!DNL CX Coworker]](./assets/audience-skills-prompt.png){width="800" zoomable="yes"}

## Áreas de enfoque de habilidades de audiencia

Utilice áreas de enfoque de habilidades de audiencia para explorar la intención de la cuenta, comprender a las personas y los perfiles, y preparar plantillas de grupo de compra.

| Focus | Tareas |
| ----- | ----- |
| Intento de cuenta | Evaluar la intención de la cuenta para productos específicos mediante niveles de intención bajos, medios y altos. Compare las tendencias de interés de productos a lo largo del tiempo e identifique cuentas que muestren interés en productos específicos. Revise los patrones de participación junto con la cobertura personal. |
| Personas y personalidades | Identifique y clasifique a las personas por intención de producto en uno o más productos. Revise las métricas de oportunidad, incluidas la tasa de ganancia, la tasa de pertenencia y los recuentos. Asigne personalidades a funciones como _Campeón_, _Encargado de tomar decisiones_ e _Influenciador_, y revise las explicaciones de las asignaciones de funciones. |
| Cobertura del grupo comprador | Evaluar el tamaño del grupo comprador y la cobertura del perfil en todas las cuentas. Revise la distribución de funciones e identifique las personas o funciones que faltan. Encuentre cuentas con campeones identificados en ofertas recientes. |
| Plantillas de grupo de compra | Genere plantillas de función de grupo de compra para productos específicos y revise las asignaciones de personas recomendadas. Refine las plantillas incluyendo o excluyendo personalidades y roles. Valide los roles necesarios antes de crear grupos de compra. |

## Limitaciones

Las perspectivas de audiencia dependen de la taxonomía por intención configurada, las asignaciones de campos XDM y los datos de evento de experiencia. Los datos de oportunidad incompletos, la taxonomía que falta o está obsoleta, o los identificadores de perfil y cuenta que faltan pueden reducir la fiabilidad de insight.

El cálculo de intención solo usa estos eventos de experiencia: `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` y `web.webpagedetails.pageViews`.

## Ejemplos de indicaciones

Escriba las siguientes indicaciones en la interfaz de [!DNL CX Coworker] para explorar la intención de la cuenta, comprender a las personas y los perfiles, y preparar plantillas de grupos de compra.

### Intento de cuenta

Explore el interés de la cuenta en los productos y revise los cambios en la intención.

* Mostrar la ventana de tendencias: actualizaciones más antiguas y más recientes de la calidad del producto de la cuenta por producto.
* ¿Qué cuentas tienen poca intención de cualquier producto pero aún tienen oportunidades abiertas (vale la pena nutrirlas)?
* ¿Qué nuevas señales de intención se registraron para `<account_name>` esta semana?

### Personas y personalidades

Identifique a las personas asociadas con el interés del producto y revise las funciones de grupo de compra recomendadas.

* Mostrarme los perfiles asociados con `<product>`.
* Mostrarme la recomendación de asignación de rol a persona para `<product>`.
* Para `<product>`, enumere los personajes y las funciones con sus métricas de oportunidad (tasa de victorias, tasa de membresía, recuentos).

### Comprar grupos y plantillas

Revise la intención y la cobertura del grupo de compra y, a continuación, genere o pula plantillas.

* Para `<product>`, enumere los grupos de compra con la intención y las puntuaciones del producto.
* Para las cuentas de `<industry>`, ¿cuál es el promedio de cobertura personal de la cuenta para `<product>`?
* Crear una plantilla de grupo de compra para `<product>`.
* Cree una plantilla de grupo de compra para `<product>` sin el perfil `<persona>` y quite el rol `<role>`.

## Conceptos

Utilice estos conceptos para interpretar la intención de la cuenta, las clasificaciones personales y las recomendaciones de grupos de compra.

| Concepto | Explicación |
| ------- | ----------- |
| Detección de audiencias | Analice las señales de participación de origen entre las personas de una cuenta para identificar el interés del producto y las personas relevantes. El análisis considera los 18 meses previos de actividad, incluida la actividad antes del cierre de la oportunidad. Los patrones de participación pueden indicar la intención del producto cuando los datos de oportunidad están incompletos, pero la falta de datos puede reducir la fiabilidad de insight. |
| Persona | Las personas agrupan a las personas por título de trabajo, función y antigüedad normalizados. Utilice personas para comprender quién se involucra en una cuenta, incluidos los responsables de la toma de decisiones, los influenciadores y las funciones de soporte. |
| Asignación de funciones de grupo de compra | Asigne personas a funciones de grupo de compra específicas del producto en función del cargo, la función, la antigüedad y los atributos configurados. Estas funciones representan a las personas de una cuenta que influyen o deciden sobre una compra. Revise la cobertura para identificar los roles que faltan. |
| Datos de oportunidad para la clasificación de personas | La fase de oportunidad, la fecha de cierre y las asignaciones de oportunidad a producto admiten la clasificación personal de cada producto. Cuando los datos de oportunidad están incompletos, la clasificación utiliza el volumen de la actividad y el tiempo decaen para dar más peso a la actividad reciente.<br/><br/>El vínculo del producto usa una tabla de asignación de oportunidades a productos proporcionada o generada cuando está disponible. De lo contrario, la coincidencia aproximada vincula las oportunidades con los productos. Si no hay ningún vínculo disponible, la intención del producto se deduce de la actividad reciente antes de la fecha de cierre de la oportunidad. Estos métodos de reserva no eliminan las limitaciones de fiabilidad de los datos incompletos. |
| Análisis de oportunidad | El análisis de oportunidades históricas utiliza tres dimensiones para identificar patrones de personalidad asociados con resultados de compra:<ul><li>Tasa de victorias: mide la frecuencia con la que se ganan oportunidades cuando participan personas concretas. Los patrones personales asociados con tasas de ganancia más altas reciben más peso.</li><li>Tasa de pertenencia a grupos: mide la frecuencia con la que una persona aparece en las oportunidades de un producto determinado.</li><li>Influencia personal: Mide la correlación entre la participación o la actividad de la persona y las ganancias, más allá de si la persona está presente.</li></ul>Estas señales informan la intención de la cuenta, el mapeo de personas y las recomendaciones de grupos de compra. |
| Intención | La intención indica el interés del producto a través de la participación, como visitas a páginas web o clics en vínculos de correo electrónico. La taxonomía de productos conecta la actividad de participación con palabras clave, productos y categorías de productos. La profundidad y la frecuencia de la participación determinan puntuaciones de intención individuales para cada palabra clave, producto o categoría de producto.<br/><br/>Las puntuaciones indican una fortaleza de interés: de intención baja: `<=0.2`, de intención de Medium: `0.2 < score <= 0.6`, de intención alta: `0.6 < score <= 1`.<br/><br/>Las puntuaciones de intención individuales se agregan entre las personas de la misma cuenta para determinar la intención de la cuenta. |
| Funciones que influyen en un grupo comprador | Las funciones de grupo de compra representan diferentes contribuciones a la decisión de compra. _Responsables de la toma de decisiones_ suelen controlar las aprobaciones presupuestarias. _Influencers_: evaluación y recomendaciones de formas. _Campeones_ crean consenso interno. _Usuarios finales_ validan el ajuste del producto.<br/><br/>Revise las asignaciones de funciones y la cobertura para comprender quién influye en la decisión y dónde persisten las brechas de participación. |
| Cobertura de persona o función | La cobertura mide cuántas personas o funciones esperadas tienen al menos un representante dentro de una cuenta. Para un producto con _N_ personalidades o roles esperados, la cobertura completa significa que todos los _N_ están representados. La cobertura parcial significa que faltan algunos. Utilice la cobertura para evaluar la integridad del grupo de compra e identificar lagunas. |

## Requisitos previos de datos XDM

Configure las siguientes asignaciones de campo XDM para admitir el análisis de intención de cuenta, la identificación de personas y la asignación de funciones de grupo de compra.

### Asignación de campo XDM

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entidad</th>
      <th>Definición comercial</th>
      <th>Detalles adicionales</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfiles</span>
        </p>
      </td>
      <td>Identificador de cuenta, que se utiliza para unir datos de oportunidad, evento e intención</td>
      <td rowspan="2">Análisis de oportunidad<br/>Exploración de cuenta<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfiles</span>
        </p>
      </td>
      <td>Identificador de persona, se utiliza en uniones que implican datos de evento para generar datos de perfil</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.departments</span>
        </p>
      </td>
      <td>
        <p>
          <span> perfiles</span>
        </p>
      </td>
      <td>Departamento de trabajo del perfil/persona</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Asignación de personas</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span> perfiles</span>
        </p>
      </td>
      <td>Puesto de trabajo del perfil/persona utilizado en el cálculo de personas</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>person.name.firstName</span>
        </p>
      </td>
      <td>
        <p>
          <span >Perfiles</span>
        </p>
      </td>
      <td>Muestra el nombre de la persona en los resultados que coinciden con la consulta.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.fullName</span>
        </p>
      </td>
      <td>
        <p>
          <span> perfiles</span>
        </p>
      </td>
      <td>Muestra el nombre completo de la persona en los resultados que coinciden con la consulta.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.lastName</span>
        </p>
      </td>
      <td>
        <p>
          <span> perfiles</span>
        </p>
      </td>
      <td>Muestra el apellido de la persona en los resultados que coinciden con la consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span> cuentas</span>
        </p>
      </td>
      <td>Identificador de cuenta, que se utiliza para unir datos de oportunidad, evento e intención</td>
      <td>Análisis de oportunidad<br/>Exploración de cuenta</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Cuentas</span>
        </p>
      </td>
      <td>Muestra el nombre de la cuenta en los resultados que coinciden con la consulta.</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Exploración de cuentas</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Cuentas</span>
        </p>
      </td>
      <td>Admite el filtrado de cuentas por descripción de cuenta según la consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span> cuentas</span>
        </p>
      </td>
      <td>Admite el filtrado de cuentas por sector según la consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span> cuentas</span>
        </p>
      </td>
      <td>Admite el filtrado de cuentas por región de dirección de facturación en función de la consulta.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Identificador de cuenta, que se utiliza para unir datos de oportunidad, evento e intención</td>
      <td rowspan="2">
        <p>Análisis de oportunidad<br/>Exploración de cuenta</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>oportunidadKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Identificador de oportunidad, utilizado en uniones para datos de cuentas</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>nombreDeOportunidad</span>
        </p>
      </td>
      <td>
        <p>
          <span> oportunidad</span>
        </p>
      </td>
      <td>Nombre de oportunidad utilizado en el análisis de oportunidades.</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Análisis de oportunidades</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>ha ganado</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Si la oportunidad está ganada (binaria)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>descripción de oportunidad</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Descripción de oportunidad utilizada en el análisis de oportunidades.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>cantidadOportunidad</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Cantidad de $ involucrados en la oportunidad</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>tipoOportunidad</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Tipo de oportunidad</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>oportunidadStage</span>
        </p>
      </td>
      <td>
        <p>
          <span> oportunidad</span>
        </p>
      </td>
      <td>Etapa de oportunidad (cerrada ganada o cerrada perdida o cualquiera de las etapas intermedias) </td>
      <td rowspan="4">
        <p>Análisis de oportunidad<br/>Exploración de cuenta</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>actualCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Fecha de cierre real de la oportunidad</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span> oportunidad</span>
        </p>
      </td>
      <td>Fecha de cierre esperado de la oportunidad</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Oportunidad</span>
        </p>
      </td>
      <td>Fecha de creación de esta oportunidad</td>
    </tr>
  </tbody>
</table>

### Datos de taxonomía

Las aptitudes de audiencia utilizan datos de intención de origen de [!DNL Adobe Journey Optimizer B2B Edition]. El cálculo de intención conecta la taxonomía de productos con la actividad de participación y agrega puntuaciones individuales en el nivel de cuenta.

1. El cálculo de intenciones requiere datos de taxonomía (productos del cliente y palabras clave correspondientes) de Clientes > Taxonomía
1. Los datos de taxonomía se utilizan para etiquetar datos de evento (etiquetado de recursos). Estos datos proporcionan perspectivas sobre las palabras clave y los productos que interesan a los visitantes en función de sus datos de evento > Etiquetado de recursos 
1. Los recursos etiquetados (datos de evento) se combinan con los comportamientos de los visitantes (número de páginas visitadas) para determinar la intención del visitante en los niveles de palabra clave, producto y categoría de producto → cálculo de intención
1. Las puntuaciones de intención a nivel de perfil del visitante se agregan a nivel de cuenta para determinar la intención de la cuenta en una palabra clave, producto y categoría de producto determinados > Agregación de cuenta de intención

Además de [configurar la taxonomía por intención](../admin/intent-data.md), se requieren los campos siguientes:

<table>
  <tbody>
    <tr>
      <th>Campo XDM</th>
      <th>Entidad</th>
      <th>Definición comercial</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>perfil de persona</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfil</span>
        </p>
      </td>
      <td>Ayuda a identificar a una persona (correo electrónico o b2b_person) como identificador</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Perfil</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>keyword_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Se utiliza como taxonomía para etiquetar recursos (eventos de experiencia, como correos electrónicos en los que se hizo clic o páginas web visitadas)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>marca de tiempo</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Se utiliza durante un tiempo para obtener el relleno y la ejecución incremental</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Identifica el tipo de evento. El cálculo de intención solo usa <code>directMarketing.emailClicked</code>, <code>directMarketing.emailOpened</code>, <code>directMarketing.emailUnsubscribed</code> y <code>web.webpagedetails.pageViews</code>.
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Solo para referencia/teneduría de libros; Información sobre el nombre de la campaña</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailkey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Solo como referencia/teneduría de libros; información sobre el ID de origen al que se dirige el correo electrónico</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailkey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Solo para referencia/teneduría de libros; información de la instancia de origen a la que se dirige el correo electrónico</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailkey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Se usa para recuperar el contenido del correo electrónico del centro de datos [!DNL Adobe Marketo Engage]. Incluye (SourceID@SourceInstanceID.SourceType).</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailkey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Solo para referencia/teneduría de libros; Información sobre el tipo de origen o de dónde se originó la fuente </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Información sobre el origen de la visita a la página web</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>URL real utilizada para obtener contenido</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Parámetro de consulta adicional para la URL utilizada para recuperar contenido de destino </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>solo para referencia/contabilidad</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Solo como referencia/teneduría de libros; información sobre el ID de origen al que se dirige el correo electrónico</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Evento de experiencia</span>
        </p>
      </td>
      <td>Solo para referencia/teneduría de libros; información sobre la instancia de origen a la que se dirige el correo electrónico</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>Evento de experiencia</span>
      </td>
      <td>Solo para referencia/contabilidad; se compone de (SourceID@SourceInstanceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>Evento de experiencia</span>
      </td>
      <td>Solo para referencia/teneduría de libros; Información para el tipo de fuente o de dónde procede la fuente</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>Evento de experiencia</span>
      </td>
      <td>Se utiliza para recuperar la dirección URL real si web.webPageDetails.name no la tiene.</td>
    </tr>
  </tbody>
</table>
