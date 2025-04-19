FROM node:20

WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install

COPY . .
RUN npm test

CMD ["node", "server.js"]
EXPOSE 3000

# This Dockerfile sets up a Node.js application in a container.
# It installs dependencies, runs tests, and starts the server.
# This Dockerfile sets up a Node.js application with the following steps:
# 1. Use the official Node.js 20 image as the base image.
# 2. This Dockerfile sets up a Node.js application in a container.
# 3. It installs dependencies, runs tests, and starts the server.