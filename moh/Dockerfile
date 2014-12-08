FROM debian:wheezy
MAINTAINER Vitaly Kovalyshyn "v.kovalyshyn@webitel.com"

ENV SND_VERSION 1.0.51
ENV SND_NAME music

RUN mkdir -p /sounds \
    && curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-8000-$SND_VERSION.tar.gz \
    | tar -xJC /sounds \
    && curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-16000-$SND_VERSION.tar.gz \
    | tar -xJC /sounds \
    curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-32000-$SND_VERSION.tar.gz \
    | tar -xJC /sounds \
    curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-48000-$SND_VERSION.tar.gz \
    | tar -xJC /sounds

VOLUME ["/sounds/music"]
ENTRYPOINT ["true"]