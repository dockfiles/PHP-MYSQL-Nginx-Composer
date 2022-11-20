FROM php:8.1.1-fpm-alpine3.15

RUN apk add --update libpq-dev \
    && docker-php-ext-configure pdo_mysql --with-pdo-mysql=mysqlnd \
    && docker-php-ext-configure mysqli --with-mysqli=mysqlnd \
    && docker-php-ext-install pdo mysqli pdo_mysql\
    && docker-php-ext-enable pdo mysqli pdo_mysql
