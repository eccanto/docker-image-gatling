FROM openjdk:8-jdk-alpine

LABEL Author="Erik Ccanto <ccanto.erik@gmail.com>"

ENV GATLING_HOME /app
ENV GATLING_VERSION 3.10.3
ENV GATLING_SOURCE https://repo1.maven.org/maven2/io/gatling/highcharts/gatling-charts-highcharts-bundle/${GATLING_VERSION}/gatling-charts-highcharts-bundle-${GATLING_VERSION}-bundle.zip

WORKDIR ${GATLING_HOME}

RUN apk add --update wget bash libc6-compat
RUN mkdir -p /tmp/downloads                                                  && \
    cd /tmp/downloads                                                        && \
    wget -O gatling-${GATLING_VERSION}.zip ${GATLING_SOURCE}                 && \
    unzip /tmp/downloads/gatling-${GATLING_VERSION}.zip                      && \
    mv gatling-charts-highcharts-bundle-${GATLING_VERSION}/* ${GATLING_HOME} && \
    rm -rf /tmp/*

VOLUME [ "${GATLING_HOME}/conf", "${GATLING_HOME}/results", "${GATLING_HOME}/user-files" ]

ENV PATH ${GATLING_HOME}/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

ENTRYPOINT [ "gatling.sh" ]
