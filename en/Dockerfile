FROM debian:wheezy
MAINTAINER Vitaly Kovalyshyn "v.kovalyshyn@webitel.com"

ENV SND_VERSION 1.0.51
ENV SND_NAME en-us-callie

RUN echo 'deb http://ftp.us.debian.org/debian/ wheezy main' >> /etc/apt/sources.list &&\
	apt-get -y --quiet update && \
	apt-get -y --quiet install curl \
	&& mkdir -p /sounds \
    && curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-8000-$SND_VERSION.tar.gz \
    | tar -xzC /sounds \
    && curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-16000-$SND_VERSION.tar.gz \
    | tar -xzC /sounds \
    curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-32000-$SND_VERSION.tar.gz \
    | tar -xzC /sounds \
    curl -SL http://files-sync.freeswitch.org/freeswitch-sounds-$SND_NAME-48000-$SND_VERSION.tar.gz \
    | tar -xzC /sounds

VOLUME ["/sounds/en"]
ENTRYPOINT ["true"]