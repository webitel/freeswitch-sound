FROM debian:wheezy
MAINTAINER Vitaly Kovalyshyn "v.kovalyshyn@webitel.com"

ENV SND_VERSION 1.0.51
ENV SND_NAME ru-RU-elena

RUN apt-get -y --quiet update \
	&& apt-get -y --quiet install curl \
	&& rm -rf /var/lib/apt/lists/* \
	&& mkdir -p /sounds \
	&& cd /sounds \
	&& curl http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-8000-$SND_VERSION.tar.gz \
	| tar zxf \
	&& curl http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-16000-$SND_VERSION.tar.gz \
	| tar zxf \
	&& curl http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-32000-$SND_VERSION.tar.gz \
	| tar zxf \
	&& curl http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-48000-$SND_VERSION.tar.gz \
	| tar zxf

VOLUME ["/sounds/ru"]
ENTRYPOINT ["true"]