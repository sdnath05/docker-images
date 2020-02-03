FROM php:7.2-fpm

RUN apt-get update && apt-get install -y curl libcurl4-gnutls-dev libxml2-dev libxslt-dev libfreetype6-dev libjpeg62-turbo-dev libpng-dev zip

RUN docker-php-ext-install curl mysqli zip gd xml bcmath mbstring soap json iconv xsl intl pdo pdo_mysql opcache

# RUN docker-php-ext-enable mysqli pdo zip gd curl mysqli dom xml bcmath xml mbstring soap zip json iconv xsl intl pdo_mysql

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php -r "if (hash_file('sha384', 'composer-setup.php') === 'c5b9b6d368201a9db6f74e2611495f369991b72d9c8cbd3ffbc63edff210eb73d46ffbfce88669ad33695ef77dc76976') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
Run php composer-setup.php
Run php -r "unlink('composer-setup.php');"

# all possible php extentions

# bcmath bz2 calendar ctype curl dba dom enchant exif fileinfo filter ftp gd gettext gmp hash iconv imap interbase intl json ldap mbstring mysqli oci8 odbc opcache pcntl pdo pdo_dblib pdo_firebird pdo_mysql pdo_oci pdo_odbc pdo_pgsql pdo_sqlite pgsql phar posix pspell readline recode reflection session shmop simplexml snmp soap sockets sodium spl standard sysvmsg sysvsem sysvshm tidy tokenizer wddx xml xmlreader xmlrpc xmlwriter xsl zend_test zip

# CMD ["-p","9000:9000"]