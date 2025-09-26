FROM openjdk:8-jdk-slim
WORKDIR /app
COPY target/*.jar app.jar
EXPOSE 8080

CMD ["java","-jar","app.jar","--sa.logic.api.url=${SA_LOGIC_API_URL}"]
