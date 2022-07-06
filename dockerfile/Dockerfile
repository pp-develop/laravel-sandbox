FROM php:7.4-fpm

COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

RUN apt-get update && apt-get install -y zip unzip gnupg git

RUN docker-php-ext-install pdo pdo_mysql

RUN pecl install xdebug \
&& docker-php-ext-enable xdebug

RUN git clone https://github.com/phpredis/phpredis.git /usr/src/php/ext/redis && \
    docker-php-ext-install redis