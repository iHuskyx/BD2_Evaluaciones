### Prueba Corta #2
#### Tecnológico de Costa Rica
#### Escuela de Ingeniería en Computación
#### Bases de datos II (IC 4302)
#### Segundo Semestre 2022

```
Estudiante: Andrea María Li Hernández - Carnet: 2021028783
```

1. Explique el concepto de shard, replica y partition.

Partition es el término usado en bases de datos SQL y consiste en agarrar la base de datos y dividirla, almacenando cada parte en nodos diferentes, lo que nos permite paralelizar la BD.


Shard se utiliza en bases de datos NoSQL, es el mismo concepto que Partition, solo que se hace la separación basada en un criterio en específico, por lo tanto, el acceso a la información es más rápido.


Replica es un método para asegurar la integridad de la base de datos, consiste en tener un tipo de copia de la BD la cual se almacena en un lugar diferente a la original. La réplica se puede sincronizar de diferentes formas con la BD original y existen diferentes métodos de réplica. 


<br></br>
1. Explique la diferencia entre Strong Consistency y Eventual Consistency.
   
En el Strong Consistency se vela por la consistencia de datos, entonces la persona no tendrá disponibilidad de un dato hasta que el sistema se asegure de tener la última versión de este. Por otro lado, con el Eventual Consistency, los datos estarán disponibles en algún momento del tiempo, pero no se asegura que el dato esté actualizado. 

<br></br>
3. ¿En que consiste warm replicas y hot replicas?

Los warm replicas son un tipo de replica que fuerza el Strong Consistency, por lo tanto, el primary y el secondary node siempre son iguales.

Los hot replicas son un tipo de replica que trabaja en Eventual Consistency, siguiendo esa idea, se permiten transacciones aunque los datos no necesariamente estén correctos. 

<br></br>
1. ¿En que consiste consiste switch over y fail over?


Un fail over detecta cuando la base de datos se cae y toma acción de manera automática.


Un switch over se podría considerar la versión “barata” del fail over, pues también detecta cuando la BD se cae, sin embargo, su función es avisar o notificar para que la persona encargada tome acción manualmente. 