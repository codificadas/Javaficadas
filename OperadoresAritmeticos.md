```bash
/*
 * las operaciones aritméticas básicas: 
 * suma (+), 
 * resta (-), 
 * multiplicación (*) 
 * división (/) y 
 * módulo (%) 
 * para datos de tipo numérico, tanto enteros como reales
 */

  /*
    Jerarquía de Operadores
    1.- paréntesis ()
    2.- signo -,+
    3.- potencias y raices ^
    4.- multiplicaciones y divisiones (módulo tmb) *,/,%
    5.- Sumas y restas, +,-

    Si hay dos o más de la misma jerarquía u orden, resolver de izquierda a derecha.
    Si se quiere alterar el orden normal de operaciones, entonces usar paréntesis.
  */
package Operadores;

/**
 *
 * @author Edith
 */
public class Aritmeticos {
    public static void main(String[] args){
        //VALORES ENTEROS
    /*    int i      = 12;
        int j      = 10;
        int suma   = i + j;
        int resta  = i - j;
        int mult   = i * j;
        int div    = i / j;
        int modulo = i % j;

        System.out.print("Suma :");
        System.out.println(suma );
        System.out.print("Resta :");
        System.out.println(resta);
        System.out.print("Multiplicacion :");
        System.out.println(mult);
        System.out.print("Division :");
        System.out.println(div);
        System.out.print("Modulo :");
        System.out.println(modulo);*/
        
        //El resultado de estas operaciones no puede quedar almacenado en una variable de tipo short o byte, por más pequeño que sea
        /*short a = 1;
        short b= 1;
        short x = a + b;*/
        
        //“overflow” (desbordamiento).  El valor 2147483647 (es decir 2^31 - 1 ) es el más grande que puede tolerar un int 
        //El intérprete de Java no nos avisa, por lo tanto tenemos que cuidarnos al trabajar cerca de los extremos.
        int j = 2147483647;
        int i = j + 1;
        System.out.println("El valor obtenido es " + i);
        
        /*No tenemos error al compilar. Pero al ejecutar el programa, el intérprete nos manda la siguiente nota:
         * Exception in thread "main" java.lang.ArithmeticException: / by zero
         * La moraleja es que no se puede dividir un entero por cero.
        */
       /* int x = 5;
        int y = 0;
        int z = x/y;
        System.out.println(z);*/
        
        
       //Con los float no nos marca error pero como resultado se obtiene un Infinity. Tener cuidad con las divisiones
        float x = 5.0f;
        float y = 0.0f;
        float z = x/y;
        System.out.println(z);
        
        // Dentro de los operadores aritméticos tenemos los unarios + y –
        int h = -1;
        int m = +h; // es equivalente a m = h * (+1)
        int n = -h; // es equivalente a n = h * (-1)
        System.out.println(m);
        System.out.println(n);
        
        //Dentro de losoperadores tenemos algunos unarios más. El auto incremental ++ y del auto decremental --
        int q = 2;
        int w = 2;
        System.out.println("q++ = "+(q++));
        System.out.println("++w = "+(++w));
        System.out.print("Estado Final (q) :");
        System.out.println(q);
        System.out.print("Estado Final (w) :");
        System.out.println(w);
  
        //Si colocamos el operador como sufijo, primero se evalúa la variable y luego se realiza la operación. 
        //es el caso de la variable q, antes de incrementar su valor se mostró por pantalla. 
        //Para la variable w el procedimiento fue inverso. Antes de mostrar su valor se incrementó.
        
        int e = 2;
        int r = 2;
        System.out.println(e--);
        System.out.println(--r);
        System.out.print("Estado Final (e) :");
        System.out.println(e);
        System.out.print("Estado Final (r) :");
        System.out.println(r);
        
        /*
            /*Ejercicios asignar valores para a, b y c obtener el resultado de las operaciones.
            1.- (a+b)/(22*a)
            2.- a+b*a-4+a
            3.- 23+a*(2+b-c)+20/a
            4.- 3+a-b*c/4
            5.- (8+a*b)/(b/4*a)
    
        */
        
       
     
    }
    
}

```
