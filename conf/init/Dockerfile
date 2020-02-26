FROM composer:latest

#RUN docker-php-ext-install pdo_mysql \
# 	&& docker-php-ext-install mysqli

WORKDIR /var/www/html

#更改国内源
CMD composer config -g repo.packagist composer https://packagist.phpcomposer.com

#更改权限
CMD chmod -R 777 .

#安装组件
CMD composer install

#数据迁移
CMD ./think migrate:run

CMD echo "脚本执行完成"