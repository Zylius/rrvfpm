FROM php:8.2

RUN docker-php-ext-install sockets

RUN apt-get update

RUN apt-get install wget
RUN apt-get install unzip
RUN wget -c https://github.com/roadrunner-server/roadrunner/releases/download/v2.12.3/roadrunner-2.12.3-linux-amd64.tar.gz -O - | tar -xz -C /tmp/
RUN cp /tmp/roadrunner-2.12.3-linux-amd64/rr /bin

RUN rm -rf /tmp/roadrunner-2.12.3-linux-amd64