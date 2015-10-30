FROM ubuntu:14.04

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        curl \
        build-essential \
        autoconf \
        automake \
        libtool \
        cmake \
        gdb \
        gdbserver \
        libboost-all-dev \
        libgtest-dev

ENV LIBRARY_PATH /usr/lib/x86_64-linux-gnu:$LIBRARY_PATH
ENV LD_LIBRARY_PATH /usr/lib/x86_64-linux-gnu:$LD_LIBRARY_PATH
