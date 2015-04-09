FROM ubuntu:14.04

RUN	apt-add-repository ppa:webupd8team/java \
	&& apt-get update \
	&& apt-get install --yes oracle-java6-installer \
	&& apt-get autoclean
        
ENV JAVA_HOME /usr/lib/jvm/java-6-oracle
