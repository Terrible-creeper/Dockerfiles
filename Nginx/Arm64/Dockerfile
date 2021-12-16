FROM arm64v8/ubuntu:20.04

RUN apt update \
    && apt install -y ca-certificates nginx \
    && apt install -y php7 php7-{fpm,mcrypt,soap,openssl,gmp,pdo_odbc,json,dom,pdo,zip,mysqli,sqlite3,apcu,pdo_pgsql,bcmath,gd,odbc,pdo_mysql,pdo_sqlite,gettext,xmlreader,xmlrpc,bz2,iconv,pdo_dblib,curl,ctype,phar,fileinfo,mbstring,tokenizer}  \
    && useradd -m -d /home/container container

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

ADD ../entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
