# Use Node.js official image
FROM node:18
WORKDIR /app

# Copy files and install dependencies
COPY package.json package-lock.json ./
RUN npm install

# Copy all files and expose port
COPY . .
EXPOSE 5000
CMD ["npm", "start"]
