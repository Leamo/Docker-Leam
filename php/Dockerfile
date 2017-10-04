FROM php:7.1-fpm

# install some apps
RUN apt-get update && apt-get install -y \
    curl \
    git \
    unzip \
    wget

# PHP Extensions
RUN apt-get update && apt-get install -y \
        libcurl3-dev \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
        libzzip-dev \
    && docker-php-ext-install iconv mcrypt curl zip \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd

# PDO
RUN docker-php-ext-install pdo pdo_mysql

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /usr/share/www
