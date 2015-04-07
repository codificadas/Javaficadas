Arreglos
==
Los Arreglos en Java son agrupaciones de campos de memoria en los cuales podemos almacenar valores de forma “ordenada”, estos  valores almacenados pueden ser de tipo primitivo o de objetos (clases), para manipular los datos(agregar, eliminar, buscar) se accede a ellos por medio de su indice, el cual va desde 0 (cero) hasta su valor -1 (n-1), para empezar a enteder lo que es un arreglo tenemos la siguiente imagen:

http://upload.wikimedia.org/wikipedia/commons/3/3f/Array1.svg?uselang=es

Es de un arreglo de 10 elementos, cabe aclarar que en los diferentes campos siempre va un valor del mismo tipo de dato (int, float, double, boolean, etc). 

sintaxis para crear los arreglos:

```bash
tipo nombre_arreglo [] = new tipo[n];  
```

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
public static void main(String[] args) {
 
        ArrayJ o = new ArrayJ();//creacion del objeto para invocar el metodo
 
        o.Ejem4();//invocacion del metodo      
        System.exit(0);//linea para asegurar la terminacion inmediata de la aplicacion
    }
 
    public void Ejem1(){
        int arr1 [] = new int[5];//arreglo de 5 elementos
        String ax="";//variable que acumula el mensaje
 
        for(int i=0; i<arr1.length; i++){//ciclo para el recorrido del elemento
            arr1[i]=i;//asignacion del elemento
            ax+="En el indice "+i+" se almaceno el valor: "+i+"n";//cuando se asigna el valor se acumulan los datos en el mensaje
        }//fin ciclo
        JOptionPane.showMessageDialog(null, ax);//cuando finaliza el ciclo se muestra el mensaje.
    }
}
```
Para la manipulación de estos se hace por medio de un ciclo, el ciclo for es el más usado para recorrerlos, en la parte del condicional del ciclo vemos el uso del método length el cual lo usamos para saber el tamaño del arreglo. 


- Unidimencionales

- Bidimensional

- Multidimensional
