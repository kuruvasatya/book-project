FROM openjdk:11-jre-slim
ARG DEFAULT_PATH=target/book-app-*.jar
WORKDIR /
ENV JAR_PATH=$DEFAULT_PATH
COPY ${JAR_PATH} app.jar
RUN useradd -m myuser
USER myuser
EXPOSE 8080
CMD ["java", "-jar", "-Dspring.profiles.active=dev", "app.jar"]
