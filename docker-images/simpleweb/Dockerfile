# Specify a base image
FROM node:alpine

WORKDIR /usr/app

# Install some dependency
COPY ./package.json ./
RUN npm install
COPY ./ ./

# Default command
CMD ["npm", "start"]

# Build: docker build -t buzonliao/simpleweb .
# Execute: docker run -p 8080:8080 buzonliao/simpleweb