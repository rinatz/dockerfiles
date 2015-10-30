FROM buildpack-deps:trusty

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        swig \
        cmake \
        gdb \
        gdbserver \
        libboost-all-dev \
        libgtest-dev \
        libprotobuf-dev
