<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 

### Actividad: Ejecicios de métodos en Java

**Implementar los siguientes métodos:**

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

### 1

```java
/**
 * numeros
 */
public class numeros {
    public static void main(String[] args) {
        numeros num_dev = new numeros();
        int result = num_dev.devolver(20, 100);
        System.out.println("El número más grande es: " + result);
    }



    public int devolver(int num1, int num2) {

        if (num1 < num2) {
            return num2;
        } else {
            return num1;
        }
    }

}
```

### 2

```java
public class vocales {
    public static void main(String[] args) {
        String cadena = "cadena de texto para contar";
        int contadorVocales = contarVocales(cadena);
        System.out.println("El número de vocales en la cadena es: " + contadorVocales);
    }

    public static int contarVocales(String cadena) {
        int contador = 0;
        for (int i = 0; i < cadena.length(); i++) {
            char caracter = cadena.charAt(i);
            
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u' ||
                    caracter == 'A' || caracter == 'E' || caracter == 'I' || caracter == 'O' || caracter == 'U') {
                contador++;
            }
        }
        return contador;
    }
}

```

### 3

```java
public class may_min {
    public static void main(String[] args) {
        String cadena = "Cadena De Texto Para Convertir";
        String cadena2 = "caDena DE TEXTO para CONVERTIR";
        String cadenaConvertida = convertir(cadena);
        String cadenaConvertida2 = convertir(cadena2);
        System.out.println("Cadena convertida 1 : " + cadenaConvertida);
        System.out.println("Cadena convertida2 : " + cadenaConvertida2);
    }

    public static String convertir(String cadena) {
        StringBuilder resultado = new StringBuilder();

        for (int i = 0; i < cadena.length(); i++) {
            char caracter = cadena.charAt(i);

            if (Character.isUpperCase(caracter)) {
                char caracterEnMinusculas = Character.toLowerCase(caracter); 
                resultado.append(caracterEnMinusculas);
            } else if (Character.isLowerCase(caracter)) {
                char caracterEnMayusculas = Character.toUpperCase(caracter); 
                resultado.append(caracterEnMayusculas);
            } else {
                resultado.append(caracter);
        
            }
        }

        return resultado.toString();
    }
}

```

### 4

```java
public class contador {
    public static void main(String[] args) {
        String cadena = "Esta es una cadena de texto";
        int contadorPalabras = contarPalabras(cadena);
        System.out.println("El número de palabras en la cadena es: " + contadorPalabras);
    }


    public static int contarPalabras(String cadena) {
        String[] palabras = cadena.split("\\s+");
        return palabras.length;
    }
}
```

### 5

```java
import java.util.Arrays;

public class alfabetico {
    public static void main(String[] args) {
        String cadena = "Cadena de texto para organizar en orden alfabético";
        String resultado = ordenar(cadena);
        System.out.println("El resultado es: " + resultado);
    }

    public static String ordenar(String cadena) {
        String[] palabras = cadena.toLowerCase().split(" "); 
        Arrays.sort(palabras); 
        return String.join(" ", palabras); 
    }
}

```





