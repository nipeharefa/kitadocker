FROM nginx:latest

ARG PHP_UPSTREAM=php-fpm

RUN apt update
ADD nginx.conf /etc/nginx/
COPY sites/*.conf /etc/nginx/sites-available/

RUN rm /etc/nginx/conf.d/default.conf
RUN echo "upstream php-upstream { server ${PHP_UPSTREAM}:9000; }" > /etc/nginx/conf.d/upstream.conf

RUN usermod -u 1000 www-data


EXPOSE 80