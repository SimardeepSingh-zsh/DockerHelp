FROM rust:latest

WORKDIR /app
COPY . .
RUN cargo build --release

CMD ["./target/release/app"]
# Expose the port the app runs on
EXPOSE 8080