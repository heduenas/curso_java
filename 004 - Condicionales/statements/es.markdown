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
