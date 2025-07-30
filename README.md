# TelecomX-parte2
Challenge 3 TelecomX parte2

## 🎯 Objetivo

- Preparar los datos para el modelado (tratamiento, codificación, normalización).
- Realizar análisis de correlación y selección de variables.
- Entrenar dos o más modelos de clasificación.
- Evaluar el rendimiento de los modelos con métricas.
- Interpretar los resultados, incluyendo la importancia de las variables.
- Crear una conclusión estratégica señalando los principales factores que influyen en la cancelación.

---

## 🛠️ Preparación de los Datos

### Carga de Datos
Carga el archivo CSV que contiene los datos tratados anteriormente.  
📂 **Atención**: Utiliza el mismo archivo que limpiaste y organizaste en la Parte 1 del desafío Telecom X. Debe contener solo las columnas relevantes, ya con los datos corregidos y estandarizados.

### Eliminación de Columnas Irrelevantes
Elimina columnas que no aportan valor al análisis o a los modelos predictivos, como identificadores únicos (por ejemplo, el ID del cliente).

### Encoding
Transforma las variables categóricas a formato numérico para hacerlas compatibles con los algoritmos de machine learning (e.g., one-hot encoding).

### Verificación de la Proporción de Cancelación (Churn)
Calcula la proporción de clientes que cancelaron en relación con los que permanecieron activos.  
🔎 Sugerencia:  
[value_counts de pandas](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.value_counts.html)

### Balanceo de Clases (opcional)
Aplica técnicas de balanceo como SMOTE si existe desbalance en las clases.  
🔎 Recurso:  
https://www.alura.com.br/artigos/lidando-com-desbalanceamento-dados

### Normalización o Estandarización (si es necesario)
Requerido para modelos basados en distancia como KNN, SVM, Regresión Logística y Redes Neuronales.  
Modelos de árboles como Decision Tree, Random Forest y XGBoost no requieren esta etapa.

---

## 📊 Correlación y Selección de Variables

### Análisis de Correlación
Visualiza la matriz de correlación para identificar relaciones entre las variables numéricas y la cancelación.

### Análisis Dirigido
Investiga relaciones específicas con gráficos como boxplot y scatter plot:
- Tiempo de contrato × Cancelación
- Gasto total × Cancelación

---

## 🤖 Modelado Predictivo

### Separación de Datos
División del conjunto en entrenamiento y prueba (70/30 o 80/20).

### Creación de Modelos
Entrena al menos dos modelos diferentes:
- Modelos con normalización: Regresión Logística, KNN
- Modelos sin necesidad de normalización: Árbol de Decisión, Random Forest

### Evaluación de los Modelos
Evalúa cada modelo usando:
- Exactitud (Acurácia)
- Precisión
- Recall
- F1-score
- Matriz de confusión

### Comparación Crítica
- ¿Cuál modelo tuvo mejor desempeño?
- ¿Se detectó overfitting o underfitting?
  - Overfitting: ajustar modelo, limitar complejidad.
  - Underfitting: aumentar complejidad o ajustar parámetros.

---

## 📋 Interpretación y Conclusiones

### Análisis de Importancia de Variables
- **Regresión Logística**: coeficientes indican contribución.
- **KNN**: analiza variables que más contribuyen a la distancia.
- **Random Forest**: importancia calculada por reducción de impureza.
- **SVM**: coeficientes de vectores de soporte.
- **Otros modelos**: usar coeficientes, pesos o importancia relativa según el tipo.

### Conclusión
Informe detallado destacando los factores que más influyen en la cancelación.  
Identificación de variables clave y estrategias de retención sugeridas con base en los hallazgos.
