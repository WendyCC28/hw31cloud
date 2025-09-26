FROM openjdk:8-jdk-slim
WORKDIR /app
COPY target/*.jar app.jar
EXPOSE 8080

ENV SA_LOGIC_API_URL http://sa-logic:80
CMD ["java","-jar","app.jar","--sa.logic.api.url=${SA_LOGIC_API_URL}"]

