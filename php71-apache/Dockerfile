FROM php:7.1-apache

MAINTAINER wesom.wang@gmail.com

RUN apt-get update \
  && apt-get install -y \
    curl \
    git \
    libmcrypt-dev \
    libz-dev \
    libpcre3-dev

RUN docker-php-ext-install \
    mcrypt \
    pdo_mysql \
    mbstring \
    zip \
  && apt-get clean \
  && apt-get autoclean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN curl -sS https://getcomposer.org/installer \
  | php -- --install-dir=/usr/local/bin --filename=composer \
  && echo "ServerName localhost" >> /etc/apache2/apache2.conf \
  && a2enmod rewrite

