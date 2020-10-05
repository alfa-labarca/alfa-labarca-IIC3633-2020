# Crítica: A User-Centric Evaluation Framework of Recommender Systems

Este paper presenta un modelo de evaluación de sistemas recomendadores basado en la experiencia percibida de los usuarios. Para esto propone un modelo llamado _ResQue_, el cual
consiste de 13 _constructs_ y 60 items de preguntas.

Creo que el approach de una evaluación basada en la experiencia de cada usuario es un factor muy importante a considerar en lugar de enfocarse únicamente en la presición del 
sistema u otras medidas objetivas. Es muy usual en muchas áreas que ocurra que un modelo, a pesar de ser sólido en la teoría, no logre adaptarse bien en la interacción con los 
usuarios, y no logré así alcanzar su objetivo principal.

El modelo propuesto en este paper, busca abordar esta interrogante desde muchas áreas distintas, como la calidad percibida de las recomendaciones, la facilidad de uso percibida, 
etc. cada una de las cuales también cuenta con sus propios sub-ítems los que son detallados en el paper.

Si bien creo que el análisis de esto es muy importante para el área, el método puede tener sus problemas. El primer problema es el tamaño del modelo. Un cuestionario de 60 preguntas
puede generar que una pequeña cantidad de usuarios estén dispuestos a contestarlo, limitando y sesgando así la cantidad de datos que pueden ser obtenidos a partir de este. Además de
esto, puede ocurrir que una evaluación objetiva de un usuario puede no corresponder a una mejora en su satisfacción real. Por ejemplo, al ser preguntado, un usuario puede creer que
preferirá un tipo de presentación, sin embargo, en la práctica, esta presentación puede terminar abrumando al usuario. Es decir, puede ocurrir que lo que los usuarios piensan preferir
al ser interrogados sobre esto, puede no adecuarse a sus preferencias reales en la práctica. Es por esto que creo que este modelo necesita ser validado por un análisis experimental que
determine si los cambios propuestos por el modelo realmente se traducen a un incremento en las interacciones de los usuarios con los ítems recomendados o a una mejor experiencia
general de los usuarios.

De esta manera, creo que este paper presenta un approach a un área vital para los sistemas recomendadores, pero que requiere de una validación prácitca para determinar su viabilidad
real.
