FROM ubuntu:14.04

RUN	apt-add-repository --yes ppa:webupd8team/java \
	&& apt-get update \
	&& apt-get --yes install oracle-java6-installer \
	&& apt-get --yes autoclean
        
ENV JAVA_HOME /usr/lib/jvm/java-6-oracle
