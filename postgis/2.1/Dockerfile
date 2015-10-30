FROM postgres:9.4

RUN localedef -i ja_JP -c -f UTF-8 -A /usr/share/locale/locale.alias ja_JP.UTF-8
ENV LANG ja_JP.utf8

RUN sed -i 's/httpredir/ftp\.jp/' /etc/apt/sources.list

RUN apt-get update && apt-get install -y \
        postgis \
        postgresql-9.4-postgis-2.1 \
    && apt-get clean \
    && rm -fr /var/lib/apt/lists/*
