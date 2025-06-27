# Backend Dockerfile

# Use a later version of node image as the base image
FROM node:16

# Set the working directory
WORKDIR /app

# Install Stripe CLI
RUN npm install -g stripe

# Copy the package.json and package-lock.json files
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port your server is running on
EXPOSE 5000

# Start the server
CMD ["npm", "run", "dev"]
