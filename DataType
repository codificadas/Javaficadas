 ```bash
 /*
 * Existen dos tipos de datos disponibles en Java: Primitivos y Referencia
 */
package basico;

/**
 * @author Edith
 */
public class TiposDatos {
    public static void main(String[] args) {
         System.out.println("TIPO DE DATOS PRIMITIVOS");
        //PRIMITIVOS
        //Hay ocho tipos de datos primitivos soportados por Java. 
       // 1.- byte    Tipo de datos Byte es un entero de 8 bits.
        byte a_max =127; 
        byte b_min = -128;
        System.out.println("Mi valor byte máximo es: "+a_max);
        System.out.println("Mi valor byte mínimo es: "+b_min);
        
        //2.- short  Tipo de datos Short es un entero de 16 bits.
        short c_max =  32767;
        short d_min = -32768;
        System.out.println("Mi valor short máximo es: "+c_max);
        System.out.println("Mi valor short mínimo es: "+b_min);
        
        //3.-int   Tipo de datos int es un entero de 32 bits
        int e_max =  2147483647;
        int f_min =  -2147483648;
        System.out.println("Mi valor int máximo es: "+e_max);
        System.out.println("Mi valor int mínimo es: "+f_min);
                
        //4.-long   Tipo de datos Long es un entero de 64 bits
        //long g_max = 9223372036854775807; 
        //long h_min = -9223372036854775808;
        long a = 100000; 
        long b =-200000;
        System.out.println("Mi valor long es: "+a+ " y "+b);
         
        //5.-float   El Float es un dato de coma flotante de precisión simple de 32 bits.
        float f1 = 234.5f;
        float f2 = 214748364799999999999999999999999999999.21474836479f;
        System.out.println("Mi valor float es: "+f2+ " y "+f1);
        
        //6.-double  El doble es un dato de coma flotante de doble precisión de 64 bits.
        double d1 = 123.4;
        double d2 = 214748364799999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999.49999999999999999999999999999999999999999999;
        System.out.println("Mi valor double  es: "+d2+ " y "+d1);
        
        //7.- boolean  Boolean representa un bit de información  Sólo hay dos posibles valores: true y false.
        boolean b1= true;
        boolean b2= false;
        System.out.println("Mi valor boleano  es: "+b1);
        System.out.println("Mi valor boleano  es: "+b2);
        
        //8.- char  Char es un carácter Unicode de 16 bits.
        char letra = 'A';
        System.out.println("Mi valor char  es: "+letra);      

        //Tipo de Dato por REFERENCIA 
         System.out.println("TIPO DE DATOS DE REFERENCIA String Y ARRAY");
       //1.- String // Para cadenas 
        String texto1="Primer línea\n";
        String texto2="Segunda línea";
        System.out.println(texto1+" "+texto2);
        
        //Formas de crear un String 
        System.out.println("El primer programa");  //Java crea un objeto de la clase String automáticamente (creación implicita)
        
       //Para crear un string explícitamente escribimos
        String str1= new String("El primer programa");
        String str2="El primer programa";
        
        //Para crear un string nulo se puede hacer de estas dos formas
        String str3="";
        String str4=new String();
        
        //Obtener información acerca del objeto através de las funciones miembro
        
        String str="El primer programa";
        //Obtener la longitud  -- Método length()
        int longitud=str.length();
        System.out.println("La longitud de mi cadena es: "+longitud); 

        //Conocer si un string comienza o termina con un determinado prefijo. -- Método startsWith()  endsWith() --  solo devuelven true o false.
        boolean reStartsWith=str.startsWith("El");
        boolean resEndsWith=str.endsWith("programa");        
        System.out.println("Mi cadena inicia con 'El'?: "+reStartsWith); 
        System.out.println("Mi cadena términa con 'programa'?: "+resEndsWith);
        System.out.println("Mi cadena términa con 'primer'?: "+str.endsWith("primer"));
        
        //Obtener la posición de la primera ocurrencia de una letra. -- Método indexOf()
        int pos=str.indexOf('p');
        System.out.println("La posición de la primer p es ?: "+pos);
        
        //obtener las sucesivas posiciones de la letra. Método indexOf(a,b)-- 
        pos=str.indexOf('p', pos+1);
        System.out.println("La posición de la siguiente p es ?: "+pos);
        
        //Métodos principales o más usados
        //*int length(): devuelve la longitud de la String, incluyendo espacios en blanco.
        String s="CU CU";
        int longitudcadena = s.length();
        System.out.println("Longitud de mi cadena: "+longitudcadena);
        
        //* int indexOf(String str, int indice):
        String mystr="expedicion";
        System.out.println("El indexOf de la 'x' es: "+mystr.indexOf("x", mystr.length()));  
        
        //String replace (char viejoChar, char nuevoChar): cambia el carácter asociado al primer argumento por el que se le pasa al segundo
        String myReplace =s.replace("U", "O");
        System.out.println("Mi cadena es: "+s);
        System.out.println("Mi cadena remplazando la 'U' po la 'O': "+myReplace);

        //Comparación de strings
        System.out.println("COMPARACION ENTRE CADENAS CON == O CON EL MÉTODO equals(cadena)");
        String stra="El lenguaje Java";
        String strb=new String("El lenguaje Java");
        if(stra==strb){
            System.out.println("Los mismos objetos");
        }else{
            System.out.println("Distintos objetos");
        }
        if(stra.equals(strb)){
            System.out.println("El mismo contenido");
        }else{
            System.out.println("Distinto contenido");
        }

        
        //Tipo de dato por referencia ARRAY
        int miArreglo[]= new int[5]; 
        miArreglo[0]=5;
        miArreglo[1]=10;
        miArreglo[2]=15;
        miArreglo[3]=45;
        miArreglo[4]=105;
        //Obtenemos la longitud del arreglo
        System.out.println("La longitud de MI arreglo es "+miArreglo.length); 
        
        //imprimir el arreglo
        for(int i=0; i<5; i++){
            System.out.println("Vector["+i+"]="+miArreglo[i]);            
        }
        
         //Ejercicios-- Practicar usando las siguientes metodos
        
       /* ● String toLowerCase(): devuelve una nueva String con caracteres  en minúsculas.
          ● String toUpperCase(): devuelve una nueva String con caracteres en mayúsculas.
          ● boolean equals(String str): investiga si dos String tienen los mismos caracteres y en el mismo orden. 
            Si es así devuelve true y si no false. 
          ● boolean equalsIgnoreCase(String str): investiga si dos String tienen los mismos caracteres y
             en el mismo orden sin tener en cuenta las mayúsculas. Si es así devuelve true y si no false. 
          ● boolean startsWith(String str): devuelve true si la String sobre la que se aplica comienza por la del argumento; false si esto no ocurre. 
          ● boolean startsWith(String str, int indice): devuelve true si la String sobre la que se aplica
            comienza por la del argumento a partir de un determinado índice asociado al segundo argumento; false si esto no ocurre. 
          ● boolean endsWith(String str): devuelve true si la String sobre la que se aplica acaba en la del argumento; false si esto no ocurre. 
          ● String trim(): devuelve una String en base a la que se le pasa al argumento, pero sin  espacios
            en blanco al principio ni al final. No elimina los espacios en blanco situados entre las palabras.    
          ● String substring(int indiceIni, int indiceFin): devuelve una String obtenida a partir del índice
            inicial incluido y del índice final excluido; es decir, se comporta como un intervalo semiabierto
            [indiceIni, indiceFin). Si el índice final sobrepasa la longitud de la String, lanza una IndexOutOfBoundsException. 
          ● char charAt (int indice): devuelve el carácter asociado al índice que se le pasa como
argumento de la String sobre la que se aplica el método. Si el índice no existe se lanza una
StringIndexOutOfBoundsException que hereda de IndexOutOfBoundsException. */
        
        System.out.println("\nEJERCICIOS");
        
        //Ejemplo con la segunda función de los ejercicios
        String myVariable="El lenguaje Java";
        System.out.println("my string convertido en mayusculas "+myVariable.toUpperCase());
       
       
    }
}
```
