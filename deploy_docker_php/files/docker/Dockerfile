FROM php:8.2.5-fpm


RUN apt-get update && apt-get install -y curl git zip  \
    && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install pdo mysqli pdo_mysql sockets

COPY --from=composer /usr/bin/composer /usr/bin/composer

EXPOSE 80
