# Use an official Node.js runtime as a parent image
FROM node:14

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy all application files to the working directory
COPY . .

# Build the React app for production
RUN npm run build

# Expose a port for the application (e.g., port 80)
EXPOSE 80

# Define the command to run your application
CMD [ "npm", "start" ]
