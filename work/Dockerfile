FROM ubuntu

MAINTAINER Nipe Setiawan Harefa <nipeharefa@gmail.com>

RUN apt update && apt-get install -y \
	 php php-curl php-cli \ 
	 php-mysql \
	 php-mbstring php-xml php-zip curl vim git
	 
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -

RUN echo "deb http://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt-get install -y nodejs

# Install gulp, bower

# RUN npm install -g npm

# RUN npm i -g gulp

# RUN npm i -g bower

# Install composer and add its bin to the PATH.
RUN curl -s http://getcomposer.org/installer | php && \
    echo "export PATH=${PATH}:/var/www/laravel/vendor/bin" >> ~/.bashrc && \
    mv composer.phar /usr/local/bin/composer
