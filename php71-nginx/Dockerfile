FROM webdevops/php-nginx:7.1

MAINTAINER yir <215766354@qq.com>

WORKDIR /app

COPY . ./
RUN chown -R application ./ \
  && chgrp -R application ./

RUN gosu application composer install
