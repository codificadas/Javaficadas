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
