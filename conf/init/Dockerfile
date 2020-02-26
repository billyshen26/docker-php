FROM composer:latest

#RUN docker-php-ext-install pdo_mysql \
# 	&& docker-php-ext-install mysqli

WORKDIR /var/www/html

#更改国内源
CMD composer config -g repo.packagist composer https://packagist.phpcomposer.com \
&& chmod -R 777 . \
&& composer install \
&& ./think migrate:run \
&& echo "脚本执行完成"