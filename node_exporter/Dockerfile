FROM resin/rpi-raspbian:latest
MAINTAINER Kakuya Ando <ando.kakuya@gmail.com>

RUN apt-get update \
  && apt-get install -y wget \
  && wget https://github.com/prometheus/node_exporter/releases/download/v0.14.0/node_exporter-0.14.0.linux-armv7.tar.gz \
  && tar zxvf node_exporter-0.14.0.linux-armv7.tar.gz \
  && cp node_exporter-0.14.0.linux-armv7/node_exporter /usr/local/bin/ \
  && chmod 755 /usr/local/bin/node_exporter

ENTRYPOINT ["/usr/local/bin/node_exporter"]

EXPOSE 9100
