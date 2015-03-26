```bash
package Matrices;

import java.util.Random;

/** *
 * @author Edith
 */
public class MatUNO {
    public static void main(String[] args) {
        int x,y;
        int A[][]=new int[3][3];
        int B[][]=new int[3][3];
        int C[][]= new int[3][3];
        
        //LLENAR  ARRAYS CON RANDOM
        Random r=new Random();
        for(x=0; x<3; x++)
        {
            for(y=0; y<3; y++)
            {
               A[x][y]=r.nextInt(10);
               B[x][y]=r.nextInt(10);
            }
        }
        
        //MOSTRAR ARRAY A
              
        String MatA="\n";
        for(int i=0; i<3; i++){
            for(int j=0; j<3; j++){
                MatA+="\t "+A[i][j];
            }
            MatA+="\n";
        }
        MatA+="\n";
        
        System.out.println("Matriz A");
        System.out.println(MatA);
        
         //MOSTRAR ARRAY B
        String MatB="\n";
        for(int i=0; i<3; i++){
            for(int j=0; j<3; j++){
                MatB+="\t "+B[i][j];
            }
            MatB+="\n";
        }
        MatB+="\n";
                
        System.out.println("Matriz B");
        System.out.println(MatB);
        
        //SUMAR ARRAYS
        for(x=0; x<3; x++)
        {
            for(y=0; y<3; y++)
            {
               C[x][y]=A[x][y]+B[x][y];
            }
        }
              
        String texto="\n";
        for(int i=0; i<3; i++){
            for(int j=0; j<3; j++){
                texto+="\t "+C[i][j];
            }
            texto+="\n";
        }
        texto+="\n";
        System.out.println("Suma Matriz");
        System.out.println(texto);
        
        //producto ARRAYS
        for(x=0; x<3; x++)
        {
            for(y=0; y<3; y++)
            {
               C[x][y]=A[x][y]*B[x][y];
            }
        }
              
        String prodMat="\n";
        for(int i=0; i<3; i++){
            for(int j=0; j<3; j++){
                prodMat+="\t "+C[i][j];
            }
            prodMat+="\n";
        }
        prodMat+="\n";
        System.out.println("Producto Matriz");
        System.out.println(prodMat);
       
    }
    
}
```
