#Specify a base image
#FROM alpine we will use other image
FROM node:alpine 
# alpine is a term in the docker world that is a small and light as possible
# alpine version of node. It will have really basic things like ls, ping and other small commands with NPM command

WORKDIR /usr/app 
# it goes by convention among developers to put project into separate folder
COPY ./package.json ./ 
# here we copy only package.json file in order to avoid rebuilds from npm
RUN npm install
COPY ./ ./ 
# here we copy all the files (remember to create .dockerignore file in the root dir to avoid copying your node_modules folder)
#but npm is not installed on alpinexie OS

#Default command
CMD [ "npm", "start" ]