Arreglos
==
Los Arreglos en Java son agrupaciones de campos de memoria en los cuales podemos almacenar valores de forma “ordenada”, estos  valores almacenados pueden ser de tipo primitivo o de objetos (clases), para manipular los datos(agregar, eliminar, buscar) se accede a ellos por medio de su indice, el cual va desde 0 (cero) hasta su valor -1 (n-1), para empezar a enteder lo que es un arreglo tenemos la siguiente imagen:

http://upload.wikimedia.org/wikipedia/commons/3/3f/Array1.svg?uselang=es

Es de un arreglo de 10 elementos, cabe aclarar que en los diferentes campos siempre va un valor del mismo tipo de dato (int, float, double, boolean, etc). 

sintaxis para crear los arreglos:

```bash
tipo nombre_arreglo [] = new tipo[n];  
```

- **Unidimencionales**

Ejemplo de un arreglo creado de nombre numeros, y tipo int, este arreglo se crea con un espacio de 5 elementos, recordemos que sus indices van desde 0 hasta 4.

```bash
int numeros [] = new int [5];
```

Ejemplo de un arreglo de tipo double, pero no se crea con un número fijo de elementos sino con los valores almacenados en sus espacios, automaticamente java reconoce que este arreglo  tiene 3 elementos.

```bash
double tales [] = new double {5.5, 3.6, 4.5};
```

En los dos ejemplos suceden dos cosas diferentes en una misma linea, se declara el tipo y nombre del arreglo, seguidamente se instancia (crea) el elemento (ya sea con un tamaño o con sus valores); lo anterior lo digo ya que se pudieron hacer de la siguiente manera:

```bash
int numeros [];                                                                                                   
numeros = new int [5];
 
double tales [];
tales = new double {5.5, 3.6, 4.5};
```
Podemos crear e instanciar en una misma linea, o por el contrario podemos declarar el arreglo y luego podemos crearlo con el tamaño deseado.

Al momento de instanciar los arreglos estos se crean con sus valores predeterminados de cada tipo, así que se puede empezar a trabajar después de haber sido creados. 

```bash
public void Ejem1(){
        int arr1 [] = new int[5];//arreglo de 5 elementos
        String msj="";//variable que acumula el mensaje

        for(int i=0; i<arr1.length; i++){//ciclo para el recorrido del elemento
            arr1[i]=i;//asignación del elemento
            msj+="En el índice "+i+" se almaceno el valor: "+i+" \n";//cuando se asigna el valor se acumulan los datos en el mensaje
        }//fin ciclo
        JOptionPane.showMessageDialog(null, msj);//cuando finaliza el ciclo se muestra el mensaje.
    }
    
    public static void main(String[] args) {

        arreglo1 o = new arreglo1();//creación del objeto para invocar el método
        o.Ejem1();//invocación del método 
        
        System.exit(0);//linea para asegurar la terminación inmediata de la aplicación
    }
```
Para la manipulación de estos se hace por medio de un ciclo, el ciclo **for** es el más usado para recorrerlos, en la parte del condicional del ciclo vemos el uso del método **length** el cual lo usamos para saber el tamaño del arreglo. 

```bash
public void Ejem2(){
        int arr1 [] = new int[5], n;//arreglo de 5 elementos y variable que almacena el número a multiplicar
        String msj="";//variable que acumula el mensaje

        for(int i=0; i<arr1.length; i++){//ciclo para el recorrido del elemento           

            n = Integer.parseInt(JOptionPane.showInputDialog(null,"Ingrese el número a multiplicar en la posición "+(i+1)+": ")); 
            arr1[i]=i*n;//asignación del número dado de la multiplicación del anterior número ingresado por el índice
            msj+="En el indice "+i+" se almaceno el valor: "+arr1[i]+" \n";//cuando se asigna el valor se acumulan los datos en el mensaje
        }//fin ciclo
        JOptionPane.showMessageDialog(null, msj);//cuando finaliza el ciclo se muestra el mensaje.
    }
```

Muchas veces es necesario pasar como parámetros los arreglos. El ejemplo es de un arreglo con los números del 1 al 5, pasare este arreglo a un método el cual modificara sus valores por medio de una suma:

```bash
 public void Ejem3(){        
        int lista[]={3,4,5};
        // pasando arreglo como parametro
        camArr(lista);
        // desplegando 
        for( int r=0; r<lista.length; r++)
        System.out.println("lista["+r+"]="+lista[r]+'\n' );
        
 }
    
 public static void camArr(int vector[] )
 {
        // agregandole 10 a vector
        for( int r=0; r<vector.length; r++)
        vector[r]= vector[r] + 10;
 }
```

En el método camArr se puede apreciar la forma en la que se recibe un arreglo como parámetro, el nombre con el que se recibe es a criterio propio ya que esta sera una variable temporal (usada solo en este arreglo), al momento de invocarlo solo es necesario enviar como parámetro el nombre del arreglo.

La mayoría de veces el tamaño de un arreglo depende de las necesidades del usuario, es por eso que se puede definir el nombre del arreglo mucho antes de ser creado, esto último se hace cuando el usuario asigna el tamaño requerido al arreglo con el cual se desea trabajar, un ejemplo es el siguiente:

```bash
public void Ejem4(){
        int arr[], tam;//Declaración variables del arreglo y el tamaño que tendra el arreglo
 
        tam = Integer.parseInt(JOptionPane.showInputDialog(null, "De que tamaño desea el arreglo: "));//se ingresa el tamaño del arreglo        
        arr = new int[tam];//se crea el arreglo con el tamaño deseado por el usuario
 
        JOptionPane.showMessageDialog(null, "El tamaño del arreglo es de "+arr.length+" elementos....");//se muestra la cantidad de elemntos del arreglo
    }
```

**Ejercicio 1:** Escribir el codigo y encontrar el error.
```bash
public class ArrayDeNombres {
 
       public static void main(String arg[ ]) {
             String[ ] nombre = new String[4];
             nombre[0] = "Luis";
             nombre[1] = "María";
             nombre[2] = "Carlos";
             nombre[3] = "Jose";
             nombre[4] = "Ismael";   
     }
  }
  ```
  **Ejercicio 2:** Tomar el ejercicio 4 asignarle valores al arreglo y mostrarlo.
- **Bidimensional**

Sintaxis

Tipo_de_variable[ ][ ]   Nombre_del_array = new  Tipo_de_variable[dimensión1][dimensión2];
La declaración de una matriz:
```bash
int[][]  matriz = new int[3][2];
          O alternativamente
   int[][]  matriz;
   matriz = new int[3][2];
```

El número de elementos sería: 3 x 2 = 6, dónde 3 es el número de filas y 2 es el número de columnas.

Ahora procedemos a cargar la matriz con valores:
```bash
matriz[0][0] = 1; matriz[0][1] = 2; matriz[1][0] = 3; matriz[1][1] = 4; matriz[2][0] = 5; matriz[2][1] = 6;
```
Hay que recordar que los elementos empiezan a numerarse por 0. Así, la esquina superior izquierda de la matriz será el elemento [0][0] y la esquina inferior derecha será el [2][1]. Hay que prestar atención a esto porque en otros lenguajes de programación la numeración puede empezar por 1 en vez de por 0.

También se pueden cargar directamente los elementos, durante la declaración de la matriz de la siguiente manera:
```bash
int[][]  matriz = {{1,2},{3,4},{5,6}};
```

donde {1,2} corresponde a la fila 1, {3,4} a la fila 2 y {5,6} a la fila 3, y los números separados por coma dentro de cada fila, corresponden a las columnas. En este caso, los números (1, 3, 5) de cada una de las filas corresponden a la primera columna y los números (2, 4, 6) atañen a la  segunda columna.

 

Para obtener el número de filas de la matriz, podemos recurrir a la propiedad **length** de los arrays, de la siguiente manera:
```bash
int filas = matriz.length;
```
 

Para el caso del número de columnas sería de la siguiente forma :
```bash
int columnas = matriz[0].length;
```
 

También Java nos permite la posibilidad de clonar una matriz, es decir, crear una matriz nueva a partir de otra matriz, siguiendo esta sintaxis:
```bash
String[][] nuevaMatriz = matriz.clone();
```
donde clone() es un método especial, que permite la clonación de arrays de cualquier dimensión en Java. De esta manera “nuevaMatriz” y “matriz” son 2 matrices distintas pero con los mismos valores.


**Ejercicio:**

Queremos almacenar en una matriz el número de alumnos con el que cuenta una academia, ordenados en función del nivel y del idioma que se estudia. Tendremos 3 filas que representarán al Nivel básico, medio y de perfeccionamiento y 4 columnas en las que figurarán los idiomas (0 = Inglés, 1 = Francés, 2 = Alemán y 3 = Ruso). Se pide realizar la declaración de la matriz y asignarle unos valores de ejemplo a cada elemento.



