FROM arm64v8/ubuntu:22.04

RUN apt update
RUN apt install -y ca-certificates nginx vim sudo
RUN apt install -y php8.1 php8.1-fpm php8.1-mysql php8.1-cli php8.1-common php8.1-opcache php8.1-readline php8.1-mbstring php8.1-xml php8.1-gd php8.1-curl
RUN useradd -m -d /home/container container

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

ADD ../entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
