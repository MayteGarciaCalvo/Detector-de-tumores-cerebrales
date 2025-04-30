# 🧠 Detector de Tumores Cerebrales con Deep Learning

![MRI Brain Scan](https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/MRI_head_side.jpg/640px-MRI_head_side.jpg)

Este proyecto aborda el problema del **diagnóstico temprano de tumores cerebrales** mediante técnicas de **visión por computador** y **aprendizaje profundo**. A través de imágenes de resonancia magnética (MRI) obtenidas de un dataset de Kaggle, se ha entrenado un modelo basado en **Keras y TensorFlow** capaz de **detectar automáticamente tumores cerebrales**.

## 🎯 Objetivo

Crear una herramienta de apoyo para profesionales médicos que:
- Agilice el diagnóstico.
- Reduzca el riesgo de errores humanos.
- Mejore la precisión en la detección de tumores, especialmente en entornos con recursos limitados.

---

## 📂 Estructura del Dataset

Las imágenes se agrupan en dos clases:
- `yes`: Con presencia de tumor cerebral.
- `no`: Sin presencia de tumor.

Cada imagen fue redimensionada a **128x128 píxeles RGB** para facilitar el procesamiento.

El dataset fue dividido así:
- **70%** para entrenamiento.
- **15%** para validación.
- **15%** para prueba.

---

## 🧪 Modelo y Arquitectura

Se utilizó una red neuronal convolucional (CNN) compuesta por:

- Capas Conv2D y MaxPooling para extracción de características.
- Capa Flatten + Densa para clasificación.
- Función de pérdida: `binary_crossentropy`.
- Métrica principal: `accuracy`.

El modelo se entrenó por **20 épocas** con imágenes normalizadas y procesamiento optimizado con `tf.data.AUTOTUNE`.

---

## 📊 Resultados

- **Precisión en conjunto de prueba:** `96.43%`
- **AUC (Área bajo la curva ROC):** `0.90`
- **Reporte de clasificación:**
  - **No Tumor:** Precisión 100%, Recall 79%
  - **Con Tumor:** Precisión 81%, Recall 100%

Incluye visualización de:
- Curva ROC.
- Matriz de confusión.
- Evolución de precisión y pérdida por época.

---

## 🧠 Visualizaciones de imágenes

Se muestran ejemplos aleatorios de imágenes con y sin tumor para confirmar la calidad del dataset y su balance.

---

## 🗃️ Dataset

- **Fuente:** [Kaggle - Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)

---

## 💾 Archivos Generados

- `modelo_tumores.h5`: Modelo entrenado.
- `historial_entrenamiento.pkl`: Historial de entrenamiento.
- Gráficos de precisión, pérdida, curva ROC, y matriz de confusión.

---

## 🙌 Agradecimientos

Gracias por visitar este proyecto.  
Este modelo puede ser base para desarrollos futuros más avanzados, como la segmentación de tumores o detección multicategoría.

**Autor:** [Iván Romaña](https://github.com/IRoma88)

## 📬 Contacto

ivan.romana88@gmail.com
