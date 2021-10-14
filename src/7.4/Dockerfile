FROM petehouston/docker-alpine-php:7.4

MAINTAINER Pete Houston <contact@petehouston.com>

RUN wget https://getcomposer.org/download/1.10.23/composer.phar -O composer \
    && mv composer /usr/bin/composer \
    && chmod +x /usr/bin/composer \
    && composer self-update

CMD ["/usr/bin/composer"]
