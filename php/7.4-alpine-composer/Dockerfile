FROM php:7.4-alpine

RUN apk update && apk add zip openssh-client && rm -rf /var/cache/apk/*

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
