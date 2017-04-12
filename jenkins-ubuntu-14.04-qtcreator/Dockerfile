FROM fpoussin/jenkins:ubuntu-14.04-qt5

ENV QTC_VER_MAJOR 4.2
ENV QTC_VER 4.2.1
ENV QTC qt-creator-opensource-src-${QTC_VER}

RUN apt build-dep -y qtcreator
RUN cd /home/jenkins
RUN wget https://download.qt.io/official_releases/qtcreator/${QTC_VER_MAJOR}/${QTC_VER}/${QTC}.tar.gz
RUN tar xf ${QTC}.tar.gz && rm ${QTC}.tar.gz
RUN mkdir qtc-build && cd qtc-build
RUN nice qmake QTC_PREFIX=/usr/local ../${QTC}
RUN nice make -j8
RUN nice make install
#RUN cd ..
#RUN rm -rf qtc-build

EXPOSE 22
CMD /usr/sbin/sshd -D
