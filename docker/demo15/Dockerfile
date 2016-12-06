From nginx
MAINTAINER "James Lee <cjlee8110@gmail.com>"

USER root

RUN apt-get update && \
    apt-get install -y vim

WORKDIR /usr/share/nginx/html

COPY ./index.html ./
COPY ./images/NUTC_cloud.png ./images/NUTC_cloud.png
