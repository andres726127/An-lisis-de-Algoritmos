## Nombre: Leonardo Mendieta
### Nota: Los talleres se encuentran en el apartado de Wiki!

# Introducción

Este libro es sobre algoritmos, o sea, esas instrucciones que te dicen cómo hacer cosas paso a paso. Al principio aclaramos qué carajo significa eso y mostramos varias formas simples de hacer multiplicaciones para que se entienda bien. Además, te damos la razón por la que estudiar algoritmos no es solo útil, sino que también puede ser interesante (aunque a veces parezca un embole).

Si tenés olvidadas las matemáticas básicas o los conceptos de computación, no te asustes: acá vas a encontrar un repaso rápido con lo más importante. No vamos a dar clases de cálculo o programación, pero sí lo básico para que sigas el libro sin perderte.

## ¿Qué es un algoritmo?

Un algoritmo es básicamente un conjunto de reglas para hacer un cálculo o resolver un problema, ya sea con lápiz y papel o en una compu. Lo que hacemos acá es estudiar los que sirven para computadoras, pero ojo que sumar o multiplicar también son algoritmos. Por ejemplo, el más viejo de todos es el de Euclides para encontrar el máximo común divisor.

Un algoritmo no tiene que dejarte elegir cosas al azar o pedirte que uses intuición. Si te dice “agrega sal al gusto” no es algoritmo, porque no es preciso. Pero si te dice “elige un número entre 1 y 6 con la misma probabilidad”, ahí sí, porque está claro cómo hacerlo (por ejemplo, tirando un dado).

## Cómo escribimos los programas

Para evitar confusiones, vamos a mostrar los algoritmos usando algo parecido a un lenguaje de programación estructurado (como Pascal), pero sin atarnos a uno solo. Así la idea queda clara sin perder tiempo en detalles.

Usamos español mezclado con símbolos matemáticos para que sea simple. Algunos conceptos (como recursividad o punteros) los damos por conocidos.

## Notación matemática rápida

Aquí repasamos rápido la notación matemática que usaremos: lógica booleana (verdadero/falso), teoría de conjuntos (conjuntos, subconjuntos, uniones, etc.), números enteros y reales, sumas, productos y cosas como factoriales y combinaciones.

También hablamos de eficiencia: cuánto tiempo y memoria usa un algoritmo, y cómo medir su rendimiento con la famosa notación O grande (ej: O(n), O(log n)).

## En resumen

- Algoritmo = instrucciones claras, sin ambigüedades ni decisiones a mano.
- Usamos notación mixta (programación y matemática) para explicarlos.
- Repasamos lo básico que necesitás para no perderte.
- Explicamos cómo medir la eficiencia para saber si un algoritmo es bueno o malo.
# Técnicas de Demostración para No Perderse

## Técnica 1: Demostración por Contradicción (o “la trampa”)

Cuando tienes un montón de algoritmos y no sabes cuál usar, lo que importa es entender bien sus propiedades matemáticas, como cuánto tardan en resolver el problema según el tamaño de la entrada. Para eso, a veces hay que hacer demostraciones, y una de las más usadas es la de contradicción.

¿Cómo funciona? Pues básicamente quieres probar que una cosa es cierta, pero en vez de hacerlo directo, dices: “Bueno, supongamos que no es verdad”. Y luego te pones a sacar consecuencias de esa idea hasta que llegas a una tontería que no puede ser. Eso prueba que la idea original no puede ser falsa, ergo es verdadera. 

Por ejemplo: quieres probar que hay infinitos números primos. Pues empiezas diciendo “No, sólo hay unos pocos”. Multiplicas todos esos primos y le sumas uno, y resulta que ese nuevo número no puede ser dividido por ninguno de esos primos. Eso es una contradicción, porque según tu suposición debería ser divisible. Por tanto, hay infinitos primos.

---

## Técnica 2: Inducción matemática (o “el truco del dominó”)

Esta técnica es la que más se usa para demostrar cosas en algoritmia. La idea es sencilla: si pruebas que algo es cierto para un caso base (por ejemplo, n = 0), y luego pruebas que si es cierto para un número cualquiera n, entonces también lo es para n + 1, entonces ya tienes la cosa comprobada para todos los números naturales.

Un ejemplo tonto es un algoritmo que calcula el cuadrado de un número `n`. Pruebas para algunos valores y ves que funciona, pero ¿cómo demostrar que siempre funciona? Con inducción: pruebas que funciona para n=0 y luego, suponiendo que funciona para n-1, demuestras que funciona para n. Así de simple.

**Ojo:** Hay que tener cuidado, porque a veces la inducción falla si no se hacen bien las bases. Hay un ejemplo clásico con caballos donde el “truco” falla porque no se cumple para pasar de 1 a 2 caballos.  

---

## Inducción matemática generalizada (o “cuando la simple no alcanza”)

A veces la inducción normal no es suficiente, y necesitas una versión más brava. Por ejemplo, para probar que cualquier número compuesto se puede descomponer en números primos, no basta con asumir que funciona para `n-1`. Necesitas asumir que funciona para **todos** los números menores que `n`. Esto se llama inducción generalizada y es más poderosa para cosas más complicadas.

---

**Resumen:**  
- Contradicción: Supón que no, y si sale algo ridículo, entonces sí.  
- Inducción: Demuestra para el caso base y que el paso de n a n+1 funciona, y listo.  
- Inducción generalizada: Cuando necesitas suponer cosas más grandes para probar lo que quieres.

---

Si te interesa ver ejemplos más locos o el porqué de todo esto, échale un ojo a los detalles más formales en la sección que sigue.

# Inducción Constructiva y Otros Chunches Matemáticos

## Inducción Constructiva
La inducción matemática es como la herramienta ninja para demostrar cosas raras que aparecen de la nada, como sacar un conejo del sombrero. Sirve no solo para confirmar que una afirmación es verdad, sino también para entender mejor qué carajos significa realmente esa afirmación y cómo funciona. 

Con la inducción constructiva, puedes demostrar que algo medio vago es cierto y, de paso, descubrir las piezas que faltaban para que tenga sentido. Un ejemplo común es con la sucesión de Fibonacci, que usaremos para mostrar cómo esta técnica ayuda a analizar algoritmos.

---

## Recordatorios Básicos (para no perderse)

### Límites
Cuando una función se vuelve loca y crece hasta el infinito o se va para el lado opuesto (menos infinito), o simplemente no se decide y baila entre valores, decimos que está oscilando. Si esa danza está controlada (no se pasa de cierto límite), es oscilación finita, si no, es oscilación infinita.

### Series Sencillas
Una serie puede ser amigable y converger a un número (suma finita), o volverse loca y divergir hacia el infinito, o andar dando vueltas sin decidir. Ejemplos clásicos: series aritméticas y geométricas.

### Combinatoria Básica
Si tienes objetos bien distintos (como figuritas con nombres), la combinatoria se encarga de contar cuántas formas hay para ordenarlos o combinarlos.

### Probabilidad Elemental
Imagina que tienes n cosas etiquetadas (a, b, c...), la probabilidad estudia cuántas maneras hay de ordenar esas cosas o sacar eventos al azar.

---

## Algoritmia Elemental

### ¿Qué es un algoritmo?
Un algoritmo es como la receta para hacer cualquier cosa paso a paso, ya sea para programar, matemáticas o hasta para armar un sándwich.

### Eficiencia de Algoritmos
La eficiencia mide qué tan bien un algoritmo usa los recursos (tiempo, memoria) para resolver su problema. Un buen algoritmo no solo funciona, sino que lo hace rápido y sin gastar mucha chamba computacional.

### Análisis: Caso Peor y Caso Medio
- **Caso Peor:** cuando la cosa se pone difícil y el algoritmo se tarda lo máximo posible (usamos la notación O grande).
- **Caso Medio:** el promedio que tarda el algoritmo considerando entradas random (se representa con Θ).

### Operación Elemental
Es la tarea más básica que hace un algoritmo y que toma tiempo fijo. Contar estas operaciones nos ayuda a medir qué tan pesado es el algoritmo.

### ¿Por qué buscar eficiencia?
Porque la compu no es mágica. Si no usas bien los recursos, tu programa va a ser un desastre, lento y poco útil, sobre todo con datos gigantescos.

---

## Notación Asintótica

Esta notación es para entender cómo se comportan los algoritmos cuando el tamaño del problema crece hasta la locura. Aunque a veces no sirve para casos chiquitos, en general te dice qué algoritmo es mejor cuando la cosa se pone seria.

---

**Resumen:**  
Si quieres sobrevivir en programación, tienes que entender estas técnicas y conceptos básicos. Sirven para demostrar que las cosas funcionan y para elegir el camino rápido y limpio cuando programas.

# Notación Big-O y Análisis de Algoritmos (Versión Desenchufada)

## ¿Qué carajo es esto del "orden de"?

La notación Big-O es la forma chida de decir “más o menos cuánto se tarda algo sin complicarnos”. Se usa para medir cómo crece la dificultad (tiempo, memoria) de un algoritmo con el tamaño del problema. Por ejemplo, cuando dicen que un algoritmo es O(n³), quiere decir que, a medida que n crece, el tiempo crece más o menos como n³.

Ojo, no siempre verás la notación igual: algunos ponen O(f(n)) y otros dicen "n es del orden de f(n)". No te calientes, es lo mismo pero con diferente estilo. A veces hasta meten funciones raras, hasta negativas o con detalles que no importan para lo grande.

## Notación asintótica para los que quieren más lío

Si el peor caso tarda menos de cierta función multiplicada por una constante, decimos que está en O(f(n)). Si en cambio tarda al menos eso (un piso), está en Ω(f(n)). Y si está en ambos lados, decimos que es Θ(f(n)). Básicamente, O es el techo, Ω el piso, y Θ el rango exacto.

Por ejemplo, ordenar con inserción es O(n²) en el peor caso, pero en muchos casos va más rápido (como cuando la lista ya está casi ordenada). Así que un algoritmo puede tener tiempos muy diferentes dependiendo de la situación.

## Varias variables, varios rollos

A veces el tiempo no depende solo de un número, sino de dos o más, como en grafos que dependen de nodos y aristas. En ese caso usamos una notación Big-O multidimensional, tipo O(f(m,n)).

## Cómo manejar la notación sin perder la cabeza

Cuando sumamos tiempos de varias partes de un algoritmo, no hay que andar con mucha paranoia: O(f(n)) + O(g(n)) es lo mismo que O(max(f(n), g(n))). O sea, el tiempo total es del que crece más rápido.

## Análisis de algoritmos: el punto real del asunto

El objetivo es diseñar algoritmos que sean rápidos y eficientes. Cuando tienes varios métodos para un problema, toca decidir cuál usar. Esto no es magia: se basa en experiencia, intuición y, claro, en analizar tiempos con técnicas como resolver ecuaciones de recurrencia o entender estructuras de control (bucles, recursión, etc.).

## Análisis rápido de bucles y cosas raras

- Los bucles `for` suelen ser fáciles: si algo se repite m veces y cada vez cuesta t, el total es m*t.
- Pero ojo, a veces el control del bucle suma tiempo que no ves a simple vista.
- Bucles `while` o `repeat` son un poco más jodidos, porque no sabes cuántas vueltas van a dar. Se analiza usando funciones que bajan cada vez y garantizan que el bucle termina.
- Las llamadas recursivas se analizan con ecuaciones de recurrencia. Algunos ejemplos, como Fibonacci recursivo, crecen muy rápido (exponencialmente).

## Usar un “barómetro”

Para no marearse con todos los detalles, se escoge una instrucción que se ejecuta más que todas (el “barómetro”). El tiempo del algoritmo es del orden de las veces que se ejecuta esa instrucción. Así se simplifica el análisis sin perder la idea principal.

## Ejemplo: inserción

El peor caso de ordenación por inserción pasa cuando la lista está ordenada al revés. Ahí, el bucle que mueve los elementos se ejecuta como n²/2 veces, o sea, O(n²). Pero si la lista ya está casi ordenada, va mucho más rápido.

---

#  Bimestre 2 – Algoritmos: Divide y Vencerás, Búsqueda, Ordenación y Grafos

## 🔹 Divide y Vencerás

Aprendimos la estrategia de “divide y vencerás”, que consiste en dividir un problema en partes pequeñas, resolverlas por separado y luego combinarlas. Se vio con un ejemplo de multiplicación: 981 × 1234.

En lugar de multiplicar directamente, se separan los números:

- 981 → w = 09, x = 81
- 1234 → y = 12, z = 34

Se calculan:
- `p = w * y = 108`
- `q = x * z = 2754`
- `r = (w + x) * (y + z) = 90 * 46 = 4140`

Y luego:
> Resultado = 10⁴ * p + 10² * (r − p − q) + q

Este método reduce el número de multiplicaciones necesarias y se basa en una técnica algorítmica eficiente.

---

```Java
package pseudoaleatorios;
import java.util.Scanner;

public class Pseudoaleatorios {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Cantidad de números a generar: ");
        int cantidad = scanner.nextInt();

        System.out.print("Ingrese la semilla (X0): ");
        long x = scanner.nextLong();

        // Parámetros clásicos para el algoritmo
        final long a = 1664525;     // multiplicador
        final long c = 1013904223;  // incremento
        final long m = (long) Math.pow(2, 32);  // módulo

        System.out.println("Números pseudoaleatorios generados:");
        for (int i = 0; i < cantidad; i++) {
            x = (a * x + c) % m;
            System.out.println(x);
        }

        scanner.close();
    }
}

```
![Pseudonumeros](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/Pseudonumeros.png)

## 🔹 Búsqueda Binaria

Es una técnica eficiente para buscar elementos en listas ordenadas. Reduce el espacio de búsqueda a la mitad en cada paso.

- Complejidad: O(log n)
- Mucho más rápida que una búsqueda lineal si los datos están ordenados.

---
```Java
package busquedabinaria;
import java.util.Arrays;
import java.util.Random;
import java.util.Scanner;

public class BusquedaBinaria {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        System.out.print("¿Cuántos números aleatorios deseas generar? ");
        int n = scanner.nextInt();

        int[] numeros = new int[n];
        for (int i = 0; i < n; i++) {
            numeros[i] = random.nextInt(100); // Números entre 0 y 99
        }

        // Ordenamos el arreglo antes de buscar
        Arrays.sort(numeros);
        System.out.println("Arreglo ordenado:");
        System.out.println(Arrays.toString(numeros));

        System.out.print("¿Qué número deseas buscar? ");
        int objetivo = scanner.nextInt();

        // Elegir método de búsqueda binaria
        int resultado = busquedaBinariaIterativa(numeros, objetivo);
        // int resultado = busquedaBinariaRecursiva(numeros, 0, numeros.length - 1, objetivo);

        if (resultado != -1) {
            System.out.println("Número encontrado en la posición: " + resultado);
        } else {
            System.out.println("Número no encontrado.");
        }

        scanner.close();
    }

    // Búsqueda binaria iterativa
    public static int busquedaBinariaIterativa(int[] arr, int objetivo) {
        int izquierda = 0;
        int derecha = arr.length - 1;

        while (izquierda <= derecha) {
            int medio = (izquierda + derecha) / 2;

            if (arr[medio] == objetivo) {
                return medio;
            } else if (arr[medio] < objetivo) {
                izquierda = medio + 1;
            } else {
                derecha = medio - 1;
            }
        }

        return -1;
    }

    // Búsqueda binaria recursiva (opcional)
    public static int busquedaBinariaRecursiva(int[] arr, int izquierda, int derecha, int objetivo) {
        if (izquierda > derecha) {
            return -1;
        }

        int medio = (izquierda + derecha) / 2;

        if (arr[medio] == objetivo) {
            return medio;
        } else if (arr[medio] < objetivo) {
            return busquedaBinariaRecursiva(arr, medio + 1, derecha, objetivo);
        } else {
            return busquedaBinariaRecursiva(arr, izquierda, medio - 1, objetivo);
        }
    }
}

```
![Busqueda Binaria](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/BusquedaBinaria.png)

## 🔹 Ordenación – Quicksort

El algoritmo **quicksort** selecciona un pivote y divide el arreglo en elementos menores y mayores. Luego aplica recursivamente la misma idea.

- Eficiente en promedio
- Amplio uso en programación

---
```Java
package busquedabinaria;
import java.util.Arrays;
import java.util.Random;
import java.util.Scanner;

public class QuickSortEjemplo {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        System.out.print("¿Cuántos números aleatorios deseas generar? ");
        int n = scanner.nextInt();

        int[] arreglo = new int[n];
        for (int i = 0; i < n; i++) {
            arreglo[i] = random.nextInt(100); // Números entre 0 y 99
        }

        System.out.println("Arreglo original:");
        System.out.println(Arrays.toString(arreglo));

        quicksort(arreglo, 0, arreglo.length - 1);

        System.out.println("Arreglo ordenado con Quicksort:");
        System.out.println(Arrays.toString(arreglo));

        scanner.close();
    }

    // Implementación de Quicksort
    public static void quicksort(int[] arr, int izquierda, int derecha) {
        if (izquierda < derecha) {
            int indicePivote = particion(arr, izquierda, derecha);

            quicksort(arr, izquierda, indicePivote - 1);  // Subarreglo izquierdo
            quicksort(arr, indicePivote + 1, derecha);    // Subarreglo derecho
        }
    }

    // Función de partición (usa el último elemento como pivote)
    public static int particion(int[] arr, int izquierda, int derecha) {
        int pivote = arr[derecha];
        int i = izquierda - 1;

        for (int j = izquierda; j < derecha; j++) {
            if (arr[j] <= pivote) {
                i++;
                intercambiar(arr, i, j);
            }
        }

        intercambiar(arr, i + 1, derecha);
        return i + 1;
    }

    // Método auxiliar para intercambiar elementos
    public static void intercambiar(int[] arr, int i, int j) {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}

```
![QuickSort](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/QuickSort.png)
## 🔹 Algoritmos Voraces (Greedy)

Son algoritmos que toman decisiones paso a paso, eligiendo la opción más conveniente en cada momento.

**Ejemplo práctico:** dar cambio con el menor número de monedas posibles.

**Ventajas:**
- Sencillos de implementar
- Eficientes para muchos casos

**Desventajas:**
- No garantizan la mejor solución en todos los casos

---
```Java
package mochilavoraz;
import java.util.*;

class Objeto {
    int valor, peso;
    double ratio;

    public Objeto(int valor, int peso) {
        this.valor = valor;
        this.peso = peso;
        this.ratio = (double) valor / peso;
    }
}

public class MochilaVoraz {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Número de objetos: ");
        int n = scanner.nextInt();

        Objeto[] objetos = new Objeto[n];

        for (int i = 0; i < n; i++) {
            System.out.print("Valor del objeto " + (i + 1) + ": ");
            int valor = scanner.nextInt();
            System.out.print("Peso del objeto " + (i + 1) + ": ");
            int peso = scanner.nextInt();
            objetos[i] = new Objeto(valor, peso);
        }

        System.out.print("Capacidad de la mochila: ");
        int capacidad = scanner.nextInt();

        double maxValor = mochilaFraccionaria(objetos, capacidad);

        System.out.printf("Valor máximo en la mochila: %.2f\n", maxValor);

        scanner.close();
    }

    public static double mochilaFraccionaria(Objeto[] objetos, int capacidad) {
        Arrays.sort(objetos, (a, b) -> Double.compare(b.ratio, a.ratio)); // Ordenar por valor/peso descendente

        double valorTotal = 0.0;

        for (Objeto obj : objetos) {
            if (capacidad == 0) break;

            if (obj.peso <= capacidad) {
                valorTotal += obj.valor;
                capacidad -= obj.peso;
            } else {
                valorTotal += obj.ratio * capacidad;
                capacidad = 0;
            }
        }

        return valorTotal;
    }
}

```
![Mochila Voraz](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/MochilaVoraz.png)
## 🔹 Grafos y Árbol de Recubrimiento Mínimo (MST)

Un **grafo** es un conjunto de nodos (vértices) conectados por enlaces (aristas).

El **árbol de recubrimiento mínimo** conecta todos los nodos con el menor costo total, sin ciclos. Se usa en redes eléctricas, transporte, etc.

El **algoritmo de Kruskal** es uno de los más usados para encontrar este árbol, seleccionando siempre la arista más barata sin formar ciclos.

---
### Grafos:
![Grafos](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/grafos.PNG)

### Arbol de recubrimiento minimo
![Arbol de recubrimiento minimo](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/Arbol%2Bde%2Bcubrimiento%2Bm%C3%ADnimo.jpg)

### Algoritmo de Kurskal
![Algoritmo de Kurskal](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/AlgoritmoDeKurskal.jpg)
# 📘 Estrategias Bajo Incertidumbre y Algoritmos Probabilísticos

## 🔸 Problema del Tesoro y el Dragón

Un tesoro con `x` lingotes está escondido en A o B. Se desconoce su ubicación exacta. Viajar desde el punto de partida (O) toma 5 días y cada noche un dragón roba `y` lingotes.

Opciones:

1. Esperar 4 días para saber con certeza la ubicación.
2. Pagarle a un elfo `3y` lingotes para saberla de inmediato.
3. Elegir al azar (por ejemplo, lanzar una moneda).

**Valor esperado con opción aleatoria:**

- Acertar (50%): pérdida de `5y` → ganancia: `x − 5y`
- Fallar (50%): pérdida de `10y` → ganancia: `x − 10y`

> Esperanza matemática:  
> `E[ganancia] = 0.5(x − 5y) + 0.5(x − 10y) = x − 7.5y`

Este enfoque usa **estrategias probabilísticas** para tomar decisiones basadas en el riesgo y beneficio esperado.

---

## 🔸 Algoritmos Probabilísticos

- No garantizan siempre el mismo resultado.
- Usan variables aleatorias para tomar decisiones.
- Son útiles cuando obtener información exacta es costoso o incierto.

**Ventajas:**
- Flexibles y rápidos
- Buen rendimiento práctico

**Desventajas:**
- Pueden fallar o no dar siempre la mejor solución
- Requieren análisis más avanzado (probabilidades, esperanza matemática)

---
![Algoritmos y probabilidades](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/AlgoritmosYprobabilidades.png)

## 🔸 Números Pseudoaleatorios

Los **números pseudoaleatorios** son generados por algoritmos (como el generador lineal congruencial) y se comportan como si fueran aleatorios.

> Fórmula: `Xₙ₊₁ = (a * Xₙ + c) mod m`

- Se usan en simulaciones, pruebas, juegos, etc.

---
### Ejemplo:
```Java
package pseudoaleatorios;
import java.util.Scanner;

public class Pseudoaleatorios {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Cantidad de números a generar: ");
        int cantidad = scanner.nextInt();

        System.out.print("Ingrese la semilla (X0): ");
        long x = scanner.nextLong();

        // Parámetros clásicos para el algoritmo
        final long a = 1664525;     // multiplicador
        final long c = 1013904223;  // incremento
        final long m = (long) Math.pow(2, 32);  // módulo

        System.out.println("Números pseudoaleatorios generados:");
        for (int i = 0; i < cantidad; i++) {
            x = (a * x + c) % m;
            System.out.println(x);
        }

        scanner.close();
    }
}

```
![Pseudonumeros](https://raw.githubusercontent.com/andres726127/An-lisis-de-Algoritmos/refs/heads/main/carpeta_nueva/Pseudonumeros.png)

## 🔸 Tiempo de Ejecución

- **Tiempo promedio:** en algoritmos deterministas (según todas las entradas).
- **Tiempo esperado:** en algoritmos probabilísticos (según decisiones aleatorias).
- **Tiempo esperado en el peor caso:** combinación de los dos anteriores para situaciones más conservadoras.

---

## 🔸 Algoritmos Deterministas vs Probabilísticos

| Determinista        | Probabilístico              |
|---------------------|-----------------------------|
| Siempre da el mismo resultado | Puede dar diferentes resultados |
| Análisis más estructurado     | Requiere análisis probabilístico |
| Útil para problemas conocidos | Útil en situaciones inciertas   |

---


