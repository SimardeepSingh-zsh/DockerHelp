FROM php:8.2-fpm-alpine

WORKDIR /var/www/html
COPY . .
RUN composer install

CMD ["php-fpm"]
EXPOSE 9000
# This Dockerfile sets up a PHP 8.2 FPM environment using Alpine Linux.