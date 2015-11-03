FROM alpine:3.2
MAINTAINER P. Barrett Little <barrett@barrettlittle.com> (@pblittle)

# Set default Logstash version
ENV RSYSLOG_VERSION 8.14

ENV PATH ${ES_HOME}/bin:$PATH

RUN apk add --update \
        bash \
        rsyslog && \
    rm -rf /var/cache/apk/*

ADD rsyslog.conf /etc/rsyslog.conf

CMD /usr/sbin/rsyslogd -n
