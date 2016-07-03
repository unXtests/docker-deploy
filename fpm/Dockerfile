FROM php:7-fpm-alpine

MAINTAINER Bruno Cascio <brunocascio@gmail.com>

RUN chown -R www-data:www-data /var/www/html \
  && sed -ri 's/^www-data:x:82:82:/www-data:x:1000:50:/' /etc/passwd

ADD ./unlp.ini /usr/local/etc/php/conf.d
ADD ./unlp.pool.conf /usr/local/etc/php-fpm.d/

RUN docker-php-ext-install pdo pdo_mysql
