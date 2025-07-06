# Use the official Node.js 23.10 image
FROM node:23.10

# Set working directory inside the container
WORKDIR /app

# Copy only package.json and lock file first for caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the app (after installing dependencies for cache efficiency)
COPY . .

# Expose the port your server listens on (adjust if needed)
EXPOSE 8005

# Start the app
CMD ["node", "server.js"]
