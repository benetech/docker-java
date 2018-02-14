FROM ubuntu:16.04

MAINTAINER Ron Ellis <rone@benetech.org>

# options are jre or jdk 
ARG JAVA_TYPE=jdk
ARG BASE_NAME=${JAVA_TYPE}-8-oracle
# string for the update number ie 144 
ARG JAVA_UPDATE=144
ARG JAVA_URL="https://artifactory.benetech.org/ext-releases-local/${BASE_TYPE}-8u$JAVA_UPDATE-linux-x64.tar.gz"
ARG JAVA_TEMP_FILE="/tmp/$BASE_NAME.tar.gz"

ADD $JAVA_URL $JAVA_TEMP_FILE 

RUN apt-get update -qy \
    && tar -zxf /tmp/$BASE_NAME.tar.gz -C /opt \
    && rm $JAVA_TEMP_FILE 

ENV JAVA_HOME /opt/${BASE_TYPE}1.8.0_${JAVA_UPDATE}
ENV PATH /opt/${BASE_TYPE}1.8.0_${JAVA_UPDATE}/bin:$PATH
