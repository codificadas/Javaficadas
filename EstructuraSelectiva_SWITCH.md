```bash
package Estructuras_Control;
import java.util.Scanner;

/**
 * @author Edith
 */
public class Condicional_Selectiva_switch {
     public static void main(String[] args) {
        /*
        * Ejemplo 1 Programa que pide un número de mes y muestra el nombre correspondiente
        */
       int mes;
        Scanner sc = new Scanner(System.in);
        System.out.print("Introduzca un numero de mes: ");
        mes = sc.nextInt();
        switch (mes)
        {
                case 1: 
                    System.out.println("ENERO");
                    break;
                case 2: 
                    System.out.println("FEBRERO");
                    //podemos usar if dentro de un switch? claro que si.
                    System.out.print("Introduzca un día: ");
                    int dia = sc.nextInt();
                    if(dia==10)
                    {
                       System.out.print("Feliz cumpleaños!!! :) "); 
                    }else{
                       System.out.print("No es tu cumple :) ");
                    }
                    break;
                case 3: 
                    System.out.println("MARZO");
                    break;
                case 4: 
                    System.out.println("ABRIL");
                    break;
                case 5: 
                    System.out.println("MAYO");
                    break;
                case 6: 
                    System.out.println("JUNIO");
                    break;
                case 7: 
                    System.out.println("JULIO");
                    break;
                case 8: 
                    System.out.println("AGOSTO");
                    break;
                case 9: 
                    System.out.println("SEPTIEMBRE");
                    break;
                case 10: 
                    System.out.println("OCTUBRE");
                    break;
                case 11: 
                    System.out.println("NOVIEMBRE");
                    break;
                case 12: 
                    System.out.println("DICIEMBRE");
                    break;
                default : 
                    System.out.println("Mes no válido");                       
        }
             
    }
}

/*Ejercicios
       1.- Pida la edad y decir si es mayor de edad
       2.- Pedir un número del 1 al 7 y decir el día de la semana correspondiemte
       3.- Determinar si un número es positivo o negativo
       4.- Pedir un número del 1 al 12 y decir el nombre del mes correspondiente
       5.- Pedir un número e indicar si es positivo y menor que 100
*/

```
