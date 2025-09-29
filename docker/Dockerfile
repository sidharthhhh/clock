# Use the official lightweight Nginx image from Docker Hub
FROM nginx:alpine

# Remove the default Nginx welcome page
RUN rm -rf /usr/share/nginx/html/*

# Copy your website's files from the parent directory (project root)
# into the Nginx public HTML directory.
COPY ../index.html /usr/share/nginx/html/
COPY ../script.js /usr/share/nginx/html/
COPY ../style.css /usr/share/nginx/html/
COPY ../clock.png /usr/share/nginx/html/

# Expose port 80 to allow traffic to the container
EXPOSE 80

# The default command for the nginx container is to start the server.
# This line is good for clarity but not strictly necessary as it's the base image's default.
CMD ["nginx", "-g", "daemon off;"]
