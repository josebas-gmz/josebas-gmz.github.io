El objetivo de los sistemas de recomendación es ayudar al usuario con la sobrecarga de información. Permite aumentar el KPI de la empresa o sistema teniendo un mejor *engagement* del usuario, teniendo un impacto directo en las ventas, *click rate* y precio promedio de la compra. El problema de recomendación consiste en seleccionar un conjunto de ítems para un usuario que maximicen una función de utilidad. Su funcionamiento se centra en la interacción de usuario con la interfaz, alimentando una base de datos que, en conjunto con un motor de recomendación, entrega recomendaciones al usuario.

# Filtrado colaborativo basado en usuarios/ítems

Su objetivo es buscar usuarios similares y recomendar usando una suma ponderada con una métrica de similitud. Si bien el filtrado colaborativo tiene una mayor exactitud con más vecinos, esto tiene un costo computacional mayor. Adicionalmente, este modelo de recomendación requiere de interacciones, si un usuario o película no cuenta con un historial previo no es posible realizar recomendaciones. Esto es conocido como cold start.

# Factorización

Las técnicas de factorización matricial buscan descomponer la matriz de ratings en una multiplicación de matrices de menor dimensión que capturan la información de usuarios e items.Recordemos que contamos con sistemas de recomendación no personalizados como most popular, random o Wilson score, semi-personalizados basados en reglas generales o segmentaciones y personalizados que consideran los intereses personales tales como el filtrado colaborativo, factores latentes, recomendaciones basadas en contenidos y ensambles o híbridos. 

# Recomendación basada en contenido

Busca recomendar contenido con características similares (género, actores, directores, país, lenguaje, año, extensión, entre otros) a las de los items que le han gustado al usuario. Cada ítem puede ser representado por un vector de características que permita determinar su parecido basado en una métrica de similitud. Esto soluciona el parte el problema del *cold-start* ya que se puede generar una representación de un ítem con facilidad en base a sus metadatos, pero tiene deficiencias para recomendar contenido diverso sesgando la capacidad del usuario de explorar cosas nuevas.

Existen tres tipos de sistemas de recomendación híbridos:

1. Monolítico que ejecuta uno a uno varios sistemas de recomendación filtrando la información de acuerdo con un esquema predeterminado.
2. Mix de sistemas de recomendación que ejecuta varios sistemas entregando todas las puntuaciones normalizadas ordenadas de mayor a menor.
3. Ensamble que combina los resultados de múltiples algoritmos de recomendación en una sola recomendación.

El contexto puede ser totalmente, parcialmente o no observable y puede describir un estado estático o dinámico. El contexto puede ser utilizado para hacer predicciones basadas en data filtrada por el contexto, o contextualizar las recomendaciones que genera un sistema en base a toda los datos. También, puede utilizarse el contexto como parte de un modelo de recomendación.

## Máquinas de factorización

Los modelos de factorización permiten estimar interacciones entre dos (o más) variables incluso si la interacción no es observada explícitamente. Existe múltiples extensiones de los métodos de factorización matricial que buscan incorporar información especifica de cada problema (SVD++, Time SVD, Fact-KNN, Time TF, Factorizing Markov Chain, Factorizing Personalized Markov Chain).

Dado que cada tarea de recomendación requiere un re-diseño del modelo de optimización y una re-implementación del algoritmo encargado de hacer las inferencias. Por lo tanto, buscamos un modelo que nos permita realizar una factorización matricial con múltiples variables iniciando desde la regresión lineal.

http://projector.tensorflow.org/
