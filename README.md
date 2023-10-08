# Proyecto Final - Modelo de Riesgo Crediticio

## Descripción del Proyecto

Este proyecto se enfoca en desarrollar un modelo de aprendizaje automático para predecir el riesgo crediticio de individuos basado en un conjunto de atributos. El objetivo principal es proporcionar una herramienta que ayude a las instituciones financieras a tomar decisiones más informadas al evaluar la solvencia de los solicitantes de crédito.

## Autor

- **Nombre**: Manuel Luján Vilchez
- **Contacto**: miveritas.vivir@gmail.com

## Dataset

El dataset utilizado en este proyecto se obtuvo de la fuente UCI y fue recopilado por el Dr. Hans Hofmann en 1994. Este conjunto de datos contiene información sobre individuos clasificados como riesgos crediticios buenos o malos. La matriz de costos asociada se presenta a continuación:

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
- **Precisión Final del Modelo Aceptable Mínima**: 0.60.
- **Precisión Final del Modelo Deseable**: 0.75.
- **Recursos de Hardware**:
- - Procesador	Intel(R) Core(TM) i7-9700K CPU @ 3.60GHz   3.60 GHz
- - RAM instalada	32,0 GB
- - Tipo de sistema	Sistema operativo de 64 bits, procesador basado en x64.
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
    - Bueno: 700 instancias
    - Malo: 300 instancias
- **Checking_status** (Estado de la cuenta corriente):
    - Categorías:
      - "<0"
      - "0<=X<200"
      - "no checking"

- **Duración** (Duración en meses del crédito):
    - Valor mínimo: 6
    - Valor máximo: 48
    - Media: 20.903 meses.
    - Desviación estándar: 12.058 meses.

- **Credit_history** (Historial crediticio):
    - "critical/other existing credit"
    - "existing paid"

- **Purpose** (Finalidad del crédito):
    - "radio/tv"
    - "education"
    - "furniture/equipment"
    - "new car"

- **Credit_amount** (Monto del crédito):
    - Estadísticas descriptivas:
        - Valor mínimo: 250.0
        - Valor máximo: 18424.0
        - Media: 3271.248
        - Desviación estándar: 2822.751
- **Savings_status** (Estado de las cuentas de ahorro/bonos):
    - Categorías:
        - "no known savings"
        - "<100"

      
## Modelo Base

En esta etapa, se desarrolló un modelo base inicial utilizando un Random Forest Classifier con los siguientes resultados:

- Precisión: 0.70 (conjunto de validación) y 0.74 (conjunto de prueba)
- Recall: 0.83 (conjunto de validación) y 0.84 (conjunto de prueba)
- F1-score: 0.75 (conjunto de validación) y 0.79 (conjunto de prueba)
- Tiempo de entrenamiento: 900 segundos.
- Desviación o sobreajuste:
- - La curva de aprendizaje mostró cierta desviación ya que la precisión en el conjunto de entrenamiento es más alta que en el conjunto de prueba, lo que - - sugiere un ligero sobreajuste. Sin embargo, este sobreajuste es relativamente bajo, ya que las puntuaciones en ambos conjuntos son cercanas y no hay - - - una brecha significativa.

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

El modelo final seleccionado fue Regresión lógistica con los siguientes resultados:

- Precisión final: 0.6667
- Recall final: 0.8
- F1-score final: 0.7273
- Tiempo de entrenamiento: 900 segundos.

El modelo final se considera adecuado para el problema de riesgo crediticio.

## Uso del Modelo

Puedes utilizar este modelo para predecir el riesgo crediticio de individuos proporcionando los atributos relevantes. Se proporciona un cuaderno Jupyter. 
