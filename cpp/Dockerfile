FROM buildpack-deps:xenial

SHELL ["/bin/bash", "-c"]
ENV PATH /root/.anyenv/bin:$PATH

RUN echo "Asia/Tokyo" > /etc/timezone
RUN sed -i 's,archive.ubuntu.com,jp.archive.ubuntu.com,g' /etc/apt/sources.list

RUN apt-get update && \
    apt-get install -y \
        apt-transport-https \
        software-properties-common

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 1484120AC4E9F8A1A577AEEE97A80C63C9D8B80B && \
    add-apt-repository "deb [arch=amd64] https://pkg.osquery.io/deb deb main" && \
    curl -fsSL "https://apt.llvm.org/llvm-snapshot.gpg.key" | apt-key add - && \
    add-apt-repository -y "deb http://apt.llvm.org/$(lsb_release -cs)/ llvm-toolchain-$(lsb_release -cs) main"

RUN apt-get update && \
    apt-get install -y \
        cifs-utils \
        cmake \
        clang \
        clang-format \
        libclang-dev \
        lldb \
        llvm-dev \
        dos2unix \
        doxygen \
        gcc-4.8 \
        g++-4.8 \
        gdb \
        graphviz \
        libfcgi-dev \
        jq \
        spawn-fcgi \
        libxml2-utils \
        ninja-build \
        nkf \
        openssh-server \
        osquery \
        qt5-default \
        stow \
        valgrind \
        vim

RUN update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 50 && \
    update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.8 50

RUN git clone https://github.com/anyenv/anyenv /root/.anyenv && \
    eval "$(anyenv init -)" && \
    anyenv install --force-init && \
    anyenv install pyenv && \
    eval "$(anyenv init -)" && \
    pyenv install 3.7.3 && \
    pyenv global 3.7.3 && \
    eval "$(anyenv init -)" && \
    pip install -U pip pipenv ansible conan

RUN curl -fsSL http://bit.ly/rinatz-dotfiles | bash

RUN curl -fsSL "https://github.com/cdr/code-server/releases/download/1.1119-vsc1.33.1/code-server1.1119-vsc1.33.1-linux-x64.tar.gz" | tar zxv && \
    mv /code-server1.1119-vsc1.33.1-linux-x64/code-server /usr/bin/ && \
    rm -rf /code-server1.1119-vsc1.33.1-linux-x64 && \
    mkdir -p /root/.local/share/code-server/User/ && \
    cp /root/.config/Code/User/settings.json /root/.local/share/code-server/User/

WORKDIR /root
EXPOSE 8443
CMD ["/usr/bin/code-server", "--allow-http", "--no-auth"]
