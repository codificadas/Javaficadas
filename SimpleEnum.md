 ```bash

/*
 * Un tipo enumerado restringe los posibles valores que puede tomar una variable
 * Cada elemento de un enumerado es un objeto único disponible para su uso, por lo tanto podemos accesar a propiedades y metodos.
 * Un tipo enumerado puede ser declarado dentro o fuera de una clase, pero no dentro de un método.
 * Un enum no es un String ni tampoco int por lo tanto si deseamos usarlos como tal debemos hacer la conversión: toString()
 *
 */
package ENUMS;

/**
 * @author Edith
 */
public class SimpleEnum {
    enum TipoDeMadera { ROBLE, CAOBA, NOGAL, CEREZO, BOJ };
    
  
    public static void main(String[] args) {
       for (TipoDeMadera tmp: TipoDeMadera.values()) {
        //Un enum no es un String  por lo tanto debemos hacer la conversión: toString()
        System.out.print(tmp.toString()+"\t");   
       } 
        System.out.print("\n");   
        TipoDeMadera maderaUsuario= TipoDeMadera.NOGAL;
        System.out.println ("La madera elegida por el usuario es " + maderaUsuario.toString().toLowerCase() );
        System.out.println ("¿Es la madera elegida por el usuario caoba? Resultado: " + (maderaUsuario==TipoDeMadera.CAOBA) );
        System.out.println ("¿Es la madera elegida por el usuario roble? Resultado: " + (maderaUsuario==TipoDeMadera.ROBLE) );
       
    }    
}
 ```
