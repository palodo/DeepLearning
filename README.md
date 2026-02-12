# 🫁 Clasificación de Cáncer de Pulmón con Deep Learning
## Dataset IQ-OTH/NCCD

---

# 📌 Descripción del Proyecto

Este proyecto aborda la clasificación automática de cáncer de pulmón a partir de imágenes de tomografía computarizada (CT) utilizando técnicas de Deep Learning.

El objetivo es desarrollar un modelo capaz de clasificar las imágenes en tres categorías:

- 🟢 Normal
- 🟡 Benigno
- 🔴 Maligno

---

# 📂 Dataset

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

# 📊 División del Dataset

A partir de las **1.097 imágenes etiquetadas**, se realizó una división estratificada:

- **Train:** 767 imágenes (69.9%)
- **Validation:** 165 imágenes (15.0%)
- **Test:** 165 imágenes (15.0%)

---

# 📈 Distribución por Clases

## 🔹 Train (767 imágenes)

| Clase      | Número | Porcentaje |
|------------|--------|------------|
| Malignant  | 392    | 51.11%     |
| Normal     | 291    | 37.94%     |
| Benign     | 84     | 10.95%     |

---

## 🔹 Validation (165 imágenes)

| Clase      | Número | Porcentaje |
|------------|--------|------------|
| Malignant  | 84     | 50.91%     |
| Normal     | 63     | 38.18%     |
| Benign     | 18     | 10.91%     |

---

## 🔹 Test (165 imágenes)

| Clase      | Número | Porcentaje |
|------------|--------|------------|
| Malignant  | 85     | 51.52%     |
| Normal     | 62     | 37.58%     |
| Benign     | 18     | 10.91%     |

---

# ⚠️ Desbalanceo de Clases

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

# 🏆 Estado del Arte (SOTA)

El dataset IQ-OTH/NCCD ha sido ampliamente utilizado en investigaciones recientes, reportando resultados muy elevados.

## 🔬 Trabajos Relevantes

### 1️⃣ Benamara et al. (2025)
Modelo: Fine-Tuning multinivel de VGG16, MobileNetV2 y ResNet50  
Accuracy reportado: 99.54%

https://link.springer.com/article/10.1007/s13721-025-00590-6

---

### 2️⃣ Giri et al. (2025)
Modelo: CNN-LSTM con mecanismo de atención  
Accuracy reportado: 99.67%

https://link.springer.com/chapter/10.1007/978-3-031-82706-8_8

---

### 3️⃣ Raza et al. (2023)
Modelo: EfficientNet-B1 (Lung-EffNet)  
Accuracy reportado: 99.10%

https://www.sciencedirect.com/science/article/pii/S0952197623010862

---

# 📊 Comparación de Resultados Reportados

| Autor / Año            | Modelo                              | Accuracy (%) | Enfoque |
|------------------------|--------------------------------------|--------------|----------|
| Giri et al. (2025)     | CNN-LSTM + Atención                 | 99.67%       | Deep Learning Híbrido |
| Benamara et al. (2025) | VGG16 Fine-Tuned Multinivel         | 99.54%       | Transfer Learning |
| Raza et al. (2023)     | EfficientNet-B1                     | 99.10%       | Transfer Learning |

---

# 📉 Limitaciones

- Dataset de tamaño reducido (~1.100 imágenes etiquetadas).
- Desbalance notable de clases (Benign subrepresentada).
- Conjunto `test/` sin etiquetas explícitas.
- Posible riesgo de sobreajuste debido a la cantidad limitada de datos.
- Los resultados reportados en la literatura (>99%) deben analizarse críticamente dado el tamaño del dataset.

---

# 🚀 Conclusión

El IQ-OTH/NCCD se ha convertido en un benchmark frecuente en clasificación automática de cáncer de pulmón mediante Deep Learning.

Sin embargo, debido a su tamaño limitado y al desbalance de clases, es fundamental aplicar una metodología rigurosa y evaluar el modelo utilizando métricas adecuadas que reflejen el rendimiento real en todas las clases.

Este proyecto busca proporcionar una implementación reproducible y una evaluación realista del problema de clasificación multiclase en imágenes CT pulmonares.

