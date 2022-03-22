FROM alpine:3.15.0

RUN apk update && apk add --no-cache python3  py3-pip && \
    pip3 install --upgrade pip   && \
    pip3 install --no-cache-dir awscli  && \
    rm -rf /var/cache/apk/*
RUN wget -O helm-v3.tar.gz https://get.helm.sh/helm-v3.8.1-linux-amd64.tar.gz && \
    tar -zxvf helm-v3.tar.gz && \
    cp linux-amd64/helm /usr/bin/helm && \
    rm -rf linux-amd64 helm-v3.tar.gz

ENTRYPOINT ["helm"]


