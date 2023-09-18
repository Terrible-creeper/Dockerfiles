# -----------------------------------------------------
# mySQL Image for Pterodactyl
# ARM64v8
# -----------------------------------------------------
FROM        arm64v8/ubuntu:22.04

LABEL       author="Terrible_creeper" maintainer="creeper5620@gmail.com"

ARG         DEBIAN_FRONTEND=noninteractive
ENV         TZ=Etc/UTC

RUN         apt update
RUN         apt install -y netcat mysql-server
RUN         useradd -d /home/container -m container -s /bin/bash

USER        container
ENV         USER=container HOME=/home/container
RUN         mkdir /var/log/mysql && chmod 777 /var/log/mysql
WORKDIR     /home/container

COPY        ../../entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]
