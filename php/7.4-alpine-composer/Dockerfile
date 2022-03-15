FROM php:7.4-alpine

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

ENTRYPOINT ["docker-php-entrypoint"]
CMD ["php" "-a"]
