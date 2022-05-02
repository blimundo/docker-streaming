# Data Streaming Processing

A simple setup to run Apache Kafka + Apache Spark.

## Services

| Service | Version | Ports |
| --- | --- | --- |
| Apache Zookeeper | 3.5.6 | 2181<br>2888<br>3888 |
| Apache Kafka | 2.2.2 | 9092<br>9997 |
| Kafka UI | 0.3.3 | 8080 |
| Apache Spark (master) | 3.2.1 | 9090<br>7077 |
| Apache Spark (worker 1) | 3.2.1 | 9091<br>7000 |
| Apache Spark (worker 2) | 3.2.1 | 90930<br>7001 |

## Running apps

1. Put app in _apps_ folder (local machine)

2. Open a terminal to _spark-master_

3. Go to apps folder inside container
```bash
cd /opt/spark-apps
```
4. Run app with
```bash
/opt/spark/bin/spark-submit --packages org.apache.spark:spark-streaming-kafka-0-10_2.12:3.2.1,org.apache.spark:spark-sql-kafka-0-10_2.12:3.2.1 <your_app>
```
