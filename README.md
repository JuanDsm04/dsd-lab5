# Laboratorio 5 — Clasificación de tweets con minería de texto

Clasificación de tweets para determinar si se refieren a un desastre real o no, usando el dataset [NLP with Disaster Tweets](https://www.kaggle.com/c/nlp-getting-started) de Kaggle.

El dataset contiene ~7,600 tweets etiquetados con `target = 1` (desastre real) o `target = 0` (no desastre).

## Estructura de notebooks

| # | Archivo | Puntos del lab |
|---|---------|----------------|
| 01 | `01_carga_y_preprocesamiento.ipynb` | Carga del dataset, limpieza y pipeline de preprocesamiento de texto |
| 02 | `02_frecuencias_y_ngramas.ipynb` | Frecuencia de palabras por clase, bigramas y trigramas |
| 03 | `03_analisis_exploratorio.ipynb` | EDA: distribución de clases, keywords, longitud de tweets, nubes de palabras, histogramas y palabras compartidas entre categorías |
| 04 | `04_modelos_clasificacion.ipynb` | Entrenamiento y comparación de modelos (Naive Bayes, Regresión Logística, SVM, Random Forest), ajuste de hiperparámetros y selección del mejor modelo |
| 05 | `05_funcion_clasificacion.ipynb` | Función que recibe un tweet sin preprocesar y devuelve si es desastre o no |
| 06 | `06_analisis_sentimientos.ipynb` | Clasificación positivo/negativo/neutro, variable de negatividad, y reentrenamiento del modelo con esa variable |

## Cómo ejecutar

1. Descargar `train.csv` desde Kaggle y colocarlo en `./data/`.
2. Ejecutar los notebooks **en orden**, ya que cada uno depende del output del anterior.
3. El notebook 04 guarda el modelo entrenado en `./models/`, que es requerido por los notebooks 05 y 06.

## Dependencias principales

```
pandas, numpy, matplotlib, seaborn
scikit-learn
nltk
wordcloud
textblob
joblib
```