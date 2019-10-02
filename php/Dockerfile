FROM php:7.2.7-fpm-alpine3.7
RUN apk update; \
    apk upgrade;
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo pdo_mysql

#####################################
# GD:
#####################################

# Install the PHP gd library
RUN apk add --update --no-cache \
        freetype-dev \
        libjpeg-turbo-dev \
        libmcrypt-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd