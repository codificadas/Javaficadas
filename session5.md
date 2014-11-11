Operadores básicos
==

Java provee un gran set de operadores para manipular variables. Podemos dividirlos en los siguientes grupos:

- Operadores aritméticos

- Operadores relacionales

- Operadores lógicos

- Operadores de asignación

- Operadores de bits

- Misc Operators

Por ahora nos vamos a enfocar en conocer a la perfección los primeros 4 grupos.

Operadores aritméticos
--

Los operadores aritméticos son usados en expresiones matemáticas de la misma manera que son usados en álgebra. La siguiente tabla lista los operadores aritméticos:

Crea una variable A = 10 y una variable B = 20, entonces:

|Operador|Descripción                                                                           |Ejemplo    |
|---     |---                                                                                   |---        |
|+       |Adición - agrega valores a cada lado del operador                                     |A + B = 30 |
|-       |Sustracción - resta el operando de la derecha del operando de la izquierda            |A - B = -10|
|*       |Multiplicación - multiplica los valores a cada lado del operador                      |A * B = 200|
|/	     |División - divide el operando de la izquierda por el operando de la derecha           |A / B = 2  |
|%       |Módulo - divide el operando de la izquierda por el de la derecha y devuelve el residuo|A % B = 0  |
|++ 	 |Incremento - incrementa el valor del operando en 1                                    |B++ = 21   |
|-- 	 |Decremento - decrementa el valor del operando en 1                                    |B-- = 19   |


Operadores relacionales
--

Estos son los operadores relacionales soportados por Java:

Crea una variable A = 10 y una variable B = 20, entonces:

|Operador |Descripción                                                                                                                                              |Ejemplo                |
|---      |---                                                                                                                                                      |---                    |
|==       |Evalúa si el valor de los dos operandos es igual o no, si lo son la condición evalúa true.                                                               |(A == B) no es true.   |
|!=       |Evalúa si el valor de los dos operandos es igual o no, si no lo son la condición evalúa true.                                                            |(A != B) es true.      |
|>        |Evalúa si el valor del operador de la izquierda es mayor que el valor del operando de la derecha, si lo es, entonces la condición evalúa true.           |(A > B) no es true.    |
|<	      |Evalúa si el valor del operador de la izquierda es menor que el valor del operando de la derecha, si lo es, entonces la condición evalúa true.           |(A < B) es true.       |
|>=       |Evalúa si el valor del operador de la izquierda es mayor o igual que el valor del operando de la derecha, si lo es, entonces la condición evalúa true.   |(A >= B) no es true.   |
|<= 	  |Evalúa si el valor del operador de la izquierda es menor o igual que el valor del operando de la derecha, si lo es, entonces la condición evalúa true.   |(A <= B) es true.      |


Operadores lógicos
--

Estos son los operadores lógicos soportados por Java:

Crea una variable A = true y una variable B = false, entonces:
0 = false
1 = true

|Operador |Descripción                                                                                                                                                      |Ejemplo                |
|---      |---                                                                                                                                                              |---                    |
|&&       |Llamado operador lógico AND. Si ambos operandos son true, entonces la condición se convierte en true.                                                            |(A && B) es false.     |
|||       |Llamado operador lógico OR. Si cualquiera de los dos operandos es true, entonces la condición se convierte en true.                                              |(A || B) es true.      |
|!        |Llamado Operador lógico NOT. Se utiliza para inviertir el estado lógico de su operando. Si una condición es true entonces el operador lógico NOT evaluará false. |!(A && B) is true.     |


Operadores de Asignación
--
Estos son los operadores lógicos soportados por Java:

|Operador |Descripción                                                                                                                                                      |Ejemplo                |
|---      |---                                                                                                                                                              |---                    |
|=        |Operador de asignación simple - asigna valores de operandos desde el lado derecho para el operando del lado izquierdo                                            |(A == B) no es true.   |
|+=       |Suma + operador de asignación - añade el valor del operando derecho al operando de la izquierda y asigna el resultado al operando de la izquierda                |(A != B) es true.      |
|-=       |Resta + operador de asignación - resta el valor del operando derecho al operando de la izquierda y asigna el resultado al operando de la izquierda               |(A > B) no es true.    |
|*=	      |Multiplicación + operador de asignación - multiplica el valor del operando derecho al operando de la izquierda y asigna el resultado al operando de la izquierda |(A < B) es true.       |
|/=       |Divición + operador de asignación - divide el valor del operando izquierdo al operando de la derecha y asigna el resultado al operando de la izquierda           |(A >= B) no es true.   |
|%= 	  |Modulo + operador de asignación - toma el módulo usando dos operadores y asigna el resultado al operando de la izquierda                                         |(A <= B) es true.      |


Jerarquía de Operadores
--

**Operadores aritméticos (su resultado es un número)**

1.- paréntesis ()

2.- signo -,+

3.- potencias y raices ^

4.- multiplicaciones y divisiones (módulo tmb) *,/,%

5.- Sumas y restas, +,-

**Operadores relacionales (su resultado es un valor de verdad, 0 falso, 1 verdadero)**

6.- ==, <, >, <=, >=, <> ó !=

**Operadores lógicos o booleanos (su resultado es un valor de verdad, 0 falso, 1 verdadero)**

7.- not, and, or (!, &&, ||)

**NOTAS:**
- Si hay dos o más de la misma jerarquía u orden, resolver de izquierda a derecha.
- Si se quiere alterar el orden normal de operaciones, entonces usar paréntesis.
- Tampoco es bueno usar paréntesis de más en una operación, esto sólo indica que no se evalúo bien la formula, como en el siguiente ejemplo: area = (base * altura) / 2

Ejercicios
--
1. Hacer un programa para ver el funcionamiento de los operadores aritméticos.
2. Hacer un programa para ver el funcionamiento de los operadores relacionales.
3. Hacer un programa para ver el funcionamiento de los operadores lógicos.
4. Hacer un programa para ver el funcionamiento de los operadores de asignación.

Slides
--

[Tipos de datos, modificadores y variables!](https://www.haikudeck.com/javaficadas-education-presentation-5xHCKLpOE8)