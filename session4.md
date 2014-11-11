Tipos de datos, modificadores y variables
==

En esta sesión recodamos algunos conceptos y los analizamos en código de Java. Luego practicamos con algunos ejercicios:

Tipos de datos
--

Las variables son espacios de memoria reservados para almacenar datos. Esto significa que cuando creamos una variable, estamos reservando espacio en memoria.

**hay dos tipos de datos disponibles en Java:**

* Tipos de datos primitivos

* Tipos de datos compuestos

Tipos de datos primitivos
--

* **byte**

* **short**

* **int**

* **long**

* **float**

* **double**

* **boolean**

* **char**

Tipos de datos compuestos
--

* **array:**

* **String:**


Tipos de modificadores
--

**Modificadores de acceso**

Java provee un numero de modificadores de acceso para acceder a clases, variables, métodos y constructores:

* Visible sólo para la clase (private).

* Visible para el mundo (public).

* Visible para los paquetes y todas las subclases (protected).


Tipos de variables
--

* **Variables locales:** están definidas sólo en ciertos bloques de código, y sólo pueden ser usadas en esa sección del código.

* **Variables de instancia:** están definidas como parte de la clase/plantilla y se llaman así porque al crear un objeto, se hace una instancia de la clase, esto quiere decir que se crea como una copia de estas variables por cada objeto definido/creado.

* **Variables de clase:** están definidas en la clase, pero no dependen de un objeto en particular para ser usadas. Usadas para definir constantes, esas variables que no cambian su valor durante la ejecución del programa.


Ejercicios
--

Hicimos un pequeño ejercicio para pedir al usuario la base y la altura para calcular el área de un cuadrado o rectángulo, experimentamos los accesos de la variables dependiendo del lugar donde fueron declaradas e hicimos uso de una librería de Java que nos permite introducir datos desde el teclado.

Practiquen modificando los programas que ya tenemos, agreguen variables, traten de imprimirlas, agreguen commentarios, compilen, ejecuten, resuelvan errores.
Todo es cuestion de práctica.

```bash
import java.util.Scanner;

public class Area{
	int base;
	int altura;
	int area;

	public void Area(){
		base = 0;
		altura = 0;
		area = 0;
	}

	public void calcularArea(int base, int altura){

		area = base * altura;
		System.out.println("El area es: " + area);
	}

	public static void main(String []args) {
    	Scanner input = new Scanner(System.in); //opens a scanner, keyboard
		System.out.print("Proporciona la base: "); //prompt the user
		int base = input.nextInt(); //store the input from the user
		System.out.print("Proporciona la altura: "); //prompt the user
		int altura = input.nextInt(); //store the input from the user


    	Area figura1 = new Area();
    	figura1.calcularArea(base, altura);


    }
}

```

Investiguen un poco más sobre los conceptos vistos para que amplien su conocimiento :)

Slides
--

[Tipos de datos, modificadores y variables!](https://www.haikudeck.com/javaficadas-uncategorized-presentation-5xHCKLpOE8)