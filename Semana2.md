# SEMANA 2

El artefacto utilizado para esta semana corresponde a una discusión proveniente de *StackOverflow* ([ver discusión]). En esta se discute profundamente los conceptos de abstracción y encapsulamiento en ingeniería de software, tratados también durante la última clase del curso.

Antes de leer la discusión mencionada, según lo que entendí durante la última clase, entendía por estos dos conceptos lo siguiente:

- Abstracción: Generalización de un objeto, para poder ser representado de manera simple al exterior sin mayor detalle de este, ni de como funciona.
- Encapsulamiento: Esconder el funcionamiento de un objeto para solo mostrar para utilizar sus funcionalidades, sin la necesidad de saber como lo hace.

Estas son las definiciones que tenía en mente, bastante amplias por lo demás, que me motivaron a revisar esta discusión.

### Abstracción

Para el concepto de abstracción me llamó mucho la atención una respuesta ([ir a respuesta sobre abstración]), en donde se realiza un la comparación entre el concepto y un artista.

En esta se menciona que el artista abstracto se dedica a pintar formas desde el punto de vista general de la obra. Lo que es comparable con herencia entre objetos, en donde las clases padre son las clases más abstractas, más generales, y a medida que se desciende se encuentran los objetos con una implementación más detallada. Un ejemplo de esto es el siguiente código:

```
public class Employee {
   public string Name { get; set; }
   public double Salary { get; set; }
}

public class SalesRepresentative : Employee {
    public double AnnualSalesAmount { get; set; }
    public void IncreaseSalary(double rate) {
        if (this.AnnualSalesAmount > 100000) {
            this.Salary += (this.Salary * (rate + 5) / 100);
        }
        else {
            this.Salary += (this.Salary * rate / 100);
        }
    }
}
```
Se puede ver que la clase *Employee* es el concepto más general para todos los empleados en este ejemplo, mientras que *SalesRepresentative* posee un mayor detalle de sus funcionalidades particulares.

### Encapsulamiento

Para este concepto tomó mi atención la definición ([ir a respuesta sobre encapsulamiento]), en donde se define como un concepto que forma parte también de abstracción. En donde se esconde el estado de los objetos encapsulados, y los usuarios solo interactuan con estos a través de métodos. Un ejemplo de esto se puede ver en el siguiente código:

```
public class Employee {
    private String name;
    public String setName(String name) {
        name = name;
    }
    public String getName() {
        return name;
    }
}
```

Como se puede ver corresponde también al ejemplo de abstracción mostrado anteriormente. De esta forma, partiendo desde encapsulamiento se puede lograr abstracción.

### Aprendizajes

1. A pesar de que estos conceptos son individualmente diferentes, encapsulamiento es en parte perteneciente al concepto de abstracción.
2. Estos conceptos se pueden relacionar con un computador. Mientras el computador en su totalidad es el objeto abstracto del que hacemos uso, y sus componentes como pantalla o mouse, son objetos encapsulados de este computador con los cuales solo interactuamos sin conocer su funcionamiento interno.
3. Luego de realizar este portafolio, tengo nuevas definiciones generales sobre estos conceptos:
    - Abstracción: Describir un concepto de forma simple para hacer uso de este a un alto nivel, sin hacer uso de funciones específicas según casos particulares.
    - Encapsulamiento: Estrategia parte de la abstracción en donde se esconde el estado real de un objeto del usuario y solo hay una interacción con este mediante métodos.




[//]: #
[ver discusión]: https://stackoverflow.com/questions/8960918/encapsulation-vs-abstraction
[ir a respuesta sobre abstración]:
https://stackoverflow.com/a/8961062/8481050
[ir a respuesta sobre encapsulamiento]:
https://stackoverflow.com/a/8960961/8481050
