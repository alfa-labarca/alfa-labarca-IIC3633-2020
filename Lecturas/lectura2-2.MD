# Crítica: BPR: Bayesian Personalized Ranking from Implicit Feedback

El paper en cuestión propone un nuevo criterio de optimización para modelos de recmoendación personalizados con feedback implícito. A diferencia de los papers anteriores, este
no presenta un modelo de recomendación, sino un criterio de optimización y algoritmo de aprendizaje genérico, el cual puede ser implementado en modelos existentes para mejorar su
rendimiento. Este criterio es implementado en los modelos de Factorización de Matriz y kNN adaptativo, comparando sus resultados con estos mismo métodos implementando distintos
criterios de optimización, concluyendo que el método propuesto presenta un mejor rendimiento que la competencia.

El optimizador propuesto es BPR-Opt, el cual es derivado a partir de un análsis bayesiano de los datos, implementado a la tarea de generar un ranking de recomendación para feedback
implícito. El paper está estructurado de manera en que, luego de introducir los términos relevantes y las soluciones actuales, primero presenta un análisis de las caracteristicas
del problema que intenta solucionar, para luego presentar la solución matemática del optimizador propuesto, para solucionar este problema y finalmente presentar un algoritmo de 
aprendizaje genérico que usa este optimizador, el cual puede ser implementado en modelos existentes de recomendación. Esta estructuración ayuda para comprender el análisis intuitivo
y teórico que llevó a la solución planteada antes de proceder a la implementación directamente. Este tipo de entendimiento detrás de la lógica de una solución es especialmente 
relevante al tratar con problemas con feedback implícito, los cuales suelen requerir un entendimiento más profundo de la característica de los datos con los que se está tratando
y suele ser más dificil su comprención desde un punto de vista matemático y práctico.

Sin embargo, el paper se extiende mucho y termina usando términos y lenguaje muy avanzado, lo que dificulta su comprensión y seguimiento. Esto se acentúa en los últimos párrafos 
del ensayo, enn los cuales, luego de haber presentado una gran cantidad de modelos, algoritmos, criterios y metodologia, hace referencia a estos, usando solamente sus iniciales,
por lo que la conclusión y análisis de datos está plagada por una gran cantidad de iniciales de distintos procedimientos, lo que dificulta en gran medida su seguimiento si no 
se tiene experiencia en los temas que está tratando. Esto puede deberse a que el objetivo es plantear un criterio de optimización el cual debe ser aplicado a métodos existentes,
por lo que su público objetivo serían programadores que ya poseen métodos recomendadores a los cuales se les puede agregar este criterio de optimización, por lo que asume que sus
lectores se manejan de manera apropiada en el tema.
