FROM alpine:3.2
MAINTAINER P. Barrett Little <barrett@barrettlittle.com> (@pblittle)

ENV RSYSLOG_VERSION 8.14

RUN apk add --update \
        bash \
        rsyslog && \
    rm -rf /var/cache/apk/*

ADD rsyslog.conf /etc/rsyslog.conf

VOLUME /var/log
VOLUME /var/spool/rsyslog

EXPOSE 514
EXPOSE 514/udp

CMD /usr/sbin/rsyslogd -n
