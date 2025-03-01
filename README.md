# recruiter-api-doc
Recruiter Public API Documentation
Rabbitmq Devops-Recruiter.com.tr
ONUR ÖZGÜLTEKİN - 5384042588
Local-192.168.1.76
user:ykc
pw: soft2022
4 Docker Container
networks: my_rabbit_network
Postgresql - Mail Consumer – RabbitMQ – Task Consumer

VPS- ssh root@104.247.166.33 -p 2232
pw:  CK2PvuArdc4q2W992A
4 Docker Container
networks: my_rabbit_network
Postgresql - Mail Consumer – RabbitMQ – Task Consumer







Docker Hub
unholyw4r/consumermail:latest
unholyw4r/consumertask:latest

Mail Consumer => docker run -d --name consumermail --network my_rabbit_network <imageid>
Task Consumer => docker run -d --name consumertask --network my_rabbit_network <imageid>

RabbitMQ => docker run -d --hostname c_rabbitmq --name c_rabbitmq --network my_rabbit_network -p 5672:5672 -p 15672:15672 -e RABBITMQ_DEFAULT_USER=user -e RABBITMQ_DEFAULT_PASS=1234567 rabbitmq:3-management

Postgresql=>docker run -d   --name postgres-container   -e POSTGRES_USER=taskconsumer   -e POSTGRES_PASSWORD=soft2022   -e POSTGRES_DB=hangfire   --network=my_rabbit_network   --mount source=postgres-data,target=/var/lib/postgresql/data   postgres:latest
Docker Engine 
Network: my_rabbit_network

   







