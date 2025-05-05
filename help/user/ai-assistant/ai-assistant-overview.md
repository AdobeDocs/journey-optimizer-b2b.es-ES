---
title: Asistente de IA en Journey Optimizer B2B Edition
description: Marcador de posición
feature: AI Assistant
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
source-git-commit: f09f3f5b7d4419ead5308e4c5be3b518b4e16ff5
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 3%

---

# Asistente de IA en Journey Optimizer B2B Edition

AI Assistant en Journey Optimizer B2B Edition se crea a partir de la misma base tecnológica de [AI Assistant en Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home). Se trata de un experiencia conversacional que puede utilizar para acelerar su flujos de trabajo en Adobe Systems Journey Optimizer B2B Edition. Puede utilizar AI Assistant para obtener una mayor comprensión de las capacidades del producto, solucionar problemas o búsqueda a través de la información y encontrar información operativa para Journey Optimizer B2B Edition.

>[!IMPORTANT]
>
>Para poder utilizar AI Assistant en Journey Optimizer B2B Edition es necesario aceptar las [directrices](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) de usuario. Este acuerdo también contiene el acuerdo de beta pública para que pueda usar funciones adicionales de AI Assistant a medida que se implementan en una capacidad beta.

+++Ver la interfaz del acuerdo de usuario

![El primer Página del acuerdo usuario.](./assets/user-agreement-1.png)

![El último Página del usuario acuerdo.](./assets/user-agreement-2.png)

+++

## Funciones del asistente de IA en Journey Optimizer B2B edition

Para formular una respuesta a las preguntas enviadas, AI Assistant consulta una base de datos y traduce los datos de la base de datos a una respuesta legible en lenguaje natural. Esta respuesta es una representación interna de los datos subyacentes y también se conoce como _&#x200B;**_Gráfico de conocimientos_**&#x200B;_, una completa web de conceptos, datos y metadatos para una respuesta determinada. El gráfico de conocimiento consta de subgráficos a los que se hace referencia cada vez que se envían consultas:

* Documentación de Experience League.
* Artefactos operativos, como esquemas, campos, audiencias y viajes.

Tenga en cuenta qué tipo de consulta necesita antes de enviar un asistente de IA consulta:

### Conocimiento del producto

El conocimiento del producto hace referencia a conceptos y temas basados en la documentación de Journey Optimizer B2B Edition sobre Adobe Systems Experience League. Las preguntas sobre conocimientos del producto se pueden especificar en los siguientes subgrupos:

| Conocimiento del producto | Ejemplos |
| --- | --- |
| Aprendizaje puntual | <li>¿Qué es una grupo de compra? <li> Mostrar un ejemplo de una compra grupo roles plantilla? |
| Descubrimiento abierto | <li>¿Cuáles son los pasos para crear grupos de compra? <li>¿Cómo utilizo los campos personalizados en las plantillas de compra grupo roles? |
| Resolución de problemas | <li>¿Por qué no se ha creado la compra de grupos para mi viaje? <li>¿Por qué no puedo encontrar eventos de experiencia para escuchar en el viaje? |

### Información operativa

_La información_ operativa se refiere a las respuestas que AI Assistant genera sobre sus objetos de metadatos (atributos, audiencias cuenta, flujos de datos, conjuntos de datos, destinos, viajes cuenta, esquemas, fuentes, plantillas de grupo de compras e intereses de soluciones). Esta información incluye recuentos, búsquedas e impacto del linaje. No miran ningún dato dentro del entorno de pruebas.

* ¿Qué audiencia de cuenta tiene el tamaño de audiencia más grande y cuál es ese tamaño?
* ¿Cuántas audiencias cuenta nunca se han utilizado en ningún viaje?
* ¿Qué viajes activos utilizan la solución interés _x_?

Puede hacer preguntas a AI Assistant sobre sus conocimientos operativos en los siguientes dominios:

| Dominio | metadatos admitido | Metadatos no admitidos |
| --- | --- | --- |
| Atributos/campos | <li>Búsqueda de nombre de atributo <li>Atributo: relación de esquema <li>Atributo: relación de conjunto de datos <li>Atributo: relación audiencia <li>Relación atributo-destino | <li>Clase de atributo <li>Auditoría <li>Estado de desaprobación <li>Etiquetas <li>Valor almacenado en atributos |
| Nota Audiences <br><br>**_cuenta:_**&#x200B;AJO B2B AI Assistant solo pueden responder audiencia preguntas para el Audiences de cuenta, mientras que Experience Platform AI Assistant solo puede responder preguntas para Audiences personales | <li>Recuento de público <li>Tipo de audiencia (streaming o por lotes) <li>Fechas de creación/modificación <li>Activation estado <li>Recuento de miembros <li>Duplicar audiencias <li>Búsqueda de nombre e ID | <li>Solapamientos de público <li>Audience Activation <li>Auditoría <li>Crear/modificación <li>Etiquetas <li>abonado tendencias de cualificación |
| Flujos de datos | <li>Recuentos del flujo de datos <li>Estado de flujo de datos <li>Flujo de datos: relación conjunto de datos <li>Flujo de datos - relación fuente | <li>Creación/modificación <li>Relaciones entre flujo de datos y lotes <li>Ingesta de recuento de perfiles |
| Conjuntos de datos | <li>Recuento de conjuntos de datos <li>Estado de habilitación de perfil <li>Fecha de creación/modificación <li>Conjunto de datos: relación esquema <li>Conjunto de datos: relación audiencia <li>Conjunto de datos: relación de atributos <li>Conjunto de datos: relación de flujo de datos <li>Búsqueda de nombres <li>Nombre e ID búsqueda | <li>Auditoría <li>Creado por <li>Conjunto de datos - relación por lotes <li>Creación/modificación de conjuntos de datos <li>Tamaño del conjunto de datos <li>Número de perfiles <li>Número de filas <li>Valor búsqueda |
| Destinos | <li>Recuentos de destinos configurados <li>Destino: relación de audiencia <li>Relación de atributo de destino | <li>Configuración de cuenta <li>Información de credenciales de cuenta <li>Perfiles únicos activados |
| Recorridos (Recorridos de cuenta) | <li>Recuento <li>Nombre e ID búsqueda <li>Estado del recorrido <li>Fechas de creación/modificación | <li>Atributos: relaciones de recorrido Auditoría <li>Creación/modificación <li>Creado por |
| Esquemas | <li>Recuentos de esquemas <li>Fecha de creación/modificación <li>Relación esquema-atributo <li>Esquema: relación del conjunto de datos <li>Esquema: relación de audiencia <li>Estado de habilitación de perfil <li>Nombre búsqueda <li>Nombre e ID búsqueda | <li>Auditoría <li>Creación/modificación <li>Creado por <li>Grupos de campos <li>Identidades <li>Áreas de nombres de identidad <li>Etiquetas <li>Número de perfiles |
| Fuentes | <li>Recuentos de cuentas <li>Estado de cuenta <li>Flujos de datos activos/inactivos para cada cuenta <li>Conector de Origen: relación flujo de datos <li>Origen relación cuenta entre flujo de datos | <li>Información sobre las credenciales de la cuenta <li>Configuración de cuentaMétricas de ingesta de datos <li>Número de relaciones profilesSource - batch |
| Plantilla de grupo de compra | <li>Recuentos <li>Estado <li>Funciones <li>Nombre e ID búsqueda | <li>Reglas de rol |
| Interés de solución | <li>Recuentos <li>Estado <li>Interés de la solución: relación de plantilla del grupo de compra <li>Búsqueda de nombre e ID | <li>Interés en la solución: relación Grupo de compra |

{style="table-layout:fixed"}

En el caso de las preguntas sobre perspectivas operativas, es posible que las respuestas no reflejen el estado actual del IU. Los datos que respaldan estas preguntas se actualizan una vez cada 24 horas. Por ejemplo, los cambios que los usuarios realizan en CDP en tiempo real durante el día se sincronizan con los almacenes de datos por la noche y, a continuación, están disponibles para usuario preguntas por la mañana. Inicie sesión en un espacio aislado para consultar datos específicos relacionados con los objetos.

### Feature ámbito

Actualmente, el ámbito de AI Assistant es el siguiente:

* [Conocimiento del producto](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home#product-knowledge): AI Assistant puede responder preguntas de conocimiento del producto para el Platform de datos del cliente en tiempo real y Adobe Systems Journey Optimizer B2B Edition.

* [Perspectivas operativas](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home#operational-insights): puede hacer preguntas al Asistente de IA sobre perspectivas operativas para los siguientes objetos de datos: atributos, audiencias de cuenta, flujos de datos, conjuntos de datos, destinos, recorridos de cuenta, esquemas, fuentes, plantillas de grupos de compra e intereses de soluciones.

### Privacidad, seguridad y gobernanza

El asistente de IA de Journey Optimizer B2B edition está diseñado con privacidad, seguridad y control en la vanguardia. Revise la siguiente información para obtener más información acerca de las capacidades centradas en la confianza del cliente que puede esperar de AI Assistant:

* AI Assistant no utiliza datos personales hoy en día, ni siquiera con fines formativos.

* AI Assistant desconoce los datos de los clientes, como personas, cuenta, oportunidades y grupos de compra.

* Debe tener un permiso explícito para interactuar con AI Assistant.

   * Un administrador puede establecer permisos mediante [la interfaz de usuario de permisos](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/permissions) y [Admin Console](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/browse).

   * Los permisos son granulares y el administrador de la zona protegida puede configurar qué usuarios pueden hacer diferentes categorías de preguntas (preguntas basadas en el conocimiento del producto con el asistente de IA o preguntas sobre perspectivas operativas).

* Puede ver un registro de las interacciones anteriores con el asistente de IA con una política de retención de 30 días.

* AI Assistant se basa en datos específicos de sandbox y documentación de Adobe Systems pública al responder a usuario solicitudes. Los datos no se comparten entre entornos aislados.

* Las solicitudes que proporcionas a AI Assistant no se comparten con otros clientes.

### Preguntas frecuentes

A continuación se ofrece una lista de respuestas a las preguntas más frecuentes sobre AI Assistant en Journey Optimizer B2B Edition.

**¿La información de AI Assistant se proporciona en tiempo real?**

Los datos presentados en las respuestas de AI Assistant se actualizan diariamente. Este ciclo significa que los datos incluidos en las respuestas pueden ser hasta 24 horas más antiguos que los datos que se muestran en la interfaz de usuario en el momento de la respuesta.

**¿Cuáles son las capacidades de AI Assistant?**

AI Assistant puede abordar consultas de conocimiento producto de Adobe y puede responder preguntas relacionadas con la información operativa de sus artefactos operativos.

**¿Puede AI Assistant proporcionar información sobre los datos de los clientes?**

No. AI Assistant no tiene acceso a los datos del cliente y, por lo tanto, AI Assistant no los mira ni los utiliza.

**¿Se utiliza mi información personal en los datos de aprendizaje del Asistente de IA?**

AI Assistant no utiliza información personal con fines formativos. No proporciones ninguna información personal sobre ti (incluido tu nombre o información de contacto) ni ninguna otra parte a AI Assistant.

## Pasos siguientes

Con una comprensión general de AI Assistant, proceda a habilitar y usar AI Assistant durante su flujos de trabajo. Consulte la siguiente documentación para obtener más información:

* [Habilitar el acceso a AI Assistant](./enable-ai-assistant-access.md)
* [Guía de preguntas](./question-guidance.md)
* [Utilizar el asistente de IA](./use-ai-assistant.md)
