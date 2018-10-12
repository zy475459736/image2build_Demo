##### multistage
FROM maven:3.5-jdk-8 AS build
COPY src /tmp/src
COPY pom.xml /tmp
RUN mvn -f /tmp/pom.xml clean package

FROM gcr.io/distroless/java
COPY --from=build /tmp/target/dockerfileGenerated.jar /tmp/app.jar
#EXPOSE 8080
ENTRYPOINT ["java","-jar","/tmp/app.jar"]



#FROM openjdk:8-jdk-alpine AS build-env
#ADD . /app/examples
#WORKDIR /app
#RUN javac examples/*.java
#RUN jar cfe main.jar examples.HelloJava examples/*.class
#
#FROM gcr.io/distroless/java
#COPY --from=build-env /app /app
#WORKDIR /app
#CMD ["main.jar"]