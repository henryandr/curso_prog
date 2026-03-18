# Reto Unidad 3

---

# ✈️ Reto de Programación: Sistema de Monitoreo de Combustible y Seguridad en Ruta (SMCS)

<aside>
⚠️

**¡Importante!**
No se permite el uso de código no visto en clase.

</aside>

## 🌍 El Contexto (Idea General)

En la aviación comercial, la gestión del combustible es un factor crítico de seguridad y eficiencia. Un avión no solo debe llevar combustible para llegar a su destino, sino también reservas legales para emergencias, desvíos por clima y tiempos de espera. Las condiciones de ruta, como el viento en contra o a favor, alteran dinámicamente el consumo.

## ❓ Pregunta Esencial

*¿Cómo podemos utilizar la lógica computacional para predecir el consumo de combustible de una aeronave en tiempo real y tomar decisiones de desvío automático que garanticen la seguridad del vuelo?*

## 🎯 El Desafío

Eres el ingeniero aeronáutico encargado de programar el **SMCS**, un sistema básico a bordo de un bimotor comercial. El avión tiene una ruta programada que consta de **un número de tramos (waypoints)**. Tu programa debe simular el vuelo, calculando el combustible restante después de cada tramo y tomando decisiones críticas si las reservas se ven comprometidas.

**Reglas del Sistema:**

1. **Capacidad Inicial:** El avión despega con un valor de combustible en el tanque en kilogramos.
2. **Consumo Base:** investiga cuál podría ser un consumo estándar en kilogramos por kilómetro.
3. **Efecto del Viento:**
    - Si hay viento en contra (Headwind), el consumo aumenta en “digamos” un 20%. Este valor, lo debes investigar tú y lo debes justificar. No puede ser el mismo de los otros grupos.
    - Si hay viento a favor (Tailwind), el consumo se reduce en `otro valor` que investigarás también.
    - Si el viento es cruzado o nulo, el consumo es el base.
4. **Reserva Legal:** El avión **nunca** puede bajar de un valor de combustible (este será el límite que tú debes definir). Si al proyectar el siguiente tramo el combustible caerá por debajo de este límite, el sistema debe emitir una alerta crítica, abortar la ruta y aterrizar en el aeropuerto alterno más cercano.

---

## 🛠️ Fases del Proyecto y Entregables (Bitácora)

### Fase 1: Análisis del Problema y Tabla de Datos

Antes de escribir una sola línea de código, un ingeniero debe entender la información que va a procesar.

> 📝 **Entregable 1 - Tablas de Análisis:**
En tu bitácora, crea las siguientes tablas documentando el problema:
> 
> - **Tabla de Entradas (Inputs):** ¿Qué datos necesita recibir el sistema en cada tramo del vuelo?
> - **Tabla de Salidas (Outputs):** ¿Qué información debe mostrarle el sistema al piloto?
> - **Tabla de Constantes y Variables de Control:** Define los valores fijos y las variables que cambiarán durante el bucle. Identifica claramente cuáles son las variables que hacen que el bucle finalice.

### Fase 2: Diseño de la Solución (Algoritmia)

Debes trazar la ruta de la información.

> 🔀 **Entregable 2 - Diagrama o Pseudocódigo:**
Diseña un diagrama de flujo (puedes usar herramientas como [draw.io](http://draw.io/), Lucidchart o a mano) o escribe el pseudocódigo general del programa.
*Asegúrate de mostrar claramente dónde ocurre el **bucle**, dónde están los **condicionales** (decisiones basadas en viento y reservas) y dónde se llama a la **función** de cálculo.*
Sube la imagen o el texto a tu repositorio.
> 

### Fase 3: Código fuente

Basándote en el algoritmo que diseñaste en la fase 2, vas a traducir dicho algoritmo al lenguaje Python. 

> 🤖 **Entregable 3 - Traducción de algoritmo a código:**
> 
> 1. Utilizando los temas vistos en clase, vas a ir traduciendo parte por parte cada uno de los bloques que conforman tu solución. Es muy importante que lo hagas tú mismo. El uso de la IA no está prohibido, pero en caso de hacer uso de esta herramienta, lo debes expresar de forma explícita en tu código. Debes comentar las partes del código donde tuviste ayuda de la IA. 
> 2. **En caso de utilizar IA en partes de tu código, debes realizar una reflexión crítica en tu Bitácora:** Pega el código que te dio la IA. Luego, responde: ¿La IA nombró bien las variables? ¿Usó las estructuras adecuadas? ¿Cometió algún error de lógica o no consideró algún caso? Escribe **qué modificaciones le hiciste** para que encaje perfectamente con la Fase 4.

### Fase 4: Implementación en Python

Desarrolla el código fuente final integrando todos los conceptos vistos en clase.

**Requisitos técnicos obligatorios para el código:**

- **Funciones:** Debes tener al menos una función llamada `calcular_consumo_tramo(distancia, viento)` que retorne los kilogramos consumidos.
- **Bucles:** Utiliza un ciclo `for` o `while` para simular el avance de la aeronave por los 5 tramos de la ruta. (Puedes solicitar al usuario la distancia y el viento en cada iteración usando `input()`).
- **Condicionales y Operadores:** Usa operadores relacionales (`>`, `<=`, etc.) para verificar constantemente si `combustible_actual <= reserva_legal`. Usa `break` para detener el bucle si ocurre una emergencia.

> 💻 **Entregable 4 - Código Fuente Final:**
Sube tu archivo `smcs_vuelo.py` a tu repositorio de GitHub.
Toma capturas de pantalla de la terminal demostrando dos escenarios:
> 
> 1. Un vuelo exitoso que llega a su destino con combustible por encima de la reserva.
> 2. Un vuelo que encuentra demasiado viento en contra y el sistema se ve forzado a abortar la misión por falta de combustible.

---

# 📊 Rúbrica de Evaluación: Sistema de Monitoreo de Combustible (SMCS)

| Criterio de Evaluación | Excelente (100%) | Bueno (75%) | Suficiente (50%) | Insuficiente (0-25%) | Pts |
| --- | --- | --- | --- | --- | --- |
| **1. Análisis de Datos (Fase 1)**
*(15 puntos)* | Crea tablas exhaustivas y precisas. Identifica correctamente todas las entradas (distancia, viento), salidas (combustible restante, alertas), constantes (10,000kg, 1,500kg) y variables de control necesarias para el ciclo. | Las tablas están completas, pero omite o clasifica incorrectamente 1 o 2 variables/constantes menores. El análisis general es correcto. | Las tablas están incompletas. Faltan variables clave como la reserva legal o las entradas de viento, lo que demuestra un análisis superficial. | No presenta el análisis de datos o las tablas no tienen relación con el problema planteado. | **/15** |
| **2. Diseño Algorítmico (Fase 2)**
*(20 puntos)* | El diagrama/pseudocódigo muestra una secuencia lógica impecable. Integra claramente el bucle (número tramos), las decisiones condicionales (viento y reserva) y la invocación a la función de cálculo. | El algoritmo es lógico y funcional, pero tiene fallos menores en la representación gráfica o en la ubicación exacta de las validaciones condicionales dentro del bucle. | El diseño algorítmico presenta errores estructurales graves (ej. el bucle no repite los tramos, o evalúa la reserva después de estrellarse). | No entrega el diagrama/pseudocódigo o este no resuelve el problema de los 5 tramos. | **/20** |
| **3. Traducción a Código y Uso Ético/Crítico de IA (Fase 3**
*(20 puntos)* | Traduce fielmente su algoritmo a Python. Si usó IA: lo comenta explícitamente en el código y presenta una profunda reflexión crítica en la bitácora (analizando variables, estructuras, errores y detallando sus modificaciones). Si NO usó IA: lo declara claramente y su código demuestra dominio propio coherente con su diagrama. | La traducción es buena pero tiene desconexiones menores con la Fase 2. Si usó IA: comenta el código y hace la reflexión, pero esta carece de profundidad (no explica *por qué* modificó el código) o viceversa. | La traducción omite partes del algoritmo. Si usó IA: declara haberla usado pero NO lo comenta en las líneas de código correspondientes, o NO presenta la reflexión crítica exigida en la bitácora. | Hay evidencia clara de uso de IA (código avanzado/no visto en clase, variables ajenas a su diseño) que **no fue declarada**, o no hay ningún intento de traducir el diagrama diseñado en la Fase 2. | **/20** |
| **4. Estructuras Python y Funcionalidad (Fase 4)**
*(30 puntos)* | El código incluye de forma correcta: Función (`def`), Bucle (`for`/`while`), Condicionales (`if`/`elif`/`else`) y Operadores. El cálculo matemático es exacto y el programa se detiene correctamente (`break`) si se viola la reserva legal. | El código utiliza las estructuras requeridas y funciona casi en su totalidad, pero tiene errores lógicos menores (ej. falla en la exactitud matemática del descuento del 10% o mal manejo de mayúsculas en el input). | Faltan una o más estructuras obligatorias exigidas (no usó funciones o no usó bucles). El programa corre, pero no respeta la reserva legal o ignora la penalización/beneficio del viento. | El código tiene errores de sintaxis graves que impiden su ejecución o no aplica los conceptos fundamentales de la unidad (Condicionales, Bucles, Funciones). | **/30** |
| **5. Pruebas, Evidencias y Repositorio**
*(15 puntos)* | Sube todos los entregables (archivos `.py` y bitácora `.md`) al repositorio. Incluye capturas de pantalla de los 2 escenarios exigidos (vuelo exitoso y vuelo abortado) demostrando el funcionamiento de la terminal. | Sube el código y bitácora, pero falta la demostración gráfica de 1 de los escenarios de prueba, o el repositorio no tiene el formato/nomenclatura solicitada. | Sube el código, pero no incluye las capturas de ejecución o los escenarios probados no demuestran que las alertas de emergencia funcionen realmente. | No utiliza el repositorio asignado, entrega por otros medios no autorizados o no presenta pruebas de funcionamiento. | **/15** |
| **Puntaje Total** |  |  |  |  | **/100** |