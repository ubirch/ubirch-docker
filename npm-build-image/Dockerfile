FROM alpine
MAINTAINER Falko Zurell <falko.zurell@gmail.com>

LABEL description="uBirch Maven build container"
RUN apk add --update nodejs
RUN apk add --update git
RUN apk add --update alpine-sdk
RUN npm install -g bower
RUN npm install -g grunt-cli
RUN mkdir -p /build
WORKDIR /build