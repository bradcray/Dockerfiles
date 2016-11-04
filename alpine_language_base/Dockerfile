FROM alpine:edge
MAINTAINER Jon Jagger <jon@jaggersoft.com>

# https://pkgs.alpinelinux.org/packages?name=shadow
# Currently shows that shadow is only under edge testing

RUN echo "http://dl-2.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories; \
    echo "http://dl-3.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories; \
    echo "http://dl-4.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories; \
    echo "http://dl-5.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories;

# usermod (needed by docker_tar_pipe_runner.sh in main cyber-dojo repo)
RUN apk --update add shadow

# - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
# install tini (for pid 1 zombie reaping)
RUN apk add --update --repository http://dl-cdn.alpinelinux.org/alpine/edge/community/ tini
ENTRYPOINT [ "/sbin/tini", "--" ]
