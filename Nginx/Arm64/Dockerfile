FROM arm64v8/ubuntu:20.04

RUN apt update
RUN apt install -y ca-certificates nginx
RUN apt install php7.4 php7.4-{fpm,mysql,common,cli,common,json,opcache,readline,mbstring,xml,gd,curl}
RUN useradd -m -d /home/container container

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

ADD ../entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
