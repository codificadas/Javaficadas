Estructuras de Control
==
Las estructuras de control determinan la secuencia de ejecución de las sentencias de un programa. 
Se dividen en tres categorías:

- Secuencial

- Condicional o selectiva

- Iterativa o repetitiva

Secuencial
--

La estructura secuencial está formada por una sucesión de instrucciones que se ejecutan en orden una a continuación de la otra.

```bash
public class Estructura_Secuencial {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double numero1, numero2;
        System.out.println("Introduce el primer número:");
        numero1 = sc.nextDouble();
        System.out.println("Introduce el segundo número:");
        numero2 = sc.nextDouble();
        System.out.println("Números introducido: " + numero1 + "  " + numero2);
        System.out.println(numero1 + " + " + numero2 + " = " + (numero1+numero2));
        System.out.println(numero1 + " - " + numero2 + " = " + (numero1-numero2));
        System.out.println(numero1 + " * " + numero2 + " = " + numero1*numero2);
    }
}

```
Condicional o selectiva
--
La estructura condicional determina si se ejecutan unas instrucciones u otras según se cumpla o no una determinada condición.
Existen dos estructuras condicionales.
- if_else

- switch

Estructura del if
```bash
    if(expresión_booleana){
      instrucción 1
      instrucción 2
      ....... 
    }
```

Estructura del switch. Se utiliza para seleccionar una de entre múltiples alternativas.
```bash
switch (expresión){
    case valor 1:
      instrucciones;
    break;
    case valor 2:
      instrucciones;
    break;
      · · ·
    default:
      instrucciones;
}
```

Iterativa o repetitiva
--

- for

- while

- Do while

Slides
--

[Estructuras de control](https://www.haikudeck.com/javaficadas-education-presentation-SfsIP7LjoV)

Ejemplos
--

[Estructura secuencial](https://github.com/codificadas/Javaficadas/blob/master/EstructuraSecuencial.md)

[if simple](https://github.com/codificadas/Javaficadas/blob/master/ifsimple.md)

[if doble](https://github.com/codificadas/Javaficadas/blob/master/ifdoble.md)

[if multiple](https://github.com/codificadas/Javaficadas/blob/master/ifmultiple.md)

[if anidado](https://github.com/codificadas/Javaficadas/blob/master/ifanidado.md)

[if sustitución](https://github.com/codificadas/Javaficadas/blob/master/Ifsustitucion.md)

[switch ejemplo 1](https://github.com/codificadas/Javaficadas/blob/master/EstructuraSelectiva_SWITCH.md)

[switch ejemplo 2](https://github.com/codificadas/Javaficadas/blob/master/EstSwitch_showmessageDialog.md)
