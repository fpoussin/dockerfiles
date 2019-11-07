FROM fpoussin/jenkins:ubuntu-18.04

ENV vprefix=9-2019q4/RC2.1
ENV version=9-2019-q4-major

RUN apt-get install -qq curl
RUN curl -kL https://developer.arm.com/-/media/Files/downloads/gnu-rm/${vprefix}/gcc-arm-none-eabi-${version}-x86_64-linux.tar.bz2 | tar -xjC /usr/local
RUN cd /usr/local/gcc-arm-none-eabi-${version}/bin/; for i in *; do ln -s /usr/local/gcc-arm-none-eabi-${version}/bin/$i /usr/local/bin/$i; done;
