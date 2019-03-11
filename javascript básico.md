# intro
Para hacer comentarios en JavaScript se puede hacer de dos maneras:
<pre><code> //comentario 1 </pre></code>
<pre></code> /* comentario 2 */ </pre></code>

Le decimos a JavaScript que cree o <i>declare</i> una <i>variable</i> usando la palabra <b>var</b> delante de ésta. Ejemplo:
<pre><code>var myName;</pre></code>
Podemos almacenar un valor en una variable utilizando el caracter <b>=</b> :
<pre><code> var a = 5; </pre></code>

Cuando se realiza una operación de dos variables no declaradas, el resulto será <b>NaN</b> (Not a number).
En JavaScript todos los nombres de funciones y variables son <i>case sensitive</i>

Podemos hacer operaciones matemáticas como:
<pre><code> var product = 8 * 10;</pre></code>

Podemos añadir un número a la variable simplemente escribiendo <b>++</b>. Así, <i>i++;</i> sería igual a <i>i = i+1;</i>.
Lo mismo podemos hacer para restar un número: <b>--</b>. 

Operadores de asignación: Podemos usar sumas (o restas) para modificar los contenidos de la variable a través del operador <b>+=</b> (o <b>-=</b>). Ej:
<pre><code>myVar = myVar + 5; es igual a myVar+=5;</pre></code>
Lo mismo sucede con la multiplicación <b>*=</b> y la división <b>/=</b>:
<pre><code>myVar /= 2;</pre></code>

Para definir caracteres (<i>strings</i>) se debe comenzar y terminar con comillas simples o dobles. Cuando introducimos comillas en strings debemos usar <b> \ </b>. Ejemplo:
<pre><code>var myStr = "I am a \"double quoted\" string inside \"double quotes\"."</pre></code>

Podemos concatenar strings con <b>+</b>: "Hello " + "World". Igualmente sería con +=. Ejemplo:
<pre><code>var myStr = "This is the first sentence. ";
myStr += "This is the second sentence.";</pre></code>
Del mismo modo, podemos añadir una variable en una sentencia:
<pre><code> "My name is " + myName + " and I am fine."</pre></code>

Para saber la longitud de la variable utilizamos <b>.length</b> junto a la variable: <i>myName.length</i>
Para saber el primer caracter de una variable pondremos <b>[0]</b> justo al final de dicha variable <i>myName[0]</i>

En JavaScript los caracteres son inmutables. Para cambiar uno, tendríamos que cambiar toda la variable. Así, no sería válido <i>myName[0] = "P";</i>. Para obtener el último, restaremos 1 a .length: <i>myName[myName.length -1]</i>

Arrays
----

En JavaScript podemos almacenar varios datos en un único lugar. Ejemplo:
<pre><code>var Sandwich = ["peanut butter", "bread", "jelly"];</pre></code>
También se puede crear un array dentro de otro:
<pre><code>var ourArray = [["the universe", 42], ["everything", 101010]];</pre></code>

Se puede añadir datos con el código <b>.push()</b>:
<pre><code>var arr = [1,2,3];
arr.push(4);
// arr is now [1,2,3,4]</pre></code>
Del mismo modo, podemos eliminar el último dato con <b>.pop()</b>:
<pre><code>var threeArr = [1, 4, 6];
var oneDown = threeArr.pop();
console.log(oneDown); // Devuelve 6, lo removido
console.log(threeArr); // Devuelve [1, 4], lo que queda</pre></code>
Si no queremos eliminar el último dato, sino el primero, debemos utilizar <b>.shift</b>:
<pre><code>var myArray = [["John", 23], ["dog", 3]];
var removedFromMyArray = myArray.shift();</pre></code>
Si lo que queremos es añadir un dato al principio del array usaremos <b>.unshift()</b>:
<pre><code>myArray.unshift(["Paul", 35]);</pre></code>

Funciones (I)
---

It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable.
A function can include the return statement but it does not have to. In the case that the function doesn't have a return statement, when you call it, the function processes the inner code but the returned value is undefined.

Comparadores
---
The inequality operator (!=) is the opposite of the equality operator. It means "Not Equal" and returns false where equality would return true and vice versa. Like the equality operator, the inequality operator will convert data types of values while comparing.
The strict inequality operator (!==) is the logical opposite of the strict equality operator. It means "Strictly Not Equal" and returns false where strict equality would return true and vice versa. Strict inequality will not convert data types.


Sometimes you will need to test more than one thing at a time. The logical and operator (&&) returns true if and only if the operands to the left and right of it are true.
The logical or operator (||) returns true if either of the operands is true. Otherwise, it returns false.

Objetos
--

Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called properties.

Objects are useful for storing data in a structured way, and can represent real world objects, like a cat.

Here's a sample cat object:

<pre><code>var cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};</pre></code>

var, let y const
--
Uno de los mayores problemas de usar <code>var</code> es que al declarar las variables, se sobreescriben. Cuando el código se hace más grande, se pueden sobreescribir sin darse cuenta. Ya que esto no muestra error, puede ser difícil dar con ello.
<code>let</code> se introdujo en ES6 para solucionar este problema. So unlike var, when using let, a variable with the same name can only be declared once.
When you declare a variable with the let keyword inside a block, statement, or expression, its scope is limited to that block, statement, or expression.
const has all the awesome features that let has, with the added bonus that variables declared using const are read-only. They are a constant value, which means that once a variable is assigned with const, it cannot be reassigned.
As you can see, trying to reassign a variable declared with const will throw an error. You should always name variables you don't want to reassign using the const keyword. This helps when you accidentally attempt to reassign a variable that is meant to stay constant. A common practice when naming constants is to use all uppercase letters, with words separated by an underscore.
However, it is important to understand that objects (including arrays and functions) assigned to a variable using const are still mutable. Using the const declaration only prevents reassignment of the variable identifier.
