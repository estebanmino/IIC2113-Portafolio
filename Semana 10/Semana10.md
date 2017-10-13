# SEMANA 10

El artefacto usado para esta semana es una discusión en *StackOverflow* ([link]), sobre las diferencias entre una librería y un framework, algo que en lo personal tengo una intuición de las definiciones, pero me gustaría poder llegar a una definición más completa y correcta a través de la realización de este portafolio.

Para poder lograr este pbjetivo, primero necesitamos la definición de *Inversion of Control*.

### Inversion of Control

- Se refiere al control del flujo que el software o sistema tiene, que puede ser controlado por el mismo sistema o debe ser implementado por el desarrollador al momento de construir el sistema.

Este término es el punto clave para entender cuando estamos en presencia de un framework o una librería.

### Frameworks

- Como se había mencionado, una característica importante de un framework es que los métodos definidos por el usuario son generalmente llamados desde el framework en sí mismo y no desde el código del usuario. Por esto el frameworrk es el encargado de realizar la coordinación de las actividades en la aplicación.

### Librerías
- Es una colección de código que se refiere a una tarea en específico, que puede ser usada para cualquier propósito en donde está pueda ser usada. Es consumida por el usuario simplemente haciendo uso de este código a través de llamados a la librería. Es por esto que el control de las actividades del sistema se debe implementar explícitamente a diferencia de un framework.

Como podemos ver, la definición de *Inversion of Control* nos permite detectar rápidamente cuando estamos en presencia de una librería o de un framework.

### Aprendizajes

1. *Inversion of Control* se refiere a el control del estado o secuencia de actividades del programa, que puede ser tarea de los desarrolladores o no implementarlo.
2. La principal diferencia entre framework y librería es el grado de control que estos tienen en el programa, a diferencia de las librerías, el framework es el encargado de manejar el control de estado del programa sin la necesidad de que el desarrollador tenga que preocuparse por esto.

[//]: #
[link]: https://stackoverflow.com/questions/3057526/framework-vs-toolkit-vs-library