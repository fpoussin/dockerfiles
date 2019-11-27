FROM ubuntu:16.04

RUN apt-get update
RUN apt-get -qq dist-upgrade
RUN apt-get -qq install python-software-properties software-properties-common sudo
RUN apt-get -qq install openssh-server default-jre-headless build-essential git unzip zip subversion
RUN apt-get -y autoremove
RUN apt-get clean
