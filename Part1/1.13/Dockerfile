FROM openjdk:8

WORKDIR spring-example-project
COPY spring-example-project .

RUN ./mvnw package

EXPOSE 8080

CMD java -jar ./target/docker-example-1.1.3.jar
