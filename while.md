while
--

```bash
/*
 Programa que lee números hasta que se lee un negativo y muestra la
 * suma de los números leídos
 */
package Estructuras_Control;
import java.util.*;

/**
 * @author Edith
 */
public class Est_while {
    public static void main(String[] args) {
         int suma = 0, num;
        Scanner sc = new Scanner(System.in);
        System.out.print("Introduzca un número: ");
        num = sc.nextInt();
        while (num >= 0){
               suma = suma + num;
               System.out.print("Introduzca un número: ");
               num = sc.nextInt();
        }
        System.out.println("La suma es: " + suma );
    }
}

```

Ejercicios
--

1.- Escribir un programa que solicite un valor positivo y nos muestre desde 1 hasta el valor ingresado.
Ejemplo: Si ingresamos 30 se debe mostrar en pantalla los números del 1 al 30.

2.- Desarrollar un programa que solicite 10 valores y nos muestre posteriormente la suma de los valores ingresados y su promedio.

3.- Una planta que fabrica perfiles de hierro posee un lote de n piezas.
Crear un programa que pida ingresar por teclado la cantidad de piezas a procesar y luego ingrese la longitud de cada perfil; sabiendo que la pieza cuya longitud esté comprendida en el rango de 1,20 y 1,30 son aptas. Imprimir por pantalla la cantidad de piezas aptas que hay en el lote.

Otros ejercicios
--

4.- Escribir un programa que solicite ingresar 10 notas de alumnos y nos informe cuántos tienen notas mayores o iguales a 7 y cuántos menores.

5.- Se ingresan un conjunto de n alturas de personas por teclado. Mostrar la altura promedio de las personas.

6.- En una empresa trabajan n empleados cuyos sueldos oscilan entre $100 y $500, realizar un programa que lea los sueldos que cobra cada empleado e informe cuántos empleados cobran entre $100 y $300 y cuántos cobran más de $300. Además el programa deberá informar el importe que gasta la empresa en sueldos al personal.

7.- Mostrar los múltiplos de 8 hasta el valor 500. Debe aparecer en pantalla 8 - 16 - 24, etc.

8.- Desarrollar un programa que permita cargar n números enteros y luego nos informe cuántos valores fueron pares y cuántos impares.
Pueden emplear el operador ?%? en la condición de la estructura condicional:
	if (valor%2==0)         //Si el if da verdadero luego es par.
