### Tema 1

1) ¿Qué es la **Programación Orientada a Objetos**? Explíquelo con sus palabras, y contrástelo con la programación estructurada.

  > La POO es un paradigma de programación, la cual pone el foco en el diseño de objetos (los cuales representan una parte de un problema real), que saben hacer cosas y comunicarse con otros objetos, pudiendo así resolver un problema.  
  > Por el contrario, la programación estructurada se basa en seguir una serie de sentencias o instrucciones que se ejecutan según el estado del problema.

2) ¿Qué es una **clase**? Proporcione al menos tres ejemplos.

  > Una `clase` es una forma de clasificar cosas, entidades, conceptos a partir de sus propiedades `atributos` y sus capacidades de hacer cosas `metodos`.

  > TODO: ejemplos

3) ¿Qué son los principios **SOLID**? Explíquelos en general, especifique el sentido que tienen en la programación orientada a objetos y enumérelos en particular.

  > Los principios SOLID son técnicas o buenas prácticas de desarrollo de software, mediante las cuales el código se hace más mantenible y escalable.

4) ¿Qué es un **HashMap**? ¿Para qué lo utilizaría? Proporcione un ejemplo.

  > Un HashMap es una clase de la interface Map, y nos permite guardar datos del tipo clave->valor en una estructura. La particularidad del HashMap es que no permite claves duplicadas ni valores nulos, y no tiene un orden lógico.  
  > Se podría implementar para guardar un listado de productos cuya clave sea un código unívoco y el valor su descripción, y asegurarse que no se cargen distintos productos con un mismo código.

  > TODO: ejemplo

5) ¿Qué elementos no deben faltar para armar un test válido con **JUnit**? Describa un caso de uso y ejemplifique utilizando los elementos mencionados anteriormente.

### Tema 2

1) ¿Cuál es la diferencia entre **clase** y **objeto**? Explíquelo sin utilizar definiciones circulares.

  > Una clase es un concepto que modela una entidad, define cuales son sus propiedades y comportamientos. Un objeto en cambio, es una instancia de una clase (existente en tiempo de ejecución del programa), que cumple con todo lo definido en ella.

2) Defina el concepto de **herencia**. Proporcione un ejemplo y un contraejemplo.

  > La herencia es un mecanismo por medio del cual podemos generar relaciones jerárquicas entre nuestras clases, ayudando a modelar nuestro problema. Esa relación está representada por la frase "__es un_".  


  ###### _Ejemplo de Herencia_

    Superclase -> Asciento  
    Subclase -> Silla  
    Silla "es un" Asciento

```java  
  public class Asciento {

    private String superficieApoyo;

     public void sentarse() {
       // Implementacion genérica de Sentarse
     }

  }

  public class Silla extends Asciento {

      private String respaldo;
      private Iteger cantidadPatas;

  }
```

  ######_Ejemplo de Herencia mal implementada_

    Superclase -> Asciento  
    Subclase -> Caballo  
    ¿Caballo "es un" Asciento?

```java
  public class Asciento {

    private String superficieApoyo;

     public void sentarse() {
       // Implementacion genérica de Sentarse
     }

  }

  public class Caballo extends Asciento {

      private Iteger cantidadPatas;

  }
```


3) ¿Qué es **git**? ¿Cuáles son sus características principales?

  > Git es un sistema de control de versiones, que permite trabajar a varias personas en un mismo proyecto.
  Sus principales caracteristicas son:
  * `branch` - Trabajar con copias del proyecto original.
  * `history` - Tener el registro de todas las versiones del proyecto.
  * `free and open source` - Es libre y gratuito, y permite la retroalimentación.

4) ¿Qué es el **Java Collection Framework**? ¿Cuáles son las principales colecciones que conoce? Proporcione un ejemplo de código del uso de cada una.

 > JCF, es un conjunto de clases e interfaces que permiten manejar colecciones de objetos. Algunas de estas colecciones son:
   * List
   * Set
   * Queue
   * Deqe
   * Map

  > TODO: ejemplos

5) ¿Qué son las **Runtime Exception**? ¿En qué casos las utilizaría? Proporcione un ejemplo que esté incluido en la API de Java.
