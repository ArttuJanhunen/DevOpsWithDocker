FROM ubuntu:16.04
FROM openjdk:8

RUN apt-get install -y git
RUN git clone https://github.com/docker-hy/spring-example-project
WORKDIR /spring-example-project
RUN ./mvnw package

EXPOSE 8080
ENTRYPOINT java -jar ./target/docker-example-1.1.3.jar

