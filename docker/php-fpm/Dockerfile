FROM php:7.2-fpm

RUN apt-get update && apt-get install -y wget git zip zlibc zlib1g zlib1g-dev \
    && pecl install xdebug-2.7.1 \
    && docker-php-ext-enable xdebug

ADD ./php.ini /usr/local/etc/php/php.ini

RUN wget https://getcomposer.org/installer -O - -q \
    | php -- --install-dir=/bin --filename=composer --quiet

RUN docker-php-ext-install zip

WORKDIR /var/www
