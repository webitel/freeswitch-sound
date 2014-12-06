FROM busybox
MAINTAINER Vitaly Kovalyshyn "v.kovalyshyn@webitel.com"

ENV SND_VERSION 1.0.51
ENV SND_NAME ru-RU-elena

ADD http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-8000-$SND_VERSION.tar.gz /
ADD http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-16000-$SND_VERSION.tar.gz /
ADD http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-32000-$SND_VERSION.tar.gz /
ADD http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-48000-$SND_VERSION.tar.gz /

VOLUME ["/sounds/ru"]
ENTRYPOINT ["true"]