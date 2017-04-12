FROM ubuntu:14.04

RUN useradd -m -s /bin/bash jenkins
RUN echo jenkins:jenkins | chpasswd
RUN echo root:root | chpasswd
RUN echo "jenkins ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
RUN mkdir -p /var/run/sshd

RUN apt-get update
RUN apt-get -qq dist-upgrade
RUN apt-get -qq install python-software-properties software-properties-common
RUN apt-get -qq install openssh-server default-jre-headless build-essential git unzip zip subversion

EXPOSE 22
CMD /usr/sbin/sshd -D
