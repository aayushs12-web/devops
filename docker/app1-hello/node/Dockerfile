# Use Node 20 LTS Alpine base image
FROM node:20-alpine

# Set environment variables
ENV NODE_ENV=production
ENV PORT=3000
ENV ENV_VALUE="Hello from Dockerized Node App"

# Set working directory inside container
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install --only=production

# Copy remaining source code
COPY . .

# Expose application port
EXPOSE 3000

# Command to run the app
CMD ["node", "app.js"]
