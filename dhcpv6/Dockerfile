FROM debian:latest

RUN apt-get update && apt-get install -y \
    build-essential \
    libboost-all-dev \
    libpcap-dev \
    libxml2-dev \
    mariadb-client \
    curl \
    wget \
    bash \
    kea-dhcp6-server

WORKDIR /etc/kea

COPY kea-dhcp6.conf /etc/kea/kea-dhcp6.conf

EXPOSE 547/udp

CMD ["kea-dhcp6", "-c", "/etc/kea/kea-dhcp6.conf"]