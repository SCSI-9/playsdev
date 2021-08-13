FROM ubuntu:20.04
#Install nginx
RUN  apt-get update
RUN  apt-get install nginx -y
#RUN  apt install apache2 libapache2-mod-fcgid -y
#RUN  apt install software-properties-common -y
#RUN  add-apt-repository ppa:ondrej/php -y
#RUN  apt-get update -y
#RUN  apt install php7.3 php7.3-fpm -y



#Add the customized NGINX configuration
RUN rm -f /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf
RUN mkdir -p /var/www/html/web1
#RUN mkdir -p /var/www/html/web2
RUN mkdir -p /var/www/html/web3
RUN mkdir -p /var/www/html/web4

COPY web1/index.html /var/www/html/web1/index.html
COPY web4/info.php /var/www/html/web4/info.php
COPY web3/index.html /var/www/html/web3/index.html
#COPY nginx/web1/2021.07.09-garage.mp3 /var/www/html/web1/2021.07.09-garage.mp3

COPY ["start.sh", "/root/start.sh"]
WORKDIR /root
CMD ["./start.sh"]


