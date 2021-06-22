FROM maven:3.8.1-jdk-8 

WORKDIR /app/

COPY . .

RUN mvn clean package

ENTRYPOINT ["sleep", "infinity"]