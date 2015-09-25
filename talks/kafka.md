# Apache Kafka and the Next 700 Stream Processing Systems

By, Jay Kreps

## 3 Types of Computing

- Request/Response
- Batch
- Stream Processing

## The hard parts

- Partitions and scalability
- Semantics and fault tolerance
- Unifying streams and tables
- Re-Processing
- Time

## Kafka

- A distributed log

## Existing Stream Processing

- Samza (Built for Kafka)
- Spark
- Storm
- Flink
- Kafka Streams

## Unifying Stream and Tables

- With kafka you can store changelogs to a table
  - And then compress them
  - To restore the tables (in memory typically)

## Links

- [Apache Kafka](http://kafka.apache.org)
- [KIP-28 (Kafka Streams)](https://cwiki.apache.org/confluence/display/KAFKA/KIP-28+-+Add+a+processor+client)
