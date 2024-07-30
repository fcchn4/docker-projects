FROM debian:12

RUN apt-get update -qq \
    && apt-get upgrade -y -qq \
    && apt-get install -y -qq iputils-ping telnet vim iproute2 nmap curl \
    && apt-get clean \
    && rm -rf /var/cache/apt/*
