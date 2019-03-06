FROM fpoussin/jenkins:ubuntu-18.04

RUN apt-get install -qq curl
RUN curl -L https://developer.arm.com/-/media/Files/downloads/gnu-rm/8-2018q4/gcc-arm-none-eabi-8-2018-q4-major-linux.tar.bz2 | tar -xjC /usr/local
RUN cd /usr/local/gcc-arm-none-eabi-8-2018-q4-major/bin/; for i in *; do ln -s /usr/local/gcc-arm-none-eabi-8-2018-q4-major/bin/$i /usr/local/bin/$i; done;

EXPOSE 22
CMD /usr/sbin/sshd -D
