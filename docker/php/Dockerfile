FROM adminer:4.6.3-fastcgi
USER root
RUN apk add --no-cache freetds-dev
RUN docker-php-ext-install pdo_dblib
USER adminer
