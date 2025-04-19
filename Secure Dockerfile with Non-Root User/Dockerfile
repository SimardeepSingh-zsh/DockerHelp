# Create a non-root user
RUN groupadd -r appgroup && useradd -r -g appgroup appuser

WORKDIR /app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy source code and set permissions
COPY . .
RUN chown -R appuser:appgroup /app

# Switch to the non-root user
USER appuser

CMD ["python", "app.py"]

# Use COPY instead of ADD for copying files
# Expose the application port (if applicable)
EXPOSE 5000
# Use a lightweight base image (e.g., Alpine or slim version of the base image)
FROM python:3.9-slim
# Use multi-stage builds to reduce image size
FROM builder AS final
# Use a non-root user to run the application
