FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive
RUN echo "APT::Get::Assume-Yes \"true\";" > /etc/apt/apt.conf.d/90assumeyes

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    jq \
    git \
    iputils-ping \
    libcurl4 \
    libicu60 \
    libunwind8 \
    netcat \
    libssl1.0 \
  && rm -rf /var/lib/apt/lists/*

RUN apt-get update && apt-get install -y --no-install-recommends \
    wget \
    unzip \
    telnet \
    iotop \
    iftop \
    htop \
    iputils-ping

RUN wget https://github.com/mikefarah/yq/releases/download/v4.25.1/yq_linux_amd64 \
    && mv ./yq_linux_amd64 /usr/bin/yq \
    && chmod +x /usr/bin/yq

RUN wget https://github.com/PowerShell/PowerShell/releases/download/v7.2.4/powershell-lts_7.2.4-1.deb_amd64.deb \
    && dpkg -i powershell-lts_7.2.4-1.deb_amd64.deb \
    && apt-get install -f