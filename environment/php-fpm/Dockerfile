FROM wordpress:php8.0-fpm

# xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug

# opcode
RUN docker-php-ext-install opcache

# curl
RUN apt install -y libcurl4
RUN apt install -y curl

# mysql
RUN apt-get update
RUN apt-get install -y mariadb-server

# wp-cli
RUN curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
RUN chmod +x wp-cli.phar
RUN mv wp-cli.phar /usr/local/bin/wp

# composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer --version