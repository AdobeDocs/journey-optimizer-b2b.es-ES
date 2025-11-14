---
title: Funciones de ayuda
description: Guía de referencia para funciones de ayuda de personalización en Journey Optimizer B2B edition. Incluye sintaxis y ejemplos de cadenas, fechas, matemáticas, etc.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor, sintaxis, personalización
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4857'
ht-degree: 6%

---

# Funciones de ayuda

Utilice las funciones de ayuda del editor de personalización para definir experiencias de contenido personalizado con precisión y eficacia, manipulando datos, realizando cálculos y dando formato al contenido. Explore y experimente con estas funciones, operadores y ayudantes para descubrir cómo trabajan juntos para ayudarle a crear recorridos personalizados y basados en datos.

>[!AVAILABILITY]
>
>Las funciones de ayuda están disponibles para los entornos de B2B edition de Journey Optimizer que se proporcionan en la [arquitectura simplificada](../simplified-architecture.md).

## Funciones de agregación

Utilice funciones de agregación para agrupar varios valores y formar un único valor de resumen. También puede utilizar funciones de matriz y lista para definir más fácilmente las interacciones con matrices, listas y cadenas.

### media {#average}

Utilice la función `average` para devolver la media aritmética de todos los valores seleccionados dentro de la matriz.

+++Sintaxis

```sql
{%= average(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio medio de todos los pedidos.

```sql
{%=average(orders.order.price)%}
```

+++

### recuento {#count}

Utilice la función `count` para devolver el número de elementos dentro de la matriz determinada.

+++Sintaxis

```sql
{%= count(array) %}
```

**Ejemplo**

La siguiente operación devuelve el número de pedidos de la matriz.

```sql
{%= count(orders) %}
```

+++

### max {#max}

Utilice la función `max` para devolver el mayor de todos los valores seleccionados dentro de la matriz.

+++Sintaxis

```sql
{%= max(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio más alto de todos los pedidos.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

Utilice la función `min` para devolver el menor de todos los valores seleccionados dentro de la matriz.

+++Sintaxis

```sql
{%= min(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio más bajo de todos los pedidos.

```sql
{%=min(orders.order.price) %}
```

+++

### sum {#sum}

Utilice la función `sum` para devolver la suma de todos los valores seleccionados dentro de la matriz.

+++Sintaxis

```sql
{%= sum(array) %}
```

**Ejemplo**

La siguiente operación devuelve la suma de todos los precios de los pedidos.

```sql
 {%=sum(orders.order.price)%}
```

+++

## Funciones aritméticas {#maths}

Utilice funciones aritméticas para realizar cálculos básicos de los valores.

### añadir {#add}

Utilice la función `+` (suma) para encontrar la suma de dos expresiones de argumento.

+++Sintaxis

```sql
{%= double + double %}
```

**Ejemplo**

La siguiente operación suma el precio de dos productos diferentes.

```sql
{%= product1.price + product2.price %}
```

+++

### multiplicar {#multiply}

Utilice la función `*` (multiplicación) para buscar el producto de dos expresiones de argumento.

+++Sintaxis

```sql
{%= double * double %}
```

**Ejemplo**

La siguiente operación encuentra el producto del inventario y el precio de un producto para encontrar el valor bruto del producto.

```sql
{%= product.inventory * product.price %}
```

+++

### restar {#substract}

Utilice la función `-` (resta) para encontrar la diferencia de dos expresiones de argumento.

+++Sintaxis

```sql
{%= double - double %}
```

**Ejemplo**

La siguiente operación encuentra la diferencia de precio entre dos productos diferentes.

```sql
{%= product1.price - product2.price %}
```

+++

### dividir {#divide}

Utilice la función `/` (división) para encontrar el cociente de dos expresiones de argumento.

+++Sintaxis

```sql
{%= double / double %}
```

**Ejemplo**

La siguiente operación encuentra el cociente entre el total de productos vendidos y el total de dinero ganado para ver el coste promedio por artículo.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### resto {#remainder}

Utilice la función `%` (resto) para buscar el resto después de dividir las dos expresiones de argumento.

+++Sintaxis

```sql
{%= double % double %}
```

**Ejemplo**

La siguiente operación comprueba si la edad de la persona es divisible entre cinco.

```sql
{%= person.age % 5 = 0 %}
```

+++

## Funciones de matrices y listas {#arrays}

Utilice estas funciones para facilitar la interacción con matrices, listas y cadenas.

### countOnlyNull {#count-only-null}

Utilice la función `countOnlyNull` para contar el número de valores nulos de una lista.

+++Sintaxis

```sql
{%= countOnlyNull(array) %}
```

**Ejemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Devuelve 3.

+++

### countWithNull {#count-with-null}

Utilice la función `countWithNull` para contar todos los elementos de una lista, incluidos los valores nulos.

+++Sintaxis

```sql
{%= countWithNull(array) %}
```

**Ejemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Devuelve 6.

+++

### distinct {#distinct}

Utilice la función `distinct` para obtener valores de una matriz o lista con valores duplicados eliminados.

+++Sintaxis

```sql
{%= distinct(array) %}
```

**Ejemplo**

La siguiente operación especifica las personas que han realizado pedidos en más de un almacén.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### distinctCountWithNull {#distinct-count-with-null}

Utilice la función `distinctCountWithNull` para contar el número de valores diferentes de una lista, incluidos los valores nulos.

+++Sintaxis

```sql
{%= distinctCountWithNull(array) %}
```

**Ejemplo**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Devuelve 3.

+++

### dirigir {#head}

Utilice la función `head` para devolver el primer elemento de una matriz o lista.

+++Sintaxis

```sql
{%= head(array) %}
```

**Ejemplo**

La siguiente operación devuelve el primero de los cinco pedidos principales con el precio más alto. Encontrará más información sobre la función `topN` en la sección [primeros `n` de la matriz](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

La función `topN` ordena una matriz en orden descendente en función de la expresión numérica dada y devuelve los primeros `N` elementos. Si el tamaño de la matriz es menor que `N`, devuelve toda la matriz ordenada.

+++Sintaxis

```sql
{%= topN(array, value, amount) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{ARRAY}` | Matriz o lista que se va a ordenar. |
| `{VALUE}` | Propiedad utilizada para ordenar la matriz o la lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente operación devuelve los cinco primeros pedidos con el precio más bajo.

```sql
{%= topN(orders,price, 5) %}
```

+++

### en {#in}

Utilice la función `in` para determinar si un elemento es miembro de una matriz o lista.

+++Sintaxis

```sql
{%= in(value, array) %}
```

**Ejemplo**

La siguiente operación define a las personas con cumpleaños en marzo, junio o septiembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### incluye {#includes}

Utilice la función `includes` para determinar si una matriz o lista contiene un elemento determinado.

+++Sintaxis

```sql
{%= includes(array,item) %}
```

**Ejemplo**

La siguiente operación define a las personas cuyo color favorito incluye el rojo.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### intersecciones {#intersects}

La función `intersects` se usa para determinar si dos matrices o listas tienen al menos un miembro común.

+++Sintaxis

```sql
{%= intersects(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas cuyos colores favoritos incluyen al menos uno de rojo, azul o verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

La función `bottomN` ordena una matriz en orden ascendente en función de la expresión numérica dada y devuelve los primeros `N` elementos. Si el tamaño de la matriz es menor que `N`, devuelve toda la matriz ordenada.

+++Sintaxis

```sql
{%= bottomN(array, value, amount) %}
```

| Argumento | Descripción |
| --------- | ----------- | 
| `{ARRAY}` | Matriz o lista que se va a ordenar. |
| `{VALUE}` | Propiedad utilizada para ordenar la matriz o la lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente operación devuelve los últimos cinco pedidos con el precio más alto.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

Utilice la función `notIn` para determinar si un elemento no es miembro de una matriz o lista.

>[!NOTE]
>
>La función `notIn`also *de* garantiza que ninguno de los valores es igual a nulo. Por lo tanto, los resultados no son una negación exacta de la función `in`.

+++Sintaxis

```sql
{%= notIn(value, array) %}
```

**Ejemplo**

La siguiente operación define a las personas con cumpleaños que no se celebran en marzo, junio o septiembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

Utilice la función `subsetOf` para determinar si una matriz específica (matriz A) es un subconjunto de otra matriz (matriz B). En otras palabras, que todos los elementos de la matriz A son elementos de la matriz B.

+++Sintaxis

```sql
{%= subsetOf(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas que han visitado todas sus ciudades favoritas.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### supersetOf {#superset}

Utilice la función `supersetOf` para determinar si una matriz específica (matriz A) es un superconjunto de otra matriz (matriz B). En otras palabras, esa matriz A contiene todos los elementos de la matriz B.

+++Sintaxis

```sql
{%= supersetOf(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas que han comido sushi y pizza al menos una vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## Funciones de fecha y hora {#date-time}

Utilice las funciones de fecha y hora para realizar operaciones de fecha y hora en los valores.

### addDays {#add-days}

La función `addDays` ajusta una fecha determinada en un número determinado de días, utilizando valores positivos para aumentar y valores negativos para disminuir.

+++Sintaxis

```sql
{%= addDays(date, number) %}
```

**Ejemplo**

* Entrada: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Salida: `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

La función `addHours` ajusta una fecha determinada en un número determinado de horas, utilizando valores positivos para aumentar y valores negativos para disminuir.

+++Sintaxis

```sql
{%= addHours(date, number) %}
```

**Ejemplo**

* Entrada: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Salida: `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

La función `addMinutes` ajusta una fecha determinada en un número determinado de minutos, utilizando valores positivos para aumentar y valores negativos para disminuir.

+++Sintaxis

```sql
{%= addMinutes(date, number) %}
```

**Ejemplo**

* Entrada: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Salida: `2024-11-01T18:09:51Z`

+++

### addMonths {#add-months}

La función `addMonths` ajusta una fecha determinada en un número determinado de meses, utilizando valores positivos para aumentar y valores negativos para disminuir.

+++Sintaxis

```sql
{%= addMonths(date, number) %}
```

**Ejemplo**

* Entrada: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Salida: `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

La función `addSeconds` ajusta una fecha determinada en un número determinado de segundos, utilizando valores positivos para aumentar y valores negativos para disminuir.

+++Sintaxis

```sql
{%= addSeconds(date, number) %}
```

**Ejemplo**

* Entrada: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Salida: `2024-11-01T17:20:01Z`

+++

### addYears {#add-years}

La función `addYears` ajusta una fecha determinada en un número determinado de años, utilizando valores positivos para aumentar y valores negativos para disminuir.

+++Sintaxis

```sql
{%= addYears(date, number) %}
```

**Ejemplo**

* Entrada: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Salida: `2026-11-01T17:19:51Z`

+++

### edad {#age}

Utilice la función `age` para recuperar la edad de una fecha determinada.

+++Sintaxis

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

La función `ageInDays` calcula el número de días transcurridos entre la fecha determinada y la fecha actual. Utiliza negativo para fechas futuras y positivo para fechas pasadas.

+++Sintaxis

```sql
{%= ageInDays(date) %}
```

**Ejemplo**

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asia/Calcuta)

* Entrada: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Salida: `5`

+++

### ageInMonths {#age-months}

La función `ageInMonths` calcula el número de meses transcurridos entre la fecha determinada y la fecha actual. Utiliza negativo para fechas futuras y positivo para fechas pasadas.

+++Sintaxis

```sql
{%= ageInMonths(date) %}
```

**Ejemplo**

currentDate = 2025-01-07T12:22:46.993748+05:30(Asia/Calcuta)

* Entrada: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Salida: `12`

+++

### compareDates {#compare-dates}

La función `compareDates` compara la fecha de la primera entrada con la otra. Devuelve 0 si fecha1 es igual a fecha2, -1 si fecha1 es anterior a fecha2 y 1 si fecha1 es posterior a fecha2.

+++Sintaxis

```sql
{%= compareDates(date1, date2) %}
```

**Ejemplo**

* Entrada: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Salida: `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

La función `convertZonedDateTime` convierte una fecha y hora en una zona horaria determinada.

+++Sintaxis

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**Ejemplo**

* Entrada: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Salida: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

Utilice la función `currentTimeInMillis` para recuperar el tiempo actual en milisegundos epoch.

+++Sintaxis

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

Utilice la función `dateDiff` para recuperar la diferencia entre dos fechas en número de días.

+++Sintaxis

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

`dayOfMonth` devuelve el número que representa el día del mes.

+++Sintaxis

```sql
{%= dayOfMonth(datetime) %}
```

**Ejemplo**

* Entrada: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Salida: `5`

+++

### DayOfWeek {#day-week}

Utilice la función `dayOfWeek` para recuperar el día de la semana.

+++Sintaxis

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

Utilice la función `dayOfYear` para recuperar el día del año.

+++Sintaxis

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

La función `diffInSeconds` devuelve la diferencia entre dos fechas en términos de segundos.

+++Sintaxis

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**Ejemplo**

* Entrada: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Salida: `50`

+++

### extractHours {#extract-hours}

La función `extractHours` extrae el componente de hora de una marca de tiempo determinada.

+++Sintaxis

```sql
{%= extractHours(date) %}
```

**Ejemplo**

* Entrada: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `17`

+++

### extractMinutes {#extract-minutes}

La función `extractMinutes` extrae el componente de minuto de una marca de tiempo determinada.

+++Sintaxis

```sql
{%= extractMinutes(date) %}
```

**Ejemplo**

* Entrada: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `19`

+++

### extractMonths {#extract-months}

La función `extractMonth` extrae el componente de mes de una marca de tiempo determinada.

+++Sintaxis

```sql
{%= extractMonths(date) %}
```

**Ejemplo**

* Entrada: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `11`

+++

### extractSeconds {#extract-seconds}

La función `extractSeconds` extrae el segundo componente de una marca de tiempo determinada.

+++Sintaxis

```sql
{%= extractSeconds(date) %}
```

**Ejemplo**

* Entrada: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `51`

+++

### formatDate {#format-date}

Utilice la función `formatDate` para dar formato a un valor de fecha y hora. El formato debe ser un patrón Java `DateTimeFormat` válido.

+++Sintaxis

```sql
{%= formatDate(datetime, format) %}
```

Donde la primera cadena es el atributo de fecha y el segundo valor es cómo desea que se convierta y muestre la fecha.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha vuelve al formato estándar ISO.
>
> Puede utilizar las funciones de formato de fecha de Java como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Ejemplo**

La siguiente operación devuelve la fecha en el siguiente formato: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### Caracteres de patrón {#pattern-characters}

Algunas letras de patrón pueden tener un aspecto similar, pero representan conceptos diferentes.

| Patrón | Significado | Ejemplo (para `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Año natural (año estándar) | `2023` |
| `Y` | Año basado en la semana (ISO 8601). Puede diferir en los límites del año. | `2024` (el 31 de diciembre de 2023 cae en la primera semana de 2024) |
| `M` | Mes del año (1-12 o texto como `Jan`, `January`) | `12` o `Dec` |
| `m` | Minuto de la hora (0-59) | `15` |
| `d` | Día del mes (1-31) | `31` |
| `D` | Día del año (1-366) | `365` |

#### Formato de fecha con compatibilidad con configuración regional {#format-date-locale}

Puede usar la función `formatDate` para dar formato a un valor de fecha y hora en su representación correspondiente con distinción de idioma, como para una configuración regional deseada. El formato debe ser un patrón Java `DateTimeFormat` válido.

+++Sintaxis

```sql
{%= formatDate(datetime, format, locale) %}
```

Cuando la primera cadena es el atributo de fecha, el segundo valor es cómo desea que se convierta y muestre la fecha y el tercer valor representa la configuración regional en formato de cadena.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha vuelve al formato estándar ISO.
>
> Puede usar funciones de formato de fecha Java como se resume en la [documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Puede usar formato y configuraciones regionales válidas, tal como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Configuraciones regionales compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Ejemplo**

La siguiente operación devuelve la fecha en el siguiente formato: MM/dd/AA y configuración regional FRANCIA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

La función `getCurrentZonedDateTime` devuelve la fecha y la hora actuales con información de zona horaria.

+++Sintaxis

```sql
{%= getCurrentZonedDateTime() %}
```

**Ejemplo**

* Entrada: `{%= getCurrentZonedDateTime() %}`
* Salida: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

La función `diffInHours` devuelve la diferencia entre dos fechas en términos de horas.

+++Sintaxis

```sql
{%= diffInHours(endDate, startDate) %}
```

**Ejemplo**

* Entrada: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Salida: `10`

+++

### diffInMinutes {#diff-minutes}

La función `diffInMinutes` devuelve la diferencia entre dos fechas en términos de minutos.

+++Sintaxis

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**Ejemplo**

* Entrada: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Salida: `60`

+++

### diffInMonths {#months-difference}

La función `diffInMonths` devuelve la diferencia entre dos fechas en términos de meses.

+++Sintaxis

```sql
{%= diffInMonths(endDate, startDate) %}
```

**Ejemplo**

* Entrada: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Salida: `3`

+++

### setDays {#set-days}

Utilice la función `setDays` para establecer el día del mes para la fecha y hora determinadas.

+++Sintaxis

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

Utilice la función `setHours` para establecer la hora de la fecha y hora.

+++Sintaxis

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

La función `toDateTime` convierte la cadena en fecha. Devuelve la fecha epoch como salida para una entrada no válida.

+++Sintaxis

```sql
{%= toDateTime(string, string) %}
```

**Ejemplo**

* Entrada: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Salida: `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

Utilice la función `toUTC` para convertir una fecha y hora a UTC.

+++Sintaxis

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

Utilice la función `truncateToStartOfDay` para modificar una fecha y hora determinada estableciéndola en el inicio del día con la hora 00:00.

+++Sintaxis

```sql
{%= truncateToStartOfDay(date) %}
```

**Ejemplo**

* Entrada: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Salida: `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

Utilice la función `truncateToStartOfQuarter` para truncar una fecha y hora al primer día de su trimestre (por ejemplo, el 1 de enero, el 1 de abril, el 1 de julio y el 1 de octubre) a las 00:00.

+++Sintaxis

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**Ejemplo**

* Entrada: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

La función `truncateToStartOfWeek` modifica una fecha y hora determinada al establecerla en el inicio de la semana (lunes a las 00:00).

+++Sintaxis

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**Ejemplo**

* Entrada: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Salida: `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

Utilice la función `truncateToStartOfYear` para modificar una fecha y hora determinada truncándola al primer día del año (1 de enero) a las 00:00.

+++Sintaxis

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**Ejemplo**

* Entrada: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

Utilice la función `weekOfYear` para recuperar la semana del año.

+++Sintaxis

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYears {#diff-years}

Utilice la función `diffInYears` para devolver la diferencia entre dos fechas en términos de años.

+++Sintaxis

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**Ejemplo**

* Entrada: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Salida: `5`

+++

## Funciones del operador {#operators}

Utilice las funciones booleana y de comparación para realizar evaluaciones lógicas.

### y {#and}

La función `and` se usa para crear una conjunción lógica.

+++Sintaxis

```sql
{%= query1 and query2 %}
```

**Ejemplo**

La siguiente operación devuelve todas las personas con país de origen (Francia) y año de nacimiento (1985).

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### o {#or}

La función `or` se usa para crear una disyunción lógica.

+++Sintaxis

```sql
{%= query1 or query2 %}
```

**Ejemplo**

La siguiente operación devuelve todas las personas con país de origen (Francia) o año de nacimiento (1985).

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### igual a {#operator-equals}

La función `=` (igual) comprueba si un valor o expresión es igual a otro valor o expresión.

+++Sintaxis

```sql
{%= expression = value %}
```

**Ejemplo**

La siguiente operación comprueba si el país de la dirección postal es Francia.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### no igual {#notequal}

La función `!=` (no es igual) comprueba si un valor o expresión es **no** igual a otro valor o expresión.

+++Sintaxis

```sql
{%= expression != value %}
```

**Ejemplo**

La siguiente operación comprueba si el país de la dirección postal no es Francia.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### más que {#greaterthan}

Utilice la función `>` (mayor que) para comprobar si el primer valor es mayor que el segundo valor.

+++Sintaxis

```sql
{%= expression1 > expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas estrictamente después de 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### mayor que o igual a {#greaterthanorequal}

Utilice la función `>=` (mayor o igual que) para comprobar si el primer valor es mayor o igual que el segundo valor.

+++Sintaxis

```sql
{%= expression1 >= expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas en o después de 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### menos que {#lessthan}

Utilice la función de comparación `<` (menor que) para comprobar si el primer valor es menor que el segundo valor.

+++Sintaxis

```sql
{%= expression1 < expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas antes del año 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### menor que o igual a{#lessthanorequal}

Utilice la función de comparación `<=` (menor o igual que) para comprobar si el primer valor es menor o igual que el segundo valor.

+++Sintaxis

```sql
{%= expression1 <= expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas en 2000 o antes.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## Funciones dinámicas {#dynamic-helpers}

Utilice las funciones de ayuda dinámica para utilizar evaluaciones condicionales, iteraciones y asignaciones de variables para la personalización dinámica.

### Valor de reserva predeterminado {#default-value}

El asistente `Default Fallback Value` se usa para devolver un valor de reserva predeterminado si un atributo está vacío o es nulo. Este mecanismo funciona para atributos de perfil y eventos de Recorrido.

+++Sintaxis

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

En este ejemplo, el valor `there` se muestra si el atributo `firstName` de este perfil está vacío o es nulo.

+++

### if (condiciones) {#if-function}

El asistente `if` se usa para definir un bloque condicional.
Si la evaluación de la expresión devuelve true, se procesa el bloque; de lo contrario, se omite.

+++Sintaxis

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Después del asistente `if`, puede escribir una instrucción `else` para especificar un bloque de código que se va a ejecutar, si la misma condición es falsa.
La instrucción `elseif` especifica una nueva condición que se debe probar si la primera instrucción devuelve el valor &quot;False&quot;.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### a menos {#unless}

Use el asistente de `unless` para definir un bloque condicional. Por oposición al asistente `if`, si la evaluación de la expresión devuelve false, se procesará el bloque.

+++Sintaxis

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Ejemplo**

Presente contenido basado en la extensión de dirección de correo electrónico:

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### cada {#each}

Utilice el asistente `each` para iterar en una matriz.

La estructura de ayuda es ```{{#each ArrayName}}``` YourContent `{{/each}}`

Puede usar la palabra clave `this` dentro del bloque para hacer referencia a los elementos de matriz individuales. Utilice `{{@index}}` para procesar el índice del elemento de la matriz.

+++Sintaxis

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Ejemplo**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Ejemplo**

Procese una lista de productos que este usuario tiene en el carro de compras:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### con {#with}

Use el ayudante `with` para cambiar el token de evaluación de la plantilla-parte.

+++Sintaxis

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

El ayudante `with` también resulta útil para definir una variable de acceso directo.

**Ejemplo**

Use `with` para asignar nombres de variables largos a otros más cortos:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### dejar {#let}

La función `let` permite almacenar una expresión como variable para usarla posteriormente en una consulta.

+++Sintaxis

```sql
{% let variable = expression %} {{variable}}
```

**Ejemplo**

El siguiente ejemplo permite calcular la suma total de los precios de los productos del carro de compras con precios entre 100 y 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## Metadatos de ejecución {#execution-metadata}

>[!AVAILABILITY]
>
>Esta capacidad está en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

Use `executionMetadata` para capturar y almacenar pares de clave-valor personalizados de forma dinámica en el contexto de ejecución de mensajes.

Con esta función, puede anexar información contextual a cualquier acción nativa desde sus campañas o recorridos. Utilícelo para exportar datos contextuales de envío en tiempo real a sistemas externos para varios fines, como seguimiento, análisis, personalización y procesamiento descendente.

>[!NOTE]
>
>Las acciones personalizadas no admiten la función `executionMetadata`.

Por ejemplo, puede usar el asistente `executionMetadata` para anexar un identificador específico a cada envío enviado a cada perfil. Esta información se genera durante el tiempo de ejecución y los metadatos de ejecución enriquecidos se pueden exportar para la reconciliación de flujo descendente con una plataforma de informes externa.

+++Sintaxis

```
{{executionMetadata key="your_key" value="your_value"}}
```

En esta sintaxis, `key` hace referencia al nombre de los metadatos y `value` son los metadatos que se van a conservar.

**Funcionamiento**

Seleccione cualquier elemento del contenido del canal dentro de una campaña o un recorrido y, con el editor de personalización, agregue el asistente de `executionMetadata` a este elemento.

>[!NOTE]
>
>La función `executionMetadata` no está visible cuando se muestra el contenido en sí.

En tiempo de ejecución, el valor de los metadatos se agrega al **[!UICONTROL Conjunto de datos de evento de comentarios de mensajes]** existente con la siguiente adición de esquema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>Hay un límite superior de 2 kb en los pares de valor clave por acción. Si se supera el límite de 2 KB, el mensaje se envía, pero cualquiera de los pares de valor clave se puede truncar.

**Ejemplo**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

En este ejemplo, suponiendo `profile.person.name.firstName` = &quot;Alex&quot;, la entidad resultante es:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## Funciones de asignación {#maps}

Utilice funciones de asignación en la personalización para facilitar la interacción con los mapas.

### get {#get}

Utilice la función `get` para recuperar el valor de un mapa para una clave determinada.

+++Sintaxis

```sql
{%= get(map, string) %}
```

**Ejemplo**

La siguiente operación obtiene el valor del mapa de identidad para la clave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### teclas {#keys}

Utilice la función `keys` para recuperar todas las claves de un mapa determinado.

+++Sintaxis

```sql
{%= keys(map) %}
```

**Ejemplo**

La siguiente operación recupera todas las claves del mapa `identityMap`.

```sql
{%= keys(identityMap) %}
```

+++

### values {#values}

La función `values` se usa para recuperar todos los valores de un mapa determinado.

+++Sintaxis

```sql
{%= values(map) %}
```

**Ejemplo**

La siguiente operación recupera todos los valores del mapa `identityMap`.

```sql
{%= values(identityMap) %}
```

+++

## Funciones matemáticas {#math}

Aprenda a utilizar las funciones matemáticas en el editor de personalización.

### absoluto {#absolute}

Utilice la función `absolute` para convertir un número en su valor absoluto.

+++Sintaxis

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

Utilice la función `formatNumber` para dar formato a cualquier número en su representación con distinción de idioma.

Acepta un número y una cadena que representa la configuración regional y devuelve una cadena con formato del número de la configuración regional deseada.

+++Sintaxis

```sql
{%= formatNumber(number/double,string) %}: string
```

Puede usar formato y configuraciones regionales válidas, tal como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Configuraciones regionales compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Ejemplo**

Esta consulta devuelve una cadena con formato en árabe correspondiente a 123456,789 como número de entrada.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

Utilice la función `random` para devolver un valor aleatorio entre 0 y 1.

+++Sintaxis

```sql
{%= random() %}: double
```

+++

### roundDown {#round-down}

Utilice la función `roundDown` para redondear un número hacia abajo.

+++Sintaxis

```sql
{%= roundDown(double) %}: double
```

+++

### roundUp {#round-up}

Utilice la función `roundUp` para redondear un número al alza.

+++Sintaxis

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

La función `toHexString` convierte cualquier número en su cadena hexadecimal.

+++Sintaxis

```sql
{%= toHexString(number) %}: string
```

**Ejemplo**

Esta consulta devuelve el valor hexadecimal de 158 como 9e.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

Utilice la función `toInt` para convertir tipos (número, doble, entero, largo, flotante, corto, byte, booleano, cadena) en un entero.

+++Sintaxis

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Ejemplo**

Esta consulta devuelve el valor entero de 42,6 como 42.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

Utilice la función `toPercentage` para convertir un número en porcentaje.

+++Sintaxis

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

Utilice la función `toPrecision` para convertir un número en una precisión requerida.

+++Sintaxis

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

La función `toString` convierte cualquier número en su representación de cadena.

+++Sintaxis

```sql
{%= toString(string) %}: string
```

**Ejemplo**

Esta consulta devuelve `"12"`.

```sql
{%= toString(12) %} 
```

+++

## Funciones de objeto {#objects}

Funciones de objeto para consultar propiedades o atributos de objeto.

### isNull {#isNull}

La función `isNull` determina si no existe una referencia de objeto.

+++Sintaxis

```sql
{%= isNull(object) %}
```

**Ejemplo**

La siguiente operación comprueba si la dirección postal de la persona no existe.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

La función `isNotNull` determina si existe una referencia a un objeto.

+++Sintaxis

```sql
{%= isNotNull(object) %}
```

**Ejemplo**

La siguiente operación comprueba si existe la dirección particular de la persona.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## Funciones de cadena {#string-functions}

Aprenda a utilizar las funciones de cadena en el editor de personalización.

### camelCase {#camelCase}

La función `camelCase` pone en mayúscula la primera letra de cada palabra de una cadena.

+++Sintaxis

```sql
{%= camelCase(string)%}
```

**Ejemplo**

La siguiente función pone en mayúscula la primera letra de una palabra en la dirección de la calle del perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

La función `charCodeAt` devuelve el valor ASCII de un carácter, como la función `charCodeAt` de JavaScript. Toma una cadena y un entero (que define la posición de un carácter) como argumentos de entrada y devuelve su valor ASCII correspondiente.

+++Sintaxis

```sql
{%= charCodeAt(string,int) %}: int
```

**Ejemplo**

La siguiente función devuelve el valor ASCII de `o` (111).

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concatena {#concate}

La función `concat` combina dos cadenas en una.

+++Sintaxis

```sql
{%= concat(string,string) %}
```

**Ejemplo**

La siguiente función combina ciudad y país de perfil en una sola cadena.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### contiene {#contains}

Utilice la función `contains` para determinar si una cadena contiene una subcadena especificada.

+++Sintaxis

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `STRING_1` | Cadena en la que se realizará la comprobación. |
| `STRING_2` | Cadena que se busca dentro de la primera cadena. |
| `CASE_SENSITIVE` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplos**

* La siguiente función comprueba si el nombre del perfil contiene la letra A (en mayúsculas o minúsculas). Si el perfil lo hace, devuelve `true`. Si no, devuelve `false`.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona contiene la cadena `2010@gm`.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContain {#doesNotContain}

Utilice la función `doesNotContain` para determinar si una cadena no contiene una subcadena especificada.

+++Sintaxis

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `STRING_1` | Cadena en la que se realizará la comprobación. |
| `STRING_2` | Cadena que se busca dentro de la primera cadena. |
| `CASE_SENSITIVE` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no contiene la cadena `2010@gm`.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

Utilice la función `doesNotEndWith` para determinar si una cadena no termina con una subcadena especificada.

+++Sintaxis

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no termina con `.com`.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

Utilice la función `doesNotStartWith` para determinar si una cadena no comienza con una subcadena especificada.

+++Sintaxis

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona no comienza con `Joe`.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

Utilice la función `encode64` para codificar una cadena con el fin de conservar la información personal (PI), como para incluirla en una dirección URL.

+++Sintaxis

```sql
{%= encode64(string) %}
```

+++

### endsWith {#endsWith}

Utilice la función `endsWith` para determinar si una cadena termina con una subcadena especificada.

+++Sintaxis

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona termina con `.com`.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### igual a {#equals}

Utilice la función `equals` para determinar si una cadena es igual a la cadena especificada, con distinción entre mayúsculas y minúsculas.

+++Sintaxis

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona es `John`.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### igual a IgnoreCase {#equalsIgnoreCase}

Utilice la función `equalsIgnoreCase` para determinar si una cadena es igual a la cadena especificada, sin distinción de mayúsculas y minúsculas.

+++Sintaxis

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, sin distinción de mayúsculas y minúsculas, si el nombre de la persona es `John`.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

Utilice la función `extractEmailDomain` para extraer el dominio de una dirección de correo electrónico.

+++Sintaxis

```sql
{%= extractEmailDomain(string) %}
```

**Ejemplo**

La siguiente consulta extrae el dominio de correo electrónico de la dirección de correo electrónico personal.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

Utilice la función `formatCurrency` para convertir cualquier número en su correspondiente representación de moneda con distinción de idioma, según la configuración regional pasada como cadena en el segundo argumento.

+++Sintaxis

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Ejemplo**

Esta consulta devuelve 56 £

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

Utilice la función `getUrlHost` para recuperar el nombre de host de una dirección URL.

+++Sintaxis

```sql
{%= getUrlHost(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Devuelve &quot;www.myurl.com&quot;

+++

### getUrlPath {#get-url-path}

Utilice la función `getUrlPath` para recuperar la ruta de acceso después del nombre de dominio de una dirección URL.

+++Sintaxis

```sql
{%= getUrlPath(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Devuelve &quot;/contact.html&quot;

+++

### getUrlProtocol {#get-url-protocol}

Utilice la función `getUrlProtocol` para recuperar el protocolo de una dirección URL.

+++Sintaxis

```sql
{%= getUrlProtocol(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Devuelve &quot;http&quot;

+++

### indexOf {#index-of}

Utilice la función `indexOf` para devolver la posición (en el primer argumento) de la primera aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia.

+++Sintaxis

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | La cadena que se busca en el primer parámetro |

**Ejemplo**

```sql
{%= indexOf("hello world","world" ) %}
```

Devuelve 6.

+++

### isEmpty {#isEmpty}

Utilice la función `isEmpty` para determinar si una cadena está vacía.

+++Sintaxis

```sql
{%= isEmpty(string) %}
```

**Ejemplo**

La siguiente función devuelve &quot;true&quot; si el número de teléfono móvil del perfil está vacío. De lo contrario, devuelve `false`.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

Utilice la función `isNotEmpty` para determinar si una cadena no está vacía.

+++Sintaxis

```sql
{= isNotEmpty(string) %}: boolean
```

**Ejemplo**

La siguiente función devuelve &quot;true&quot; si el número de teléfono móvil del perfil no está vacío. De lo contrario, devuelve `false`.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

Utilice la función `lastIndexOf` para devolver la posición (en el primer argumento) de la última aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia.

+++Sintaxis

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | La cadena que se busca en el primer parámetro |

**Ejemplo**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Devuelve 7.

+++

### leftTrim {#leftTrim}

Utilice la función `leftTrim` para eliminar espacios en blanco del principio de una cadena.

+++Sintaxis

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

Utilice la función `length` para obtener el número de caracteres de una cadena o expresión.

+++Sintaxis

```sql
{%= length(string) %}
```

**Ejemplo**

La siguiente función devuelve la longitud del nombre de ciudad del perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### gustar {#like}

Utilice la función `like` para determinar si una cadena coincide con un patrón especificado.

+++Sintaxis

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | La expresión que debe coincidir con la primera cadena. Existen dos caracteres especiales admitidos para crear una expresión: `%` y `_`. <ul><li>`%` se usa para representar cero o más caracteres.</li><li>`_` se usa para representar exactamente un carácter.</li></ul> |

**Ejemplo**

La siguiente consulta recupera todas las ciudades en las que residen los perfiles que contienen el patrón `es`.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### lowerCase {#lower}

Utilice la función `lowerCase` para convertir una cadena en letras minúsculas.

+++Sintaxis

```sql
{%= lowerCase(string) %}
```

**Ejemplo**

Esta función convierte el nombre del perfil en letras minúsculas.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### matches {#matches}

Utilice la función `matches` para determinar si una cadena coincide con una expresión regular específica. Para obtener más información sobre patrones coincidentes en expresiones regulares, consulte [la documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

+++Sintaxis

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Ejemplo**

La siguiente consulta determina, sin distinción de mayúsculas y minúsculas, si el nombre de la persona comienza por `John`.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### enmascarar {#mask}

Utilice la función `mask` para reemplazar una parte de una cadena con caracteres &quot;X&quot;.

+++Sintaxis

```sql
{%= mask(string,integer,integer) %}
```

**Ejemplo**

La siguiente consulta reemplaza la cadena &quot;123456789&quot; por los caracteres &quot;X&quot;, excepto para los dos primeros y los últimos caracteres.

```sql
{%= mask("123456789",1,2) %}
```

La consulta devuelve `1XXXXXX89`.

+++

### md5 {#md5}

Utilice la función `md5` para calcular y devolver el hash md5 de una cadena.

+++Sintaxis

```sql
{%= md5(string) %}: string
```

**Ejemplo**

```sql
{%= md5("hello world") %}
```

Devuelve &quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot;

+++

### notEqualTo {#notEqualTo}

Utilice la función `notEqualTo` para determinar si una cadena no es igual a la cadena especificada.

+++Sintaxis

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona no es `John`.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

Utilice la función `notEqualWithIgnoreCase` para comparar dos cadenas ignorando mayúsculas y minúsculas.

+++Sintaxis

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina si el nombre de la persona no es `john`, sin distinción de mayúsculas y minúsculas.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### regexGroup {#regexGroup}

Utilice la función `regexGroup` para extraer información específica, basada en la expresión regular proporcionada.

+++Sintaxis

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING}` | Cadena en la que se realizará la comprobación. |
| `{EXPRESSION}` | La expresión regular que debe coincidir con la primera cadena. |
| `{GROUP}` | Grupo de expresiones con el que debe coincidir. |

**Ejemplo**

La siguiente consulta extrae el nombre de dominio de una dirección de correo electrónico.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### replace {#replace}

Utilice la función `replace` para reemplazar una subcadena determinada de una cadena por otra subcadena.

+++Sintaxis

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se debe reemplazar la subcadena. |
| `{STRING_2}` | La subcadena que se va a reemplazar. |
| `{STRING_3}` | La subcadena de reemplazo. |

**Ejemplo**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Devuelve `Hello Mark, here is your monthly newsletter!`

+++

### replaceAll {#replaceAll}

Utilice la función `replaceAll` para reemplazar todas las subcadenas de un texto que coincida con la expresión regex con la cadena de reemplazo literal especificada. Regex tiene un control especial de `\` y `+`, y todas las expresiones regex siguen la estrategia de escape de PQL. El reemplazo continúa desde el principio de la cadena hasta el final, por ejemplo, reemplazar `aa` por `b` en la cadena `aaa` da como resultado `ba` en lugar de `ab`.

+++Sintaxis

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Cuando la expresión tomada como segundo argumento sea un carácter regex especial, utilice una doble barra invertida (`//`).  Los caracteres regex especiales son: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Obtenga más información en [Documentación de Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

+++

### rightTrim {#rightTrim}

La función `rightTrim` elimina los espacios en blanco del final de una cadena.

+++Sintaxis

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

La función `sha256` calcula y devuelve el hash sha256 de una cadena.

+++Sintaxis

```sql
{%= sha256(string) %} : string
```

**Ejemplo**

```sql
{%= sha256("Eliechxh")%}
```

Devuelve `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

+++

### split {#split}

Utilice la función `split` para dividir una cadena entre un carácter determinado.

+++Sintaxis

```sql
{%= split(string,string) %}
```

+++

### startsWith {#startsWith}

Utilice la función `startsWith` para determinar si una cadena empieza con una subcadena especificada.

+++Sintaxis

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona comienza por `Joe`.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

La función `stringToDate` convierte un valor de cadena en un valor de fecha y hora. Se necesitan dos argumentos: la representación de cadena de una fecha y hora y la representación de cadena del formateador.

+++Sintaxis

```sql
{= stringToDate("date-time value","formatter" %}
```

**Ejemplo**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### cadena_a_entero {#string-to-integer}

Utilice la función `string_to_integer` para convertir un valor de cadena en un valor entero.

+++Sintaxis

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

Utilice la función `stringToNumber` para convertir una cadena en número. Devuelve la misma cadena como salida para la entrada no válida.

+++Sintaxis

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

Utilice la función `substr` para devolver la subcadena de la expresión de cadena entre el índice inicial y el índice final.

+++Sintaxis

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

Utilice la función `titleCase` para poner en mayúscula las primeras letras de cada palabra de una cadena.

+++Sintaxis

```sql
{%= titleCase(string) %}
```

**Ejemplo**

Si la persona vive en Washington high street, esta función devuelve `Washington High Street`.

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

Utilice la función `toBool` para convertir un valor de argumento en un valor booleano, según su tipo.

+++Sintaxis

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

Utilice la función `toDateTime` para convertir la cadena a fecha. Devuelve la fecha epoch como salida para una entrada no válida.

+++Sintaxis

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

Utilice la función `toDateTimeOnly` para convertir un valor de argumento en un valor de solo fecha y hora. Devuelve la fecha epoch como salida para una entrada no válida. Esta función acepta tipos de campo de cadena, fecha, longitud y entero.

+++Sintaxis

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trim {#trim}

La función `trim` elimina todos los espacios en blanco del principio y al final de una cadena.

+++Sintaxis

```sql
{%= trim(string) %}
```

+++

### upperCase {#upper}

La función `upperCase` convierte una cadena en letras mayúsculas.

+++Sintaxis

```sql
{%= upperCase(string) %}
```

**Ejemplo**

Esta función convierte los apellidos del perfil en letras mayúsculas.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

Utilice la función `urlDecode` para descodificar una cadena con codificación URL.

+++Sintaxis

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

Utilice la función `urlEncode` para codificar una cadena como dirección URL.

+++Sintaxis

```sql
{%= urlEncode(string) %}: string
```

+++
