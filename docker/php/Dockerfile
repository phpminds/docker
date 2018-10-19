FROM composer:1.7.2 as composer
FROM php:7.2.11-fpm

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apt-get update && apt-get install -y \
    && docker-php-ext-install -j$(nproc) pdo pdo_mysql \
    && docker-php-source delete

CMD ["php-fpm","-F"]

