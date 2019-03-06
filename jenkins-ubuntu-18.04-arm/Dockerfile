FROM fpoussin/jenkins:ubuntu-18.04

RUN add-apt-repository -y ppa:team-gcc-arm-embedded/ppa
RUN apt-get -qq dist-upgrade
RUN apt-get -y install gcc-arm-embedded=8-2018q4-1~xenial1
#RUN apt-get -y install gcc-arm-embedded
RUN apt-get clean 

EXPOSE 22
CMD /usr/sbin/sshd -D
