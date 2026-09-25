# EP1 Deep Learning - Sign Language MNIST con MLP

Proyecto desarrollado para la Evaluación Parcial 1 de la asignatura Deep Learning.

El objetivo es implementar y evaluar una red neuronal artificial tipo **MLP (Multilayer Perceptron)** para clasificar imágenes correspondientes a letras de lengua de señas utilizando el dataset **Sign Language MNIST**.

## Dataset

Se utiliza el dataset **Sign Language MNIST**, compuesto por imágenes de 28x28 píxeles en escala de grises.

El problema contiene 24 clases correspondientes a letras del alfabeto, excluyendo J y Z.

El dataset es obtenido automáticamente desde Kaggle mediante `kagglehub`, por lo que no es necesario almacenar los archivos CSV dentro del repositorio.

## Modelo final

La configuración seleccionada fue:

- Arquitectura: 784 → 256 → 128 → 24
- Capas ocultas: Tanh
- Capa de salida: Softmax
- Función de pérdida: Sparse Categorical Crossentropy
- Optimizador: Adam
- Learning rate: 0.001
- Batch size: 32
- Épocas: 5
- Dropout: no utilizado

## Experimentos realizados

Durante el desarrollo se compararon distintas configuraciones de:

- Funciones de activación: ReLU, Tanh y Sigmoid
- Funciones de pérdida
- Learning rate
- Batch size
- Dropout
- Optimizadores
- Número de capas y neuronas de la MLP

Los experimentos fueron realizados modificando un parámetro a la vez y utilizando el conjunto de validación para seleccionar la configuración final.

## Resultados

La configuración final obtuvo aproximadamente:

- Validation Accuracy: 97.69%
- Test Accuracy: 77.89%
- Precision Macro: 77.55%
- Recall Macro: 76.50%
- F1-score Macro: 76.06%

También se analizaron los resultados mediante:

- Matriz de confusión
- Precision y Recall por clase
- Ejemplos de predicciones correctas e incorrectas
- Análisis de TP, FP, FN y TN
- Curvas de entrenamiento y validación

## Ejecución

La forma recomendada de ejecutar el proyecto es mediante **Google Colab**.

1. Descargar o clonar este repositorio.
2. Abrir el archivo:

   `EP1_DeepLearning_SignLanguage_MLP.ipynb`

   en Google Colab.
3. Seleccionar:

   `Entorno de ejecución → Ejecutar todas`

4. El notebook descargará automáticamente el dataset mediante `kagglehub`.
5. Esperar a que finalicen los entrenamientos y experimentos.

Se requiere conexión a Internet para descargar el dataset.

## Tecnologías utilizadas

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- KaggleHub
- Google Colab

## Archivo principal

`EP1_DeepLearning_SignLanguage_MLP.ipynb`

El notebook contiene el proceso completo de:

- carga y exploración de datos,
- preprocesamiento,
- construcción de la MLP,
- experimentación,
- selección de hiperparámetros,
- evaluación final,
- análisis de métricas,
- visualización de resultados,
- y persistencia del modelo.
