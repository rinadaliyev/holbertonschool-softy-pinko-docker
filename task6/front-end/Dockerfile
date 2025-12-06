# Use the latest Nginx image
FROM nginx:latest

# Create the directory where we will host the static files
RUN mkdir -p /var/www/html/softy-pinko-front-end

# Copy all front-end files into the hosting directory
COPY . /var/www/html/softy-pinko-front-end

# Copy our custom Nginx configuration to replace the default
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose port 80 for web traffic
EXPOSE 80

# Nginx starts automatically via the base image's default CMD

