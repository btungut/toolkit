FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
RUN echo "APT::Get::Assume-Yes \"true\";" > /etc/apt/apt.conf.d/90assumeyes

RUN apt-get update

RUN apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    jq \
    git \
    libssl1.0

RUN apt-get install -y --no-install-recommends \
    netcat \
    wget \
    unzip \
    telnet \
    iotop \
    iftop \
    htop \
    dnsutils \
    iputils-ping \
    traceroute \
    iperf3

#nginx web server
RUN apt-get install -y --no-install-recommends nginx
RUN rm -rf /var/www/html/*
COPY index.html /var/www/html/index.html
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
CMD [ "/entrypoint.sh" ]
