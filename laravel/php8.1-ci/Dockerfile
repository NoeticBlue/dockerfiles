FROM php:8.1-alpine

# Install composer.
RUN wget https://getcomposer.org/download/latest-stable/composer.phar \
  && mv composer.phar /usr/local/bin/composer \
  && chmod +x /usr/local/bin/composer

# Install PHP modules and clean up.
RUN apk add --no-cache $PHPIZE_DEPS git \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
    && echo "xdebug.mode=coverage" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini;
