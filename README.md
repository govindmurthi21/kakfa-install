# INSTALL GUIDE

## PreReqs

- Need docker desktop installed on box. Make sure you get latest.

1. `docker compose -f docker-compose.yml up`
2. After installation - `docker images`
3. `docker ps`
4. `docker exec -it kafka /bin/sh`
5. cd into the /opt/kafka_2.13-2.8.1/bin
6. Create topic - `kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic firsttopic`
7. Check topic created in Offset Explorer - If not downloaded download it from [here](https://www.kafkatool.com/download.html)
8. Run command - `kafka-console-producer.sh --topic firsttopic --bootstrap-server localhost:9092` And then send a few messages
9. Check Offset explorer again. 
10. Open new shell - preferably side by side. 
11. Run 4 and 5 again in new shell. 
12. Run command - `kafka-console-consumer.sh --topic firsttopic --from-beginning --bootstrap-server localhost:9092`