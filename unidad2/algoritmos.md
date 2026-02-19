# Actividad 2: Representación de algoritmos

## Introducción

Un **algoritmo** es un conjunto de pasos o instrucciones secuenciales que permiten resolver un problema.

![Figura 1. Representación de un algoritmo de forma gráfica.](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/6b9c9772-e8ce-4645-9668-1fd7f2c7cc3e/image.png)

Figura 1. Representación de un algoritmo de forma gráfica.

Existen dos tipos principales:

1. **Cualitativos**: Describen pasos a través de palabras. Por ejemplo, las instrucciones para preparar una receta de cocina, como "mezclar los ingredientes" u "hornear durante 30 minutos", constituyen un algoritmo cualitativo.
2. **Cuantitativos**: Incluyen cálculos numéricos. Por ejemplo, un algoritmo para calcular el volumen de una caja: `Volumen = Largo * Ancho * Alto`.

## Características de los Algoritmos

Un buen algoritmo debe cumplir las siguientes características:

- **Precisión**: Los pasos deben ser claros y concisos. Te voy a poner un ejemplo de lo que no se debe hacer: un algoritmo que diga `Suma los números ingresados y muestra el resultado` sin especificar cómo ingresarlos, cómo procesarlos ni cómo mostrarlos. Este nivel de ambigüedad genera confusión y dificulta su implementación correcta.
- **Determinismo**: Dados los mismos datos de entrada, siempre produce el mismo resultado. Por ejemplo, si mi algoritmo calcula el factorial de un número entero, cada vez que yo le ingrese 5, el resultado será 120, no importa cuántas veces ejecute el programa.
- **Finitud**: Debe terminar en un tiempo razonable y no caer en ciclos infinitos. Aquí te voy a dar otro ejemplo de lo que no se debe hacer: Un algoritmo que incluye una condición mal diseñada:

```powershell
Leer x
Mientras (x != 10) { x = x - 2 }
```

Si `x` empieza siendo impar, nunca alcanzará el valor 10 y el ciclo será infinito.

Un bucle sin límite de iteraciones:

```cpp
Para i desde 0 hasta infinito { imprimir(i) }
```

Este bucle no tiene fin y puede colapsar el sistema.

Estos ejemplos ilustran problemas comunes a evitar en el diseño de algoritmos.

## Etapas del Diseño de Algoritmos

1. Análisis del problema: esta etapa consiste en desglosar completamente el problema a resolver.

![Figura 2. Etapas para la solución de un problema mediante un algoritmo.](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/712824f7-9a79-45e9-96ba-4d0e0010bade/image.png)

Figura 2. Etapas para la solución de un problema mediante un algoritmo.

Se deben identificar claramente:

- **Entradas**: Datos que el algoritmo recibirá.
- **Salidas**: Resultados esperados que el algoritmo debe generar.
- **Restricciones**: Condiciones o límites que se deben cumplir.
- **Procesos**: Operaciones necesarias para transformar las entradas en salidas.
- Además, se debe verificar si hay ambigüedades en el enunciado del problema y resolverlas antes de proceder.

<aside>
💡

**Ejemplo**: Si el problema es calcular el promedio de calificaciones de un grupo de estudiantes, las entradas son las calificaciones individuales, la salida es el promedio y el proceso es sumar las calificaciones y dividirlas entre el número total de estudiantes.

</aside>

1. **Diseño del algoritmo**: esta etapa implica desarrollar un plan detallado para resolver el problema identificado. Se deben definir los pasos lógicos necesarios y las herramientas que se emplearán, como estructuras de control, variables y constantes. Además, se puede optar por representar el algoritmo utilizando pseudocódigo, diagramas de flujo u otros medios visuales para garantizar su claridad y comprensión. El objetivo principal es asegurar que el diseño sea fácil de traducir a un lenguaje de programación y que aborde de manera eficiente el problema identificado.
2. **Verificación del algoritmo**: en esta etapa, se comprueba que el diseño del algoritmo sea correcto y cumpla con los requisitos planteados. Se revisan los pasos propuestos para garantizar que produzcan las salidas esperadas a partir de las entradas especificadas. Esto puede incluir pruebas manuales utilizando datos de ejemplo, análisis lógico del flujo del algoritmo y simulaciones en herramientas de software. Además, es importante validar la eficiencia del algoritmo y verificar que no existan errores o redundancias que puedan impactar negativamente en su rendimiento.

    <aside>
    💡

    Ejemplo: Si el algoritmo calcula el promedio de calificaciones, se puede verificar manualmente con un conjunto pequeño de datos como `[80, 90, 70]`. Calcular manualmente el promedio `(80 + 90 + 70) / 3 = 80`, y confirmar que el algoritmo produce el mismo resultado.

    </aside>

3. **Implementación en código**: esta etapa consiste en traducir el diseño del algoritmo a un lenguaje de programación específico. Para ello, es fundamental seleccionar un lenguaje que se adapte a los requerimientos del problema y a las capacidades del programador. Durante la implementación, se deben seguir buenas prácticas, como:
    - Usar nombres descriptivos para las variables y funciones.
    - Comentar el código para explicar bloques o partes complejas.
    - Modularizar el programa dividiéndolo en funciones o módulos.
    - Es importante mantener un enfoque iterativo, verificando continuamente que las partes del código implementadas funcionen correctamente antes de avanzar.
4. **Pruebas y correcciones**: en esta etapa, se evalúa la funcionalidad del algoritmo implementado para garantizar que produce los resultados esperados en todos los casos posibles. Se realizan pruebas con diferentes conjuntos de datos, tanto normales como extremos, para identificar posibles errores. Las pruebas también permiten verificar el rendimiento del algoritmo, asegurándose de que es eficiente en términos de tiempo y uso de recursos. Si se encuentran fallos, se depura el código, ajustando las partes problemáticas del algoritmo y repitiendo el proceso de prueba hasta lograr la corrección completa.
    - **Ejemplo**: Para un programa que calcula el área de un triángulo, probar con valores normales (base = 10, altura = 5), valores límite (base = 0 o altura = 0), y datos inválidos (como caracteres en lugar de números), para confirmar que el algoritmo responde adecuadamente a cada caso.

## Herramientas para Diseñar y Representar Algoritmos

![](https://images.unsplash.com/photo-1515879218367-8466d910aaa4?ixlib=rb-4.0.3&q=85&fm=jpg&crop=entropy&cs=srgb)

## **Pseudocódigo**

Es una representación en lenguaje natural de los pasos que conforman un algoritmo. Se utiliza para describir de manera estructurada y comprensible las acciones necesarias para resolver un problema antes de implementarlo en un lenguaje de programación.

Por ejemplo, para calcular el área de un triángulo:

```
Inicio
Leer base, altura
area = (base * altura) / 2
Mostrar area
Fin
```

## **Diagramas de flujo**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/b3fd3e5c-48ba-4de4-b3e5-6a17014694d6/image.png)

Representación gráfica de las operaciones lógicas del algoritmo. Utilizan un conjunto de símbolos estándar como óvalos para representar inicio y fin, rectángulos para procesos, y rombos para decisiones. Esto permite visualizar de manera clara y secuencial el flujo de ejecución del algoritmo, facilitando la comprensión y detección de errores.

## 📤 Ejercicio 1

Investiga cuáles son los símbolos que se utilizan para representar cada operación de un algoritmo con un diagrama de flujo. Asegúrate de que la fuente es confiable, discute lo que encontraste con tus compañeros y con el profe. Cuando estés seguro/a de tener los símbolos correctos, consigna la información en la bitácora.

## 📔 Reglas para el uso de diagramas de flujo

1. Todo diagrama de flujo debe tener un **inicio y** un **fin.**
2. Las líneas utilizadas para indicar la dirección del flujo del  diagrama deben ser rectas: verticales u horizontales.
3. Todas las líneas utilizadas para indicar la dirección del flujo  del diagrama deben estar conectadas. La conexión puede  ser a un símbolo que exprese lectura, proceso, decisión,  impresión, conexión o fin del diagrama.
4. El diagrama de flujo debe construirse de arriba hacia abajo  (*top-down*) y de izquierda a derecha (*left to right* ).
5. La notación utilizada en el diagrama de flujo debe ser  independiente del lenguaje de programación.
6. Al realizar una tarea compleja, es conveniente poner  comentarios que expresen o ayuden a entender lo que  hayamos hecho.
7. Si la construcción del diagrama de flujo requiriera más de  una hoja, debemos utilizar los conectores adecuados y  enumerar las páginas correspondientes.
8. No puede llegar más de una línea a un símbolo  determinado

## Ejemplo

Para calcular el volumen de un cubo:

1. Inicio
2. Leer A, B y C.
3. volumen = A*B*C
4. Mostrar: volumen
5. Fin.

![Figura 3. Diagrama de Flujo](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/16f3fed9-a7bc-4090-b437-ac4d571fea18/image.png)

Figura 3. Diagrama de Flujo

En un diagrama de flujo, cada paso se conecta mediante flechas que indican el orden de las operaciones.

## Conceptos Básicos: Identificadores

- **Variable**: Valor que cambia durante la ejecución. Ejemplo: sueldo, pago, descuento.
- **Constante**: Valor fijo. Ejemplo: PI = 3.141592.

## Estructuras de Control

## **Estructuras secuenciales**

Pasos que se ejecutan uno tras otro. Por ejemplo, encontrar la suma y la multiplicación de dos números enteros.

![Figura 4. Diagrama de flujo de un algoritmo secuencial. Fuente: https://www.tutorialesprogramacionya.com/delphiya/detalleconcepto.php?punto=6&codigo=88&inicio=0](attachment:566e10b2-8a49-49d5-8e2f-ca2c4e068dd1:image.png)

Figura 4. Diagrama de flujo de un algoritmo secuencial. Fuente: <https://www.tutorialesprogramacionya.com/delphiya/detalleconcepto.php?punto=6&codigo=88&inicio=0>

## Ejercicio 2

Analicemos el siguiente problema y representemos su solución mediante un algoritmo secuencial.

- Construye un algoritmo que, al recibir como datos **el ID** del empleado y los seis primeros sueldos del año, calcule el ingreso total semestral y el promedio mensual, e imprima el ID del empleado, el ingreso total y el promedio mensual.

## **Estructuras selectivas**: Involucran la toma de decisiones

Observa el símbolo que representa la comparación y fíjate que tiene 2 salidas, una cuando el resultado de la comparación es verdadero (V) y otra cuando es falso (F). No hay más opciones. Por ejemplo, determinar si un número es par o impar.

![Figura 5. Estructura selectiva.](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/48f547b8-96a0-44c7-8dea-47181d3d5096/image.png)

Figura 5. Estructura selectiva.

# Operadores Relacionales

Igual a                  =

Mayor que          >

Mayor o igual     ≥

Menor que         <

Menor o igual   ≤

Diferente            ≠

## Ejemplo

Implementar un algoritmo para determinar cuál de dos valores proporcionados es el mayor. Representarlo con pseudocódigo y diagrama de flujo

### Pseudocódigo

Inicio
Leer A, B
Si A > B:
      M = A
Si no
      M = B
Fin Si
Escribir “el mayor es”, M
Fin

### Diagrama de flujo

![Figura 6. Diagrama de flujo para determinar cuál de dos números es mayor.](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/fb4f9ef2-10db-4f6b-8f12-de59512275ca/image.png)

Figura 6. Diagrama de flujo para determinar cuál de dos números es mayor.

## Ejercicios

1. Un **acuario** necesita determinar cuántos litros o galones (eso lo decide el usuario) de agua caben en un acuario, pero solo dispone de una cinta métrica (en centímetros). Diseña un algoritmo para solucionar el problema.
2. Realice un algoritmo para determinar cuánto se debe pagar por equis cantidad de lápices considerando que si son 1000 o más el costo es de $85 cada uno; de lo contrario, el precio es de $90. Represéntelo con el pseudocódigo y el diagrama de flujo.
3. Un almacén de ropa tiene una promoción: por compras superiores a $250 000 se les aplicará un descuento de 15%, de caso contrario, sólo se aplicará un 8% de descuento. Realice un algoritmo para determinar el precio final que debe pagar una persona por comprar en dicho almacén y de cuánto es el descuento que obtendrá. Represéntelo mediante el pseudocódigo y el diagrama de flujo.
4. El director de una escuela está organizando un viaje de estudios, y requiere determinar cuánto debe cobrar a cada alumno y cuánto debe pagar a la compañía de viajes por el servicio. La forma de cobrar es la siguiente: si son 100 alumnos o más, el costo por cada alumno es de $65.00; de 50 a 99 alumnos, el costo es de $70.00, de 30 a 49, de $95.00, y si son menos de 30, el costo de la renta del autobús es de $4000.00, sin importar el número de alumnos.

## 🔂 Bucles o Ciclos

Un bucle en programación es una estructura de control que permite ejecutar repetidamente un bloque de código mientras se cumple una condición específica o durante un número determinado de iteraciones. Son fundamentales para automatizar tareas repetitivas, realizar cálculos iterativos y procesar grandes conjuntos de datos. En el lenguaje C, existen tres tipos principales de bucles: **for**, **while**, y **do-while**. El bucle **for** se utiliza cuando se conoce de antemano la cantidad de iteraciones, especificando un inicio, una condición y un incremento o decremento. El bucle **while** ejecuta el bloque de código mientras la condición sea verdadera, siendo útil cuando no se conoce el número exacto de iteraciones. Finalmente, el bucle **do-while** es similar al **while**, pero garantiza que el bloque de código se ejecute al menos una vez, ya que evalúa la condición al final de cada iteración. Estas estructuras son herramientas esenciales para la resolución eficiente de problemas en C.

## for

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/52b4fa76-c1b8-4364-b3b9-a8af40da55ee/image.png)

## while

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/129f5400-f8f7-4356-afcc-f345307c1277/image.png)

## do-while

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/72af9375-9e66-4378-8927-847284d9ba97/image.png)

## Ejemplo 1

Se requiere un algoritmo para obtener la suma de diez cantidades, que se leen del teclado, mediante la utilización de un ciclo `while`. Realice el diagrama de flujo y el pseudocódigo.

## Pseudocódigo

Inicio
SU = 0
C = 1
Mientras C < = 10
     Leer VA
     SU = SU + VA
     C = C + 1
Fin mientras
Escribir SU
Fin

## Diagrama de flujo

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/64fe6dfe-53ec-467d-ac31-dc18bf6c1b57/image.png)

## Ejemplo 2

Se requiere un algoritmo para obtener la suma de diez cantidades mediante la utilización de un ciclo `for`. Realice el diagrama de flujo y el pseudocódigo.

## Pseudocódigo

Inicio
SU = 0
Desde C = 1 hasta C = 10
     Leer VA
     SU = SU + VA
Fin desde
Escribir SU
Fin

## Diagrama de flujo

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/86ff57e3-0a96-46be-a958-59ebefbb5e94/96f8503b-96d6-4daa-9ed1-2dbe8efe314f/image.png)

## Actividad de Evaluación: Comprensión de Conceptos

![](https://images.unsplash.com/photo-1606326608606-aa0b62935f2b?ixlib=rb-4.0.3&q=85&fm=jpg&crop=entropy&cs=srgb)

# 📤 **Consigna tus respuestas en la bitácora**

A continuación, se presentan enunciados relacionados con los temas tratados en el texto. Los estudiantes deben responder si los enunciados corresponden o no con las definiciones o conceptos aprendidos.

### Parte 1: Identificar Algoritmos

Responde si los siguientes enunciados representan un algoritmo. Justifica la respuesta:

1. Una página web.
2. Una receta para hacer un pastel, donde se indican ingredientes y pasos a seguir.
3. "Piensa en un número y multiplícalo por otro".
4. Un manual de instrucciones para armar un mueble, con pasos detallados y un orden claro.
5. Una lista de compras organizada en orden alfabético

### Parte 2: Variables y Constantes

Indica si las siguientes afirmaciones describen una variable o una constante:

1. El valor de la gravedad en la Tierra, 9.8 m/s².
2. La edad de una persona calculada con base en el año actual y su año de nacimiento.
3. La cantidad de dinero en una cuenta bancaria.
4. La velocidad de la luz en el vacío, 299,792,458 m/s.
5. El radio de un círculo.

### Parte 3: Características de los Algoritmos

Responde si los siguientes enunciados cumplen con las características de un algoritmo. Justifica la respuesta:

1. Para elegir la ruta más corta entre varias ciudades, el algoritmo examina rutas candidatas, deteniéndose cuando los cambios en la distancia parecen lo suficientemente pequeños.
2. Suma los números ingresados y muestra el resultado.
3. Un conjunto de pasos para calcular el área de un rectángulo dado su base y altura.
4. El algoritmo cuenta el número de votos obtenidos por cada uno de los candidatos de una elección para presidente. Empieza solicitando el nombre del candidato y finaliza cuando se ingresa el valor -1.

### Parte 4: Comprensión de Herramientas

Indica si las siguientes afirmaciones son ciertas o falsas respecto al pseudocódigo y diagramas de flujo:

1. El pseudocódigo utiliza símbolos estándar para representar las operaciones lógicas.
2. Los diagramas de flujo son una representación gráfica de un algoritmo.
3. El pseudocódigo debe estar escrito en un lenguaje de programación específico.
4. Un diagrama de flujo siempre debe tener un inicio y un fin claramente definidos.

### Parte 5: Estructuras de Control

Describe para qué sirven las estructuras de control. Redacta dos ejemplos, uno de tu vida diaria, es decir cuando tienes que tomar decisiones en tus actividades diarias y oto ejemplo en el que se tengan que utilizar cálculos matemáticos para tomar una u otra decisión.

---
