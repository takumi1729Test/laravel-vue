FROM php:7.4.1-fpm

#copy php.ini
COPY ./docker/php/php.ini /usr/local/etc/php/php.ini

#composer install
COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer

#install Node.js
COPY --from=node:18.16 /usr/local/bin /usr/local/bin
COPY --from=node:18.16 /usr/local/lib /usr/local/lib

RUN apt-get update && \
    apt-get -y install \
    git \
    zip \
    unzip \
    vim \
    && docker-php-ext-install pdo_mysql bcmath

WORKDIR /var/www/html