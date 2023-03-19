# Basic Kafka Server

## Topics

### Create topic
``
$ kafka-topics.sh --bootstrap-server kafka:9092 --create --topic quickstart
``

### Describe topic
``
$ kafka-topics.sh --bootstrap-server kafka:9092 --describe --topic quickstart 
``

### List topics
``
$ kafka-topics.sh --list
``

## Messages

### Producer
``
$ kafka-console-producer.sh --bootstrap-server kafka:9092 --topic quickstart
``

### Consumer
``
$ kafka-console-consumer.sh --bootstrap-server kafka:9092 --topic quickstart --from-beginning
``