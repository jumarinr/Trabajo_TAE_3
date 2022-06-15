# Trabajo 3 Técnicas de Aprendizaje Estadístico

## Integrantes 
- Camilo Loaiza Fonnegra
- Juan Diego Marin Rodriguez
- Juan Pablo Rivera Sierra
- Eduardo Santos Ruiz
- Ivan Andrés Velasco Arias

## Planteamiento del Problema

### Objetivo:

* Caracterizar, comprender y desarrollar un modelo de clustering que permita reunir en grupos instituciones de educación superior.

### Tipo de Problema:

* Problema de predicción de mejor decisión en la elección de instituciones de educación superior a partir de los datos y recursos.

### Información Disponible:

* El insumo principal de este trabajo son datos de estudiantes de diferentes universidades provenientes del departamento de eduación de Estados Unidos https://data.world/exercises/cluster-analysis-exercise-2 (7.804 registros)


### Reducción de la dimensionalidad mediante ACP:

* Análisis de componentes principales, Técnica lineal que se utiliza para la eliminación de la redundancia de los datos, utilizada para describir un conjunto de datos en términos de nuevos componentes no correlacionados. Para su implementación se realizó el siguiente proceso: 

  1. Se realiza un preprocesamiento de los datos.
  2. Se realiza la reducción de la dimensionalidad.
  3. Se encuentra el número óptimo de componentes principales.
  4. Se crea la matriz de componentes principales a usar en el agrupamiento.

### Método de Clustering:

* K Means: Algoritmo de agrupamiento no supervisado que reúne objetos en “k” basándose en sus características. Este agrupamiento se realiza minimizando la suma de distancias entre cada objeto y el centroide de su grupo o cluster. Para su implementación de este se realizaron los siguientes procedimientos: 

  1. Utilizando los componentes principales escogidos, se realiza un análisis mediante una gráfica que permite encontrar el número óptimo de clusters. 
  2. Con el número óptimo de clusters, se realiza el entrenamiento del modelo.


## Definiciones

* **Instituto de educación superior:** para este trabajo se define como institutos que se encuentran en el proyecto college scorecard ya que estos datos salen de informes federales.

## Fuentes de Datos y Preprocesamiento

### Poblaciones:

* Instituto de educación superior.
* Centro educativo.


### Registro de Muestra y Características de Medición:

* Datos obtenidos de los estudiantes por el departamento de educación  estadounidense [CollegeScorecard.csv](https://data.world/exercises/cluster-analysis-exercise-2/workspace/file?filename=CollegeScorecard.csv) (7.804 registros). 

### Recopilación de Datos:

* Registros de solicitudes seleccionados de la base de datos a partir de las definiciones presentadas en este trabajo.

### Estructuras de Datos y Tipos:

* Variables continuas y discretas seleccionadas de la base de datos.

### Preprocesamiento de Datos:

* Se realizó el siguiente preprocesamiento para los datos:

  * Reemplazo de los valores “PrivacySuppressed” por valores nulos.
  * Eliminación de todas las columnas que sobrepasan el 20% de valores nulos.
  * Eliminación de columnas que solo contienen dos y tres valores ya que se consideran categóricas.
  * Eliminación de columnas a partir de análisis exploratorio de los datos.
  * Reemplazo de los valores nulos restantes con la media de la columna en la que aparecen.

### Link a la Información:

* [CollegeScorecard.csv](https://data.world/exercises/cluster-analysis-exercise-2/workspace/file?filename=CollegeScorecard.csv).

## Desarrollo del Modelo

### Software Utilizado:

* Modelo realizado en [Google Collaboratory](https://www.google.com/url?q=https://colab.research.google.com/notebooks/welcome.ipynb?hl%3Des&sa=D&source=editors&ust=1651468799400076&usg=AOvVaw3BsmzIFA0LLERerLBE2zcG) con el lenguaje de programación Python utilizando la librerías [Sklearn](https://scikit-learn.org/stable/).

### Reproducibilidad y Reutilización del Código:

* Modelo para el agrupamiento de universidades:
  * [Código fuente en Google Colab](https://colab.research.google.com/drive/1kW8cXqE39fJZ7ep0Wu0mjwCtVxmfP-CW?usp=sharing)
  * [Código fuente en Github](https://github.com/jumarinr/Trabajo_TAE_3)

## Propuesta de implementación en Colombia

Como trabajos previos se encuentra unas encuestas realizadas por la universidad nacional de Colombia durante el periodo de 2008-1 hasta el 2022-1 en donde se obtiene las siguientes características de la población admitida y egresada: 

  * Modalidad de la formación
  * Nivel de la formación
  * Nacionalidad
  * Lugar de nacimiento
  * Lugar de procedencia
  * Sexo
  * Estrato
  * Discapacidad

La encuesta para la recolección de datos puede estar basada en la encuesta mencionada anteriormente.

La propuesta consistiría en recolectar datos respecto al ingreso de estudiantes y la salida de estudiantes graduados de las carreras más comunes en las universidades; además de generar una división de estudiantes por estratos, realizar un análisis de gastos de las universidades y el valor de la matrícula para observar qué universidades podrían ser buenas opciones para los jóvenes en general. Los datos se recolectarían de todas las universidades del país y se solicitaría crear un estándar para las preguntas que adopte las variables recolectadas por el trabajo previo encontrado.

## Conclusiones

* Se puede concluir que sin importar a qué grupo pertenece la universidad dado el agrupamiento realizado, se presenta una gran cantidad de estudiantes de raza blanca en todas.

## Referencias

A. (2020, 23 septiembre). US College Scorecard Clustering. Kaggle. https://www.kaggle.com/code/amritasengupta/us-college-scorecard-clustering/notebook

PCA con Python. (s. f.). Joaquín Amat Rodrigo. https://www.cienciadedatos.net/documentos/py19-pca-python.html

US Dept of Education: College Scorecard. (2017, 9 noviembre). Kaggle. https://www.kaggle.com/datasets/kaggle/college-scorecard/code?select=Scorecard.csv

UNAL en un vistazo  (2022, Enero) Universidad Nacional de Colombia http://estadisticas.unal.edu.co/home/
