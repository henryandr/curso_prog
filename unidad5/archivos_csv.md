# Archivos CSV

# ❇️ Archivos separados por comas (CSV)

# **Introducción**

Los archivos CSV (Valores Separados por Comas) son un formato común para almacenar e intercambiar datos. Python proporciona varias bibliotecas y métodos para leer y escribir archivos CSV. En este tutorial, exploraremos cómo leer y escribir archivos CSV utilizando Python.

## **Lectura de Archivos CSV**

Para leer un archivo CSV, puedes utilizar la biblioteca `csv` de Python. Aquí tienes un ejemplo:

```python
import csv

with open('ejemplo.csv', 'r') as csvfile:   #usamos el manejador de contexto
    lector = csv.reader(csvfile) #se utiliza el método reader
    for fila in lector:          #con el for se itera sobre el objeto para leer
        print(fila)
```

En este ejemplo, abrimos el archivo `ejemplo.csv` en modo de lectura (`'r'`) y creamos un objeto `lector` utilizando la función `csv.reader`. El objeto `lector` es un iterador que devuelve cada fila del archivo CSV como una lista.

## Parámetro newline en modo lectura

El parámetro `newline` en el método `open` se utiliza para especificar el carácter de nueva línea que se utilizará en el archivo. En este caso, el parámetro `newline` se establece en `''`, lo que significa que no se utilizará ningún carácter de nueva línea especial.

En Python 3.x, el método `open` utiliza un carácter de nueva línea especial llamado `newline` para indicar el fin de la línea. Sin embargo, algunos archivos CSV pueden utilizar un carácter de nueva línea diferente, como `\\r\\n` o `\\n`. Si no se especifica un carácter de nueva línea, el método `open` puede interpretar incorrectamente el archivo.

Por ejemplo, si un archivo CSV utiliza `\\r\\n` como carácter de nueva línea, pero el método `open` utiliza `\\n` como carácter de nueva línea por defecto, el archivo puede no ser leído correctamente.

Al especificar `newline=''`, se indica que no se utilizará ningún carácter de nueva línea especial, lo que permite que el método `open` lea el archivo correctamente.

En resumen, el parámetro `newline` se utiliza para especificar el carácter de nueva línea que se utilizará en el archivo, lo que ayuda a evitar problemas de lectura incorrecta de archivos CSV.

Aquí tienes un ejemplo de cómo se utiliza el parámetro `newline` en el método `open`:

```python
with open('eggs.csv', newline='') as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(row)
```

En este ejemplo, el parámetro `newline` se establece en `''`, lo que indica que no se utilizará ningún carácter de nueva línea especial. Esto ayuda a evitar problemas de lectura incorrecta del archivo CSV.

## Ejercicio 1

Practica el método reader que acabas de aprender. Crea un archivo separado por comas e intenta leerlo utilizando el código anterior. Este archivo será útil en los siguientes ejemplos. 

## **Lectura de Archivos CSV con Encabezados**

Si tu archivo CSV tiene encabezados, puedes especificar la fila de encabezados utilizando la función `csv.reader`:

```python
import csv

with open('ejemplo.csv', 'r') as csvfile:
    lector = csv.reader(csvfile)
    encabezados = next(lector)  # Lee la fila de encabezados
    for fila in lector:
        print(fila)

```

En este ejemplo, utilizamos la función `next` para leer la fila de encabezados y almacenarla en la variable `encabezados`. Luego, iteramos sobre las filas restantes utilizando el objeto `lector`.

## Ejercicio 2

Bueno, ya te puedes imaginar el siguiente ejercicio. Agrega un encabezado a los datos que creaste atneriormente, ahora prueba el código anterior para serciorarte de que entendiste el concepto. 

## Ejercicio 3

Ahora hagamos algo diferente. Abre tu archivo separado por comas en el block de notas, ahora presiona `Ctrl+R` para reemplazar las comas de tu archivo por el símbolo `:` (dos puntos). Recuerda que los archivos CSV no usan exclusivamente la coma para separar los valores, pueden aparecer otro tipo de símbolos y debes estar preraparado para manejarlos. 

Ahora intenta nuevamente leer el archivo, con los códigos vistos anteriormente.

Discute con tus compañeros y con el profesor lo que sucede y cuál es la causa. 

> **¿Cómo podrías solucionar el problema?** Investiga y comparte la respuesta con tus compañeros y profesor.
> 

## **Escritura de Archivos CSV**

Para escribir un archivo CSV, puedes utilizar la biblioteca `csv` de Python de nuevo. Aquí tienes un ejemplo:

```python
import csv

with open('salida.csv', 'w', newline='') as csvfile:
    escritor = csv.writer(csvfile)
    escritor.writerow(['Nombre', 'Edad', 'Ciudad'])  # Escribe la fila de encabezados
    escritor.writerow(['John', 25, 'Nueva York'])
    escritor.writerow(['Jane', 30, 'Los Ángeles'])

```

En este ejemplo, abrimos el archivo `salida.csv` en modo de escritura (`'w'`) y creamos un objeto `escritor` utilizando la función `csv.writer`. Luego, escribimos la fila de encabezados utilizando el método `writerow` y dos filas adicionales.

## Parámetro newline en modo escritura

El parámetro `newline` en la función `open()` en Python se utiliza para especificar el carácter de nueva línea que se utilizará en el archivo. Por defecto, el parámetro `newline` se establece en `None`, lo que significa que el carácter de nueva línea se determinará según el sistema operativo en el que se está ejecutando el programa.

Sin embargo, en algunos casos, es posible que desees especificar un carácter de nueva línea específico para que se utilice en el archivo. Por ejemplo, si estás trabajando con un archivo que contiene caracteres de nueva línea en formato de Windows (`\\r\\n`), puedes especificar el parámetro `newline` como `'\\r\\n'` para que se utilice este carácter de nueva línea en el archivo.

Aquí te muestro un ejemplo:

```python
with open('example.txt', 'w', newline='\\r\\n') as f:
    f.write('Hello, world!')
```

En este ejemplo, se abre un archivo llamado `example.txt` en modo de escritura (`'w'`) y se especifica que se utilizará el carácter de nueva línea `\\r\\n` en el archivo. Luego, se escribe el texto `'Hello, world!'` en el archivo.

Es importante tener en cuenta que el parámetro `newline` solo se aplica cuando se abre el archivo en modo de escritura (`'w'`) o en modo de actualización (`'a'`). Si se abre el archivo en modo de lectura (`'r'`), el parámetro `newline` no tiene efecto.

## Ejercicio 4

Crea un archivo separado por comas utilizando el anterior código. 

## **Escritura de Archivos CSV con Citas**

Si necesitas escribir archivos CSV con valores citados, puedes utilizar la función `csv.writer` con el parámetro `quoting` establecido en `csv.QUOTE_ALL`:

```python
import csv

with open('salida.csv', 'w', newline='') as csvfile:
    escritor = csv.writer(csvfile, quoting=csv.QUOTE_ALL)
    escritor.writerow(['Nombre', 'Edad', 'Ciudad'])  # Escribe la fila de encabezados
    escritor.writerow(['John', 25, 'Nueva York'])
    escritor.writerow(['Jane', 30, 'Los Ángeles'])

```

En este ejemplo, establecemos el parámetro `quoting` en `csv.QUOTE_ALL`, lo que citará todos los valores en el archivo CSV, pero… **¿qué son archivos csv con citas?**

💡 **!Excelente pregunta!**

La "Escritura de Archivos CSV con Citas" se refiere a la capacidad de citar los valores en un archivo CSV para que sean más fáciles de leer y entender.

En un archivo CSV, los valores suelen estar separados por comas (o otros caracteres de separación). Sin embargo, en algunos casos, los valores pueden contener comas o otros caracteres especiales que pueden causar problemas al leer el archivo. Por ejemplo, si un valor contiene una coma, el programa que lee el archivo CSV puede interpretar que es un separador de valores en lugar de un valor real.

Para solucionar este problema, se utiliza la citación de valores. La citación de valores es un mecanismo que permite rodear los valores con comillas (o otros caracteres) para que sean más fáciles de leer y entender.

En Python, la biblioteca `csv` proporciona la capacidad de citar los valores al escribir un archivo CSV utilizando el parámetro `quoting` en la función `csv.writer`. El parámetro `quoting` puede tener los siguientes valores:

- `csv.QUOTE_MINIMAL`: Citará los valores que contengan comas o otros caracteres especiales.
- `csv.QUOTE_ALL`: Citará todos los valores, incluyendo aquellos que no contengan comas o caracteres especiales.
- `csv.QUOTE_NONNUMERIC`: No citará los valores numéricos, pero sí citará los valores que contengan comas o caracteres especiales.

En el ejemplo que te mostré anteriormente, se utiliza `csv.QUOTE_ALL` para citar todos los valores en el archivo CSV. Esto significa que todos los valores, incluyendo aquellos que no contengan comas o caracteres especiales, serán rodeados con comillas para que sean más fáciles de leer y entender.

En resumen, la "Escritura de Archivos CSV con Citas" se refiere a la capacidad de citar los valores en un archivo CSV para que sean más fáciles de leer y entender, lo que puede ser especialmente útil cuando se trabajan con datos que contienen comas o caracteres especiales.

## Otros métodos de escritura

Además del método `writerow` que utilizamos anteriormente, hay otros métodos de `csv` que se pueden utilizar para escribir un archivo CSV. Aquí te menciono algunos de ellos:

1. `writerows`: Este método es similar al `writerow`, pero se utiliza para escribir varias filas en el archivo CSV de una sola vez.
2. `writerow` con `extrasaction`: Este método se utiliza para escribir una fila en el archivo CSV y especificar qué acción se debe realizar si se produce un error al escribir la fila.
3. `writerow` con `newline`: Este método se utiliza para escribir una fila en el archivo CSV y especificar el carácter de nueva línea que se utilizará en el archivo.
4. `writerow` con `dialect`: Este método se utiliza para escribir una fila en el archivo CSV y especificar el dialecto que se utilizará para leer y escribir el archivo.

Aquí tienes un ejemplo de cómo se utiliza el método `writerows` para escribir varias filas en un archivo CSV:

```python
import csv

with open('example.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile)
    writer.writerows([
        ['Name', 'Age', 'City'],
        ['John', 25, 'New York'],
        ['Jane', 30, 'Los Angeles'],
        ['Bob', 35, 'Chicago']
    ])
```

En este ejemplo, se utiliza el método `writerows` para escribir varias filas en el archivo CSV. El método `writerows` acepta una lista de listas, donde cada lista representa una fila en el archivo CSV.

## **Recursos Adicionales**

- Documentación de Python: https://docs.python.org/3/library/csv.html
- Documentación de la biblioteca `csv`: https://docs.python.org/3/library/csv.html