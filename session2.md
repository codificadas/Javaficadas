Sintaxis básica de Java
===

En esta sesión hablaremos de manera general sobre la sintaxis básica del lenguaje; qué podemos usar?, qué no?, consideraciones y buenas prácticas para la hora de escribir programas.


Objetos, clases, métodos, variables de instancia
--

* **Objeto:** los objetos tienen características y comportamientos. Ejemplo: Un perro tiene como características - color y nombre, así como comportamientos - ladrar, comer, etc. Un objeto es una instancia de una clase.

* **Clase:** Una clase puede ser definida como una plantilla que describe los comportamientos y características que objetos de su tipo soportan.

* **Métodos:** Un método es básicamente un comportamiento. Una clase puede contener muchos métodos. Es en los métodos donde se escribe la lógica, los datos son manipulados y las acciones son ejecutadas.

* **Variables de instancia:** Cada objeto tiene un único set de variables de instancia. Una característica del objeto es creado por el valor asignado a estas variables de instancia.


Análisis de MiPrimerPrograma
--

1. Crear una carpeta llamada programas de Java

2. Abrir Textmate

3. Copiar el siguiente código de Java:

    ```bash
    /* Este es mi primer programa en Java.
     * Imprimira Hola Javaficadas como salida.
     */

    public class MiPrimerPrograma {

        public static void main(String []args) {
           System.out.println("Hola Javaficadas!"); //Imprime Hola Javaficadas
        }
    }
    ```

4. Guardar el archivo: nombre **MiPrimerPrograma.java**

3. Abrir la consola/terminal

4. Ir hasta la carpeta que hemos creado, en mi caso: cd Documents/Codificadas/java/programas

5. Podemos hacer un **ls** (**dir** para windows) para ver si nuestro programa está ahí

6. Ahora necesitamos compilar nuestro código, para eso usaremos el comando **javac**

    ```bash
    javac MiPrimerPrograma.java
    ```
7. Ahora que nuestro programa está compilado hacemos un **ls** (**dir** para windows) y veremos que se ha generado un archivo llamado **MiPrimerPrograma.class**

8. Para ejecutar nuestro programa usamos el comando **java**

    ```bash
    java MiPrimerPrograma
    ```

9. Y debemos ver nuestro mensaje: **Hola Javaficadas!**

10. Yeiii todo muy bien!


Sintaxis básica de Java
--

En relación a los programas de Java, es muy importante tener en cuenta los siguientes puntos:

* **Case Sensitivity** - Java es sensible a mayúsculas y minúsculas, lo que significa que el identificador Hello y hello tendrían diferente significado en Java.

* **Class Names** - La primer letra de los nombres de clases debe ser mayúscula. Si se utilizará más de una palabra para nombrar una clase, cada palabra deberá iniciar en mayúscula.

    ```bash
    Example class MiPrimerPrograma
    ```

* **Method Names** - Todos los nombres de métodos deben iniciar con una letra minúscula. Si se utilizará más de una palabra para nombrar una clase, cada palabra deberá iniciar en mayúscula luego de la primera.

    ```bash
    Example public void myMethodName()
    ```

* **Program File Name** - El nombre del archivo que contiente tu programa debe ser exactamente igual a como nombraste la clase. Cuando lo guardes, debes guardarlo usando el nombre de la clase (Recuera que Java es case sensitive) y ponle '.java' al final del nombre (si el nombre del archivo y el de la clase no coinciden, tu programa no podrá compilar).

    ```bash
    Example : Si 'MiPrimerPrograma' es el nombre de la clase. Entonces el archivo deberá ser guardado como 'MiPrimerPrograma.java'
    ```

* **public static void main(String args[])** - Java inicia su proceso de ejecución desde el método main() el cual es obligatoriamente parte de cada programa de Java.

Identificadores
--

Todos los componentes de Java requieren nombres. Nombres para clases, variables y métodos son llamados **identificadores**.

En java, hay varios puntos que debemos tener en cuenta con respecto a los identificadores:

* Todos los identificadores deben iniciar con una letra ("A" a "Z", o "a" a "z"), el signo de pesos ($) o un guión bajo (_).

* Después del primer caracter, los identificadores pueden incluir cualquier combinación de caracteres.

* Una palabra reservada no puede ser usada como un identificador.

* Los identificadores son case sensitive.

* Ejemplos de identificadores válidos: edad, $salario, _valor, __1_valor

* Ejemplos de identificadores inválidos: 123abc, -salario


Modificadores
--

Como con otros lenguajes, es posible modificar clases, métodos, etc. usando modificadores. Hay 2 categorías:

* Modificadores de acceso: default, public , protected, private

* Modificadores de no acceso: final, abstract, strictfp

Los vemos luego a detalle.


Variables
--

Veremos los siguientes tipos de variabes en Java:

* Variables locales

* Variables de clase (Variables Estáticas)

* Variables de instancia (Variables No-estáticas )

Arrays
--

Los arreglos son objetos que guardan multiples variables del mismo tipo. Veremos como declararlos, construirlos e inicializarlos en próximas sesiones.

Enums
--

Enums fueron introducidos en java 5.0. Enums restringe una variable a tener uno de sólo unos valores predefinidos. Los valores en esta lista enumerada son llamados enums.

Con el uso de enums es posible reducir el numero de bugs en tu código.

Por ejemplo, si consideramos una aplicación para una tienda de jugos, sería posible restringir la medida del vaso a pequeño, mediano y grande. Esto aseguraría que no permitiría a nadie ordenar cualquier otro tamaño diferente a pequeño, mediano y grande.

Ejemplos

```bash
class FreshJuice {

   enum FreshJuiceSize{ SMALL, MEDIUM, LARGE }
   FreshJuiceSize size;
}

public class FreshJuiceTest {

   public static void main(String args[]){
      FreshJuice juice = new FreshJuice();
      juice.size = FreshJuice. FreshJuiceSize.MEDIUM ;
      System.out.println("Size: " + juice.size);
   }
}
```

```bash
/*
 * Un tipo enumerado restringe los posibles valores que puede tomar una variable
 * Cada elemento de un enumerado es un objeto único disponible para su uso, por lo tanto podemos accesar a propiedades y métodos.
 * Un tipo enumerado puede ser declarado dentro o fuera de una clase, pero no dentro de un método.
 * Un enum no es un String por lo tanto si deseamos usarlos como tal debemos hacer la conversión: toString()
 */

public class Enumeradores {
  enum TipoDeMadera { ROBLE, CAOBA, NOGAL, CEREZO, BOJ };
  
    public static void main(String[] args) {
    //Imprimir todos los valores del enum usando el método values()
       for (TipoDeMadera tmp: TipoDeMadera.values()) {
        //  \t  usamos el tabulador para separar los valores 
        System.out.print(tmp.toString()+"\t");   
       } 
       //accesando a las propiedades
        TipoDeMadera maderaUsuario= TipoDeMadera.ROBLE;
        System.out.println ("La madera elegida por el usuario es " + maderaUsuario.toString().toLowerCase() );
        System.out.println ("¿Es la madera elegida por el usuario caoba? Resultado: " + (maderaUsuario==TipoDeMadera.CAOBA) );
        System.out.println ("¿Es la madera elegida por el usuario roble? Resultado: " + (maderaUsuario==TipoDeMadera.ROBLE) );
       
       
    }
  
}
```




Palabras reservadas (keywords)
--

La siguiente lista muestra las palabras reservadas en Java. Estas palabras reservadas no pueden ser usadas como constantes o variables o cualquier otro nombre de identificador.

|        |            |         |          |
|---     |---         |---      |---       |
|abstract|assert      |boolean  |break     |
|byte    |case        |catch    |char      |
|class   |const       |continue |default   |
|do	     |double      |else	    |enum      |
|extends |final	      |finally  |float     |
|for	 |goto	      |if	    |implements|
|import	 |instanceof  |int      |interface |
|long	 |native	  |new	    |package   |
|private |protected	  |public	|return    |
|short	 |static	  |strictfp |super     |
|switch	 |synchronized|this     |throw     |
|throws	 |transient	  |try	    |void      |
|volatile|while       |         |          |


Comentarios
--

* Java soporta comentarios de una sola línea o de múltiples líneas, muy similar a C y C++. Todos los caracteres que estén dentro de un comentario son ignorados por el compilador de Java.

    ```bash
    public class MiPrimerPrograma{

       /* Este es mi primer programa de Java.
        * Imprimira Hola Javaficadas como salida.
        * Este es un ejemplo de comentarios multilínea.
        */

        public static void main(String []args){
           // Este es un ejemplo de comentarios en una sóla línea
           /* Este también es un ejemplo de comentarios en una sóla línea. */
           System.out.println("Hola Javaficadas");
        }
    }
    ```

Herencia
--

En Java, las clases pueden derivar de clases. Básicamente si necesitas crear una clase nueva y ya hay una clase que tiene algo del código que requieres, entonces es posible derivar tu clase nueva desde esa que ya existe.

Este concepto te permite reusar los atributos y métodos de la clase existente sin tener que reescribirlos en una nueva clase. En este escenario la clase existente es llamada **superclase** y la que deriva es llamada **subclase**

Interfaces
--

En Java, una interfaz puede definirse como un contrato entre o objetos sobre cómo se comunican entre ellos. Las interfaces juegan un rol vital cuanto viene el concepto de herencia.

Una interfaz define los métodos, ésta debe usar una clase derivada (subclase). La implementación de los métodos es totalmente parte de la subclase.


Slides
--

[Sintaxis básica de Java](https://www.haikudeck.com/javaficadas-education-presentation-7Pimz72zw1)
