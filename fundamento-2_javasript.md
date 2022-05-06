https://javascript.info/types#string

# Tipos de datos

Hay ocho tipos de datos basicos en javascript.

ejemplo una variable puede una cadena y luego un numero

```javascript
// no hay error
let message = "hello";
message = 123456;
```

# Numero

```javascript
let n = 123;
n = 12.345;
```

el tipo de numero repreenta numeros y de tipo flotante

hay numero iregulares llamados **infinity, -infinity y NaN.**

**Infinity** representa el infinito matematico y es un valor espaecial que es mayor a cualquier numero se puede obtener como resultado de la division por cero.

```javascript
alert(1/0;)//infinity
```

o simplemente directamente

```javascript
alert(infinity); //infinity
```

**NaN** Representa un error de calculos.

```javascript
alert("not a number" / 2); // NaN , such division.
```

# cadenas \_\_ Las bases

las cadenas se tratan como los numeros,
pero cuando profundisas empiezas a ver algo notable.

# Creando una cadena

```javascript
let string = "La revolucion no sera televisada";
```

al igual que con los numeros debemos declarar una variable la unica diferencia es que debemos colocarle las comillas,
**si no agrega un error**

```javascript
var malString = Esto es una prueba;
var malString = 'Esto es una prueba;
var malString = Esto es una prueba';

```

# Comillas Simples vs. comillas dobles

en Javascript puedes utilizar comillas simples y dobles pero **es menos confuso usar una de las dos** lo que no podemos hacer es usar las dos juntas en una declaracion.

> var simp = 'Comillas simples.';

> var dobl = "Comillas dobles.";

> simp;
> dobl;

**\* si se mezcla ('...... ") te dara un error.**

Este es otro tipo de cita que es correcto usar.

> var sglDbl = 'Would you eat a "fish supper"?';

> var dblSgl = "I'm feeling blue.";

> sglDbl;
> dblSgl;

sin embargo ste causara confucion al navegador por que no sabra donde termina lacadena.

> var bigmouth = 'I've got no right to take my place...';
> /

## Dooleano (tipologico)

El tipo solo tiene valores true y false.

```javascript
let naeFielCheked = true; //yes, ame fie is cheked
let ageFieldCheked = false; // no, age field is not cheked
```

Los valores booleanos también vienen como resultado de comparaciones:

```javascript
let isGreater = 4 > 1;
alert(isGreater); //tru (the comparison result is "yes)
```

## Valor (null)

no pertenece aninguno de los mencionanos anteriormente es propio que contiene solo el null.

## El valor "Indefinido"

es especial y es propio
significado es que "no se asigna valor"
si se declara una variable, pero no se asigna valor, entonces el valor es undefinided:

# Objetos y Símbolos

el "object" es tipo especial.

todos los demas se denominan primitivos por que sus valores pueden contener solo una cosa, ya sea una cadena o un numero.

el "symbol "se utiliza para crear identificadores.

```javascript
typeof undefined; // "undefined"

typeof 0; // "number"

typeof 10n; // "bigint"

typeof true; // "boolean"

typeof "foo"; // "string"

typeof Symbol("id"); // "symbol"

typeof Math; // "object"  (1)

typeof null; // "object"  (2)

typeof alert; // "function"  (3)
```

Las últimas tres líneas pueden necesitar una explicación adicional:

1. Math es un objeto integrado que proporciona operaciones matemáticas. Lo aprenderemos en el capítulo Números . Aquí, sirve solo como un ejemplo de un objeto.

2. El resultado de typeof nulles "object". Ese es un error reconocido oficialmente en typeof, que proviene de los primeros días de JavaScript y se mantiene por compatibilidad. Definitivamente, nullno es un objeto. Es un valor especial con un tipo separado propio. El comportamiento de typeofes incorrecto aquí.

3. El resultado de typeof alertes "function", porque alertes una función. Estudiaremos las funciones en los próximos capítulos donde también veremos que no hay un tipo especial de "función" en JavaScript. Las funciones pertenecen al tipo de objeto. Pero typeoflos trata de manera diferente, regresando "function". Eso también viene de los primeros días de JavaScript. Técnicamente, tal comportamiento no es correcto, pero puede ser conveniente en la práctica.

> la typeof(x)sintaxis
> También puede encontrar otra sintaxis: typeof(x). Es lo mismo que typeof x.

> Para decirlo claramente: typeofes un operador, no una función. Los paréntesis aquí no son parte de typeof. Es el tipo de paréntesis que se usa para la agrupación matemática.

> Por lo general, estos paréntesis contienen una expresión matemática, como (2 + 2), pero aquí solo contienen un argumento (x). Sintácticamente, permiten evitar un espacio entre el typeofoperador y su argumento, y a algunas personas les gusta.

> Algunas personas prefieren typeof(x), aunque la typeof xsintaxis es mucho más común.

## Metodos Y propiedades de string

https://www.w3schools.com/js/js_string_methods.asp

Los valores primitivos, como "John Doe", no pueden tener propiedades ni métodos (porque no son objetos).

Pero con JavaScript, los métodos y propiedades también están disponibles para valores primitivos, porque JavaScript trata los valores primitivos como objetos cuando ejecuta métodos y propiedades.

## Longitud de string

**length** esta propiedad devuelve la longitud de cualquier cadena.

## Extracción de partes de string

Hay tres metodos para la extraccion de cadenas

- **slice(start, end)**
- **substring(start, end)**
- **substr(start, length)**

## slice

extrae una parte de la cadena segun su posicion el metodo toma dos parametros la inicial y la final (la final no se incluye o no se visualiza) **slice (0,0)** este ejemplo toma dese la posicion 7 a la 12.

```javascript
let str = "Apple, Banana, Kiwi";
let part = str.slice(7, 13);
```

> # Nota
>
> JavaScript cuenta posiciones desde cero
> La primera posición es 0
> La segunda posición es 1.

Si un parámetro es negativo, la posición se cuenta desde el final de la cadena.

Este ejemplo corta una porción de una cadena desde la posición -12 a la posición -6:

```javascript
let str = "apple, Banana, Kiwi";
let part = str.slice(-12, -6);
```

https://developer.mozilla.org/es/docs/Learn/JavaScript/First_steps/Strings

# Bases de las cadenas

```javascript
var string = "La revolución no será televisada.";
string;
```

Al igual que los numeros decalramos una variable , iniciandola con el valort de una cadena.

## error de cadenas ( ej. "missing ; before statement").

```javascript
var malString = Esto es una prueba;
var malString = 'Esto es una prueba;
var malString = Esto es una prueba';
```

es por que al no completar las comillas el navegador o consola no sabe donde empieza o donde termina.

> en **string** se pueden usar una comilla o de dos comillas pero no las dos juntas.

# concatenandos Cadenas

1. Concatenar en la programacion es unir palabras o numeros mediante el signo de mas **(+)**
   > ej:

```javascript
var one = "Hello, ";
var two = "how are you?";
var joined = one + two;
joined;
```

> lo pudes unir cuantas veces decees siempre y cuando coloques el signo de mas.

> ### Nota:
>
> Cuando ingresas una string real en tu código
>
> entre comillas simples o dobles, se llama string literal.

# Concatenacion en contexto

```html
<button>Press me</button>
```

```javascript
var buttton = document.querySelector("button");

button.onclick = function () {
  var name = prompt("what is your name");
  alert("hello" + name + ", nice to see you");
};
```

> Aquí estamos usando una función Window.prompt()
> en la línea 4, que le pide al usuario la respuesta a una pregunta,
> através de un cuadro emergente (también llamado popup) y luego,
> almacenará el dato dentro de una variable dada — en este caso llamada
> name (nombre). Luego, en la línea 5, usamos una función Window.alert()
>
> para mostrar otra ventana emergente que contiene una cadena que hemos unido de la concatenación de dos string literales y la variable name (nombre).

# Numeros versus cadenas

1. Los string y los numero se pueden concatenar pudiera dar error pero no es asi,

```javascript
"font" + 242;
```

> esto saldria como string en la consola

2. si tenemos una variable numerica que queremos cambiar a string o viceversa

- el bojeto **number** convertira cualquier cosa en numero.

```javascript
var mySatring = "123";
var myNum = Number(myString);
typeof myNum;
```

- **toString()** es el equivalente en una string.

```javascript
var myNum = 123;
var myString = myNum.toString();
typeof myString;
```
