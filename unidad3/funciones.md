# Funciones

## Introducción

En Python, las funciones y módulos son componentes esenciales para organizar y reutilizar código de manera eficiente. Las funciones permiten encapsular un conjunto de instrucciones bajo un nombre y pueden recibir parámetros para realizar tareas específicas. Por otro lado, los módulos son archivos que contienen funciones, variables y clases relacionadas, que pueden ser importados en otros programas para facilitar la modularidad y la reutilización de código. Ambos conceptos son fundamentales para escribir programas Python más limpios y estructurados.

Algunas ventajas de la programación con funciones son:

- **Modularización**: permite segmentar un programa complejo en una serie de partes o módulos más simples, facilitando así la programación y el depurado.
- **Reutilización**: permite reutilizar una misma función en distintos programas.

## Estructura de una Función

Una función está compuesta principalmente por tres elementos:

- Nombre de la función (identificador)
- Parámetros de entrada (variables entre los paréntesis) `*opcional`
- Resultados o elementos de salida (`return`) `*opcional`
- Dos puntos (`:`), indican donde inicia el bloque de código de la función

Los parámetros de entrada y resultados no son de obligatorios para la definición de una función.

Observa la siguiente imagen para que veas la estructura de una función:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/794d3fb8-211e-4d0c-a024-467bc450ae9d/Untitled.png)

Observa el siguiente ejemplo, la palabra clave `def` se utiliza para definir lo que hace la función, luego se pone el nombre o identificacor, seguidamente entre paréntesis los parámetros de entrada y por último los dos puntos `(:)`. El bloque de código de la función debe estar ***indentado***. 

```python
def suma(a, b):
	resultado = a + b
	return resultado

#Llamando a la función
numero1 = 5
numero2 = 3
resultado_suma = suma(numero1, numero2)
print(f"{numero1} + {numero2} = {resultado_suma}")
print(suma(9898,564))
suma(45, 78)
```

## Argumentos Vs Parámetros

Los parámetros de la función son **`a`** y **`b`**, y cuando llamamos a la función **`suma(5, 3)`**, estamos pasando los argumentos 5 y 3, que se asignarán a **`a`** y **`b`** respectivamente dentro de la función.

<aside>
🔥 Las variables que se colocan dentro de los paréntesis cuando se llama a una función se llaman **"argumentos"** o **"parámetros"** de la función, dependiendo del contexto. Se llaman **argumentos,** cuando se utilizan en la llamada de la función (cuando se envían). Se llaman **parámetros** en la definición de la función (cuando se reciben).

</aside>

## Funciones propias de Python

En la siguiente tabla encontrarás algunas de las muchas funciones propias de Python y una breve descripción. Revisa si ya has utilizado algunas de ellas, seguramente lo has hecho. 

| **Función** | **Descripción** |
| --- | --- |
| `print()` | Imprime un mensaje o valor en la consola. |
| `len()` | Devuelve la longitud (número de elementos) de un objeto. |
| `input()` | Lee una entrada del usuario desde la consola. |
| `range()` | Genera una secuencia de números dentro de un rango. |
| `type()` | Devuelve el tipo de un objeto. |
| `str()` | Convierte un valor a una cadena de caracteres. |
| `int()` | Convierte un valor a un entero. |
| `float()` | Convierte un valor a un número de punto flotante. |
| `list()` | Crea una lista a partir de un iterable. |
| `dict()` | Crea un diccionario. |
| `set()` | Crea un conjunto. |
| `len()` | Devuelve la longitud de un objeto iterable. |
| `max()` | Devuelve el valor máximo en un iterable. |
| `min()` | Devuelve el valor mínimo en un iterable. |
| `sum()` | Calcula la suma de los elementos en un iterable. |

## Funciones y métodos

En Python, las funciones y los métodos son dos conceptos clave, y la principal diferencia entre ellos radica en su asociación con los objetos.

---

## Objetos en Python

Aquí voy a hacer un paréntesis para recordarte lo que es un objeto. Este concepto es sumamente importanet en lenguajes de programación como Python.

<aside>
💡 **Recordemos**: un objeto es una entidad que combina datos (atributos) y funciones (métodos) que operan en esos datos. Los objetos son `instancias` de `clases`, que son plantillas o moldes que definen cómo se comportarán esos objetos. Cada objeto tiene un tipo, como una cadena, una lista o incluso un objeto personalizado definido por el usuario. Los objetos son fundamentales en la programación orientada a objetos (POO) y permiten organizar y manipular datos de manera estructurada y eficiente.

</aside>

Te voy a dejar este corto video para que te hagas una idea más clara sobre los objetos y las clases en Python. 

https://youtube.com/shorts/BeI81t_NDDc?si=BNu9NLzYfrMGOi17

---

### Funciones en Python

Las funciones son bloques de código independientes que pueden recibir parámetros y realizar tareas específicas. No están vinculadas a un objeto particular y se pueden llamar desde cualquier parte del código. Por ejemplo, la función `len()` se utiliza para obtener la longitud de cualquier objeto iterable, como una lista o una cadena.

```python
lista = [1, 2, 3]
longitud = len(lista) # Llamando a la función len() en una lista
>>> 3
```

### **Métodos de objetos:**

Los métodos son funciones específicas de un objeto en particular. Cada tipo de objeto en Python (como listas, cadenas, diccionarios, etc.) tiene sus propios métodos que pueden utilizarse para realizar acciones específicas relacionadas con ese tipo de objeto. Los métodos están vinculados al objeto y se llaman usando la notación de punto. Por ejemplo, el método `append()` se utiliza para agregar un elemento a una lista.

```python
mi_lista = [1, 2, 3]
mi_lista.append(4)  # Llamando al método append() en una lista
```

## Ejercicio 1

- Abre la consola de Python y ejecuta el siguiente comando:

```python
institucion = "Universidad Pontificia Bolivariana"
type(institucion)
```

Seguramente obtendrás como resultado esto:

`<class 'str'>`

El comando **`type()`** en Python determina y devuelve el tipo de datos de un objeto o valor dado. Puedes utilizar **`type()`** para averiguar si una variable es una cadena de caracteres, un número entero, un número de punto flotante, una lista, un diccionario u otro tipo de dato.

- Luego ejecuta este comando:

```python
dir(institucion)
```

Y vas a obtener mucha más información:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/a0ee46a5-0cb6-4c73-89d1-3f464718e56a/Untitled.png)

El comando **`dir()`** en Python es una función integrada que se utiliza para obtener una lista de todos los atributos y métodos disponibles de un objeto. Puedes usar **`dir()`** para explorar la estructura y funcionalidad de un objeto en Python.

## Ejercicio 2

Es hora de ver lo que has aprendido, hagamos un poco de ***“[retrieval practice](https://escuelaconcerebro.wordpress.com/2022/08/01/la-practica-de-recuperacion-la-tecnica-de-estudio-y-aprendizaje-mas-efectiva/)”.*** Sin mirar los apuntes, trata de contestar las siguientes preguntas. Escribe las respuestas en tus apuntes:

- [ ]  ¿Cuál es la diferencia entre función y método?
- [ ]  Trata de recordar al menos cinco funciones propias de `Python`
- [ ]  Con tus propias palabras, describe para qué sirve el comando `dir()`
- [ ]  ¿Cómo se llaman las variables que se ponen dentro de los paréntesis cuando se llama a una función?
- [ ]  Describe la diferencia que hay entre los términos argumentos y parámetros

## Dónde ubicar las funciones en mi archivo de Python

<aside>
⚠️ **Importante**: Las funciones siempre se declaran al principio del archivo.

</aside>

La estructura de un programa con funciones es:

```python
# Definición de la primera función
def funcion1(parametros1):
    # Código función 1
    return valor1

# Definición de la segunda función
def funcion2(par1,par2):
    # Código función 2
    return valor1,valor2

# Definición de la tercera función
def funcion3(par1,par2,par3):
    # Código función 3
    return valor3

# Función principal
def main():
    # Llamada a la función saludar
    var1 = funcion1(argumentos1)
    # Llamada a la función calcular_promedio
    var1, var2 = funcion2(arg1,arg2)
    # Llamada a la función imprimir_resultado
    var3 = funcion3(arg1,arg2,arg3)

# Llamada a la función principal para iniciar el programa
if __name__ == "__main__":
    main()
```

## Orden de los parámetros

Cuando envía argumentos a una función, estos se reciben por orden en los parámetros definidos. Observa la siguiente imagen y fíjate que el argumento 1 (`48`) se copia en el parámetro 1 (`Num1`) y el argumento 2 (`6`) se copia en el parámetro 2 (`Num2`).

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/ea3e307d-65be-424d-9adb-d63dfcc50d76/Untitled.png)

Sin embargo, en algunas ocasiones, cuando se conoce el nombre de los parámetros, se pueden usar en la llamada a la función. En ese caso, no importa el orden en el que se ubiquen los argumentos. Mira el siguiente ejemplo:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/d8e01c94-b1f2-4509-81bc-fda21f8d408b/Untitled.png)

Ten cuidado de utilizar correctamente la llamada a la función. De otro modo, podrías causar errores de sintaxis. Observa el ejemplo de la siguiente imagen. 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/00e3bfc5-abd6-4ac2-8abf-9930b0df0cab/Untitled.png)

## Ejercicio 4

Reproduce el caso de la imagen anterior en la consola de Python, lee el error y trata de interpretarlo. ¿Sabes cómo corregir el error? Si la respuesta es afirmativa, corrígelo y mira como se ejecuta el código, de lo contrario, pide una explicación al profesor. 

## Una posible solución al error anterior

En la definición de la función, puedes definir **parámetros por defecto**, en caso de que el usuario no ponga argumentos en la llamada de la función, puedes configurar unos valores preestablecidos. Mira los dos ejemplos en la siguiente imagen. 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/ea8b93f3-bcf5-459d-ab06-f496694c28bc/Untitled.png)

Ahora trata de interpretar que hace cada una de las funciones. 

## Tipo de valor especial None

<aside>
💡 En Python, `None` es un valor especial que se utiliza para representar la ausencia de un valor o la falta de definición de una variable o función. Puedes pensar en `None` como un marcador que indica que no hay un valor válido presente en ese contexto.

</aside>

Algunos casos comunes en los que se utiliza `None` incluyen:

1. Cuando una función no tiene una instrucción `return` explícita o cuando una función no devuelve nada, implícitamente se considera que devuelve `None`.

```python
def funcion_vacia():
    # Esta función no devuelve nada explícitamente, por lo que devuelve None

```

1. Cuando una variable se declara, pero aún no se le asigna un valor, su valor predeterminado es `None`.

```python
mi_variable = None  # La variable mi_variable se inicializa con None

```

1. Cuando se elimina un elemento de una lista o diccionario, el valor en esa ubicación se convierte en `None`.

```python
mi_lista = [1, 2, 3]
del mi_lista[1]  # Ahora, mi_lista es [1, None, 3]

```

### Cantidad de argumentos arbitrarios

Puedes pasar una cantidad indeterminada de parámetros a una función en Python utilizando argumentos arbitrarios.

**`args`** (Argumentos posicionales arbitrarios):

- Permite pasar una cantidad variable de argumentos posicionales a una función.
- Los argumentos se reciben como una tupla.
- Debes preceder el nombre de los argumentos con un asterisco (*).

Ejemplo:

```python
pythonCopy code
def mi_funcion(*args):
    for arg in args:
        print(arg)

mi_funcion(1, 2, 3)  # Puedes pasar cualquier cantidad de argumentos
```

## Retorno de valores (salida de datos)

En Python, la declaración `return` se utiliza en una función para especificar qué valor o valores desea que la función devuelva como resultado. La forma en que uses `return` depende de si deseas devolver uno o más valores.

**Devolver un solo valor:**
Cuando deseas devolver un solo valor desde una función, simplemente utilizas `return` seguido del valor que deseas devolver. Por ejemplo:

```python
def suma(a, b):
    resultado = a + b
    return resultado  # Devuelve el resultado de la suma

resultado_suma = suma(5, 3)
```

En este caso, la función `suma` devuelve un solo valor, que es el resultado de la suma de `a` y `b`.

**Devolver múltiples valores:**
Si deseas devolver más de un valor desde una función, puedes hacerlo envolviendo esos valores en una tupla, una lista o cualquier otro tipo de objeto contenedor. Luego, usas `return` para devolver ese objeto contenedor. Por ejemplo:

```python
def obtener_nombre_y_edad():
    nombre = "Juan"
    edad = 30
    return nombre, edad  # Devuelve una tupla con nombre y edad

nombre, edad = obtener_nombre_y_edad()

```

En este caso, la función `obtener_nombre_y_edad` devuelve dos valores, un nombre y una edad, en forma de una tupla, y luego podemos desempaquetar esos valores cuando llamamos a la función.

## Ejercicio 5

Resuelve los siguientes ejercicios con lo aprendido en la clase de hoy:

### **Problema 1: Conversión de Puntuación**

Escribe una función llamada **`convertir_puntuacion()`** que tome una puntuación numérica (de 0 a 100) como argumento. La función debe devolver una letra de calificación según la siguiente escala:

- Si la puntuación está entre 90 y 100, devuelve "A".
- Si la puntuación está entre 80 y 89, devuelve "B".
- Si la puntuación está entre 70 y 79, devuelve "C".
- Si la puntuación está entre 60 y 69, devuelve "D".
- Si la puntuación está por debajo de 60, devuelve "F".

Asegúrate de manejar casos en los que la puntuación esté fuera de este rango, por ejemplo, mostrar "Puntuación inválida" si es negativa.

### **Problema 2: Determinar el Día de la Semana**

Escribe una función llamada **`determinar_dia()`** que tome un número entero del 1 al 7 como argumento. La función debe devolver el nombre del día de la semana correspondiente (por ejemplo, 1 = "Lunes", 2 = "Martes", etc.). Asegúrate de manejar casos en los que el número esté fuera de este rango y devuelva "Número de día inválido".

## Exploremos los Métodos

<aside>
✏️ A continuación realizarás una serie de ejercicios para que comprendas el uso de los **métodos** asociados a ciertos objetos en `Python`

</aside>

## **Métodos de los objetos tipo string**

Las cadenas de caracteres en Python tienen una variedad de métodos que permiten realizar diversas operaciones. Para explorar estos métodos, sigue estos pasos:

1. **Crear una Cadena**: Define una cadena de caracteres a la que quieras aplicar métodos. Por ejemplo:

```python
mi_cadena = "Ingeniería Aeronáutica"
```

1. **Usar el Operador de Punto (.)**: Para acceder a los métodos de una cadena, utiliza el operador de punto seguido del nombre de la cadena y luego el nombre del método. Por ejemplo:
    
    ```python
    # Ejemplo de método: mayúsculas
    mi_cadena_mayusculas = mi_cadena.upper()
    ```
    

## Ejercicio 6

**Explorar Métodos**: Ahora, puedes explorar varios métodos de cadenas. Algunos ejemplos comunes incluyen:

- **`.upper()`**: Convierte la cadena a mayúsculas.
- **`.lower()`**: Convierte la cadena a minúsculas.
- **`.replace(subcadena, nueva_subcadena)`**: Reemplaza subcadenas.
- **`.split(separador)`**: Divide la cadena en una lista utilizando un separador.
- **`.strip()`**: Elimina espacios en blanco al principio y al final.

## **Métodos de los objetos tipo int**

Los enteros en Python tienen sus propios métodos y operadores. Para explorarlos, sigue estos pasos:

1. **Definir un Entero**: Crea una variable con un valor entero. Por ejemplo:
    
    ```python
    mi_entero = 42
    ```
    
2. **Operadores Matemáticos**: Los enteros admiten operadores matemáticos como **`+`**, `-`, `*`, **`/`**, etc. Utilízalos para realizar cálculos.
3. **Métodos de Enteros**: Los enteros en Python tienen algunos métodos útiles, como:
    - **`.bit_length()`**: Devuelve la cantidad mínima de bits necesarios para representar el número.

## **Métodos de los objetos tipo float**

Los números de punto flotante en Python, es decir, los números decimales, también tienen sus propios métodos. Para explorarlos:

1. **Definir un Número de Punto Flotante**: Crea una variable con un valor de punto flotante. Por ejemplo:
    
    ```python
    mi_punto_flotante = 3.14159
    ```
    
2. **Métodos de Punto Flotante**: Algunos métodos útiles para números de punto flotante incluyen:
- **`.is_integer()`**: Verifica si el número es un entero.
- **`.as_integer_ratio()`**: Devuelve el número como una fracción.