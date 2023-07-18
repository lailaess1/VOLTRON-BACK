FROM php:8.2-cli

# Install pdo
# (Je l'ai oublié dans la vidéo, c'est important car sans ça vous ne pouvez pas vous connecter à votre base de données)
RUN docker-php-ext-install pdo_mysql

WORKDIR /back

# Install composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && php composer-setup.php && php -r "unlink('composer-setup.php');" && mv composer.phar /usr/local/bin/composer

# Symfony CLI
# RUN wget https://get.symfony.com/cli/installer -O - | bash 
RUN curl -sS https://get.symfony.com/cli/installer | bash && mv /root/.symfony5/bin/symfony /usr/local/bin/symfony
# RUN apt update \
#     && apt install -y zlib1g-dev g++ git libicu-dev zip libzip-dev zip \
#     # && docker-php-ext-install intl opcache pdo pdo_mysql 
#     # && pecl install apcu \
#     # && docker-php-ext-enable apcu \
#     && docker-php-ext-configure zip \
#     && docker-php-ext-install zip

# RUN apt-get update && apt-get install -y libmcrypt-dev \
#     libmagickwand-dev --no-install-recommends 

# RUN apt-get install -y p7zip \
#     p7zip-full \
#     unace \
#     zip \
#     unzip \
#     xz-utils \
#     sharutils \
#     uudeview \
#     mpack \
#     arj \
#     cabextract \
#     file-roller \
#     && rm -rf /var/lib/apt/lists/*
    # && pecl install imagick \
    # && docker-php-ext-enable  
# && docker-php-ext-install mcrypt pdo_mysql


# Install Composer
# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# RUN curl -sS https://get.symfony.com/cli/installer | bash

# RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
# RUN docker-php-ext-install pdo mbstring


# COPY . .
# RUN composer install

# EXPOSE 8000
# CMD php bin/console server:run 127.0.0.1:8000
ENTRYPOINT ["./start.sh"]