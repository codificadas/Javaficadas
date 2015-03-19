```bash

/*
 * Estructura de seleccción o control multiple
 */
package Estructuras_Control;
import javax.swing.*;

public class Switch {
    public static void main(String[] args) {
        int opcion;
        
        opcion=Integer.parseInt(JOptionPane.showInputDialog(null, "Menú\n1)-Opción 1\n2)-Opción 2\n3)-Opción3"));
       switch(opcion){
            case 1:
                JOptionPane.showMessageDialog(null, "Elegiste caso 1");
                break;
            case 2:
                JOptionPane.showMessageDialog(null, "Elegiste caso 2");
                break;
            case 3:
                JOptionPane.showMessageDialog(null, "Elegiste caso 3");
                break;
            default:
                JOptionPane.showMessageDialog(null, "No es correcta tu seleción");
                break;
       }
       
       /*Ejercicios
       1.- Pida la edad y decir si es mayor de edad
       2.- Pedir un número del 1 al 7 y decir el día de la semana correspondiente
       3.- Determinar si un número es positivo o negativo
       4.- Pedir un número del 1 al 12 y decir el nombre del mes correspondiente
       5.- Pedir un número e indicar si es positivo y menor que 100
       */
           
    }
    
}

```
