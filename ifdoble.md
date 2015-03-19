```bash
package Estructuras_Control;
import java.util.Scanner;

public class Condicional_Selectiva_If {
   public static void main(String[] args) {
    //Ejemplo de estructura condicional doble IF_ELSE
        Scanner sc = new Scanner(System.in);
        System.out.println("\nEstructura condicional doble");
        System.out.print("Nota: ");
        int nota1 = sc.nextInt();
        if (nota1 >= 5 ){
            System.out.println("Enorabuena!!");
            System.out.println("Has aprobado");
        }
        else
            System.out.println("Lo Siento, has suspendido");
   }
}
```
