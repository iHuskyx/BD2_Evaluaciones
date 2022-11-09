### Prueba Corta #9
#### Tecnológico de Costa Rica
#### Escuela de Ingeniería en Computación
#### Bases de datos II (IC 4302)
#### Segundo Semestre 2022

```
Estudiante: Andrea María Li Hernández - Carnet: 2021028783
```

1. Suponiendo que un sistema de bases de datos relacional que presenta un read-heavy
workload y los queries son muy diferentes, explique detalladamente ¿porque el uso
de caches puede afectar el rendimiento del sistema de forma negativa? (30 pts)

Si se tiene un sistema de base de datos que tiene que afrontar una carga de trabajo de gran volumen de lecturas y de forma constante, donde los queries requieren de datos muy diferentes, al consultar en caché se tendrá una mayor probabilidad de toparse con una cache miss. Es decir, los datos solicitados no se encuentran en el caché, por lo que se necesita ir a consultar con la memoria principal. 

Esto significa que se tiene más overhead al consultar en el caché, aún sin tener garantizado que los datos requeridos por el query se podrán encontrar; si se da el caso que no se encuentran, hay que hacer una segunda consulta, pero esta vez con la memoria principal, donde se tiene que pasar por un mayor volumen de datos para encontrar lo que se busca. 

Si se tiene el conocimiento previo sobre el patrón de acceso a los datos y el tipo de información que se estará consultando, lo ideal sería para este caso, no depender tanto del caché porque afecta el rendimiento de la BD cuando sencillamente uno se podría ahorrar ese overhead e ir a consultar directamente con la memoria principal.

2. El particionamiento de tablas en bases de datos relacionales es un concepto muy
parecido al de shards en bases de datos NoSQL, explique detalladamente ¿Cómo
afecta el particionamiento y el sharding en el rendimiento de bases de datos SQL y
NoSQL? (30 pts)

En las bases de datos SQL, con el particionamiento podemos tomar la base de datos y partirla en diferentes pedazos o contenedores, entonces en lugar de realizar búsquedas en un solo servidor con un gran volumen de datos, podemos paralelizar las transacciones en la base de datos pues se puede tener diferentes servidores trabajando. Gracias a esto se puede reducir el tiempo de respuesta porque se agilizan las búsquedas de datos y así, del lado del usuario, se obtiene mayor eficiencia en las consultas. 

En las bases NoSQL se utiliza el concepto de sharding, el cual consiste en separar los datos como en el particionamiento, pero según criterios o filtros específicos; esto posee un mayor impacto en el rendimiento de la base datos, porque si se saca el máximo beneficio, se pueden tomar los criterios más utilizados en las consultas de la BD y aplicar sharding con ellos. Al hacer esto aumentamos la velocidad de búsqueda en las consultas en general y aún más en las consultas que se realizan con mayor frecuencia y facilitamos el acceso a los datos; entonces al final se potencia el rendimiento de la base de datos.


3. En un sistema de bases de datos con Strong Consistency cuyo workload es de
read-heavy y write-heavy, ¿Cómo afectan los exclusive locks el rendimiento de las
bases de datos NoSQL? (20 pts)

Una base de datos que implementa los exclusive locks no permitirá que más de una transacción modifique un recurso al mismo tiempo, es decir, se tienen transacciones que únicamente se realizan de forma secuencial pues se busca asegurar la consistencia de los datos. Si tenemos una base de datos que tendrá lecturas y escrituras de forma simultánea y muy constante, cada transacción tendrá que esperar a que se libere un recurso determinado, esto se traduce a timeout para el usuario y, finalmente, el rendimiento se ve penalizado. 

Por lo menos, si se implementaran shared locks, se permite que dos transacciones realicen una lectura sobre el mismo recurso; por lo que mantenemos el rendimiento para la carga de trabajo en lecturas; sin embargo, con los exclusive locks no se permiten más de dos transacciones, independientemente si es lectura o escritura, por lo que la base de datos no estará capacitada para satisfacer la carga de trabajo en lecturas y escrituras. 


4. Explique detalladamente, ¿Cómo afecta la selección de discos físicos el rendimiento
de una base de datos SQL y NoSQL? (20 pts)

Los discos físicos pueden brindar beneficios a la base de datos, en primer lugar, no se deben estar moviendo los datos entre redes lo que nos brinda más velocidad en consultas. Además, en comparación con los discos en red, no se está limitado a la velocidad de la tarjeta de red.

Otro aspecto donde las los discos físicos afectan de forma positiva al rendimiento de la base de datos, es que corremos menor riesgo de tener que paginar e ir a disco, lo que disminuye el memory footprint que se puede tener en la BD. 
