FROM jenkins

USER root

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/g' /etc/apt/sources.list
RUN curl -fsSL https://get.docker.com/ | sh
RUN gpasswd -a jenkins docker

USER jenkins
