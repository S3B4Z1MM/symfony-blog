FROM php:8.1-fpm

RUN echo 'deb [trusted=yes] https://repo.symfony.com/apt/ /' > /etc/apt/sources.list.d/symfony-cli.list \
    && apt update \
    && apt install -y \
      git  \
      libpq-dev \
      libzip-dev \
      libicu-dev \
      symfony-cli \
      unzip \
    && pecl install apcu xdebug-3.1.5 \
    && docker-php-ext-install opcache pdo pdo_mysql intl \
    && docker-php-ext-enable apcu xdebug \
    && apt clean && apt purge -y --auto-remove

RUN mkdir -p /usr/local/etc/php/disabled \
    && mv /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini /usr/local/etc/php/disabled/

COPY conf.d/php.ini /usr/local/etc/php/php.ini

# composer
ENV COMPOSER_ALLOW_SUPERUSER=1
COPY --from=composer:2 /usr/bin/composer /usr/local/bin/composer

RUN chown www-data:www-data /var/www

WORKDIR /var/www/html
