https://docs.google.com/presentation/d/1u5FT9oG2lkSP6BKS9xYcHAd-MP17L3KSQFsX44nAzAY/edit#slide=id.g1db6bb72b7_0_8

- Using HDFS to distribute large data sets
- Using MapReduce to distribute computational tasks to a distributed data sets.

Discuss:
- Spark
- Spark vs MapReduce
- Spark RDD
- Spark DataFrames

You can think of Spark as a flexible alternative to MapReduce
Spark can use data stored in variety of formats:
- Cassandra
- AWS S3
- HDFS
- and more

Spark vs MapReduce
MapReduce requires files to be stored in HDFS, spark does not!
Spark also can perform operations up to 100x faster than MapReduce
So how does it achieve this speed?
- MapReduce writes most data to disk after each map and reduce operation
- Spark keeps most of the data in memory after each transformation
- Spark can spill over to disk if the memory is filled

**Spark RDD**
- At the core of the spark is the idea of the Resilient Distributed Dataset (RDD)
- RDD has 4 more features:
	- Distributed collection of Data
	- Fault-tolerant
	- Parallel operation - partitioned
	- Ability to use many data sources

 Components: Driver program, Cluster management, and Worker nodes
 Mater, Slave(Data cached in RAM/Disk)

RDDs are immutable, lazily evaluated, and cacheable
There are two types of Spark operations:
	Transformations
	Actions
Transformations are basically a recipe to follow.
Actions actually perform what the recipe says to do and returns something back.

