# Análisis y Predicción de Deserción Estudiantil

---

## Resumen del Proyecto

Este proyecto tiene como objetivo analizar y predecir la **deserción estudiantil** utilizando un modelo de **Red Neuronal**. Se enfoca en el **preprocesamiento de datos** de estudiantes y la creación, entrenamiento y evaluación de un modelo de regresión con **Keras (TensorFlow)** para entender mejor los factores que influyen en la deserción.

---

## Contenido del Repositorio

Los archivos clave en este repositorio son:

* **`df_completado.csv`**: Archivo CSV resultante de la fusión de datos.
* **`df_codificado_final.csv`**: Dataset preprocesado con variables categóricas codificadas (One-Hot Encoding).
* **`df_salida_final.csv`**: Archivo con la variable objetivo (`y`) para la predicción.
* **`X_train.csv`, `X_test.csv`, `y_train.csv`, `y_test.csv`**: Conjuntos de datos divididos para entrenamiento y prueba.

---

## Preparación de los Datos

El proceso de preparación de datos incluye:

1.  **Unificación de Códigos**: Asegurar la consistencia del `CODIGO` de los estudiantes.
2.  **Consolidación de Información**: Fusionar diferentes fuentes de datos para enriquecer la información de los estudiantes.
3.  **Codificación de Variables Categóricas**: Transformar variables como `GENERO`, `ESTUDIANTE`, `FACULTAD`, `PROGRAMA`, `SEDE` y `JORNADA` utilizando **One-Hot Encoding**.
4.  **División del Dataset**: Separar los datos en un 70% para **entrenamiento** y un 30% para **prueba**.

---

## Modelo de Red Neuronal

Se emplea una **Red Neuronal Secuencial** de **Keras** para la tarea de regresión, estructurada de la siguiente manera:

* **Capa de Normalización**: `Normalization(axis=-1)` para escalar los datos de entrada.
* **Capas Ocultas (Dense Layers)**: Tres capas densas con activación `relu` (32, 64, 32 neuronas respectivamente) para aprender patrones complejos.
* **Capa de Salida**: Una capa densa con una sola neurona para la predicción de valores continuos.
* **Compilación**: El modelo se compila con `loss='mean_absolute_error'` (Error Absoluto Medio) y el optimizador `Adam(0.001)`.

---

## Evaluación del Rendimiento

El modelo se entrena durante **100 épocas**. La métrica principal de evaluación es el **Error Absoluto Medio (MAE)**. Se incluye un gráfico de dispersión "Predicción vs Real" para visualizar la precisión de las predicciones del modelo.

---

## Cómo Ejecutar el Proyecto

1.  **Clona el Repositorio**:
    ```bash
    git clone [https://github.com/Eigna-atonim1030/IA_Final.git](https://github.com/Eigna-atonim1030/IA_Final.git)
    cd IA_Final/Parcial_3Corte_Grupo2
    ```

2.  **Instala las Dependencias**:
    ```bash
    pip install pandas numpy tensorflow matplotlib scikit-learn
    ```

3.  **Ejecuta los Scripts**:
    Asegúrate de que los archivos CSV originales estén en la misma carpeta. Luego, puedes ejecutar los scripts de preprocesamiento y del modelo. Si tienes los notebooks (`.ipynb`), ábrelos con Jupyter para ejecutar celda por celda.

---

## Contribuciones

¡Las contribuciones son bienvenidas! Si tienes ideas para mejorar el modelo, el preprocesamiento o la documentación, no dudes en abrir un *issue* o enviar un *pull request*.
