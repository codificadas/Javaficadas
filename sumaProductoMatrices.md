```bash
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package Matrices;

/**
 *
 * @author Edith
 */
public class matInicio {
    public int n; // dimension de la matriz
    private double[][] x; //array bidimensional
    
    //crea una matriz de "n" elementos con ceros
     public matInicio(int n) {
        this.n = n;
        x = new double[n][n];
        for(int i=0; i<n; i++){
            for(int j=0; j<n; j++){
                x[i][j]=0.0;
            }
        }
     }
     
     //crea una matriz con un array bidimensional pasado como parametro
     public matInicio(double[][] x) {
        this.x=x;
        n=x.length;
    }

     //muestra en pantalla a la matriz 
      public String mostrar(){
        String texto="\n";
        for(int i=0; i<n; i++){
            for(int j=0; j<n; j++){
                // tabulador "\t" y se limita el numero de decimales a tres
                texto+="\t "+(double)Math.round(1000*x[i][j])/1000;
            }
            //cuando se alcanza el final de la linea se inserta un  retorno de carro
            texto+="\n";
        }
        texto+="\n";
        return texto;
  }
      
      public  matInicio suma(matInicio a, matInicio b){
        matInicio resultado=new matInicio(a.n);
        for(int i=0; i<a.n; i++){
            for(int j=0; j<a.n; j++){
                resultado.x[i][j]=a.x[i][j]+b.x[i][j];
            }
        }
        return resultado;
    }
      
      public  matInicio producto(matInicio a, matInicio b){
        matInicio resultado=new matInicio(a.n);
        for(int i=0; i<a.n; i++){
            for(int j=0; j<a.n; j++){
                for(int k=0; k<a.n; k++){
                    resultado.x[i][j]+=a.x[i][k]*b.x[k][j];
                }
            }
        }
        return resultado;
    }  
      
      public static void main(String[] args) {                    
        double[][] a1={{2, 0, 1},{3,0,0},{5,1,1}};
        matInicio a=new matInicio(a1);
        
        double[][] a2={{1, 0, 1},{1,2,1},{1,1,0}};
        matInicio b=new matInicio(a2);
        
        System.out.println("Matriz A: " + a.mostrar());
        System.out.println("Matriz B: " + b.mostrar());        
        
        matInicio re = a.suma(a, b);
        System.out.println("Suma "+re.mostrar());
        matInicio re2 = a.producto(a, b);
        System.out.println("Producto "+re2.mostrar());
    }       
}

```
