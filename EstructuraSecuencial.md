```bash
/*
 Las estructuras de control determinan la secuencia de ejecución de las sentencias de un programa. 
 Las estructuras de control se dividen en tres categorías:
    Secuencial
    Condicional o Selectiva
    Iterativa o Repetitiva.
  
La estructura secuencial está formada por una sucesión de instrucciones que se ejecutan en orden una a continuación de la otra.
 */
package Estructuras_Control;

import java.util.Scanner;

/**
 *
 * @author Edith
 */
public class Estructura_Secuencial {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double numero1, numero2;
        System.out.println("Introduce el primer número:");
        numero1 = sc.nextDouble();
        System.out.println("Introduce el segundo número:");
        numero2 = sc.nextDouble();
        System.out.println("Números introducido: " + numero1 + "  " + numero2);
        System.out.println
          (numero1 + " + " + numero2 + " = " + (numero1+numero2));
        System.out.println
          (numero1 + " - " + numero2 + " = " + (numero1-numero2));
        System.out.println
          (numero1 + " * " + numero2 + " = " + numero1*numero2);
    }
}

```
