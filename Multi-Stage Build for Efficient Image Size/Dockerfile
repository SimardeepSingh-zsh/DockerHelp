# Use a build stage for compiling dependencies
FROM node:20 AS build
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install --production

# Use a separate stage for the final runtime
FROM node:20-alpine
WORKDIR /app
COPY --from=build /app/node_modules ./node_modules
COPY . .
CMD ["node", "index.js"]
EXPOSE 3000
# This Dockerfile uses a multi-stage build to first install dependencies in a larger image and then copy only the necessary files into a smaller image for production. This reduces the final image size and improves security by not including unnecessary build tools.