FROM alpine

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get -y install nginx

RUN ln -s /etc/nginx/sites-available/localhost /etc/nginx/sites-enabled/

RUN chown -R www-data:www-data /var/www/*
RUN chmod -R 755 /var/www/*

EXPOSE 80 443

COPY ./srcs/nginx/start.sh /var/
CMD bash /var/star.sh
