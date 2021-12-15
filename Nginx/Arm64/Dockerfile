FROM arm64v8/ubuntu:20.04

RUN apt-get update -y
RUN apt-get install -y nginx

ENV USER=container HOME=/home/container
USER container
WORKDIR /home/container
RUN mkdir /home/container/html
RUN echo "Nginx" >> index.html

COPY ../nginx.conf /home/container

ADD ./entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
