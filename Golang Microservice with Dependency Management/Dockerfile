FROM golang:1.21-alpine AS build

WORKDIR /app
COPY . .
RUN go mod tidy && go build -o app

FROM alpine:latest
WORKDIR /app
COPY --from=build /app/app .
CMD ["./app"]
EXPOSE 8080
# Build the Docker image