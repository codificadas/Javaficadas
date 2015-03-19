```bash
package Estructuras_Control;
import java.util.Scanner;

public class Condicional_Selectiva_If {
   public static void main(String[] args) {
      /*Se puede utilizar en sustitución de la sentencia de control if-else po ? :.
       *Si expresión1 es cierta entonces se evalúa expresión2
       *Si expresión1 es falsa, se evalúa expresión3
    */
     Scanner sc = new Scanner( System.in );
     System.out.println("\nOPERADOR CONDICIONAL ? :");
        int num;      
        System.out.println("Introduzca numero: ");
        num = sc.nextInt();
        System.out.println((num%2)==0 ? "PAR" : "IMPAR"); 
    } 
}
```
