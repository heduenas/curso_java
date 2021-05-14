# ¡Hola Mundo! #

El primer programa que la mayoría de los programadores escriben es el clásico "Hola Mundo". El propósito de este programa es mostrar el texto "Hola Mundo" al usuario. [Ejemplos de programas en diferentes lenguajes de programación](https://excelwithbusiness.com/blog/say-hello-world-in-28-different-programming-languages/).

    public class Main {
      public static void main(String[] args) {
        System.out.println("¡Hola Mundo!");
      }
    }

[Pruébalo en línea!](https://tio.run/##y0osS9TNL0jNy0rJ/v@/oDQpJzNZITknsbhYwTcxM0@hmosTKlhcklgCpMryM1MUcoFSGsElRZl56dGxColF6cWaIJWcwZXFJam5evmlJXoFQMmSnDwNpUMLPfJzEhV8S/NS8hWVNK25OGu5av//BwA  "C++ (gcc) – Try It Online")

## Explicación del Código ##

Antes de entrar en detalles, es útil pensar simultáneamente en un programa en términos de su *estructura* y también de su *significado*.

Un programa de Java está estructurado de forma específica y particular. Java es un lenguaje y por ende tiene una *gramática* similar a un lenguaje hablado, como el español. La gramática de los lenguajes de computación es mucho más simple que la de los lenguajes hablados, pero tiene reglas más estrictas. Al aplicar esta gramática al lenguaje, la computadora puede entender el programa y lo que se supone que debe de hacer.

Para tener un mejor entendimiento de la estructura y el significado del clásico "Hola Mundo", veamos un análisis línea por línea del programa.

## Una Explicación Detallada del Código ##

### La Línea `public class Main {` ###

In nuestro código de Hola Mundo, `public class Main` es la declaración de la clase. Consiste en dos palabras clave, `public` y `class` seguido del identificador `Main`.

Esto quiere decir que estamos definiendo una clase llamada `Main`. Otras clases se pueden referir a esta clase por ese nombre. La palabra clave `public` es un modificador de acceso, la cual declara que esta clase y sus miembros pueden ser accesados desde otras clases. La palabra clave `class`, obviamente identifica esta declaracion como una clase. Java también permite la declaracion de interfaces y anotaciones, las cuales aprenderemos más adelante en este curso.  

### La Línea `public static void main(String[] args)`

El punto de partida de todos los programas de Java es la función `main()`. El sistema operativo llama a esta función cuando la computadora ejecuta tu programa. Por ejecución queremos decir: realizar las acciones especificadas por las declaraciones en tu programa.

Podrás notar que en este caso la declaración de la función `main()` está acompañada de las palabras clave `public`, `static` y `void`. `public` igual que en línea anterior significa que está función puede ser llamada desde otras clases. `static` significa que está función puede ser llamada sin necesidad de crear una `instancia` de la clase, más tarde aprenderemos qué es eso y para que sirve. `void` es el tipo de valor de retorno de la función `main()`, en este caso nuestra función no necesita retornar nada y por eso ponemos `void`, pero las funciones pueden regresar valores númericos, textos, etc. 

### La Línea `System.out.println("¡Hola Mundo!");` ###

En esta lína *hacemos una llamada* a la función `println` la cual *vive* dentro del objeto `out`, el cual a su vez vive dentro de la clase `System`, y le pasamos la cadena de texto `¡Hola Mundo!` como *paramétro*. Esa llamada hace que se imprima el texto "¡Hola Mundo!" en la consola.
