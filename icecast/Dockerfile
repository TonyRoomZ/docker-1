FROM armhf/ubuntu

MAINTAINER SilentProtest

RUN set -x \
    &&  apt-get update \
    &&  apt-get install -y icecast2 \
    &&  rm -rf /var/lib/apt/lists/*

USER icecast2

WORKDIR /etc/icecast2

COPY icecast.xml /etc/icecast2/icecast.xml

EXPOSE 8000

CMD ["icecast2", "-c", "icecast.xml" ]
