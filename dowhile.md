do while
--

```bash
/*
 * Programa que obliga al usuario a introducir un número menor que 100
 */
package Estructuras_Control;
import java.util.Scanner;

/**
 * @author Edith
 */
public class Est_do_while {
    public static void main(String[] args) {
        int valor;
        Scanner in = new Scanner( System.in );
        do {
            System.out.print("Escribe un entero < 100: ");
            valor = in.nextInt();
        }while (valor >= 100);
        System.out.println("Ha introducido: " + valor);
    }
}

```

Ejercicios
--

1.- Escribir un programa que solicite un número entre 0 y 999, y nos muestre un mensaje de cuántos dígitos tiene el mismo. Finalizar el programa cuando se ingrese el valor 0.

2.- Escribir un programa que solicite números por teclado y obtener su promedio. Finalizar de ingresar cuando se ingrese el valor 0.
