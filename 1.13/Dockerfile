FROM openjdk:8-jdk-stretch
RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/docker-hy/spring-example-project
RUN cd spring-example-project && ./mvnw package
EXPOSE 8080
CMD java -jar /spring-example-project/target/docker-example-1.1.3.jar