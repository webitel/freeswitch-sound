FROM debian:wheezy
MAINTAINER Vitaly Kovalyshyn "v.kovalyshyn@webitel.com"

ENV SND_VERSION 1.0.51
ENV SND_NAME en-us-callie

RUN apt-get -y --quiet update \
	&& apt-get -y --quiet install wget \
	&& mkdir -p /sounds \
	&& cd /sounds \
	&& wget -O - http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-8000-$SND_VERSION.tar.gz | tar zxf - \
	&& wget -O - http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-16000-$SND_VERSION.tar.gz | tar zxf - \
	&& wget -O - http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-32000-$SND_VERSION.tar.gz | tar zxf - \
	&& wget -O - http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-48000-$SND_VERSION.tar.gz | tar zxf - \
	&& rm -rf /var/lib/apt/lists/*

VOLUME ["/sounds/en"]
ENTRYPOINT ["true"]