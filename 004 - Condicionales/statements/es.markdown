# Bloques condicionales

Los bloques condicionales permiten a los programas tomar distintos caminos dependiendo de
condiciones. Estas permiten al programa realizar una evaluación y entonces determinar la
action a ejecutar basada en el resultado de esta.

## IF (Condicional Si) 

El bloque condicional `if` se ejecuta si la expresión boleana es verdadera. La estructura
de un bloque `if` es la siguiente:

```
if (expresion boleana) {
  acción_1
  acción_2
  ...
  acción_n
}
```

Ejemplo de lo que pasa si la condicional es verdadera y si la condicional es falsa.
[Pruébalo en línea!](https://tio.run/##fY49D4IwEIbn8itOJhgkfiQuqIOTixNuxuGklRRLS2ghaQy/HVt00IQ4Xe7ueZ@8JXY4VzWTJX0MQ93eBM8hF6g1nJBLeAbkc9QGjRud4hQq94oy03BZXK6ATaFjTxIuDTCKFHawSd2eWW1YlajWJLWDjZBReFQCZ2GcBp6/QzTyW1iu3wqAqdCZyUJBxaTSQJmDE28gpP@x7GG1@GfJlHXVrWq8wye@LVOBg2VjVUf0w/AC "Java (OpenJDK 8) – Try It Online")

```java
int edad = 6;
System.out.println("Hola!");

if (edad < 13) {
  System.out.println("Tengo menos de 13.");
}

if (edad > 20) {
  System.out.println("Soy mayor de edad.");
}

System.out.println("Bye!");
```

> Nota: Si sólo una acción será ejecutada en un bloque `if` entonces la acción puede ir
sin las llaves. Por ejemplo,
`if (i ==0) i = 1;` es una sentencia valida en Java.

## IF/ELSE (Condicional Si/De lo contrario)

El bloque `if` puede ser continuado con un `else`, que se ejecutará si la expresión de
la acción `if` es falsa. Su esctuctura es como la siguiente:


```
if (expresion boleana) {
  acción_1
  acción_2
  ...
  acción_n
} else {
  acción_1_else
  acción_2_else
  ...
  acción_n_else
}
```

## IF/ELSE-IF/ELSE(Múltiples  Condicional Si/De lo contrario)

El bloque `else-if` se puede usar cuando múltiples condiciones necesitan ser evaluadas.
El enunciado `else-if` va después  de un bloque `if` pero antes de un bloque `else`. La
esctuctura es como la siguiente:


```
if (expresion boleana 1) {
  acción_1_1
  acción_1_2
  ...
  acción_1_n
} if (expresion boleana 2) {
  acción_2_1
  acción_2_2
  ...
  acción_2_n
} else {
  acción_3_1_else
  acción_3_2_else
  ...
  acción_3_n_else
}
```

Ejemplo:

```java
public class CondicionalPrograma {
    public static void main (String[] args) {
      int a = 5;
      if (a > 0) {
          // como a es mayor que 0, entonces la siguiente acción  se ejecutará.
          System.out.println("a es positivo");
      } else if (a >= 0) {
          // Como el primer if ya fue ejecutado, el if no será evaluado y la siguiente acción 
          // no será ejecutada.
          System.out.println("a es positivo or cero");
      } else {
          // El primer if ya fue ejecutado, entonces  la siguiente acción  no será ejecutada.
          System.out.println("a es negativo");
      }
    }
}
```

> Nota: Recuerda que solo un bloque se ejecutará y será la primera condición que sea verdadera.



## Expresiones condicionales ternarias

Las expresiones condicionales usan los operadores `?:`

```
expresión_boleana ? expresión1 : expressión2
```

Se evalua la expresión_boleana, si es `verdadera` entonces se usará el valor de
`expressión1`, de lo contrario se usará el valor de `expressión2`

Ejemplo:
```java
String respuesta = (a >= 0)? "a es positivo o cero" : "a es negativo";
```

Es código es equivalente al siguiente:

```java
String respuesta;

if (a >= 0) {
  a = "a es positivo o cero";
} else {
  a = "a es negativo";
}
```

## SWITCH (Bloque condicional switch)

La sentencia condicional `switch` es básicamente una versión corta o
simplificada de muchos bloques `if...else`. El bloque `switch` evalua `char`,
`bytes`, `short`, `int`, `enum`*, `String`* y basando en el valor de entrada,
salta a uno de los casos y ejecuta la acción correspondiente hasta llegar a un
comando `break` o el final del bloque. Si el valor no corresponde a unos de los
casos especificados, se ejecturá el caso (opcional) default.

> \* La compatibilidad depende de la versión de Java que se utilice.
La estructura del comando es la siguiente:

```
switch (value_to_evaluate) {
    case value1:
        statement1.1
        ...
        statement1.n
        break;
    case value2:
        statement2.1
        ...
        statement2.n
        break;
    default:
        statementn.1
        ...
        statementn.n
} 
```

Ejemplo:

```java
int i = 3;
switch(i) {
    case 1:
        // i no es igual a 1, entonces la siguiente código no se ejecutará.
        System.out.println("i es igual a 1");
        break;
    case 2:
        // i no es igual a 2, entonces la siguiente código no se ejecutará.
        System.out.println("i es igual a 2");
        break;
    default:
        // i no concuerda con ninguno de los casos hasta este punto, entonces
        // la operación default se ejecutará.
        System.out.println("i es algo que no es 1 o 2");
}
```

Si un caso (`case`) no termina con un comando `break`, entonces el siguiente
caso se revisará; en caso contrario se saltará al final del bloque. 

Revisa los siguientes ejemplos:

```java
int i = -1;
switch(i) {
    case -1:
    case 1:
        // i=-1, como no tiene una comando `break`, caerá en este caso y
        // ejecutará el siguiente código.
        System.out.println("i es 1 o -1");
        break;
    case 0:
        // El comando `break` es usando antes de llegar a este caso, por lo
        // que si i=1 o i=-1 el siguiente código no se ejecutará.
        System.out.println("i es 0");
}
```

```java
String dia = "Lunes";
switch(day) {
    case "Lunes":
        // Como dia == "Lunes", este comando se ejecutará.
        System.out.println("Lunes son lo peor!");
        break;
    case "Martes":
    case "Miercoes":
    case "Jueves":
        System.out.println("Entre semana no está mal.");
        break;
    case "Viernes":
    case "Sabado":
    case "Domingo":
        System.out.println("Fines de semana son lo mejor!");
        break;
    default:
        throw new IllegalArgumentException("Día no válido de la semana:" + dia);
}
```
