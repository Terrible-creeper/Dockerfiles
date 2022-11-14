FROM arm64v8/ubuntu:20.04

RUN apt update
RUN apt install -y ca-certificates nginx vim sudo
RUN apt -y install php8.1 php8.1-{common,cli,gd,mysql,mbstring,bcmath,xml,fpm,curl,zip,json,opcache,readline}
RUN useradd -m -d /home/container container

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

ADD ../entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
