### Prueba Corta #1 
#### Tecnológico de Costa Rica
#### Escuela de Ingeniería en Computación
#### Bases de datos II (IC 4302)
#### Segundo Semestre 2022

```
Estudiante: Andrea María Li Hernández - Carnet: 2021028783
```

1. Explique en que consisten los siguientes conceptos:

    **a. Data Warehouse:**
    Es una base de datos especializada para consultas, procesamiento y análisis de datos de forma rápida con grandes volúmenes de datos. Además, están optimizadas para poder hacer acciones de escritura y lectura de grandes lotes de datos.
    
    **b. Data Lake:**
    Los Data Lake permiten almacenar objetos o archivos de "raw data" o datos masivos sin procesar y son de menor costo comparados con los Data Warehouse.

    **c. Data Mart:**
    Consiste en una forma simple de un Data Warehouse, está centrada en un área funcional o un tema en específico. Son sencillas de diseñar y administrar; además, se pueden crear varios Data Marts a partir de un gran Data Warehouse.

<br>

2. ¿De que forma se benefician las aplicaciones del uso de Columnar Storage? Explique.

    Las aplicaciones que utilizan el Columnar Storage cuentan con una mayor eficiencia para operaciones de lectura y de compresión, dado que todo los datos de una columna son del mismo tipo de dato y los datos no se deben leer secuencialmente en cada operación de lectura. Gracias a estos factores, se reduce el input-output y los requerimientos de almacenamiento. 

<br>

3. ¿En que consiste streaming y batch processing?
    
    El streaming consiste en el procesamiento en tiempo real de grandes volúmenes de datos provenientes de aplicaciones web o de dispositivos móviles; por esto, el streaming requiere de una capa de procesamiento robusta. Por otro lado, el batch processing consiste en procesamiento de lotes o "paquetes" de datos, esto se divide en tres tipos: 
    - Extract Transform Load (ETL): Se extraen datos de diferentes fuentes, se procesan o transforman y luego se cargan en el data warehouse, de forma continua y con un flujo definido. 
    
    - Extract Load Transform (ELT): Se extraen datos de diferentes fuentes, se cargan en el data warehouse y posteriormente se realizan las transformaciones necesarias.
    
    - Online Analytical Processing (OLAP): Permite extraer datos e identificar patrones en múltiples dimensiones.

<br>

4. ¿En que consiste datos estructurados, semi estructurados y no estructurados?
    - Datos estructurados: Siguen un esquema tabular (filas y columnas), es decir, existe un dominio de tipo.
     
    - Datos semi estructurados: Son datos que no necesariamente tienen los mismos atributos, es decir, existe diferente información y tipos. Por ejemplo, archivos xml y json. 
    
    - Datos no estructurados: No siguen ningún patrón, se deben utilizar herramientas como el procesamiento de lenguaje natural.

<br>

### Referencias:

Amazon Web Services. (15 de enero de 2021). *Data Warehousing on AWS*. Obtenido de Amazon Web Services: https://docs.aws.amazon.com/whitepapers/latest/data-warehousing-on-aws/data-warehousing-on-aws.html
