# Spring Kafka producer

Simple Kafka message producer server written in Spring. Dockerized.

## Deploying with Docker

1. Install Docker on your machine. Make sure it's running.
2. Navigate to the root folder of the project, where the Dockerfile and the docker-compose.yml are.

### Setting up
```bash
docker build -t spring/kafka-producer .
docker-compose up -d
```

### Troubleshoot
1. Go to <http://localhost:8081/kafka/publish/{YourNameHere}>
2. SSH into the Kafka container
```bash
docker exec -it kafka-producer_kafka_1 bash
```
3. List the messages
```bash
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic Kafka_E --from-beginning
```
4. You should see something like this:
```bash
{ "name": "Ted", "dept": "IT", "salary": 4500 }
```