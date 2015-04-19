Interfaces
==

Como sabemos en Java no existe la herencia múltiple, pudiendo heredar solamente de una clase, las Interfaces son una gran herramienta para simular este concepto.

Para empezar debemos saber que una Interface es una Clase completamente Abstracta, como regla, sabemos que las clases abstractas poseen como mínimo un método abstracto, pero hablando de una interface, todos sus métodos tienen que serlo.

Cuando creamos un Interface, lo que hacemos es definir lo que la clase que la implemente podrá hacer, pero no indicamos la forma en que lo hará.

En java se usa la palabra reservada implements para indicar que implementamos una interface, la estructura general de una clase que implementa una interface es la siguiente.
```bash
interface InterfacePrincipal {
  
 public void metodoAbstracto();
  
 public String otroMetodoAbstracto();
  
}
 
public class Principal implements InterfacePrincipal,otraInterface,otraMas{
 
 public void metodoAbstracto() {
  /**Implementación definida por la clase concreta*/
 }
 
 public String otroMetodoAbstracto() {
  /**Implementación definida por la clase concreta*/
  return "retorno";
 }
 
 public void metodoAbstractoDeOtraInterface() {
  /**Implementación definida por la clase concreta*/
 }
 
 public void metodoAbstractoDeOtraMas() {
  /**Implementación definida por la clase concreta*/
 }
}
```
**Características de las Interfaces**
odos los métodos de una interfaz son implícitamente public abstract, no es necesario especificarlo en la declaración del mismo.
Todas las variables y atributos de una interfaz son implícitamente constantes (public static final), no es necesario especificarlo en la declaración del misma
Los métodos de una interfaz no pueden ser: static, final, strictfp ni native.
Una interfaz puede heredar (extends) de una o más interfaces.
Una interfaz no puede heredar de otro elemento que no sea una interfaz.
Una interfaz no puede implementar (implements) otra interfaz.
Una interfaz debe ser declarada con la palabra clave interface.
Los tipos de las interfaces pueden ser utilizados polimórficamente.
Una interfaz puede ser public o package (valor por defecto). 
Los métodos toman como ámbito el que contiene la interfaz.
```bash
/**Las interfaces Heredan de cualquier cantidad de interfaces usando extends*/
 public interface PrimerInterface extends SegundaInterface, TercerInterface
{
    
/**Las siguientes son declaraciones validas para los atributos*/
   int ATRIBUTO1= 5;
   public int ATRIBUTO2= 5;
   public static int ATRIBUTO3= 5;
   public final int ATRIBUTO4= 5;
   static int ATRIBUTO5= 5;
   final int ATRIBUTO6= 5;
   static final int ATRIBUTO7= 5;
   public static final int ATRIBUTO8= 5;
 
/**Las siguientes son declaraciones validas para los métodos*/
   void metodoPrimerInterface1();
   public void metodoPrimerInterface2();
   abstract void metodoPrimerInterface3();
   public abstract void metodoPrimerInterface4();
 }
```
Hay que tener presente algo, ya vimos que tanto para clases Abstractas como para Interfaces la herencia es permitida, pero por ejemplo para este tipo componentes, si una interface hereda de otra, esta no está obligada a implementar los métodos que posee la Interface padre, ya que la implementación tanto de los métodos de la clase padre como de la interface que los hereda depende de la clase concreta que implemente dicha interface........ este principio también aplica a las clases Abstractas, si una clase abstracta implementa una interface, los métodos de esta no necesariamente se deben implementar en la clase Abstracta, pero si se tienen que implementar en la clase concreta que herede de la clase abstracta.

**¿Cuando Utilizarlas?**

Su uso esta muy ligado al concepto de herencia y cumple el mismo principio que aplicamos al usar clases abstractas, lo que buscamos es establecer un mecanismo donde podamos compartir características comunes entre clases diferentes, además al igual que con clases abstractas nos aseguramos que los métodos y atributos solo están disponibles para las clases que las implementen.

http://1.bp.blogspot.com/-fYmNue2Au68/UaJhBGl71SI/AAAAAAAABKM/VSUL9cx-aUA/s1600/interfaces.jpg

En el diagrama de clases vemos 6 clases concretas y 2 interfaces, las clases Humano y Animal son clases padre de "Hombre y Mujer" y "Perro y Gato" respectivamente, ahora bien, Humano y Animal son clases diferentes con un árbol de herencia marcado, pero ambas poseen características comunes que podemos usar por medio de la interface AccionesGeneral.

Podemos decir que tanto un Hombre como un Gato pueden caminar, usando para esto el método desplazarse(), donde cada clase dará el mecanismo de desplazamiento, por ejemplo el hombre lo hace en 2 piernas mientras que el gato en 4 patas (o dependiendo de la forma como lo realicen), y este mismo concepto puede aplicarse a los otros métodos enmarcados en la Interface AccionGeneral que tanto Humanos como Animales comparten.

También tenemos la interface AccionesHumano para esos métodos o características que solo son aplicables a los humanos y que tanto Hombre como Mujer pueden adoptar, así la clase Humano podrá simular la herencia múltiple al implementar las 2 interfaces mencionadas.

Y listo!!! Básicamente esta es la lógica detras de las Interfaces
