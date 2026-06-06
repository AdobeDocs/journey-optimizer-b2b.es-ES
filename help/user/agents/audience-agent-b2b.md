---
title: Audience Agent B2B
description: Audience Agent B2B en Journey Optimizer B2B edition utiliza el análisis de intención y la asignación de personas para crear grupos de compra y acelerar los flujos de trabajo de marketing B2B.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: b43117c1e47f698d62b29f56b4713ac776c497a0
workflow-type: tm+mt
source-wordcount: 2500
ht-degree: 1%

---

# Audience Agent B2B

Con la tecnología [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), Audience Agent B2B está disponible en Journey Optimizer B2B edition. El uso de este agente mejora la eficacia y la eficacia en la exploración y ampliación de audiencias, lo que acelera la creación de grupos de compra y los flujos de trabajo ininterrumpidos para la activación de recorridos:

* **_Priorizar las audiencias de destino por intención_**: infiera las personas en función de la intención del producto para distintas audiencias y optimice la planificación de la campaña, lo que reduce el tiempo empleado en la validación de audiencias.

* **_Aproveche la IA para detectar y crear grupos de compra_**: Utilice IA, datos estructurados y no estructurados y datos unificados de origen para optimizar la detección y creación de grupos de compra.

![Audience Agent B2B en modo de página completa](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Para usar Audience Agent B2B, se requieren definiciones y asignaciones de datos:<br/>
>
>* [Asignación/taxonomía de datos por intención](../admin/intent-data.md)
>* [Asignación/taxonomía de campos XDM](#xdm-data-prerequisites)

## Funciones de Audience Agent B2B

| Área | Qué hace | Valor comercial |
| ---- | ------------ | -------------- |
| Análisis por intención | <li> Mida la intensidad de la intención de la cuenta (como baja, media y alta) para productos específicos. <li>Comparar las tendencias de interés de productos con el paso del tiempo (por ejemplo, los productos principales de los últimos _n_ días). <li>Identifique las cuentas que muestren interés de forma activa en productos específicos. <li>Patrones de participación superficial que combinan la actividad de la cuenta con la cobertura personal. | <li>Ayuda a los equipos a centrarse en las cuentas correctas en el momento adecuado. <li>Mejora la calidad de la canalización priorizando las cuentas con señales de compra genuinas. <li>Habilita la participación proactiva antes de que la competencia actúe. |
| Asignación de persona | <li>Detecte y clasifique las personas principales por intención de producto. <li>Identifique a las personas involucradas en la compra de uno o varios productos. <li>Asigne personalidades a funciones funcionales (como _Campeón_, _Responsable de la toma de decisiones_ e _Influenciador_) con justificación. <li>Validar por qué una persona determinada se considera un campeón. | <li>Garantiza que el equipo de ventas involucre a los verdaderos tomadores de decisiones e influenciadores. <li>Reduce el esfuerzo perdido en contactos de bajo impacto. <li>Aumenta las tasas de ganancia al alinear el alcance con la dinámica del poder del comprador. |
| Evaluación del grupo de compra | <li>Evalúe el tamaño del grupo comprador (por ejemplo, grupos con más de _n_ miembros). <li>Mida la cobertura personal entre cuentas (por ejemplo, por debajo de _x_%). <li>Rastree la distribución de funciones y las brechas de cobertura dentro de los grupos compradores. <li>Resaltar cuentas con campeones identificados en acuerdos recientes. | <li>Revela brechas de cobertura que podrían estancar acuerdos. <li>Fortalece las estrategias de subprocesamiento múltiple al garantizar la representación completa de las funciones. <li>Mejora el seguimiento de la salud de los acuerdos mediante perspectivas de participación a nivel de grupo. |
| Creación de grupos de compra y capacidad de acción | <li>Recomendar asignaciones de función a persona en función de los patrones de función y persona observados. <li>Genere una plantilla de rol de grupo de compra para un producto especificado. <li>Admitir la personalización de plantillas al incluir o excluir personas y funciones específicas. <li>Compruebe que los roles necesarios se han definido antes de crear los grupos de compra. | <li>Reduce el esfuerzo manual y el riesgo de plantillas de grupo de compra incompletas. <li>Garantiza que la cobertura de funciones se valide antes de la creación y mitiga el riesgo de lagunas de cobertura. <li>Convierte los datos del análisis en próximos pasos inmediatos y operativos. |

## Limitaciones

Audience Agent B2B depende de la taxonomía por intención configurada, las asignaciones de campos XDM y los datos de evento de experiencia. Las perspectivas son menos fiables cuando los datos de oportunidad están incompletos, falta la taxonomía por intención o están obsoletos, o los identificadores de perfil y cuenta requeridos no están asignados. Para el cálculo de intención, el agente procesa solo estos eventos de experiencia: `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` y `web.webpagedetails.pageViews`.

## Ejemplos de indicaciones

Estos ejemplos de mensajes muestran algunas de las formas en que puede utilizar el agente:

* Mostrar la ventana de tendencias: actualizaciones más antiguas y más recientes de la calidad del producto de la cuenta por producto.
* Para `<product>`, enumere los grupos de compra con la intención y las puntuaciones del producto.
* Para `<product>`, enumere los personajes y las funciones con sus métricas de oportunidad (tasa de victorias, tasa de membresía, recuentos).
* Para las cuentas de `<industry>`, ¿cuál es el promedio de cobertura personal de la cuenta para `<product>`?
* ¿Qué cuentas tienen poca intención de cualquier producto pero aún tienen oportunidades abiertas (vale la pena nutrirlas)?
* ¿Qué cuentas agregaron nuevas señales de intención para `<account_name>` esta semana?
* Mostrarme los perfiles asociados con `<product>`.
* Mostrarme la recomendación de asignación de rol a persona para `<product>`.
* Crear una plantilla de grupo de compra para `<product>`.
* Cree una plantilla de grupo de compra para `<product>` sin el perfil `<persona>` y quite el rol `<role>`.

## Conceptos

| Concepto | Explicación |
| ------- | ----------- |
| Detección de audiencias | Entre bastidores, el agente observa las señales de intención de origen basadas en dos cosas: qué tan comprometidas están las personas con su marca y el tipo de personas que representan. El análisis repasa los últimos 18 meses de actividad para detectar la intención del producto en todos los usuarios de la cuenta, especialmente durante el tiempo previo al cierre de una oportunidad. Este análisis ayuda al agente a resaltar las personas que tienen más probabilidades de influir en el acuerdo.<br/><br/>A veces las cuentas no tienen todos sus datos de oportunidad en perfecta forma, lo cual está bien y el agente puede detectar la intención del producto únicamente a partir de patrones de participación. |
| Persona | Personas representa los tipos de personas que se relacionan con una cuenta. El agente los crea mirando el cargo, la función y el nivel de antigüedad, y luego normalizando esa información para que sea coherente en las diferentes cuentas. De esa manera, en lugar de perderse en títulos desordenados, puede ver rápidamente si está llegando a los encargados de tomar decisiones, influenciadores o roles de soporte. Las personas le ayudan a comprender quién muestra interés, no solo cuánto interés hay. |
| Asignación de funciones de grupo de compra | Una vez que las personas se asignan a las funciones, las reúne en un grupo de compra: el equipo completo dentro de la cuenta que tiene más probabilidades de influir o decidir la compra. Cada rol (como _encargado de tomar decisiones_, _influencer_ o _campeón_) agrega una parte de la imagen para que tengas una visión clara del comité que está impulsando el acuerdo.<br/><br/>El agente asigna a cada persona identificada la función que tiene más probabilidades de desempeñar para un producto específico, según el cargo, la función, la antigüedad y otros atributos que configure. También muestra la cobertura de cada función para que pueda ver qué funciones están bien representadas y dónde quedan las lagunas en la estrategia de participación. |
| Uso de datos de oportunidad para detectar un perfil | Para ofrecerle la visión más precisa de quién es atractivo y dónde se encuentran sus intereses, el agente aborda la clasificación personal y la intención del producto de acuerdo con lo siguiente: <ul><li>Caso más probable: si puede proporcionar datos como _Fase de oportunidad_, _Fecha de cierre de oportunidad_ y una _asignación de oportunidad a producto_ clara, el agente puede clasificar con confianza a las personas por producto.<li>Esta clasificación proporciona una comprensión precisa de la participación y el interés en toda la cuenta. </ul>Pero el agente sabe que los datos no siempre están completos, lo cual es correcto. Incluye retrocesos inteligentes para mantener las cosas en movimiento:<ul><li>El agente analiza el volumen de las actividades, dando más peso a las recientes utilizando la decadencia temporal.<li>Esta ponderación permite al agente diferenciar y clasificar personas, incluso sin datos de oportunidad completos. </ul>Cuando se trata de vincular oportunidades a productos, el agente se encarga de ello de la siguiente manera:<ul><li>_Ideal_: usted proporciona o ayuda al agente a crear la tabla de asignación.<li>_Si no está disponible_: el agente usa la coincidencia difusa para conectar los puntos.<li>_Sin vinculación_: el agente infiere la intención del producto en función de las actividades recientes anteriores a la fecha de cierre.</ul>Este enfoque por niveles garantiza que el agente pueda seguir ofreciendo perspectivas significativas, incluso cuando los datos no sean perfectos. |
| Análisis de oportunidad | El agente examina los datos de oportunidades históricas para comprender qué factores predicen más fuertemente una victoria y utiliza tres dimensiones principales para hacerlo:<ol><li>Tasa de victorias: muestra la frecuencia con la que se cierran correctamente las ofertas cuando participan determinadas personas. Si las cuentas con un patrón personal específico (como un evaluador técnico o un tomador de decisiones a nivel de vicepresidente) tienden a convertirse con más frecuencia, el modelo le da mayor peso a ese patrón. Esta información es un porcentaje del total de oportunidades, como las oportunidades cerradas o ganadas.<li>Tasa de pertenencia a grupos: mide la frecuencia con la que se muestra un tipo de persona en las oportunidades de un producto determinado. Si ciertas personas aparecen de forma consistente en las ofertas exitosas, esto indica que juegan un papel crítico en el proceso de compra.<li>Influencia personal: cuantifica cuánto contribuye una persona determinada al resultado, no solo si está presente, sino también cómo se correlaciona su nivel de participación o actividad con las ganancias.</ol>En conjunto, estas señales ayudan a deducir qué personas tienen el mayor impacto en los resultados de compra, incluso cuando los datos de oportunidad están incompletos. Con el tiempo, permite que el sistema muestre personalidades de alto impacto y patrones que son más predictivos del éxito de la operación, lo que a su vez informa la intención de la cuenta, el mapeo de personalidades y las recomendaciones de grupos de compra. |
| Intención | Cuando alguien visita una página web o hace clic en un vínculo de correo electrónico relacionado con un producto, es una señal de que está interesado y se llama _intención_.<br/><br/>El agente comienza con una taxonomía, que es básicamente una lista de los productos del cliente y las palabras clave que los describen. Esta información ayuda al agente a comprender de qué trata cada parte del contenido o interacción.<br/><br/>A continuación, el agente usa esa taxonomía para etiquetar la actividad del visitante, como las palabras clave o los productos a los que se relacionan sus acciones.<br/><br/>A continuación, el agente observa la profundidad con que se involucra alguien, como la cantidad de páginas que visita o la frecuencia con que interactúa. Utiliza esta información para calcular la puntuación de intención individual para palabras clave, productos o categorías de productos específicos. Agrupa cada puntuación de intención en _Alta_, _Medium_ o _Baja_ para indicar la intensidad del interés. (Intención baja: `<=0.2`, intención de Medium: `0.2 < score <= 0.6`, intención alta: `0.6 < score <= 1`)<br/><br/>Por último, el agente combina las puntuaciones de intención de todas las personas de la misma compañía (cuenta) para ver la intención general a nivel de cuenta, mostrando qué productos o temas parecen interesar más a la compañía. |
| Funciones que influyen en un grupo comprador | Cada grupo comprador está formado por funciones que contribuyen de forma diferente a la decisión de compra, como _Decisionista_, _Influenciador_, _Campeón_ y _Usuario final_. Cada función tiene un grado variable de impacto.<br/><br/>Los encargados de tomar decisiones tienen la mayor influencia y generalmente controlan las aprobaciones presupuestarias. Los influenciadores modelan la evaluación y las recomendaciones. Los Campeones ayudan a crear un consenso interno, mientras que los Usuarios finales validan el ajuste del producto.<br/><br/>Al mostrarle estas funciones, el agente le ayuda a comprender quién es el responsable de la decisión de compra, dónde es más sólida su participación y dónde pueden existir brechas de cobertura. Esta información le permite centrarse en las funciones más importantes para este producto. |
| Cobertura de persona o función | Para cualquier producto dado, normalmente hay un conjunto de roles y personalidades clave que se sabe que influyen en la compra (_N_ personalidades o roles).<br/><br/>Para cada cuenta, el agente calcula la cobertura comprobando cuántos de esos roles de _N_ están representados por al menos una persona dentro de esa cuenta.<br/><br/>Si todos los roles de _N_ están presentes, la cuenta tiene cobertura total. Si solo se representan algunos roles, la cobertura es parcial.<br/><br/>En términos sencillos, la cobertura de funciones y personas mide la integridad del grupo de compra de un producto, en función de si se incluyen todas las personas que toman decisiones, influyentes y campeones importantes. |

## Requisitos previos de datos XDM

Audience Agent proporciona perspectivas sobre las cuentas que muestran la intención de origen de los productos y calcula las personas y las funciones en función de los datos definidos. Asegúrese de que los siguientes datos previos estén configurados para utilizar las funciones de Audience Agent:

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
      <td>Nombre de la persona que Audience Agent utiliza para mostrar los nombres en la interfaz de usuario cuando se cumplen los criterios</td>
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
      <td>Nombre completo de la persona que Audience Agent utiliza para mostrar los nombres en la interfaz de usuario cuando se cumplen los criterios</td>
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
      <td>Apellidos de la persona que Audience Agent utiliza para mostrar los nombres en la interfaz de usuario cuando se cumplen los criterios</td>
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
      <td>Nombre de la cuenta que Audience Agent utiliza para mostrar en la interfaz de usuario cuando se cumple cualquier criterio planteado en la consulta del usuario</td>
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
      <td>Descripción de la cuenta o empresa utilizada por Audience Agent para aplicar filtros a las cuentas según las consultas del usuario en la interfaz de usuario </td>
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
      <td>Sector de la cuenta o compañía utilizado por Audience Agent para aplicar filtros a las cuentas según las consultas del usuario en la interfaz de usuario </td>
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
      <td>Dirección de facturación de la cuenta o compañía utilizada por Audience Agent para aplicar filtros a las cuentas según las consultas del usuario en la IU. </td>
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
      <td>Nombre de la oportunidad utilizada por Audience Agent </td>
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
      <td>Descripción de la oportunidad utilizada por Audience Agent </td>
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

Audience Agent aprovecha la intención de origen detectada en Journey Optimizer B2B edition:

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
      <td>Obtenga el tipo de evento, ya que el agente procesa solo cuatro eventos (<span>directMarketing.emailClicked, directMarketing.emailOpened, directMarketing.emailUnsuscribed, web.webpagedetails.pageViews)</span>
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
      <td>Se utiliza para recuperar el contenido del correo electrónico del centro de datos de Marketo Engage; se compone de (SourceID@SourceInstanceID.SourceType)</td>
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
