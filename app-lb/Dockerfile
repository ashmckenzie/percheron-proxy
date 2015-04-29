FROM proxy_base:1.0.0
MAINTAINER ash@the-rebellion.net

ADD config/haproxy.cfg /etc/haproxy/haproxy.cfg
ADD config/syslog-ng.conf /etc/syslog-ng/conf.d/haproxy.conf
ADD services/haproxy.ini /etc/supervisord.d/haproxy.ini

RUN touch /var/log/haproxy_system.log /var/log/haproxy_access.log

EXPOSE 80

CMD [ "/usr/sbin/supervisord", "-n", "-c", "/etc/supervisord.conf" ]
