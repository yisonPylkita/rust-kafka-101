# rust-kafka-101
Checking how Rust and Kafka works together


### Create topic
$KAFKA_HOME/bin/kafka-topics.sh --create --topic rcs-measurands --bootstrap-server 192.168.88.237:9092

### List topics
$KAFKA_HOME/bin/kafka-topics.sh --list --bootstrap-server 192.168.88.237:9092

### Read topic messages
$KAFKA_HOME/bin/kafka-console-consumer.sh --bootstrap-server 192.168.88.237:9092 --topic rcs-measurands --from-beginning

### Add topic messages
kafkacat -P -b 192.168.88.237:9092 -t rcs-measurands -p 0 t1.txt t2.txt t3.txt
