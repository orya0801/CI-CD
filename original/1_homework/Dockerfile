FROM maven:3.8.1-jdk-8 AS builder

WORKDIR /app/

COPY . .

RUN mvn clean package

FROM openjdk:8-jre-alpine3.7

COPY --from=builder /app/target/my-app-1.0-SNAPSHOT.jar .

ENTRYPOINT ["java", "-jar", "./my-app-1.0-SNAPSHOT.jar"]