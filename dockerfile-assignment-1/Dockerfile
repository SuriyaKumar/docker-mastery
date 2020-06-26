FROM node:14.4.0-alpine3.12

RUN apk add --update tini && mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install && npm cache clean --force

COPY . .

EXPOSE 80

CMD [ "/sbin/tini -- node ./bin/www" ]