# Use Nginx to serve the pre-built React application
FROM nginx:stable-alpine

# Copy the build output from the local dist folder to the Nginx directory
COPY dist /usr/share/nginx/html

# Copy a custom Nginx configuration to handle React Router navigation
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Expose the port Nginx runs on
EXPOSE 80

# Start Nginx and print the URL to the terminal
CMD ["/bin/sh", "-c", "echo '--- FRONTEND IS READY! ---'; echo 'Access the web app at: http://localhost'; echo '-------------------------'; nginx -g 'daemon off;'"]
