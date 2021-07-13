FROM php:7.4-fpm-alpine
RUN echo "http_proxy: $http_proxy | https_proxy: $https_proxy | no_proxy: $no_proxy"

COPY *.crt /usr/local/share/ca-certificates/
RUN update-ca-certificates

RUN apk update && apk upgrade
RUN apk add bash
RUN apk add wget
RUN wget --version

RUN curl https://example.com
RUN wget https://example.com

COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer
RUN composer init --name foo/bar
RUN composer require symfony/string