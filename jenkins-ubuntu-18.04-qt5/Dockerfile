FROM fpoussin/jenkins:ubuntu-18.04

RUN apt-get update
RUN apt-get -qq dist-upgrade
RUN apt-get -qq install libusb-1.0-0-dev libhidapi-dev 
RUN apt-get -qq install qt5-qmake qt5-default "^qt.*5-dev(-tools)?" "^qt.*5-private-dev"
RUN apt-get -qq install software-properties-common
RUN add-apt-repository -y ppa:fpoussin/ppa
RUN apt-get -qq install libqt5usb5 libqt5usb5-dev
RUN apt-get autoclean
