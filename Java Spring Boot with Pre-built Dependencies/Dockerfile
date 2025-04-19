FROM eclipse-temurin:17-jdk-alpine AS build

WORKDIR /app
COPY . .
RUN ./mvnw package

FROM eclipse-temurin:17-jre-alpine
WORKDIR /app
COPY --from=build /app/target/app.jar app.jar
CMD ["java", "-jar", "app.jar"]
EXPOSE 8080
# docker build -t spring-boot-app .