# SPARK

https://github.com/rockthejvm/spark-essentials

## SPARK-SQL

 #### Spark Tables:

##### Managed:
(i) Spark is in charge of the metadata + the data.

(ii) If you drop the table, you lose the data.

##### External(ummanaged):

(i) Spark is in charge of the metadata +the data

(ii) If you drop the table, you keep the data.



## RDD(Resilient Distributed Datasets):

Distributed typed collections of JVM objects

The "first citizens" of Spark, all higher level APIs reduce to RDDs

#### Pros: Can be highly optimized.
* Partitioning can be controlled.
* Order of element can be controlled
* Order of operations matters for performance

#### Cons: Hard to Work with
* for Complex operations, need to know the internals of spark
* poor APIs for quick data processing 

For 99% of operations use the Dataframe/Dataset APIs

If you work on RDDs, you need to create the SparkContext

#### RDD vs DataFrame vs Dataset

DataFrame = Dataset[Row]

In common:
* collection API: map, flatmap, filter, take, reduce etc.
* union, count, distinct
* groupBy, sortBy

RDDs over Datasets

* partition control: repartition, coalesce, mapPartitions etc 
* operation control: checkpoint, isCheckpointed, localCheckpoint,cache
* storage control: cache, getStorageLevel persist

Datasets over RDDs

* select and join!
* Spark planning/optimization before running the code

For the 99% operations, use the Dataframe/Dataset APIs

Soure: https://www.udemy.com/course/spark-essentials/