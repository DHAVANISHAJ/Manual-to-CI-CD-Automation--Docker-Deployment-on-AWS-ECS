# Use a lightweight Nginx image
FROM nginx:alpine

# Copy the HTML file into the Nginx directory
COPY index.html /usr/share/nginx/html/

# Expose port 80
EXPOSE 80

# Start Nginx in foreground
CMD ["nginx", "-g", "daemon off;"]