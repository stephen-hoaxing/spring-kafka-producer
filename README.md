###1. docker build -t spring/kafka-producer .
###2. docker-compose up -d
###3. http://localhost:8081/kafka/publish/{YourNameHere}
###4. ssh into the kafka container: docker exec -it kafka-producer_kafka_1 bash
    See the messages in the kafka container
    kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic Kafka_E --from-beginning
    You will see something like this { "name": "Sam", "dept": "IT", "salary": 4500 }
    type exit to exit the shell