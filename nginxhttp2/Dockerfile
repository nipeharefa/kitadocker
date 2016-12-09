FROM ubuntu:16.04

ARG PHP_UPSTREAM=php-fpm

RUN apt update && apt install vim nginx -y

# ADD nginx.conf /etc/nginx/
# COPY sites/*.conf /etc/nginx/sites-available/
# COPY mirrors.list /etc/apt/sources.list.d


# RUN echo "upstream php-upstream { server ${PHP_UPSTREAM}:9000; }" > /etc/nginx/conf.d/upstream.conf

# RUN usermod -u 1000 www-data


EXPOSE 80 443
