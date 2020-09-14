# Crítica: Combining Predictions for Accurate Recommender Systems

Este paper propone métodos de "ensemble blending", el cual se basa en combinar recomendaciones provenientes de distintos métodos, para así encontrar una mejor solución para el 
problema de CF.

El paper explica de manera breve los métodos principales de CF de manera teorica, para luego hacer lo mismo, explicando de manera un poco más detallada, los distintos métodos de 
combinación usados para generar una recomendación final a partir de la combinación de recomendaciones por parte de los métodos tradicionales.

Finalmente, en los resultados se muestra que el sistema propuesto en el paper supera al rendimiento de los sistemas del estado del arte y al resto de los sistemas disponibles de 
ensemble blending. Algo muy beneficioso que aporta este paper es que proporciona de manera libre y gratuita el código y dataset con el que fue testeado el experimento. Esto permite
que sea sencillo reproducir el experimento para así corroborrar los resultados o realizar cambios con el objetivo de encontrar mejoras en el procedimiento.

Un paso que me llamó la atención que no logré comprender la razón es el hecho de que para el testeo del rendimiento de los algoritmos, se dividió el set de "probe" del dataset
del Netflix Prize, en un set de train y un set de test, pero la división se hizo con un 50% de los datos del set original para cada set. Esto es un split muy inusual, ya que en 
general, se proporciona una razón mayor al set de entrenamiento, ya que este en general es más relevante para el rendimiento de los algoritmos. La razón de este split inusual no
me quedó clara, pero no creo que influya en las conclusiones finales y, nuevamente, el hecho de que se proporcione de manera abierta el código con el que se realizó el test, da 
confianza de que decisiones inusuales como esta puedan ser testeadas con decisiones más estándar de manera fácil y así corroborar los resultados de manera óptima.
