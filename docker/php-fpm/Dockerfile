FROM bitnami/php-fpm

RUN apt-get update
RUN apt-get install -y \
    curl \
    bash

RUN echo "$(curl -sS https://composer.github.io/installer.sig) -" > composer-setup.php.sig \
        && curl -sS https://getcomposer.org/installer | tee composer-setup.php | sha384sum -c composer-setup.php.sig \
        && php composer-setup.php && rm composer-setup.php* \
        && chmod +x composer.phar && mv composer.phar /usr/bin/composer

CMD ["php-fpm", "-F"]

WORKDIR /app
EXPOSE 9000