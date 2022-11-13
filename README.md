# kafka-producer-consumer-example

Step: 1 
>get the WSL Ipv4 ip of your Windows machine using: "ipconfig"
>Edit the kafka-config/docker-compose.yml file and configure <ip>:9092 
~~~
KAFKA_ADVERTISED_LISTENERS: INSIDE://kafka:9093,OUTSIDE://<ip>:9092
~~~

## Run Zookeeper & Kafka in single command: 
~~~
docker compose -f ./kafka-config/docker-compose.yml up -d
(OR)
docker-compose -f ./kafka-config/docker-compose.yml up -d
~~~


## HTTP Request
~~~
curl --location --request POST 'http://localhost:8080/users' \
--header 'Content-Type: application/json' \
--data-raw '{
    "name": "dhananjaya",
    "mobile": "12564",
    "address": "Bangalore"
}'
~~~
