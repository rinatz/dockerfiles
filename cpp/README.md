# cpp

Dockerfile for building C++ applications.

## Build

```shell
$ docker build -t buildpack https://raw.githubusercontent.com/rinatz/dockerfiles/master/cpp/Dockerfile
```

## Run

```shell
$ docker run --name buildpack -p 8443:8443 -d --privileged buildpack
```

Asscess to http://localhost:8443 and [code-server] will be shown.

[code-server]: https://github.com/cdr/code-server
