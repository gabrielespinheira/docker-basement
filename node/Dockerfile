FROM alpine:latest

WORKDIR /app

COPY . .

RUN apk update

RUN apk upgrade

RUN apk add bash

RUN apk add --update nodejs npm

RUN npm install -g yarn