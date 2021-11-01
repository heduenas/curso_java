# Ciclos

Los ciclos son una herramienta que permite a los programadores hacer tareas repetitivas con el mínimo esfuerzo.
Por ejemplo, si queremos un programa que cuente de 1 hasta 10 podemos hacer lo siguiente:

<!---
TODO(hopkins0): Create execution and add a link to example.
--->

```Java
class Count {
    public static void main(String[] args) {
        System.out.println("1");
        System.out.println("2");
        System.out.println("3");
        System.out.println("4");
        System.out.println("5");
        System.out.println("6");
        System.out.println("7");
        System.out.println("8");
        System.out.println("9");
        System.out.println("10");
    }
}
```

La tarea será completada como se espera, los números del 1 al 10 serán imprimidos. Sin embargo, la solución tiene algunos problemas:

*   **Flexibility**: ¿Qué pasa si queremos cambiar el número de inicio o el número donde terminar? Tendríamos que agregar, remover y modificar las líneas de código. Esto lo tendríamos que hacer cada vez que sea necesario cambiar los límites.

*  **Escalabilidad**: Imprimir 10 números es trivial, pero ¿qué pasaría si queremos 100 o 1000 repeticiones? El número de líneas de código crecerían conforme más repeticiones se necesiten.

*  **Mantenimiento**: Mientras más líneas se tengan que cambiar, es más probable que algún error ocurra.

*  **Caracteristicas**: La salida siempre es la misma y no cambia en cada ejecución.

Mediante el uso de ciclos, podemos resolver todos los problemas antes mencionados. Por ejemplo, 

<!---
TODO(hopkins0): Create execution and add link to example.
-->

```Java
class Loop {
    public static void main(String[] args) {
        int i;
        for (i = 1; i <= 10; i++) {
            System.out.println(i + " ");
        }
    }
}
```

Si corremos el programa, este dará el mismo resultado pero con una menor cantidad de código. En vez de tener diez líneas de código distintas, estas se redujeron a sólo cuatro.
Además, podemos cambiar donde iniciar y donde terminar de manera sencilla.
Por ejemplo, reemplazar el `1` por un `3` y reemplazar el `10` por un `20` . De esta forma, nuestra secuencia irá del 3 hasta el 20 con un par de simples cambios.

## Mientras que (While)

Los ciclos `while` son uno de las repeticiones más sencillas. Este ciclo se repetirá mientras la condición que se especifique sea verdadera. Su estructura es la siguiente:

```
while (expresion booleana) {

    acción_1
    acción_2
    ...
    acción_n

} 
```

La expresión booleana es revisada antes de cada iteración. Sí la condición es `falsa` , el ciclo no se ejecutará. En el siguiente ejemplo, se usa el ciclo while para obtener el entero más pequeño que su cuadrado sea mayor que 200.

<!---
TODO(hopkins0): Create execution and add link to example.
--->

```Java
int cuadradoMayorQue200 = 0;

while (cuadradoMayorQue200 * cuadradoMayorQue200 < 200) {
  cuadradoMayorQue200 = cuadradoMayorQue200 + 1;
}

```

Cuidado; Sí la condición nunca se vuelve verdadera, por ejemplo si se usa la constante `true` (palabra), el ciclo se conoce como ciclo infinito. Ese ciclo se ejecuta de manera indefinida a menos que algo lo rompa.
Los ciclos infinitos pueden ser usados para realizar tareas que sean repetidas sin detenerse como actualizar imágenes en la pantalla.

## Mientras que... al menos una vez (do... while)

El ciclo `do - while` funciona de una manera similar a el ciclo `while` , excepto que la condición es evaluada al final, después que las instrucciones fueron ejecutadas. Su estructura es la siguiente:

```
do {

    instrucción_1
    instrucción_2
    ...
    instrucción_n

} while (expresión booleana); 
```

Usando el ejemplo anterior, se vería de la siguiente forma. La diferencia radica en que primero se incrementa el valor y luego se evaluaría.

<!---
TODO(hopkins0): Create execution and add link to example.
-->

```Java
int cuadradoMayorQue200 = 0;
do {
	cuadradoMayorQue200 = cuadradoMayorQue200 + 1;
}
while (cuadradoMayorQue200 * cuadradoMayorQue200 < 200);
```
