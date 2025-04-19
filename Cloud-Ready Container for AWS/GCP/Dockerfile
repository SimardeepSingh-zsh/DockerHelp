FROM python:3.12

WORKDIR /app
COPY . .
ENV GOOGLE_APPLICATION_CREDENTIALS /app/creds.json
CMD ["python", "cloud_app.py"]
EXPOSE 8080
# Build the Docker image