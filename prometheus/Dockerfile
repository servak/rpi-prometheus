FROM resin/rpi-raspbian:latest
MAINTAINER Kakuya Ando <ando.kakuya@gmail.com>

RUN apt-get update \
  && apt-get install -y wget \
  && wget https://github.com/prometheus/prometheus/releases/download/v1.6.1/prometheus-1.6.1.linux-armv7.tar.gz \
  && tar zxvf prometheus-1.6.1.linux-armv7.tar.gz \
  && cp prometheus-1.6.1.linux-armv7/prometheus /usr/local/bin/ \
  && chmod 755 /usr/local/bin/prometheus

COPY prometheus.yml /etc/prometheus.yml

ENTRYPOINT ["/usr/local/bin/prometheus", "-config.file=/etc/prometheus.yml"]

EXPOSE 9090
