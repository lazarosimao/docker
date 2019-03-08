FROM php:5.6-apache

# install apache modules
RUN a2enmod headers \
 && a2enmod rewrite

RUN apt-get update && apt-get install -y libmemcached-dev zlib1g-dev \
	&& pecl install memcached-2.2.0 \
	&& docker-php-ext-enable memcached \
	&& docker-php-ext-install mysqli \
	&& docker-php-ext-enable mysqli