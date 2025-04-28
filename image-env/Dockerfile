FROM debian:12

ARG APITOKEN_ENV
ARG APIEMAIL_ENV
ARG APIURL_ENV

ENV APITOKEN=${APITOKEN_ENV}
ENV APIEMAIL=${APIEMAIL_ENV}
ENV APIURL=${APIURL_ENV}

WORKDIR /app

COPY ./config/ /app/config/

RUN apt-get update \
    && apt-get install -y gettext \
    && apt-get clean \
    && rm -rf /var/lib/{apt,dpkg,cache,log}/ \
    && envsubst < /app/config/example-settings.env > /app/config/settings.env
