---
title: Calificador de ventas
description: Automatice la calificación y alcance de clientes potenciales B2B con el Calificador de ventas. Proporciona investigación basada en IA, redacción de correos electrónicos, integración de CRM y flujos de trabajo salientes de IA para BDR.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
exl-id: cc590444-41df-44fe-830b-92241718ee81
autotag-review: '2026-06-05T16:42:16.451Z'
TQID: 'https://experienceleague.adobe.com/VNgs0cTpjCTG7JpFjFErnVMmRtR-gmw-iRRHZanZDUs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: fc1ff3b2-6614-41ad-a113-de48597598fd
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
subfeature_v2:
  - id: fe583b80-65a2-48c2-b4e1-9ea8fbac0a8a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a5145b53d6b5c9462392f7c540a81b7d85abdd7b
workflow-type: tm+mt
source-wordcount: 6084
ht-degree: 1%

---

# Calificador de ventas

El cualificador de ventas es una aplicación controlada por IA que puede utilizar con Adobe Journey Optimizer B2B edition. Implementa Account Qualification Agent y está diseñado para optimizar los flujos de trabajo para los representantes de desarrollo empresarial (BDR). El Cualificador de ventas automatiza los flujos de trabajo de cualificación de clientes potenciales, alcance y participación del comprador en todos los canales. Reduce la carga manual de BDR y acelera la velocidad de la canalización para las empresas B2B empresariales.

Los BDR pueden utilizar los complementos de explorador y correo electrónico para acceder a inteligencia empresarial directamente desde CRM o Outlook. El siguiente vídeo proporciona una breve demostración del Cualificador de ventas y Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476550)

## Inicio de aplicación

El Calificador de ventas se incluye con [!UICONTROL Journey Optimizer B2B edition], pero es una aplicación independiente dentro de Adobe Experience Platform.

![Pantalla de inicio del calificador de ventas](./assets/home-screen.png){width="800" zoomable="yes"}

### Account Qualification Agent

Account Qualification Agent (AQA) es el núcleo del Calificador de ventas. El AQA utiliza IA para leer sus cuentas y determinar cuáles están listas para el siguiente paso. Ayuda con la investigación, el borrador del correo electrónico y el contexto informado sobre CRM cuando su organización se ha conectado a CRM.

<!--
## Edit the left navigation bar

At the bottom left of the application, click the _Edit_ ( ![Edit icon](../assets/do-not-localize/icon-edit.svg) ) icon to control which elements are visible in the left navigation. You can also drag and drop them to reorder as you want.
-->

### Uso básico del agente

Los agentes de Adobe AI usan _consultas en lenguaje natural_, lo que significa que usan el mismo idioma en el mensaje de texto que cuando se habla con una persona. Cuanto más detallado sea, mejores serán los resultados.

Con el lenguaje natural, puede pedir al agente que:

* `Tell me the latest financial results of Bodea`
* `Tell me more about hiring at TechNova`
* `Tell me about the new AI features in Bodea LumaSecure4`

Itere los flujos de trabajo salientes refinando los indicadores para obtener los resultados que necesita. Por ejemplo:

* _Borrador de un dibujo de seguimiento de correo electrónico a partir de contexto, como llamadas de ganancias o informes._ Hasta 120 palabras. Línea de asunto: cautivador, que incorpora un tema clave. Introducción: Comience con una cita directa de las fuentes de contexto. Cuerpo: conéctese a puntos problemáticos y propuestas de valor. CTA: Proponga una breve llamada para explorar más en profundidad._

* _El objetivo de este correo electrónico es iniciar una conversación y generar credibilidad._ Redacte un correo electrónico con menos de 120 palabras que tenga un tono consultivo y empático. Evite un enfoque demasiado familiar o de ventas y no utilice las frases &quot;espero que esté bien&quot;, &quot;solo registrarse&quot; o &quot;por favor&quot;._

### Acceso a productos y grupos de usuarios

El acceso a las funciones del cualificador de ventas se administra mediante dos grupos de usuarios en Adobe Admin Console. Los administradores de productos deben configurar los grupos durante la incorporación para que los usuarios puedan acceder a la aplicación.

#### Usuarios del calificador de ventas

Los usuarios deben ser miembros del grupo de usuarios `Sales Qualifier` para tener acceso a la aplicación Calificador de ventas.

1. En Adobe Admin Console, cree un grupo de usuarios denominado `Sales Qualifier`.
1. Asigne el perfil de AEP **Acceso predeterminado a todos los equipos de producción** al grupo.
1. Añada usuarios que necesiten acceder al cualificador de ventas.

#### Administradores de cualificador de ventas

Los administradores que configuran [conexiones CRM](#integrations-and-crm), el [Centro de conocimiento](#knowledge-center) y la configuración global de exclusión de correo electrónico también deben ser miembros del grupo de usuarios `Sales Qualifier Admins`.

1. En Adobe Admin Console, cree un grupo de usuarios denominado `Sales Qualifier Admins`.
1. Agregue los administradores a los grupos `Sales Qualifier` y `Sales Qualifier Admins`.

La pertenencia a ambos grupos hace que **[!UICONTROL Configuración de administración]** sea visible en **[!UICONTROL Administración]** en el panel de navegación izquierdo. Los usuarios estándar pueden utilizar los campos, los filtros y el manual configurados, y el pie de página de exclusión configurado se aplica a sus correos electrónicos salientes. No pueden cambiar esta configuración.

>[!NOTE]
>
>Los nombres de los grupos de usuarios deben coincidir exactamente como se muestra en los pasos anteriores.

## Clientes potenciales

Seleccione **[!UICONTROL Clientes potenciales]** en el panel de navegación izquierdo para ver una lista de los posibles clientes a los que puede acceder. La lista proporciona una revisión rápida de la información, como el estado del posible cliente y la última actividad.

![Tabla de clientes potenciales que muestra el estado del posible cliente y la última actividad para la administración de clientes potenciales](./assets/prospects.png){width="800" zoomable="yes"}

### Crear su lista de clientes potenciales

La lista de clientes potenciales combina personas de más de una fuente:

* **Clientes potenciales con origen en CRM**: cuando conecta un CRM, importa automáticamente los posibles clientes que sean propiedad del usuario conectado. Consulte [Integraciones y CRM](#integrations-and-crm).
* **Perspectivas importadas**: importe una lista de posibles clientes desde un archivo CSV.
* **Clientes potenciales agregados manualmente**: agregue una persona individual directamente en la aplicación.

Para agregar clientes potenciales que no provienen de su CRM:

1. En la página **[!UICONTROL Clientes potenciales]**, seleccione **[!UICONTROL Agregar clientes potenciales]**.
1. Elija **[!UICONTROL Importar CSV]** o **[!UICONTROL Agregar manualmente]**.

   * Para una importación CSV, cargue el archivo y asigne sus columnas a los campos del cliente potencial.
   * Para añadir a una persona manualmente, introduzca sus detalles en el formulario.

1. Seleccione **[!UICONTROL Guardar]**.

### Filtrado y búsqueda de clientes potenciales

Seleccione el icono _Filtrar_ ![Icono de filtro](../../assets/do-not-localize/icon_filter-outline.svg) para reducir la lista. Puede filtrar por:

* Estado del posible cliente
* Puntuación de participación
* Momentos interesantes marcados por marketing
* Puntuación de estrellas y puntuación de llamas
* Ofertas asociadas

Los administradores también pueden hacer que los campos CRM asignados estén disponibles como filtros. En **[!UICONTROL Configuración de administración]**, activan **[!UICONTROL Filtrable]** para los campos que los representantes usan para encontrar clientes potenciales. Ver [Asignar campos CRM](#map-crm-fields-inbound-mapping).

### Revisar detalles del cliente potencial

Seleccione un cliente potencial para abrir su perfil. Revise las señales que importan antes de ponerse en contacto con:

* **Lista de actividades**: una lista cronológica de las actividades del posible cliente, con un **resumen de actividad de IA** en la parte superior que resalta el comportamiento reciente más relevante.
* **Vista de cronología**: una cronología visual de la participación en todos los canales.
* **Contenido visualizado**: abra el contenido real que vio un cliente potencial, como una página web o un recurso, directamente desde una actividad.

## Cuentas

Seleccione **[!UICONTROL Cuentas]** en la sección de navegación izquierda para trabajar con las cuentas que vende en. El Cualificador de ventas aúna detalles firmográficos, canalización y participación para que pueda priorizar el alcance a nivel de cuenta.

La descripción general de la cuenta resume aspectos básicos como ingresos, sector, tamaño de la empresa y sede central. Junto a estos detalles, aparece cada cuenta:

* **Oportunidades de apertura**: las oportunidades de apertura asociadas con la cuenta, que provienen de su CRM conectado, para que pueda alinear el alcance con la canalización activa.
* **Miembros con mayor participación**: los contactos de la cuenta con la participación más reciente para que sepa a quién priorizar dentro del grupo comprador.
* **Entradas de CRM**: campos de cuenta, oportunidades e información de propietario aparecidos en su CRM conectado. Consulte [Integraciones y CRM](#integrations-and-crm) para ver cómo se asignan estos datos.

### Análisis profundo de la cuenta

Para comenzar una inmersión profunda, abra una cuenta. Account Qualification Agent (AQA) da prioridad a las señales que son más relevantes para la estrategia de venta de su organización, de modo que pueda comprender rápidamente cuál es la situación de la cuenta y decidir qué hacer a continuación.

## Flujos de trabajo salientes

>[!NOTE]
>
>Los flujos de trabajo salientes creados por los administradores de productos se comparten con todos los usuarios de su organización.

Un _flujo de trabajo saliente_ es la estructura que usa el calificador de ventas para ejecutar una cadencia guiada por objetivos. Usted define un objetivo de alcance y criterios de segmentación, y la IA propone una cadencia multitáctil y escribe contenido de correo electrónico personalizado para cada cliente potencial. Revise y apruebe cada correo electrónico antes de que la inscripción active la cadencia, de modo que los mensajes se envíen únicamente durante la ventana configurada.

Un flujo de trabajo saliente conecta cuatro elementos:

* **Objetivo**: el resultado que desea obtener del alcance (por ejemplo, reservar una llamada de contacto o registrar un evento de conducción).
* **Filtros de segmentación**: condiciones que determinan qué clientes potenciales son elegibles.
* **Cadencia de puntos de contacto**: la secuencia ordenada de pasos, cada uno en un día programado. Los puntos de contacto pueden ser **correos electrónicos**, **llamadas telefónicas** o **InMails de LinkedIn**.
* **Contenido de correo electrónico personalizado**: para cada punto de contacto de correo electrónico, la inteligencia artificial aplicada crea borradores de contenido usando el perfil del posible cliente, el contexto de la cuenta, el historial de participación y las noticias recientes.

El objetivo impulsa todo hacia abajo: la IA lo utiliza para sugerir filtros de direccionamiento, diseñar la cadencia, dibujar indicadores de punto de contacto y dar forma a la personalización para cada correo electrónico generado.

![Ficha Información general del flujo de trabajo saliente](./assets/outbound-workflow-overview.png){width="800" zoomable="yes"}

### Conceptos clave

| Concepto | Descripción |
| --- | --- |
| **Flujo de trabajo** | Una actividad saliente reutilizable definida por un objetivo, filtros de objetivo, cadencia y configuración. |
| **Meta** | Lo que debe lograr el alcance. |
| **Punto de contacto** | Un paso en la cadencia (correo electrónico, llamada de teléfono o LinkedIn In InMail), programado en relación con la inscripción. |
| **Mensaje de Touchpoint** | Instrucciones que sigue la IA al generar el cuerpo y el asunto del correo electrónico para un cliente potencial: tono, longitud, enfoque y call to action. |
| **Cadencia** | La secuencia completa de puntos de contacto: cuántos, en qué orden y en qué días. |
| **Filtro de segmentación** | Condición que limita el flujo de trabajo a un subconjunto de posibles clientes. |
| **Borrador** | Un correo electrónico generado que está listo para revisarse, pero aún no se ha aprobado. |
| **Razonamiento** | La explicación de la IA de cómo escribió un correo electrónico determinado (qué señales y fuentes de datos utilizó). |
| **Inscripción** | Aprobación de los borradores de un cliente potencial, que activa la cadencia y pone en cola los correos electrónicos que se enviarán durante la ventana de envío del flujo de trabajo. |

Las secciones siguientes describen el ciclo de vida completo: creación de un flujo de trabajo en el asistente, revisión de correos electrónicos generados, aprobación de clientes potenciales y administración de flujos de trabajo a lo largo del tiempo.

### Creación de un flujo de trabajo saliente

La creación del flujo de trabajo es un asistente de cinco pasos: **Objetivo**, **Segmentación**, **Generar puntos de contacto**, **Configuración** y **Agregar perspectivas**. Cada paso se basa en el último; su objetivo inicial moldea cada decisión posterior.

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Flujo de trabajo saliente]**.

1. En la ficha **[!UICONTROL Examinar]**, haga clic en **[!UICONTROL + Crear flujo de trabajo]** en la esquina superior derecha.

#### Paso 1: Defina su objetivo

El objetivo es la entrada más importante: indica a la IA el aspecto del éxito y ancla el direccionamiento, la cadencia y la generación de correo electrónico.

1. Elige **[!UICONTROL Comenzar desde cero]** para escribir tu propio objetivo o **[!UICONTROL Comenzar desde la plantilla]** para usar una plantilla guardada.

   ![Crear flujo de trabajo saliente desde cero](./assets/outbound-workflow-create-start-from-scratch.png){width="700" zoomable="yes"}

1. Elige una de las **[!UICONTROL metas recomendadas]** como punto de partida o ingresa tu propia meta.

1. Haga clic en **[!UICONTROL Siguiente: Segmentación]**.

Los objetivos funcionan mejor cuando establecen un **resultado concreto**, no solo un tema. Para que la IA funcione mejor, use una meta como `Book a 15-minute discovery call with marketing leaders evaluating campaign automation` en lugar de `Promote campaign automation`.

#### Paso 2: Configuración de los filtros de segmentación

Los filtros de segmentación definen qué clientes potenciales son aptos. Cuando se agregan perspectivas más adelante, sólo aparecen en la lista de selección los posibles clientes que coinciden con estos filtros.

1. Haga clic en la flecha hacia abajo para mostrar la lista **[!UICONTROL Agregar un filtro]** y seleccione el filtro que desee aplicar.

   ![Crear filtros de destino de flujo de trabajo saliente](./assets/outbound-workflow-create-targeting-filter-list.png){width="700" zoomable="yes"}

1. Establezca valores para el filtro.

1. Añada más filtros si necesita reducir la audiencia.

   ![Crear flujo de trabajo saliente Segmentación añadió filtros con valores](./assets/outbound-workflow-create-targeting-filters-values.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Siguiente: Generar puntos de contacto]**.

#### Paso 3: Generar y revisar puntos de contacto

Una vez establecido el objetivo, la IA crea la **_cadencia_**: analiza el objetivo y el objetivo, define la secuencia de puntos de contacto y escribe un **_indicador de punto de contacto_** para cada paso. Verá una cadencia de varios pasos con cada punto de contacto en un día específico. La cadencia puede combinar pasos de correo electrónico, llamada de teléfono y LinkedIn In InMail.

![Mensajes y cadencia de punto de contacto generados por flujo de trabajo saliente](./assets/outbound-workflow-create-touchpoints.png){width="700" zoomable="yes"}

Para leer su mensaje, expanda un punto de contacto de correo electrónico. Esta instrucción guía a la inteligencia artificial aplicada al escribir el correo electrónico de cada posible cliente, incluido el tono, la longitud, el enfoque y _call to action_.

**Volver a generar la cadencia**

Si la cadencia no es la deseada, haga clic en **[!UICONTROL Volver a generar]** e introduzca una instrucción de refinamiento. Por ejemplo:

* `Make it 3 touchpoints across 2 weeks`
* `Lead with an executive briefing offer in the first email`
* `Add a nurture touch focused on a relevant case study`

La IA reescribe la cadencia completa en función de sus instrucciones.

Para ajustar un solo punto de contacto de correo electrónico sin regenerar toda la cadencia, edite el texto del mensaje directamente en su área de texto.

**Use un manual de instrucciones**

Si su organización ha creado un manual de implementación en el [Centro de conocimiento](#knowledge-center), puede indicar a la IA que saque de él al escribir correos electrónicos. En la solicitud, asigne un nombre al documento y al contexto que desea que utilice la API; por ejemplo, `Use the ABC positioning guide from the Knowledge Center and focus on the security value proposition`. A continuación, los correos electrónicos generados reflejan los mensajes de ese manual de implementación.

Cuando la cadencia y las indicaciones tengan el aspecto correcto, haga clic en **[!UICONTROL Siguiente: configuración]**.

Refinar los indicadores de punto de contacto antes de la generación de clientes potenciales importa: estos indicadores son las instrucciones principales que la IA utiliza para cada cliente potencial más adelante. El tiempo empleado aquí se escala en todos los correos electrónicos generados.

#### Paso 4: Configuración del flujo de trabajo

El paso **Configuración** controla cómo se ejecuta el flujo de trabajo.

![Configuración de flujo de trabajo saliente](./assets/outbound-workflow-create-settings.png){width="700" zoomable="yes"}

1. Revise **[!UICONTROL Workflow name]** y cámbielo si desea una etiqueta más clara.
1. En **[!UICONTROL Máximo de clientes potenciales por flujo de trabajo]**, confirme el límite superior de cuántos clientes potenciales puede administrar el flujo de trabajo a la vez.
1. Establece la ventana de **[!UICONTROL envío]** para las horas en las que se permite enviar correos electrónicos salientes.
1. Active **[!UICONTROL Omitir fines de semana]** para mover cualquier punto de contacto que caiga en un fin de semana al siguiente día laborable.
1. Para detener automáticamente los puntos de contacto de seguimiento una vez que el posible cliente reserve una reunión, active **[!UICONTROL Pausa para reserva de reuniones]**.
1. Confirme que la **[!UICONTROL zona horaria]** coincida con su audiencia.
1. Haga clic en **[!UICONTROL Guardar y agregar clientes potenciales]**.

Un administrador configura globalmente el pie de página de exclusión y se aplica a los correos electrónicos salientes independientemente de la configuración del flujo de trabajo. Consulte [Sincronización global de exclusión](#global-opt-out-sync).

#### Paso 5: Añadir clientes potenciales e iniciar la generación de correo electrónico

Guardar abre la vista de selección de clientes potenciales, ya filtrada por la segmentación del Paso 2.

![Perspectivas de adición de flujo de trabajo saliente](./assets/outbound-workflow-create-add-prospects.png){width="700" zoomable="yes"}

1. Revise la lista.

   Las filas suelen incluir el nombre del cliente potencial, la cuenta, el correo electrónico, el puesto, el estado de participación y el estado del cliente potencial.

1. Ajuste los filtros aquí si necesita expandir o reducir la lista.
1. Seleccione los clientes potenciales mediante las casillas de verificación.
1. Haga clic en **[!UICONTROL Siguiente: revise los puntos de contacto]** para iniciar la generación de correo electrónico de **por cliente potencial**.

La IA genera correos electrónicos personalizados para cada posible cliente seleccionado para **cada punto de contacto de correo electrónico** en la cadencia. Los puntos de contacto de Phone y LinkedIn In InMail permanecen en la cadencia como pasos programados. La generación se puede ejecutar en segundo plano: use **[!UICONTROL Notificar cuando esté listo]** si desea continuar con otro trabajo mientras se completa.

Para cada cliente potencial, la IA combina cada mensaje de punto de contacto con datos específicos del cliente potencial (persona, cuenta, historial de participación, noticias recientes) para producir la línea de asunto y el cuerpo.

### Revisar y perfeccionar correos electrónicos generados

Cuando termina la generación, la vista de detalles del flujo de trabajo muestra un banner para revisar los borradores. La revisión es obligatoria y nada envía hasta que la apruebe.

![Correos electrónicos generados por revisión de flujo de trabajo saliente](./assets/outbound-workflow-create-review-generated-emails.png){width="700" zoomable="yes"}

1. En la vista de detalles del flujo de trabajo, haga clic en **[!UICONTROL Revisar borradores]** en el banner.
1. El paso **[!UICONTROL Revisar puntos de contacto]** tiene dos pestañas:
   * **[!UICONTROL Listo para revisión]** - Correos electrónicos que terminaron de generarse.
   * **[!UICONTROL Generando]**: se siguen escribiendo correos electrónicos.
1. En la lista de clientes potenciales de la izquierda, haga clic en un nombre para cargar los puntos de contacto de ese cliente potencial a la derecha.
1. Use las comillas angulares (**>**) en un punto de contacto para expandir y leer la línea de asunto y el cuerpo completos.

#### Lea el razonamiento de IA

Para cada correo electrónico generado, **[!UICONTROL Reasoning]** explica cómo la IA creó ese mensaje, incluidas las señales, atributos y fuentes que dieron forma al contenido y a call to action. Revise esta información y valide la personalización antes de aprobarla.

![Motivo de IA de correo electrónico generado por flujo de trabajo saliente](./assets/outbound-workflow-create-review-generated-email-reasoning.png){width="600" zoomable="yes"}

#### Editar correos electrónicos directamente

Para pequeñas ediciones (redacción, tono, una sola frase):

1. En el punto de contacto expandido, haga clic en el icono _Editar_ para abrir el editor.
1. Edite la línea de asunto o el cuerpo.
1. Haga clic en **[!UICONTROL Guardar]**.

#### Refinamiento de correos electrónicos con IA

Para cambios más grandes (reestructurar, cambiar el énfasis o reformular el mensaje), use **[!UICONTROL Generar con IA]**. El agente de IA reescribe el correo electrónico y mantiene el contexto de personalización.

1. En el editor de correo electrónico, haga clic en **[!UICONTROL Generar con IA]**.

   ![El flujo de trabajo saliente generó refinamiento de correo electrónico con IA](./assets/outbound-workflow-create-review-generated-email-edit-regenerate.png){width="600" zoomable="yes"}

1. Introduzca una instrucción de borrado, por ejemplo:
   * `Make it shorter and more direct. Keep it under 100 words.`
   * `Focus more on the prospect's role and how the solution helps them specifically.`
   * `Change the call-to-action to suggest a 15-minute introductory call instead.`
1. Revise la revisión y realice la modificación manualmente si es necesario.
1. Haga clic en **[!UICONTROL Guardar]**.

>[!TIP]
>
>Las ediciones directas se adecúan a la redacción y al tono. Use _[!UICONTROL Generar con IA]_ para reescribir el correo electrónico desde cero.

### Aprobar e inscribir clientes potenciales

La aprobación activa la cadencia de un cliente potencial. Hasta que se aprueba e inscribe a un posible cliente, el sistema no le envía correos electrónicos.

1. En la lista de clientes potenciales de la izquierda, seleccione los clientes potenciales cuyos correos electrónicos ha revisado y que están listos para enviar.
1. Haga clic en **[!UICONTROL Aprobar e inscribir clientes potenciales]** (parte inferior derecha).

![Flujo de trabajo saliente para seleccionar y aprobar clientes potenciales](./assets/outbound-workflow-create-approve-enroll-prospects.png){width="700" zoomable="yes"}

Los correos electrónicos aprobados se envían durante el flujo de trabajo **ventana de envío** en la **zona horaria** configurada, en el día programado de cada punto de contacto en relación con la inscripción. Los clientes potenciales que no apruebe permanecerán en **[!UICONTROL Listo para revisión]** hasta que actúe. Después de la aprobación, el flujo de trabajo se ejecuta según la cadencia definida.

### Administrar flujos de trabajo existentes

En la página _[!UICONTROL Flujo de trabajo saliente]_, la pestaña **[!UICONTROL Examinar]** muestra todos los flujos de trabajo. Cada tarjeta muestra el objetivo, los puntos de contacto configurados y las métricas de rendimiento. Utilice esta vista para monitorizar los flujos de trabajo activos, volver a los borradores que aún deben revisarse o abrir un flujo de trabajo para agregar más posibles clientes.

### Prácticas recomendadas de flujo de trabajo saliente

* **Invierta en la meta.** El direccionamiento descendente, la cadencia y los correos electrónicos se remontan al objetivo. Los objetivos específicos, centrados en los resultados, superan a los vagos.
* **Finalizar mensajes de punto de contacto antes de la generación por cliente potencial.** Después de la generación masiva, los cambios se suelen realizar de un cliente potencial a la vez.
* **Usar razonamiento como comprobación de calidad.** Si se enfatiza la señal incorrecta (o falta una obvia), edite el correo electrónico o vuelva a visitar el indicador de punto de contacto y vuelva a generar la cadencia.
* **Hacer coincidir la herramienta de edición con el cambio.** Ediciones directas de redacción y tono; **[!UICONTROL Generar con IA]** para reestructurar o reenmarcar.
* **Aprobar solo lo que ha revisado.** Amplíe los puntos de contacto, lea el contenido y perfeccione lo que necesite antes de inscribirse.

### Sincronización de exclusión global

Los administradores pueden anexar un pie de página de cancelación de suscripción de toque ligero que use expresiones [!DNL Marketo] preaprobadas a cada correo electrónico saliente. Cuando un cliente potencial selecciona el vínculo de no participación, el calificador de ventas suprime permanentemente al cliente potencial de más correos electrónicos y sincroniza el estado de no participación con el CRM conectado. Consulte [Configurar la exclusión de correo electrónico global](#configure-global-email-opt-out).

## Bandeja de salida de correo

El panel Bandeja de salida de correo electrónico enumera todos los correos electrónicos automatizados que ha enviado.

<!--
## Meeting bookings

This panel displays all meetings set up through automation.

## Chat inbox

This panel displays all your chat threads.

![Panel showing chat threads with contact and thread summaries for sales automation](assets/chat-inbox.png)

You can interact with clients, and see summaries for the contact and the thread so that you can quickly know where you are in the thread.

-->

## Tareas

El área _Tareas_ del Calificador de ventas proporciona a los Representantes de desarrollo de negocios (BDR) un espacio dedicado para administrar y procesar sus acciones de flujo de trabajo salientes. El motor de flujo de trabajo saliente genera automáticamente tareas que representan las acciones específicas que un BDR necesita realizar con cada posible cliente: llamadas telefónicas, InMails de LinkedIn y revisiones de correo electrónico.

La experiencia de administración de tareas es una **cola de procesamiento**, no una lista de tareas pendientes. Puede abrir una tarea, realizar acciones, marcarla como completada y pasar al siguiente sin salir de la página.

Seleccione **[!UICONTROL Tareas]** en la barra de navegación izquierda para abrir la página de tareas completa. Esta página es el espacio de trabajo principal para procesar las tareas una por una.

![Página de tareas que muestra la cola de tareas y el panel de detalles](./assets/tasks.png){width="800" zoomable="yes"}

<!--
**Homepage feed** - The homepage displays a running feed of your most urgent tasks, with overdue items at the top followed by today's tasks. Each item in the feed has an "Open" button that takes you directly to that task in the Tasks page with the detail panel already loaded.
-->

### Tipos de tareas

Todas las tareas están vinculadas a pasos de flujo de trabajo salientes. Existen tres tipos:

**Llamada telefónica**: se crea cuando una cadencia alcanza un paso de llamada telefónica. El panel de tareas muestra los puntos de paso generados por el agente y un campo de notas en línea para capturar notas de llamada.

**LinkedIn In InMail**: se crea cuando una cadencia alcanza un paso de LinkedIn In InMail. El panel de tareas muestra una línea de asunto y un cuerpo de mensaje generados por IA que puede copiar y enviar fuera del producto.

**Revisión de correo electrónico**: creada una vez que el sistema termina de generar correos electrónicos personalizados para un cliente potencial inscrito en un flujo de trabajo. Revise y apruebe los mensajes de correo electrónico antes de que comience la salida para ese cliente potencial. Cada cliente potencial recibe una tarea de revisión de correo electrónico independiente; si inscribe a 10 clientes potenciales en un flujo de trabajo, verá hasta 10 tareas de revisión de correo electrónico a medida que se complete la generación.

### Administración de tareas

La página Tareas se divide en dos paneles:

* **Izquierda — Lista de tareas:** Su cola de tareas, ordenadas y filtradas según la configuración de orden y vista seleccionada.
* **Derecha — Panel de trabajo de la tarea:** Detalles de la tarea seleccionada, incluida la información del cliente potencial, el contexto del flujo de trabajo, el contenido específico de la tarea y los controles de acción.

Al seleccionar cualquier tarea en el panel izquierdo, se cargan sus detalles en el panel derecho sin salir de la página.

#### Controles de cola

El panel de trabajo incluye los controles **Siguiente** y **Anterior** para moverlos por la cola de tareas en orden. La cola respeta la configuración de ordenación y filtro que aplique a la lista. Por lo tanto, si está trabajando en tareas de llamada de teléfono vencidas ordenadas por fecha de vencimiento, _Siguiente_ y _Anterior_ se mueven exactamente a través de ese conjunto.

Cuando marca una tarea como completada, el panel avanza automáticamente a la siguiente tarea de la cola.

#### Notas

Para las tareas de Phone Call y LinkedIn In InMail, hay un campo de notas en línea disponible en el panel de trabajo. Las notas se guardan automáticamente cuando hace clic fuera para no perderlas cuando vaya a otra tarea antes de marcar la tarea actual como completada.

#### Acciones de tarea

Utilice las siguientes acciones para administrar sus tareas:

* **[!UICONTROL Marcar como completada]** - La acción principal. Utilice esta acción después de ejecutar la tarea: realizar la llamada, enviar el mensaje de InMail o revisar y aprobar los mensajes de correo electrónico. Al finalizar, la tarea se registra como **Completada** y la cola avanza automáticamente.

* **[!UICONTROL Omitir punto de contacto]**: disponible en el menú de desbordamiento del panel de trabajo. Utilice esta opción cuando no pueda completar este paso, pero el cliente potencial siga siendo un destino válido en el flujo de trabajo.
  * El cliente potencial avanza al siguiente paso de la cadencia. Las tareas futuras se siguen generando según lo programado.
  * Seleccione un motivo: *Información de contacto incorrecta*, *mal tiempo*, *Contenido no relevante* o *Otro* (con un campo de texto libre).
  * El estado de la tarea se ha establecido en **Omitido** y se ha registrado con el motivo y la marca de tiempo.
  * Si este fue el último paso del flujo de trabajo, finaliza la ejecución del flujo de trabajo del cliente potencial. La tarea sigue registrándose como Omitido (no eliminado).

* **[!UICONTROL Quitar del flujo de trabajo]** - Disponible en el menú de desbordamiento del panel de trabajo. Utilícelo cuando el cliente potencial ya no pertenezca a este flujo de trabajo.

  Cuando elimina un cliente potencial de un flujo de trabajo:
  * Todas las tareas pendientes y futuras de ese cliente potencial dentro de este flujo de trabajo se cancelan.
  * El estado de inscripción del cliente potencial cambia a **Eliminado por BDR**.
  * Seleccione un motivo: *Se fue de la compañía*, *Duplicado*, *Ajuste incorrecto*, *Ya se ha convertido* o *Otro* (con un campo de texto).
  * Aparece un cuadro de diálogo de confirmación: *&quot;Esta acción cancelará todos los puntos de contacto restantes para [Cliente potencial] en [Nombre de flujo de trabajo]. ¿Continuar?&quot;*
  * El estado de la tarea se ha establecido en **Eliminada**. Todas las tareas del mismo nivel canceladas también están marcadas como **Eliminadas**.

>[!NOTE]
>
>Los datos de omisión y eliminación de motivos informan a los análisis, incluidas las tasas de omisión de canales, las tasas de eliminación de flujos de trabajo y los motivos principales. Esto ayuda a mejorar la calidad del flujo de trabajo e informa al análisis del rendimiento a lo largo del tiempo.

**Omisión automática**

Las tareas estancadas de LinkedIn In InMail y llamadas telefónicas se omiten automáticamente si permanecen incompletas durante dos días. La omisión automática mantiene a un posible cliente en movimiento a través de la cadencia sin detener la ejecución y no afecta a la cronología del correo electrónico. Los puntos de contacto de correo electrónico programados siguen enviándose según lo planificado.

### Estado de tarea

Cada tarea se desplaza por los siguientes estados:

| Estado | Descripción |
|---|---|
| **Pendiente** | Se ha creado, pero el paso de flujo de trabajo anterior aún no se ha completado. No visible en la lista de tareas. |
| **Próximamente** | El paso anterior se ha completado, pero la fecha de vencimiento es futura. Visible y procesable: puede completarlo antes si es el momento adecuado. |
| **Abri** | Vence hoy. Visible y procesable. |
| **Vencido** | Fecha de vencimiento pasada, aún no completada. Visible, procesable y marcado visualmente. |
| **Completado** | Ha ejecutado y marcado la tarea como completada. |
| **Omitido** | Se ha omitido este punto de contacto. El cliente potencial avanza en el flujo de trabajo. |
| **Eliminado** | Ha eliminado al posible cliente del flujo de trabajo. Todas las tareas del mismo nivel se cancelan. |
| **Cancelado** | Cancelado por el sistema debido a un cambio en el flujo de trabajo o a una posible eliminación. |

### Vistas de lista

Utilice las pestañas de la parte superior de la lista de tareas para cambiar entre vistas:

* **Hoy** *(predeterminado)* — Tareas pendientes hoy que no se han completado.

* **Vencidas**: tareas cuya fecha de vencimiento ha pasado y siguen abiertas. Aborde primero estas tareas.

* **Próximas**: tareas con una fecha de vencimiento futura en las que el paso anterior del flujo de trabajo ya se haya completado. Estas tareas se pueden ver antes de tiempo, por lo que puede planificar con antelación o actuar antes si el momento es el adecuado (por ejemplo, si ya está en una llamada con un posible cliente). Se muestra la fecha de vencimiento programada para que sepa el tiempo previsto.

* **Completadas**: un registro de tareas que ha completado, omitido o eliminado. Útil para fines de revisión y auditoría.

### Filtrado y búsqueda

Existen varias formas de filtrar la lista de tareas:

* Filtre por tipo de tarea mediante una lista de selección múltiple. Si se seleccionan varios tipos, se mostrarán las tareas que coincidan con *cualquier* de los tipos seleccionados (por ejemplo, Llamada telefónica **o** Revisión de correo electrónico).

* Filtrar por estado de tarea. Al seleccionar varios estados, se muestran las tareas que coinciden con cualquiera de los estados seleccionados.

* Filtre entre grupos con la lógica **AND**. Por ejemplo, `Type = Phone Call and Status = Overdue` muestra solamente las tareas de llamada vencidas.

Utilice la barra de búsqueda para buscar tareas por nombre del cliente potencial, nombre de la empresa o nombre de la participación. La búsqueda se aplica junto con cualquier filtro activo. Coincidencia de texto solamente: coincidencias parciales exactas, sin búsqueda parcial.

### Orden

Utilice el control **Ordenar por** para elegir cómo se ordena la lista de tareas. La ordenación también determina el orden en que Siguiente y Anterior se mueven por la cola.

| Opción de orden | Comportamiento |
|---|---|
| **Fecha de vencimiento (ascendente)** *(predeterminado)* | Primero, la fecha límite más antigua. Las tareas vencidas aparecen antes de las tareas de hoy. |
| **Fecha de vencimiento (descendente)** | Primero la fecha límite. |
| **Fecha de creación (más reciente)** | Primero las tareas creadas más recientemente. |
| **Fecha de creación (más antigua)** | Primero, las tareas creadas más antiguas. |
| **Tipo de tarea** | Agrupadas por tipo en orden: Llamada telefónica → revisión de correo electrónico de → de LinkedIn. Dentro de cada grupo, ordenado por fecha de vencimiento en orden ascendente. |

### Tareas vencidas

Una tarea pasa a estar vencida el día siguiente a su fecha de vencimiento si no se ha completado. Tareas vencidas:

* Aparecen en la vista **Vencido** y en la parte superior de la fuente de la página principal.
* Se marcan visualmente con un distintivo &quot;Vencido&quot; en la lista de tareas.
* Permanecer totalmente procesable: puede completarlos, omitirlos o eliminarlos.

### Próximas tareas

Las próximas tareas se crean en el momento en que un cliente potencial completa un paso del flujo de trabajo, incluso si la fecha de vencimiento del siguiente paso sigue siendo futura. Esta visibilidad le proporciona la incorporación temprana de insight a su canalización para que pueda planificar con anticipación o actuar con anticipación cuando se presente la oportunidad.

Las próximas tareas muestran su fecha de vencimiento programada, para que siempre sepa cuándo se van a abordar. La finalización anticipada de una tarea inminente es totalmente compatible: el motor de flujo de trabajo registra la fecha real de finalización y adelanta al posible cliente normalmente.

### Finalización de tarea

La finalización de tareas no se limita a la página Tareas.

**Vista del posible cliente comprometido:** Las vistas previas del punto de contacto en la página de un posible cliente comprometido incluyen una acción _Marcar como completado_ junto con una vista previa de contenido y un campo de notas opcional. Al completar una tarea aquí, se actualiza su estado inmediatamente en la página Tareas. Esta vista no almacena en déclencheur el comportamiento de avance automático; es una superficie de vista y acción, no una superficie de procesamiento de colas.

**Salesforce (complemento CRM):** El complemento Calificador de ventas de Salesforce muestra el estado de la tarea (próxima, pendiente, finalizada, vencida, omitida) en la tarjeta de flujo de trabajo saliente. En la versión actual, la tarjeta CRM es **de solo lectura**; puede ver el estado de la tarea, pero debe completar las tareas desde el Calificador de ventas.

### Estados vacíos

* **Hoy sin tareas:** Verá un mensaje de _Se ha puesto al día con respecto al mensaje de hoy_. Si existen tareas próximas, aparece un mensaje como _Tiene [N] tareas próximas — ver_ próximas.
* **Tareas vencidas presentes:** Un mensaje le recomienda que primero aborde las tareas vencidas.

## Reserva de reuniones

El Calificador de ventas convierte las conversaciones comprometidas en reuniones reservadas sin abandonar el flujo de salida. Al conectar el calendario, el Cualificador de ventas genera un vínculo de reserva personal que los posibles clientes utilizan para programar el tiempo con usted.

* **Vínculos de reserva**: configura la conexión y disponibilidad del calendario en [Configuración del perfil](#profile-settings). El vínculo de reserva se puede añadir a la firma de correo electrónico para que aparezca en los correos electrónicos salientes.
* **Inserción automática en una cadencia**: el Cualificador de ventas inserta el vínculo de reserva en puntos apropiados de una cadencia, de modo que la invitación a reunirse aparezca cuando sea más relevante. Puede anular la ubicación manualmente.
* **Pausa para la reserva** - Cuando un cliente potencial reserva una reunión, **[!UICONTROL Pausa para la reserva de la reunión]** detiene automáticamente más seguimientos. Consulte [Configurar la configuración del flujo de trabajo](#step-4-configure-workflow-settings).

Rastree los resultados de las reservas en la sección [Rendimiento](#performance).

## Centro de información

El _[!UICONTROL Centro de conocimientos]_ proporciona a Account Qualification Agent (AQA) acceso a sus propios materiales de ventas, para que el Calificador de ventas pueda generar investigaciones, perspectivas de calificación y alcance que reflejen las ventas de su organización. Crear y administrar el manual es una tarea de administrador.

![Centro de conocimientos](./assets/integrations-knowledge-center.png){width="700" zoomable="yes"}

### Cargar material promocional de ventas

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Configuración de administración]**.
1. Seleccione **[!UICONTROL Centro de conocimiento]** en **[!UICONTROL Integraciones]**.
1. Establezca **[!UICONTROL Nombre de la compañía]** y **[!UICONTROL URL de la compañía]** que el calificador de ventas usa para investigar su compañía y redactar correos electrónicos.
1. Cargar reproducciones de ventas, perfiles de cliente (ICP) ideales, guías de posicionamiento y otros materiales de promoción de ventas en formato PDF, PPTX o DOCX.

Cada documento cargado muestra su estado de procesamiento, como **[!UICONTROL Listo]**, y la última vez que se actualizó.

### Creación de un manual

Después de cargar los documentos, selecciona **[!UICONTROL Crear libro de estrategias]** para convertirlos en un libro de estrategias.

>[!NOTE]
>
>Un libro de estrategias tarda unas 24 horas en procesarse antes de estar listo para usarse.

Cuando el manual está listo, alimenta tanto el alcance como la asistencia:

* **Mensajes de correo electrónico salientes**: consulte el manual de implementación al generar mensajes de correo electrónico nombrando el documento y el contexto en el mensaje. Consulte [Generar y revisar puntos de contacto](#step-3-generate-and-review-touchpoints).
* **Asistente de ventas para la conversación** - Para extraer del manual, diríjase al asistente al Centro de conocimientos. Consulte [Asistente de ventas para conversaciones](#conversational-sales-assistant).

## Asistente de ventas conversacional

El Asistente de ventas conversacional es una experiencia de chat en la que realiza preguntas en lenguaje natural y obtiene respuestas basadas en su contexto de ventas. El asistente se basa en:

* Su base de conocimientos interna, incluido cualquier manual del [Centro de conocimientos](#knowledge-center)
* Señales CRM de su CRM conectado
* [!DNL Marketo] datos de actividad y participación
* Investigación web

Utilice el asistente para prepararse antes de la divulgación; por ejemplo, para crear una posición de la cuenta antes de una reunión. Para extraer de un manual creado, diríjase al asistente al Centro de conocimientos en su pregunta. Por ejemplo: `From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

## Desempeño

La sección **[!UICONTROL Rendimiento]** muestra el rendimiento de tu salida, para que puedas ver qué está funcionando y dónde ajustarlo.

### Rendimiento del correo electrónico

Revise el volumen y la eficacia del correo electrónico saliente:

* Correos electrónicos enviados
* Tasa de apertura
* Tasa de pulsaciones
* Tasa de respuesta

El cualificador de ventas identifica las respuestas y devoluciones fuera de la oficina con sus estados correspondientes, para que pueda distinguirlas de las participaciones potenciales.

### Rendimiento de reservas de reuniones

Las tarjetas de estado de reserva de reuniones resumen el lugar de las reuniones reservadas. Filtre las tarjetas para centrarse en las reuniones y los estados que desee revisar.

## Integraciones y CRM

Con las integraciones, el cualificador de ventas se conecta a su CRM para que el Account Qualification Agent (AQA) y los flujos de trabajo salientes compartan una vista coherente de los posibles clientes, las cuentas, los contactos, las actividades y los propietarios en Salesforce o Microsoft Dynamics 365. El calificador de ventas lee los datos y las actividades de ventas de CRM para enriquecer las perspectivas y puede escribir las actividades de alcance registradas y el estado de exclusión. De lo contrario, no modifica los registros CRM a través de esta conexión.

Las conexiones CRM, la asignación de campos entrantes y la sincronización de actividades las configura un administrador en **[!UICONTROL Administración]** > **[!UICONTROL Configuración de administración]** > **[!UICONTROL Conexiones CRM]**. Los usuarios estándar consumen los datos y filtros de CRM configurados, pero no pueden cambiar esta configuración.

### CRM MCP y el complemento incrustado

El Cualificador de ventas trabaja con su CRM de más de una manera:

* **Consulta de datos de CRM a través del MCP de CRM**: Account Qualification Agent consulta datos de CRM activos a través del MCP de CRM, de modo que las respuestas y perspectivas reflejen el estado actual de sus registros.
* **Complemento incrustado**: el complemento de CRM incrustado muestra información básica de [!DNL Marketo Sales Insights] (MSI) junto con los nuevos datos reales, directamente en su CRM. Desde el complemento, agregue un cliente potencial al Calificador de ventas con un solo clic.
* **Sincronización de actividades**: cuando un administrador habilita **[!UICONTROL Sincronización de actividades]**, las actividades de alcance se sincronizan con el CRM, de modo que los representantes vean la actividad del Calificador de ventas en las herramientas que ya usan.

>[!IMPORTANT]
>
>El acceso a **[!UICONTROL Configuración de administración]** requiere la pertenencia a los grupos de usuarios `Sales Qualifier` y `Sales Qualifier Admins`.

### Ámbito de acceso CRM

El cualificador de ventas lee las entidades CRM que necesita y solo puede escribir un conjunto definido de datos. Las entidades habituales que se leen incluyen usuarios, contactos, asignaciones de propietarios, posibles clientes, cuentas, oportunidades y actividades. La reescritura se limita a las actividades de divulgación registradas y al estado de exclusión. El administrador de CRM prepara el acceso a la API en Salesforce o Dynamics. A continuación, conecte el cualificador de ventas, asigne los campos de entrada y elija si desea sincronizar las actividades en la aplicación.

>[!NOTE]
>
>Los pasos de credenciales que siguen describen el acceso de lectura a los objetos CRM. Si habilita la sincronización de actividades o la reescritura de exclusión, trabaje con su administrador de CRM para conceder el acceso de escritura correspondiente requerido por su configuración de CRM.

### Preparar credenciales en su CRM

Póngase en contacto con el administrador de CRM antes de conectar el cualificador de ventas. A continuación se resume lo que se suele crear en cada sistema.

#### Microsoft Dynamics 365 (Dataverse/Power Platform)

1. En Azure Active Directory, registre una aplicación (**[!UICONTROL Registros de aplicaciones]**).

   Observe **ID de cliente** y **ID de inquilino**, y cree un **Secreto de cliente**.

1. En el **[!UICONTROL Centro de administración de Power Platform]**, abra su entorno y vaya a **[!UICONTROL Configuración]** > **[!UICONTROL Usuarios + permisos]** > **[!UICONTROL Usuarios de la aplicación]**.

1. Cree un usuario de aplicación vinculado a esa aplicación de Azure AD.

1. Asigne una función de seguridad que conceda a **read** acceso a las necesidades del calificador de ventas de las entidades, como posibles clientes, contactos, cuentas, oportunidades y actividades.

   La aplicación requiere una función de seguridad con acceso de lectura para leer datos.

**Información que se debe proporcionar al conectar con Dynamics:**

* Identificación del cliente
* Secreto de cliente
* ID de inquilino
* URL de instancia de Dynamics (URL de organización)

#### Salesforce

En Salesforce, [cree una aplicación cliente externa](https://help.salesforce.com/s/articleView?id=xcloud.create_a_local_external_client_app.htm&type=5) (o una _aplicación conectada_) con OAuth habilitado y ámbitos que permitan el acceso de API a la identidad y los datos, siguiendo los estándares de seguridad de su organización. El usuario que realiza la integración debe tener acceso de lectura a objetos como posibles clientes, cuentas, contactos, tareas, eventos y oportunidades. Las tareas administrativas a menudo requieren que un usuario con **[!UICONTROL Administrar aplicaciones conectadas]** (entre otros permisos) vea una clave de consumidor y un secreto después de la creación.

>[!PREREQUISITES]
>
>Para crear una aplicación de cliente externa, un administrador de productos debe comprobar que tiene lo siguiente habilitado (de Perfil o Conjunto de permisos):
>
>* Personalizar aplicación
>* Ver instalación y configuración
>* Modificar todos los datos
>* Administrar aplicaciones conectadas (importante)
>
>   Si _Administrar aplicaciones conectadas_ no está habilitada, no podrá ver el ID de cliente y el secreto de cliente después de crear la aplicación cliente externa.

Cuando cree la aplicación cliente externa, habilite OAuth y conceda permisos. Habilite también las siguientes credenciales de cliente:

* Acceso al servicio de URL de identidad (ID, perfil, correo electrónico, dirección, teléfono)
* Administración de datos de usuario mediante API
* Acceso a identificadores de usuario únicos (openid)

Después de crear la aplicación, vuelva a habilitar el flujo de credenciales del cliente y utilice el correo electrónico de contacto como nombre de usuario.  Cuando las credenciales del cliente estén habilitadas, configure un usuario para _Ejecutar como_.

Asegúrese de que el usuario configurado tenga acceso de lectura a los siguientes objetos:

* Clientes potenciales
* Cuentas
* Contactos
* Tareas
* Eventos
* Oportunidad
* OpportunityContactRoles
* OpportunityLineItems

**Información que se debe proporcionar al conectar Salesforce en el Calificador de ventas:**

* ID de cliente (clave del cliente)
* Secreto del cliente (Secreto del consumidor)
* URL de devolución de llamada (según la configuración en la aplicación conectada)
* URL de instancia de Salesforce

>[!IMPORTANT]
>
>No enviar secretos de cliente por correo electrónico. Utilice el canal seguro aprobado de su organización para compartir credenciales con quien las introduzca en el cualificador de ventas.

### Conéctese a su CRM

1. Inicie sesión en el cualificador de ventas y confirme que la zona protegida o el entorno correctos están seleccionados.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Configuración de administración]**.

1. Seleccione **[!UICONTROL conexiones CRM]** en **[!UICONTROL Integraciones]**.

   La página muestra tarjetas para Salesforce y Microsoft Dynamics. Una conexión inactiva muestra **[!UICONTROL Connect]**. Una conexión configurada muestra **[!UICONTROL Conectado]** y una acción **[!UICONTROL Administrar]**.

   ![Configuración de administración y conexiones CRM con tarjetas de conexión de Salesforce y Dynamics](./assets/integrations-crm-connections.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Conectar]** para el CRM que utilice.

1. Introduzca el ID de cliente, los secretos, los valores de inquilino o devolución de llamada y la **URL de instancia** de su administrador de CRM.

1. Después de una conexión correcta, confirma que la tarjeta muestra **[!UICONTROL Conectado]**.

### Directrices de URL de instancia

La **URL de instancia** debe ser la URL base de entorno que su CRM use para la configuración de integración y API, no un nombre de host solo de interfaz de usuario.

**Salesforce**

1. Inicie sesión y anote el subdominio de organización _Mi dominio_ desde la barra de direcciones del explorador (el valor `{{mydomain}}`).

1. Para el Calificador de ventas, use el formulario canónico: `https://{{mydomain}}.my.salesforce.com` .

   **no** usa una dirección URL `lightning.force.com` como dirección URL de instancia.

**Microsoft Dynamics 365**

1. Abra el CRM en el explorador y copie la URL base de la barra de direcciones.

   Suele estar en el formulario `https://{{org}}.crm.dynamics.com`.

### Asignar campos CRM (asignación de entrada)

Una vez conectado el CRM, seleccione **[!UICONTROL Administrar]** para la conexión y abra **[!UICONTROL Asignación entrante]**. La asignación de entrada controla qué campos CRM extrae el cualificador de ventas en la aplicación.

1. Seleccione un grupo de objetos: **[!UICONTROL Contacto]**, **[!UICONTROL Cliente potencial]** o **[!UICONTROL Cuenta]**.
1. Seleccione **[!UICONTROL Agregar sección]** e introduzca un nombre de sección y una descripción opcional.
1. Agregue los campos CRM a la sección.

   Cada fila de campo muestra su **[!UICONTROL nombre para mostrar]**, **[!UICONTROL nombre de campo]** y **[!UICONTROL tipo de datos]**.

1. Active **[!UICONTROL Filtrable]** para cada campo que deba estar disponible como filtro en la lista **[!UICONTROL Posibles clientes]**.
1. Obtenga una vista previa de la asignación y guárdela.

Los campos asignados aparecen en las áreas correspondientes del cualificador de ventas:

* Los campos Cliente potencial y Contacto aparecen en la ficha **[!UICONTROL Persona]** para los clientes potenciales.
* Los campos de cuenta aparecen en la vista de cuentas.
* Los campos relacionados con la oportunidad aparecen en las áreas de oportunidad de la experiencia de la cuenta.

### Configuración de la sincronización de actividades (asignación saliente)

1. De **[!UICONTROL conexiones CRM]**, seleccione **[!UICONTROL Administrar]** para el CRM conectado.
1. Abrir **[!UICONTROL asignación saliente]**.
1. Active **[!UICONTROL Sincronización de actividades]** para sincronizar las actividades de alcance del Calificador de ventas con el CRM.

Cuando la sincronización de actividades está desactivada, el cualificador de ventas puede seguir utilizando datos CRM entrantes, pero no vuelve a escribir las actividades de divulgación en el CRM.

### Configuración de la exclusión de correo electrónico global

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Administración]** y seleccione **[!UICONTROL Configuración de administración]**.
1. Seleccione **[!UICONTROL Configuración de correo electrónico]** en **[!UICONTROL Cumplimiento]**.
1. Active **[!UICONTROL Incluir vínculo de no participación en cada correo electrónico]** para anexar un pie de página de cancelación de suscripción a los correos electrónicos salientes.
1. En **[!UICONTROL Plantilla de mensaje de exclusión]**, escriba el texto del pie de página. Incluya el token `{{opt_out_link}}` donde debería aparecer el vínculo de cancelación de suscripción al que se puede hacer clic.
1. Guarde la configuración.

Cuando un cliente potencial selecciona el enlace, el Cualificador de ventas suprime permanentemente al cliente potencial de más correos electrónicos. El estado de exclusión también se sincroniza con el CRM conectado.

### Referencia: Parámetros de API de muestra

Su equipo de CRM puede utilizar estos ejemplos para confirmar que el acceso de lectura devuelve los campos de posibles clientes esperados.

**Dynamics (extracto estilo OData)**

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

**Salesforce (extracto de SOQL)**

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

## Configuración de perfil

La configuración del perfil especifica información sobre usted, incluidos sus datos personales, el correo electrónico, el calendario y la disponibilidad del chat.

### Configuración de correo electrónico

En la pestaña **[!UICONTROL Configuración de correo electrónico]**, configure las conexiones de correo electrónico.

![Pestaña Configuración de correo electrónico que muestra las opciones de conexión de correo electrónico y la configuración de firma de correo electrónico](assets/email-settings.png)

* **[!UICONTROL Conexiones de correo electrónico]** - Haga clic en **[!UICONTROL Conectar]** y siga el procedimiento de inicio de sesión de Microsoft.

* **[!UICONTROL Firma de correo electrónico]**: configure la firma de correo electrónico que se usa en los correos electrónicos generados automáticamente. Agregue su vínculo [reserva de reuniones](#meeting-booking) a la firma para que los posibles clientes puedan programar su hora con usted.

### Configuración del calendario

En la ficha **[!UICONTROL Configuración del calendario]**, establezca la zona horaria y la disponibilidad.

<!-- 
![Calendar settings tab showing time zone and availability options](assets/calendar-settings.png)
-->

* **[!UICONTROL Conexión de calendario]** - Haga clic en **[!UICONTROL Conectar]** y siga el procedimiento de inicio de sesión de Microsoft para integrar su calendario.

* **[!UICONTROL Correo electrónico de confirmación de la reunión]**: cuando un cliente confirma una reunión con usted, recibe el correo electrónico de confirmación como respuesta. Utilice esta configuración para definir el asunto y el cuerpo del correo electrónico.

* **[!UICONTROL Preferencias]**: establezca la duración predeterminada de la reunión y el tiempo entre reuniones consecutivas.

Si desconecta el calendario:

* Los vínculos de reserva activos están desactivados.
* La página de reserva muestra un estado descriptivo, temporalmente no disponible.
* La reconexión conserva la configuración.

### Disponibilidad del calendario

La disponibilidad del calendario en el Cualificador de ventas se basa en dos entradas:

* Calendario de trabajo conectado (Outlook o Gmail)
* Su disponibilidad configurada y reglas de franja horaria en _Configuración del calendario_.

El calificador de ventas lee el estado de disponibilidad del calendario conectado, no del contenido completo del evento, y lo utiliza junto con las reglas configuradas para decidir qué espacios de reserva puede ver un cliente potencial.

Puede configurar lo siguiente:

* Horas laborables por día de la semana
* Varios bloques al día (por ejemplo, de 9:00 a 12:00 y de 1:00 a 5:00)
* Su huso horario
* Duración de la reunión
* Búfer antes/después de las reuniones
* Aviso mínimo
* Ventana de reserva

<!-- 
### Chat settings

In the **[!UICONTROL Chat settings]** tab, set your Timezone Live chat availability.

![Chat settings tab for configuring timezone and live chat availability](assets/chat-settings.png)

## Representative management

The _[!UICONTROL Representative management]_ panel displays the defined representatives and their calendar status.

## Meeting performance

This panel presents analytics around your completed meetings.
-->

<!--
 SHPHR-24341 remove section
## Set up the Chrome plugin

The AI Assistant Chrome plugin is available on the [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

When the plugin is installed in Chrome, the Adobe logo appears on the middle right when you are on an integrated site:

* Adobe web applications
* Salesforce
* Outlook
* Microsoft Dynamics and web applications
* Google applications 
-->
