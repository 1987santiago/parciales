### Tema 1

1) ¿Para qué se utilizan los *branch* en **git**?

  * Los `branch` o "_ramas_" se utilizan para generar copias a partir del proyecto "_padre_", pudiendo realizar cambios en ellos sin afectar el original.

2) Enumere y describa al menos cuatro conceptos relacionados a la *programación orientada a objetos*. Relaciónelos en una sola frase.

  > **Clase**  
  Las clases nos permiten representar entidades o conceptos, estableciendo  propiedades `atributos` y comportamientos `metodos` comunes.

  > **Objeto**  
  Los objetos son instancias de una clase, materializan el concepto modelado por la clase y poseen todos los atributos y metodos definidos en la clase.

  > **Encapsulamiento**  
  El encapsulamiento es una acción que nos permite modularizar nuestro código y definir responsabilidades, a través del aislamiento de atributos y metodos que modelan algo. Gracias a esto, el código se vuelve mas especializado, abstracto, completo y sustentable.

  > **Herencia**  
  La herencia nos permite establecer relaciones jerárquicas.

  > **Polimorfismo**  
  El polimorfismo (*de tipos*) es la capacidad que tiene el lenguaje o programa, de evaluar multiples tipos de datos en tiempo de ejecución.

3) ¿Existe la **herencia múltiple en Java**? En caso de contestar afirmativamente, proporcione ejemplos de uso. En caso contrario, explicar por qué y cómo se subsana dicha carencia.

  * En Java no existe la herencia múltiple para evitar el acoplamiento excesivo de clases. Sin embargo, se puede simular este comportamiento mediante la utilización de interfaces o composiciones.


4) Defina y explique en un párrafo el **Single Responsibility Principle**.

  * El principio de responsabilidad simple, indica que toda clase debe tener una única responsabilidad, de no ser así, ésta sera más vulnerable a cambios y acoplamientos (_de responsabilidades_)

5) ¿Qué es el **Java Collection Framework**? ¿Cuáles son las principales colecciones que conoce? Proporcione un ejemplo de código del uso de cada una.

 * JCF, es un conjunto de clases e interfaces que permiten manejar colecciones de objetos. Algunas de estas colecciones son:
   * List
   * Set
   * Queue
   * Deqe
   * Map

  > TODO: ejemplos

### Tema 2

1) ¿Para qué sirven las **clases abstractas**? ¿Qué uso le daría?

  * Las clases abstractas sirven para formar jerarquías, tienen fines meramente taxonométricos ya que nos permiten modelar soluciones de una manera conceptual. Estas clases se pueden usar para definir una "_plantilla_" en la generación de otras clases que la heredan.

2) Defina y proporcione un ejemplo original del **Open/Closed Principle**. Utilice sus propias palabras.

 * El principio Open/Closed indica que todo código debe permitir ser extendido, pero no modificado, es decir, que si necesitamos implementar una nueva funcionalidad en nuestro programa, deberíamos poder solucionarlo agregando funcionalidad al código existente y no modificandolo.
 > TODO: ejemplo

3) ¿Qué es el **encapsulamiento**? Proporcione un ejemplo que demuestre el concepto.

 * El encapsulamiento es una técnica con la cual se agrupa una serie de elementos que nos ayuda a generar entidades. Además su uso nos facilita especializar nuestro código para que cumpla con un sólo requerimiento y hacerlo del modo más completo posible.
 > TODO: ejemplo

4) Explique el significado y uso de la frase *"Tell, don't ask"*. Proporcione un ejemplo original del mismo.

 * La frase "*Decir, no hacer*" hace referencia al ocultamiento de la información e implementación de un programa y su encapsulamiento. En la POO se instruye a los objetos para que hagan cosas abstrayendonos de como es que las saben hacer. No es conveniente ni lógico, preguntarle a un objeto sobre su estado, ya que vilaríamos el principio de encapsulamiento.
 > TODO: ejemplo

5) ¿Qué es un **HashMap**? ¿Para qué lo utilizaría? Proporcione un ejemplo.

  * Un HashMap es una clase de la interface Map, y nos permite guardar datos del tipo clave->valor en una estructura. La particularidad del HashMap es que no permite claves duplicadas ni valores nulos, y no tiene un orden lógico.
  Se podría implementar para guardar un listado de productos cuya clave sea un código unívoco y el valor su descripción, y asegurarse que no se cargen distintos productos con un mismo código.
  > TODO: ejemplo
