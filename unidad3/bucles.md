# Bucles o Ciclos

## Introducción

Una de las principales aplicaciones en programación es el manejo de datos. Los datos se generan continuamente y deben almacenarse, procesarse, analizarse, etc. Por ejemplo, 

- Temperatura del motor de un avión
- Nivel de combustible de un automóvil
- Presión y altitud de una aeronave
- Humedad relativa
- Presión de los neumáticos
- Temperatura de una habitación

En Python, los bucles son estructuras fundamentales que permiten ejecutar un conjunto de instrucciones repetidamente hasta que se cumpla una condición específica. Los bucles son esenciales para la automatización de tareas repetitivas y la manipulación de datos en programación. Python ofrece dos tipos principales de bucles: el bucle `for` que se utiliza para iterar sobre una secuencia (como una lista o una cadena) y el bucle `while` que se ejecuta mientras una condición sea verdadera. Estos bucles proporcionan una poderosa capacidad de control de flujo en Python y son una parte esencial en la construcción de programas eficientes y flexibles.

---

# Bucle while

El bucle `while` en Python es una estructura de control que permite ejecutar un bloque de código repetidamente mientras una condición específica se cumpla. El funcionamiento de este bucle se basa en la evaluación de una expresión booleana. Mientras la condición sea verdadera, el código dentro del bucle  se ejecutará una y otra vez. Este tipo de bucle es especialmente útil cuando no se sabe cuántas veces se debe ejecutar el código de antemano y se desea que la ejecución continúe hasta que se cumpla una condición de salida. Sin embargo, es importante tener cuidado al utilizar bucles, ya que si la condición no se vuelve falsa en algún momento, podría resultar en un bucle infinito que puede causar que el programa se bloquee o se vuelva inmanejable. Observa el siguiente gráfico donde se utiliza un diagrama de flujo para representar el concepto:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/9dffd706-5bb1-4224-bf7f-539e7f76a5ad/Untitled.png)

La sintaxis básica de un bucle `while` en Python consta de la palabra clave `while`, seguida de una condición. El bloque de código que se encuentra indentado debajo del bucle `while` se ejecutará repetidamente mientras la condición sea verdadera. Aquí está la estructura general:

```python
while condicion:
    # Código a ejecutar mientras la condición sea verdadera
```

- `condicion`: Es una expresión booleana que se evalúa antes de cada iteración. Mientras esta condición sea verdadera, el bucle continuará ejecutándose. Tan pronto como la condición se vuelva falsa, la ejecución del bucle `while` se detendrá y el programa continuará con la siguiente instrucción fuera del bucle.

## Ejercicio 1:

Observa el siguiente ejemplo práctico de un bucle `while` que imprime números del 1 al 5:

```python
numero = 1
while numero <= 5:
    print(numero)
    numero += 1      #numero = numero + 1
```

En este ejemplo, la condición `numero <= 5` se evalúa antes de cada iteración. Mientras `numero` sea menor o igual a 5, el bucle imprimirá el valor de `numero` y luego aumentará su valor en 1 con la instrucción `numero += 1`. El bucle continuará ejecutándose hasta que `numero` sea mayor que 5, momento en el que la condición se volverá falsa y el bucle se detendrá.

La salida de este bucle será:

```powershell
1
2
3
4
5
```

Ahora es tu turno. Modifica el código anterior, para que se imprima en la consola únicamente los números pares que hay entre 10 y 50. Analiza el ejemplo y responde las siguientes preguntas antes de comenzar a programar:

- ¿En qué valor debe iniciar la variable número?
- ¿Cuál es la condición que se debe cumplir para que el bucle se repita?
- ¿Cuál es el incremento que debo aplicar a la variable de control?

Luego de responder estas preguntas, habrás entendido lo que hay que hacer y podrás proponer tu solución. 

## ⚠️ Mucha atención con los bucles infinitos

Un bucle infinito es un tipo de bucle que se ejecuta indefinidamente sin una condición de salida adecuada. En otras palabras, el código dentro del bucle se ejecuta una y otra vez sin detenerse, lo que puede hacer que un programa se vuelva inmanejable y no responda. Los bucles infinitos son un error común en la programación y deben evitarse, ya que pueden agotar los recursos del sistema y hacer que un programa se bloquee.

Aquí tienes un ejemplo donde un error en la condición podría causar un bucle infinito:

```python
numero = 5
while numero > 0:  
    print(numero)
    numero += 1
```

Analiza el código anterior y responde:

- ¿Por qué se causa el bucle infinito?
- ¿Cómo se soluciona el problema?

<aside>
📢 Si ejecutaste el código y estás dentro de un bucle infinito, puedes presionar `Ctrl+C` para detener la ejecución del bucle.

</aside>

## Variable tipo contador

Un **contador** es una variable entera que se incrementa o decrementa dentro del bloque de código, con el fin de realizar el control de la ejecución del código. Observa el siguiente ejemplo:

```python
# Inicializamos la variable contador
contador = 0

# Definimos el valor máximo hasta el cual queremos contar
valor_maximo = 10

# Usamos un bucle while para contar hasta el valor máximo
while contador <= valor_maximo:
    print(contador)
    contador += 1  # Incrementamos el contador en 1 en cada iteración
```

## Variable de control (tipo bandera)

Una bandera es una variable tipo `Bool` que sirve para determinar el estado de un proceso. Se puede aprovechar las estructuras condicionales para cambiar el estado de dicha variable y de ese modo controlar un bucle. Observa el siguiente ejemplo:

```python
# Inicializamos una variable booleana tipo bandera
bandera = True

# Creamos un bucle while que se ejecutará mientras la bandera sea True
while bandera == True:
    respuesta = input("¿Quieres salir del bucle? (Si/No): ")
    if respuesta.lower() == "si": #Convertimos a minúscula antes de comparar
        bandera = False  # Cambiamos la bandera a False para salir del bucle

print("Has salido del bucle.")
```

## Ejercicios:

### 1. Serie de Fibonacci:

La serie de Fibonacci es una secuencia matemática infinita que comienza generalmente con los números 0 y 1. A partir de estos dos valores iniciales, cada número subsiguiente en la serie se obtiene sumando los dos números anteriores. En otras palabras, cada número en la serie de Fibonacci es la suma de los dos números precedentes. La secuencia comienza de la siguiente manera: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ... y así sucesivamente. La serie de Fibonacci tiene una amplia gama de aplicaciones en matemáticas, ciencia, informática y naturaleza, y sus propiedades y patrones únicos han sido objeto de estudio y fascinación durante siglos.

- Realiza un programa para generar N elementos de la sucesión de Fibonacci (0, 1, 1, 2, 3, 5, 8, 13,…). **N** será un número entero ingresado por el usuario.

<aside>
💡 Recuerda que nunca debes empezar a escribir código si antes no has entendido el problema.

</aside>

A continuación te dejo un pseudocódigo que podría ayudarte a entender mejor el problema. 

```bash
# Solicitar al usuario un número entero
Imprimir("Ingrese un número entero para generar la serie de Fibonacci:")
Leer(num)

# Verificar si el número ingresado es válido
Si num <= 0, entonces:
    Imprimir("Por favor, ingrese un número entero positivo.")
Sino si num == 1, entonces:
    Imprimir("Serie de Fibonacci:")
    Imprimir(0)
Sino:
    # Inicializar los primeros dos términos de la serie
    a = 0
    b = 1
    contador = 2  # Iniciar en 2 debido a los dos primeros términos ya impresos

    # Imprimir los primeros dos términos
    Imprimir("Serie de Fibonacci:")
    Imprimir(a)
    Imprimir(b)

    # Calcular e imprimir los términos restantes
    Mientras contador < num, hacer:
        siguiente = a + b
        Imprimir(siguiente)
        a = b
        b = siguiente
        contador += 1
```

A continuación te dejo un diagrama de flujo con la solución del problema:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/c43c1214-5596-45a2-b535-b29a07bc4d6e/Untitled.png)

### 2. Tabla de multiplicar

Escribe un programa que solicite al usuario ingresar un número entero positivo. Luego, utiliza un bucle `while` para imprimir la tabla de multiplicar de ese número, desde 1 hasta 10. Por ejemplo, si el usuario ingresa el número 5, el programa debería imprimir:

```powershell
Tabla de Multiplicar del 5:
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

## ⚙️Python tutor

Cuando quieras probar tu código paso a paso, existe una herramienta muy interesante que te permite corres tu programa y visualizar el estado de cada variable paso a paso. Entra a este link: [**virtual tutor**](https://pythontutor.com/) 

---

# 🔄 Bucle for

El ciclo `for` en programación es una estructura de control que se utiliza para iterar o recorrer elementos en una secuencia (***elemento iterable***), como una lista, una cadena de caracteres, una tupla o un rango de números. A diferencia del ciclo `while`, que se basa en una condición booleana, el ciclo `for` se utiliza principalmente cuando se conoce la cantidad de elementos en la secuencia y se desea realizar una operación específica en cada uno de ellos. El ciclo `for` es especialmente útil para automatizar tareas repetitivas y procesar datos en colecciones, ya que permite recorrer cada elemento de manera ordenada y predecible. En Python, el ciclo `for` se destaca por su sintaxis simple y expresiva, lo que facilita la creación de código legible y eficiente.

```powershell
# Definir una lista de frutas
lista_frutas = ["Manzana", "Banana", "Cereza", "Maracuyá"]

# Utilizar un ciclo for para imprimir cada fruta en la lista
for fruta in lista_frutas:
    print(fruta)
```

Observa el bucle `for`, la variable `fruta` va a **almacenar** el valor de cada elemento de la `lista_frutas`, es decir, en la primera iteración, `fruta` va a almacenar la palabra “Manzana”, en la segunda iteración, “Banana” y así sucesivamente. Esa es la manera como se recorre la lista utilizando el bucle `for`.  

## Función range()

La función `range()` en Python es una función incorporada que se utiliza para generar una secuencia de números enteros en un rango específico. La sintaxis básica de `range()` es la siguiente:

```python
range(inicio, fin-1, paso)
```

- `inicio`: El valor inicial de la secuencia (inclusive).
- `fin`: El valor final de la secuencia (exclusivo). La secuencia se detendrá antes de llegar a este valor.
- `paso` (opcional): El valor que se agregará en cada paso de la secuencia. Por defecto, es 1.

La función `range()` es comúnmente utilizada en combinación con el ciclo `for` para generar iteraciones controladas en un rango específico de números. Aquí hay un ejemplo de cómo se usa `range()` con un ciclo `for`:

```python
# Imprimir los números del 0 al 4
for numero in range(5):
    print(numero)
```

Este código generará la salida:

```yaml
0
1
2
3
4
```

En este ejemplo, `range(5)` genera una secuencia de números desde 0 hasta 4 (inclusive) con un paso de 1, que luego se recorre utilizando el ciclo `for`. Puedes personalizar el inicio, el final y el paso de la secuencia según tus necesidades al utilizar la función `range()` en combinación con el ciclo `for`. Esto es útil para iterar sobre una colección de elementos o realizar tareas repetitivas en un rango de valores específico.

### 📊 Ejercicio 2: usando la función `range()`

Escribe un programa que solicite al usuario ingresar un número entero positivo **`n`**. Luego, utiliza un bucle **`for`** con la función **`range()`** para calcular la suma de todos los números pares desde 1 hasta **`n`**. Finalmente, muestra el resultado de la suma en pantalla.

**Ejemplo de ejecución:**

```yaml
Ingresa un número entero positivo: 6
La suma de los números pares desde 1 hasta 6 es: 12
```

# Ejercicios adicionales con Bucles y Condicionales

## Ejercicios con Bucle While y Condicionales

### Ejercicio 1: Conversor de Temperatura

**Dificultad:** Principiante

Crea un programa que convierta temperaturas entre Celsius y Fahrenheit. El programa debe:

1. Preguntar al usuario si desea convertir de Celsius a Fahrenheit (ingresando 'C') o de Fahrenheit a Celsius (ingresando 'F')
2. Aceptar un valor de temperatura como entrada
3. Realizar la conversión usando la fórmula apropiada
4. Continuar pidiendo conversiones hasta que el usuario ingrese 'Q' para salir

**Entrada:** Un carácter ('C', 'F', o 'Q') y un valor numérico de temperatura
**Salida:** El valor de temperatura convertido con las unidades correspondientes

### Ejercicio 2: Juego de Adivinar el Número

**Dificultad:** Principiante

Desarrolla un juego donde la computadora "piensa" en un número entre 1 y 100, y el usuario debe adivinarlo. El programa debe:

1. Generar un número aleatorio entre 1 y 100
2. Pedir al usuario que adivine el número
3. Indicar si el número ingresado es mayor o menor que el número secreto
4. Contar los intentos que toma el usuario para adivinar el número
5. Mostrar el número de intentos cuando el usuario adivine correctamente

**Entrada:** Números enteros ingresados por el usuario
**Salida:** Pistas ("Mayor", "Menor") y el número de intentos al final

### Ejercicio 3: Calculadora de Interés Compuesto

**Dificultad:** Intermedio

Crea una calculadora de interés compuesto que permita al usuario ver el crecimiento de una inversión año por año. El programa debe:

1. Solicitar el capital inicial, la tasa de interés anual y el número de años
2. Calcular y mostrar el balance al final de cada año
3. Continuar hasta alcanzar el número de años especificado
4. Permitir al usuario decidir si quiere realizar otro cálculo o salir

**Entrada:** Capital inicial, tasa de interés (%), número de años
**Salida:** Balance al final de cada año

**Ejemplo:**

```python
Capital inicial: 1000
Tasa de interés anual: 5
Años: 3

Año 1: $1050.00
Año 2: $1102.50
Año 3: $1157.63
```

### Ejercicio 4: Sistema de Validación de Contraseña

**Dificultad:** Intermedio

Diseña un programa que valide contraseñas según ciertos criterios de seguridad. El programa debe:

1. Solicitar al usuario una contraseña
2. Verificar que la contraseña tenga al menos 8 caracteres
3. Verificar que contenga al menos un número
4. Verificar que contenga al menos una letra mayúscula
5. Verificar que contenga al menos un carácter especial (!, @, #, $, %, etc.)
6. Seguir solicitando una nueva contraseña hasta que cumpla con todos los requisitos
7. Informar al usuario qué requisitos no cumple cada intento

**Entrada:** Cadenas de texto (contraseñas)
**Salida:** Mensajes indicando si la contraseña cumple con los requisitos o qué requisitos faltan

### Ejercicio 5: Aproximación de Pi con el Método de Leibniz

**Dificultad:** Avanzado

Implementa un programa que calcule una aproximación del número π utilizando la serie de Leibniz:
π/4 = 1 - 1/3 + 1/5 - 1/7 + 1/9 - ...

El programa debe:

1. Pedir al usuario el nivel de precisión (número de términos a calcular o error máximo permitido)
2. Calcular π utilizando la serie de Leibniz hasta alcanzar la precisión deseada
3. Mostrar el valor aproximado de π y cuántos términos fueron necesarios
4. Comparar el resultado con el valor de π del módulo math

**Entrada:** Número de términos o error máximo permitido
**Salida:** Aproximación de π, número de términos utilizados y comparación con el valor real

**Ejemplo:**

```
Ingrese precisión (error máximo permitido): 0.001
Aproximación de π: 3.1426...
Número de términos utilizados: 1000
Error absoluto: 0.00097...

```

## Ejercicios con Bucle For y Condicionales

### Ejercicio 6: Generador de Tablas de Multiplicar

**Dificultad:** Principiante

Crea un programa que genere la tabla de multiplicar para un número ingresado por el usuario. El programa debe:

1. Solicitar al usuario un número entero
2. Generar la tabla de multiplicar de ese número del 1 al 12
3. Mostrar las multiplicaciones que resultan en números pares con un formato especial

**Entrada:** Un número entero
**Salida:** La tabla de multiplicar con formato especial para resultados pares

### Ejercicio 7: Calculadora de Factorial

**Dificultad:** Principiante

Desarrolla un programa que calcule el factorial de un número. El programa debe:

1. Pedir al usuario que ingrese un número entero positivo
2. Calcular el factorial de ese número utilizando un bucle for
3. Mostrar cada paso del cálculo (multiplicaciones intermedias)
4. Presentar el resultado final

**Entrada:** Un número entero positivo
**Salida:** Pasos intermedios y resultado final del cálculo factorial

### Ejercicio 8: Verificador de Números Primos

**Dificultad:** Intermedio

Implementa un programa que determine si un número es primo y, en caso de no serlo, muestre sus factores. El programa debe:

1. Solicitar al usuario un número entero positivo mayor que 1
2. Determinar si el número es primo
3. Si no es primo, mostrar todos sus factores
4. Permitir al usuario verificar múltiples números

**Entrada:** Un número entero positivo
**Salida:** Mensaje indicando si el número es primo o no, y sus factores si corresponde

**Ejemplo:**

```
Ingrese un número: 15
15 no es un número primo.
Factores: 1, 3, 5, 15
```

### Ejercicio 9: Suma de Dígitos y Análisis

**Dificultad:** Intermedio

Crea un programa que analice los dígitos de un número. El programa debe:

1. Solicitar al usuario un número entero positivo
2. Calcular la suma de sus dígitos
3. Contar cuántos dígitos son pares y cuántos impares
4. Identificar el dígito más grande y el más pequeño
5. Mostrar todos estos análisis

**Entrada:** Un número entero positivo
**Salida:** Suma de dígitos, conteo de pares e impares, dígito mayor y menor

**Ejemplo:**

```
Ingrese un número: 1234
Suma de dígitos: 10
Dígitos pares: 2 (2, 4)
Dígitos impares: 2 (1, 3)
Dígito mayor: 4
Dígito menor: 1
```

### Ejercicio 10: Generador de Secuencias Numéricas

**Dificultad:** Avanzado

Desarrolla un programa que genere y analice diferentes secuencias numéricas. El programa debe:

1. Ofrecer un menú con varias opciones de secuencias (Fibonacci, triangulares, cuadrados, etc.)
2. Solicitar al usuario cuántos términos desea generar (n)
3. Generar los primeros n términos de la secuencia seleccionada
4. Para cada término generado, indicar si cumple con ciertas propiedades (es primo, es par/impar, etc.)
5. Calcular estadísticas de la secuencia generada (promedio, suma, etc.)

**Entrada:** Tipo de secuencia y número de términos
**Salida:** Términos de la secuencia con análisis de propiedades y estadísticas
Ejemplo:

Seleccione tipo de secuencia:
1. Fibonacci
2. Triangulares
3. Cuadrados perfetos
Opción: 1

Número de términos: 10

Secuencia Fibonacci:
1 (impar)
1 (impar)
2 (par)
3 (impar, primo)
5 (impar, primo)
8 (par)
13 (impar, primo)
21 (impar)
34 (par)
55 (impar)

Estadísticas:
- Suma: 143
- Promedio: 14.3
- Cantidad de primos: 3
- Cantidad de pares: 3
- Cantidad de impares: 7