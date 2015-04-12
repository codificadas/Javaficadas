Operaciones con Arreglos
==
En la sesión anterior miramos el uso de arreglos en esta ocasión trabajaremos con ellos.
- **Insertar**
```bash
void Insertar(){
         for(int i=0; i<4; i++){
             vector[i]=Integer.parseInt(JOptionPane.showInputDialog("Ingresa valor en vector["+i+"]"));
         }
         menu();
}
```
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
```bash
Ya tenemos nuestros metodos pero qué necesitamos para utilizarlos?
Lo  primero es crear un método adicional con las opciones para que el usuario pueda elejir la que desea.

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

Agregar otro método para sumar los valores del arreglo con otro arreglo de la misma dimención.
