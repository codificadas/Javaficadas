```bash
package Estructuras_Control;
import java.util.Scanner;

public class Condicional_Selectiva_If {
   public static void main(String[] args) {
    System.out.println("IF");
       Scanner sc = new Scanner( System.in );
       System.out.print("Nota: ");
       int nota = sc.nextInt();
       if (nota >= 5 ){
           System.out.println("Enorabuena!!");
           System.out.println("Has aprobado");
       }
   }
}
```
