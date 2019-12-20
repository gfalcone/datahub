# Wherehows Data Model
The module contains the data model used by WhereHows, including the table DDLs for MySQL DB, Elastic search indices, 
and avro schemas for Kafka events. It also includes the auto generated Kafka event java classes, to be used by other modules.

## Code Generation for Avro Schema
The java code here under src/main/java are auto generated by Avro-tool from avro schema (.avsc) of Kafka events. 
They should not be edited directly.

Note that we currently require avro version 1.4 in Kafka related tasks.

To generate java code, first download avro-tool-1.4.1, then use command line from wherehows-data-model/: 
```
java -jar avro-tools-1.4.1.jar compile schema xxx.avsc src/main/java
```


## Build
```
$ ../gradlew build
  
  BUILD SUCCESSFUL in 0s
  4 actionable tasks: 2 executed, 2 up-to-date
```