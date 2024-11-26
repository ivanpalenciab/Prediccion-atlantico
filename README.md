# Descripción del Proyecto

Este repositorio es la continuación del proyecto de predicción del precio del maíz; está enfocado en la predicción de los precios del maíz en el atlántico. Se predijo el precio del maíz utilizando diversas técnicas de machine learning, incluyendo redes neuronales recurrentes, redes neuronales densas y XGBoost como se hizo en el proyecto anteriormente mencionado.  Adicionalmente, a estos se probó un nuevo modelo que fue el LGBM.

El proceso se llevó a cabo en las siguientes etapas:

1. Descomposición de la serie de tiempo: Se descompuso la serie temporal mediante el método EMD:

 * Empirical Mode Decomposition (EMD).

2. Entrenamiento de los modelos: Cada uno de los modos resultantes de la descomposición fue utilizado para entrenar los siguientes modelos:

 * Redes neuronales recurrentes (RNN).
 * Redes neuronales densas (DNN).
 * XGBoost.
 * LGBM

3. Generación de modelos individuales: Las predicciones de cada modo fueron sumadas para formar un modelo individual.

4. Optimización mediante ensamblaje (ensemble): Finalmente, se utilizó un método de optimización para mejorar el rendimiento del modelo mediante un ensemble de los modelos que obtuvieron los mejores resultados.

# Segunda fase del proyecto

En la segunda fase del proyecto, se probó una nueva variable predictora para determinar si su uso mejoraba el rendimiento de nuestro modelo. Las dos variables evaluadas fueron el clima en el departamento del Atlántico y el precio de los futuros del maíz en Estados Unidos. De estas dos variables, la única que proporcionó una mejora en el modelo fue el precio de los futuros del maíz.

Se reinició el proceso con los pasos anteriormente mencionados, con la diferencia de que se eliminaron los modelos de redes neuronales durante la optimización con PSO-CS, debido a que su rendimiento no era óptimo. El mejor modelo resultante fue un ensemble a través de optimización PSO-CS de los modelos LGBM y XGBoost, utilizando retrasos de 7 semanas y el precio de los futuros del maíz como variables predictoras.

# Siguiente Fase del Modelo

En la última fase del proyecto se probó el modelo para determinar su eficiencia con otros datos diferentes, obteniendo resultados aceptables. 