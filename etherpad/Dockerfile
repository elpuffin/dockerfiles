FROM alpine:latest

LABEL mainttainer='nostrum@tuta.io'

RUN ((echo "3th3rp4d";echo "3th3rp4d"))  | adduser etherpad 

RUN apk update && apk upgrade; \
  apk add gzip git curl python openssl-dev nodejs nodejs-npm; \
  git clone git://github.com/ether/etherpad-lite.git;\
  chown -R etherpad. etherpad-lite

RUN cd etherpad-lite; \
  su etherpad -c bin/run.sh
