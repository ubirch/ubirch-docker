FROM ubirch/java:v8
MAINTAINER Falko Zurell <falko.zurell@gmail.com>

LABEL description="uBirch Maven build container"
RUN apt-get update && apt-get install maven git -y && \
    apt-get autoclean && apt-get --purge -y autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN echo "umask 000" >> /etc/profile 
RUN mkdir /build && mkdir /maven-repo
VOLUME /build /maven-repo
WORKDIR /build
ENV JAVA_HOME /usr
ENTRYPOINT ["/usr/bin/mvn"]
ENV MAVEN_OPTS=-Dmaven.repo.local=/maven-repo
CMD ["--help"]
