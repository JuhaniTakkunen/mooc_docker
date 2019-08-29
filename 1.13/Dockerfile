FROM openjdk:8
COPY spring-example-project /usr/local/java
WORKDIR /usr/local/java

RUN ./mvnw package

EXPOSE 8080
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
