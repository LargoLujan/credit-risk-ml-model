# Proyecto Final - Modelo de Riesgo Crediticio

## Descripción del Proyecto

Este proyecto se enfoca en desarrollar un modelo de aprendizaje automático para predecir el riesgo crediticio de individuos basado en un conjunto de atributos. El objetivo principal es proporcionar una herramienta que ayude a las instituciones financieras a tomar decisiones más informadas al evaluar la solvencia de los solicitantes de crédito.

## Autor

- **Nombre**: Manuel Luján Vilchez
- **Contacto**: miveritas.vivir@gmail.com

## Dataset

El dataset utilizado en este proyecto se obtuvo de la fuente UCI y fue recopilado por el Dr. Hans Hofmann. Este conjunto de datos contiene información sobre individuos clasificados como riesgos crediticios buenos o malos. La matriz de costos asociada se presenta a continuación:

|              | Good (predicted) | Bad (predicted) |
|--------------|------------------|-----------------|
| **Good (actual)** | 0                | 1               |
| **Bad (actual)**  | 5                | 0               |

La matriz de costos refleja la penalización por clasificar erróneamente a un cliente como bueno cuando es malo (5) en comparación con clasificarlo como malo cuando es bueno (1).

### Descripción de Atributos

El conjunto de datos consta de 21 características que se dividen en características nominales y numéricas. A continuación, se presenta una descripción de algunos de los atributos clave:

- **Clase (Destino)**: Clasificación en dos categorías, bueno o malo.
- **Checking_status**: Estado de la cuenta corriente existente en marcos alemanes.
- **Duración**: Duración en meses del crédito.
- **Credit_history**: Historial crediticio, que incluye créditos tomados, pagados debidamente, retrasos y cuentas críticas.
- **Purpose**: Finalidad del crédito, como coche, televisión, etc.
- **Credit_amount**: Monto del crédito.
- **Savings_status**: Estado de las cuentas de ahorro/bonos en marcos alemanes.
- **Employment**: Empleo actual en número de años.
- **Personal_status_sex**: Situación personal (casado, soltero, etc.) y sexo.
- **Age**: Edad en años.
- **Housing**: Tipo de vivienda (alquiler, propiedad, etc.).

## Requisitos Técnicos

- **Métricas de Evaluación Propuestas**: En este proyecto, utilizaremos métricas como precisión, recall y F1-score para evaluar el rendimiento del modelo.
- **Precisión Final del Modelo Aceptable Mínima**: [Especificar valor].
- **Precisión Final del Modelo Deseable**: [Especificar valor].
- **Recursos de Hardware**: [Especificar recursos de CPU y RAM disponibles].
- **Tiempo Máximo de Entrenamiento**: [Especificar tiempo máximo permitido para el entrenamiento].
- **Dependencias**: Asegúrate de tener instaladas las siguientes bibliotecas de Python:
    - Numpy
    - Pandas
    - Scikit-learn

## Análisis del Dataset

### Origen y Fuente del Dataset

El conjunto de datos se obtuvo de la fuente UCI y fue recopilado por el Dr. Hans Hofmann. La referencia para citar este dataset es la propia UCI.

### Tamaño del Dataset

El dataset contiene un total de 1000 instancias.

### Preprocesamiento de Datos

No se detectaron datos faltantes en el conjunto de datos, y no se realizaron preprocesamientos previos.

### Análisis de Atributos

- **Clase (Destino)**: Dos categorías, bueno o malo.
    - Bueno: [Número de instancias]
    - Malo: [Número de instancias]

- **Checking_status** (Estado de la cuenta corriente):
    - [Descripción detallada de las categorías y distribución de datos]

- **Duración** (Duración en meses del crédito):
    - [Estadísticas descriptivas y visualizaciones]

- **Credit_history** (Historial crediticio):
    - [Descripción detallada de las categorías y distribución de datos]

- **Purpose** (Finalidad del crédito):
    - [Descripción detallada de las categorías y distribución de datos]

- **Credit_amount** (Monto del crédito):
    - [Estadísticas descriptivas y visualizaciones]

- **Savings_status** (Estado de las cuentas de ahorro/bonos):
    - [Descripción detallada de las categorías y distribución de datos]

- [Continúa con el análisis de otros atributos]

## Modelo Base

En esta etapa, se desarrolló un modelo base inicial utilizando un [tipo de modelo] con los siguientes resultados:

- Precisión: [Valor de precisión]
- Recall: [Valor de recall]
- F1-score: [Valor de F1-score]
- Tiempo de entrenamiento: [Tiempo en segundos]
- Desviación o sobreajuste: [Indicar si se observa desviación o sobreajuste]

## Ingeniería de Características

Se realizaron experimentos para mejorar las características utilizadas en el modelo, lo que incluyó:

- Evaluación de la relevancia de las características.
- Planteamiento y prueba de mejoras, como polinomios, logaritmos y cruces entre variables.
- Reducción de dimensionalidad mediante PCA cuando fue necesario.

## Refinado del Modelo

Se probaron varios modelos de aprendizaje automático, incluyendo [lista de modelos] con diferentes hiperparámetros. Cada modelo se evaluó utilizando las siguientes métricas:

- Precisión
- Recall
- F1-score
- Tiempo de entrenamiento
- Desviación o sobreajuste

El modelo final seleccionado fue [nombre del modelo] con los siguientes resultados:

- Precisión final: [Valor de precisión final]
- Recall final: [Valor de recall final]
- F1-score final: [Valor de F1-score final]
- Tiempo de entrenamiento: [Tiempo en segundos]

El modelo final se considera adecuado para el problema de riesgo crediticio.

## Uso del Modelo

Puedes utilizar este modelo para predecir el riesgo crediticio de individuos proporcionando los atributos relevantes. Se proporciona un cuaderno Jupyter (`Bueno.ipyn
