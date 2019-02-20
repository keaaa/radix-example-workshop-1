# Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. 
# Containers allow a developer to package an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package
# Dockerfile is a definition of how to create a Docker image. 
# 
# -- Base node image with app
#
# FROM scratch
# dockerhub.com - offical images
FROM node:10-alpine
# available: npm, apt, ..

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install --only=production
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

EXPOSE 3000
# used by express
ENV NODE_ENV=production
# command run on docker run
CMD [ "npm", "start" ]
# not multistage