FROM gcc:latest AS build

WORKDIR /app
COPY . .
RUN g++ -o app main.cpp

FROM alpine:latest
WORKDIR /app
COPY --from=build /app/app .
CMD ["./app"]
EXPOSE 8080