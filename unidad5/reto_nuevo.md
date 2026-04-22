# Reto Unidad 5: Análisis Visual de Datos Reales

---

# **Título:** Explorador CLI para el Análisis y Visualización de Archivos Reales

## **Objetivo:**

Desarrollar una aplicación de interfaz de línea de comandos (CLI) en Python enfocada en el procesamiento, análisis estadístico y visualización de conjuntos de datos del mundo real. A diferencia de ejercicios anteriores, los estudiantes trabajarán con archivos `.txt` (como *logs* de servidores o libros clásicos) y `.csv` (datos abiertos como clima, ventas o censos), extrayendo conclusiones fundamentadas mediante múltiples tipos de gráficos.

---

## **Requerimientos de la Aplicación:**

La aplicación debe ser interactiva, robusta ante errores (como archivos faltantes) y presentar el siguiente flujo:

### **Menú Principal**
1. **Explorar directorio:** Listar todos los archivos `.txt` y `.csv` disponibles en una ruta especificada por el usuario.
2. **Procesar Bitácoras / Textos Reales (.txt)**
3. **Analizar Dataset de Datos Abiertos (.csv)**
4. **Salir**

### **Submenú 1: Procesamiento de Textos (.txt)**
*(Ejemplo de archivos reales: Logs de acceso de un servidor web, o un libro de dominio público).*
- **Resumen Estadístico del Texto:** Mostrar cantidad total de líneas, palabras, caracteres (con y sin espacios) y el top 5 de palabras más repetidas (excluyendo conectores).
- **Extracción de Patrones (Logs):** Si es un archivo de *log*, extraer y contar cuántos errores (ej. "ERROR", "404") o fechas específicas aparecen.
- **Gráfico 1 - Frecuencia de Palabras Clave:** Generar un gráfico de barras horizontales (`barh`) mostrando las 10 palabras más frecuentes.
- **Gráfico 2 - Distribución de Longitud de Líneas:** Generar un histograma (`hist`) que agrupe cuántas líneas tienen entre 0-50 caracteres, 51-100, etc.

### **Submenú 2: Análisis de Datasets (.csv)**
*(Ejemplo de archivos reales: Registro de temperaturas anuales, ventas mensuales de una tienda, o datos demográficos).*
- **Vista Previa de Datos:** Imprimir en consola las primeras 10 filas y las últimas 5 para entender la estructura.
- **Cálculo de Estadísticas Descriptivas:** El usuario selecciona una columna numérica. El sistema debe limpiar los datos nulos/vacíos y calcular: Total de registros válidos, Promedio, Mediana, Valor Máximo y Valor Mínimo.
- **Gráfico 3 - Evolución Temporal / Tendencia:** El usuario selecciona dos columnas (ej. Fechas vs. Ventas o Temperaturas) y el sistema genera un gráfico de líneas (`plot`).
- **Gráfico 4 - Comparación Categórica:** El usuario selecciona una columna categórica (ej. "Ciudad" o "Categoría de Producto") y el sistema genera un gráfico de pastel (`pie`) con los porcentajes de participación.
- **Gráfico 5 - Correlación de Variables:** El usuario selecciona dos columnas numéricas y el sistema genera un gráfico de dispersión (`scatter`) para ver la relación entre ambas.

---

## **Cronograma de Trabajo (3 Semanas)**

El reto está diseñado para desarrollarse progresivamente durante las clases:

### **Semana 1: Infraestructura y Exploración**
- **Clase 1:** Definición del dataset real a utilizar. Creación de la estructura del menú principal y la función para listar archivos en el directorio usando `pathlib` o `os`.
- **Clase 2:** Implementación de la lectura de archivos `.txt`, manejo de errores (`try-except` para `FileNotFoundError`) y cálculos básicos (conteo de palabras).

### **Semana 2: Procesamiento Estructurado y CSV**
- **Clase 3:** Implementación del módulo `csv` para leer los datasets. Limpieza de datos (ignorar filas vacías o con formato incorrecto).
- **Clase 4:** Desarrollo de las funciones matemáticas para calcular las estadísticas descriptivas en columnas específicas del CSV.

### **Semana 3: Visualización de Datos y Cierre**
- **Clase 5:** Integración de la biblioteca `matplotlib.pyplot`. Desarrollo de los gráficos 1, 2 y 3.
- **Clase 6:** Desarrollo de los gráficos 4 y 5. Pruebas finales, depuración de código y preparación del video de sustentación.

---

## **Entregables**

Para dar por superado el reto, el equipo o estudiante deberá entregar estrictamente lo siguiente:

1. **Código Fuente (`main.py` y módulos):** Subido al repositorio correspondiente, estructurado en funciones, aplicando las mejores prácticas y sin usar librerías externas no vistas en clase (a excepción de `matplotlib`).
2. **Archivos de Datos (`/data`):** Los archivos `.txt` y `.csv` reales que se utilizaron para probar la aplicación.
3. **Carpeta de Resultados (`/outputs`):** Al menos 5 imágenes (PNG o JPG) guardadas con los gráficos generados por el programa durante el análisis.
4. **Documento de Análisis (`README.md`):** 
   - Breve explicación de los datos elegidos (¿De dónde salieron? ¿Qué representan?).
   - 3 conclusiones reales que hayan descubierto al observar los gráficos de sus datos.
5. **Video de Sustentación (5–8 minutos):** 
   - Ejecución del programa en vivo demostrando los flujos.
   - Explicación rápida de cómo se manejó la lectura de archivos y la creación de un gráfico específico.

---

## **Rúbrica de Evaluación**

| Criterio | Excelente (5.0 - 4.5) | Bueno (4.4 - 3.5) | Aceptable (3.4 - 3.0) | Insuficiente (< 3.0) |
| :--- | :--- | :--- | :--- | :--- |
| **Funcionalidad (Lectura y Escritura)** | El programa lee correctamente ambos formatos, maneja errores sin cerrarse y limpia los datos de forma robusta. | Lee ambos formatos, pero el manejo de errores es básico o se rompe con datos nulos. | Solo procesa correctamente un tipo de archivo o tiene fallos frecuentes al leer. | El programa no logra abrir los archivos o colapsa inmediatamente. |
| **Visualización (Gráficos)** | Genera los 5 gráficos solicitados. Todos tienen título, etiquetas en los ejes (X y Y) y son comprensibles. | Genera la mayoría de los gráficos, pero faltan títulos o etiquetas en los ejes. | Genera gráficos básicos, a menudo usando el tipo de gráfico equivocado para los datos. | No genera gráficos o las visualizaciones están vacías/rotas. |
| **Lógica y Código Limpio** | Código modularizado en funciones, nombres de variables descriptivos, comentarios pertinentes. Uso correcto de `with open()`. | Código funcional pero algo repetitivo o funciones demasiado largas. Usa `with`. | Lógica confusa, código espagueti. Olvida cerrar archivos o usa métodos obsoletos. | Código incomprensible, dependiente de IA sin comprensión del estudiante. |
| **Calidad de los Datos y Análisis** | Usa datasets reales e interesantes. Las conclusiones del README tienen valor analítico real. | Usa datos reales, pero el análisis es superficial o poco detallado. | Usa datos ficticios muy básicos o no redacta conclusiones. | No adjunta los datos ni presenta el análisis solicitado. |
| **Sustentación (Video)** | Explicación clara, fluida. Demuestra dominio total del código escrito sin dudar ante preguntas/conceptos. | Explica bien el funcionamiento, pero titubea al justificar partes específicas del código. | Lee un guion todo el tiempo. La explicación del código es muy superficial. | No entrega video o demuestra no haber escrito el código. |

<aside>
🚫 **¡Nota Importante!** 
Cualquier uso de funciones avanzadas no vistas en clase (`pandas`, `numpy`, etc.) o código generado por Inteligencia Artificial que el estudiante no pueda explicar paso a paso, anulará el criterio de evaluación correspondiente.
</aside>