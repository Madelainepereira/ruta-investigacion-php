- ¿Qué es PHP y cuál es su función principal en el desarrollo web? 

Es un lenguaje de código abierto muy popular especialmente adecuado para el desarrollo web y 
que puede ser incrustado en HTML.

Ejemplo

<!DOCTYPE html>
<html>
<head>
<title>Ejemplo</title>
</head>
<body>

<?php
            echo "¡Hola, soy un script de PHP!";
        ?>

</body>
</html>

PHP está enfocado principalmente a la programación de scripts del lado del servidor, por lo que se puede hacer cualquier cosa que pueda hacer otro programa CGI, como recopilar datos de formularios, generar páginas con contenidos dinámicos, o enviar y recibir cookies.

- ¿Cuáles son las características clave de PHP que lo diferencian de otros lenguajes de
programación?

 Es un código abierto y gratuito. Es un lenguaje orientado a objetos, lo que hace el procesamiento de datos mucho más rápido. Permite la separación de códigos, es decir, es posible manipular datos mientras que otros se encuentran estáticos

 - ¿Cuál es la sintaxis básica de PHP y cuáles son las convenciones de nomenclatura utilizadas?

 1. Un script PHP se puede colocar en cualquier parte del documento.
 2. Un script PHP comienza <?phpy termina con ?>:

<?php
// PHP code goes here
?>
3. La extensión de archivo predeterminada para los archivos PHP es " .php".
4. Un archivo PHP normalmente contiene etiquetas HTML y algún código de secuencias de comandos PHP.
5. las declaraciones de PHP terminan con un punto y coma ( ;).
6. En PHP, las palabras clave (p. ej. if, else, while, echo, etc.), clases, funciones y funciones definidas por el usuario no distinguen entre mayúsculas y minúsculas. Sin embargo; ¡Todos los nombres de variables distinguen entre mayúsculas y minúsculas!

- ¿Cuáles son los tipos de datos admitidos en PHP y cómo se manejan?



- ¿Cuál es la diferencia entre una variable local y una variable global en PHP?

Las variables globales resultan visibles y disponibles para todas las sentencias de un script. Las variables locales sólo resultan visibles y disponibles dentro de la función en la que están definidas.

Alcance de las variables de PHP

En PHP, las variables se pueden declarar en cualquier parte del script.

El alcance de una variable es la parte del script donde se puede hacer referencia/utilizar la variable.

PHP tiene tres ámbitos variables diferentes:

local
global
estático

Alcance Global y Local
Una variable declarada fuera de una función tiene un ALCANCE GLOBAL y solo se puede acceder fuera de una función:

<?php
$x = 5; // global scope

function myTest() {
  // using x inside this function will generate an error
  echo "<p>Variable x inside function is: $x</p>";
}
myTest();

echo "<p>Variable x outside function is: $x</p>";
?>

Una variable declarada dentro de una función tiene un ÁMBITO LOCAL y solo se puede acceder dentro de esa función:

<?php
function myTest() {
  $x = 5; // local scope
  echo "<p>Variable x inside function is: $x</p>";
}
myTest();

// using x outside the function will generate an error
echo "<p>Variable x outside function is: $x</p>";
?>


- ¿Qué son los arrays en PHP y cómo se utilizan para almacenar y manipular datos?

Un array en PHP es en realidad un mapa ordenado. Un mapa es un tipo de datos que asocia valores con claves. Este tipo se optimiza para varios usos diferentes; se puede emplear como un array, lista (vector), tabla asociativa (tabla hash - una implementación de un mapa), diccionario, colección, pila, cola, y posiblemente más. Ya que los valores de un array pueden ser otros arrays, también son posibles árboles y arrays multidimensionales.

- ¿Cómo declarar variables en PHP?

Variables PHP

Una variable puede tener un nombre corto (como x e y) o un nombre más descriptivo (edad, nombre del coche, volumen_total).

Reglas para variables de PHP:

Una variable comienza con el $signo, seguido del nombre de la variable
Un nombre de variable debe comenzar con una letra o el carácter de subrayado
Un nombre de variable no puede comenzar con un número
Un nombre de variable solo puede contener caracteres alfanuméricos y guiones bajos (Az, 0-9 y _)
Los nombres de las variables distinguen entre mayúsculas y minúsculas ( $agey $AGEson dos variables diferentes)

Variables de salida
La echodeclaración de PHP se usa a menudo para enviar datos a la pantalla.

El siguiente ejemplo mostrará cómo generar texto y una variable:

<?php
$txt = "W3Schools.com";
echo "I love $txt!";
?>

- ¿Cómo declarar funciones en PHP?

// Declarar
function nombre_de_funcion(tipo_de_parametro $parametros): tipo_return
{
    ...
    return ...;
}

// Llamar
nombre_de_funcion($parametros);
