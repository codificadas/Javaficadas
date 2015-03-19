```bash
package Estructuras_Control;
import java.util.Scanner;

public class Condicional_Selectiva_If {
   public static void main(String[] args) {
     //Ejemplo estructura condicional multiple de IF _ELSE
     Scanner sc = new Scanner(System.in);
      System.out.println("\nEstructura condicional multiple");
      int hora;
      System.out.println("Introduzca una hora (un valor entero): ");
      hora = sc.nextInt();
      if (hora >= 0 && hora < 12)
          System.out.println("Buenos días");
      else if (hora >= 12 && hora < 21)
           System.out.println("Buenas tardes");
      else if (hora >= 21 && hora < 24)
            System.out.println("Buenas noches");
      else
            System.out.println("Hora no válida");
   }
}
```
