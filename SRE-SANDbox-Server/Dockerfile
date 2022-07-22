#BASE-IMAGE

FROM node:14
RUN apt-get update && apt-get full-upgrade -yqq && apt-get install build-essential cmake -yqq

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

#NPM-BUILD - BACKEND

COPY . /usr/src/app

RUN npm ci && \
     npm cache clean --force && \
     npm run build 


