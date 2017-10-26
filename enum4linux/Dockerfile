FROM alpine:latest

LABEL maintainer='nostrum@tuta.io'
ENV VERS=0.8.9

RUN apk update; apk upgrade ;\
  apk add openssl

RUN wget https://labs.portcullis.co.uk/download/enum4linux-${VERS}.tar.gz && \
  tar zxvf enum4linux-${VERS}.tar.gz && \
  cp -pvar enum4linux-${VERS}/enum4linux.pl /usr/local/bin/ && \
  rm -rfv enum4linux-${VERS}

RUN perl /usr/local/bin/enum4linux.pl -h
