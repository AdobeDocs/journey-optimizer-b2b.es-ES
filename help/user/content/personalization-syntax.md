---
title: Sintaxis de personalización
description: Obtenga información sobre la sintaxis de personalización basada en Handlebars en Journey Optimizer B2B edition, incluidas expresiones, ayudantes, tipos literales y reglas de formato.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor, sintaxis, personalización
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 2%

---

# Sintaxis de personalización {#personalization-syntax}

Las expresiones del [!DNL Journey Optimizer B2B Edition] [editor de personalización](./personalization.md#personalization-editor) se basan en la sintaxis de creación de plantillas _Handlebars_. Utiliza una plantilla y un objeto de entrada para generar HTML u otros formatos de texto. Las plantillas Handlebars se parecen al texto normal con expresiones Handlebars incrustadas.

Para obtener más información sobre Handlebars y cómo funciona, consulte la [documentación de HandlebarsJS](https://handlebarsjs.com/){target="_blank"}.

## Reglas generales

Ejemplo de expresión simple:

```
{{account.accountName}}
```

Donde:

* `account` es un área de nombres.
* `accountName` es un token compuesto por atributos.

  >[!NOTE]
  >
  >La estructura de atributos se define en un [esquema XDM de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}.

* Los identificadores pueden ser cualquier carácter Unicode excepto los siguientes:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La sintaxis distingue entre mayúsculas y minúsculas.

* Las palabras **true**, **false**, **null** y **undefined** solo se permiten en la primera parte de una expresión de ruta.

* En Handlebars, los valores devueltos por {\{expression}\} son _HTML-escaped_. Si la expresión contiene `&`, el resultado devuelto con escape de HTML se generará como `&amp;`. Si no desea que Handlebars escape un valor, utilice el signo +triple-stash_.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

* Para los argumentos de funciones literales, el analizador de idioma de plantilla no admite un único símbolo de barra invertida sin escape (`\`). Este carácter debe especificarse con una barra invertida (`\`) adicional. Por ejemplo:

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## Ayudantes {#helpers-all}

Una función de ayuda Handlebars es un identificador simple que se puede anexar con parámetros. Cada parámetro es una expresión Handlebars. Se puede acceder a estos ayudantes desde cualquier contexto en una plantilla de correo electrónico.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

Para obtener información más detallada sobre estas funciones, consulte [Funciones de ayuda](./personalization-helper-functions.md).

## Tipos literales {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition] admite los siguientes tipos literales:

| Literal | Definición |
| ------- | ---------- |
| Cadena | Un tipo de datos compuesto por caracteres entre comillas dobles. <br>Ejemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Un tipo de datos que puede ser verdadero o falso. |
| Entero | Un tipo de datos que representa un número entero. Puede ser positivo, negativo o cero. <br>Ejemplos: `-201`, `0`, `412` |
| Matriz | Un tipo de datos que se comprende como un grupo de otros valores literales. Utiliza corchetes para agrupar y comas para delimitar entre distintos valores. <br> **Nota:** No puede tener acceso directo a las propiedades de los elementos de una matriz. <br> ejemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>El uso de la variable **xEvent** no está disponible en expresiones de personalización. Cualquier referencia a xEvent provoca errores de validación.
