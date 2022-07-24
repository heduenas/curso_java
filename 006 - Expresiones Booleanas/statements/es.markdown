# Expresiones Booleanas

Los valores booleanos son valores que se evalúan como verdadero (`true`) o falso
(`false`) y están representados por el tipo de datos `boolean`. Las expresiones
booleanas son muy similares a las expresiones matemáticas, pero en lugar de
utilizar operadores matemáticos como "+" o "-", utiliza operadores comparativos
o booleanos como "==" o "!".

## Operadores comparativos

Java tiene varios operadores que se pueden usar para comparar variables. Por
ejemplo, ¿cómo sabrías si una variable tiene un valor mayor que otra? La
respuesta: use el operador "mayor que".

Aquí hay una lista de los operadores comparativos en Java:

- `>` : Mayor que
- `<` : Menor que
- `>=` : Mayor o igual que
- `<=` : menor o igual que
- `==` : Igual a
- `!=` : No igual a

```Java
int a = 5, b = 3;
System.out.println(a > b); // El valor es verdadero porque a es mayor que b
System.out.println(a == b); // El valor es falso porque a no es igual a b
System.out.println(a != b); // El valor es verdadero porque a no es igual a b
System.out.println(b <= a); // El valor es verdadero porque b es menor que a
```

Los operadores comparativos se pueden usar en cualquier tipo primitivo (excepto
booleano), pero solo los operadores "igual" y "no es igual" funcionan en objetos.
Esto se debe a que los operadores menor que/mayor que no se pueden aplicar a los
objetos, pero los operadores de equivalencia sí.

> Específicamente, los operadores == y != prueban si ambas variables apuntan al
  mismo objeto. Los objetos se tratarán más adelante en el tutorial, en el módulo
  "Clases, objetos y tipos".

## Operadores booleanos

Los operadores booleanos de Java se basan en las operaciones del álgebra booleana.
Los operadores booleanos operan directamente sobre valores booleanos.

Aquí hay una lista de cuatro operadores booleanos comunes en Java:

- `!`: Booleano 'NO' (NOT)
- `&&`: Booleano 'Y' (AND)
- `||`: Booleano inclusive 'O' (OR)
- `^`: XOR booleano exclusivo

El operador booleano NOT ("!") invierte el valor de una expresión booleana. El
operador booleano AND ("&&") dará como resultado verdadero si y solo si los
valores en ambos lados del operador son verdaderos. El operador booleano
inclusivo OR ("||") dará como resultado verdadero si uno o ambos valores a los
lados del operador son verdaderos. El operador booleano XOR exclusivo ("^") dará
como resultado verdadero si uno y solo uno de los valores a los lados del operador
es verdadero.

Para mostrar cómo se utilizan estos operadores, aquí hay un ejemplo:

<!---
TODO(hopkins0): Create execution and add link to example.
-->

```Java
boolean iMTrue = true;
boolean iMTrueToo = true;
boolean iMFalse = false;
boolean iMFalseToo = false;

System.out.println("operador NOT:");
System.out.println(!iMTrue);
System.out.println(!iMFalse);
System.out.println(!(4 < 5));
System.out.println("operador AND:");
System.out.println(iMTrue && iMTrueToo);
System.out.println(iMFalse && iMFalseToo);
System.out.println(iMTrue && iMFalse);
System.out.println(iMTrue && !iMFalse);
System.out.println("operador OR:");
System.out.println(iMTrue || iMTrueToo);
System.out.println(iMFalse || iMFalseToo);
System.out.println(iMTrue || iMFalse);
System.out.println(iMFalse || !iMTrue);
System.out.println("operador XOR:");
System.out.println(iMTrue ^ iMTrueToo);
System.out.println(iMFalse ^ iMFalseToo);
System.out.println(iMTrue ^ iMFalse);
System.out.println(iMFalse ^ !iMTrue);
```

Aquí están las tablas de verdad para los operadores booleanos:

|a | !a |
|--|----|
|true | false |
|false | true |

|a | b | a && b| a \|\| b | a ^ b|
|--|---|-------|--------|------|
|true | true | true |true | false|
|true | false | false | true | true|
|false | true | false | true | true|
|false | false | false | false | false|

En Java, la lógica booleana tiene una propiedad útil llamada cortocircuito. Esto
significa que las expresiones solo se evaluarán en la medida en que sea
necesario. En la expresión (a && b), si a es falso, entonces b no se evaluará
porque la expresión será falsa sin importar nada. Aquí hay un ejemplo que
muestra que la segunda expresión no se verifica automáticamente:

<!---
TODO(hopkins0): Create execution and add link to example.
-->
```Java
System.out.println((4 < 5) || ((10 / 0) == 2));
```

Para deshabilitar esta propiedad, puede usar `&` en lugar de `&&` y `|` en lugar
de `||` pero no es recomendable.

<!---
TODO(hopkins0): Add link to bitwise aritmetic operations.
-->
