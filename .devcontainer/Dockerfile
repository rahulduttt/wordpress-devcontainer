FROM wordpress:php8.2-apache

# Install development dependencies and tools
RUN apt-get update && apt-get install -y \
    git \
    unzip \
    zip \
    curl \
    ssh \
    nano \
    mariadb-client \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Configure Xdebug
RUN echo "xdebug.mode=debug,develop" >> /usr/local/etc/php/conf.d/xdebug.ini \
    && echo "xdebug.client_host=host.docker.internal" >> /usr/local/etc/php/conf.d/xdebug.ini \
    && echo "xdebug.start_with_request=yes" >> /usr/local/etc/php/conf.d/xdebug.ini

# Set up Apache rewrite module
RUN a2enmod rewrite

# Configure PHP for development
RUN mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"

WORKDIR /var/www/html