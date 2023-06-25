FROM thideki/alpine-laravel9:init

RUN apk update
RUN apk add php8-pear php8-dev linux-headers autoconf
RUN pecl install xdebug
RUN echo -e "\n[xdebug] \nxdebug.client_host=host.docker.internal \nxdebug.client_port=9003 \nxdebug.start_with_request=yes \nxdebug.mode=debug \n" >> /etc/php8/php.ini
RUN sed -i 's/;zend_extension=opcache/zend_extension="xdebug.so"/g' /etc/php8/php.ini