FROM nginx:latest

ARG PHP_UPSTREAM=php-fpm

RUN apt update && apt install vim -y

ADD nginx.conf /etc/nginx/
COPY sites/*.conf /etc/nginx/sites-available/
COPY mirrors.list /etc/apt/sources.list.d


RUN rm /etc/nginx/conf.d/default.conf
RUN echo "upstream php-upstream { server ${PHP_UPSTREAM}:9000; }" > /etc/nginx/conf.d/upstream.conf

RUN usermod -u 1000 www-data

# RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 40976EAF437D05B5


EXPOSE 80 443