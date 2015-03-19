```bash
package Estructuras_Control;
import java.util.Scanner;

public class Condicional_Selectiva_If {
   public static void main(String[] args) {
     Scanner sc = new Scanner(System.in);
      System.out.println("\nEstructura condicional multiple");
      int hora;
      System.out.println("Introduzca una hora (un valor entero): ");
      hora = sc.nextInt();
      if (hora >= 0 && hora < 12){
          System.out.println("Buenos días");
          //IF ANIDADO
            if (hora>=8){
              System.out.println("Ya LEVANTATE!!!");                      
            }else{
                System.out.println("Si gustas puedes dormir un poco más!!!"); 
            }  
      }else if (hora >= 12 && hora < 21)
           System.out.println("Buenas tardes");
      else if (hora >= 21 && hora < 24){
            System.out.println("Buenas noches");
            //IF ANIDADO
            if (hora==23){
              System.out.println("Ya duerme!!!");  
            }else{
                System.out.println("Si quieres aun no te duermas!!!"); 
            }  
      }else
            System.out.println("Hora no válida");
   }
}
```
