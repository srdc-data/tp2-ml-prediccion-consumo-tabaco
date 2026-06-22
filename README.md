# TP2 - Machine Learning - Predicción de Consumo de Tabaco

## Predicción de hábito de fumador

** Universidad de Palermo **

** Programa Intensivo:** Diplomatura en Inteligencia Artificial

**Alumno:** Silvio De Cicco

**Profesor:** Martin Jaureguy

**Fecha de entrega:** 23/06/2026 18:59.59 hs.



## Descripción

Este proyecto corresponde al Trabajo Práctico 2 del Módulo II, Machine Learning.

El objetivo consiste en construir un modelo de clasificación capaz de predecir si una persona es fumadora o no fumadora a partir de información clínica y hábitos de salud.

---

## Estructura del Proyecto

```TP2
data/
├── raw/
└── processed/
└── external/

notebooks/
├── 01_discovery.ipynb
├── 02_eda.ipynb
├── 03_preprocesamiento.ipynb
├── 04_entrenamiento_optimizacion.ipynb
├── 05_validacion.ipynb
└── 06_predicciones.ipynb

models/

predictions/

README.md

requirements.txt

```

## Diccionario de Datos: DataSet de TRAIN smoking_prediction.xlsx - smoking_prediction.csv

 #   Column                 Dtype  
---  ------                 -----  
 0   ID                     int64  
 1   gender                 object 
 2   age                    int64  
 3   height(cm)             int64  
 4   weight(kg)             int64  
 5   waist(cm)              float64
 6   eyesight(left)         float64
 7   eyesight(right)        float64
 8   hearing(left)          float64
 9   hearing(right)         float64
 10  systolic               float64
 11  relaxation             float64
 12  fasting blood sugar    float64
 13  Cholesterol            float64
 14  triglyceride           float64
 15  HDL                    float64
 16  LDL                    float64
 17  hemoglobin             float64
 18  Urine protein          float64
 19  serum creatinine       float64
 20  AST                    float64
 21  ALT                    float64
 22  Gtp                    float64
 23  oral                   object 
 24  dental caries          int64  
 25  tartar                 object 
 26  smoking                int64

## Diccionario de Datos: DataSet de TEST smoking_prediction_entrega.xlsx - smoking_prediction.csv

 #   Column                 Dtype  
---  ------                 -----  
 0   ID                      int64  
 1   gender                  object 
 2   age                     int64  
 3   height(cm)              int64  
 4   weight(kg)              int64  
 5   waist(cm)               float64
 6   eyesight(left)          float64
 7   eyesight(right)         float64
 8   hearing(left)           float64
 9   hearing(right)          float64
 10  systolic                float64
 11  relaxation              float64
 12  fasting blood sugar     float64
 13  Cholesterol             float64
 14  triglyceride            float64
 15  HDL                     float64
 16  LDL                     float64
 17  hemoglobin              float64
 18  Urine protein           float64
 19  serum creatinine        float64
 20  AST                     float64
 21  ALT                     float64
 22  Gtp                     float64
 23  oral                    object 
 24  dental caries           int64  
 25  tartar                  object 

---

## Metodología

El trabajo se desarrolló siguiendo las siguientes etapas:

1. Discovery del conjunto de datos.
2. Análisis exploratorio (EDA).
3. Limpieza y preprocesamiento.
4. Entrenamiento y comparación de modelos.
5. Validación del modelo seleccionado.
6. Generación de predicciones finales.

---


## Variables Relevantes

Durante el análisis exploratorio se observó una asociación significativa entre la variable objetivo y atributos como:

* gender
* hemoglobin
* dental caries
* tartar

Estas variables fueron consideradas especialmente relevantes durante el modelado.

---

## Modelos Evaluados

Se evaluaron los siguientes algoritmos:

* Logistic Regression
* Random Forest
* XGBoost

La métrica principal utilizada para la comparación fue:

**F1 Score**

---

## Modelo Seleccionado

El modelo seleccionado para generar las predicciones finales fue:

**Random Forest**

Motivos:

* Si bien presentó cierto grado de sobreajuste (Overfitting), tuvo mayor valor de F1 Score sobre la clase objetivo.

---

## Resultados

| Modelo              | F1 Score Test |
| ------------------- | ------------- |
| Random Forest       | 0.73          |
| XGBoost             | 0.69          |
| Logistic Regression | 0.67          |

---

## Archivo de Predicciones

El archivo final generado contiene:

* ID
* smoking_prediction

y se encuentra dentro de la carpeta:

```TP2
predictions/
```

---

## Librerías Utilizadas

Las dependencias necesarias se encuentran en:

```
requirements.txt
```
