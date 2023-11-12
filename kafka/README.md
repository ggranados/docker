# Basic Kafka Server


```bash
docker-compose up -d
docker ps
docker exec -it container_name /bin/bash
```

## Exec command from docker
```bash
PS C:\Users\guill> docker exec -it kafka-kafka-1 kafka-topics.sh --list --bootstrap-server localhost:9092
```

## Topics

### Create topic
```bash
$ kafka-topics.sh --bootstrap-server kafka:9092 --create --topic quickstart
```

### Describe topic
```bash
$ kafka-topics.sh --bootstrap-server kafka:9092 --describe --topic quickstart 
```

### List topics
```bash
$ kafka-topics.sh --list --bootstrap-server kafka:9092
```

## Messages

### Producer
```bash
$ kafka-console-producer.sh --bootstrap-server kafka:9092 --topic quickstart
```

### Consumer
```bash
$ kafka-console-consumer.sh --bootstrap-server kafka:9092 --topic quickstart --from-beginning
``