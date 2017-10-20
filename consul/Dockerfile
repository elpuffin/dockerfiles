FROM alpine:latest

LABEL maintainer="nostrum@tuta.io"

ENV VERS=1.0.0 

RUN apk update; apk upgrade ;\
  apk add openssl

RUN wget https://releases.hashicorp.com/consul/${VERS}/consul_${VERS}_linux_amd64.zip && \
  unzip consul_${VERS}_linux_amd64.zip && \
  mv consul /usr/local/bin

#ENTRYPOINT ["consul", "server", "-dev"]
