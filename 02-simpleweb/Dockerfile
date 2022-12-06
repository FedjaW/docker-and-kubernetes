# Specify a base image
FROM node:alpine

# Set a working directory in the container
# This is a best practice to avoid potential conflicts with the root folders
WORKDIR /usr/app

# Copy only package.json to not rerun npm install 
# when only index.js changes (chaching)
COPY ./package.json ./

# Install some dependencies
RUN npm install

# Copy all files into the container
COPY ./ ./

# Default command
CMD ["npm", "start"]