FROM fpoussin/jenkins:ubuntu-14.04

RUN apt-get update
RUN apt-get -qq dist-upgrade
RUN apt-get -qq install libusb-1.0-0-dev
RUN apt-get -qq install qt5-qmake qt5-default "^qt.*5-dev(-tools)?"

EXPOSE 22
CMD /usr/sbin/sshd -D
