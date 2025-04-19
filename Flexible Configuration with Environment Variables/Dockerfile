FROM node:20

WORKDIR /app
COPY . .
ENV PORT=8080
CMD ["node", "server.js"]
EXPOSE 8080

# Build the Docker image
# docker build -t my-node-app .
# Run the Docker container with an environment variable
# docker run -p 8080:8080 -e PORT=3000 my-node-app
# Access the application in your browser at http://localhost:3000
