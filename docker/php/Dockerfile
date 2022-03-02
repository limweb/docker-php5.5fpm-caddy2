FROM php:5.5-fpm

RUN apt-get update && \
     apt-get install -y \
         libzip-dev \
         && docker-php-ext-install zip

# Install application dependencies
RUN docker-php-ext-install pdo_mysql \
    && docker-php-ext-install mysqli && docker-php-ext-enable mysqli \
    && docker-php-ext-install mbstring pdo pdo_mysql

# CMD ["/usr/bin/caddy", "--conf", "/etc/Caddyfile", "--log", "stdout"]