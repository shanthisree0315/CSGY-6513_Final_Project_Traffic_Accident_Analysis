To run the inferences, ensure that you have an environment with PySpark and other relevant libraries installed and directly run the notebook. 

To run kafka, start the Zookeeper Service

```
$ bin/zookeeper-server-start.sh config/zookeeper.properties
```

Start the Broker Service

```
$ bin/kafka-server-start.sh config/server.properties
```

Create a topic (one time only)

```
$ bin/kafka-topics.sh --create --topic accident_tmp_input --bootstrap-server localhost:9092
```

Run the KafkaProducer first and then the KafkaConsumer. Your output should be accumulated from time to time in a HTML file. 
