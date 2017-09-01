# SEMANA 4

El artefacto utilizado para esta semana es un artículo que habla de los principios *SOLID*, y de como llegar a este desde los principios *STUPID* ([link]).

El análisis de este artefacto se realizó leyendo y comprendiendo los conceptos involucrados en ambos "principios", que se analizará en menor detalle al artículo a continuación.

### STUPID

- **Singleton**: 
Cuando pensamos que que *singleton* es el mejor patrón para aplicar en un caso, probablemente nos equivocamos.
- **Tight coupling**: 
Se debe reducir siempre el acomplamiento existente entre modulos de un programa.
- **Untestability**: 
El testeo no puede ser difícil, hecho que es causado generalmente por acoplamiento.
- **Premature optimization**:
Hacer optimizaciones de manera temprana es considerado un anti patrón,  muchas veces causan un código más difícil de entender de lo necesario, sin un beneficio considerable.
- **Indescriptive naming**:
Nombrar clases, métodos, atributos y variables de una manera comprensible.
- **Duplication**:
"Don't repeat yourself"

Me llamaron mucho la atención estos "principios", creo que agrupa los conceptos principales de lo que hemos escuchado constantemente en clases y en todos los lugares en donde hayamos encontrado algo en relación a la programación, en una forma reducida y memorizable.

###  SOLID

- **Single Responsability Principle**:
Todas las clases deben tener solo una responsabilidad, nunca debe haber más de una razón para cambiar la clase.
- **Open/Closed principle**:
Todas las entidades deben estar abiertas a extensión, pero cerradas a modificaciones. Es decir, se debe extender el comportamiento de la entidad, pero sin modificar su código fuente.
- **Liskov substitution principle**:
Cada clase que hereda de otra puede usarse como su padre sin la necesidad de conocer las diferencias entre ellas.
- **Interface segregation principle**:
Los clientes no debieran tener la implementación de métodos que no va a usar. Esto además entrega bajo acoplamiento y alta cohesión.
- **Dependency inversion principle**:
La idea principal es que al diseñar la interacción al diseñar las interacciones entre módulos de alto y bajo nivel, se debe pensar como una interacción abstracta. Sus dos puntos principales son,
    1. Módulos de alto nivel no deben depender de módulos de bajo nivel, pero ambos dependen de abstracciones.
    2. Abstracciones no deben depender de detalles. Detalles deben depender de abstración.

Personalmente entendí mucho más de los principios *SOLID* de la manera en que se explican en este artículo. Se puede ver que estos principios buscan fuertemente la modularización del código y la independencia de los módulos de este.

### Aprendizajes

1. *SOLID* son principios que nos dicen principalmente la importancia de que el código de cualquier programa debe ser modular, con bajo acoplamiento y alta cohesión.
2. Podemos ver en los "principios" *STUPID* muchas cosas que realizamos muchas veces programando en algun momento y que probablemente, seguimos siguiendo alguno de estos. Por lo que tener estos en cuenta, es una buena forma de reconocer cuando estamos haciendo algo mal.
3. El principio I de *SOLID*, *Interface segregation principle*, es algo que no conocía pero que se ve obvio cuando uno lo lee, es algo que tenía una noción por lo que llevarlo a un nombre en específico me va hacer tenerlo en cuenta a futuro.

[//]: #
[link]: http://williamdurand.fr/2013/07/30/from-stupid-to-solid-code/