FROM arm64v8/nginx

RUN apt-get update

COPY static-html-directory /usr/share/nginx/html

USER container
ENV USER=container HOME=/home/container
WORKDIR /home/container

ADD ./entrypoint.sh /entrypoint.sh
CMD [ "/bin/bash", "/entrypoint.sh" ]
