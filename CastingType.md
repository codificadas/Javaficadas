 ```bash
 /*
 * El casting es un procedimiento para transformar una variable primitiva de un tipo a otro, 
 * o transformar un objeto de una clase a otra clase siempre y cuando haya una relación de herencia entre ambas
 * 
 * Implícito: no se necesita escribir código para que se lleve a cabo. 
    Ocurre cuando se coloca un valor pequeño en un contenedor grande.
 * Explícito: sí es necesario escribir código. 
    Ocurre cuando se coloca un valor grande en un contenedor pequeño. Son susceptibles de pérdida de datos.

 http://www.roseindia.net/java/java-conversion/
 */
package basico;

/**
 *
 * @author Edith
 */
public class CastingType {
    public static void main(String[] args) {
        //Implícito
        byte a_max =127; 
        int b =a_max;

        int x = 123999;
       // byte y = x;

        //Explícito
        int entero = 12399;
        String i= Integer.toBinaryString(entero);
        System.out.println("Binary: " + i);
        
        //Convertir String a entero
        String stra = "126";
        int c = Integer.parseInt(stra);
        //System.out.println("String: " + stra);
        System.out.println("Integer: " + c);

        //Convertir un entero a String
        int e = 123;
        String str = Integer.toString(e);
        System.out.println("Int to String:=" +str);


        double f = 123;
        String str1 = Double.toString(f);
        System.out.println("Double to String:=" +str1);



        //Convertir caracter a string
        String s = "hol a";
        char c1 = s.charAt(0);
        System.out.println("Character value is " + c1);
        String s1 = Character.toString(c1);
        System.out.println("String value is " + s1);
        
       
    }
    
}
```
