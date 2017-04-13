FROM fpoussin/jenkins:ubuntu-16.04

RUN add-apt-repository -y ppa:team-gcc-arm-embedded/ppa
RUN apt-get update
RUN apt-get -qq dist-upgrade
RUN apt-get -qq install gcc-arm-embedded=6-2016q4-1~xenial1
RUN apt-get clean 

EXPOSE 22
CMD /usr/sbin/sshd -D
