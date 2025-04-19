FROM tensorflow/tensorflow:latest

WORKDIR /app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .
CMD ["python", "model.py"]
EXPOSE 5000
# This Dockerfile is for a TensorFlow model packaging application. It uses the official TensorFlow Docker image as the base image. The working directory is set to /app, and the requirements.txt file is copied into the container. The pip install command installs the required Python packages without caching to reduce image size. Finally, the model.py script is executed when the container starts, and port 5000 is exposed for communication.