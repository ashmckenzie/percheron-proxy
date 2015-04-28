FROM base/archlinux:latest
MAINTAINER ash@the-rebellion.net

ENV TERM ansi

RUN pacman-key --refresh-keys
RUN pacman -yS --noconfirm syslog-ng supervisor nginx haproxy netcat
RUN pacman -Sc --noconfirm

ADD config/nginx.conf /etc/nginx/nginx.conf
ADD config/supervisord.conf /etc/supervisord.conf
ADD config/syslog-ng.conf /etc/syslog-ng/syslog-ng.conf
ADD services/syslog-ng.ini /etc/supervisord.d/syslog-ng.ini

RUN mkdir -p /etc/nginx/sites-enabled /etc/supervisord.d /etc/syslog-ng/conf.d
