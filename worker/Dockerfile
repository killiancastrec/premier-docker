FROM maven:3.5-jdk-8-alpine AS builder
COPY . /build
WORKDIR /build
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
COPY --from=builder /build/target/worker-jar-with-dependencies.jar /build/
WORKDIR /build
CMD  java -jar worker-jar-with-dependencies.jar