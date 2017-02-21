FROM alpine
MAINTAINER Falko Zurell <falko.zurell@gmail.com>

LABEL description="uBirch Maven build container"
RUN apk add --update nodejs git alpine-sdk autoconf nasm file automake make g++ gcc
RUN npm install -g bower
RUN npm install -g grunt-cli
RUN mkdir -p /build
WORKDIR /build
