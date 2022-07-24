# DOCKER_KAFKA
docker file Kafka for testing

1. Software installed:
	- Docker Desktop
	- Offset Explorer (Kafka Tool: https://kafkatool.com/download.html)



2. Let's start the Kafka server by spinning up the containers using the docker-compose command (port 29092):
    $ docker-compose up -d
	Creating network "kafka_default" with the default driver
	Creating kafka_zookeeper_1 ... done
	Creating kafka_kafka_1     ... done


3. Now let's use the nc command to verify that both the servers are listening on the respective ports:
	$ nc -z localhost 22181
	Connection to localhost port 22181 [tcp/*] succeeded!
	$ nc -z localhost 29092
	Connection to localhost port 29092 [tcp/*] succeeded!


<Optional>
	In /multi-cluster docker-compose for start multi node Kafka cluster. 
	Although zookeeper-1 and zookeeper-2 are listening on port 2181, they're exposing it to the host via ports 22181 and 32181, respectively. 
	The same logic applies for the kafka-1 and kafka-2 services, where they'll be listening on ports 29092 and 39092, respectively.

		$ docker-compose up -d
		Creating network "kafka_default" with the default driver
		Creating kafka_zookeeper-1_1 ... done
		Creating kafka_zookeeper-2_1 ... done
		Creating kafka_kafka-2_1     ... done
		Creating kafka_kafka-1_1     ... done
	
	

