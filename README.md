
<div align="center">
<img width="800" height="300" alt="image" src="https://github.com/user-attachments/assets/0e0d8de6-2264-40bb-afe7-dd57be017b3f" />

# DeepFake Detector: AI vs Human  
<br>

[Jeferson Acevedo](https://github.com/Jeferson0809) • [Samuel Noriega](https://github.com/samdng) • [Oscar Silva](https://github.com/Oscar-Silva-D)

---

</div>

La creciente sofisticación de los modelos generativos ha dificultado la distinción entre imágenes reales y aquellas creadas mediante Inteligencia Artificial. Esta problemática afecta la veracidad de la información, la seguridad digital y la confianza en los contenidos visuales que circulan en la web.

Este proyecto busca construir un sistema que pueda distinguir automáticamente si una imagen es real o fue generada por Inteligencia Artificial. Para lograrlo, probamos diferentes tipos de modelos de Deep Learning y comparamos su desempeño.
La idea principal es identificar cuál de ellos funciona mejor frente a un conjunto de imágenes muy variado y con muchos estilos visuales.

> **Objetivo:** Diseñar y evaluar modelos de Deep Learning para la detección automatizada de imágenes generadas por IA.

---

## Enfoques evaluados

1. **Redes Neuronales Profundas (DNN / MLP)**  
   Modelos densos utilizados como línea base.

2. **CNNs diseñadas desde cero**  
   Arquitecturas convolucionales ligeras para aprender patrones espaciales.

3. **Transfer Learning con CNNs preentrenadas**  
   Se empleó *ResNet50* como arquitectura base para aprovechar sus pesos preentrenados y adaptarla a la clasificación entre imágenes reales y sintéticas.

4. **Autoencoder como extractor de características**  
   Se utilizó el autoencoder como extractor de características, seguido de una capa de clasificación basada en un MLP.

---

## Dataset: AI-Generated-vs-Real-Images (Hemg)

🔗 **HuggingFace Dataset:** 
[Link](https://huggingface.co/datasets/Hemg/AI-Generated-vs-Real-Images-Datasets?clone=true)
 *152,710 imágenes*  
- 81,174 sintéticas  
- 71,536 reales  

Este conjunto destaca por su **alta heterogeneidad visual**: fotografías reales, arte digitalizado, documentos escaneados, ilustraciones y paisajes.  
En particular, el subconjunto real incluye imágenes con deterioro físico (rasgaduras, quemaduras, decoloración, ruido analógico), lo que obliga a los modelos a aprender representaciones robustas que diferencien entre:

- **Ruido natural físico**, y  
- **Artefactos sintéticos** propios de algoritmos generativos.

---

## Métricas de evaluación

El desempeño de los modelos se mide mediante:

- Accuracy  
- Precision  
- Recall  
- F1-Score  

Estas métricas permiten evaluar el nivel de discriminación entre imágenes reales y generadas por IA.

---

## Estructura del repositorio

- `data/` — Scripts y notebooks para carga y preparación de datos.  
- `images/` — Resultados, visualizaciones y ejemplos del modelo.  
- `models/` — Implementación de arquitecturas evaluadas.  
- `notebooks/` — Experimentos y análisis exploratorios.  
- `train/` — Scripts de entrenamiento, callbacks y configuración de experimentos.  

---

## Ejemplo del dataset

<div align="center">
  
<img src="https://github.com/user-attachments/assets/7b582700-a545-4db7-b16a-cb6223ef5faa" width="55%">

</div>

---

