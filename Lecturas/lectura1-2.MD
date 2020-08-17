# Crítica: _Netflix Update: Try This at Home_

El texto en cuestión pertenece a una entrada de un blog de **Simon Funk**, en la cual explica el algoritmo que usó para obtener el tercer lugar en el _Netflix Price_.
Dentro de este blog, explica el problema que busca solucionar, junto con los desafios que este presenta, para luego ir ahondando paulatinamente en el método y algoritmo que 
utiliza para lograr llegar a la solución que presentó. La intención del texto es servir de guía para que otros desarrolladores puedan guiarse por el trabajo que plantea y 
desarrollar soluciones para este mismo problema u otros problemas similares. Tal como dice el texto "Después de leer este texto tú también deberías ser capaz de llegar al top 10
(del desafío _Netflix Price_)".

Debido al medio que usa este texto, este no sigue una estructura ni lenguajes formales. En lugar de esto el texto contiene chistes y lenguaje en primera y segunda persona. En un
comienzo, el texto aborda los contenidos de manera que es fácil de seguir sin necesidad de tener un amplio conocimiento de los temas tratados, al explicar el desafío en cuestión y
los problemas que este tiene, lo hace de manera clara y fácil de entender, y una vez que se adentra en las técnicas específicas de su implementación, comienza a utilizar conceptos
más avanzados sin proveer una extensa explicación de como funcionan ni como sirven.

El principal problema captado en la forma del texto, es que no no es consistente con su público objetivo. Como se dijo inicialmente, el objetivo del texto pareciera ser que otros
programadores con conocimientos previos del tema puedan entender y replicar su trabajo. De esta manera, el texto introduce conceptos como la Regularización de Tikhonov y el 
sobreentrenamiento y funciones sigmoideales sin explicar su significado ni aplicación, ya que asume que el lector está familiarizado con estos temas. Sin embargo, esto es 
contradictorio con la manera en que explica de manera muy simple y general otros temas como la _sparsity_ de los datos entregados, los cuales son explicados como si el lector
no estuviera familiarizado con este tipo de trabajo. Esto genera que al leerlo, cambie muy abruptamente la complejidad de los temas y conceptos que son discutidos.

Por otra parte, analizando el algoritmo propuesto, tal como lo menciona, es un trabajo conceptualmente simple y directo, el cual se va complicando en la implementación más fina,
pero que es fácil entender las ideas principales que intenta abordar con su proyecto. Me hubiera gustado que se especificara y se profundizara en el análisis de las fechas de las
clasificaciones proporcionadas por Netflix, de las cuales se menciona que se intentó realizar algunos procedimientos, sin obtener ningún resultado significativo con ellos, sin 
especificar cuales fueron estos experimentos. Se menciona que las fechas pueden tener una implicancia, ya que un usuario puede haberle dado una nota distinta a una misma película
en dos ocasiones distintas, sin embargo, yo creo que sería más relevante usar las fechas de la clasificación para considerar posibles cambios en los gustos de los usuarios, quizás
con una suma ponderada, en la cual, una clasificación realizada en el último mes, tenga mayor peso que una clasificación realizada hace tres años. debido a que los gustos de una
persona pueden haber cambiado, así como la exigencia con la que una persona ponga una clasificación (alguien puede exigirle más a una película para que esta reciba 5 estrellas de 
lo que le exigia hace años).
