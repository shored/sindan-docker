FROM php:7.4-apache
LABEL maintainer "Tomohiro Ishihara <sho@wide.ad.jp>"

ENV LANG C.UTF-8

USER root

# hadolint ignore=DL3018,DL3028
#RUN apt-get update \
# && apt-get install -y build-essential

COPY sindan-client-setting .
