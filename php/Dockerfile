FROM php:7.4-fpm-alpine

RUN apk update && apk --no-cache add \
    shadow \
    icu-dev \
    && docker-php-ext-install -j$(nproc) intl

COPY ./php.ini /usr/local/etc/php/

RUN usermod -u 1000 www-data

