# DeepFake Detector: AI vs Human
*Clasificacion de imagenes reales vs generadas con IA por medio de DeepLearning*

* ***Jefferson Acevedo***
* ***Samuel Noriega***
* ***Oscar Silva***

La creciente sofisticación de los modelos generativos ha dificultado la distinción entre imágenes reales y artificiales. Este fenómeno impacta negativamente en la veracidad de la información y la seguridad digital, haciendo imperativo el desarrollo de herramientas de detección automatizada.

Tenemos como objetivo general desarrollar un sistema de clasificación basado en redes neuronales capaz de discriminar entre imágenes fotográficas reales e imágenes sintéticas generadas por IA.

El proyecto se centra en un análisis comparativo de distintas arquitecturas de Deep Learning para identificar la más eficiente en esta tarea específica. Se evaluarán los siguientes enfoques:

1. Redes Neuronales Profundas (DNN / MLP).

2. Redes Neuronales Convolucionales (CNN) diseñadas desde cero.

3. CNNs optimizadas mediante Transfer Learning.
   
5. Autoencoders para detección de anomalías.

El estudio se fundamenta en el dataset 'AI-Generated-vs-Real-Images' (Hemg) alojado en HuggingFace, el cual consta de un corpus de 152,710 muestras balanceadas entre clases (81,174 sintéticas y 71,536 reales).

Una característica crítica de este conjunto de datos es su alta heterogeneidad y entropía visual. A diferencia de los datasets curados tradicionales, este repositorio incluye una vasta diversidad de dominios visuales que van más allá de la fotografía digital estándar, incorporando digitalizaciones de obras de arte, escaneos de documentos, ilustraciones y paisajes.

Particularmente, el subconjunto de imágenes reales presenta desafíos significativos para la clasificación, dado que incluye muestras con degradación física y temporal. Se observan instancias con decoloración cromática, rasgaduras, quemaduras y artefactos propios del envejecimiento del material (ruido analógico). Esta diversidad obliga a los modelos a aprender características robustas, diferenciando entre el ruido natural del mundo físico y los artefactos de generación sintética propios de los algoritmos de IA.

El desempeño de los modelos se medirá a través de métricas de clasificación supervisada (Accuracy, Precision, Recall, F1-score). El alcance del proyecto es un prototipo de detección y no contempla la generación de contenido.
