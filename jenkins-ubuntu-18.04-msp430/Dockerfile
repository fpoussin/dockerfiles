FROM fpoussin/jenkins:ubuntu-18.04

ENV GCC_VER=msp430-gcc-8.3.1.25_linux64
ENV GCC_RELEASE=8_3_2_2
ENV GCC_URL=http://software-dl.ti.com/msp430/msp430_public_sw/mcu/msp430/MSPGCC/${GCC_RELEASE}/export/${GCC_VER}.tar.bz2

RUN apt-get install -qq curl
RUN curl -kL ${GCC_URL} | tar -xjC /usr/local
RUN cd /usr/local/${GCC_VER}/bin/; for i in *; do ln -s /usr/local/${GCC_VER}/bin/$i /usr/local/bin/$i; done;

