# 🫁 Clasificación de Cáncer de Pulmón con Deep Learning  
# 🫁 Lung Cancer Classification with Deep Learning  

## Dataset IQ-OTH/NCCD

---

# 🇪🇸 Versión en Español

## 📌 Descripción del Proyecto

Este proyecto aborda la clasificación automática de cáncer de pulmón a partir de imágenes de tomografía computarizada (CT) utilizando técnicas de Deep Learning.

El objetivo es desarrollar un modelo capaz de clasificar las imágenes en tres categorías:

- 🟢 Normal  
- 🟡 Benigno  
- 🔴 Maligno  

---

## 📂 Dataset

Se utiliza el **IQ-OTH/NCCD Lung Cancer Dataset**, recopilado por:

- Iraq Oncology Teaching Hospital (IQ-OTH)  
- National Center for Cancer Diseases (NCCD)  

🔗 Dataset oficial (Mendeley Data):  
https://data.mendeley.com/datasets/bhmdr45bh2  

🔗 Versión utilizada (Kaggle):  
https://www.kaggle.com/datasets/adityamahimkar/iqothnccd-lung-cancer-dataset  

---

## 📊 Composición del Dataset

Según la documentación oficial, el dataset completo contiene:

- 1.190 imágenes CT  
- 110 pacientes  
- 3 clases: Normal, Benigno y Maligno  

En la versión utilizada en este proyecto:

- Se dispone de **1.097 imágenes etiquetadas**  
- Las imágenes restantes hasta completar las 1.190 se encuentran en una carpeta `test/` sin etiquetas explícitas  

---

## 🗂 Estructura de Carpetas

```
dataset/
   ├── Benign/
   ├── Malignant/
   ├── Normal/
   └── test/
```

- Las carpetas `Benign`, `Malignant` y `Normal` contienen las imágenes etiquetadas.  
- La carpeta `test` contiene imágenes adicionales sin etiquetas visibles.  

---

## 📊 División del Dataset

A partir de las **1.097 imágenes etiquetadas**, se realizó una división estratificada:

- **Train:** 767 imágenes (69.9%)  
- **Validation:** 165 imágenes (15.0%)  
- **Test:** 165 imágenes (15.0%)  

---

## 📈 Distribución por Clases

### 🔹 Train (767 imágenes)

| Clase      | Número | Porcentaje |
|------------|--------|------------|
| Malignant  | 392    | 51.11%     |
| Normal     | 291    | 37.94%     |
| Benign     | 84     | 10.95%     |

### 🔹 Validation (165 imágenes)

| Clase      | Número | Porcentaje |
|------------|--------|------------|
| Malignant  | 84     | 50.91%     |
| Normal     | 63     | 38.18%     |
| Benign     | 18     | 10.91%     |

### 🔹 Test (165 imágenes)

| Clase      | Número | Porcentaje |
|------------|--------|------------|
| Malignant  | 85     | 51.52%     |
| Normal     | 62     | 37.58%     |
| Benign     | 18     | 10.91%     |

---

## ⚠️ Desbalanceo de Clases

Se observa un **desbalance significativo entre clases**:

- Malignant ≈ 51%  
- Normal ≈ 38%  
- Benign ≈ 11%  

La clase **Benign** está claramente subrepresentada, lo que puede afectar el aprendizaje del modelo y sesgar las predicciones hacia la clase mayoritaria.

Por ello, la evaluación no debe basarse únicamente en la accuracy, sino también en métricas más robustas como:

- Precision por clase  
- Recall por clase  
- F1-score (macro)  
- Matriz de confusión  

---

## 🏆 Estado del Arte (SOTA)

El dataset IQ-OTH/NCCD ha sido ampliamente utilizado en investigaciones recientes, reportando resultados muy elevados.

### 🔬 Trabajos Relevantes

**Benamara et al. (2025)**  
Modelo: Fine-Tuning multinivel de VGG16, MobileNetV2 y ResNet50  
Accuracy reportado: 99.54%  
https://link.springer.com/article/10.1007/s13721-025-00590-6  

**Giri et al. (2025)**  
Modelo: CNN-LSTM con mecanismo de atención  
Accuracy reportado: 99.67%  
https://link.springer.com/chapter/10.1007/978-3-031-82706-8_8  

**Raza et al. (2023)**  
Modelo: EfficientNet-B1 (Lung-EffNet)  
Accuracy reportado: 99.10%  
https://www.sciencedirect.com/science/article/pii/S0952197623010862  

---

# 🇬🇧 English Version

## 📌 Project Description

This project focuses on the automatic classification of lung cancer from Computed Tomography (CT) images using Deep Learning techniques.

The goal is to develop a model capable of classifying CT images into three categories:

- 🟢 Normal  
- 🟡 Benign  
- 🔴 Malignant  

---

## 📂 Dataset

The project uses the **IQ-OTH/NCCD Lung Cancer Dataset**, collected by:

- Iraq Oncology Teaching Hospital (IQ-OTH)  
- National Center for Cancer Diseases (NCCD)  

🔗 Official Dataset (Mendeley Data):  
https://data.mendeley.com/datasets/bhmdr45bh2  

🔗 Kaggle Version Used:  
https://www.kaggle.com/datasets/adityamahimkar/iqothnccd-lung-cancer-dataset  

---

## 📊 Dataset Composition

According to the official documentation, the full dataset contains:

- 1,190 CT images  
- 110 patients  
- 3 classes: Normal, Benign, and Malignant  

In the version used in this project:

- **1,097 labeled images** are available  
- The remaining images (to complete 1,190) are located in a `test/` folder without explicit labels  

---

## 🗂 Folder Structure

```
dataset/
   ├── Benign/
   ├── Malignant/
   ├── Normal/
   └── test/
```

- `Benign`, `Malignant`, and `Normal` contain labeled images.  
- `test` contains additional unlabeled images.  

---

## 📊 Dataset Split

From the **1,097 labeled images**, a stratified split was performed:

- **Train:** 767 images (69.9%)  
- **Validation:** 165 images (15.0%)  
- **Test:** 165 images (15.0%)  

---

## 📈 Class Distribution

### 🔹 Train (767 images)

| Class      | Count | Percentage |
|------------|--------|------------|
| Malignant  | 392    | 51.11%     |
| Normal     | 291    | 37.94%     |
| Benign     | 84     | 10.95%     |

### 🔹 Validation (165 images)

| Class      | Count | Percentage |
|------------|--------|------------|
| Malignant  | 84     | 50.91%     |
| Normal     | 63     | 38.18%     |
| Benign     | 18     | 10.91%     |

### 🔹 Test (165 images)

| Class      | Count | Percentage |
|------------|--------|------------|
| Malignant  | 85     | 51.52%     |
| Normal     | 62     | 37.58%     |
| Benign     | 18     | 10.91%     |

---

## ⚠️ Class Imbalance

There is a **significant class imbalance**:

- Malignant ≈ 51%  
- Normal ≈ 38%  
- Benign ≈ 11%  

The **Benign** class is clearly underrepresented, which may negatively impact model learning and bias predictions toward majority classes.

Therefore, evaluation should not rely solely on accuracy, but also on more robust metrics such as:

- Per-class Precision  
- Per-class Recall  
- Macro F1-score  
- Confusion Matrix  

---

## 🏆 State of the Art (SOTA)

The IQ-OTH/NCCD dataset has been widely used in recent research, reporting very high performance results.

### 🔬 Relevant Works

**Benamara et al. (2025)**  
Model: Multi-level Fine-Tuning of VGG16, MobileNetV2, and ResNet50  
Reported Accuracy: 99.54%  
https://link.springer.com/article/10.1007/s13721-025-00590-6  

**Giri et al. (2025)**  
Model: CNN-LSTM with Attention Mechanism  
Reported Accuracy: 99.67%  
https://link.springer.com/chapter/10.1007/978-3-031-82706-8_8  

**Raza et al. (2023)**  
Model: EfficientNet-B1 (Lung-EffNet)  
Reported Accuracy: 99.10%  
https://www.sciencedirect.com/science/article/pii/S0952197623010862  

---


