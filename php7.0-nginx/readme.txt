1 . docker pull docker.io/ubuntu

2 . docker build -t php7-fpm  .

3 . nginx 目录下  docker build -t lara-nginx .

4 . docker run -d --name php -v /home/liucai/adp/adx/:/var/app php7-fpm

5 . docker run -d -p 8080:80 -v /conf/:/etc/nginx/conf.d/ --volumes-from php --link php:php lara-nginx