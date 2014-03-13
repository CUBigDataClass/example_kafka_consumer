This is just an example of how to run a kafka producer.

### To run it
assuming you installed kafka in your home directory:
- `sbt compile`
- `~/kafka/bin/zookeeper-server-start.sh ~/kafka/config/zookeeper.properties`
- `~/kafka/bin/kafka-server-start.sh ~/kafka/config/server.properties`
- `~/kafka/bin/kafka-create-topic.sh --topic page_visits --zookeeper localhost:2181`
- `sbt run`
- `bin/kafka-console-consumer.sh --zookeeper localhost:2181 --topic page_visits --from-beginning`

This is adapted from the example below if you have trouble:
https://cwiki.apache.org/confluence/display/KAFKA/0.8.0+Producer+Example
