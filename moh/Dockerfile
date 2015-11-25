FROM progrium/busybox
MAINTAINER Vitaly Kovalyshyn "v.kovalyshyn@webitel.com"

ENV SND_VERSION 1.0.7
ENV SND_NAME music

RUN opkg-install wget tar gzip \
	&& mkdir -p /sounds \
	&& cd /sounds \
	&& wget -O - http://files-sync.freeswitch.org/releases/music/freeswitch-sounds-$SND_NAME-8000-$SND_VERSION.tar.gz | gzip -dc - | tar xf - \
	&& wget -O - http://files-sync.freeswitch.org/releases/music/freeswitch-sounds-$SND_NAME-16000-$SND_VERSION.tar.gz | gzip -dc - | tar xf - \
	&& wget -O - http://files-sync.freeswitch.org/releases/music/freeswitch-sounds-$SND_NAME-32000-$SND_VERSION.tar.gz | gzip -dc - | tar xf - \
	&& wget -O - http://files-sync.freeswitch.org/releases/music/freeswitch-sounds-$SND_NAME-48000-$SND_VERSION.tar.gz | gzip -dc - | tar xf -

VOLUME ["/sounds/music"]
ENTRYPOINT ["true"]
