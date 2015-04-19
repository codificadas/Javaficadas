Un ejemplo completo
==
```bash
package arreglos;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

/**
 *
 * @author Edith
 */
public class operacionesArrays {
   
 

    public static void main(String[] args) throws IOException
    {
        //Creamos un objeto para obtener datos desde el teclado
        BufferedReader teclado = new BufferedReader(new InputStreamReader (System.in));
         
        String arreglo[];
        int i, n;
        String modifica;
        int posicion;
        String buscador;
        char opcion = 0;
         
        System.out.print("Introduce el número de datos a procesar: ");
        n = Integer.parseInt(teclado.readLine());
        arreglo = new String [n];
         
        for (i=0; i<n; i++)
        {
            System.out.print("Ingresa el elemento no. "+(i+1)+ ": ");
            arreglo[i] = teclado.readLine();
        }
        while(opcion !='x')
        {
            System.out.println("\n******************************");
            System.out.println("a.- Registrar nuevos elementos");
            System.out.println("b.- Contar elementos");
            System.out.println("c.- Quitar un elemento");
            System.out.println("d.- Exhibir los elementos");
            System.out.println("e.- Convertir elementos de minuscula-mayuscula"); 
            System.out.println("f.- Buscar un elemento");
            System.out.println("g.- Limpiar el arreglo");
            System.out.println("h.- Remplazar un elemento");
            System.out.println("i.- Invertir arreglo");
            System.out.println("x.- Salir");
            System.out.println("******************************");
            System.out.print("Ingresa una opción...  ");
            opcion = (char)System.in.read();
            teclado.readLine();
            
            //Sentencia switch para elegir una de varias opciones
            switch(opcion) //dependiendo de la opción ingresada se ejecuta una sentencia de las varias opciones disponibles
            {
                case 'a':                  
                    String nuevo;
                    System.out.println("Registrando nuevos elementos para el arreglo\n");
 
                    for(i=0; i<arreglo.length; i++)
                    {
                        System.out.print("Ingresa el elemento ["+(i)+"] = ");
                        arreglo[i] = teclado.readLine();                      
                    }
                    System.out.println("\nLos "+arreglo.length+" elementos han sido ingresado correctamente");
                break;
                 
                case 'b':    //Si se ingresa la opcion "b" ejecuta esta sentencia
                    System.out.println("Total de elementos \n "+arreglo.length);
                    break;
                
                case 'c':
                    System.out.println("Los Elementos almacenados en el arreglo son\n");
                    for(i=0; i<n; i++)
                    {
                        System.out.print(arreglo[i] + ", ");
                    }                  
                    System.out.println("\n");
                    String quitar;                   
                    System.out.print("Que elemento desea quitar?? ");
                    quitar = teclado.readLine();                   
                    
                    System.out.println();                   
                    for(i=0; i<n; i++)
                    {
                        if( arreglo[i].equals(quitar) )
                        {
                            System.out.println("Elemento ["+i+"] = "+arreglo[i]+" <- eliminado");
                            arreglo[i] = null;                          
                            //System.out.println("elemento ["+(i)+ "] eliminado"); 
                        }                
                       }
                       System.out.println("\nAhora los elementos son:\n");
                       for(i=0; i<n; i++)
                    {
                        System.out.println("Elemento ["+i+"] = "+arreglo[i]);
                    }                      
                    break;                   
                
                case 'd':    //Si se ingresa la opcion "d" ejecuta esta sentencia
                    System.out.println("\nElementos del arreglo son: \n");
                    for(i=0; i<n; i++)
                    {
                        System.out.print(" "+arreglo[i] + ", ");
                    }
                    System.out.println();                   
                    break;
                    
                case 'e':
                    System.out.println("\nVerificación: \n");
                    for(i=0; i<arreglo.length; i++)
                    {
                        if(arreglo[i].equals(arreglo[i].toLowerCase()))
                        {
                            System.out.println("["+i+"] = "+arreglo[i]+" <- es Minuscula ");                          
                            arreglo[i] = arreglo[i].toUpperCase();
                        }
                        else
                        {
                            System.out.println("["+i+"] = "+arreglo[i]+" <- es MAYUSCULA ");
                        }
                    }
                    System.out.println();
                    System.out.println("Elementos ");
                    for(i=0; i<arreglo.length; i++)
                    {                      
                        System.out.println("["+i+"] = "+arreglo[i]);
                    }                 
                    break;
                
                case 'f':    //Si se ingresa la opción "f" ejecuta esta sentencia
                    System.out.println();
                    System.out.print("Introduce el caracter a buscar: ");                 
                    buscador = teclado.readLine();                   
                    System.out.println();
                    
                    for(i=0; i<n; i++)
                    {
                        if( arreglo[i].equals (buscador) )
                        {
                            System.out.println("Buscando en posición ["+i+"] = "+arreglo[i]+" <- Caracter ENCONTRADO!");
                            //System.out.println("Buscando en posición ["+i+"] = "+arreglo[i]+" = "+buscador+" <- Caracter ENCONTRADO!");
                            //System.out.print("\nCaracter encontrado en la posicion ["+(i)+"] "); //Encuentra el caracter en la posición
                        }
                        else
                        {
                            System.out.println("Buscando en posición ["+i+"] = "+arreglo[i]+" <- Caracter no encontrado");
                            //System.out.print("\nCaracter no encontrado en ["+i+"]");                    
                        }                     
                       }
                       System.out.println();                 
                    break;
                     
                case 'g':
                        String confirmar;
                    System.out.print("\nHa elegido la opción limpiar, esta seguro de que quiere hacerlo?\nFavor de confirmar si o no? ");
                        confirmar = teclado.readLine();
                        
                        String eliminar = "si";
                        //System.out.println("\nHa elegido la opción limpiar, esta seguro de que quiere hacerlo?");
                        //confirmar = teclado.readLine();
                        System.out.println();
                        if(eliminar.equals(confirmar))
                        {
                        for (i=0; i<n; i++)
                        {
                            arreglo[i] = null;
                            System.out.println("elemento ["+(i)+ "] eliminado");                           
                            //System.out.println("elemento ["+(i)+ "] eliminado");
                            //arreglo[i] = " ";
                            //System.out.print(arreglo[i] + ", ");
                        }
                        }
                        else
                        {
                            System.out.println("Ha elegido conservar los elementos\n\tGracias!");
                        }
                     
                                
                                /*for (i=0; i<N; i++)
                        {
                            System.out.println("elemento ["+(i)+ "] eliminado");
                            arreglo[i] = null; //Elementos del arreglo se eliminan, pero el tamaño sigue siendo el mismo
                            //System.out.print("valor de ["+i+"] = "+arreglo[i]);
                        }*/
                    break;
                     
                case 'h':
                    System.out.print("\nIntroduce el nuevo Elemento: ");                 
                    modifica = teclado.readLine();
 
                    System.out.print("Introduce la posición valida en el Arreglo.. de [0] hasta ["+(arreglo.length-1)+"] : ");
                    posicion = Integer.parseInt(teclado.readLine());
                    
                    System.out.println("\nEl elemento ha sido reemplazado y se ha agregado el nuevo elemento: \n");
                    if( modifica !=  arreglo[posicion] )
                    {
                        arreglo[posicion] = modifica;
                        for (i = 0; i < n; i++)
                        {
                            System.out.print(" " + arreglo[i] + ",");
                        }
                    }
                    System.out.println();
                    break;
                     
                case 'i':    //Si se ingresa la opcion "i" ejecuta esta sentencia
                    System.out.println("\nArreglo Invertido: \n");                   
                    for (i = arreglo.length-1; i >= 0; i--)
                    {
                        System.out.print(" "+arreglo[i] + ", ");
                    }
                    System.out.println();
                    break;
                
                case 'x':    //Si se ingresa la opcion "x" ejecuta esta sentencia
                    opcion = 'x';
                    break;
                     
                default:    //Si el compilador no encuentra la opcioón que se ingreso entonces se ejecuta esta sentencia (default)
                    System.out.println("\nOpción incorrecta.. favor de insertar la opción disponible en el Menu");
                    break;
            }
        }
        System.out.println("\nHa salido correctamente de la Aplicación...");
    }
}
    


```
