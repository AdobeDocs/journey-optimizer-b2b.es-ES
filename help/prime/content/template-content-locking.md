---
title: Bloqueo de contenido para plantillas de correo electrónico
description: Utilice la configuración de gobernanza en Journey Optimizer B2B Prime para bloquear el contenido en plantillas de correo electrónico en el nivel de estructura o componente y controlar lo que los autores de correo electrónico pueden editar.
badgeBeta: label="Beta" type="informative" tooltip="Esta función forma parte de una versión beta limitada."
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# Bloqueo de contenido para plantillas de correo electrónico

El bloqueo de contenido permite a los autores de plantillas definir reglas de gobernanza que restringen qué partes de una plantilla de correo electrónico se pueden modificar cuando se utiliza en un recorrido. Esto ayuda a los equipos de conformidad y marca a proteger los elementos clave de diseño, como encabezados, logotipos y contenido legal, al tiempo que permiten a los equipos de marketing personalizar el mensaje dentro de la estructura aprobada.

>[!NOTE]
>
>El bloqueo de contenido es una función de control en el nivel de editor. Controla lo que los autores pueden editar en el espacio de diseño de correo electrónico, pero no evita los cambios realizados a través de la API.

Solo los usuarios que tengan el permiso **[!UICONTROL Administrar plantillas de contenido]** pueden establecer la configuración de control.

## Modos de gobernanza {#modes}

Cuando habilite el control en una plantilla, seleccione uno de estos dos modos:

| Modo | Descripción |
| ---- | ----------- |
| **[!UICONTROL Bloqueo de contenido]** | Bloquear selectivamente estructuras o componentes específicos. Los autores pueden editar las áreas desbloqueadas. |
| **[!UICONTROL Sólo lectura]** | Bloquee toda la plantilla. Los autores pueden aplicarlo a un correo electrónico, pero no pueden modificar ninguna parte de su contenido. |

## Habilitar gobernanza {#enable}

1. Abra la plantilla en el espacio de diseño de correo electrónico.
1. En el carril derecho, haga clic en el componente **[!UICONTROL Cuerpo]** para seleccionarlo.
1. Alternar en **[!UICONTROL Gobernanza]**.
1. En el menú desplegable de modo, seleccione **[!UICONTROL Bloqueo de contenido]** o **[!UICONTROL Solo lectura]**.

Si seleccionó **[!UICONTROL Bloqueo de contenido]**, siga bloqueando elementos individuales.

### Bloqueo de una estructura {#lock-structure}

1. En el lienzo, seleccione la estructura (diseño de columna) que desee proteger.
1. En el carril derecho, habilite la opción **[!UICONTROL Bloquear estructura]**.

Todo el contenido anidado en una estructura bloqueada se bloquea automáticamente. Para permitir que un componente específico dentro de una estructura bloqueada permanezca editable, seleccione el componente y habilite **[!UICONTROL Editable]** en el carril derecho.

### Bloquear un componente {#lock-component}

En una estructura editable, puede bloquear componentes de contenido individuales.

1. Seleccione el componente en el lienzo.
1. En el carril derecho, habilite la opción **[!UICONTROL Bloquear contenido]**.

### Permitir adiciones de contenido {#allow-additions}

Al usar el modo **[!UICONTROL Bloqueo de contenido]**, puede permitir que los autores agreguen contenido nuevo a la plantilla mientras mantiene los elementos bloqueados protegidos:

1. Habilitar **[!UICONTROL Permitir la adición de contenido]**.
1. Elija si los autores pueden agregar estructuras y componentes de contenido o solo componentes de contenido.

## Identificar elementos bloqueados {#identify}

El **[!UICONTROL árbol de navegación]** en el carril izquierdo muestra iconos de candado y lápiz para ayudar a los autores a identificar rápidamente lo que pueden y no pueden modificar:

* Un **icono de candado** indica un elemento que está bloqueado.
* Un **icono de lápiz** indica un elemento que se puede editar.

Los elementos bloqueados se indican visualmente en el lienzo cuando un autor abre la plantilla.

## Consideraciones

La configuración de gobernanza se guarda con la plantilla. Cualquier correo electrónico creado a partir de una plantilla controlada hereda su configuración de bloqueo en el momento en que se aplica. La actualización de la configuración de gobernanza en una plantilla no afecta a los correos electrónicos creados anteriormente a partir de ella.
