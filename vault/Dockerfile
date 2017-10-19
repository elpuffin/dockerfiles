FROM alpine:latest

LABEL maintainer="nostrum@tuta.io"

ENV VERS=0.8.3 

RUN apk update; apk upgrade ;\
  apk add openssl

RUN wget https://releases.hashicorp.com/vault/${VERS}/vault_${VERS}_linux_amd64.zip && \
  unzip vault_${VERS}_linux_amd64.zip && \
  mv vault /usr/local/bin

ENTRYPOINT ["vault", "server", "-dev"]
