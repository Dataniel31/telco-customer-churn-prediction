# Telco Customer Churn Prediction

## Overview

Este proyecto se enfoca en la predicción de la deserción de clientes para una empresa de telecomunicaciones. El objetivo es identificar a los clientes propensos a cancelar sus servicios basándonos en datos históricos. Utilizamos un modelo de regresión logística para hacer estas predicciones.

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

Para manejar los valores nulos en el dataset, utilizamos la mediana o valores predeterminados adecuados.

### 2.2 Detección de Outliers

Visualizamos los outliers en variables clave usando boxplots.

### 2.3 Transformación de Variables Categóricas

Convertimos las variables categóricas en variables numéricas utilizando One-Hot Encoding.

### 2.4 Manejo del Desbalanceo de Clases

Utilizamos SMOTE para manejar el desbalanceo en las clases.

### 2.5 División de Datos y Escalado

Dividimos los datos en conjuntos de entrenamiento y prueba, y escalamos las características.

## 3. Modelado

Entrenamos y evaluamos un modelo de regresión logística para predecir la deserción de clientes.

## 4. Predicción en el Conjunto de Prueba

Realizamos predicciones en el conjunto de prueba y preparamos el archivo para la presentación.

## 5. Conclusiones

Este proyecto ha cubierto el proceso de predicción de la deserción de clientes utilizando un modelo de regresión logística. Hemos abordado la imputación de valores nulos, el manejo del desbalanceo de clases, la transformación de variables categóricas, y la evaluación del modelo. Finalmente, hemos preparado un archivo de predicciones para su envío.
