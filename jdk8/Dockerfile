FROM ubuntu:16.04

MAINTAINER Ron Ellis <rone@benetech.org>

ENV JAVA_HOME /opt/java-8-oracle

ARG JAVA_URL="http://download.oracle.com/otn-pub/java/jdk/8u31-b13/jdk-8u31-linux-x64.tar.gz"
ARG BUILDTIME_DEPS="curl"

RUN apt-get update -qy \
    && apt-get install -qy $BUILDTIME_DEPS \
    && curl -L -O -o /tmp/java-8-oracle.tar.gz -H "Cookie: oraclelicense=accept-securebackup-cookie" $JAVA_URL \
    && mkdir /opt/java-8-oracle \
    && tar -xf /tmp/java-8-oracle.tar.gz -C /opt/java-8-oracle \
    && apt-get remote --purge -qy $BUILDTIME_DEPS

ENV PATH /opt/java-8-oracle:$PATH
