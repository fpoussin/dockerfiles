FROM fpoussin/jenkins:ubuntu-14.04

RUN add-apt-repository -y ppa:terry.guo/gcc-arm-embedded
RUN apt-get update
RUN apt-get -qq dist-upgrade
RUN apt-get -qq install gcc-arm-none-eabi=4.9.3.2015q3-1trusty1

EXPOSE 22
CMD /usr/sbin/sshd -D
