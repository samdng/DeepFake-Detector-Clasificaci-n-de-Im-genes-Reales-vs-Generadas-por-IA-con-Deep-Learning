<div align="center">
<img width="800" height="300" alt="image" src="https://github.com/user-attachments/assets/0e0d8de6-2264-40bb-afe7-dd57be017b3f" />

# 🤖 DeepFake Detector: AI vs Human  
<br>

👨‍💻 [Jeferson Acevedo](https://github.com/Jeferson0809) •  👨‍💻 [Samuel Noriega](https://github.com/samdng) •  👨‍💻 [Oscar Silva](https://github.com/Oscar-Silva-D)

---

</div>

La creciente sofisticación de los modelos generativos ha dificultado la distinción entre imágenes reales y aquellas creadas mediante Inteligencia Artificial. Esta problemática afecta la veracidad de la información, la seguridad digital y la confianza en los contenidos visuales que circulan en la web.

Este proyecto busca construir un sistema que pueda distinguir automáticamente si una imagen es real o fue generada por IA. Para lograrlo, se entrenaron y compararon diferentes modelos de Deep Learning sobre un conjunto de imágenes altamente variado.

> 🎯 **Objetivo:** Diseñar y evaluar modelos capaces de clasificar imágenes reales vs generadas por IA.

---

## 🧠 Enfoques evaluados

1. **🔹 Redes Neuronales Profundas (DNN / MLP)**  
   Modelos densos usados como línea base.

2. **🔹 CNNs diseñadas desde cero**  
   Arquitecturas convolucionales ligeras para extracción de patrones espaciales.

3. **🔹 Transfer Learning con CNN preentrenada**  
   Se empleó **ResNet50**, ajustada para distinguir imágenes reales y sintéticas.

4. **🔹 Autoencoder como extractor de características**  
   Utilizado para generar embeddings, seguido de una capa MLP de clasificación.

---

## 🗂️ Dataset: AI-Generated-vs-Real-Images (Hemg)

🔗 **HuggingFace Dataset:**  
https://huggingface.co/datasets/Hemg/AI-Generated-vs-Real-Images-Datasets?clone=true

📦 **152,710 imágenes:**
- 🧪 81,174 sintéticas  
- 📷 71,536 reales  

Este dataset destaca por su **alta variabilidad visual**: fotos reales, ilustraciones, arte digital, escaneos y documentos envejecidos.  
El subconjunto real incluye imágenes con:

- 🟤 Decoloración  
- 🔥 Quemaduras  
- 📄 Rasgaduras  
- 🎞️ Ruido analógico  

Estas características obligan a los modelos a ser robustos ante variaciones reales y artefactos generados por IA.

---

## 📏 Métricas de evaluación

Los modelos se evaluaron usando:

- 🎯 Accuracy  
- 🎯 Precision  
- 🎯 Recall  
- 📈 AUC  

Estas métricas miden la capacidad de distinguir entre imágenes reales y sintéticas.

---

## 📊 Resultados del estudio

| **Modelo**              | **Accuracy** | **Precisión** | **Recall** | **AUC**   |
|-------------------------|--------------|----------------|------------|-----------|
| 🔵 **DNN**              | 71.12%       | 71.24%         | 71.30%     | 70.00%    |
| 🟣 **Vision Transformer** | 73.64%     | 73.64%         | 73.64%     | 82.32%    |
| 🟠 **CNN**              | 62.53%       | 62.36%         | 62.34%     | 60.00%    |
| 🔴 **Transfer Learning (ResNet50)** | 86.61% | 86.95% | 87.00% | 94.40% |
| 🟢 **AutoEncoder**      | 82.00%       | 82.00%         | 82.00%     | 89.00%    |

---

## 🗂️ Estructura del repositorio

### 📸 `images/` — Resultados por modelo
- **Autoencoder/** → Matriz, reporte y métricas.  
- **CNN/** → Accuracy, matriz de confusión y reporte.  
- **CNN+Transfer-Learning/** → Resultados del modelo ResNet50.  
- **DNN/** → Curvas, matrices y reportes.  
- **Vision-Transformer/** → Métricas y visualizaciones del ViT.

### 🧠 `models/` — Modelos entrenados
- `CNN.keras`  
- `CNNTL.keras`  
- `DNN_model.keras`

### 📓 `notebooks/` — Notebooks utilizados
- `Autoencoder.ipynb`  
- `CNN.ipynb`  
- `CNN+transfer-learning.ipynb`  
- `DNN.ipynb`  
- `Vision_Transformer.ipynb`

### 📄 `README.md`
Documentación completa del proyecto.

---

## 🖼️ Ejemplo del dataset

<div align="center">
  
<img width="880" height="440" alt="image" src="https://github.com/user-attachments/assets/0b8eaefd-1059-466c-a0ae-96798a2162e4" />

</div>

---

## 🎬 Presentación del Proyecto

📹 **Video en YouTube:**  
https://www.youtube.com/watch?v=30R0Vg_JfKM

🖥️ **Diapositivas en Canva:**  
https://www.canva.com/design/DAG3My3vKXM/2s-gnqmvPG6LM3aHe3lMQQ/edit?utm_content=DAG3My3vKXM&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

---

## 🏁 Conclusiones

El **Transfer Learning con ResNet50** fue la arquitectura con mejor desempeño, demostrando gran capacidad para diferenciar imágenes reales de imágenes generadas por IA.  
La diversidad del dataset permitió evaluar la robustez de cada modelo ante ruido, degradación física y estilos visuales muy variados.

Este proyecto constituye una base para futuros sistemas de **detección de DeepFakes** y herramientas de **verificación digital**.

---
