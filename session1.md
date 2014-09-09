Introducción a Java
===
En esta primera sesión haremos una introducción al lenguaje, un poco de historia y sus principales características.


Java
--

James Gosling inició el proyecto del lenguaje Java en Junio de 1991 para uso de sus proyectos. Inicialmente fue llamado Oak, luego Green y al final se renombró como Java.

Java es un lenguaje de programación de alto nivel desarrollado por Sun Microsystems y publicado en 1995. Java se ejecuta en una gran variedad de plataformas, tales como Windows, Mac OS, y en las versiones de UNIX.

Java posee diferentes versiones que pueden ser usadas dependiendo de la plataforma de desarrollo. Tales como Java SE (Standard Edition), Java EE (Enterprise Edition) and Java ME (Micro Edition). Java garantiza ser **escrito una vez, ejecutado donde sea**.


Características
--

* **Orientado a objetos:** En Java, todo es un Objeto.

* **Plataforma independente:** A diferencia de muchos otros lenguajes de programación, incluyendo C y C ++, cuando Java es compilado, no se compila en la máquina específica de la plataforma, tampoco en la plataforma de código byte independiente. Este código byte se distribuye a través de Internet y es interpretado por la máquina virtual (JVM) en la que la plataforma se está ejecutando.

* **Simple:** Java está diseñado para ser fácil de aprender. Si entiendes el concepto básico de POO, Java te será fácil de dominar.

* **Seguro:** Con la característica de seguridad de Java que permite desarrollar sistemas de manipulación libres libres de virus. Técnicas de autenticación se basan en el cifrado de clave pública.

* **Arquitectura neutral:** El compilador de Java genera un formato de archivo de arquitectura neutral que hace que el código compilado sea ejecutable en muchos procesadores, con la presencia del sistema de ejecución de Java.

* **Portable:** Siendo arquitectónico-neutral y no tener aspectos dependientes de implementación. El compilador de Java está escrito en ANSI C con un límite portabilidad limpio, que es un subconjunto POSIX.

* **Robusto:** Java hace un esfuerzo por eliminar las situaciones propensas a errores haciendo hincapié principalmente en la comprobación de errores en tiempo de compilación y en tiempo de ejecución.

* **Multihilos (Multithreaded)**: Con la característica de multiproceso de Java es posible escribir programas que pueden hacer muchas tareas simultáneamente. Esta característica de diseño permite a los desarrolladores construir aplicaciones interactivas que se ejecutan sin problemas.

* **Interpretado:** Java byte code se traduce sobre la marcha para instrucciones nativas de la máquina y no se almacena. El proceso de desarrollo es más rápido y analítico ya que el enlace es un proceso incremental y ligero.

* **Alto rendimiento:** Con el uso de los compiladores Just-In-Time, Java permite un alto rendimiento.

* **Distribuído:** Java está diseñado para el entorno distribuido de internet.

* **Dinámico:** Java es considerado por ser más dinámico que C o C++ ya que está diseñado para adaptarse a un entorno en evolución. Los programas de Java pueden llevar una extensa cantidad de información en tiempo de ejecución que puede ser utilizada para verificar y determinar los accesos a los objetos en tiempo de ejecución.


Setup
--

Herramientas que necesitamos:

* Editor de textos: [Descarga Textmate aquí](http://www.sublimetext.com/)

* Java! [Descarga e instala Java aquí](http://www.java.com/en/download/help/download_options.xml)


Probemos si funcionó!
--

1. Crear una carpeta llamada programas de Java

2. Abrir Textmate

3. Copiar el siguiente código de Java:

    ```bash
    public class MiPrimerPrograma {

        public static void main(String []args) {
           System.out.println("Hola Javaficadas!");
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


Slides
--

[Introducción a Java](https://www.haikudeck.com/javaficadas-education-presentation-2wxTF3Fqb7)