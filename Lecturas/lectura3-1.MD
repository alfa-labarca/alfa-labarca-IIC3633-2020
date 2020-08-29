# Crítica: Performance of Recommender Algorithms on Top-N Recommendation Tasks

Este trabajo se enfoca en cuestionar la métrica usual de RMSE como métrica estándar para la evaluación de sistemas recomendadores top-N utilizada habitualmente en la mayoría de los
modelos propuestos, proponiendo una nueva métrica nueva y un nuevo modelo de recomendaciones ajustado a esta métrica.

Habitualmente, en la mayoría de los papers que hemos leído en este curso, se usa el RMSE (Root Mean Standard Error) para evaluar la eficacia de un método de recomendación y así
comparar el desempeño entre distintos modelos. Esta métrica funciona obteniendo el promedio del error entre la calificación predicha por el modelo y la calificación real asignada
por el usuario. El funcionamiento de la mayoría de estos algoritmos es tomar entonces los ítems con una mayor calificación predicha y estos recomendárselos al usuario. De esta 
manera parece lógico evaluar los modelos bajo esta métrica, ya que bajo un menor error entre la predicción y la realidad, se esperaría una mayor precisión en recomendar ítems que
realmente se ajusten a los gustos del usuario. Sin embargo, la mayoría de los sitios que utilizan estos sistemas recomendadores, no le muestran la calificación predicha al usuario,
o incluso si lo hacen, lo que realmentebuscan es poder recomendarle al usuario ítems que son de su interés, por lo que es más importante determinar si las películas que son 
recomendadas al usuario le gustarán a este en lugar de minimizar el error entre la predicción y la calificación real entregada por el usuario. Para esto, propone una nueva métrica
que busca medir justamente esto y, bajo esta métrica, compara los modelos que se usan como el estado del arte, junto con modelos que han sido desechados como los modelos 
no-personalizados y además presenta su propio modelo ajustándose a la nueva métrica.

El modelo propuesto se basa en la descomposición SVD de la matriz de calificaciones de los usuarios, así como lo hacen muchos de los principales métodos utilizados como FunkSVD, 
sin embargo, la diferencia yace cómo maneja el modelo los datos faltantes. Uno de los principales problemas con los que se encontraban los métodos que utilizan SVD es que si se 
rellenan los datos faltantes con valores arbitrarios como 0, las predicciones se ven influenciadas por estos valores, aumentando el error de estas, por lo que deben recurrir a
métodos como la reducción de dimensionalidad para tratar con este problema. Ya que para la investigación del paper, el error de las predicciones no es el objetivo final, este no
es un problema para el modelo, por lo que el método propuesto, PureSVD, rellena los valores faltantes con 0s, lo que le permite acceder a muchas técnicas matemáticas modeladas 
para el manejo de matrices _sparse_.

Ya que el paper busca comparar muchos métodos distintos bajo su nueva métrica, explica el funcionamiento de todos estos métodos. Esto lo realiza de manera muy detallada para mi
gusto, quizás porque ya conozco estos métodos, sin embargo, como el objetivo final de este paper no es presentar estos métodos, sino presentar la nueva métrica y el nuevo modelo,
me hubiera gustado que estas explicaciones las hubiera hecho de manera más resumida, concentrándose más en su propio modelo y en los resultados.

El mayor problema que tuve con el paper es en la definición de la métrica. Creo que es importante el cuestionamiento que realiza, midiendo los métodos directamente bajo la medida 
que es realmente relevante para las aplicaciones que hacen uso de los sistemas recomendadores, en lugar de medirlos bajo una métrica que no es de principal interés para los sitios
ni los usuarios, asumiendo que existe una correlación trivial entre estas métricas, sin embargo, creo que la manera en que define la métrica asume condiciones que bajo mi opinión
pueden generar errores en los resultados finales. La manera en que se define la métrica es en tomar un elemento de testeo al que el usuario calificó con la nota máxima 
(5 estrellas) en este caso, y luego tomar otros 1000 elementos aleatorios y pedirle al módelo que recomiende N ítems de este set de 1001 ítems. Si el elemento que se sabe que 
es calificado con 5 estrellas se encuentra entre los elementos recomendados, entonces se considera que la recomendación fue exitosa. El problema es que este método asume que 
el ítem elegido es una mejor recomendación que los otros 1000 elementos, lo cual es una generalización que en mi opinión puede generar errores. Por ejemplo, si un usuario
califica con 5 estrellas a un 30% de las películas que vé, al tomar 1000 elementos de manera aleatoria, se esperaría que el usuario califique con 5 estrellas a 300 elementos,
luego, si N=20 (lo cual es un valor incluso grande para el estándar de recomendaciones dadas por un sitio habitual), entonces, para que la métrica mida realmente si las 
recomendaciones correctas, seria necesario que el ítem elegido inicialmente se ubique entre los 20 ítems que mejor se ajusten a los gustos del usuario, es decir, necesita ser
una mejor recomendación que otras 280 ítems que el usuario calificó de la misma manera, y no existe nada que nos asegure eso. De esta manera, creo que el método necesita mejoras
como ajustar el valor de N según los hábitos de calificación de cada usuario o en lugar de elegir 1000 ítems de manera aleatoria, elegir estos 1000 ítems asegurándose que 
ninguno haya sido calificado con 5 estrellas por el usuario, así asegurándose que el ítem observado sea realmente una de las N mejores recomendaciones posibles.
