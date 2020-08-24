# Crítica: Collaborative Filtering for Implicit Feedback Datasets

El paper se enfoca en explicar en cómo funciona un sistema recmoendador de Filtrado Colaborativo basado en una plataforma que recibe feedback implícito. A diferencia de los 
que se detallaban en lecturas anteriores, los cuales funcionaban en base a feedback explícito como reseñas y calificaciones de los productos que eran consumidos, un modelo que
usa feedback implícito no recibe feedback de manera directa de los usuarios, en cambio, debe inferirlo en base a su comportamiento. El ensayo plantea un modelo de feedback
implícito y luego es testeado con una base de datos de consumo de programas de televisión, recibiendo la información de la sintonía de cada usuario, para así realizar una 
recomendación en base a esta.

Como se explica en el paper, un análisis de un feedback implícito llega a ser muy distinto a un modelo con feedback explícito, ya que se deben tener en cuenta muchas
consideraciones en el momento de realizar la transición. Por ejemplo, en el feedback explícito, una película sin clasificación en el usuario, se considera como información
faltante, por lo que no se considera en el momento de formar el perfil del usuario, sin embargo, con feedback explícito no se puede considerar de esta manera, ya que si un 
usuario no ve un programa, esto puede significar que este no está interesado (así como muchos otros factores). Asímismo, incluso si un usuario, si registra el programa, esto
puede deberse a otros factores que no implican realmente un interés por parte del usuario en el programa. Así, el ensayo plantea un modelo que entrega como respuesta no una 
predicción, sinó que una tupla de valoración estimada, junto con un valor de confianza de esta estimación.

El paper sigue un formato de ensayo clásico y bien logrado. Explica de manera fácil de seguir y entender, todo el procedimiento y la formación del modelo, y lo que es más
importante, al explicar la formación del modelo lo realiza en un formato en que, primero presenta un problema que surge a partir de el feedback implícito, luego explica de 
manera intuitiva una posible solución, y luego explica como esta puede ser aplicada al modelo de manera efectiva. Los resultados en base a la sintonía de televisión son acompañados
por gráficos cuando corresponde que hacen el análisis facil de seguir y usa un nivel de tecnisismo adecuado, sin que esto genere que el lenguaje haga que la investigación sea
dificil de seguir.

Un problema que surge, que en mi opinión es un problema inerente del feedback implícito, es que estos modelos pueden ser dificiles de generalizar entre distintos servicios que 
requieren un modelo similar. Por ejemplo, al final menciona el problema de que una tupla usuario item evaluada en cero, lo cual significa que el usuario no vio un programa, puede
deberse a que este no está interesado, debido a que se transmite en un horario muy irregular o debido a que al mismo tiempo, existe otro programa que el usuario sigue, por lo que 
plantea como trabajo futuro el implementar una variable dinámica que considere el tiempo en el que se transmitió el programa. Aunque esta solución llegara a funcionar, generando
predicciones más certeras, esta solución no se aplicaría por ejemplo a un sitio de ventas online, del cual surgirían otros problemas distintos, para los cuales habría que buscar 
otras soluciones. Aunque el modelo principal que se plantea en el paper es un modelo generalizado que intenta servir para cualquier tipo de algoritmo que necesite realizar 
recomendaciones con filtros implícitos, las implementaciones adicionales que generan que aumente la precisión terminan siendo específicas para el problema específico con el que se
está tratando, por lo que si un algoritmo funciona muy bien para un problema, no necesariamente este mismo algoritmo podrá ser implementado en otro contexto, o se asegurará que en
este nuevo contexto también funcione de manera deseable. Desafortunadamente, el algoritmo del ensayo solo es testeado bajo un contexto específico, por lo que resta analizar si este
sistema funcionará en otros contextos también.
