## Soluciones a los Ejercicios de Estructuras de Control en Java

### Ejercicio 1: Clasificación de Edad

```java
import java.util.Scanner;

public class ClasificacionEdad {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // pedimos la edad
        System.out.print("Ingresa tu edad: ");
        int edad = scanner.nextInt();

        // usamos if para clasificar la edad
        if (edad < 18) {
            System.out.println("Eres menor de edad.");
        } else if (edad >= 18 && edad <= 64) {
            System.out.println("Eres un adulto.");
        } else {
            System.out.println("Eres un adulto mayor.");
        }

        scanner.close();
    }
}
```

---

### Ejercicio 2: Contador de Vocales

```java
import java.util.Scanner;

public class ContadorVocales {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // pedimos la palabra
        System.out.print("Ingresa una palabra: ");
        String palabra = scanner.nextLine().toLowerCase(); // pasamos todo a minúsculas

        int contador = 0;

        // recorremos la palabra con un for
        for (int i = 0; i < palabra.length(); i++) {
            char letra = palabra.charAt(i);
            if ("aeiou".indexOf(letra) != -1) { // si la letra es una vocal
                contador++;
            }
        }

        System.out.println("Número de vocales: " + contador);
        scanner.close();
    }
}
```

---

### Ejercicio 3: Simulación de una Calculadora

```java
import java.util.Scanner;

public class Calculadora {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Menú:");
        System.out.println("1. Sumar");
        System.out.println("2. Restar");
        System.out.println("3. Multiplicar");
        System.out.println("4. Dividir");
        System.out.print("Elige una opción: ");

        int opcion = scanner.nextInt();

        System.out.print("Ingresa el primer número: ");
        double num1 = scanner.nextDouble();
        System.out.print("Ingresa el segundo número: ");
        double num2 = scanner.nextDouble();

        switch (opcion) {
            case 1:
                System.out.println("Resultado: " + (num1 + num2));
                break;
            case 2:
                System.out.println("Resultado: " + (num1 - num2));
                break;
            case 3:
                System.out.println("Resultado: " + (num1 * num2));
                break;
            case 4:
                if (num2 != 0) {
                    System.out.println("Resultado: " + (num1 / num2));
                } else {
                    System.out.println("No se puede dividir por cero.");
                }
                break;
            default:
                System.out.println("Opción no válida.");
        }

        scanner.close();
    }
}
```

---

### Ejercicio 4: Números Pares hasta N

```java
import java.util.Scanner;

public class NumerosPares {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingresa un número: ");
        int n = scanner.nextInt();

        for (int i = 2; i <= n; i += 2) {
            System.out.print(i + " ");
        }

        scanner.close();
    }
}
```

---

### Ejercicio 5: Contraseña con Intentos Limitados

```java
import java.util.Scanner;

public class VerificacionContrasena {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String contrasenaCorrecta = "secreta";
        int intentos = 3;

        while (intentos > 0) {
            System.out.print("Ingresa la contraseña: ");
            String contrasena = scanner.nextLine();

            if (contrasena.equals(contrasenaCorrecta)) {
                System.out.println("Acceso concedido.");
                return;
            } else {
                intentos--;
                System.out.println("Contraseña incorrecta. Te quedan " + intentos + " intentos.");
            }
        }

        System.out.println("Acceso bloqueado.");
        scanner.close();
    }
}
```

---

### Ejercicio 6: Adivina el Número

```java
import java.util.Scanner;
import java.util.Random;

public class AdivinaNumero {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random rand = new Random();
        int numeroSecreto = rand.nextInt(100) + 1;
        int intento;

        do {
            System.out.print("Adivina el número (1-100): ");
            intento = scanner.nextInt();

            if (intento < numeroSecreto) {
                System.out.println("Muy bajo.");
            } else if (intento > numeroSecreto) {
                System.out.println("Muy alto.");
            }
        } while (intento != numeroSecreto);

        System.out.println("¡Felicidades! Adivinaste el número.");
        scanner.close();
    }
}
```

---

### Ejercicio 7: Serie Fibonacci

```java
import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Número de términos: ");
        int n = scanner.nextInt();

        int a = 0, b = 1, c;

        for (int i = 0; i < n; i++) {
            System.out.print(a + " ");
            c = a + b;
            a = b;
            b = c;
        }

        scanner.close();
    }
}
```

---
