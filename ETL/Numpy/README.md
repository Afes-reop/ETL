# Numpy: 

## Introducción
En aplicaciones científicas, de ingeniería y principalmente de ciencia de datos, existe la necesidad de realizar cálculos numéricos especializados.

Cuando haces la suma de todos los valores de una columna en un software de hojas de cálculo o incluso operaciones matemáticas entre diferentes columnas, hay un código implementado para hacer estas operaciones posibles. De la misma manera, si has utilizado una función de una biblioteca de Python que realiza regresión lineal o un algoritmo de machine learning cualquiera, debes saber que este código es la traducción de un conjunto de ecuaciones matemáticas a código. Esta implementación necesita ser eficiente y fácil de comprender. Cuanto más cercano esté el código escrito a la escritura matemática, mejor.

En este contexto, en Python, surge NumPy. Esta es una poderosa biblioteca ampliamente utilizada que ha revolucionado el segmento de computación científica, principalmente debido al carácter abierto del lenguaje Python. Con NumPy, es posible realizar operaciones matemáticas complejas con matrices de forma eficiente y optimizada. ¿Pero qué es exactamente y cómo funciona NumPy?

## ¿Qué es NumPy?
NumPy, una abreviatura de Numerical Python, es una biblioteca de código abierto de Python para computación científica, un campo de estudio que utiliza recursos computacionales para comprender y resolver problemas. Esta biblioteca permite trabajar con la manipulación de objetos array multidimensionales, así como con sus derivados, como matrices, secuencias y otros. Además de eso, también posee una amplia variedad de operaciones rápidas con los arrays, incluyendo operaciones matemáticas y lógicas, manipulación de formato, ordenación y selección, herramientas de estadística y cálculo, y mucho más.

La biblioteca NumPy fue lanzada en 2005 por el científico de datos Travis Oliphant, con la propuesta de ser una herramienta rápida, eficiente y fácil de usar, permitiendo así la realización de cálculos numéricos y matemáticos a gran escala, a través de la funcionalidad llamada vectorización. Por eso, se ha convertido en una de las bases fundamentales para el análisis de datos, el aprendizaje automático (machine learning) y la computación científica en general, estando presente también en la construcción de varias bibliotecas de ciencia de datos, incluyendo: Pandas, Matplotlib, Scikit-learn, SciPy, y mucho más.

Una curiosidad sobre esta biblioteca es que también ha estado presente en trabajos de descubrimientos científicos importantes, como la detección de la primera imagen de un agujero negro y la detección de ondas gravitacionales.

¿Pero cómo funciona exactamente NumPy?

## Estructuras básicas de NumPy
NumPy funciona a través de estructuras llamadas arrays, que son estructuras de datos homogéneas, es decir, donde los elementos poseen el mismo tipo. Estas estructuras pueden tener varios formatos y dimensiones, que varían según las necesidades de cada tipo de proyecto. De manera general, para varios tipos de aplicación, trabajamos hasta la tercera dimensión, pero existen casos donde podemos necesitar más.

El concepto de dimensiones puede aplicarse en Python a partir del concepto de listas anidadas (nested lists). Para eso, utilizaremos las siguientes estructuras:

Escalar: Un elemento único, sin dimensiones. Puede ser un entero, flotante, hexadecimal, caracter y varios otros tipos de datos.

En Python, después de importar la biblioteca, definimos un escalar como:

import numpy as np
np.array(42)

Array unidimensional: una lista de escalares donde podemos identificar cada uno de ellos por su posición, o índice, en la lista. Es necesario destacar que todos los elementos escalares aquí poseen el mismo tipo, y aunque no se especifique durante la definición del array, NumPy trabajará en una rutina para determinar el tipo que garantice la homogeneidad.

np.array([4,5,22,20])

Array bidimensional: una lista de arrays unidimensionales, con el formato de una matriz (tabla), donde necesitamos especificar una posición de fila y una posición de columna para localizar un elemento escalar.

np.array([3,2,7],

		 [4,9,1],
		 
		 [5,6,8])

Array tridimensional: una lista de arrays bidimensionales. Un ejemplo de aplicación de un array tridimensional es la matriz de imágenes RGB, como se puede observar en el funcionamiento de un televisor. En este caso, tenemos una estructura bidimensional (el formato de pantalla), donde podemos localizar un píxel con una referencia vertical y otra horizontal. Para cada píxel, también tenemos una representación de un array de 3 elementos, que es la unión de tres LEDs de colores rojo, verde y azul. 

Array multidimensional (n-dimensional): las operaciones de creación de arrays en NumPy no están limitadas solo a las dimensiones anteriores: es posible construir estructuras de cantidades mayores, tanto como sea necesario, siempre que los objetivos del mismo nivel tengan el mismo formato. 

En este esquema, cuando llegamos a la cuarta dimensión y más allá, es más difícil visualizar la matriz como un objeto geométrico. En su lugar, podemos interpretar una matriz de orden superior como un objeto matemático que contiene información sobre otros objetos matemáticos.

Por ejemplo, una matriz de cuarto orden puede ser vista como una matriz de matrices de matrices, es decir, cada elemento de la matriz es una matriz de matrices. Podemos interpretar esta matriz como un objeto matemático que contiene información sobre varios objetos matemáticos más simples.

## Broadcasting
El broadcasting es una funcionalidad de NumPy que permite trabajar con operaciones en arrays de formas y tamaños diferentes, sin necesidad de crear copias de los datos. Por este motivo, es una técnica que ahorra tiempo y memoria. En muchos casos, el broadcasting puede reducir el número de líneas de código necesarias para realizar una determinada operación.

Por ejemplo, en la operación a continuación:

import numpy as np
a = np.array([1,2],[3,4])

b = np.array([10,20])

a + b

En el ejemplo anterior, estamos trabajando con la suma de dos arrays con dimensiones diferentes, en este caso, un array bidimensional y un array unidimensional. Sin embargo, NumPy puede analizar las dimensiones a través de reglas preestablecidas y ejecutar la operación, retornando:

array([[11,24],

	   [13,24]])

## NumPy en la computación científica
Siendo una biblioteca de Python, una gran ventaja de trabajar con NumPy es la posibilidad de integración con otras bibliotecas del gran ecosistema de Python. Esto abre espacio para trabajar con soluciones end-to-end, que van desde la recolección de datos, procesamiento, hasta la entrega del producto final, como por ejemplo un panel de control o un sistema con un análisis detallado de modelos de aprendizaje automático.

Esta característica, sumada al hecho de que la biblioteca es de código abierto y libre, convierte a NumPy en un gran competidor de otras soluciones presentes en el mercado y en la academia, como MATLAB, Octave, Scilab, entre otros.

## Instalación de NumPy

La forma más sencilla de instalar NumPy en Python es usando pip, el gestor de paquetes de Python. Abre la terminal o símbolo del sistema y ejecuta el comando pip install numpy.

### Instalación con pip:

1. Asegúrate de tener Python y pip instalados: Si no tienes Python, descárgalo e instálalo desde la página oficial de Python. Pip generalmente se instala con Python, pero puedes verificarlo con pip --version.
2. Abre la terminal o símbolo del sistema: En Windows, puedes buscar "Símbolo del sistema" o "cmd". En macOS y Linux, abre la aplicación de Terminal.
3. Ejecuta el comando: Escribe pip install numpy y presiona Enter.
4. Espera a que termine la instalación: Pip descargará e instalará NumPy y sus dependencias.
5. Verifica la instalación: Abre un intérprete de Python y ejecuta import numpy. Si no hay errores, la instalación fue exitosa. 

### Instalación en entornos de desarrollo:
Si usas entornos de desarrollo como Visual Studio Code o Jupyter Notebook, puedes instalar NumPy dentro de ese entorno usando el gestor de paquetes correspondiente (pip).


Esta formación forma parte del Programa ONE, una alianza entre Alura Latam y Oracle.
