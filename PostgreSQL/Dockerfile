FROM ubuntu:20.04

RUN apt-get update
RUN apt-get install -y wget iproute2

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

ADD ./entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
