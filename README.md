You need to install java for running appache kafka 

Basic setup for linux for running apache Kafka

START THE KAFKA ENVIRONMENT

`bin/zookeeper-server-start.sh config/zookeeper.properties`

Open another terminal session and run:


`bin/kafka-server-start.sh config/server.properties`

CREATE A TOPIC TO STORE YOUR EVENTS

bin/kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092

WRITE SOME EVENTS INTO THE TOPIC

`bin/kafka-console-producer.sh --topic quickstart-events --bootstrap-server localhost:9092`

e.g

This is my first event
This is my second event

You can stop the producer client with `Ctrl-C` at any time.

Open another terminal session and run the console consumer client to read the events you just created:

bin/kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092

output
This is my first event
This is my second event



