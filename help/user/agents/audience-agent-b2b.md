---
title: Audience Agent para B2B
description: Audience Agent B2B en Recorrido OptimizerB2B Edition utiliza el análisis de intención y la asignación de personas para crear grupos de compra y acelerar los flujos de trabajo de marketing B2B.
feature: Audiences, AI Assistant
role: User
source-git-commit: fa53458db4576af037dcf4b16ab1bf7b103b2fdd
workflow-type: tm+mt
source-wordcount: '3066'
ht-degree: 0%

---

# Audience Agent para B2B

Con la tecnología [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/es/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), Audience Agent B2B está disponible en Journey Optimizer B2B edition. El uso de este agente mejora la eficacia y la eficacia en la exploración y ampliación de audiencias, lo que acelera la creación de grupos de compra y los flujos de trabajo ininterrumpidos para la activación de recorridos:

* **_Priorizar las audiencias de destino por intención_**: infiera las personas en función de la intención del producto para distintas audiencias y optimice la planificación de la campaña, lo que reduce el tiempo empleado en la validación de audiencias.

* **_Aproveche la IA para detectar grupos compradores_**: Utilice IA, datos estructurados y no estructurados y datos unificados de origen para optimizar la detección y creación de grupos compradores.

![Audience Agent para B2B en modo de página completa](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Para usar Audience Agent para B2B, se requieren definiciones y asignaciones de datos:<br/>
>
>* [Asignación/taxonomía de datos por intención](../admin/intent-data.md)
>* [Asignación/taxonomía de campos XDM](#xdm-data-prerequisites)

## Funciones de Audience Agent para B2B

| Área | Qué hace | Valor comercial |
| ---- | ------------ | -------------- |
| Análisis por intención | <li> Mida la intensidad de la intención de la cuenta (como baja, media y alta) para productos específicos. <li>Comparar las tendencias de interés de productos con el paso del tiempo (por ejemplo, los productos principales de los últimos _n_ días). <li>Identifique las cuentas que muestren interés de forma activa en productos específicos. <li>Patrones de participación superficial que combinan la actividad de la cuenta con la cobertura personal. | <li>Ayuda a los equipos a centrarse en las cuentas correctas en el momento adecuado. <li>Mejora la calidad de la canalización priorizando las cuentas con señales de compra genuinas. <li>Habilita la participación proactiva antes de que la competencia actúe. |
| Asignación de personas | <li>Detecte y clasifique las personas principales por intención de producto. <li>Identifique a las personas involucradas en la compra de uno o varios productos. <li>Asigne personalidades a funciones funcionales (como _Campeón_, _Responsable de la toma de decisiones_ e _Influenciador_) con justificación. <li>Validar por qué una persona determinada se considera un campeón. | <li>Garantiza que el equipo de ventas involucre a los verdaderos tomadores de decisiones e influenciadores. <li>Reduce el esfuerzo perdido en contactos de bajo impacto. <li>Aumenta las tasas de ganancia al alinear el alcance con la dinámica del poder del comprador. |
| Evaluación del grupo de compra | <li>Evalúe el tamaño del grupo comprador (por ejemplo, grupos con más de _n_ miembros). <li>Mida la cobertura personal entre cuentas (por ejemplo, por debajo de _x_%). <li>Rastree la distribución de funciones y las brechas de cobertura dentro de los grupos compradores. <li>Resaltar cuentas con campeones identificados en acuerdos recientes. | <li>Revela brechas de cobertura que podrían estancar acuerdos. <li>Fortalece las estrategias de subprocesamiento múltiple al garantizar la representación completa de las funciones. <li>Mejora el seguimiento de la salud de los acuerdos mediante perspectivas de participación a nivel de grupo. |

## Ejemplos de mensajes

Estos ejemplos de mensajes muestran algunas formas de utilizar el agente:

* Mostrar la ventana de tendencias: actualización más reciente y más temprana de la calidad del producto de la cuenta por producto.
* Para `<product>`, enumere los grupos de compra con la intención y las puntuaciones del producto.
* Para `<product>`, enumere los personajes y las funciones con sus métricas de oportunidad (tasa de victorias, tasa de membresía, recuentos).
* Para las cuentas de `<industry>`, ¿cuál es el promedio de cobertura personal de la cuenta para `<product>`?
* ¿Qué cuentas tienen poca intención de cualquier producto pero aún tienen oportunidades abiertas (vale la pena nutrirlas)?
* ¿Qué cuentas agregaron nuevas señales de intención para `<account_name>` esta semana?

## Conceptos

| Concepto | Explicación |
| ------- | ----------- |
| Detección de audiencias | Entre bastidores, el agente observa las señales de intención de origen basadas en dos cosas: qué tan comprometidas están las personas con su marca y el tipo de personas que representan. El análisis repasa los últimos 18 meses de actividad para detectar la intención del producto en todos los usuarios de la cuenta, especialmente durante el tiempo previo al cierre de una oportunidad. Este análisis ayuda al agente a resaltar las personas que tienen más probabilidades de influir en el acuerdo.<br/><br/>A veces las cuentas no tienen todos sus datos de oportunidad en perfecta forma, lo cual está bien y el agente puede detectar la intención del producto únicamente a partir de patrones de participación. |
| Persona | Personas representa los tipos de personas que se relacionan con una cuenta. El agente lo crea mirando el cargo, la función y el nivel de antigüedad, y luego normalizando esa información para que sea coherente en las diferentes cuentas. De esa manera, en lugar de perderse en títulos desordenados, puede ver rápidamente si está llegando a los encargados de tomar decisiones, influenciadores o roles de soporte. Las personas le ayudan a comprender quién muestra interés, no solo cuánto interés hay. <br/><br/> Cuando el agente asigna personas a roles de grupo de compra, toma el tipo de persona identificada, según su cargo, función, antigüedad y cualquier otro atributo que elija agregar, y los alinea con los roles que tienen más probabilidades de desempeñar en una decisión de compra, como _encargado de tomar decisiones_, _influencer_ o _campeón_. Estas funciones son relevantes para el producto específico en cuestión, para que pueda ver quién importa más para esa oportunidad. El agente también muestra la cobertura de cada función, lo que le ayuda a comprender rápidamente qué funciones están bien representadas y dónde puede haber lagunas para rellenar su estrategia de participación. |
| Asignación de funciones de grupo de compra | Una vez que las personas se asignan a las funciones, las reúne en un grupo comprador. Piense en él como el equipo completo dentro de la cuenta que tiene más probabilidades de influir o decidir la compra. Cada rol (como _encargado de la toma de decisiones_, _influencer_ o _campeón_) agrega una parte de la imagen, para que tengas una visión clara de todo el comité que está impulsando el acuerdo. <br/><br/> Al asignar personas a roles de grupo de compra, toma el tipo de persona identificada, según su cargo, función, antigüedad y cualquier otro atributo que elija agregar, y los alinea con el rol que es más probable que desempeñen en una decisión de compra, como _encargado de tomar decisiones_, _influencer_ o _campeón_. Estas funciones son relevantes para el producto específico en cuestión, para que pueda ver quién importa más para esa oportunidad. El agente muestra la cobertura de cada función, lo que le ayuda a comprender rápidamente qué funciones están bien representadas y dónde puede haber lagunas para rellenar su estrategia de participación. |
| Grupos de compras | Los grupos de compra permiten a los especialistas en marketing gestionar la verdadera complejidad de los comités de compra, no las posibles clientes o las cuentas aisladas. Adobe Journey Optimizer B2B edition ofrece las herramientas (perspectivas impulsadas por IA, recorridos basados en roles y seguimiento de integridad) para aportar estructura, personalización y claridad analítica a ese proceso, lo que a la larga alinea más estrechamente el marketing y las ventas con los resultados de ingresos.<br/><br/>Crear un grupo de compra es realmente acerca de unir tres cosas clave: la audiencia correcta, el contexto del producto y los roles del grupo de compra. A continuación se muestra una vista previa paso a paso de cómo funciona: <ol><li>**Identifique a su audiencia** <ul><li>En primer lugar, el agente descubre las cuentas más relevantes para su producto. Este descubrimiento incluye cuentas que ya muestran interés y cuentas con potencial.<li>Dentro de estas cuentas, identifica a las personas (sus personalidades clave) que pueden influir en la decisión de compra o formar parte de ella.<li>Elige entre las cuentas que aparecen: una lista de cuentas o una audiencia de cuentas.</ul><li>**Considerar el contexto del producto**<ul><li>A continuación, examina el producto o la solución en los que se centra, lo que garantiza que las personas identificadas sean realmente relevantes para lo que desea vender o promocionar.<li>También ayuda a resaltar cualquier brecha en la cobertura (tal vez falten ciertas funciones para el producto) para que sepa dónde centrarse.</ul> <li>**Asignar perfiles a roles de grupo compradores** <ul><li>Por último, el agente asigna esas personas a funciones específicas de grupos de compra, como responsables de la toma de decisiones, influyentes y campeones.<li>En función de esta asignación, el agente puede recomendar una composición de grupo de compra para usted, que puede revisar, ajustar o confirmar.</ul> </ol> Cuando estos tres componentes se unen, crea su grupo de compra con detalles de miembros, funciones y perspectivas listas para usar. |
| Comprar grupos en un recorrido | Dentro de un recorrido, un grupo comprador puede utilizarse como unidad central de orquestación, lo que permite a los especialistas en marketing diseñar experiencias que se adapten a la dinámica del grupo en lugar de tratar a los miembros de forma aislada. Por ejemplo, puede dirigirse a todo el grupo con mensajes coordinados, y al mismo tiempo adaptar el contenido específico de la función a los responsables de la toma de decisiones, las personas influyentes o los usuarios finales. A medida que las señales de intención y los datos de participación fluyen en, los recorridos pueden ramificarse en función de la preparación del grupo, las alertas de superficie para las ventas cuando interactúan con funciones críticas o los pasos de nutrición del déclencheur automáticamente si faltan personas clave. Este flujo garantiza que cada punto de contacto (desde correos electrónicos hasta anuncios basados en cuentas o alcance de ventas) trabaje en conjunto para hacer avanzar al grupo en su proceso de compra, acelerando el consenso y reduciendo la fricción en el camino hacia la compra. |
| Recorridos en Journey Optimizer B2B edition | Un recorrido se puede crear con o sin un grupo de compra, pero el nivel de precisión y el impacto cambian significativamente:<ul><li>**Sin un grupo de compras**, los recorridos se suelen generar alrededor de las cuentas. Los especialistas en marketing pueden seguir utilizando señales como la intención, la conducta o el interés en un producto para fomentar los flujos y el alcance de los déclencheur. Este método funciona para movimientos más simples o cuando tiene datos limitados sobre una cuenta. Sin embargo, se corre el riesgo de pasar por alto el conjunto más amplio de partes interesadas que influyen en el acuerdo, lo que puede ralentizar la conversión o causar lagunas en la participación.<li>**Con un grupo comprador**, los recorridos se organizan en torno al conjunto completo de personas involucradas en una decisión de compra. Puede alinear los pasos con los hitos de nivel de grupo (como cuando el comité alcanza una puntuación de integridad o muestra un compromiso colectivo), al mismo tiempo que personaliza los puntos de contacto para cada función. Este método le permite diseñar una participación coordinada de varios subprocesos: un responsable de la toma de decisiones puede recibir contenido de retorno de la inversión estratégico, mientras que los influyentes reciben análisis exhaustivos del producto y se avisa a las ventas cuando interactúan funciones críticas. Al asignar el recorrido individual y colectivo, los especialistas en marketing y los vendedores pueden acelerar la creación de consenso y hacer que las oportunidades avancen de forma más eficiente. </ul> |
| Uso de datos de oportunidad para detectar un perfil | Para ofrecerle la visión más precisa de quién es atractivo y dónde se encuentran sus intereses, el agente aborda la clasificación personal y la intención del producto de acuerdo con lo siguiente: <ul><li>Caso más probable: si puede proporcionar datos como _Fase de oportunidad_, _Fecha de cierre de oportunidad_ y una _asignación de oportunidad a producto_ clara, el agente puede clasificar con confianza a las personas por producto.<li>Esta clasificación proporciona una comprensión precisa de la participación y el interés en toda la cuenta. </ul>Pero el agente sabe que los datos no siempre están completos, lo cual es correcto. Incluye retrocesos inteligentes para mantener las cosas en movimiento:<ul><li>El agente analiza el volumen de las actividades, dando más peso a las recientes utilizando la decadencia temporal.<li>Esta ponderación permite al agente diferenciar y clasificar personas, incluso sin datos de oportunidad completos. </ul>Cuando se trata de vincular oportunidades a productos, el agente se encarga de ello de la siguiente manera:<ul><li>_Ideal_: usted proporciona o ayuda al agente a crear la tabla de asignación.<li>_Si no está disponible_: el agente usa la coincidencia difusa para conectar los puntos.<li>_Sin vinculación_: el agente infiere la intención del producto en función de las actividades recientes anteriores a la fecha de cierre.</ul>Este enfoque por niveles garantiza que el agente pueda seguir ofreciendo perspectivas significativas, incluso cuando los datos no sean perfectos. |
| Análisis de oportunidad | El agente examina los datos de oportunidades históricas para comprender qué factores predicen más fuertemente una victoria y utiliza tres dimensiones principales para hacerlo:<ol><li>Tasa de victorias: muestra la frecuencia con la que se cierran correctamente las ofertas cuando participan determinadas personas. Si las cuentas con un patrón personal específico (como un evaluador técnico o un tomador de decisiones a nivel de vicepresidente) tienden a convertirse con más frecuencia, el modelo le da mayor peso a ese patrón. Esta información es un porcentaje del total de oportunidades, como las oportunidades cerradas o ganadas.<li>Tasa de pertenencia a grupos: mide la frecuencia con la que se muestra un tipo de persona en las oportunidades de un producto determinado. Si ciertas personas aparecen de forma consistente en las ofertas exitosas, esto indica que juegan un papel crítico en el proceso de compra.<li>Influencia personal: cuantifica cuánto contribuye una persona determinada al resultado, no solo si está presente, sino también cómo se correlaciona su nivel de participación o actividad con las ganancias.</ol>En conjunto, estas señales ayudan a deducir qué personas tienen el mayor impacto en los resultados de compra, incluso cuando los datos de oportunidad están incompletos. Con el tiempo, permite que el sistema muestre personalidades de alto impacto y patrones que son más predictivos del éxito de la operación, lo que a su vez informa la intención de la cuenta, el mapeo de personalidades y las recomendaciones de grupos de compra. |
| Intención | Cuando alguien visita una página web o hace clic en un vínculo de correo electrónico relacionado con un producto, es una señal de que está interesado y se llama _intención_.<br/><br/>El agente comienza con una taxonomía, que es básicamente una lista de los productos del cliente y las palabras clave que los describen. Esta información ayuda al agente a comprender de qué trata cada parte del contenido o interacción.<br/><br/>A continuación, el agente usa esa taxonomía para etiquetar la actividad del visitante, como las palabras clave o los productos a los que se relacionan sus acciones.<br/><br/>A continuación, el agente observa la profundidad con que se involucra alguien, como cuántas páginas visita o con qué frecuencia interactúa. Utiliza esta información para calcular la puntuación de intención individual para palabras clave, productos o categorías de productos específicos. Agrupa cada puntuación de intención en _Alta_, _Medium_ o _Baja_ para indicar la intensidad del interés. (Intención baja: `<=0.2`, intención de Medium: `0.2 < score <= 0.6`, intención alta: `0.6 < score <= 1`)<br/><br/>Por último, el agente combina las puntuaciones de intención de todas las personas de la misma compañía (cuenta) para ver la intención general a nivel de cuenta, mostrando qué productos o temas parecen interesar más a la compañía. |
| Funciones que influyen en un grupo comprador | Cada grupo comprador está formado por funciones que contribuyen de forma diferente a la decisión de compra, como _Decisionista_, _Influenciador_, _Campeón_ y _Usuario final_. Cada función tiene distintos grados de impacto.<br/><br/>Los encargados de tomar decisiones tienen la mayor influencia y generalmente controlan las aprobaciones presupuestarias. Los influenciadores modelan la evaluación y las recomendaciones. Los Campeones ayudan a crear un consenso interno, mientras que los Usuarios finales validan el ajuste del producto.<br/><br/>Al mostrarle estas funciones, el agente le ayuda a comprender quién es el responsable de la decisión de compra, dónde es más sólida su participación y dónde pueden existir brechas de cobertura. Esta información le permite centrarse en las funciones más importantes para este producto. |
| Cobertura de persona o función | Para cualquier producto dado, normalmente hay un conjunto de roles y personalidades clave que se sabe que influyen en la compra (_N_ personalidades o roles).<br/><br/>Para cada cuenta, el agente calcula la cobertura comprobando cuántos de esos roles de _N_ están representados por al menos una persona dentro de esa cuenta.<br/><br/>Si todos los roles de _N_ están presentes, la cuenta tiene cobertura total. Si solo se representan algunos roles, la cobertura es parcial.<br/><br/>En términos sencillos, la cobertura de funciones y personas mide la integridad del grupo de compra de un producto, en función de si se incluyen todas las personas que toman decisiones, influyentes y campeones importantes. |

## Requisitos previos de datos XDM

Audience Agent proporciona perspectivas sobre las cuentas que muestran la intención de origen de los productos y calcula el perfil y las funciones en función de los datos definidos. Asegúrese de que los siguientes datos previos estén configurados para utilizar las funciones de Audience Agent:

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
          <span>  Perfiles</span>
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
          <span>  Perfiles</span>
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
          <span>  Cuentas</span>
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
          <span>  Cuentas</span>
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
      <td>si la oportunidad está ganada (binaria)</td>
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
      <td>Solo para referencia/mantenimiento de libros; información sobre el ID de origen al que se dirige el correo electrónico</td>
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
      <td>Se utiliza para recuperar el contenido del correo electrónico del centro de datos de Marketo Engage; se compone de (SourceID@SourceInsatceID.SourceType)</td>
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
      <td>Solo para referencia/teneduría de libros; Información sobre el tipo de fuente o desde dónde se originó la fuente </td>
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
      <td>Información sobre el origen para el que se dirige el correo electrónico</td>
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
      <td>Solo para referencia/mantenimiento de libros; información sobre el ID de origen al que se dirige el correo electrónico</td>
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
      <td>Solo para referencia/teneduría de libros; Información sobre la instancia de origen a la que se dirige el correo electrónico</td>
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
      <td>Solo para referencia/contabilidad; se compone de (SourceID@SourceInsatceID.SourceType)</td>
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
      <td>Solo para referencia/teneduría de libros; Información sobre el tipo de fuente o desde dónde se originó la fuente</td>
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
