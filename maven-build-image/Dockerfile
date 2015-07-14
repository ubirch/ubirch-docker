FROM debian:jessie
MAINTAINER Falko Zurell <falko.zurell@gmail.com>

LABEL description="uBirch Maven build container"
RUN apt-get update && apt-get install maven -y && \
    apt-get autoclean && apt-get --purge -y autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
VOLUME ["/build"]
WORKDIR /build
ENTRYPOINT ["/usr/bin/mvn"]
ENV MAVEN_OPTS=-Dmaven.repo.local=/build/maven-repo
CMD ["--help"]
