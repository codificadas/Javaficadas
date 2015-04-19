Operaciones con Arreglos
==
En la sesión anterior se trabajo con los arreglos,  miramos como crear e instanciarlos y asignarles los valores directamente, pero cómo podemos pedirle al usario que ingrese los valores y cómo los guardamos en el arreglo? 

Bueno hay muchas forma de hacerlo aquí les mostraremos una. Crearemos un programa el cual estará compuesto por 5 funciones Insertar, Mostrar, Modificar, Eliminar y menu.


Iniciemos, lo primero que debemos de hacer es crear una función en la que realizaremos la solicitud al usuario para que ingrese los valores al arreglo.

- **Insertar**
```bash
void Insertar(){
         for(int i=0; i<4; i++){
             vector[i]=Integer.parseInt(JOptionPane.showInputDialog("Ingresa valor en vector["+i+"]"));
         }
         menu();
}
```
Nuestra función Insertar esta sencilla, lo que realizamos simplemente es hacer un recorrido con el ciclo For a nuestro arreglo  el cual esta compuesto de 4 posiciones y en nuestro vector o arreglo ir guardando el valor que el usuario ingrese.

Después de recorrer el arreglo y guardar todos los valores regresamos al menú.

Nuestro segundo método es Mostrar el cual nos mostrara los valores del arreglo, revisemos el código, es practicamente lo mismo que el anterior, realizamos un ciclo For para recorrer el arreglo y mostrar los valores que contiene.

- **Mostrar**
```bash
 void Mostrar(){
         for(int i=0; i<4; i++){
             JOptionPane.showMessageDialog(null, "El valor en vector["+i+"] = "+vector[i]);
         }
         // Otra opción para mostrar
//         JOptionPane.showMessageDialog(null, "El valor en vector[0] = "+vector[0]+
//                 "\nEl valor en vector[1] = "+vector[1]+
//                 "\nEl valor en vector[2] = "+vector[2]+
//                 "\nEl valor en vector[3] = "+vector[3]);
         menu();
    }
```

En ocaciones necesitamos modificar los valores que ingresamos pero, cómo podemos hacerlo? Bien de una forma muy sencilla lo primero que necesitamos es conocer la posición en la cual se encuentra nuestro elemento que queremos modificaar, si la posición es correcta pedimos que ingresen el nuevo valor y lo guardamos de lo contrario debemos de indicarle que la posición no existe.
- **Modificar**
```bash
void Modificar(){
        opcion=Integer.parseInt(JOptionPane.showInputDialog("Posición a modificar!!"));
        if (opcion>=4){
            JOptionPane.showMessageDialog(null, "Esa posición no existe\nIngresa una posición correcta");
            Modificar();
        }else{
            vector[opcion]=Integer.parseInt(JOptionPane.showInputDialog("Ingrese el nuevo valor en vector["+opcion+"]"));
            menu();
        }
    }
```
Ahora bien, esta función solo funciona para modificar de uno por uno y proporcionando una posición pero si necesitaramos modificar todos los valores del arreglo tendriamos que hacerlo algo similar a los métodos anteriores con un ciclo For.


Nuestro siguiente metodo es similar al  anterior. Analicenlo y digame qué hacemos en él?

- **Eliminar**
```bash
void Eliminar(){
         opcion=Integer.parseInt(JOptionPane.showInputDialog("Posición a eliminar!!"));
        if (opcion>=4){
            JOptionPane.showMessageDialog(null, "Esa posición no existe\nIngresa una posición correcta");
            Eliminar();
        }else{
            vector[opcion]=0;
             JOptionPane.showMessageDialog(null, "se elimino el vector["+opcion+"]");
            menu();
        }
         
    }
```
Ya tenemos nuestros metodos pero qué necesitamos para utilizarlos?
Lo  primero es crear un método adicional con las opciones para que el usuario pueda elegir la que desea.
```bash

void menu(){
        opcion=Integer.parseInt(JOptionPane.showInputDialog("MENÚ\n\n1)-Ingresar\n2)-Mostrar\n3)-Modificar\n4)-Eliminar\n5)-Salir"));
        
        switch(opcion){
            case 1:
                Insertar();
                break;
             case 2:
                Mostrar();
                break;
             case 3:
                Modificar();
             case 4:
                Eliminar();            
             case 5:
                JOptionPane.showMessageDialog(null, "Adios");
                break;
            default:
                JOptionPane.showMessageDialog(null, "No se eligio ninguna opción anterior");
                break;
        }
    }
```

ok, ya esta pero y que más necesitamos?

pista 1.- Crear el arreglo.

pista 2.- por qué nos marca error en opcion.

pista 3.- Falta el método main, y que debo de hacer en él?.

-Ejercicios:

Modificar el metodo de insertar para que los datos se ingresen con un random.

Crear un metodo nuevo o modificar  el metodo de Modificar para actualizar todos los valores.

Agregar otro método para sumar los valores del arreglo con otro arreglo de la misma dimención.

Otro ejemplo: [Ver](https://github.com/codificadas/Javaficadas/blob/master/operacionesArrays.md)
