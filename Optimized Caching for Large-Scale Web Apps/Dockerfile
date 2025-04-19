FROM node:20

WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install --cache-min=86400

COPY . .
CMD ["node", "server.js"]
EXPOSE 3000
# Build the Docker image