# Telco Customer Churn Prediction

## Overview

Este proyecto se enfoca en la predicción de la deserción de clientes para una empresa de telecomunicaciones. El objetivo es identificar a los clientes propensos a cancelar sus servicios basándonos en datos históricos. Utilizamos un modelo de regresión logística y técnicas avanzadas para hacer estas predicciones.

## Dataset

El proyecto utiliza dos conjuntos de datos:

- **Train Dataset:** `train.csv` que contiene datos sobre clientes y su historial de cancelación.
- **Test Dataset:** `test.csv` para realizar predicciones y evaluar el modelo.

## 1. Introducción

### 1.1 Descripción del Proyecto

El objetivo es predecir la cancelación de clientes (churn) en una empresa de telecomunicaciones. Esto permite a la empresa implementar estrategias de retención proactivas para mantener a los clientes existentes.

### 1.2 Dataset

El dataset incluye:
- **Churn:** Indica si un cliente ha abandonado el servicio en el último mes.
- **Servicios Contratados:** Información sobre los servicios que cada cliente ha contratado.
- **Información de la Cuenta:** Detalles sobre la duración de la relación, tipo de contrato, método de pago, etc.
- **Datos Demográficos:** Incluye género, si son ciudadanos mayores, si tienen pareja y dependientes.

## 2. Procesamiento de Datos

### 2.1 Imputación de Valores Nulos

Se manejaron los valores nulos en el dataset utilizando la mediana para variables numéricas y valores predeterminados para variables categóricas. Esto asegura que el modelo pueda entrenarse con un conjunto de datos completo y consistente.

### 2.2 Detección de Outliers

Se identificaron outliers en variables clave (tenure, MonthlyCharges, TotalCharges) utilizando boxplots. Los outliers pueden afectar negativamente el rendimiento del modelo, por lo que se revisaron y gestionaron adecuadamente.

### 2.3 Transformación de Variables Categóricas

Se aplicó One-Hot Encoding para convertir variables categóricas en variables numéricas. Esto permite que el modelo de regresión logística pueda utilizar estas características en el proceso de entrenamiento.

### 2.4 Manejo del Desbalanceo de Clases

Para abordar el desbalanceo en las clases (más clientes que no abandonan el servicio), se utilizó SMOTE (Synthetic Minority Over-sampling Technique). Esta técnica genera ejemplos sintéticos para la clase minoritaria, equilibrando así la distribución de las clases y mejorando la capacidad del modelo para identificar clientes que podrían abandonar el servicio.

### 2.5 División de Datos y Escalado

Se dividió el conjunto de datos en conjuntos de entrenamiento y prueba. Además, se escaló las características para que todas las variables tuvieran una escala similar, lo cual es importante para el rendimiento de los modelos de clasificación.

## 3. Modelado

Se entrenó un modelo de regresión logística utilizando el conjunto de datos balanceado y escalado. Este modelo fue seleccionado por su capacidad para manejar datos binarios y proporcionar probabilidades de predicción claras.

### 3.1 Librerías Utilizadas

- **Pandas:** Para la manipulación y análisis de datos.
- **NumPy:** Para operaciones matemáticas y manejo de arrays.
- **Matplotlib y Seaborn:** Para la visualización de datos, incluyendo la detección de outliers mediante boxplots.
- **Scikit-learn:** Para el modelado y evaluación del modelo, incluyendo la regresión logística, división de datos, escalado y métricas de evaluación.
- **Imbalanced-learn (imblearn):** Para la implementación de SMOTE, que ayuda a manejar el desbalanceo de clases.

## 4. Predicción en el Conjunto de Prueba

Se realizaron predicciones en el conjunto de prueba y se preparó el archivo de resultados en el formato requerido. Estas predicciones serán utilizadas para evaluar el desempeño del modelo en datos no vistos.

## 5. Conclusiones

El modelo de predicción de churn ha logrado un F1-score de **0.56093** en el conjunto de prueba. Este puntaje indica que el modelo tiene una capacidad moderada para identificar a los clientes propensos a abandonar el servicio, equilibrando adecuadamente la precisión y el recall.

