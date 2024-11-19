FROM node:16
# Set working directory
WORKDIR /app
# Copy dependency definitions
COPY package*.json ./
# Install dependencies
RUN npm install
# Copy application files
COPY . .
# Expose the application port
EXPOSE 80
# Use npm start to start the application
CMD ["npm", "start"]
