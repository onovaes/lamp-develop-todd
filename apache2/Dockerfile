FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    zip \
    apt-utils \
    curl \
    # Install git
    git \
    # Install apache
    apache2 \
    # Install php 7.2
    libapache2-mod-php7.2 \
    php7.2-cli \
    php7.2-json \
    php7.2-curl \
    php7.2-fpm \
    php7.2-gd \
    php7.2-ldap \
    php7.2-mbstring \
    php7.2-mysql \
    php7.2-soap \
    php7.2-sqlite3 \
    php7.2-xml \
    php7.2-zip \
    php7.2-intl \
    php-imagick \
    php-xdebug \
    # Install tools
    openssl \
    nano \
    graphicsmagick \
    imagemagick \
    ghostscript \
    mysql-client \
    iputils-ping \
    locales \
    sqlite3 \
    ca-certificates \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Set locales
RUN locale-gen en_US.UTF-8

# Configure PHP for php-laravel.ini
COPY php.ini /etc/php/7.2/apache2/php.ini
RUN a2enmod rewrite 

# Configure vhost for site
COPY site.conf /etc/apache2/sites-available/
RUN a2dissite 000-default
RUN a2ensite site.conf

EXPOSE 80 443

WORKDIR /var/www/html

RUN rm index.html

#HEALTHCHECK --interval=5s --timeout=3s --retries=3 CMD curl -f http://localhost || exit 1

# Install composer AND Laravel
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN composer global require laravel/installer
ENV PATH="~/.composer/vendor/bin:$PATH"

#STARTA O APACHE
CMD apachectl -D FOREGROUND 