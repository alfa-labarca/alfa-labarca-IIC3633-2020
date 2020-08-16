#Crítica: _Item-Based Collaborative Filtering Recommendation
Algorithms_

El ensayo en cuestión presenta una alternativa basada en _items_ para los algoritmos de _collaborative filtering_,
los cuales generalmente son enfocados en usuarios implementados en distintos sitios de _E-Commerce_. Como explica el paper, en el momento de su publicación, los algoritmos
más populares usados por sitios en el momento de realizar recomendaciones a los usuarios basadas en sus gustos, se basan buscar usuarios que tengan gustos similares, y realizar
recomendaciones basadas en _items_ que estos usuarios similares han opinado de manera positiva. Este tipo de algoritmos, a pesar de que han demostrado tener una presición alta,
presentan un problema de escalabilidad, en el cual, mientras mayor cantidad de usuarios tenga el sitio, la cantidad de posibles usuarios similares para cada usuario al que se le
desea presentar una recomendación, aumenta, con lo cual aumenta el tiempo y complejidad de los algoritmos hasta un punto en que no pueden no lograr a ser capaces de funcionar con
la velocidad óptima si se tiene un sitio con miles o millones de usuarios. En cambio, un enfoque basado en _items_, se trata de buscar _items_ que son similares a otros _items_
que el usuario en cuestion a reaccionado de manera positiva. Como la cantidad de items en un sitio suelen ser significativamente menor a la cantidad de usuarios y suelen ser más
estáticos (se crean y borran menos items que usuarios en general), este enfoque puede solucionar este problema.

La organización y presentación de información de este ensayo está muy bien lograda, permite una continuidad natural en la lectura. Al introducir conceptos nuevos que son
relevantes en el seguimiento, se explican brevemente de manera en que son fáciles de entender, sin perder el foco del ensayo. Por ejemplo, al explicar cómo se estima la similitud
entre dos usuarios o dos _items_, explica que existen tres métodos: La similitud basada en Coseno, la similitud basada en correlación y la similitud basada en coseno ajustado.
Entender estos tres métodos es relevante para la investigación, debido a que en el momento de evaluar experimentalmente este enfoque, se compara el rendimiento usando estos tres
métodos para estimar la similitud. Sin embargo, debido a que el funcionamiento de estos métodos no son el tema central del ensayo, cada uno de ellos son explicados en no más de 
dos párrafos de manera general, lo que permite que el lector entienda el razonamiento y funcionamiento general detrás de estos métodos sin necesidad de entenderlos a profundidad.
Lo mismo ocurre al comparar los métodos de suma ponderada y regresión al momento de explicar la computación de la predicción final y las métricas de evaluación utilizadas. Cuando 
es necesario además se presentan diagramas de apoyo para explicar conceptos relevantes.

En el momento de presentar los resultados experimentales, también se logra hacer de manera intuitiva y fácil de seguir. Se muestran las comparaciones entre los tres métodos del 
cálculo de la similitud y se expresa que se elige el que presenta un mejor rendimiento para los futuros resultados mostrados. Luego se presentan el resto de los resultados 
experimentales que comparan el rendimiento de todos los métodos que se habían presentado según las métricas correspondientes acompañados por gráficos cuando es necesario, para 
finalmente presentar el resultado final comparando el rendimiento entre el rendimiento de el enfoque por _items_ y el enfoque por usuarios, concluyéndo así que, de acuerdo a lo
obtenido en este experimento, se logra un resultado con mayor presición y en menor tiempo, siguiendo el enfoque por _items_.

Un aspecto que podría haber mejorado en el ensayo es presentar teorías que busquen explicar los resultados experimentales. Por ejemplo, al comparar la calidad de las predicciones
entre los métodos explorados, se dice que el método que basado en regresión para realizar las predicciones presenta un mejor rendimiento en valores pequeños de x, pero este
resultado cambia al aumentar el valor de x. Esto lo intenta explicar diciendo que la regresión puede presentar sobreentrenamiento al tener una cantidad muy alta de datos. Sin
embargo, otros resultados, como por ejemplo el resultado al que se llegó variando el tamaño de las _vecindades_, mostró que el rendimiento aumenta al variar de 10 a 30 el tamaño 
de la _vecindad_, pero después de eso, la curva se aplana al seguir aumentando, por lo que decide realizar los experimentos con una vecindad de 30. Este resultado, junto con otros
es tomado y utilizado para la continuación del experimento sin presentar una teoría que explique de manera intuitiva este resultado. Creo que buscar y presentar estas teorias que
interpreten intuitivamente los datos obtenidos aporta a lograr un mejor entendimiento y apreciación de los resultados.

Finalmente, existen otros experimentos que la investigación podría haber abordado, como los métodos y costos asociados de actualizar la matriz o espacio de similitudes en el 
momento de añadir o eliminar un nuevo _item_ o de recibir un nuevo _rating_ de un usuario, etc. Sin embargo, debido a que el foco de la investigación es comparar el rendimiento
de un enfoque por _items_ con un enfoque por usuarios, creo que se logra de manera correcta el objetivo principal de la investigación.
