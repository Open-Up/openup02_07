FROM monsantoco/min-jessie:latest

RUN apt-get update
RUN apt-get install -y nginx

COPY wp-site.conf /etc/nginx/sites-enabled/default

RUN touch /var/log/nginx/wp.log

ENTRYPOINT /etc/init.d/nginx start && tail -f /var/log/nginx/wp.log
