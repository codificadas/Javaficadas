Aprendamos a definir clases para crear objetos!
==

En esta sesión retomamos algunos conceptos para explicarlos en código de Java. Iniciamos esta sesión definiendo una vez más que es una **clase** y un **objeto**:

Clases
--

Es el molde/plantilla a partir de la cual podemos crear objetos.

**Ejemplo de la definición de una clase**


```bash
public class Perro{
    //definición de características
    String raza;
    int edad;
    String color;

    public void ladra(){
        //Definición del método ladra
    }

    public void come(){
        //Definición del método come
    }

    public void duerme(){
        //Definición del método duerme
    }
}
```

Variables locales, variables de instancia y variables de clase
--

* **Variables locales:** están definidas sólo en ciertos bloques de código, y sólo pueden ser usadas en esa sección del código.

* **Variables de instancia:** están definidas como parte de la clase/plantilla y se llaman así porque al crear un objeto, se hace una instancia de la clase, esto quiere decir que se crea como una copia de estas variables por cada objeto definido/creado.

* **Variables de clase:** están definidas en la clase, pero no dependen de un objeto en particular para ser usadas. Usadas para definir constantes, esas variables que no cambian su valor durante la ejecución del programa.

**Ejemplo:**

```bash

public class Persona{ //Definición de la clase Persona
   int edad;
   String nombre;
   double peso; //Estas variables son de instancia y están definidas en la clase, y serán las características de cada objeto creado/instanciado
   static double PI = 3.1416; //Esta es la definición de una variable de clase.

   public void saluda() //definición del método saluda
   {
       String nombre = "Erika"; //Esta es la definición de **nombre** como una variable local, ya que está siendo creada dentro de este método y sólo aquí puedo usarla
       System.out.println("Hola, " + nombre);
   }

}

```

Constructores
--

Los constructores son los métodos de inicialización de las variables de instancia.

* Cada clase tiene un constructor.

* Si no se especifica, el compilador de Java ejecuta uno.

* Cada que se crea un objeto el método constructor es invocado.

* Una característica importante es que el método constructor tiene el mismo nombre de la clase.

* Una clase puede tener uno o más métodos constructores definidos.

**Ejemplo:**

```bash
public class Area{
    int base;
    int altura;
    int area;

    public void Area(){ //Definición del método constructor de la clase Area.
        base = 0;
        altura = 0;
        area = 0;
    }
}

```

Objetos
--

En el mundo real los objetos tienen características y comportamientos. En el mundo del software también, sólo que las características las identificaremos en variables y los comportamientos en métodos, los cuales deben estar definidos en la clase.

* Un objeto es creado desde la clase.

* la palabra reservada **new** es usada para crear nuevos objetos.

* **Declaración:** de qué clase será tu objeto? qué nombre tendrá?

* **Instanciación:** usamos la palabra new

* **Inicialización:** llamada al método constructor, para inicializar el nuevo objeto.

Ejemplo:

```bash

Area figura1 = new Area();
```

Acceso a variables de instancia y métodos
--

Luego de crear un objeto, en nuestro caso **figura1** podemos acceder a las variables de instancia y a los métodos disponibles. Aquí ejemplos de cómo lo pueden hacer:

```bash
Area figura1 = new Area(); //creación de un objeto de la clase Area.

figura1.base; //acceso a la variable **base**
figura1.calcularArea(); //Acceso al método **calcularArea()**

```

Ejercicios
--

Hicimos un pequeño ejercicio para imprimir en los valores de una variables.

Practiquen modificando los programas que ya tenemos, agreguen variables, traten de imprimirlas, agreguen commentarios, compilen, ejecuten, resuelvan errores.
Todo es cuestion de práctica.

```bash
public class Persona{

	public static void main(String[] args) {
		String nombre = "Erika";
		int edad = 25;
		double estatura = 1.54;
		double peso = 43.3;

		System.out.println("Bienvenida!");
		System.out.println("Tu nombre es: " + nombre);
		System.out.println("Tu edad es: " + edad + " , estás muy joven!");
		System.out.println("Tu estatura es: " + estatura);
		System.out.println("Tu peso es: " + peso);
	}
}
```

Este es el ejercicio que les presenté mientras explicaba algunos conceptos:

```bash
public class Area{
	int base;
	int altura;
	int area;

	public void Area(){
		base = 0;
		altura = 0;
		area = 0;
	}

	public void calcularArea(){
		base = 6;
		altura = 4;
		area = base * altura;
		System.out.println("El area es: " + area);
	}

	public static void main(String []args) {
    	Area figura1 = new Area();
    	figura1.calcularArea();

    }
}

```

Analicen este ejercicio y hagan la relación con los conceptos vistos pero en el código.

Slides
--

[Aprendamos a definir clases para crear objetos!](https://www.haikudeck.com/javaficadas-education-presentation-l3u9YwMDPr)