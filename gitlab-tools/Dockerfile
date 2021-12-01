FROM debian:bullseye-slim

ENV TF_URL "https://releases.hashicorp.com/terraform/1.0.11/terraform_1.0.11_linux_amd64.zip"

RUN apt-get update -qq && apt-get upgrade -y -qq \
    && apt-get install -y -qq \
    openssh-client \
    zip \
    unzip \
    wget \
    && wget -q -P /tmp ${TF_URL} \
    && unzip /tmp/terraform_1.0.11_linux_amd64.zip -d /usr/local/bin \
    && apt clean \
    && rm -rf /var/lib/apt/lists/* \
    && rm -rf /tmp/* \
    && rm -rf /var/cache/apt/archives/* \
    && rm -rf /var/cache/apt/*.bin
