# Crítica: Content-Based Recommendation Systems

Este paper explica un nuevo modelo de sistemas recomendadores llamado sistemas de recomendación basados en contenido. A diferencia de los modelos basados en filtrado colaborativo,
este busca realizar recomendaciones que cumplan con características que sean afín al perfil del usuario que es generado basado en input explícito o basado en sus experiencias e 
interacciones con la plataforma.

Este paper presenta los objetivos, complicaciones y manera de representar los datos, tanto de input como de output, para luego presentar diversas técnicas que se han estudiado
e implementado bajo este modelo.

Este paper sirve como introducción al concepto de sistemas recomendadores basados en contenido. Como tal, explica las distintas aplicaciones existentes de manera muy ligera, 
enfocándose en explicar principalmente el concepto detrás en lugar de proporcionar observaciones prácticas o experimentales. Como tal, algunas de las técnicas como k-vecinos más
cercanos y árboles de desición, son explicados únicamente en palabras sin proporcionar gráficos o ecuaciones matemáticas.

De esta manera, enumera una gran cantidad de enfoques que se han utilizado en este ámbito de manera que sean fáciles de entender y seguir, proporcionando ecuaciones matemáticas 
únicamente cuando son necesarias para el entendimiento del funcionamiento de un sistema y apoyándose de ejemplos de la vida real o simples de entender. No realiza ningún estudio
experimental, ni comparación objetiva entre los sistemas, sino que habla únicamente de sus ventajas y desventajas teóricas. Personalmente creo que cumple adecuadamente una función
introductoria al tema, aunque me hubiera gustado un poco más de detalles en la implementación de algunos de estos algoritmos.

A parte de esto, no aborda el problema que puede surgir con la asimetría de información que pueden presentar estos modelos, habla de la comparación entre datos estructurados y no
estructurados, pero al presentar un ejemplo teórico de distintos restaurantes, no menciona que existe la posibilidad de que exista una variable que un restaurante en específico
no proporcione una respuesta clara o que no sea trivial calificar, pudiéndose generar así datos faltantes en la base de datos.
