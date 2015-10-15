# Manual

## Instructions

Run `pre-install.sh`, `download.sh`, `install.sh` in this order.

Edit the file `/opt/kafka_2.10-0.8.2.2/config/server.properties`.

- Set the broker.id in line number 20.
- Add your hostname:port in line number 28.
- Add the address of the Zookeeper host in line number 118.



Edit the file `/opt/kibana-4.1.2-linux-x64/config/kibana.yml`.

- Add the address of the Elasticsearch host in line number 8.

## Commands to execute

#### Run Elasticsearch on a node (say dbnode).
`/opt/elasticsearch-1.7.2/bin/elasticsearch`

#### Run Kafka zookeeper, followed by the server on a node (say node0).
`/opt/kafka_2.10-0.8.2.2/bin/zookeeper-server-start.sh /opt/kafka_2.10-0.8.2.2/config/zookeeper.properties`
`/opt/kafka_2.10-0.8.2.2/bin/kafka-server-start.sh /opt/kafka_2.10-0.8.2.2/config/server.properties`


`/opt/kafka_2.10-0.8.2.2/bin/kafka-console-producer.sh --broker-list <> --topic tokafka`
