FROM ubuntu:16.04

# Add webupd8team ppa
RUN	echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main" | \
		tee /etc/apt/sources.list.d/webupd8team-java-trusty.list && \
	echo "deb-src http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main" | \
		tee -a /etc/apt/sources.list.d/webupd8team-java-trusty.list && \
	apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys EEA14886 && \
	echo oracle-java6-installer shared/accepted-oracle-license-v1-1 select true | \
		/usr/bin/debconf-set-selections

RUN	apt-get update \
	&& apt-get --yes install 'oracle-java8-installer=8u131-1~webupd8~2' \
	&& apt-get --yes autoclean
        
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
