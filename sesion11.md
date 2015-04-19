Clases Abstractas
==

La abstracción permite resaltar lo mas representativo de algo sin importar los detalles.

Una clase Abstracta es similar a una clase normal, poseen nombre, atributos y métodos pero para que una clase sea abstracta la condición es que al menos uno de sus métodos sea abstracto. Por ejemplo.

```bash
public abstract class Principal{
 
    /**Método concreto con implementación*/
    public void metodoConcreto(){
       ...............
       ............... 
    }
 
    /**Método Abstracto sin implementación*/
    public abstract void metodoAbstracto();
   
}
 
class subClase extends Principal{
 
 @Override
 public void metodoAbstracto() {
  /**Implementación definida por la clase concreta*/
 }
  
}
```

**Caracteristicas de una Clase Abstracta**
Una clase Abstracta No puede ser instanciada (no se pueden crear objetos directamente - new ), solo puede ser heredada. 
Si al menos un método de la clase es abstract, esto obliga a que la clase completa sea definida abstract, sin embargo la clase puede tener el resto de métodos no abstractos.
Los métodos abstract no llevan cuerpo (no llevan los caracteres {}). 
La primer subclase concreta que herede de una clase abstract debe implementar todos los métodos de la superclase.

**¿Cuando Utilizarlas?**
Al trabajar clases y métodos abstractos, no solo mantenemos nuestra aplicación mas organizada y fácil de entender sino que también al no poder instanciar una clase abstracta nos aseguramos de que las propiedades especificas de esta, solo estén disponibles para sus clases hijas.

Con las Clases Abstractas lo que hacemos es definir un proceso general que luego sera implementado por las clases concretas que hereden dichas funcionalidades.

Veamos una clase Abstracta Instrumento, la cual posee una propiedad tipo y un método abstracto tocar(), las clases hijas Guitarra, Saxofon y Violin.

Todos los instrumentos musicales se pueden tocar, por ello creamos este método abstracto, ya que es un proceso común en todos los instrumentos sin importar el detalle de como se tocan, pues sabemos que una guitarra no se toca de la misma manera que el saxofón, así al heredar de la clase Instrumento, todas sus clases hijas están obligadas a implementar este método y darle la funcionalidad que le corresponda.

```bash
/**
 * Clase Abstracta Instrumento
 */
abstract class Instrumento{ 
  
 public String tipo;
  
 public abstract void tocar();
}
 
/**
 * Clase Concreta Guitarra, hija de Instrumento
 */
class Guitarra extends Instrumento {
 
 public Guitarra(){
  tipo="Guitarra";
 }
  
 public void tocar() {
  System.out.println("Tocar La Guitarra");
 }
}
 
/**
 * Clase Concreta Violin, hija de Instrumento
 */
class Violin extends Instrumento {
 
 public Violin(){
  tipo="Violin";
 }
  
 public void tocar() {
  System.out.println("Tocar El violin");
 }
}
 
/**
 * Clase Concreta Saxofon, hija de Instrumento
 */
class Saxofon extends Instrumento {
 
 public Saxofon(){
  tipo="Saxofon";
 }
  
 public void tocar() {
  System.out.println("Tocar el Saxofon");
 }
}
 
public class Principal {
  
 public static void main(String arg[]){
  /**Objeto miGuitarra de tipo Instrumento */
  Instrumento miGuitarra= new Guitarra();
  System.out.println("Instrumento : "+miGuitarra.tipo);
  miGuitarra.tocar();
  System.out.println();
  /**Objeto miSaxofon de tipo Instrumento */
  Instrumento miSaxofon= new Saxofon();
  System.out.println("Instrumento : "+miSaxofon.tipo);
  miSaxofon.tocar();
  System.out.println();
  /**Objeto miViolin de tipo Instrumento */
  Instrumento miViolin= new Violin();
  System.out.println("Instrumento : "+miViolin.tipo);
  miViolin.tocar();
   
 }
 
}
```
cada una de las clases concretas implementan el método tocar() y le dan la funcionalidad dependiendo de como se toque el instrumento, también en cada constructor de las clases definimos el tipo, pero si nos fijamos bien en las clases concretas no tenemos la variable tipo declarada, pues estamos usando la variable heredada de la clase Instrumento.

Hay que tener en cuenta que cuando trabajamos con clases Abstractas, estas solo pueden ser heredadas mas no instanciadas, esto quiere decir que no podemos crear objetos directamente de estas clases.

Como vemos en la clase Principal tenemos la lógica para ejecutar nuestra aplicación y usamos el concepto de Polimorfismo para crear los objetos de tipo Instrumento por medio de sus clases Hijas, pero en ningún momento creamos un objeto como instancia directa de la clase abstracta.
