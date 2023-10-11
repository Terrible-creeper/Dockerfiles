# -----------------------------------------------------
# mySQL Image for Pterodactyl
# ARM64v8
# -----------------------------------------------------
FROM        arm64v8/ubuntu:22.04

LABEL       author="Terrible_creeper" maintainer="creeper5620@gmail.com"

ARG         DEBIAN_FRONTEND=noninteractive
ENV         TZ=Etc/UTC

RUN         apt update
RUN         apt install -y netcat php8.1 php8.1-{common,cli,gd,mysql,mbstring,bcmath,xml,fpm,curl,zip} mariadb-server tar unzip git redis-server
RUN         useradd -d /home/container -m container -s /bin/bash

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ../../entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]
