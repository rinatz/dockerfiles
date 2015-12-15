FROM buildpack-deps:trusty

RUN sed -i 's/archive.ubuntu.com/ftp.riken.jp\/Linux/' /etc/apt/sources.list

RUN curl -fSL 'http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key' | apt-key add - \
    && echo 'deb http://pkg.jenkins-ci.org/debian binary/' > /etc/apt/sources.list.d/jenkins.list

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
        libboost1.55-all-dev \
        libgtest-dev \
        libprotobuf-dev \
        python-pip \
        openjdk-7-jdk \
        jenkins \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 8080

CMD ["java", "-jar", "/usr/share/jenkins/jenkins.war"]
