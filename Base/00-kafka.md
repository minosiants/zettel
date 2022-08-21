# Kafka
https://kafka.apache.org/

[How does kafka work in nutshell](https://kafka.apache.org/documentation/#intro_nutshell)

### Key concepts
- **Servers** - kafka runs as a cluster of one or more servers 
- **Clients** - allow to write distributed applicatons and microservices that read, write process streams of events in paralel.  
- **Events** - ( message, record) has _key_ _value_ and _timestamp_.
- **Producers** - client apps that publish (write) events to kafka.
- **Consumers** - those applications that subscibe to process events.
- **Topics** - events are organised and durably stored in topics. Events are not deleted after consumtion. Durability is configured via topic configuration.
- **Partitions** - topics are partitioned means topics are spread over number of buckets. Event key determins to which partition to write.
- **Replication** - every topic can be replicated  

### API 
- **Admin api** - to manage and inspect topics and brockers
- **Producer api** - to publish a stream of events to one or more topics
- **Consumer api** - to subscribe to one or more topics to process events
- **Kafka streams api** - to implement stream processing apps
- **Kafka connect api** -  to build and run reusable data import/export connectors  




