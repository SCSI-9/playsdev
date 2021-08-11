FROM ubuntu:18.04

RUN apt update -y
RUN apt install apache2 -y

COPY /web4/info.php /var/www/html/info,php
COPY ./start.sh  /root/start.sh

WORKDIR /root
CMD ["./start.sh"]

