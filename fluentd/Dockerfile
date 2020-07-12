FROM fluent/fluentd:v1.11-debian-armhf-1
LABEL maintainer "mi2428 <tmiya@protonmail.ch>"

ENV LANG C.UTF-8

USER root

# hadolint ignore=DL3018,DL3028
#RUN apk add --no-cache --update mariadb-connector-c \
# && apk add --no-cache --update --virtual .build-deps \
#      build-base ruby-dev mariadb-dev mariadb-connector-c \
RUN apt-get update \
 && apt-get install -y build-essential ruby-dev libmariadb-dev \
 && gem install fluent-plugin-http-heartbeat \
 && gem install fluent-plugin-mysql \
 && gem sources --clear-all \
 && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem

COPY fluent.conf /fluentd/etc/

USER fluent
