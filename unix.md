En la terminal, si vemos <b>$</b> nos indica que está listo para aceptar comandos.
Cuando escribimos <b>ls</b>, la línea de comando mira la carpeta en la que estás y "hace una lista" de los archivos y directorios (carpetas) dentro de ella.
<b>pwd</b> significa <i>"print working directory"</i> y muestra el nombre del directorio en el que te encuentras.
<b>cd</b> significa <i>"change directory"</i> tal y como si seleccionaras una carpeta en tu OS.
The cd command takes a directory name as an argument, and switches into that directory.
Para volver a la carpeta superior, después de cd añadimos <b>..</b>
<b>mkdir</b> significa <i>"make directory"</i> crea un directorio en el directorio actual.
<b>touch</b> crea un archivo dentro del directorio actual.

Si a <b>ls</b> añadimos <b>-a</b>, nos muestra también los archivos ocultos, que no se muestran solo con ls. A -a se le denomina <i>opción</i>. Las opciones modifican el comportamiento de los comandos. <b>-l</b> muestra todo el contenido de un directorio en formato largo. <b>-t</b> ordena archivos por el tiempo que fueron modificados por última vez.
Ejemplo de <b>ls -l</b>:
<pre><code>drwxr-xr-x   5 saramarin  staff    160 12 oct 17:31 Applications
drwxr-xr-x  16 saramarin  staff    512  6 nov 11:44 Biblioteca de calibre</pre></code>

ls -alt lists all contents, including hidden files and directories, in long format, ordered by the date and time they were last modified.

<b>cp</b> copia archivos o directorios. Después del archivo fuente (primer argumento) que queremos copiar indicamos el directorio (segundo argumento) en el que lo queremos pegar. Ejemplo:
<pre><code>cp biopic/cleopatra.txt historical/</pre></code>
*Se pueden copiar varios elementos a la vez si están situados en el mismo directorio.
Usando el caracter * seleccionamos grupos de archivos. * Selecciona todos los archivos en un directorio. A estos caracteres especiales se les llama <i>wildcards</i>.
