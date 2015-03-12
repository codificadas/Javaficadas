 ```bash
 package ENUMS;

/**
 * @author Edith
 */
public class ClassEnum {
    //Creamos un enum más detallado cada tipo de madera tiene un color y un peso
    public enum TipoDeMadera {
        ROBLE ("Castaño verdoso", 800), //Separamos con comas
        CAOBA ("Marrón oscuro", 770),
        NOGAL("Marrón rojizo", 820),
        CEREZO ("Marrón cereza", 790),
        BOJ ("Marrón negruzco", 675);  //Cuando terminamos cerramos con ;

        //Campos tipo constante   
        private final String color; //Color de la madera
        private final int pesoEspecifico; //Peso específico de la madera

        /**
         * Constructor. Al asignarle uno de los valores posibles a una variable del tipo enumerado el constructor asigna 
            automáticamente valores de los campos
         */ 
        TipoDeMadera (String color, int pesoEspecifico) { 
            this.color = color;
            this.pesoEspecifico = pesoEspecifico;
        } //Cierre del constructor

        //Métodos de la clase tipo Enum
        public String getColor() { return color; }
        public int getPesoEspecifico() { return pesoEspecifico; }
    } //Cierre del enum
    
    
     public static void main (String[ ] Args) {
         //Cramos una variable referenciada al enum y obligamos a qie tome solo los valores del enum
       TipoDeMadera maderaUsuario1 = TipoDeMadera.ROBLE;
       System.out.println ("La madera elegida por el usuario es " + maderaUsuario1.toString() + "\ncon un color " +
       maderaUsuario1.getColor() + " y con un peso específico de " + maderaUsuario1.getPesoEspecifico() + " kg/m3");
 
       //Imprimimos todo nuestro enum
       System.out.println ("TODO MI ENUM");
        for (TipoDeMadera tmp: TipoDeMadera.values() ) {
            System.out.println (tmp.toString() + "  pesa " + tmp.getPesoEspecifico() + " kg y su color es "+tmp.getColor());
        }
    } 
    
}
 ```
