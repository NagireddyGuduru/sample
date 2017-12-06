FROM openjdk:8-jdk-alpine

COPY oauth2-authorization-service-0.0.1-SNAPSHOT.jar app.jar
COPY wait-for /wait-for
RUN chmod +x /wait-for

EXPOSE 8000

ENV JAVA_OPTS=""

ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar