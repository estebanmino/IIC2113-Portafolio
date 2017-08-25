# SEMANA 3

El artefacto utilizado para esta semana es un paper ([link]), académico que explica con mucho detalle el modelo 4+1 y su relación con el método *RUP*.

### RUP - Rational Unified Process

Proviene directamente desde los diagramas *UML* y su uso efectivo para la realización de modelos. Al igual que el *Modelo 4+1*, tiene distintas fases para construirlo, estas son:

1. Inception: Elaborar especificaciones del producto final, requerimientos y funcionalidades de los casos de uso.
2. Elaboration: Análisis profundo del problema real, definiendo la arquitectura y los casos de uso del sistema.
3. Construction: Desarrollo del producto iterativamente hasta que está listo para para su distribución, mitigando riesgos.
4. Transition: Transferencia del producto al ambiente del cliente.
5. Evolution: El producto comienza nuevamente el proceso, volviendo a la fase *Inception*.

### Modelo 4+1
Como sabemos posee 4 vistas principales: *Vista lógica*, *Vista de implementación*, *Vista de procesos* y *Vista física*. Más los casos de uso.

### Diseño web con RUP en el Modelo 4+1
Busca un desarrollo rápido, pero con una planificación detallada para alcanzar una arquitectura confiable en conjunto con la búsqueda de flexibilidad y extensivilidad, en forma secuencial para las 5 vistas del *Modelo 4+1*.

1. Vista Lógica: Descripción de clases a partir de los casos de uso.
2. Vista de implementación: A partir de la vista lógica, se descompone el software en componentes.
3. Vista de procesos: Busca la integridad del sistema, incluyendo los funcionamientos no funcionales.
4. Vista física: Busca reunir lo realizado en las etapas anteriores y enfocarse en los requerimientos no funcionales.
5. Escenarios: Busca poner todo lo anterior a prueba en conjunto para diversos casos.

Como podemos ver, el *Modelo 4+1* puede ser complementado por otros modelos, algo que fue nuevo para mí al encontrar este paper. Y en este caso combina de buena forma el modelo de forma secuencial para poder ir logrando los diagramas de cada vista según los anteriores, permitiendo llegar a un mejor resultado para empezar con el desarrollo de un software.

### Aprendizajes

1. A pesar de que los modelos son independientes unos de otros, pueden ser facilmente combinables para lograr un mejor resultado.
2. El realizar las vistas del *Modelo 4+1* de manera secuencial permite un mejor resultado al final del proceso. Algo que no hicimos por ejemplo en la entrega 1 del proyecto, en donde el grupo de dividió para la realización de estas, por lo que posiblemente podríamos haber llegado a un mejor resultado.

[//]: #
[link]: http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.107.2290&rep=rep1&type=pdf
