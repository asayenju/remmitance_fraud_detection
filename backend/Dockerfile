# Use an official Node.js runtime as base image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package files first (better caching)
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy the rest of the source code
COPY . .

# Expose backend port
EXPOSE 5000

# Start the app
CMD ["npm", "start"]
