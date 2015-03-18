 ```bash
/*
 * En java disponemos de los operadores relacionales para verificar si se cumple una relación
 *Mayor que >
 *Mayor o igual que >=
 *Menor que <
 *Menor o igual que <=
 *Igual que ==
 *Distinto de !=
 */
/*
    Jerarquía de Operadores
    6.- ==, <, >, <=, >=, <> ó !=
  */
package Operadores;

/**
 *
 * @author Edith
 */
public class Relacionales {
    public static void main(String args[]){
       int    i = -3;
       byte   b = 5;
       float  f = 1e-10f;
       double d = 3.14;
       boolean b1 = i > i;
       boolean b2 = i < b;
       boolean b3 = b <= f;
       boolean b4 = f >= d;
       boolean b5 = d != 0;
       boolean b6 = 1 == f;
 
       System.out.println("b1: " + i + " > " + i + " = " + b1);
       System.out.println("b2: " + i + " < " + b + " = " + b2);
       System.out.println("b3: " + b + " <= " + f + " = " + b3);
       System.out.println("b4: " + f + " >= " + d + " = " + b4);
       System.out.println("b5: " + d + " != " + 0 + " = " + b5);
       System.out.println("b6: " + 1 + " == " + f + " = " + b6);
       
       System.out.println();
       //Podemos comparar caracteres, pues internamente están almacenados como números
       System.out.println("COMPARACIÓN DE CARACTERES");
       char y = 'A';
       char z = 'B';
       boolean x = y > z;
       System.out.println("y > z " + x);
       
       System.out.println();
       //Entre los booleanos solo se permiten los operadores de equivalencia, es igual (==) o es distinto (!= )
       System.out.println("Entre los booleanos solo se permiten los operadores de equivalencia");
       boolean r = true;
       boolean t = r == r;
       boolean u = r != t;
       System.out.println("r == r " + t);
       System.out.println("r != t " + u);
   }
    
}
 ```
