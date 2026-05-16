Laboratorio 10: Aprendizaje Semi-Supervisado

Introducción

Esta actividad tiene como propósito principal que los estudiantes comprendan el fundamento matemático y conceptual de los algoritmos de aprendizaje semi supervisado a través de la experimentación. Para lograr esto, deberán trabajar en los grupos de laboratorio.

Se espera que los grupos puedan:

* Comprender el fundamento conceptual y matemático de los algoritmos de aprendizaje semisupervisado.

* Sean capaces de implementarlos a través de su lenguaje de programación de preferencia utilizando librerías existentes.

* Realicen experimentación controlada variando hiperparámetros, asegurándose de descartar cualquier problema de sobreajuste/subajuste o similar.

* Para ello, se espera que puedan explicar los hiperparámetros de cada algoritmo.

* Evalúan rigurosamente el desempeño del algoritmo, así como también que puedan discutir del error presentado utilizando análisis visual.

---

Restricciones

* **Elección del Dataset:** Deben trabajar con un dataset real (no dummy, o generado por IA) de al menos 8 columnas y 1000 filas. Para ello puede utilizar fuentes como Kaggle o bien, investigar de diversas fuentes oficiales por su cuenta.

* **Escenario:** Deben simular un escenario semi-supervisado utilizando solo una fracción pequeña de datos etiquetados (5% \- 20%). El resto debe tratarse como no etiquetado.

* **Comparativas:** Deben comparar contra al menos un modelo supervisado puro (baseline) y un modelo semi-supervisado usando 2 algoritmos diferentes de los estudiados en clase.

* **Visualizaciones:** Utilizar gráficos que permitan entender los resultados de la ejecución.

---

Temario de Aprendizaje Semisupervisado

Self-Training

* **Idea central:** Pseudo-etiquetado iterativo.

* **Temas:** Confianza en predicciones , propagación de error y threshold selection.

* **Algoritmos:** Self-training con SVM / Random Forest.

Co-Training

* **Idea central:** Uso de multiples vistas independientes del dataset.

* **Temas:** Supuesto de independencia condicional y feature splitting.

* **Algoritmos:** Co-training con clasificadores distintos (ej. Naive Bayes \+ SVM).

Métodos de Propagación

* **Idea central:** Basados en grafos.

* **Temas:** Construcción de grafos (k-NN, RBF) y Laplacianos.

* **Algoritmos:** Label propagation y label spreading.

Métodos basados en SVM semi-supervisado

* **Idea central:** Maximización del margen con datos no etiquetados.

* **Temas:** Transductive SVM y Laplacian SVM.

* **Algoritmos y enfoque:** Comparar SVM tradicional vs semi-supervisado.

Métodos generativos y clústering con restricciones

* **Idea central:** Modelos probabilísticos y clústering guiado.

* **Temas:** EM con datos parcialmente etiquetados y K-means con restricciones (must-link / cannot link).

* **Algoritmos:** Gaussian Mixtured Models semi-supervisados y Constrained K-means.

---

Actividades

Selección y Análisis de Dataset

* Investigar un dataset a partir de una fuente confiable (UCI, Kaggle, OpenML, etc.), que cumpla con las condiciones anteriormente descritas.

* Análisis y exploración de datos, indagando tipos de variables, dimensionalidad, balance de clases, etc., aplicando todo el procedimiento de EDA al que ya están acostumbrados.

* Preprocesamiento de datos aplicando normalización/estandarización, codificación de variables categóricas, etc.

* Cualquier procedimiento de limpieza y transformación de datos que consideren relevante a partir del objetivo de su investigación y algoritmo.

* Acompañar su EDA con un análisis gráfico y estadístico de los datos presentados.

Diseño Experimental

* Separación de datos (entrenamiento y prueba), considerando que los datos de entrenamiento deben de tener una porción reducida con datos etiquetados y el resto con datos sin etiquetar.

* Evaluar el procentaje de datos etiquetados (5%, 10%, 20%, etc.).

* Definir y comparar el modelo supervisado vs semi-supervisado.

Experimentación

* Variación de hiperparámetros (por ejemplo, número de vecinos, kernel, threshold, etc).

* Evaluación de métricas para determinar el éxito del algoritmo: accuracy, F1-score, recall, RMSE, RMAE, etc. (según corresponda).

* Realizar un análisis de sensibilidad a hiperparámetros y qué tan robusto es el algoritmo con los pocos datos etiquetados.

Visualización

* Gráficos requeridos incluyen curvas de desempeño en comparación al % de etiquetas, matrices de confusión, evolución del error, etc.

* Visualizar cómo queda la predicción en comparación al valor real.

* Incluir cualquier otro gráfico que considere importante para la presentación y discusión de resultados.

---

Evaluación

| Criterio | Puntuación | Descripción |
| :---- | :---- | :---- |
| **Selección y Análisis del Dataset** | 15 puntos | El dataset utilizado cumple con los requisitos establecidos (dataset real, al menos 1000 filas y 8 columnas). Se realiza un análisis exploratorio adecuado del conjunto de datos, incluyendo tipos de variables, balance de clases, análisis estadístico y visualizaciones relevantes. |
| **Preprocesamiento** | 10 puntos | Se aplican correctamente técnicas de limpieza, transformación, normalización/codificación y preparación de datos. Se explica claramente por qué fueron necesarias estas transformaciones para el problema y algoritmo seleccionado. |
| **Diseño Experimental** | 5 puntos | Se implementa correctamente un escenario semisupervisado utilizando únicamente una pequeña fracción de datos etiquetados (5%, 10%, 20%, etc.). Se explica claramente la separación entre datos etiquetados y no etiquetados. |
| **Implementación Modelo Supervisado** | 10 puntos | Se implementa correctamente un modelo supervisado tradicional para utilizarlo como referencia. Se explican los parámetros, configuración y desempeño del modelo. |
| **Modelos Semisupervisados** | 15 puntos | Se implementan correctamente dos algoritmos semisupervisados estudiados en clase. Se explica ampliamente el fundamento conceptual y matemático de ambos métodos, incluyendo supuestos, ventajas y limitaciones. |
| **Experimentación** | 10 puntos | Se realiza experimentación controlada variando hiperparámetros relevantes (threshold, vecinos, kernel, etc.). Se explica claramente cómo afectan los hiperparámetros al desempeño del modelo y se analiza la presencia de sobreajuste/subajuste. |
| **Métricas y Análisis** | 10 puntos | Se utilizan métricas apropiadas para evaluar el desempeño de los modelos (accuracy, F1-score, recall, RMSE, etc.). Se comparan resultados entre modelos supervisados y semisupervisado, acompañados de una explicación crítica y detallada. |
| **Visualización** | 10 puntos | Se incluyen gráficos relevantes como curvas de desempeño según porcentaje de etiquetas, matrices de confusión, evolución del error y comparación entre valores reales y predicciones. Los gráficos son claros y correctamente interpretados. |
| **Informe y Organización** | 10 puntos | El reporte está redactado de manera formal y estructurada. Incluye introducción, metodología, análisis exploratorio, diseño experimental, resultados, discusión y conclusiones. No tiene subtítulos como Actividad 1, Actividad 2…., Punto 1, Punto n. El repositorio, código fuente y enlaces al dataset son funcionales y organizados. |
| **Conclusiones** | 5 puntos | Se selecciona el mejor modelo semisupervisado con base en evidencia experimental. Se reflexiona críticamente sobre el comportamiento de los algoritmos, ventajas, limitaciones y efecto de trabajar con pocos datos etiquetados. |

---

Notas

* La consultoría es en grupo, por lo que solo se tendrán en cuenta los grupos conformados por más de un especialista.

* Cada individuo será evaluado de forma individual basado en sus aportes al trabajo grupal, por lo que deben versionar el código para poder revisar las contribuciones de cada uno.

* Adicionalmente, se tendrá una matriz de co-evaluación a los demás integrantes del grupo.

* Tiene que poderse comprobar su aporte al trabajo grupal a través de commits.

* Si no existen al menos 3 commits con su aporte significativo no va a tener nota de la hoja de trabajo.

* Utilice una herramienta que permita registrar los aportes de cada uno.

* Debe entregar los avances durante el período de clase para poder tener derecho a la calificación de la entrega.

* El dataset seleccionado debe estar disponible públicamente en internet.

---

Material a Entregar

* Archivo .r o .py con el código fuente.

* Link del set de datos seleccionado.

* Vínculo del repositorio usado para trabajar la hoja de trabajo.

* Documento en pdf con el reporte de resultados.

Fechas de Entrega

* **ENTREGA FINAL:** 15 de Mayo (15:40hrs, antes de clase).

* Deberá presentar a sus compañeros en la clase del viernes 15 de Mayo.  
