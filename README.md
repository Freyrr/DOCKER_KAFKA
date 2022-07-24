# DOCKER_KAFKA
docker file Kafka for testing



Let's start the Kafka server by spinning up the containers using the docker-compose command:
$ docker-compose up -d


Now let's use the nc command to verify that both the servers are listening on the respective ports:
$ nc -z localhost 22181
Connection to localhost port 22181 [tcp/*] succeeded!
$ nc -z localhost 29092
Connection to localhost port 29092 [tcp/*] succeeded!
