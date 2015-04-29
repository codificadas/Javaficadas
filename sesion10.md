Herencia
==

La herencia en java representa lo que conocemos de herencia en el mundo real, básicamente mediante esta obtenemos las características o rasgos comunes de nuestros padres o abuelos, en java es el mismo enfoque permitiendo la creación de nuevas clases basadas en clases ya existentes, con las cuales podemos obtener las características de las clases padres, heredando campos, atributos, métodos o funcionalidades.

En Java solo se puede heredar de una sola clase padre y se representa mediante la palabra **extends**

```bash
public class Animal{
 public String tamaño;
  
 public void comer(){
  /**Comportamiento.....*/
 }
}

class Perro extends Animal{
  
 public int dientes;
 
 public void correr(){
  /**Comportamiento.....*/
 }
}
 
class Paloma extends Animal{
   
 public int plumas;
 
 public void volar(){
  /**Comportamiento.....*/
 }
}
```
**NOTA:** Se debe tener claro que solo se puede heredar de una sola clase pues el lenguaje no permite la Herencia múltiple (En Java por defecto todas las clases heredan de la clase Object, es decir, esta es la clase Padre de todas las clases en Java).

Conociendo el concepto de clases y objetos vamos a asumir que necesitamos construir una aplicación sobre los diferentes tipos de vehículos existentes, pero para esto necesitamos clasificarlos, en este caso trabajaremos con vehículos acuáticos y aéreos. Cuál es el factor común de estos 2 tipos?

R.- Ambos son vehículos. Entonces nuestra clase principal de nuestro sistema sera la clase Vehiculo.

Ahora bien  sabemos que un barco o un avión son vehículos, pero ambos tienen características propias que los diferencian, entonces tenemos que pensar de forma general para poder definir un correcto árbol de herencia, por eso podemos decir que un barco además de descender de un vehículo, también desciende del tipo de vehículos Acuáticos los cuales tienen un conjunto de características comunes para cualquier vehículo acuático (sin olvidar que cada vehículo acuático puede tener sus características propias) y de la misma forma un avión desciende del tipo de vehículos Aéreos, tenemos así nuestras clases Acuatico y Aereo que a su vez descienden de la clase Vehiculo, y son padres de cualquier vehículo en su jerarquía.

Al final tendriamos definida la Clase Padre Vehiculo, la cual tiene como hijas a las clases Acuatico y Aereo, estas a su vez son clases Padre de Barco, Velero, Avion y Helicoptero que a la vez son nietas de Vehiculo.

Con esto ya tenemos una jerarquía de herencia definida, esto quiere decir que por ejemplo la clase Avion puede usar el método volar() de la clase Aereo, así como también usar el método transportar() de la clase Vehiculo, pues se encuentra en el mismo árbol de herencia, sin embargo no puede usar el método navegar() de la clase Acuatico, ya que no es de tipo Acuatico.

Teniendo nuestro diagrama definido, vamos a aplicar el concepto en Java.

**Clase Padre**
```bash
public class Vehiculo {
  
 public int modeloVehiculo;
  
 public String nombreVehiculo="";
  
 public String transportar(){
  return "Metodo transportar de clase Vehiculo";
 }
}
```
**SubClase Acuatico extiende de Vehiculo**
```bash
public class Acuatico extends Vehiculo{
  
 public String nombreAcuatico="";
  
 public String navegar(){
  return "Método navegar de clase Acuatico";
 }
 
}
```
**SubClase Aereo extiende de Vehiculo**
```bash
public class Aereo extends Vehiculo {
  
 public String nombreAereo="";
  
 public String volar(){
  return "Método volar desde clase Aereo";
 }
}
```
**SubClase Barco extiende de Acuatico**
```bash
public class Barco extends Acuatico {
  
 public String prenderMotor(){
   return "Método prenderMotor en clase Barco";
 }
}
```
**SubClase Velero extiende de Acuatico**
```bash
public class Velero extends Barco{
  
 public String izarVelas(){
  return "Método izarVelas en clase Velero";
 }
}
```
**SubClase Avion extiende de Aereo**
```bash
public class Avion extends Aereo{
  
 public String bajarTrenDeAterrizaje(){
  return "Método bajarTrenDeAterrizaje en clase Avion";
 }
}
```
**SubClase Helicoptero extiende de Aereo**
```bash
public class Helicoptero extends Aereo{
  
 public String encenderHelices(){
  return "Método encenderHelices en clase Helicoptero";
 }
}
```
Como vemos seguido del nombre de la clase se tiene la palabra extends la cual indica que se extiende o hereda de la clase definida, así mismo todas las clases tienen al menos un método que representa la característica propia de la clase, para las clases hijas ese método define el proceso que solo ellas pueden realizar, para las clases padre, ese método define el proceso que es común o general para las clases hijas.

Ya tenemos todas las clases ahora haremos el llamado a los métodos tanto propios como heredados de las clases padres.
```bash
public class Principal {
 
 /**
  * @param args
  */
 public static void main(String[] args) {
 System.out.println("-------------------<< Clase Padre Vehiculo >>-----------------------");
 Vehiculo miVehiculo = new Vehiculo();
 miVehiculo.nombreVehiculo="El Gran Transportador";
 System.out.println("usando miVehiculo, nombreVehiculo : "+miVehiculo.nombreVehiculo);
 System.out.println("usando miVehiculo llama a: "+miVehiculo.transportar());
 System.out.println("--------------------------------------------------------------------");
 System.out.println();
  
 System.out.println("----------<< SubClase hija Acuatico Extiende de Vehiculo >>---------");
 Acuatico miAcuatico= new Acuatico();
 miAcuatico.nombreVehiculo="El Navegante";
 System.out.println("usando miAcuatico, nombreVehiculo : "+miAcuatico.nombreVehiculo);
 System.out.println("usando miAcuatico llama a : "+miAcuatico.transportar());
 System.out.println("usando miAcuatico llama a : "+miAcuatico.navegar());
 System.out.println("---------------------------------------------------------------------");
 System.out.println();
  
 System.out.println("-----<< SubClases hijas extienden de la Subclase Padre Acuatico>-----");
 Barco miBarco=new Barco();
 miBarco.nombreVehiculo="Titanic";
 System.out.println("usando miBarco, nombreVehiculo : "+miBarco.nombreVehiculo);
 System.out.println("usando miBarco llama a : "+miBarco.transportar());
 System.out.println("usando miBarco llama a : "+miBarco.navegar());
 System.out.println("usando miBarco llama a : "+miBarco.prenderMotor());
 System.out.println();
  
 Velero miVelero=new Velero();
 miVelero.nombreVehiculo="Tormenta";
 System.out.println("usando miVelero, nombreVehiculo : "+miVelero.nombreVehiculo);
 System.out.println("usando miVelero llama a : "+miVelero.transportar());
 System.out.println("usando miVelero llama a : "+miVelero.navegar());
 System.out.println("usando miVelero llama a : "+miVelero.izarVelas());
 System.out.println("---------------------------------------------------------------------");
  
 System.out.println("----------<< SubClase hija Aereo Extiende de Vehiculo >>---------");
 Aereo miAereo= new Aereo();
 miAereo.nombreVehiculo="El Volador";
 System.out.println("usando miAereo, nombreVehiculo : "+miAereo.nombreVehiculo);
 System.out.println("usando miAereo llama a : "+miAereo.transportar());
 System.out.println("usando miAereo llama a : "+miAereo.volar());
 System.out.println("---------------------------------------------------------------------");
 System.out.println();
  
 System.out.println("-----<< SubClases hijas extienden de la Subclase Padre Aereo >-----");
 Avion miAvion=new Avion();
 miAvion.nombreVehiculo="El Condor";
 System.out.println("usando miAvion, nombreVehiculo : "+miAvion.nombreVehiculo);
 System.out.println("usando miAvion llama a : "+miAvion.transportar());
 System.out.println("usando miAvion llama a : "+miAvion.volar());
 System.out.println("usando miAvion llama a : "+miAvion.bajarTrenDeAterrizaje());
 System.out.println();
  
 Helicoptero miHelicoptero=new Helicoptero();
 miHelicoptero.nombreVehiculo="El lobo del Aire";
 System.out.println("usando miHelicoptero, nombreVehiculo : "+miHelicoptero.nombreVehiculo);
 System.out.println("usando miHelicoptero llama a : "+miHelicoptero.transportar());
 System.out.println("usando miHelicoptero llama a : "+miHelicoptero.volar());
 System.out.println("usando miHelicoptero llama a : "+miHelicoptero.encenderHelices());
 System.out.println("---------------------------------------------------------------------");
 System.out.println();
  
 System.out.println("--<< Propiedad de la clase Vehiculo usada por todas las clases Hijas >--");
 System.out.println("nombre Vehiculo :"+miVehiculo.nombreVehiculo);
 System.out.println("nombre Acuatico :"+miAcuatico.nombreVehiculo);
 System.out.println("nombre Aereo :"+miAereo.nombreVehiculo);
 System.out.println("nombre Barco :"+miBarco.nombreVehiculo);
 System.out.println("nombre Velero :"+miVelero.nombreVehiculo);
 System.out.println("nombre Avion :"+miAvion.nombreVehiculo);
 System.out.println("nombre Helicoptero :"+miHelicoptero.nombreVehiculo);
 System.out.println("---------------------------------------------------------------------");
  
 }
}
```

Como vemos podemos acceder a los diferentes métodos desde otras clases, y si nos fijamos bien podemos identificar que siempre usamos la misma propiedad nombreVehiculo de la clase Vehiculo, lo hicimos usando objetos diferentes por tal razón el valor de la propiedad depende del asignado por cada objeto

**Ejercicios:**
https://github.com/codificadas/Javaficadas/blob/master/herencia_ejercicios.md
