# Specify base image
FROM node:20-alpine3.17

# Setting work directory
WORKDIR /usr/app

# Copy files
COPY ./package.json ./
# Install dependencies
RUN npm install
COPY ./ ./

# Default command that run when container is created
CMD ["npm","start"]