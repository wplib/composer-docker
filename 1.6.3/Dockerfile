FROM composer:1.6.3
MAINTAINER WPLib Team <team@wplib.org>

RUN apk update && \
	apk add --no-cache bash shadow && \
	groupadd -g 1000 vagrant && \
	useradd -d /var/cache/nginx -c "WPLib vagrant user" -u 1000 -g 1000 -N -s /bin/bash vagrant

COPY container.json /etc/container.json
COPY files /
