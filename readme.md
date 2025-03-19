MC-8843 Aprendizaje Automático
Prof. MSc. Felipe Meza-Obando
Escuela de Ingeniería en Computación
Tecnológico de Costa Rica

# Tarea 1: Preprocesamiento y Análisis Exploratorio de Datos
*Diego Solis Peñaranda*
*Isaac Arturo Vargas Chacón*

### Objetivos:
- Familiarizarse con las principales librerías de Python para preprocesamiento y análisis de
datos.
- Aplicar técnicas de preprocesamiento para limpiar y preparar conjuntos de datos.
- Realizar análisis exploratorio de datos (EDA) utilizando visualizaciones efectivas.
- Desarrollar habilidades prácticas en la manipulación y visualización de datos en notebooks.
Introducción:
- Debe seleccionar un conjunto de datos que considere interesante y que sea de mediana
dificultad (de acuerdo a los principios expuestos en clase). Este dataset debe cumplir con al
menos tres requisitos: primero, los datos deben requerir tratamiento importante, es decir,
no deben ser datos "limpios" o preprocesados. Segundo, debe tratarse de un dataset que
no haya sido ampliamente utilizado con estos fines en otras fuentes, es decir, que no sea un
conjunto de datos clásico. Tercero, debe contener variables categóricas, outliers y valores
faltantes, si 1 de los 3 requerimientos anteriores no lo posee su dataset, puede incluirlo
sintéticamente (solo 1 de los 3).
- Hay varios lugares donde puede obtener este tipo de datasets, sin embargo, acá se indican
dos recomendaciones para empezar la búsqueda:
- https://datasetsearch.research.google.com/
- https://github.com/awesomedata/awesome-public-datasets
- Al dataset elegido debe llamarlo Original.

### Actividades:
1. Cargar Conjuntos de Datos:
- Objetivo: Aprender a cargar datasets en una notebook en Google Colab desde
diferentes fuentes.
- Instrucciones:
1. Cargar el conjunto de datos a la notebook en Colab desde un archivo CSV (o
el que disponga para su set de datos) en Google Drive.
2. Cargar el conjunto de datos a la notebook en Colab desde su repositorio en
GitHub.
3. Para ambos casos y usando pandas despliegue los 10 primeros ejemplos del
dataset en la notebook como un DataFrame.
- Librerías: pandas
2. Exploración Inicial de Datos:
- Objetivo: Realizar una exploración inicial para comprender la estructura del
dataset.

- Instrucciones:
1. Usar funciones como head(), tail(), info(), y describe() para
explorar las características del dataset.
2. Comente las características más importantes de su dataset, basados en los
resultados del punto anterior.
3. Haga un análisis del problema que pretenden abordar los datos elegidos.
- Librerías: pandas

3. Manejo de Valores Nulos:
- Objetivo: Identificar y manejar valores nulos en el dataset.
- Instrucciones:
1. Identifique la presencia de valores nulos (NaN) en su dataset.
2. Aplicar al menos tres técnicas para rellenar o eliminar valores nulos. Como
producto de este ejercicio, debe tener tres nuevos datasets resultantes cada
uno con la técnica especifica. Coloque a estos dataset nombres significativos,
por ejemplo original_faltantes_mean etc.
3. Medir el tiempo para la creación de los datasets anteriores usando %timeit
- time (o el método que requiera para comparar los tiempos de ejecución).
Almacene los resultados obtenidos.
- Librerías: pandas
  
4. Normalización y Escalado de Datos:
- Objetivo: Aprender a normalizar y escalar datos numéricos.
- Instrucciones:
1. A partir de los 3 datasets anteriores elija 2 de ellos y use MinMaxScaler y
StandardScaler de scikit-learn respectivamente, para escalar las
características numéricas, obtenga dos nuevos dataset, uno normalizado y
otro escalado. Coloque a estos dataset nombres significativos, por ejemplo
original_faltantes_mean_norm etc.
- Librerías: pandas, scikit-learn

5. Codificación de Variables Categóricas:
- Objetivo: Transformar variables categóricas en representaciones numéricas.
- Instrucciones:
1. Implementar OneHotEncoder y/o LabelEncoder para codificar las
variables categóricas de sus 2 dataset anteriores. Coloque a estos dataset
nombres significativos, por ejemplo
original_faltantes_mean_norm_onehot etc.
- Librerías: pandas, scikit-learn

6. Detección de Valores Atípicos (Outliers):
- Objetivo: Identificar y manejar valores atípicos en el dataset.
- Instrucciones:
1. Utilizar gráficos de caja y métodos estadísticos para detectar outliers y
decidir cómo manejarlos, basado en las particularidades de su dataset.
2. Haga una descripción detallada de su procedimiento.
- Librerías: pandas, matplotlib

7. Análisis Exploratorio de Datos (EDA):
- Objetivo: Visualizar la distribución de las variables y detectar patrones.
- Instrucciones:
1. A partir de uno de los dos datasets obtenidos en el punto anterior, hacer un
EDA completo, haciendo uso de por ejemplo histogramas, diagramas de
dispersión y en general, todo tipo de gráfico que haga sentido para entender
mejor los datos.
2. Debe usar las cuatro librerías clásicas: matplotlib, seaborn, bokeh y
ploty resaltando las ventajas de cada una de ellas y para qué son
particularmente mejores.
3. Investigue al menos dos librerías diferentes a las expuestas en este apartado,
indicando
- Librerías: matplotlib, seaborn, bokeh y ploty.

8. Análisis de Correlación:
- Objetivo: Evaluar la relación entre variables numéricas.
- Instrucciones:
1. Calcular y visualizar una matriz de correlación entre variables usando un
heatmap.
2. Hacer un análisis completo con lo que pueda visualizar del punto anterior. El
análisis debe ser de la forma que haga sentido al contexto de los datos de su
dataset.
- Librerías: pandas, seaborn

9. Análisis de polars y pandas:
- Objetivo: Comparar polars con pandas en términos de rendimiento, facilidad
de uso y funcionalidad para la manipulación de datos.
- Instrucciones:
1. Investigar sobre la librería polars destacando sus mayores ventajas en
comparación con pandas.
2. Instalar polars.
3. Realizar una exploración inicial: mostrar las primeras filas, describir
estadísticas, contar nulos.
4. Escoja 4 tareas de las realizadas en los ejercicios anteriores con pandas y
mida el tiempo usando %timeit o time (o el método que requiera para
comparar los tiempos de ejecución).
5. Repita esas 4 tareas pero con polars y mida el tiempo usando %timeit o
time (o el método que requiera para comparar los tiempos de ejecución).
6. Compare los resultados en términos de rendimiento, facilidad de uso y
funcionalidad, use graficas comparativas. Comente las principales
conclusiones.
- Librerías: pandas, polars

10. Creación de un Informe de EDA en Notebook:
- Objetivo: Resumir todos los hallazgos y sobre todo el análisis a partir de los
resultados de todos los puntos anteriores como si fuera un informe haciendo uso
de la notebook.
- Instrucciones:
1. Todos los pasos anteriores debe ejecutarlos en la notebook en formato tipo
informe que incluya visualizaciones clave, imágenes, ecuaciones, análisis
descriptivos, y conclusiones sobre la calidad y características del dataset.
2. Debe asegurarse que la notebook tenga el nombre de los dos integrantes o
integrante al inicio en el encabezado.
3. Debe asegurar que la notebook pueda ser accedida y ejecutada por el
profesor.
- Herramientas: Markdown dentro de la notebook.
11. Investigar un artículo (paper) reciente (publicado en los últimos 3 años) que aborde técnicas
modernas de preprocesamiento de datos en Machine Learning.
- Instrucciones:
1. Encuentre un artículo científico reciente en conferencias o revistas
reconocidas (NeurIPS, ICML, ICLR, IEEE, Nature AI, etc.).
2. El paper debe enfocarse en nuevas estrategias de preprocesamiento como
por ejemplo:
- Métodos avanzados de imputación de valores faltantes.
- Reducción de dimensionalidad moderna (Autoencoders, UMAP).
- Preprocesamiento para datos no estructurados (texto, imágenes, audio).
- Normalización/transformación avanzada de datos.
- Estrategias para mejorar el balanceo de clases en datasets
desbalanceados.
3.Prepare un recumen de no mas de 500 palabras que incluya:
- Título y fuente del artículo.
- Problema que aborda el artículo y su importancia en el preprocesamiento
de datos.
- Principales técnicas propuestas y cómo se comparan con enfoques
tradicionales.
- Resultados y hallazgos más relevantes.
- Conclusión y posibles aplicaciones prácticas.

Tip: Usar Google Scholar, ArXiv, IEEE Xplore u otras bases de datos para encontrar artículos de
calidad.
