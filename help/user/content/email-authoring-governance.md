---
title: Autor a partir de una plantilla gobernada
description: 'Cree correos electrónicos a partir de plantillas gobernadas con contenido bloqueado: identifique áreas editables y trabaje dentro de las restricciones de gobernanza en Journey Optimizer B2B edition.'
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 1%

---

# Crear a partir de una plantilla controlada

Los diseñadores de contenido pueden habilitar el [control (_bloqueo de contenido_)](./template-content-governance.md) al crear plantillas de correo electrónico. Las funciones de control les permiten designar las partes del diseño que no se pueden cambiar cuando se utilizan en un recorrido de cuentas. Cuando [selecciona una plantilla guardada](./email-authoring.md#select-a-template) para crear un mensaje de correo electrónico, el espacio de diseño visual carga la plantilla para que pueda utilizarla como base para el correo electrónico.

Si la plantilla tiene el control habilitado, se muestra una alerta en el panel de propiedades de la derecha. Puede activar **[!UICONTROL Resaltar áreas editables]** en la parte superior del lienzo para ver qué componentes y elementos de contenido se pueden editar para usarlos en el recorrido.

![Ver áreas editables en una plantilla controlada](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

También puede determinar los elementos que están bloqueados o son editables mediante el _árbol de navegación_. Haga clic en el icono _Árbol de navegación_ ( ![Icono de vínculo](../assets/do-not-localize/icon-navigation-tree.svg) ) a la izquierda del lienzo para mostrar el árbol.

![Ver áreas editables en una plantilla controlada](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Los iconos indican la configuración de bloqueo del contenido aplicada.

| Ícono | Nombre | Descripción |
|------|------|-------------|
| ![Icono de solo lectura](../assets/do-not-localize/icon-tree-lock.svg) | Solo lectura | El componente está bloqueado y no se puede editar. Cuando se aplican en el nivel raíz (_[!UICONTROL Body]_), todos los componentes secundarios están bloqueados y no se pueden editar. |
| ![Icono de edición de contenido](../assets/do-not-localize/icon-tree-content-lock.svg) | Bloqueo de contenido | El bloqueo de contenido se aplica en el nivel de componente. |
| ![Icono editable](../assets/do-not-localize/icon-edit.svg) | Editable | El componente es totalmente editable. Sin embargo, es posible que no pueda eliminar el elemento. |
| ![Icono de edición de contenido](../assets/do-not-localize/icon-tree-edit-text.svg) | Editable: solo contenido | El componente y el estilo son estáticos, pero puede cambiar el contenido (como texto o imagen). |
