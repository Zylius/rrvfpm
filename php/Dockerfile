FROM php:8.2-fpm
RUN docker-php-ext-install sockets
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/bin --filename=composer --2


RUN apt-get update

RUN apt-get install unzip
RUN apt-get install git -y

RUN rm -rf  /usr/local/etc/php-fpm.d/www.conf

COPY php/www.conf /usr/local/etc/php-fpm.d/www.conf
