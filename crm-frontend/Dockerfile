# Use an official Node runtime as a parent image
FROM node:14 as build

# Set the working directory in the container
WORKDIR /app

# Install dependencies
COPY package*.json ./
RUN npm install

# Bundle app source
COPY . .

# Build the application
RUN npm run build

# Serve the application using serve
FROM nginx:alpine
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
