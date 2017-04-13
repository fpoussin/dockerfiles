FROM fpoussin/jenkins:ubuntu-16.04-arm

RUN wget http://software-dl.ti.com/msp430/msp430_public_sw/mcu/msp430/MSPGCC/latest/exports/msp430-gcc-6.2.1.16_linux64.tar.bz2
RUN tar vxf msp430-gcc-6.2.1.16_linux64.tar.bz2
RUN rm msp430-gcc-6.2.1.16_linux64.tar.bz2
RUN chmod a+x /msp430-gcc-6.2.1.16_linux64/bin/*
RUN echo "PATH=$PATH:/msp430-gcc-6.2.1.16_linux64/bin/" >> /etc/profile

EXPOSE 22
CMD /usr/sbin/sshd -D
