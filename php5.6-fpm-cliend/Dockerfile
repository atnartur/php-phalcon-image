FROM php:5.6-fpm

MAINTAINER Artur Atnagulov <i@atnartur.ru>

RUN apt-get update && \
	apt-get install -y --no-install-recommends \
		libcurl4-gnutls-dev \ 
		zlib1g-dev \
		git \
		mysql-client \
		libmysqlclient-dev \
		php5-mysqlnd && \
	docker-php-ext-install \
		pdo_mysql \
		curl \
		mysqli \
		zip && \
	apt-get clean && \
	rm -r /var/lib/apt/lists/*

RUN docker-php-ext-enable mysqli 