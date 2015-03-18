 ```bash
/*
 * = Operador de asignación simple
 * += Suma + operador de asignación. 
 * -= Resta + operador de asignación
   *= Multiplicación + operador de asignación
 * /= División + operador de asignación
 * /= Modulo + operador de asignación
 */
package Operadores;

/**
 *
 * @author Edith
 */
public class Asignacion {
    public static void main(String[] args) {
        int A=10;
        int B=30;
        
        int C = A + B; //se asignará el valor de A + B a C
        C += A; //es equivalente a C = C + A
        System.out.println(C);
        C -= A; //es equivalente a C = C - A
        System.out.println(C);
        C *= A; //es equivalente a C = C * A
        System.out.println(C);
        C /= A; //es equivalente a C = C / A
        System.out.println(C);
        C %= A; //es equivalente a C = C % A
        System.out.println(C);
    }
}
 ```
