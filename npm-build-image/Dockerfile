FROM node:boron
MAINTAINER Falko Zurell <falko.zurell@ubirch.com>

LABEL description="uBirch Maven build container"
# RUN apt-get update && apt-get install -y nodejs npm git build-essential
RUN npm install -g bower
RUN npm install -g grunt-cli
RUN mkdir -p /build
WORKDIR /build
