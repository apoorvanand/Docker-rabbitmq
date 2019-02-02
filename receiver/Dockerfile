FROM openjdk:8-jdk-alpine
VOLUME /tmp
ARG JAVA_OPTS
ENV JAVA_OPTS=$JAVA_OPTS
ADD rabbitmq-tutorials.jar spring-amqp.jar
ENTRYPOINT exec java $JAVA_OPTS -jar spring-amqp.jar --spring.profiles.active=publish-subscribe,receiver
# For Spring-Boot project, use the entrypoint below to reduce Tomcat startup time.
#ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar spring-amqp.jar
