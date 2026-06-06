---
title: Aplicaciones de una sola página
description: 'Cree experiencias web para aplicaciones de una sola página (SPA): configure el seguimiento de vistas, gestione el contenido dinámico y administre la navegación del lado del cliente en Journey Optimizer B2B edition.'
feature: Channels, Personalization
role: User
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
exl-id: 7691006d-3d22-4db4-94d3-cfd420128b86
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
autotag-review: 2026-03-30T22:02:23.111Z
TQID: https://experienceleague.adobe.com/L5Mn4u-o4xACD2L1TW2lx7pB9gkC3O2uRmL8b0alDkA
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 846
ht-degree: 2%

---

# Aplicaciones de una sola página

Las aplicaciones de una sola página (SPA) presentan desafíos únicos para la personalización web porque actualizan dinámicamente el contenido de la página sin recargas de página completas. Journey Optimizer B2B edition proporciona herramientas especializadas para gestionar la personalización de SPA de forma eficaz.

## Explicación de SPA

A diferencia de los sitios web tradicionales de varias páginas, en los que cada navegación déclencheur una carga de página completa, las SPA utilizan JavaScript para actualizar el contenido de forma dinámica, manteniendo al mismo tiempo una sola página de HTML. Este método tiene varias consideraciones para las experiencias web:

* **No hay recargas de página**: los cambios de contenido se producen sin activar los eventos tradicionales de carga de página.
* **Vistas virtuales** - Diferentes _vistas_ o _pantallas_ dentro de la SPA que deben seguirse como páginas separadas.
* **Enrutamiento del lado del cliente**: los enrutadores JavaScript (como React Router, Vue Router y Angular Router) administran la navegación en lugar de las solicitudes del servidor.
* **DOM dinámico**: los elementos de página se pueden crear, modificar o eliminar después de la carga inicial de la página.

## Configuración de la compatibilidad con SPA

Para personalizar las SPA de forma eficaz, debe configurar el seguimiento de vistas para que Journey Optimizer B2B edition pueda identificar cuándo los usuarios navegan entre vistas virtuales.

### Configuración de declaraciones de vista

Trabaje con su equipo de desarrollo para implementar declaraciones de vista mediante Adobe Web SDK. El uso de estas declaraciones de vista implica llamar al comando `sendEvent` con información de vista cada vez que el SPA navega a una nueva vista.

**Implementación de ejemplo:**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### Ver convenciones de nomenclatura

Utilice nombres de vista coherentes y descriptivos que coincidan con la estructura lógica de la aplicación:

| Ver | Nombre de ejemplo |
| ---- | ------------ |
| Página de inicio | `home` |
| Lista de productos | `product-list` |
| Detalles del producto | `product-detail` |
| Carro de compras | `cart` |
| Finalizar compra | `checkout` |
| Tablero de cuentas | `account-dashboard` |

>[!NOTE]
>
>Los nombres de las vistas distinguen entre mayúsculas y minúsculas. Utilice una convención de nombres uniforme (se recomiendan minúsculas con guiones) en la implementación.

## Creación de experiencias web para SPA

Cuando cree experiencias web para SPA, tenga en cuenta las siguientes prácticas recomendadas:

### Vistas específicas del objetivo

* En la [configuración del canal web](../admin/configure-channels-web.md), configure las reglas de coincidencia de URL que se alineen con la estructura de enrutamiento de SPA.

* Al crear modificaciones, especifique la vista donde debe aplicarse la modificación.

* Utilice selectores CSS dirigidos a elementos específicos de cada vista.

### Gestión del contenido dinámico

Las SPA suelen cargar el contenido dinámicamente después del procesamiento inicial de la página. Utilice estas técnicas para asegurarse de que las modificaciones se aplican correctamente:

#### Esperar elementos

Configure las modificaciones para esperar a que los elementos de destinatario existan antes de aplicar:

1. En el editor no visual, agregue una modificación con un selector CSS.

1. Habilite **[!UICONTROL Esperar al elemento]** y especifique el tiempo de espera máximo.

1. La modificación se aplica una vez que el elemento de destino aparece en el DOM.

#### Implementar observadores de mutaciones

Para el contenido altamente dinámico, Web SDK incluye observadores de mutación que detectan cuándo se añaden nuevos elementos a la página. Estos observadores garantizan que las modificaciones se apliquen incluso cuando los elementos se cargan asincrónicamente.

### Marcos de SPA

Las experiencias web de Journey Optimizer B2B edition funcionan con marcos de SPA populares:

| Marco | Consideraciones |
| --------- | -------------- |
| **Reaccionar** | Las modificaciones se aplican después de que React procese componentes en el DOM. Utilice nombres de clase o atributos de datos para el direccionamiento. |
| **Angular** | Elementos de destino después de ejecutar la detección de cambios de Angular. Evite segmentar elementos con `*ngIf` antes de que se representen. |
| **Vue.js** | Espere a que Vue `nextTick` se asegure de que los elementos se encuentren en el DOM. Utilice referencias o atributos personalizados para una segmentación estable. |
| **Next.js / Nuxt.js** | Para las páginas SSR/SSG, asegúrese de que la hidratación de Web SDK se complete antes de esperar modificaciones. |

## Prácticas recomendadas para la personalización de SPA

### Uso de selectores estables

Las SPA suelen generar nombres de clase dinámicos o ID (especialmente con soluciones CSS-en-JS). Como alternativa, puede utilizar:

* **Atributos de datos** - Agregar atributos de datos personalizados (`data-testid`, `data-section`, etc.) a los elementos que desee segmentar.
* **HTML semántico**: destino basado en la estructura y los elementos semánticos de HTML.
* **Atributos de ID** - Use atributos de ID estables siempre que sea posible.

**Ejemplo:**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**Selector de CSS:** `[data-action="signup"]`

### Vistas de prueba

Al probar experiencias web de SPA:

1. Navegue por todas las vistas donde se aplican las modificaciones.

1. Pruebe el flujo de usuario completo, incluido lo siguiente:
   * Navegación directa a una vista (vinculación profunda)
   * Navegación desde otras vistas dentro de la SPA
   * Navegación hacia atrás y hacia adelante del explorador

1. Compruebe que las modificaciones se vuelven a aplicar al volver a una vista visitada anteriormente.

### Controlar transiciones de vista

Algunos SPA utilizan animaciones o transiciones entre vistas. Considere:

* **Intervalo**: asegúrese de que las modificaciones se apliquen después de completar las animaciones de transición.
* **Visibilidad del elemento**: los elementos pueden existir pero están ocultos durante las transiciones.
* **Parpadeo**: aplique las modificaciones con la suficiente antelación para evitar cambios en el contenido visible.

## Resolución de problemas

A medida que revise los cambios de diseño de la SPA, utilice las siguientes recomendaciones para abordar algunos problemas comunes:

* **Las modificaciones no aparecen**. Si no aparecen en su SPA:

   1. **Comprobar seguimiento de vista** - Comprobar que las llamadas de `sendEvent` incluyen el nombre de vista correcto.

   1. **Verificar la existencia del elemento** - Asegúrese de que los elementos de destino estén en el DOM cuando se apliquen las modificaciones.

   1. **Revisar selectores**: confirme que los selectores CSS coinciden con la estructura DOM real.

   1. **Comprobar consola**: busque errores de JavaScript que puedan impedir modificaciones.

* **Modificaciones que aparecen brevemente y luego desaparecen**. Este problema suele ocurrir cuando el SPA vuelve a procesar y reemplaza elementos modificados:

   1. Utilice selectores CSS más específicos que permanezcan estables entre procesamientos.

   1. Permitir que los observadores de mutaciones vuelvan a aplicar modificaciones cuando se vuelvan a crear los elementos.

   1. Trabaje con su equipo de desarrollo para añadir atributos estables a los elementos de destino.

* **Duplicar modificaciones** - Si las modificaciones aparecen varias veces:

   1. Compruebe que los eventos de seguimiento de vista se activan solo una vez por transición de vista.

   1. Compruebe que las modificaciones están enfocadas a vistas específicas en lugar de aplicarse globalmente.

## Temas relacionados

* [Información general sobre experiencias web](./web-experiences.md)
* [Diseño de experiencia web](./web-experience-design.md)
* [Configuraciones del canal web](../admin/configure-channels-web.md)
