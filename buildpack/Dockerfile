FROM buildpack-deps:trusty

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        build-essential \
        autoconf \
        clang-3.5 \
        clang-format-3.5 \
        clang-modernize-3.5 \
        libclang-3.5-dev \
        gdb \
        gdbserver \
        cgdb \
        valgrind \
        google-perftools \
        strace \
        cmake \
        swig \
        protobuf-compiler \
        libprotobuf-dev \
        libboost1.55-all-dev \
        python-pip \
        openjdk-7-jdk \
    && rm -rf /var/lib/apt/lists/*
