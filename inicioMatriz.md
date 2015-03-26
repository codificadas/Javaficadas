```bash
package Matrices;
import java.util.Scanner;

public class Matriz {
    public static void main(String[] args) {
        Scanner leer= new Scanner(System.in);
        Secundaria sec= new Secundaria();
        int x,y,a,b,valor, opcion;
        
        System.out.println("#######################################");
        System.out.println("          BI EN VE NI DO");
        System.out.println("Ingresa la dimensión de la matriz");
        System.out.println("Ingresa X");
        x=leer.nextInt();
        System.out.println("Ingresa Y");
        y=leer.nextInt();
        
        int vec[][] = new int [x][y];
        System.out.println("Ingresa la opción deseada");
        System.out.println("1)Llenar matriz\n2)Ordenar matriz\n3)Imprimir matriz\n4)Eliminar matriz\n5)Actualizar casilla de la matriz\n6)Suma total de los elementos de la matriz\n7)Salir");
        opcion=leer.nextInt();
        
        while(opcion != 7){
            switch(opcion){
                case 1:
                    sec.Llenar_Matriz(vec);
                    break;
                case 2:
                    sec.Ordenar_Matriz(vec);
                    break;
                case 3:
                    sec.Imprimir_Matriz(vec);
                    break;
                case 4:
                     System.out.println("Ingresa la posición  X");
                     a=leer.nextInt();
                     System.out.println("Ingresa la posición  Y");
                     b=leer.nextInt();
                     sec.Eliminar_Matriz(vec, a, b);
                    break;
                case 5:
                     System.out.println("Ingresa la posición  X");
                     a=leer.nextInt();
                     System.out.println("Ingresa la posición Y");
                     b=leer.nextInt();
                     System.out.println("Ingresa el nuevo valor");
                     valor=leer.nextInt();
                     sec.Actualizar_Matriz(vec, a, b, valor);
                    break;
                case 6:
                    sec.Sumar_Matriz();
                    break;
                case 7:
                    System.exit(0); 
                    break;
                default:
                    System.out.println("Opción incorrecta");
                    System.exit(0); 
                    break;
            }
            System.out.println("Ingresa la opción deseada");
            opcion=leer.nextInt();
        }
           
    }
    
}
```
