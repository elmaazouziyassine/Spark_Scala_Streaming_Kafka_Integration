# Spark_Scala_Streaming_Kafka_Integration
Spark Streaming with Kafka Integration


Kafka Installation on Windows (Standalone mode)
- Download & install JDK/JRE
- Download Kafa from https://kafka.apache.org/downloads
- Edite the configuration files : server.properties & zookeeper.properties
- Start Zookeeper service
- Start Apache Kafka
- Create a Kafka Topic, Kafka Producer & Kafka Consumer


##### Start Zookeeper service
>kafka\bin\windows\**zookeeper-server-start.bat C:\BigDataLocalSetup\kafka_2.12-2.4.0\config\zookeeper.properties**

##### Start Kafka service (in another terminal)
>kafka\bin\windows\**kafka-server-start.bat C:\BigDataLocalSetup\kafka_2.12-2.4.0\config\server.properties**

##### Check active processes 
>**jps**

##### Create a kafka topic
>kafka\bin\windows>**kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 -topic myFirstTopic**

##### Consult the available topics on the server
>kafka\bin\windows>**kafka-topics.bat --list --zookeeper localhost:2181**

##### Start the Kafka Producer
>kafka\bin\windows>**kafka-console-producer.bat --broker-list localhost:9092 --topic myFirstTopic** 

##### Start the Kafka Consumer
>kafka\bin\windows>**kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic myFirstTopic --from-beginning**


