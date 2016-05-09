FROM buildpack-deps:trusty

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        ccache \
        clang-3.5 \
        clang-format-3.5 \
        cmake \
        doxygen \
        gdb \
        gdbserver \
        libboost1.55-all-dev \
    && rm -rf /var/lib/apt/lists/*
