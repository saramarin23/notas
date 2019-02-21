# notas
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
<pre><code>myVar = myVar + 5; es igual a myVar=+5;</pre></code>
Lo mismo sucede con la multiplicación <b>*=</b> y la división <b>/=</b>:
<pre><code>myVar /= 2;</pre></code>

Para definir caracteres (<i>strings</i>) se debe comenzar y terminar con comillas simples o dobles. Cuando introducimos comillas en strings debemos usar <b> \ </b>. Ejemplo:
<pre><code>var myStr = "I am a \"double quoted\" string inside \"double quotes\"."</pre></code>

Podemos concatenar strings con <b>+</b>: "Hello " + "World". Igualmente sería con +=. Ejemplo:
<pre><code>var myStr = "This is the first sentence. ";
myStr += "This is the second sentence.";</pre></code>
