FROM php:7.4-fpm

RUN apt-get update && apt-get install -y libicu-dev && docker-php-ext-install intl && docker-php-ext-enable intl
RUN apt-get update && apt-get install -y libxslt-dev && docker-php-ext-install xsl

RUN apt-get update -y && apt-get install -y libpng-dev && docker-php-ext-install gd

RUN apt-get install libsodium-dev -y && docker-php-ext-install sodium

RUN pecl install redis && docker-php-ext-enable redis

RUN apt-get update && apt-get install -y libcurl3-openssl-dev && docker-php-ext-install curl

RUN apt-get update && apt-get install -y libpq-dev && docker-php-ext-install pdo pdo_pgsql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN apt-get install -y \
        libzip-dev \
        zip \
  && docker-php-ext-install zip

WORKDIR /symfony
