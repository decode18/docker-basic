FROM php:7.3-fpm

RUN apt-get update && apt-get install -y git bash wget curl libzip-dev libxml2-dev libssl-dev zlib1g-dev apt-transport-https lsb-release ca-certificates libpng-dev libturbojpeg0 libjpeg-dev \
    && wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg \
    && docker-php-ext-configure gd --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-configure opcache --enable-opcache \
    && docker-php-ext-install mbstring iconv xml pdo_mysql phar zip gd opcache sockets \
    && wget https://getcomposer.org/download/1.6.3/composer.phar -O /usr/local/bin/composer \
    && chmod a+rx /usr/local/bin/composer

RUN echo "Asia/Jakarta" > /etc/timezone
RUN dpkg-reconfigure -f noninteractive tzdata