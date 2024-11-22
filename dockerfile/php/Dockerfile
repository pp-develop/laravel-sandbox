FROM php:8.4-fpm

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update \
    && apt-get install -y git zip unzip \
    && docker-php-ext-install pdo_mysql bcmath

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug 