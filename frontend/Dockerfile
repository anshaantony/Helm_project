# Use Node image to run http-server
FROM node:18-alpine

# Create app directory
WORKDIR /app

# Copy HTML and static files from current directory (since you're in ./frontend)
COPY ./templates/index.html ./index.html
COPY ./static ./static

# Install http-server globally
RUN npm install -g http-server

# Expose port
EXPOSE 8080

# Serve the frontend
CMD ["http-server", "-p", "8080"]
