 ```bash
/*
 * Realizan las operaciones lógicas de conjunción (AND), disyunción (OR), negación (NOT) y la disyunción exclusiva (XOR)
 *AND &&
 *OR ||
 *NOT !
 
  * Cada una de estas operaciones tiene asociada una tabla de verdad. 
  * Esto nos permite ver el resultado de un operador aplicado a las distintas combinaciones de valores que pueden tener los operandos. 

 */

/*
    Jerarquía de Operadores
    7.- not, and, or (!, &&, ||)
*/

package Operadores;

/**
 * @author Edith
 */
public class Logicos {
    public static void main(String[] args) {
       //Tabla de verdad del AND
        boolean x = true;
        boolean y = false;
        boolean a1 = x && x;
        boolean a2 = x && y;
        boolean a3 = y && x;
        boolean a4 = y && y;

        System.out.println("Tabla de verdad de la conjunción AND");
        System.out.println( x + " AND " + x + " = " + a1 );
        System.out.println( x + " AND " + y + " = " + a2 );
        System.out.println( y + " AND " + x + " = " + a3 );
        System.out.println( y + " AND " + y + " = " + a4 );
        
        
        //Otro ejemplo.  El intérprete nos avisa que el resultado es "false"
        System.out.println();
        int m = 0;
        int n = 2;
        boolean b = ( m != 0 ) && ( ( n / m ) != 0 ); 
        System.out.println(b);
        
        System.out.println();
        int r = 4;
        boolean t = ( r > 3 ) && ( r < 6 );
        System.out.println(t);
        
        char f = 'b';
        boolean g = ( f == 'a' ) || ( f == 'A' );
        System.out.println(g);
        
        //Ejercicio crear las tabla de verdad del OR || y NOT !
    }
   
}
 ```
