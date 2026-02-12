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

- **1.097 imágenes etiquetadas**  
- Las imágenes restantes hasta completar las 1.190 se encuentran en `test/` sin etiquetas explícitas  

---

## 🗂 Estructura de Carpetas

```
dataset/
   ├── Benign/
   ├── Malignant/
   ├── Normal/
   └── test/
```

---

## 📊 División del Dataset

- **Train:** 767 imágenes (69.9%)  
- **Validation:** 165 imágenes (15.0%)  
- **Test:** 165 imágenes (15.0%)  

---

## 📈 Distribución por Clases (Train)

| Clase      | Número | Porcentaje |
|------------|--------|------------|
| Malignant  | 392    | 51.11%     |
| Normal     | 291    | 37.94%     |
| Benign     | 84     | 10.95%     |

---

## ⚠️ Desbalanceo de Clases

- Malignant ≈ 51%  
- Normal ≈ 38%  
- Benign ≈ 11%  

La clase **Benign** está subrepresentada.

Se recomienda evaluar con:

- Precision por clase  
- Recall por clase  
- F1-score (macro)  
- Matriz de confusión  

---

## 🏆 Estado del Arte (SOTA)

### 🔬 Trabajos Relevantes

**Benamara et al. (2025)**  
VGG16, MobileNetV2 y ResNet50 Fine-Tuned  
Accuracy: 99.54%  

**Giri et al. (2025)**  
CNN-LSTM + Atención  
Accuracy: 99.67%  

**Raza et al. (2023)**  
EfficientNet-B1  
Accuracy: 99.10%  

---

## 📊 Comparación de Resultados Reportados

| Autor / Año            | Modelo                              | Accuracy (%) | Enfoque |
|------------------------|--------------------------------------|--------------|----------|
| Giri et al. (2025)     | CNN-LSTM + Atención                 | 99.67%       | Deep Learning Híbrido |
| Benamara et al. (2025) | VGG16 Fine-Tuned Multinivel         | 99.54%       | Transfer Learning |
| Raza et al. (2023)     | EfficientNet-B1                     | 99.10%       | Transfer Learning |

---

# 🇬🇧 English Version

## 📌 Project Description

This project focuses on automatic lung cancer classification from CT images using Deep Learning techniques.

The model classifies images into:

- 🟢 Normal  
- 🟡 Benign  
- 🔴 Malignant  

---

## 📂 Dataset

**IQ-OTH/NCCD Lung Cancer Dataset**

- 1,190 CT images  
- 110 patients  
- 3 classes  

Used version:

- **1,097 labeled images**
- Remaining images located in `test/` without labels  

---

## 📊 Dataset Split

- **Train:** 767 images (69.9%)  
- **Validation:** 165 images (15.0%)  
- **Test:** 165 images (15.0%)  

---

## ⚠️ Class Imbalance

- Malignant ≈ 51%  
- Normal ≈ 38%  
- Benign ≈ 11%  

The **Benign** class is underrepresented.

Recommended evaluation metrics:

- Per-class Precision  
- Per-class Recall  
- Macro F1-score  
- Confusion Matrix  

---

## 🏆 State of the Art (SOTA)

### 🔬 Relevant Works

**Benamara et al. (2025)**  
Fine-Tuned VGG16, MobileNetV2, ResNet50  
Accuracy: 99.54%  

**Giri et al. (2025)**  
CNN-LSTM + Attention  
Accuracy: 99.67%  

**Raza et al. (2023)**  
EfficientNet-B1  
Accuracy: 99.10%  

---

## 📊 Reported Results Comparison

| Author / Year          | Model                               | Accuracy (%) | Approach |
|------------------------|--------------------------------------|--------------|-----------|
| Giri et al. (2025)     | CNN-LSTM + Attention                | 99.67%       | Hybrid Deep Learning |
| Benamara et al. (2025) | Multi-level Fine-Tuned VGG16        | 99.54%       | Transfer Learning |
| Raza et al. (2023)     | EfficientNet-B1                     | 99.10%       | Transfer Learning |

---
