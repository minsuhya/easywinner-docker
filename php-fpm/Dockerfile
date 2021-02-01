# FROM ubuntu:18.04
# MAINTAINER your_name "email@gmail.com"
# RUN apt-get update -y
# RUN apt-get install -y python-pip python-dev build-essential
# COPY . /app
# WORKDIR /app
# RUN pip install -r requirements.txt
# ENTRYPOINT ["python"]
# CMD ["app.py"]


FROM php:7.3-fpm
MAINTAINER rupi "rupi@nemo-c.com"

RUN apt-get update
RUN apt-get install -y libz-dev libmemcached-dev libpng-dev libjpeg-dev && \
    pecl install memcached && \
    docker-php-ext-enable memcached
RUN docker-php-ext-install gd mysqli pdo pdo_mysql && docker-php-ext-enable gd mysqli pdo pdo_mysql
