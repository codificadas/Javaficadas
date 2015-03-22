
Estructuras de Control parte 2
==
Iterativa o repetitiva
--
Permiten ejecutar de forma repetida un bloque específico de instrucciones.
Las instrucciones se repiten mientras o hasta que se cumpla una determinada condición. Esta condición se conoce como condición de salida.

Tipos de estructuras repetitivas:
- for

- while

- Do while

For
--
Hace que una instrucción o bloque de instrucciones se repitan un número determinado de veces mientras se cumpla la condición.

Estructura del for:
```bash
for(inicialización; condición; incremento/decremento){
  instrucción 1;
  ...........
  instrucción N;
}
```
Inicialización. Es la parte en la que la variable de control del bucle toman su valor inicial. La inicialización se realiza solo una vez.

Condición. Es una expresión booleana que hace que se ejecute la sentencia o bloque de sentencias mientras que dicha expresión sea cierta. Generalmente en la condición se compara la variable de control con un valor límite.

Incremento/decremento es una expresión que decrementa o incrementa la variable de control del bucle.

La ejecución de un bucle for sigue los siguientes pasos:

1. Se inicializa la variable de control (inicialización).
2. Se evalúa la condición.
3. Si la condición es cierta se ejecutan las instrucciones. Si es falsa, finaliza la ejecución del bucle y continúa el programa en la siguiente instrucción después del for.
4. Se actualiza la variable o variables de control (incremento/decremento)
5. Se vuelve al punto 2.

while
--
Estructura del while:
```bash
while (condición) {
  instrucción 1;
  ...........
  instrucción N;
}
```
La ejecución de un bucle while sigue los siguientes pasos:

1.      Se evalúa la condición.
2.       Si el resultado es false las instrucciones no se ejecutan y el programa sigue ejecutándose por la siguiente instrucción a continuación del while.
3.      Si el resultado es true se ejecutan las instrucciones y se vuelve al paso 1

do while
--
Las instrucciones se ejecutan mientras la condición sea cierta.
La condición se comprueba al final del bucle por lo que el bloque de instrucciones se ejecutarán al menos una vez. Esta es la diferencia fundamental con la instrucción while. Las instrucciones de un bucle while es posible que no se ejecuten si la condición inicialmente es falsa. 

Estructura del do while:
```bash
do {
  instrucción 1;
  ...........
  instrucción N;
}while (condición)
```

La ejecución de un bucle do - while sigue los siguientes pasos:

1.    Se ejecutan las instrucciones a partir de do{.
2.    Se evalúa la condición.
3. Si el resultado es false el programa sigue ejecutándose por la siguiente instrucción a continuación del while.
4.    Si el resultado es true se vuelve al paso 1.

Estructuras de control o Bucles anidados
--
Bucles anidados son aquellos que incluyen instrucciones for, while o do-while unas dentro de otras.
Debemos tener en cuenta que las variables de control que utilicemos deben ser distintas.
Los anidamientos de estructuras tienen que ser correctos, es decir, que una estructura anidada dentro de otra lo debe estar totalmente.

Slides
--

[Estructuras de control](https://www.haikudeck.com/javaficadas-education-presentation-SfsIP7LjoV)

Ejemplos
--

[For](https://github.com/codificadas/Javaficadas/blob/master/EstructuraSecuencial.md)
[while](https://github.com/codificadas/Javaficadas/blob/master/EstructuraSecuencial.md)
[do while](https://github.com/codificadas/Javaficadas/blob/master/EstructuraSecuencial.md)

