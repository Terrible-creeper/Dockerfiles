FROM arm64v8/ubuntu:20.04

RUN apt update
RUN apt install -y ca-certificates nginx vim sudo
RUN apt install -y php7.4 php7.4-fpm php7.4-mysql php-common php7.4-cli php7.4-common php7.4-json php7.4-opcache php7.4-readline php7.4-mbstring php7.4-xml php7.4-gd php7.4-curl
RUN useradd -m -d /home/container container
RUN chmod -R 766 /var/log/nginx/error.log;

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

ADD ../entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
