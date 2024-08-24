# Semana 1 
## Tabla de Contenidos

1. [Flujo de Control / Control Flow](#1-flujo-de-control--control-flow)
   - [Sentencias If](#sentencias-if)
   - [Ejercicio Práctico: Calculadora de Calificaciones](#ejercicio-práctico-calculadora-de-calificaciones-15-minutos)
   - [Bucles](#bucles)
   - [Ejercicio Práctico: Generador de Tablas de Multiplicar](#ejercicio-práctico-generador-de-tablas-de-multiplicar-20-minutos)
2. [Arreglos - Arrays](#2-arreglos---arrays)
   - [¿Qué es un Array?](#qué-es-un-array)
   - [¿Por Qué Usar Arrays?](#por-qué-usar-arrays)
   - [Declaración e Inicialización de Arrays](#declaración-e-inicialización-de-arrays)
   - [Acceso a los Elementos de un Array](#acceso-a-los-elementos-de-un-array)
   - [Modificación de los Elementos de un Array](#modificación-de-los-elementos-de-un-array)
   - [Longitud de un Array](#longitud-de-un-array)
   - [Iteración a Través de los Arrays](#iteración-a-través-de-los-arrays)
   - [Operaciones Comunes en Arrays](#operaciones-comunes-en-arrays)
   - [Ejercicio Práctico: Rastreador de Temperaturas](#ejercicio-práctico-rastreador-de-temperaturas-20-minutos)

---

## 1. Flujo de Control / Control Flow

### Sentencias If
Las sentencias If son fundamentales en la programación, ya que permiten que tu código tome decisiones y ejecute diferentes bloques de código en función de condiciones.

#### Sentencia If Básica
```java
if (condición) {
    // código a ejecutar si la condición es verdadera
}
```

Ejemplo:
```java
int temperatura = 25;
if (temperatura > 30) {
    System.out.println("¡Hace calor!");
}
```

#### Sentencia If-Else
```java
if (condición) {
    // código a ejecutar si la condición es verdadera
} else {
    // código a ejecutar si la condición es falsa
}
```

Ejemplo:
```java
int temperatura = 25;
if (temperatura > 30) {
    System.out.println("¡Hace calor!");
} else {
    System.out.println("No hace tanto calor hoy.");
}
```

#### Sentencia Else-If
```java
if (condición1) {
    // código a ejecutar si la condición1 es verdadera
} else if (condición2) {
    // código a ejecutar si la condición2 es verdadera
} else {
    // código a ejecutar si todas las condiciones son falsas
}
```

Ejemplo:
```java
int temperatura = 25;
if (temperatura > 30) {
    System.out.println("¡Hace calor!");
} else if (temperatura > 20) {
    System.out.println("Hace un buen día.");
} else {
    System.out.println("Hace un poco de frío.");
}
```

#### Sentencias If Anidadas
También puedes colocar sentencias If dentro de otras sentencias If. Esto se llama anidación.

Ejemplo:
```java
boolean esFinDeSemana = true;
boolean estáLloviendo = false;

if (esFinDeSemana) {
    if (estáLloviendo) {
        System.out.println("Quedémonos en casa y veamos una película.");
    } else {
        System.out.println("¡Vamos de picnic!");
    }
} else {
    System.out.println("Es un día de trabajo.");
}
```

#### Sentencias Switch
Las sentencias `switch` son útiles cuando tienes que tomar decisiones múltiples basadas en el valor de una sola variable. En lugar de escribir múltiples sentencias `if-else`, puedes usar `switch` para simplificar el código.

```java
switch (variable) {
    case valor1:
        // código a ejecutar si la variable es igual a valor1
        break;
    case valor2:
        // código a ejecutar si la variable es igual a valor2
        break;
    // más casos según sea necesario
    default:
        // código a ejecutar si la variable no coincide con ningún caso
}
```

Ejemplo:
```java
int día = 4;
switch (día) {
    case 1:
        System.out.println("Lunes");
        break;
    case 2:
        System.out.println("Martes");
        break;
    case 3:
        System.out.println("Miércoles");
        break;
    case 4:
        System.out.println("Jueves");
        break;
    case 5:
        System.out.println("Viernes");
        break;
    default:
        System.out.println("Fin de semana");
        break;
}
```

#### Operadores Ternarios
El operador ternario es una forma compacta de escribir una sentencia `if-else`. Es útil para expresiones simples donde se asigna un valor basado en una condición.

```java
variable = (condición) ? valorSiVerdadero : valorSiFalso;
```

Ejemplo:
```java
int edad = 18;
String resultado = (edad >= 18) ? "Eres mayor de edad" : "Eres menor de edad";
System.out.println(resultado);
```

### Ejercicio Práctico: Calculadora de Calificaciones (15 minutos)

Vamos a crear un programa que asigne calificaciones de letras basadas en puntajes numéricos.

#### Descripción de la Tarea:
1. Crea un programa que tome una calificación numérica (0-100) e imprima la calificación correspondiente en letra.
2. Usa la siguiente escala de calificaciones:
   - 90-100: A
   - 80-89: B
   - 70-79: C
   - 60-69: D
   - Por debajo de 60: F
3. El programa también debe manejar calificaciones inválidas (por debajo de 0 o por encima de 100).

### Bucles
Los bucles son constructos fundamentales de la programación que te permiten repetir un bloque de código múltiples veces. Son esenciales para la programación eficiente y son particularmente útiles al trabajar con colecciones de datos.

#### ¿Por Qué Usar Bucles?
Los bucles te ayudan a:
- Automatizar tareas repetitivas
- Procesar colecciones de datos de manera eficiente
- Implementar algoritmos que requieren operaciones repetidas

#### Tipos de Bucles en Java
1. **Bucle for**: Se usa cuando sabes de antemano cuántas veces quieres repetir un bloque de código.
   ```java
   for (inicialización; condición; actualización) {
       // código a repetir
   }
   ```

2. **Bucle while**: Se usa cuando quieres repetir un bloque de código mientras una condición sea verdadera.
   ```java
   while (condición) {
       // código a repetir
   }
   ```

3. **Bucle do-while**: Similar al bucle while, pero garantiza que el bloque de código se ejecute al menos una vez.
   ```java
   do {
       // código a repetir
   } while (condición);
   ```

#### Sentencias de Control de Bucles
Java proporciona sentencias para controlar el flujo de los bucles:
- `break`: Sale del bucle inmediatamente
- `continue`: Omite el resto de la iteración actual y pasa a la siguiente

### Ejercicio Práctico: Generador de Tablas de Multiplicar (20 minutos)

Vamos a crear un programa que genere una tabla de multiplicar para practicar el uso de bucles.

#### Descripción de la Tarea:
1. Crea un programa que imprima una tabla de multiplicar para los números del 1 al 5.
2. Usa bucles anidados para generar la tabla.
3. La salida/putput debería ser algo así:
   ```
   1  2  3  4  5
   2  4  6  8 10
   3  6  9 12 15
   4  8 12 16 20
   5 10 15 20 25
   ```

## 2. Arreglos - Arrays

### ¿Qué es un Array?
Un array es un contenedor que guarda un número fijo de valores de un solo tipo. Piensa en un array como una fila de cajas, donde cada caja puede contener un elemento de un tipo específico (como enteros, cadenas, etc.).

### ¿Por Qué Usar Arrays?
Los arrays te permiten almacenar múltiples elementos del mismo tipo bajo un solo nombre de variable. Esto facilita:
- Agrupar datos relacionados
- Realizar operaciones en múltiples valores de manera eficiente
- Organizar y gestionar grandes conjuntos de datos

### Declaración e Inicialización de Arrays
En Java, puedes declarar e inicializar un array de varias maneras:

1. Declarar un array sin inicializar:
   ```java
   int[] números;  // Declara un array de enteros
   ```

2. Declarar y asignar memoria para el array:
   ```java
   int[] números = new int[5];  // Crea un array que puede contener 5 enteros
   ```

3. Declarar, asignar memoria e inicializar el array:
   ```java
   int[] números = {1, 2, 3, 4, 5};  // Crea e inicializa un array con 5 enteros
   ```

### Acceso a los Elementos de un Array
Los elementos de un array se acceden utilizando su índice. En Java, los índices de los array comienzan en 0.

```java
int[] números = {10, 20, 30, 40, 50};
System.out.println(números[0]);  // Imprime: 10
System.out.println(números[2]);  // Imprime: 30
```

### Modificación de los Elementos de un Array
Puedes cambiar el valor de un elemento de un array asignando un nuevo valor a un índice específico:

```java
números[1] = 25;  // Cambia el segundo elemento (índice 1) a 25
```

### Longitud de un Array
Puedes averiguar cuántos elementos tiene un arreglo utilizando la propiedad `length`:

```java
int tamañoArray = números.length;  // tamañoArray será 5
```

### Iteración a Través de los Arrays
Puedes usar bucles para iterar a través de los elementos de un array:

1. Usando un bucle for:
   ```java
   for (int i = 0; i < números.length; i++) {
       System.out.println(números[i]);
   }
   ```

2. Usando un bucle for mejorado (bucle for-each):
   ```java
   for (int número : números) {
       System.out.println(número);
   }
   ```

### Operaciones Comunes en Arrays
1. Encontrar la suma de los elementos de un array:
   ```java
   int suma = 0;
   for (int número : números) {
       suma += número;
   }
   ```

2. Encontrar el elemento más grande:
   ```java
   int máximo = números[0];
   for (int i = 1; i < números.length; i++) {
       if (números[i] > máximo) {
           máximo = números[i];
       }
   }
   ```

### Ejercicio Práctico: Rastreador de Temperaturas (20 minutos)

En este ejercicio, crearás un programa que rastrea las temperaturas diarias de una semana y realiza algunos análisis básicos.

#### Descripción de la Tarea:
1. Crea un array para almacenar 7 lecturas diarias de temperatura (como integers).
2. Inicializa el array con valores de temperatura para una semana.
3. Calcula e imprime la temperatura promedio.
4. Encuentra e imprime las temperaturas más alta y más baja de la semana.
5. Cuenta cuántos días estuvieron por encima de la temperatura promedio.

