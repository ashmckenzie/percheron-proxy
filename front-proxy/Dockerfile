FROM proxy_base:1.0.0
MAINTAINER ash@the-rebellion.net

ADD config/nginx.conf /etc/nginx/sites-enabled/front-proxy.conf
ADD services/nginx.ini /etc/supervisord.d/nginx.ini

EXPOSE 80

CMD [ "/usr/sbin/supervisord", "-n", "-c", "/etc/supervisord.conf" ]
