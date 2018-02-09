FROM ubuntu:16.04

MAINTAINER Ron Ellis <rone@benetech.org>

ENV JAVA_HOME /opt/java-8-oracle

ARG JAVA_URL="https://artifactory.benetech.org/ext-releases-local/jdk-8u131-linux-x64.tar.gz"
ARG BUILDTIME_DEPS="curl"

RUN apt-get update -qy \
    && apt-get install -qy $BUILDTIME_DEPS \
    && curl --silent -L -O --output /tmp/java-8-oracle.tar.gz -H "Cookie: oraclelicense=accept-securebackup-cookie" $JAVA_URL \
    && mkdir /opt/java-8-oracle \
    && tar -zxf /tmp/java-8-oracle.tar.gz -C /opt/java-8-oracle \
    && apt-get remote --purge -qy $BUILDTIME_DEPS

ENV PATH /opt/java-8-oracle:$PATH
