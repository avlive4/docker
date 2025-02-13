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
    kea-dhcp4-server

WORKDIR /etc/kea

COPY kea-dhcp4.conf /etc/kea/kea-dhcp4.conf

EXPOSE 67/udp

CMD ["kea-dhcp4", "-c", "/etc/kea/kea-dhcp4.conf"]