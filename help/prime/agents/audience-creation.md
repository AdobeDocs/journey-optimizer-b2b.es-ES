---
title: Crear audiencias para programas
description: Utilice la habilidad Creación de audiencias en Journey Optimizer B2B Prime para crear listas de personas, adaptar las listas inteligentes de Marketo y editar las reglas de listas en el chat.
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
autotag-review: '2026-06-25T19:19:21.361Z'
TQID: 'https://experienceleague.adobe.com/l3xd0u8LR0UDLfeGMXPEEJ9qwXPJX5DxkaH41W4Q7PE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0f014bd931324eb41e841a788ee4cf2058522455
workflow-type: tm+mt
source-wordcount: 1496
ht-degree: 1%

---

# Creación de audiencias para programas

En [!DNL Adobe Journey Optimizer B2B Prime], [_listas de personas_](../audiences/people-lists.md) definen la audiencia para los recorridos de personas, ya sea como listas dinámicas basadas en filtros que se actualizan automáticamente o como listas estáticas con pertenencia fija. Desde la [interfaz de chat](./chat-interface.md), la aptitud de _Creación de audiencias_ crea, adapta y edita listas de personas a través de una conversación guiada.

* **Habilidades** - `audience-creation` y `people-list-comparison`
* **Invocación**: describe los criterios de audiencia directamente, carga una lista inteligente [!DNL Marketo Engage] o nombra una lista existente para editar
* **Lee/escribe en** - [!DNL Journey Optimizer B2B Prime]; lee [!DNL Marketo Engage] al adaptar listas inteligentes

## Flujos de trabajo admitidos {#workflows}

El asistente admite tres flujos de trabajo y determina cuál se aplica a partir de la solicitud. Si su intención es ambigua, pregunta antes de continuar.

| Flujo de trabajo | Cuándo se debe utilizar | Mensaje de ejemplo |
|---|---|---|
| **Crear desde cero** | Desea una nueva lista de personas definida por criterios o pertenencia. | _&quot;Crear una lista dinámica de los VP de marketing en las empresas SaaS de Norteamérica&quot;._ |
| **Adaptar una lista inteligente [!DNL Marketo Engage]** | Ya tiene una lista inteligente [!DNL Marketo Engage] o una campaña inteligente y quiere una lista de personas equivalente. | _&quot;Adaptar esta lista inteligente de Marketo a una lista de personas.&quot;_ (adjuntar el recurso) |
| **Editar una lista existente** | Desea agregar o reemplazar las reglas de una lista que ya tiene. | _&quot;Agregar una regla a mi lista de &#39;Ensayos empresariales&#39; para obtener una puntuación de posibles clientes superior a 50.&quot;_ |

## Crear una lista de personas desde cero {#create-from-scratch}

Antes de generar nada, el asistente confirma las cuatro acciones siguientes. Solicita los que faltan, en un solo mensaje.

1. **Reglas / criterios**: una descripción en lenguaje sencillo de quién pertenece a la lista.
1. **Nombre** — Cómo llamar a la lista.
1. **Ubicación**: en qué programa debe residir la lista. Proporcione un nombre de programa y el asistente lo encontrará; si hay varias coincidencias, le pedirá que elija.
1. **Tipo**: dinámico (basado en filtros, actualización automática) o estático (pertenencia fija). Esto es obligatorio: el asistente no adivina; si no se especifica, pregunta.

### Listas dinámicas

Para las listas dinámicas, el asistente sugiere de forma proactiva incluir atributos de personalización para enriquecer la segmentación. Estos atributos están **_incluidos de forma predeterminada; usted decide excluirse, no en_**:

| Atributo | Por qué ayuda |
|---|---|
| **Persona derivada** | Comprador deducido por IA para la segmentación de contenido basada en persona. |
| **Intención derivada** | Señales de intención de compra deducidas que aparecen en las cuentas del mercado. |
| **Nivel de participación** | Nivel de participación calculado que prioriza los contactos comprometidos. |

Informe al ayudante si desea eliminar alguno de estos elementos antes de continuar.

### Listas estáticas

* **Estática, sin criterios**: la lista se crea vacía, lista para que pueda agregar miembros manualmente.
* **Estático a partir de los criterios (una instantánea)**: el Asistente de IA crea el conjunto coincidente y copia a esas personas en. La población es asíncrona: el asistente confirma que la lista se ha creado, pero observa que las personas pueden tardar unos minutos en aparecer. No alegará que la lista está lista inmediatamente.

## Revisar tarjeta {#review-card}

No se crea nada hasta que lo apruebe. Después de describir los criterios, el asistente presenta una tarjeta _Revisión de creación de lista de personas_ interactiva (para las adaptaciones de las listas [!DNL Marketo Engage], la tarjeta se titula _Revisión de conversión de lista de personas_).

Cada fila de la tarjeta representa una condición:

| Columna | Significado |
|---|---|
| **Requisitos** (o el nombre de lista [!DNL Marketo Engage] para adaptaciones) | Su solicitud original o el filtro de Marketo de origen. |
| **(regla)** | La regla basada en atributos real generada para esa condición. |
| **Incluir** | Casilla de verificación para mantener o eliminar esa regla. |

**Niveles de confianza:**

* **Las filas de alta confianza** coinciden perfectamente y se comprueban de forma predeterminada.
* Las filas **Baja confianza** (asignaciones aproximadas o cualquier elemento marcado) se muestran con un indicador de aviso y están desactivadas de forma predeterminada.
* Las filas que el sistema no pudo asignar muestran **&quot;No se encontró ningún equivalente&quot;**; no tienen regla y permanecen desmarcadas.

Un _resumen de conversión_ cuenta _N alta confianza_ y _N baja confianza_, con una sugerencia: las reglas de baja confianza están desactivadas de forma predeterminada; márquelas para incluir o describir el cambio que desee en el chat.

**Acciones de tarjeta:**

* **Continuar**: crea la lista utilizando únicamente las reglas seleccionadas.
* **Describa los cambios que desee en el chat**: rellena previamente la entrada con _&quot;Deseo cambiar: &quot;_ para que pueda perfeccionarlo; el Asistente para IA vuelve a generar y muestra una tarjeta nueva, conservando las reglas que ya había aprobado.

También puede escribir un seguimiento en cualquier momento (por ejemplo, _&quot;también restringido a compañías de más de 500 empleados&quot;_) y el Asistente de IA vuelve a generar la tarjeta.

## Asignación de atributos {#attribute-mapping}

Cuando describe criterios, el asistente traduce cada condición en un atributo real conocido de nivel de persona. En la tarjeta Revisar pueden aparecer tres resultados:

1. **Coincidente (alta confianza)**: su condición se asigna directamente a un atributo (por ejemplo, _&quot;el correo electrónico es acme.com&quot;_ se asigna al atributo `email`). Activada de forma predeterminada.
1. **Aproximado (poco fiable)**: el atributo disponible más cercano difiere en el nombre o el modelo de datos (por ejemplo, un filtro de Marketo _Cantidad_ aproximado como _Puntuación de posibles clientes_). Se muestra con una nota que explica la diferencia; desactivada de forma predeterminada.
1. **No encontrado** — La condición no se pudo asignar a ningún atributo conocido. Se muestra como _&quot;No se encontró ningún equivalente&quot;_; no se genera ninguna regla.

Por este motivo, es posible que una lista que describa vuelva con menos reglas que las condiciones especificadas: las condiciones no coincidentes aparecen explícitamente en lugar de perderse de forma silenciosa. Si los criterios importantes terminan como &quot;no encontrado&quot;, escríbalos utilizando el nombre real del atributo y el asistente volverá a intentarlo.

>[!NOTE]
>
>Si va a asignar columnas de hoja de cálculo a campos (una tarjeta de asignación de campos con _Columna Source_, _Campo de destino_, un porcentaje de confianza y una lista de _Columnas no asignadas_), ese es el flujo de importación de posibles clientes, no la creación de audiencias. Ver la [aptitud para importar posibles clientes](./skills.md#audiences-people).

## Editar reglas para una lista existente {#edit-rules}

Cuando solicita cambiar reglas en una lista que ya tiene, el asistente establece qué lista y qué modo de edición:

* **Agregar / anexar** (predeterminado para _&quot;agregar reglas&quot;_, _&quot;agregar más reglas&quot;_): las nuevas reglas se combinan con las existentes.
* **Reemplazar** (predeterminado para _&quot;reemplazar reglas&quot;_, _&quot;cambiar reglas a&quot;_): las nuevas reglas reemplazan todas las reglas existentes en la lista.

El asistente resume lo que se aplicará y establece claramente si se añade o reemplaza. A continuación, le pide que confirme antes de comprometerse. Después de la aplicación, informa del recuento total de reglas y de cuántas se añadieron o reemplazaron.

>[!NOTE]
>
>Las ediciones utilizan una ruta según la combinación, por lo que una operación &quot;añadir&quot; nunca sobrescribe de forma silenciosa las reglas existentes.

## Solapamiento de público {#overlap}

Solicite al Asistente de IA que compare listas de dos personas (por ejemplo, _&quot;Muéstreme la superposición entre &#39;Seminario web del tercer trimestre&#39; y &#39;Cuentas de empresa&#39;&quot;_) y procese una tarjeta _Superposición de lista de personas_:

* Distintivo de encabezado que muestra el recuento: **&quot;{N} en común.&quot;**
* Una fila de estadísticas con el recuento total de miembros de cada lista y la superposición como **&quot;X% de A · Y% de B.&quot;**
* Una tabla de miembros de las personas de ambas listas, con una columna **Nombre** y una segunda columna que puede dirigir: **Correo electrónico** (predeterminado), **Compañía** o **Puesto**, según lo que haya preguntado.
* Haga clic en cualquier nombre para abrir esa persona en el espacio de trabajo.
* Si no hay superposición, la tarjeta indica claramente: _&quot;No hay miembros en común entre estas dos listas.&quot;_

**Limitaciones:**

| Límite | Detalles |
|---|---|
| **Tamaño de tabla** | Muestra hasta 200 miembros; más allá de eso, anota _&quot;Mostrando 200 de N — pídeme que refine la consulta para reducir los resultados.&quot;_ |
| **Cálculo de superposición** | Se calcula según la dirección de correo electrónico; las personas sin correo electrónico se excluyen de la intersección. |
| **Tamaño de lista** | Lee hasta aproximadamente los primeros ~1,000 miembros de cada lista. Para listas más grandes, el asistente le informa de que los resultados son parciales. |
| **Listas dinámicas de borrador** | No se puede comparar: una lista que no se ha publicado no tiene ningún segmento activo. El asistente le pedirá que lo publique primero o que utilice una lista estática en su lugar. |

## Validación de QA {#qa-validation}

Después de crear o actualizar una lista, el Asistente de IA ofrece: _&quot;¿Desea que compruebe que la lista está configurada correctamente?&quot;_ Si acepta, recupera la lista e informa de las siguientes comprobaciones:

| Marque | Resultado |
|---|---|
| La lista se encuentra en el programa o la carpeta correctos | Aprobado/suspenso |
| El recuento de filtros coincide con lo que se aplicó | _N_ filtros / no coinciden |
| Atributos de Personalization presentes (si se incluyen) | Presente/ausente |
| El nombre de la lista coincide con lo solicitado | Aprobado/suspenso |
| Recuento estimado de miembros | _count_ o N/A |

## Limitaciones {#limitations}

| Limitación | Detalles |
|---|---|
| **Adaptación de lista estática de[!DNL Marketo Engage]** | No puede adaptar una lista estática [!DNL Marketo Engage] (o un correo electrónico u otro recurso sin filtro) a una lista de personas. Las listas estáticas son ID de miembro explícitos y no se pueden expresar como filtros; en su lugar, el asistente solicita una lista inteligente o una campaña inteligente. |
| **Filtros basados en la actividad y la pertenencia** | Al adaptarse de [!DNL Marketo Engage], los filtros como _Se abrió el correo electrónico_, _Se completó la página web visitada_, _Se rellenó el formulario_, _Miembro de la lista_ y _Miembro de la campaña inteligente_ no tienen equivalente de lista de personas y regresan como &quot;No se encontró un equivalente&quot;. |
| **Condiciones a nivel de compañía** | Se traduce al atributo de nivel de persona más cercano siempre que sea posible (las listas de personas funcionan con atributos de persona) y se marca como de baja confianza cuando el ajuste es holgado. |
| **Lógica AND/OR profundamente anidada** | La lógica anidada compleja puede contraerse a un AND/OR de nivel superior; el asistente observa esto cuando se produce. |
| **Conflictos de nombres** | No se resuelve automáticamente: si se usa el nombre, el asistente le pedirá uno distinto en lugar de anexar silenciosamente un sufijo. |
| **Se requiere aprobación** | El asistente no creará ni modificará una lista hasta que haga clic en **[!UICONTROL Continuar]**, confirme o dé un visto bueno claro (_&quot;aprobado&quot;_, _&quot;se ve bien&quot;_, _&quot;compilarlo&quot;_). |
| **Población de instantáneas estáticas** | La pertenencia a listas estáticas creadas a partir de criterios se completa en unos minutos, no de forma inmediata. |
