FROM openjdk:8-jdk-alpine

COPY edge-service-0.0.1-SNAPSHOT.jar app.jar
COPY docker-application.yml application.yml
COPY wait-for /wait-for
RUN chmod +x /wait-for

EXPOSE 80

ENV JAVA_OPTS=""

ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar