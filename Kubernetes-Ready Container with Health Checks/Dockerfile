FROM python:3.12

WORKDIR /app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .
HEALTHCHECK --interval=30s --timeout=10s --retries=3 CMD curl -f http://localhost:5000/health || exit 1

CMD ["python", "app.py"]
EXPOSE 5000
# This Dockerfile sets up a Python application with health checks for Kubernetes readiness.