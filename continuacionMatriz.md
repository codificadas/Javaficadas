```bash
package Matrices;
import java.util.Random; // para obtener numeros aleatorios

public class Secundaria {
    Random r=new Random();
    int sum=0;
    //Llenar matriz con valores aleatorios
    public void Llenar_Matriz(int vec[][]){
        for(int f=0; f < vec.length; f++){
            for(int c=0;c < vec[f].length; c++){
                vec[f][c]=r.nextInt(10);
                //sumo valores de matriz
                sum=sum+vec[f][c];
            }
        }
    }
    
    public void Imprimir_Matriz(int vec[][]){
        for(int f=0;f<vec.length; f++){
            for(int c=0;c<vec[f].length; c++){
               System.out.print(" "+vec[f][c]);
            }
            System.out.println("");
        }
        
    }
    
    public void Ordenar_Matriz(int vec[][]){
        for(int i=0;i<vec.length; i++){
            for(int j=0;j<vec[1].length; j++){
                for(int x=0;x<vec.length; x++){
                    for(int y=0;y<vec[i].length; y++){
                        if(vec[i][j]< vec[x][y]){
                            int c = vec[i][j];
                            vec[i][j]=vec[x][y];
                            vec[x][y]=c;
                        }
                    }
                }
              
            }
        }
    }
    
    public void Eliminar_Matriz(int vec[][], int f, int c)
    {
        vec[f][c]=0;
    }
    
    //Actualizar contenido de una casilla de la matriz
    public void Actualizar_Matriz(int vec[][], int f, int c,int valor){
        vec[f][c]=valor;
    }
    
    public void Sumar_Matriz(){
       System.out.println("La suma es "+sum);
    }
       
}
```
