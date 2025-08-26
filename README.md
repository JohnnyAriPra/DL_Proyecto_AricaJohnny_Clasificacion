# Clasificación de Basura utilizando Deep Learning: Estudio Comparativo de tres Modelos de Transfer Learning

## Ruta Elegida: Clasificación con Modelos Preentrenados

### Dataset:
El dataset utilizado en este proyecto proviene de **Roboflow** y contiene imágenes de basura clasificadas en seis categorías: cartón, vidrio, plástico, metal, papel y basura. Este conjunto de datos está dividido en tres particiones: **train**, **val** y **test**.

- **Fuente:** [Roboflow Garbage Classification](https://universe.roboflow.com/jakob-kruijer/garbage-classification-fw9gx)
- **Licencia:** [Roboflow License](https://roboflow.com/terms)
- **Número de Imágenes:**
  - **Train:** 3092 imágenes
  - **Validation:** 504 imágenes
  - **Test:** 252 imágenes

---

## Cómo Ejecutar:

1. **Abrir en Google Colab:**
   - Abre el archivo `Proyecto_Clasificacion.ipynb` en Google Colab desde tu Google Drive o en el [enlace proporcionado](#) (asegúrate de tener acceso a la carpeta de Google Drive).

2. **Seleccionar GPU:**
   - Ve a **Entorno de ejecución > Cambiar tipo de entorno > Acelerador de hardware** y selecciona **GPU** para acelerar el entrenamiento de los modelos.

---

## Cómo Entrenar y Evaluar:

### Pasos para Entrenar:

1. **Configurar el Entorno:**
   - Verifica que se esté utilizando la GPU en Google Colab. En las primeras celdas del notebook, el código automáticamente verifica la disponibilidad de la GPU.

2. **Instalar Librerías Necesarias:**
   - El código del notebook instalará automáticamente las librerías requeridas como **TensorFlow**, **Keras**, **scikit-learn**, entre otras.

3. **Cargar y Preprocesar el Dataset:**
   - Los datos se cargan directamente desde Google Drive y se preprocesan para que sean compatibles con los modelos preentrenados (MobileNetV3Small, EfficientNetB0 y ResNet50).

4. **Entrenamiento de Modelos:**
   - Los modelos se entrenan utilizando el enfoque de Transfer Learning con **fine-tuning**. Cada modelo se entrena durante 20 épocas con los conjuntos de datos de entrenamiento y validación.
   - Se usa el optimizador **Adam** y las métricas **Accuracy**, **F1 Macro**, **Precision Macro**, **Recall Macro**, y **ROC-AUC Macro** para la evaluación del rendimiento.

### Pasos para Evaluar:

1. **Evaluar en el Conjunto de Prueba:**
   - Se evalúa cada modelo en el conjunto de prueba para calcular las métricas mencionadas anteriormente.

2. **Generar la Matriz de Confusión:**
   - Al final de la evaluación, se genera la **matriz de confusión** para cada modelo, visualizando el rendimiento de las predicciones en las diferentes clases.

---

## Cómo Generar la Tabla y el Gráfico de Métricas:

1. **Generar Tabla Comparativa:**
   - Los resultados de la evaluación de los tres modelos se presentan en una tabla comparativa, que incluye las métricas de rendimiento (accuracy, F1 macro, precision macro, recall macro, y ROC-AUC macro) en el conjunto de prueba.

2. **Generar Gráficos Comparativos:**
   - Durante la evaluación, se generarán gráficos comparativos para cada métrica (accuracy, F1 macro, etc.) entre los tres modelos. Estos gráficos permiten visualizar de manera clara cuál modelo tiene el mejor rendimiento en cada métrica.

3. **Ubicación de los Resultados:**
   - Los resultados generados (gráficos y tablas) se guardan en la carpeta `results` dentro de Google Drive. Puedes acceder a ellos fácilmente para revisarlos o utilizarlos en tu informe.

---

## Estructura del Proyecto:

```
/DL_Proyecto_AricaJohnny_Clasificacion
    /data
        /roboflow_splits
            /train
            /valid
            /test
    /models
        A_MobileNetV3Small.keras
        B_EfficientNetB0.keras
        C_ResNet50.keras
    /results
        confusion_MobileNetV3Small.png
        confusion_EfficientNetB0.png
        confusion_ResNet50.png
        train_acc_MobileNetV3Small.png
        train_acc_EfficientNetB0.png
        train_acc_ResNet50.png
        ...
    /notebook
	Proyecto_Clasificacion.ipynb
    /README
	README.md
```

---

## Enlace al Proyecto:
- [Enlace al código en Google Drive](#)
https://drive.google.com/drive/folders/1TRKTMPqi1A2O4xtC7OfOulFfWDTr87np?usp=sharing 
---

Este `README.md` proporciona las instrucciones necesarias para que puedas ejecutar el proyecto de manera eficiente. Asegúrate de tener configurado el entorno adecuado en Google Colab y seguir los pasos descritos para entrenar y evaluar los modelos.
