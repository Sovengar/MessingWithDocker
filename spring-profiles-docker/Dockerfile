FROM maven:3.8.4-openjdk-17 AS build
WORKDIR /app

ARG CONTAINER_PORT

COPY ./pom.xml /app
RUN mvn dependency:resolve
COPY . /app
RUN mvn clean package -DskipTests -X

FROM openjdk:17-jdk
COPY --from=build /app/target/*.jar app.jar
EXPOSE ${CONTAINER_PORT}
CMD ["java", "-jar", "app.jar"]