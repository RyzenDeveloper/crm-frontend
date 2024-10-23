# Use a Node.js base image
FROM node:16

# Set the working directory
WORKDIR /usr/src/app

# Install live-server globally
RUN npm install -g live-server

# Copy your frontend code into the Docker image
COPY . .

# Expose the port live-server will run on
EXPOSE 8080

# Start live-server
CMD ["live-server", "--port=8080", "--host=0.0.0.0", "--entry-file=index.html"]
