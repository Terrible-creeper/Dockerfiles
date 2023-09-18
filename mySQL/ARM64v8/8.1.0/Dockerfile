# -----------------------------------------------------
# mySQL Image for Pterodactyl
# ARM64v8
# -----------------------------------------------------
FROM        arm64v8/mysql:8.1.0

LABEL       author="Terrible_creeper" maintainer="creeper5620@gmail.com"

ENV         DEBIAN_FRONTEND noninteractive

RUN         apt update -y
RUN         apt install -y netcat
RUN         useradd -d /home/container -m container -s /bin/bash

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ../../entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]
