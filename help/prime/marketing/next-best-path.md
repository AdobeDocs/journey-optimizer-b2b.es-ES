---
title: Siguiente nodo de mejor ruta
description: Utilice el nodo Siguiente mejor ruta en Journey Optimizer B2B Prime para el enrutamiento de recorrido impulsado por IA con indicadores de lenguaje natural, simulación de ruta, puntuaciones de confianza y resultados de ruta dividida en directo.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-12T23:02:18.769Z'
TQID: 'https://experienceleague.adobe.com/OCsqXogJ7C1u2iKrmI9O2ZCPi3FC9xKSU-uIa-Ngki8'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ff10f619-348f-47e3-99bf-3ce4c817cf2cid: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 2205
ht-degree: 0%

---

# Siguiente nodo de mejor ruta

En Journey Optimizer B2B Prime, el nodo *Siguiente mejor ruta* incorpora la toma de decisiones de ruta dividida impulsada por IA directamente en el lienzo de recorrido. En lugar de configurar las condiciones de filtro en un nodo [rutas divididas](./split-merge-paths-nodes.md), describirá la intención en lenguaje natural y permitirá que el sistema determine la ruta más relevante para cada persona.

En las compras B2B, un perfil puede parecer un tipo de comprador, pero su comportamiento, los datos firmográficos y el contexto de participación revelan una historia con más matices. El siguiente nodo de mejor ruta evalúa ese contexto para tomar una decisión de enrutamiento inteligente, al tiempo que le permite revisar, modificar o anular cualquier recomendación de IA antes de activar el recorrido.

## Path Decisioning {#path-decisioning}

Hay tres pasos para pasar de la intención a la activación.

* **Paso 1: Defina las rutas**: agregue un nodo de la siguiente mejor ruta al recorrido, asigne un nombre a cada ruta y escriba un mensaje en lenguaje natural que describa quién debe avanzar por la ruta. Puede añadir o quitar rutas de acceso en cualquier momento.

* **Paso 2: Simular** — Elija una audiencia de muestra y ejecute una simulación. Verá recuentos de perfiles por ruta, puntuaciones de confianza y el razonamiento de IA para que pueda validar la lógica antes de activarla.

  >[!NOTE]
  >
  >La simulación se ejecuta únicamente con datos de muestra y nunca afecta a la ejecución del recorrido en directo.

* **Paso 3: Activar** — Publica el recorrido en tu audiencia real. La IA evalúa a cada persona en tiempo de ejecución, asigna la ruta más adecuada en tiempo real y una alternativa predeterminada garantiza que nadie llegue a un callejón sin salida.

### Entradas de decisiones de IA {#ai-decisioning-inputs}

Cuando una persona llega al nodo, el sistema obtiene el contexto de perfil, aplica restricciones y utiliza un LLM para seleccionar la ruta que mejor se ajuste. La inteligencia artificial evalúa a cada persona mediante una combinación de las siguientes aportaciones:

* **Historial de participación**: aperturas de correo electrónico, clics en vínculos, visitas a páginas web y otras señales de comportamiento de los recorridos actuales y anteriores
* **Señales en tiempo real**: eventos de alta intención, como rellenos de formularios y visitas a la página de precios
* **Atributos de perfil** - Datos demográficos, de puesto, personales y firmográficos
* **Atributos de cuenta**: datos firmográficos y tecnológicos asociados con la cuenta de la persona

### Creación de contexto de IA {#ai-context-building}

Tras la decisión de enrutamiento, la IA crea una capa deducida para cada perfil. Combina datos demográficos y firmográficos, detalles de la cuenta y señales de comportamiento (como detalles personales, intención del problema e intención del producto) en un resumen contextual para esa persona. Con este contexto enriquecido, la IA puede dirigir a cada persona hacia el camino óptimo y proporcionar una puntuación de confianza y el razonamiento en lenguaje natural detrás de cada decisión.

Cada decisión se registra con una puntuación de confianza y un razonamiento en lenguaje natural para la transparencia y la observabilidad.

Si ninguna ruta es una coincidencia sólida o si el mensaje hace referencia a datos no disponibles para un perfil, la persona se enruta a la ruta de reserva predeterminada.

## Añadir un siguiente nodo de mejor ruta {#add-node}

1. Abra el recorrido de persona y vaya al mapa del recorrido.

1. Haga clic en el icono de signo más ( **+** ) en una ruta y elija **Siguiente mejor ruta**.

   El nodo se añade al lienzo y el panel de configuración de la división AI se abre a la derecha. Comienza con una ruta y una ruta predeterminada *Otras personas* para dirigir a las personas que no cumplen los requisitos para ninguna de las rutas definidas.

## Configuración de rutas {#configure-paths}

Para cada ruta, defina un nombre y una petición de datos en lenguaje natural que describa a quién se debe dirigir allí. La entrada del mensaje reemplaza por completo la interfaz de usuario de la condición de filtro; no hay condiciones de atributo que configurar.

1. Haga clic en **Agregar ruta** para cada ruta adicional que desee incluir.

   Para quitar una ruta, haga clic en el icono *Eliminar* de la tarjeta de ruta.

1. Para cada tarjeta de ruta del panel derecho:

   * Escriba una **Etiqueta** que refleje la audiencia o la intención de ese segmento.

   * Escriba un **indicador** en lenguaje natural que describa quién pertenece a esta ruta. Céntrese en la intención y el resultado, no en los valores de atributo específicos.

     **El ejemplo solicita una división de tres rutas:**

      * *Ruta 1 - Líderes de RRHH:* Identifique a las personas en roles de liderazgo de RRHH que tienen más probabilidades de involucrarse con la administración de talentos y el contenido de experiencia de los empleados.
      * *Ruta 2 - Evaluadores técnicos:* Identifique a las partes interesadas técnicas que tienen más probabilidades de interactuar con la arquitectura del producto, las integraciones y el contenido de implementación.
      * *Ruta 3 - Responsables de la toma de decisiones empresariales:* Identifique a las partes interesadas empresariales que tienen más probabilidades de interactuar con el retorno de la inversión, los resultados empresariales y el contenido de los estudios de casos.

1. Si es necesario, reordene las rutas para establecer el orden de prioridad de las coincidencias.

   El filtrado de rutas se evalúa en orden descendente. Cada persona continúa por el primer camino que coincida. Haga clic en las flechas arriba y abajo en la parte superior derecha de cada tarjeta de ruta para moverla hacia arriba o hacia abajo en la lista.

1. Revise la ruta predeterminada (la última de la lista de rutas) y cambie la etiqueta si es necesario.

   La ruta predeterminada se utiliza cuando la IA no puede asignar una persona con seguridad a ninguna ruta definida o cuando los datos relevantes no están disponibles. Cuando una solicitud hace referencia a datos que no existen en el conjunto de datos para un perfil determinado, el sistema enruta ese perfil a la ruta predeterminada e indica el intervalo de datos.

>[!BEGINSHADEBOX]

**Controles humanos en el bucle**

Las recomendaciones de IA no son vinculantes. Antes de activar el recorrido, puede:

* Edite cualquier petición de ruta para restringir la lógica de enrutamiento.
* Agregar, quitar o reordenar rutas.
* Anule las sugerencias de IA con condiciones personalizadas según sea necesario.

Las asignaciones de rutas controladas por IA no surtirán efecto hasta que publique el recorrido.

>[!ENDSHADEBOX]

## Solicitar ejemplos por caso de uso {#prompt-examples}

Los siguientes ejemplos muestran cómo escribir indicadores de ruta efectivos en casos de uso comunes de marketing B2B. Utilícelos como punto de partida y adapte el idioma para que coincida con el contexto de recorrido y los datos de audiencia.

+++Señales activas de investigación y compra

**Ruta 1 - Investigadores activos de productos**
*Identifique a las personas que investigan activamente el software CRM. Busque visitas repetidas a la página del producto, participación con contenido de comparación, visitas frecuentes de retorno y señales de intención de terceros elevadas durante los últimos 30 días.*

**Ruta 2 - Comportamiento de comparación de precios**
*Identifique a los usuarios que hayan visto páginas de comparación de precios o planes varias veces en los últimos 14 días, especialmente los que alternan entre páginas de precios y de documentación de características.*

**Ruta 3 - Intento alto, sin conversión**
*Identifique a los visitantes con intenciones altas que hayan participado en demostraciones de productos, páginas de precios o documentación de integración en los últimos 21 días, pero que no hayan enviado un formulario ni se hayan convertido.*

**Ruta 4 - Comportamiento de cierre de compra dudoso**
*Identifique a los usuarios que iniciaron flujos de reservas de cierre de compra o de demostración, pero no los completaron y que regresaron al menos una vez después sin realizar la conversión.*

+++

+++Riesgo de pérdida y retención

**Ruta 1 - Señales de riesgo de pérdida**
*Identifique a los clientes que muestran signos de pérdida en función del menor uso del producto, la menor frecuencia de inicio de sesión, los picos en los tickets de asistencia y la disminución de la participación de marketing en los últimos 60 días.*

**Ruta 2 - Desvincular usuarios avanzados**
*Identifique a los usuarios comprometidos anteriormente cuya velocidad de interacción ha disminuido significativamente en los últimos 30 días en comparación con su línea de base histórica.*

+++

+++Educación a las brechas de evaluación

**Ruta 1: investigación de la secuencia de precios**
*Identifique a los usuarios que descargaron un libro electrónico y luego visitaron la página de precios en un plazo de 7 días, pero que no solicitaron una demostración.*

**Ruta 2 - Seminario web sin seguimiento**
*Identifique a las personas que asistieron a un seminario web y posteriormente regresaron a las páginas de productos, pero nunca reservaron una demostración ni contactaron con las ventas.*

**Ruta 3 - Evaluación basada en comparación**
*Identifique a los visitantes que vieron un artículo de comparación de competidores y luego visitaron la documentación de integración o migración en un plazo de 14 días.*

+++

+++Secuencias de participación de correo electrónico

**Ruta 1: se abre sin clics**
*Identifique a los posibles clientes que abrieron tres o más correos electrónicos de marketing en un plazo de 30 días pero que nunca hicieron clic en el sitio web.*

**Ruta 2 - Se hizo clic pero no hay participación más profunda**
*Identifique a los usuarios que hicieron clic desde un correo electrónico hasta una página de producto, pero que no exploraron páginas adicionales ni regresaron en un plazo de 7 días.*

+++

+++Patrones de prueba y conversión

**Ruta 1 - Convertidores rápidos**
*Identifique a los clientes que se actualizaron dentro de los 30 días posteriores al inicio de una prueba y que mostraron una alta participación en el producto durante el período de prueba.*

**Ruta 2 - Usuarios de prueba bloqueados**
*Identifique a los usuarios de prueba que iniciaron sesión durante la primera semana pero mostraron una actividad mínima posteriormente y no se convirtieron antes de la caducidad de la prueba.*

+++

+++Compradores multicanal

**Ruta 1 - Convergencia de anuncios y orgánica**
*Identifique a los usuarios que primero se comprometieron a través de anuncios pagados y luego regresaron a través de canales directos u orgánicos en un plazo de 14 días.*

**Ruta 2 - Evaluación de evento a producto**
*Identifique las cuentas que participaron en un evento personal o virtual y que posteriormente aumentaron el comportamiento de la investigación de productos en un plazo de 30 días.*

**Ruta 3 - Investigadores de medios sociales a sitios**
*Identifique a los usuarios que interactuaron con el contenido social y más tarde visitaron páginas con intenciones altas, como precios o reservas de demostración.*

+++

+++Señales de compra regionales

**Ruta 1 - Marejada en una región específica**
*Identifique cuentas en Norteamérica que muestren una mayor actividad de investigación de productos y señales de intención de terceros elevadas en los últimos 30 días en comparación con su línea de base histórica.*

**Ruta 2 - Impulso de los mercados emergentes**
*Identifique las cuentas en APAC donde la velocidad de participación haya aumentado significativamente en los últimos 14 días, incluso si el volumen de participación general sigue siendo moderado.*

**Ruta 3 - Interés empresarial específico de la región**
*Identifique las cuentas de tamaño empresarial en EMEA que se involucren con la documentación de cumplimiento, residencia de datos o seguridad en los últimos 21 días.*

**Ruta 4 - Territorio subpenetrado**
*Identifique las cuentas de alta adecuación en los territorios de ventas asignados que han mostrado señales de intención pero que las ventas aún no han contactado.*

+++

+++Segmentación de audiencia de seminario web

**Ruta 1: líderes de RRHH interesados en IA**
*Identifique a las personas que han participado en sitios de RRHH (shrm.org, hbr.org/topic/human-resource-management), interesadas en Journey Optimizer en los últimos 30 días y que probablemente asistan a un seminario web sobre &quot;IA en operaciones de RRHH&quot;. También deberían haber mostrado algún interés en los productos de IA.*

**Ruta 2 - Profesionales de finanzas interesados en IA**
*Identifique a las personas que hayan participado en sitios de finanzas (wsj.com/finance, investopedia.com), interesadas en Marketo en los últimos 30 días y que probablemente asistan a un seminario web sobre &quot;IA en la planificación financiera&quot;. También deberían haber mostrado algún interés en los productos de IA.*

**Ruta 3 - Profesionales de riesgos e investigación interesados en IA**
*Identifique a las personas que hayan participado en los sitios de Riesgo/Investigación (mckinsey.com/capabilities/risk-and-resilience, forrester.com/research), interesadas en GenStudio en los últimos 30 días y que probablemente asistan a un seminario web sobre &quot;IA en la gestión de riesgos&quot;. También deberían haber mostrado algún interés en los productos de IA.*

+++

+++Señales de temporización de comportamiento

**Ruta 1 - Investigadores fuera de horario**
*Identifique a los usuarios que interactúan repetidamente con las páginas de productos y precios fuera del horario laboral normal en su huso horario local.*

**Ruta 2 - Ventana de investigación comprimida**
*Identifique las cuentas que muestren una densidad de participación inusualmente alta en un breve período de 72 horas en varias áreas de productos.*

**Ruta 3 - pico de actividad al final del trimestre**
*Identifique cuentas con un aumento en la actividad de la fase de evaluación durante los últimos 30 días del trimestre fiscal.*

+++

## Simular la toma de decisiones antes de publicar {#simulate}

Utilice la simulación para probar cómo la IA evalúa los indicadores con respecto a una audiencia real antes de que el recorrido se active. La simulación solo está disponible mientras el recorrido esté en estado *Borrador* y no tiene efecto en ningún recorrido publicado.

### Ejecución de una simulación {#run-simulation}

1. Seleccione el siguiente nodo de mejor ruta y haga clic en el icono *Simular* en la parte superior del panel derecho.

1. En el cuadro de diálogo, elija la audiencia que desea utilizar para la simulación:

   * **[!UICONTROL Listas de personas originales]**: use la audiencia del nodo de audiencia. Especifique un tamaño de muestra cuando la audiencia completa supere el umbral de simulación.
   * **[!UICONTROL Listas dinámicas y estáticas]**: use una lista estática o dinámica de Marketo Engage.
   * **[!UICONTROL Registros de pruebas]** - Usar perfiles de prueba sugeridos por IA.

   >[!NOTE]
   >
   >* Si la audiencia seleccionada supera el umbral de simulación, el sistema ejecuta la simulación en una muestra de 100 perfiles. Un indicador en la IU muestra que los resultados se basan en muestras.
   >* Si la audiencia seleccionada aún no se ha materializado, la simulación se bloquea. Una advertencia en línea le indica que primero debe materializar la audiencia.

1. Haga clic en **[!UICONTROL Simular]**.

### Revisar resultados de simulación {#review-results}

Después de ejecutar la simulación, el panel derecho muestra la distribución de perfiles en cada ruta y el razonamiento de IA detrás de esas asignaciones:

| Resultado | Descripción |
|---|---|
| **Perfiles** | El número de perfiles enrutados a la ruta. |
| **División** | El porcentaje de perfiles enrutados a la ruta. |
| **Confianza** | Nivel de confianza de IA para la asignación de ruta. La confianza refleja la actualización de los datos, la intensidad y la coherencia de la señal y el éxito histórico de patrones de enrutamiento similares. |
| **Mensaje** | El indicador que se evaluó para la ruta. |
| **Razonamiento de IA** | Una explicación en lenguaje natural de por qué los perfiles se asignaron colectivamente a esta ruta. |

>[!NOTE]
>
>Cuando los datos disponibles o el alcance limitan una decisión, los resultados incluyen información sobre la limitación. Por ejemplo, cuando un atributo requerido no está presente en el conjunto de datos, los resultados incluyen un indicador explícito que explica cómo los datos que faltan afectaron a los resultados.

Utilice los resultados para restringir las peticiones de datos y confirmar que la ruta refleja el resultado deseado. Puede modificar los indicadores de ruta y volver a ejecutar la simulación tantas veces como sea necesario antes de publicar.

## Publicación y monitorización del recorrido {#publish-monitor}

Después de validar los resultados de la simulación:

1. Conecte la audiencia de personas al nodo de entrada de recorrido.

2. [Publicación del recorrido](./journeys-overview.md).

Una vez que el recorrido está activo, el siguiente nodo de mejor ruta se ejecuta en el momento de la ejecución. A medida que cada persona llega al nodo, la IA los evalúa en tiempo real utilizando las señales más recientes y los enruta hacia la ruta más relevante.

Para un recorrido publicado, abra el mapa del recorrido y seleccione el siguiente nodo de mejor ruta para ver la sección **_[!UICONTROL Resultados en directo]_** en el panel derecho. Los resultados en directo muestran:

* La distribución porcentual de perfiles en cada ruta
* La puntuación de confianza para cada asignación de ruta
* Razonamiento a nivel de ruta y de perfil, con detalles ampliables para perfiles individuales

Los resultados en directo también están disponibles en la consola de Recorrido y a través de la habilidad de observación de Recorrido en el centro de IA.