# Technical Test

Checkout/download this project. The goal is to complete the following exercise that contains both coding challenges and
theorical questions in 1 hour.

Please either create a new branch that you will push back to Github or archive your project at the end of the hour
(send it to enterprisedata-datalake@ubisoft.com if you choose the archive option). You can answer the questions part
directly in this README file.

--------


The goal of this exercise is to ingest and manipulate a small dataset contained in the Avro files located at
src/main/resources/input. The Avro schema is provided in the src/main/resources/avro_utils folder.

A few libraries are already setup in the build.sbt, you can add or remove any dependency as you wish during this
exercise.

Please initiate a Spark Session in local mode, no interaction with an Hadoop cluster will happen during this
exercise.

1. **Compaction** : Using the Spark API, please generate one Avro file that will contain all the records of the four
 input files. You can output this file to the path of your choice on your local machine. Result file does not have to be committed to the
 repository at the end of the exercise.

2. **Transformation/Datamart** : Using the result of the first step, please output the data again (again at the path
 of your choice), but this time partitioned by age, *excluding* people that are younger than 21. Output should look
 like :

    - \path\age=21\\***.avro
    - \path\age=24\\***.avro
    - ...


### Questions:

    Even if our use case is too simple to show the real advantage of compacting small files in fewer bigger ones,
    can you explain why it is critical to run this kind of compaction in HDFS?


