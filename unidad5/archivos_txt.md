# Archivos de texto

## **Introducción**

En el mundo de la programación, existen dos tipos principales de archivos:

1. **Archivos de texto:** Almacenan información de manera legible para los seres humanos, utilizando caracteres y símbolos (como un documento de Word, código fuente o archivos de configuración).
2. **Archivos binarios:** Almacenan información en un formato que solo la máquina puede entender y procesar directamente, como imágenes, videos o ejecutables.

En esta sección nos enfocaremos principalmente en los **archivos de texto**.

### **Secuencia para el manejo de archivos**

Observa el siguiente gráfico que describe los pasos fundamentales para interactuar con un archivo en Python:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/e85947fd-13cd-4a0f-8385-db83dd765800/Untitled.png)

1. **Apertura:** Crear la conexión entre tu programa y el archivo.
2. **Lectura/Escritura:** Extraer datos del archivo o guardar nueva información en él.
3. **Cierre:** Liberar los recursos del sistema y guardar los cambios.
4. **Manejo de errores:** Asegurar que el programa no colapse si el archivo no existe o falla un permiso.

## **Tema 1: Apertura, Modos y Cierre de Archivos**

### **📖 Teoría**

Para interactuar con un archivo, primero debemos usar la función integrada `open()`. Esta función nos devuelve un "objeto archivo" que nos permitirá manipular su contenido. Cuando terminamos, **siempre** debemos usar el método `.close()` para liberar la memoria.

```powershell
var_archivo = open("nombre_archivo.txt", "modo")
```

## Modos de apertura

Existen diferentes **modos de apertura** según lo que queramos hacer:

- **`r` (Read - Lectura):** Es el modo por defecto. Abre el archivo solo para leer. *El archivo debe existir, de lo contrario dará error.*
- **`w` (Write - Escritura):** Abre el archivo para escribir. *Si el archivo ya existe, borra todo su contenido previo (lo sobrescribe).* Si no existe, lo crea.
- **`a` (Append - Adición):** Abre el archivo para escribir, pero *agrega el texto al final* sin borrar lo que ya estaba escrito.

Escritura (w) siempre sobrescribe el archivo. Adición (a) escribe al final del archivo. Lectura (r) necesita que el archivo exista, de otro modo, producirá un error.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/02c0faed-67db-4983-90f8-e5241784386a/Untitled.png)

### **💻 Ejemplo**

```python
# Abre (o crea) un archivo en modo escritura
mi_archivo = open("saludo.txt", "w")
mi_archivo.write("Hola, mundo!")
mi_archivo.close() # ¡Muy importante cerrar!
```

### **🏃‍♂️ Ejercicio 1**

1. Abre tu bloc de notas (o cualquier editor de texto) y crea un archivo. Escribe en él tres líneas de texto.
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/f062088d-9fe2-49d9-b0fc-8c4babb505e8/Untitled.png)
    
2. Guárdalo con el nombre: `texto.txt` exactamente en la misma carpeta donde crearás tu script de Python.
3. Crea un script en Python llamado `leer.py` y copia el siguiente código:

```python
fp = open("texto.txt", "r")
datos_1 = fp.read(5)
print("Primera lectura:", datos_1)

datos_2 = fp.read(5)
print("Segunda lectura:", datos_2)
fp.close()
```

### **🧠 Preguntas de comprensión**

1. ¿Cuál es la diferencia en el resultado impreso entre la primera y la segunda llamada al método `read()`?
2. ¿Por qué no se imprimen los mismos datos en ambas lecturas, si el código es exactamente igual? *(Pista: Piensa en un "cursor" que avanza mientras lees).*
3. ¿Por qué es obligatorio utilizar el método `close()` al final?

## **Tema 2: Técnicas de Lectura**

### **📖 Teoría**

Una vez abierto un archivo en modo lectura (`r`), Python nos ofrece tres métodos principales para extraer su texto:

- `read(cantidad)`: Lee la cantidad especificada de caracteres. Si lo dejas vacío `read()`, lee **todo** el archivo de golpe.
- `readline()`: Lee una sola línea hasta encontrar el salto de línea (`\n`).
- `readlines()`: Lee todas las líneas y devuelve una **lista** de Python, donde cada elemento es una línea.

### **💻 Ejemplo**

```python
fichero = open("texto.txt", "r")
primera_linea = fichero.readline()
print("La primera línea es:", primera_linea)
fichero.close()
```

### **🏃‍♂️ Ejercicio 2**

Crea un nuevo script y prueba la función `readlines()` con el archivo `texto.txt` que creaste en el ejercicio anterior:

```python
fichero = open("texto.txt", "r")
todas_las_lineas = fichero.readlines()
print(todas_las_lineas)
fichero.close()
```

### **🧠 Preguntas de comprensión**

1. Al imprimir el resultado de `readlines()`, ¿qué estructura de datos (tipo de variable) observas en la consola?
2. ¿Notaste el símbolo `\n` al final de cada frase impresa? ¿Qué significa ese símbolo?

## **Tema 3: Escritura de Archivos**

### **📖 Teoría**

Para escribir, usamos el modo `w` (sobrescribir) o el modo `a` (añadir al final). Los métodos principales son:

- `write(texto)`: Escribe una cadena de texto en el archivo. No agrega saltos de línea automáticamente, debes incluir `\n` manualmente si quieres cambiar de renglón.
- `writelines(lista_de_textos)`: Escribe una lista de cadenas en el archivo.

### **💻 Ejemplo**

```python
archivo = open("log.txt", "a")
archivo.write("Nueva entrada de registro\n")
archivo.close()
```

### **🏃‍♂️ Ejercicio 3**

Copia y ejecuta el siguiente código que genera números aleatorios y guarda sus estadísticas en un archivo:

```python
from random import randint

lista = []
for i in range(50):
    lista.append(randint(0, 100))

maximo = str(max(lista))
minimo = str(min(lista))
prom = str(sum(lista)/len(lista))

file_datos = open("datos.txt", "w")
file_datos.write("El valor máximo es: " + maximo + "\n")
file_datos.write("El valor mínimo es: " + minimo + "\n")
file_datos.write("El promedio es: " + prom + "\n")
file_datos.close()
print("Archivo creado con éxito. Revisa tu carpeta.")
```

### **🧠 Preguntas de comprensión**

1. ¿Qué pasaría con el archivo `datos.txt` si ejecutas este mismo script 3 veces seguidas? ¿Tendrías 3 reportes o solo 1? ¿Por qué?
2. Si quisieras que el programa guardara el historial completo de cada ejecución sin borrar el anterior, ¿qué modificarías en el código?

## **Tema 4: La forma "Pythónica" (Contextos con `with`)**

### **📖 Teoría**

En Python, la mejor práctica para manejar archivos es usar la sentencia **`with`**. Esto crea un "contexto de ejecución". ¿La mayor ventaja? **Python se encarga de llamar a `.close()` de manera automática** en el momento en que el bloque de código termina, incluso si ocurre un error inesperado a la mitad. Esto evita fugas de memoria y bloqueos de archivos.

### **💻 Ejemplo**

Compara la forma antigua vs la nueva:

```python
# Forma antigua
f = open("datos.txt", "r")
contenido = f.read()
f.close()

# Forma moderna (Recomendada)
with open("datos.txt", "r") as f:
    contenido = f.read()
# ¡Ya está cerrado automáticamente aquí!
```

### **🏃‍♂️ Ejercicio 4**

Ejecuta el siguiente programa que interactúa con el usuario utilizando `with`:

```python
nombre_archivo = input("Nombra tu nuevo archivo (ej: diario.txt): ")

# Contexto de escritura
with open(nombre_archivo, 'w') as archivo:
    datos = input("Escribe tu primer secreto: ")
    archivo.write(datos)

# Contexto de lectura
with open(nombre_archivo, 'r') as archivo:
    print("\n--- Leyendo tu archivo ---")
    print(archivo.read())
```

### **🧠 Preguntas de comprensión**

1. En el código del Ejercicio 4, ¿en qué línea exacta se cierra el archivo después de escribir el secreto?
2. ¿Por qué usar `with` hace que el código sea "más seguro" frente a fallas del sistema?

## **Tema 5: Navegando el Sistema de Archivos (Rutas / Paths)**

### **📖 Teoría**

Hasta ahora, hemos asumido que el archivo y el script de Python están en la **misma carpeta** (Ruta Relativa). Pero en la vida real, los archivos están organizados en diferentes carpetas.

Para manejar direcciones (Paths) de manera profesional y sin preocuparnos si estamos en Windows (`\`) o Mac/Linux (`/`), Python incluye una librería maravillosa llamada `pathlib`.

### **💻 Ejemplo**

```python
from pathlib import Path

# Construimos una ruta hacia una carpeta específica
ruta_carpeta = Path("mis_documentos/finanzas")
# Creamos la carpeta si no existe
ruta_carpeta.mkdir(parents=True, exist_ok=True)

# Apuntamos a un archivo dentro de esa carpeta
ruta_archivo = ruta_carpeta / "reporte.txt"

with open(ruta_archivo, "w") as f:
    f.write("Reporte financiero generado.")
```

### **🏃‍♂️ Ejercicio 5**

Crea un script que verifique si un archivo existe antes de intentar leerlo, usando `.exists()`:

```python
from pathlib import Path

archivo_buscado = Path("texto.txt")

if archivo_buscado.exists():
    print("¡El archivo existe! Procediendo a leer...")
    with open(archivo_buscado, "r") as f:
        print(f.read())
else:
    print("Lo siento, el archivo no se encuentra en esa ruta.")
```

### **🧠 Preguntas de comprensión**

1. ¿Cuál es la diferencia entre una ruta **absoluta** (ej: `C:/Usuarios/Juan/texto.txt`) y una ruta **relativa** (ej: `texto.txt`)?
2. ¿Por qué es mejor usar `Path` (de la librería `pathlib`) en lugar de simplemente concatenar textos como `"carpeta" + "/" + "archivo.txt"`?

## **Tema 6: Manejo de Errores y Excepciones**

### **📖 Teoría**

Cuando trabajamos con archivos, muchas cosas pueden salir mal: el archivo fue borrado, el disco duro está lleno, o no tenemos permisos de administrador. Si Python encuentra un error, el programa colapsará ("crasheará") y se detendrá.

Para evitar esto, usamos los bloques `try` (intentar) y `except` (excepción). Esto nos permite capturar el error y tomar una decisión elegante sin que el programa muera.

### **💻 Ejemplo**

```python
try:
    with open("archivo_que_no_existe.txt", "r") as f:
        print(f.read())
except FileNotFoundError:
    print("Error: Estás intentando abrir un archivo que no existe.")
```

### **🏃‍♂️ Ejercicio 6**

Modifica este código para evitar que el programa colapse. Envuélvelo en un bloque `try-except`:

```python
# Código propenso a errores (Si el usuario escribe algo mal, el programa explota)
nombre = input("Dime qué archivo quieres leer: ")

# TODO: Añade el bloque try - except aquí
with open(nombre, "r") as archivo:
    print(archivo.read())

print("Fin del programa. Gracias por usar nuestro sistema.")
```

### **🧠 Preguntas de comprensión**

1. ¿Qué sucedería en el código del Ejercicio 6 si no usas `try-except` y el usuario ingresa un archivo inexistente? ¿Llegaría a imprimirse la frase "Fin del programa..."?
2. Además de `FileNotFoundError`, ¿qué otro problema del mundo físico/real crees que podría causar un error al intentar guardar datos en un archivo?

# Material complementario

## Página web

El siguiente material pertenece al sitio web: [**freecampcode.org**](https://www.freecodecamp.org/espanol/news/python-como-escribir-en-un-archivo-abrir-leer-escribir-y-otras-funciones-de-archivos-explicadas/) 

Autora: **Estefania Cassingena Navone**

[**Python cómo escribir en un archivo - abrir, leer, escribir y otras funciones de archivos explicadas**](https://www.freecodecamp.org/espanol/news/python-como-escribir-en-un-archivo-abrir-leer-escribir-y-otras-funciones-de-archivos-explicadas/)

## Video en Youtube sobre archivos

**Fuente**: Canal de Youtube **UskoKruM2010**

https://youtu.be/71xSLk8l25Q?si=UammTRGS8MPxo2mG