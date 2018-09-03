FROM php:7.2-apache

RUN apt-get update \
 && apt-get install -y zlib1g-dev libicu-dev git \
 && docker-php-ext-configure intl \
 && docker-php-ext-install pdo pdo_mysql zip \
 && a2enmod rewrite \
 && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/html
