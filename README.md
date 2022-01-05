# spring-boot-ibm-mq-jms
MQ JMS application development with Spring Boot
Use the MQ Spring JMS Starter to access an IBM MQ server from a Spring Boot application

Prerequisites
Maven and Java installed on your computer. It is assumed that you can build and run a Maven based Spring Initializr project.
Docker installed on your computer. It is assumed that you are able to start/stop containers and are generally familiar with Docker.

Follow below steps
1. Create a Spring Boot application using the Spring Initializr
2. Launch a local MQ Server using Docker

The IBM MQ for Developers container provides a quick and simple way to launch a local MQ Server via Docker. You can launch one using the following command:

docker run ‑‑env LICENSE=accept ‑‑env MQ_QMGR_NAME=QM1
           ‑‑publish 1414:1414
           ‑‑publish 9443:9443
           ‑‑detach
           ibmcom/mq

Check that the server is running using docker ps:
It will show something like below
$ docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS                                            NAMES
3a225c721428        ibmcom/mq           "runmqdevserver"    4 hours ago        Up 4 hours      

3. Add the MQ server config (credentials and URL) to your application
4. Add the MQ Spring Starter to your application
5. Add a REST endpoint that sends a message
6. Add a REST endpoint that retrieves messages
7. Build the app and invoke the REST endpoint and display the results from MQ.
