FROM centos:latest

LABEL maintainer='nostrum@tuta.io'

RUN adduser etherpad

RUN curl --silent --location https://rpm.nodesource.com/setup_6.x | bash -

RUN yum update -y && \
  yum install -y \
  gzip git curl python \
  openssl-devel nodejs && \
  yum -y groupinstall "Development Tools" && \
  yum clean all

USER etherpad

WORKDIR /home/etherpad

RUN git clone git://github.com/ether/etherpad-lite.git

COPY settings.json etherpad-lite/settings.json

WORKDIR /home/etherpad/etherpad-lite

ENTRYPOINT ["bin/run.sh"]
