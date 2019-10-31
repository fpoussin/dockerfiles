FROM fpoussin/jenkins:ubuntu-18.04

ENV vprefix=8-2019q3/RC1.1
ENV version=8-2019-q3-update

RUN apt-get install -qq curl
RUN curl -kL https://developer.arm.com/-/media/Files/downloads/gnu-rm/${vprefix}/gcc-arm-none-eabi-${version}-linux.tar.bz2 | tar -xjC /usr/local
RUN cd /usr/local/gcc-arm-none-eabi-${version}/bin/; for i in *; do ln -s /usr/local/gcc-arm-none-eabi-${version}/bin/$i /usr/local/bin/$i; done;
