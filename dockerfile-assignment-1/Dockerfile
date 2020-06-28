## Docker-Mastery Course Assingment 01
## Author : SURIYAKUMAR RAJARAJAN


## BASE IMAGE
FROM node:14.4.0-alpine3.12

## PORT
EXPOSE 3000

## PACKAGE INSTALLATION
RUN apk add --update tini

## APP DIRECTORY
WORKDIR /usr/src/app

## COPY THE package.json file FROM LOCAL
COPY package.json package.json

## NODE MODULE INSTALLATION
RUN npm install && npm cache clean --force

## COPY THE NODE APP FILE FROM LOCAL
COPY . .

## DOCKER CONTAINER RUN COMMAND
CMD [ "/sbin/tini", "--", "node", "./bin/www" ]