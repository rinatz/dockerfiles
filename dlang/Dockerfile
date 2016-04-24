FROM buildpack-deps:trusty

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        gdb \
        gdbserver \
    && rm -rf /var/lib/apt/lists/*

RUN curl -fsSO "https://dlang.org/install.sh" \
    && chmod +x /install.sh

# gdbserver
EXPOSE 2159

CMD ["tail", "-f", "/dev/null"]
