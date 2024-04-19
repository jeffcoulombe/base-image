FROM php:7.4.3-apache

RUN apt-get update && apt-get install -y sudo
RUN docker-php-ext-install mysqli pdo pdo_mysql
RUN apt-get install -y gcc make autoconf libc-dev pkg-config libssh2-1-dev
RUN pecl install ssh2-beta
RUN echo "extension=ssh2.so" >> /usr/local/etc/php/php.ini

RUN chmod 777 -R /var/www