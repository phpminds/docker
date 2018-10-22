<<<<<<< Updated upstream
FROM composer:1.7.2 as composer
FROM php:7.2.10-fpm
=======
FROM php:7.2.11-fpm
>>>>>>> Stashed changes

RUN apt-get update && apt-get install -y \
    git zip unzip \
    && docker-php-ext-install -j$(nproc) pdo pdo_mysql \
    && docker-php-source delete

CMD ["php-fpm","-F"]

