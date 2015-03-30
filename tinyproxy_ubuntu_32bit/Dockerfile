# Tinyproxy

# VERSION 1.0.0

FROM intersoftlab/ubuntu:14.04-i386

MAINTAINER pgeraghty

RUN \
  echo "deb http://archive.canonical.com/ubuntu trusty partner" > /etc/apt/sources.list.d/partner.list && \
  apt-get update && \
  apt-get upgrade -y && \

  apt-get install -y tinyproxy && \

  apt-get autoremove -y && \
  apt-get clean all

# allow all connections
RUN sed -i -e"s/^Allow /#Allow /" /etc/tinyproxy.conf
RUN mkdir -p /var/run/tinyproxy/ && chmod 777 /var/run/tinyproxy/

USER nobody
EXPOSE 8888

# Default command
ENTRYPOINT ["/usr/sbin/tinyproxy"]
CMD ["-d"]
