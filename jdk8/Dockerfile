FROM ubuntu:16.04

MAINTAINER Ron Ellis <rone@benetech.org>

ENV JAVA_HOME /opt/java-8-oracle

ARG JAVA_URL="https://artifactory.benetech.org/ext-releases-local/jdk-8u131-linux-x64.tar.gz"

ADD $JAVA_URL /tmp/java-8-oracle.tar.gz

RUN apt-get update -qy \
    && mkdir /opt/java-8-oracle \
    && tar -zxf /tmp/java-8-oracle.tar.gz -C /opt/java-8-oracle

ENV PATH /opt/java-8-oracle:$PATH
