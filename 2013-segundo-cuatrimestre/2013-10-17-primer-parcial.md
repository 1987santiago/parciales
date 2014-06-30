### Tema 1

1) ¿Existe la **herencia múltiple** en Java? En caso de contestar afirmativamente, proporcione ejemplos de uso. En caso contrario, explicar por qué y cómo se subsana dicha carencia.

  > En Java no existe la herencia múltiple para evitar el acoplamiento excesivo de clases. Sin embargo, se puede simular este comportamiento mediante la utilización de interfaces o composiciones.

2) ¿Qué es el **encapsulamiento**? Proporcione un ejemplo que demuestre el concepto.

 > El encapsulamiento es una técnica con la cual se agrupa una serie de elementos que nos ayuda a generar entidades. Además su uso nos facilita especializar nuestro código para que cumpla con un sólo requerimiento y hacerlo del modo más completo posible.

 > TODO: ejemplo

3) ¿Qué son las **Runtime Exception**? ¿En qué casos las utilizaría? Proporcione un ejemplo que esté incluido en la API de Java.

4) Defina y proporcione un ejemplo original del **Open/Closed Principle**. Utilice sus propias palabras.

  > El principio Open/Closed indica que todo código debe permitir ser extendido, pero no modificado, es decir, que si necesitamos implementar una nueva funcionalidad en nuestro programa, deberíamos poder solucionarlo agregando funcionalidad al código existente y no modificandolo.

  > TODO: ejemplo  

5) ¿Qué es **JUnit**? ¿Para qué lo utilizó? Proporcione un ejemplo breve pero completo de uso de JUnit.

### Tema 2

1) ¿Para qué sirven las **clases abstractas**? ¿Qué uso le daría?

  > Las clases abstractas al igual que las clases comunes sirven para formar jerarquías, tienen fines meramente taxonométricos ya que nos permiten modelar soluciones de una manera conceptual. Su particularidad es que jamás serán instanciadas.  
  > Se pueden usar para generalizar un modelo.

2) Explique el significado y uso de la frase *"Tell, don't ask"*. Proporcione un ejemplo original del mismo.

 > La frase "*Decir, no hacer*" hace referencia al ocultamiento de la información e implementación de un programa y su encapsulamiento. En la POO se instruye a los objetos para que hagan cosas abstrayendonos de como es que las saben hacer. No es conveniente ni lógico, preguntarle a un objeto sobre su estado, ya que vilaríamos el principio de encapsulamiento.

 > TODO: ejemplo

3) Diferencie conceptual y prácticamente los conceptos de **encapsulamiento** y **ocultamiento de la información**.

  > El encapsulamiento es una tecnica para agrupar elementos, que nos permite armar nuestros objetos de una manera especializada, completa y segura (protegiendo sus datos), determinando las responsabilidades que estos tendrán.  
  > Por otra parte, el ocultamiento de la información, es el uso de buenas prácticas de programación que permiten abstraer a los módulos clientes de cómo es que se procesan los datos que ellos necesitan, beneficiando así la escalabilidad de nuestro código a futuro.

###### Ejemplo de encapsulamiento sin ocultar información
```java

  public class EncapsulamientoSinOcultarInformacion {
    private <ArrayList> lista = new ArrayList();
    public ArrayList getList() {
      // ...
    }
  }

```

###### Ejemplo de No encapsulamiento con ocultamiento de la información
```java

  public class NoEncapsulamientoConOcultamientoDeLaInformacion {
    public <List> lista = new ArrayList();
  }

```

###### Ejemplo de encapsulamiento con ocultamiento de la información
```java

  public class EncapsulamientoConOcultamientoDeLaInformacion {
    private <List> lista = new ArrayList();
    public ArrayList getList() {
      // ...
    }
  }

```

4) ¿Qué significa **componer** en el ámbito de la programación orientada a objetos? Proporcione un ejemplo apropiado para el caso.

  > Componer significa incluir en una clase funcionalidades ajenas a ella. También se puede entender como delegación, ya que la clase no es responsable del código esa implementación, sino que simplemente la consume para extender su funcionalidad.

```java
  public class Rueda {
    // Omito los atributos
    public void rodar() {
      // código para girar la rueda.
    }
  }

  public class Bicicleta {
    private List<Rueda> ruedas; // Aquí se utiliza la composición
    public void rodar() {
      // iteramos entre las ruedas que tiene la bicicleta
      this.ruedas.rodar();
    }
  }
```

5) En el *Java Collection Framework* hay dos tipos de **List**. Explique ambos, sus parecidos y las diferencias fundamentales.

  > El JCF implementa tanto ArrayList como LinkedList, por ambas ser Listas, poseen semejanzas en sus metodos:  
  `size()`, `hasNext()`, `add()`, `remove()`, `clear()`  
  > Sin embargo se diferencian una de la otra ya que según el uso que se le quiera dar a la Lista, conviene una u otra.  
  > En primer lugar el ArrayList, que se caracteriza por tener una dimensión variable y un rapido y efectivo acceso a sus datos, conviene utilizarlo cuando se quiere iterar una lista en busca de un valor.  
  > El LinkedList, implementa una lista doblemente enlazada, lo cual la presenta como una buena opción a la hora de insertar o borrar datos al inicio o fin de esta.
