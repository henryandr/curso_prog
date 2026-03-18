# Operadores

## Descubriendo los Operadores en Python

¡Te damos la bienvenida a tu primer gran paso en el mundo de la programación!

Para que un programa sea útil, necesita procesar información: calcular totales, comparar datos o tomar decisiones lógicas. Aquí es donde entran los **operadores**.

> 🧐 **Pregunta Orientadora:** Piensa en tu día a día. ¿Cuántas veces realizas cálculos mentales (como saber si te alcanza el dinero) o tomas decisiones basadas en condiciones (como "si llueve Y hace frío, llevo abrigo")? ¿Cómo crees que le enseñamos a una computadora a hacer exactamente lo mismo?
> 
> 
> 📓 **Bitácora:** Reflexiona sobre esta pregunta y escribe una breve respuesta (2-3 líneas) en la bitácora de tu repositorio antes de continuar.
> 

Python ofrece una amplia gama de operadores para realizar distintos tipos de operaciones. Hoy dominaremos los tres principales: **aritméticos, relacionales y lógicos**.

---

## 1. Operadores Aritméticos 🧮

Se utilizan para realizar operaciones matemáticas básicas. Funcionan de manera muy similar a la calculadora de tu teléfono.

| **Operador** | **Descripción** | **Ejemplo mental** |
| --- | --- | --- |
| `+` | Suma | `5 + 2 = 7` |
| `-` | Resta | `5 - 2 = 3` |
| `*` | Multiplicación | `5 * 2 = 10` |
| `/` | División (resultado decimal) | `5 / 2 = 2.5` |
| `//` | División entera (ignora decimales) | `5 // 2 = 2` |
| `%` | Módulo (residuo de la división) | `5 % 2 = 1` |
| `**` | Potenciación | `5 ** 2 = 25` |

**Ejemplo de uso en código:**

```python
a = 10
b = 3

suma = a + b
resta = a - b
multiplicacion = a * b
division = a / b
division_entera = a // b
modulo = a % b
potenciacion = a ** b

print("Suma:", suma)
print("División exacta:", division)
print("División entera:", division_entera)
print("Módulo (lo que sobra):", modulo)
```

> 💡 **Ejercicio 1: La cuenta del restaurante**
Imagina que fuiste a cenar con 3 amigos (son 4 en total). La cuenta fue de $85. Además, quieren dejar un 15% de propina.
Escribe un programa en Python que calcule:
> 
> 1. El total de la propina.
> 2. El total a pagar (cuenta + propina).
> 3. Cuánto debe pagar cada uno, dividiendo en partes iguales.
> 
> 📤 **Acción en Bitácora:** Crea un archivo llamado `ejercicio1_aritmetica.py`, resuelve el problema y sube el código junto con una captura de pantalla de la ejecución a la bitácora de tu repositorio.
> 

---

## 2. Operadores Relacionales (Comparación) ⚖️

Los operadores relacionales se utilizan para comparar dos valores. El resultado de esta comparación **siempre** será un valor Booleano: `True` (Verdadero) o `False` (Falso).

| **Operador** | **Descripción** | **Ejemplo (`x=5`, `y=10`)** |
| --- | --- | --- |
| `==` | Igual que (¡Ojo! Son dos símbolos `=`) | `x == y` *(False)* |
| `!=` | Diferente que | `x != y` *(True)* |
| `>` | Mayor que | `x > y` *(False)* |
| `<` | Menor que | `x < y` *(True)* |
| `>=` | Mayor o igual que | `x >= 5` *(True)* |
| `<=` | Menor o igual que | `y <= 5` *(False)* |

**Ejemplo de uso en código:**

```python
edad_usuario = 20
edad_minima = 18

es_mayor = edad_usuario >= edad_minima
es_exacto = edad_usuario == 20

print("¿El usuario es mayor de edad?", es_mayor)
print("¿Tiene exactamente 20 años?", es_exacto)
```

> 💡 **Ejercicio 2: El guardián de la montaña rusa**
Para subir a la nueva montaña rusa del parque, los visitantes deben medir al menos 150 cm.
Escribe un programa donde declares una variable `altura_visitante` (asígnale el valor que quieras). Luego, utiliza un operador relacional para imprimir `True` si puede subir o `False` si no puede.
> 
> 
> 📤 **Acción en Bitácora:** Escribe tu solución, pruébala con una altura de 145 y otra de 160. Sube tus hallazgos a la bitácora de tu repositorio.
> 

---

## 3. Operadores Lógicos 🧠

A veces no basta con hacer una sola pregunta; necesitamos evaluar múltiples condiciones al mismo tiempo. Aquí entran los operadores lógicos.

| **Operador** | **Descripción** | **¿Cuándo es `True`?** |
| --- | --- | --- |
| `and` | Y lógico | Solo si **AMBAS** condiciones son verdaderas. |
| `or` | O lógico | Si **AL MENOS UNA** de las condiciones es verdadera. |
| `not` | NO lógico (Inversión) | Invierte el valor (de `True` a `False` y viceversa). |

**Ejemplo de uso en código:**

```python
tiene_boleto = True
esta_vacunado = False

# Para entrar al concierto necesita ambas cosas:
puede_entrar = tiene_boleto and esta_vacunado
print("¿Puede entrar al concierto?", puede_entrar) # Resultado: False

# Para recibir descuento debe ser estudiante O adulto mayor:
es_estudiante = True
es_adulto_mayor = False
tiene_descuento = es_estudiante or es_adulto_mayor
print("¿Tiene descuento?", tiene_descuento) # Resultado: True
```

> 💡 **Ejercicio 3: Sistema de Becas**
Una universidad otorga becas a los estudiantes si cumplen **alguna** de estas dos condiciones:
> 
> - Tener un promedio mayor o igual a 9.0.
> - Estar en un nivel socioeconómico nivel 1 **Y** tener un promedio mayor a 8.0.
> 
> 📤 **Acción en Bitácora:** Diseña la lógica en Python utilizando variables y operadores relacionales y lógicos. Sube tu análisis y código a la bitácora de tu repositorio explicando cómo funciona la evaluación de tu programa.
> 

---

## 🚀 Reto Final de la Semana

¡Es hora de poner a prueba todo lo que has aprendido juntando los tres tipos de operadores!

> 🏆 **Reto Final: El Validador de Videojuegos**
> 
> 
> Estás programando la lógica de una tienda de videojuegos en línea. Un usuario quiere comprar un juego de clasificación "M" (Mature / Para mayores de 17 años) que cuesta $60.
> 
> Crea un programa que declare las siguientes variables:
> 
> - `edad_usuario` (asigna un número)
> - `saldo_billetera` (asigna un número decimal)
> - `tiene_suscripcion_premium` (asigna `True` o `False`)
> 
> Tu programa debe evaluar y guardar en una variable llamada `compra_exitosa` (que será True o False) si el usuario puede comprar el juego.
> 
> **Condiciones para que la compra sea exitosa:**
> 
> 1. El usuario debe tener al menos 17 años.
> 2. El usuario debe tener suficiente saldo en su billetera. ¡Pero atención! Si tiene suscripción premium, el juego tiene un 10% de descuento.
> 
> *Pista: Primero calcula el precio final usando operadores aritméticos y luego evalúa la lógica con operadores relacionales y lógicos.*
> 
> 📤 **Acción en Bitácora:** Sube el código de tu Reto Final a tu repositorio en un archivo llamado `reto_operadores.py`. En tu archivo Markdown de bitácora, explica brevemente qué se te dificultó más de este reto y cómo lo resolviste. ¡Mucho éxito!
>