FROM buildpack-deps:trusty

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        clang-3.5 \
        clang-format-3.5 \
        cmake \
        gdb \
        gdbserver \
        libboost1.55-all-dev \
        libprotobuf-dev \
        protobuf-compiler \
        python-pip \
        swig \
    && rm -rf /var/lib/apt/lists/*
