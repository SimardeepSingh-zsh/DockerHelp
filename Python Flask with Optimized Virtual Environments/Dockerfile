FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt ./
RUN python -m venv venv && source venv/bin/activate && pip install --no-cache-dir -r requirements.txt

COPY . .
CMD ["sh", "-c", "source venv/bin/activate && python app.py"]
EXPOSE 5000
# This Dockerfile creates a lightweight Python environment using the slim variant of the Python image. It sets up a virtual environment, installs dependencies, and runs a Flask application.