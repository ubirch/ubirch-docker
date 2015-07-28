FROM debian:jessie
MAINTAINER Falko Zurell <falko.zurell@gmail.com>

LABEL description="uBirch avr build container"
RUN apt-get update && apt-get install gcc-avr avrdude arduino-core binutils-avr avr-libc cmake -y && \
    apt-get autoclean && apt-get --purge -y autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN mkdir /build
VOLUME /build
WORKDIR /build
ENV ARDUINO_SDK_PATH=/usr/share/arduino 
