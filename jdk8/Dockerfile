FROM ubuntu:16.04

MAINTAINER Ron Ellis <rone@benetech.org>

ARG BASE_NAME=jdk-8-oracle
# pass this in with ie "docker build --build-arg JAVA_UPDATE=131"
ARG JAVA_UPDATE
ARG JAVA_URL="https://artifactory.benetech.org/ext-releases-local/jdk-8u$JAVA_UPDATE-linux-x64.tar.gz"
ARG JAVA_TEMP_FILE="/tmp/$BASE_NAME.tar.gz"

ADD $JAVA_URL $JAVA_TEMP_FILE 

RUN apt-get update -qy \
    && mkdir /opt/$BASE_NAME \
    && tar -zxf /tmp/$BASE_NAME.tar.gz -C /opt/$BASE_NAME \
    && $JAVA_TEMP_FILE 

ENV JAVA_HOME /opt/$BASE_NAME/jdk1.8.0_${JAVA_UPDATE}
ENV PATH /opt/$BASE_NAME/jdk1.8.0_${JAVA_UPDATE}/bin:$PATH
