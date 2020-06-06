FROM fpoussin/jenkins:ubuntu-18.04-qt5

ENV QTC_VER_MAJOR 4.12
ENV QTC_VER 4.12.2
ENV QTC_URL https://download.qt.io/official_releases/qtcreator/${QTC_VER_MAJOR}/${QTC_VER}/installer_source/linux_gcc_64_rhel72

RUN apt-get install -qq curl p7zip-full wget
RUN mkdir /qtcreator && cd /qtcreator

RUN wget ${QTC_URL}/qtcreator_dev.7z -P /qtcreator
RUN wget ${QTC_URL}/qtcreator.7z -P /qtcreator
RUN cd /qtcreator && 7z x -y qtcreator_dev.7z
RUN cd /qtcreator && 7z x -y qtcreator.7z
RUN cd /qtcreator && rm qtcreator_dev.7z qtcreator.7z
