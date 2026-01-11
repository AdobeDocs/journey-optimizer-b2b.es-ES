---
title: Configuraciones del canal web
description: Obtenga información sobre cómo configurar los canales web para definir propiedades web y reglas de coincidencia de página para la entrega de contenido en Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Actualmente, esta función está en versión beta limitada"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Configuraciones del canal web

Una configuración web es una propiedad web identificada por una dirección URL donde se entrega el contenido. Puede hacer coincidir una dirección URL de una sola página o varias páginas para que las experiencias web puedan enviar modificaciones en una o varias páginas web. Estas configuraciones son necesarias para que los especialistas en marketing [agreguen nodos de acción de personalización web en recorrido](../content/web-experiences.md#create-a-web-experience) y [diseñen las modificaciones de experiencia](../content/web-experience-design.md) para una campaña.

>[!BEGINSHADEBOX]

**Requisitos previos**

Para usar canales web, tu sitio web debe tener [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/es/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementado para la identificación de visitantes y la entrega de contenido. Asegúrese de que la versión de Adobe Experience Platform Web SDK sea 2.16 o superior.

La configuración del canal web en Journey Optimizer B2B edition requiere los siguientes [permisos](../admin/user-management.md#b2b-product-permissions):

* _[!UICONTROL Configuraciones de canal]_ > _[!UICONTROL Administrar ajustes preestablecidos de mensajes]_ - Necesario para crear, actualizar y eliminar configuraciones de canal web.
* _[!UICONTROL Configuraciones de canal]_ > _[!UICONTROL Ver ajustes preestablecidos de mensajes]_ - Necesario para ver las configuraciones de canal web.

>[!ENDSHADEBOX]

## Creación de una configuración de canal web

1. En el panel de navegación izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]**.

1. En _[!UICONTROL Web]_ en el panel de navegación, seleccione **[!UICONTROL Configuraciones de canal]**.

   ![Acceder a las configuraciones del canal web](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. Haga clic en **[!UICONTROL Crear configuración de canal]** en la parte superior derecha.

1. Escriba un **[!UICONTROL Nombre]** (obligatorio) y una **[!UICONTROL Descripción]** (opcional) para la configuración.

   >[!NOTE]
   >
   >Los nombres deben comenzar por una letra (A-Z) y solo pueden contener caracteres alfanuméricos. También puede utilizar caracteres de guion bajo `_`, punto `.` y guión `-`.

1. En la sección **[!UICONTROL Configuración web]**, seleccione una de las siguientes opciones:

   * **[!UICONTROL Página única]**: si desea aplicar los cambios solo a una página, escriba o seleccione una **[!UICONTROL URL de página]**.

     ![Selección de una dirección URL de página para una configuración de canal web de una sola página](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL Regla de coincidencia de páginas]**: para segmentar varias direcciones URL que coincidan con la misma regla, genere una [regla de coincidencia de páginas](#build-a-pages-matching-rule) e introduzca una **[!UICONTROL URL de creación y vista previa predeterminada]**.

1. Haga clic en **[!UICONTROL Enviar]** para guardar los cambios.

Después de guardar la configuración, pasa a estar en _Borrador_ y estará disponible para los especialistas en marketing cuando usen un canal web en sus recorridos. Puede seguir editando la configuración mientras permanezca en estado de borrador. También puede eliminar un borrador de configuración de canal web si hace clic en el icono _Más_ (**...**) que aparece junto al nombre y elige **[!UICONTROL Eliminar]**.

Tan pronto como el canal web se usa en un recorrido, pasa a un estado _Activo_. En este estado, puede editar el nombre y la descripción de la configuración. No puede cambiar la configuración web ni eliminarla.

## Reglas de coincidencia de páginas {#pages-matching-rule}

Al crear una configuración web, puede generar _[!UICONTROL reglas que coincidan con las páginas]_ para que se dirijan a varias direcciones URL que coincidan con la misma regla. Estas reglas permiten aplicar los mismos cambios de contenido en varias páginas.

Por ejemplo, es posible que desee aplicar cambios a un banner a pantalla completa en todo un sitio web o agregar una imagen superior que se muestre en todas las páginas de productos.

### Creación de reglas

1. Cuando [cree una configuración de canal web](#create-a-web-channel-configuration), elija **[!UICONTROL Regla de coincidencia de página]**.

1. Defina sus criterios para los campos **[!UICONTROL Dominio]** y **[!UICONTROL Página]** utilizando los diferentes operadores en cada sección para generar la regla.

   +++Operadores de dominio

   Utilice los siguientes operadores para dominios coincidentes según el valor de cadena introducido:

   | Operador | Descripción | Ejemplos |
   | --- | --- | --- |
   | [!UICONTROL Es igual a] | Coincidencia exacta del dominio. | |
   | [!UICONTROL Comienza con] | Coincide con todos los dominios (incluidos los subdominios) que comienzan con la cadena introducida. | `Starts with: dev` coincide con todos los dominios y subdominios que comienzan con `dev`, como `dev.example.com`, `dev.products.example.com` y `developer.example.com` |
   | [!UICONTROL Termina con] | Coincide con todos los dominios (incluidos los subdominios) que terminan con la cadena introducida. | `Ends with: example.com` coincide con todos los dominios y subdominios que terminan con `example.com`, como `stage.example.com`, `prod.example.com` y `myexample.com` |
   | [!UICONTROL Coincidencia de comodín] | Permite definir una coincidencia de comodín en medio de la cadena, como `dev.*.example.com`. Las reglas de validación requieren que el valor contenga un único comodín (asterisco) cuando el operador tiene _coincidencias de comodín_. | `Wildcard matching: dev.*.example.com` coincide con dominios como `dev.products.example.com`, `dev.mytest.products.example.com` y `dev.blog.example.com` |
   | [!UICONTROL Cualquiera] | Coincide con todos los dominios. Resulta útil al probar una ruta determinada entre dominios. | |

   +++

   +++Operadores de ruta

   Utilice los siguientes operadores para las rutas coincidentes según el valor de cadena introducido:

   | Operador | Descripción | Ejemplos |
   | --- | --- | --- |
   | [!UICONTROL Es igual a] | Coincidencia exacta de la ruta. | |
   | [!UICONTROL Comienza con] | Coincide con todas las rutas (incluidas las subrutas) que comienzan con la cadena. | |
   | [!UICONTROL Termina con] | Coincide con todas las rutas (incluidas las subrutas) que terminan con la cadena. | |
   | [!UICONTROL Cualquiera] | Coincide con todas las rutas. Resulta útil cuando se segmentan todas las rutas en uno o varios dominios. | |
   | [!UICONTROL Coincidencia de comodín] | Permite definir un comodín interno dentro de la ruta, como `/products/*/detail`. El carácter comodín `*` del componente de ruta de acceso coincide con cualquier secuencia de caracteres hasta el primer carácter `/`.  Y `/*/` coincide con cualquier secuencia de caracteres (incluidas las subrutas). | `Wildcard matching: /products/*/detail` coincide con rutas como `example.com/products/yoga/detail`, `example.com/products/surf/detail`, `example.com/products/tennis/detail` y `example.com/products/yoga/pants/detail` |
   | [!UICONTROL Contiene] | El valor se traduce a un comodín, como `*mystring*`, y coincide con todas las rutas que contienen la secuencia de caracteres. | `Contains: product` coincide con todas las rutas de acceso que contienen la cadena `product`, como `example.com/products`, `example.com/yoga/perfproduct`, `example.com/surf/productdescription` y `example.com/home/product/page` |

   +++

   Por ejemplo, para admitir cambios de contenido en todas las páginas de la solución _LumaSecure_ de su sitio web _Bodea_, seleccione **[!UICONTROL Dominio]** > **[!UICONTROL Comienza con]** > `bodea` y **[!UICONTROL Página]** > **[!UICONTROL Contiene]** > `lumasecure`.

   ![Definir una regla de coincidencia de páginas para una configuración de canal web](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. Si el caso de uso requiere varias reglas, haga clic en **[!UICONTROL Agregar otra regla de página]** y repita el paso anterior.

   * Puede definir hasta 10 reglas.

   * Use los operadores **[!UICONTROL Or]** o **[!UICONTROL Exclude]** entre las diferentes reglas.

     _[!UICONTROL Or]_ es el operador predeterminado para definir varias reglas y resulta útil para agregar varias definiciones de criterios que puedan coincidir.

     _[!UICONTROL Excluir]_ resulta útil cuando una de las páginas que coinciden con la regla definida no debe ser un destino. Por ejemplo, puede dirigirse a todas las `bodea.com` páginas que contienen `lumasecure`, pero excluyendo las páginas de blog (como `bodea.com/blogs/lumasecure/latest-release`).

   ![Las páginas coinciden con las reglas con exclusión](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. Escriba la **[!UICONTROL URL de creación y vista previa predeterminada]**.

   Este paso garantiza que las páginas generadas o coincidentes por la regla tengan una URL designada tanto para el diseño del contenido de la experiencia web como para la vista previa.

## Duplicación de un canal web

Puede duplicar una configuración de canal web existente y cambiarla para crear un nuevo canal web basado en una existente. No se puede modificar una configuración de canal Web activa guardada en la biblioteca.

1. Haga clic en el icono _Más menú_ (**...**) de la variante y elija **[!UICONTROL Duplicado]**.

   ![Haga clic en el icono del menú Más para duplicar una configuración de canal web existente](./assets/config-web-channels-more-menu.png){width="450"}

   Esta acción crea un canal web duplicado con `_Copy_nnn` anexado al nombre.

1. Haga clic en el nombre del canal web duplicado para editar los parámetros.

   * Cambie el nombre y la descripción para que coincidan con el propósito o los elementos de la regla.
   * Si es necesario, cambie la dirección URL de una sola página.
   * Si es necesario, cambie la regla de coincidencia de páginas según sus necesidades.

1. Cuando finalice la configuración, haga clic en **[!UICONTROL Enviar]**.
