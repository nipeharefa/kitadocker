FROM ubuntu

MAINTAINER Nipe Setiawan Harefa <nipeharefa@gmail.com>

RUN apt update && install --force-yes \
	 php php-curl php-cli \ 
	 php-mysql \
	 php-mbstring php-xml php-zip curl vim git
	 
RUN curl -sL https://deb.nodesource.com/setup_4.x | bash -

RUN apt-get install -y nodejs

# Install gulp, bower
RUN npm i -g bower gulp npm

# Install composer and add its bin to the PATH.
RUN curl -s http://getcomposer.org/installer | php && \
    echo "export PATH=${PATH}:/var/www/laravel/vendor/bin" >> ~/.bashrc && \
    mv composer.phar /usr/local/bin/composer