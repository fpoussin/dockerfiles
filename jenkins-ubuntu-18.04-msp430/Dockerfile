FROM fpoussin/jenkins:ubuntu-18.04

ENV GCC_VER msp430-gcc-7.3.2.154_linux64

RUN apt-get install -qq p7zip-full
RUN wget http://software-dl.ti.com/msp430/msp430_public_sw/mcu/msp430/MSPGCC/latest/exports/$GCC_VER.7z -P /usr/local
RUN cd /usr/local; 7z x -y $GCC_VER.7z
RUN rm /usr/local/$GCC_VER.7z
RUN cd /usr/local/$GCC_VER/bin/; for i in *; do ln -s /usr/local/$GCC_VER/bin/$i /usr/local/bin/$i; done;
