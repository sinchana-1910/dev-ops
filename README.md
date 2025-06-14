# Use official Apache HTTP Server image
FROM httpd:2.4

# Copy your HTML file to the Apache web server's root folder
COPY index.html /usr/local/apache2/htdocs/
5th...
# Stop and remove any previous container
docker rm --force container1 || true

# Build Docker image
docker build -t nginx-image1 .

# Run new container on port 8081
docker run -d -p 8081:80 --name=container1 nginx-image1
6th

