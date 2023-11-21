FROM nextcloud:fpm-alpine

RUN apk add --no-cache supervisor \
  && mkdir /var/log/supervisord /var/run/supervisord

COPY supervisord.conf /

ENV NEXTCLOUD_DOCKER_MODE=php-fpm

CMD ["/usr/bin/supervisord", "-c", "/supervisord.conf"]
