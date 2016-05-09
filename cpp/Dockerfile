FROM buildpack-deps:trusty

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        ccache \
        clang \
        cmake \
        doxygen \
        gdb \
        gdbserver \
        libboost1.55-all-dev \
    && rm -rf /var/lib/apt/lists/*

# gdbserver
EXPOSE 2159

CMD ["tail", "-f", "/dev/null"]
