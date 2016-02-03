FROM gcc:4.8

ENV DMD_VERSION 70

RUN curl -fSL http://master.dl.sourceforge.net/project/d-apt/files/d-apt.list -o /etc/apt/sources.list.d/d-apt.list \
    && apt-get update \
    && apt-get -y --allow-unauthenticated install --reinstall d-apt-keyring \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
        gdb \
        dmd-bin \
        dub \
        libphobos2-dev \
        libphobos2-$DMD_VERSION \
    && rm -rf /var/lib/apt/lists/*
