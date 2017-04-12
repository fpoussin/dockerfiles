FROM fpoussin/jenkins:ubuntu-15.10

RUN add-apt-repository -y ppa:terry.guo/gcc-arm-embedded
RUN apt-get update
RUN apt-get -qq dist-upgrade
RUN apt-get -qq install gcc-arm-none-eabi=4.9.3.2015q3-1wily1
RUN apt-get clean 

EXPOSE 22
CMD /usr/sbin/sshd -D
